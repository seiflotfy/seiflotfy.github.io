---
layout: post
title: Counting flows (Semi-evaluation of CMS, CML and PMC)
date: '2015-08-31 22:25:58'
tags:
- go
- algorithms
- big-data
---

Assume we have a stream of events coming in one at a time, and we need to count the frequency of the different types of events in the stream.

*In other words:
We are receiving fruits one at a time in no given order, and at any given time we need to be able to answer how many of a specific fruit did we receive.*

The most naive implementation is a dictionary in the form of ```<string, int>```, and is most accurate and suitable for streams with limited types of events.

Let us assume a unique item consists of 15 bytes and has a dedicated uint32 (4 bytes) counter assigned to it.

At 10 million unique items we end up using 19 MB which is a bit much, but on the plus side its as accurate as it gets.

But what if we don't have the 19 MB. Or what if we have to keep track of several streams?

Maybe saving to a DB? Well when querying the DB upon request, something in the lines of:

`SELECT count(event) WHERE event = ?)`

The more items we add, the more resource intensive the query becomes.

Thankfully solutions come in the form of [Probabalistic datastructures (sketches)](https://highlyscalable.wordpress.com/2012/05/01/probabilistic-structures-web-analytics-data-mining/).

I won't get into details but to solve this problem I semi-evaluated the following data structures:

* Count-Min sketch (CMS) [[1]](https://en.wikipedia.org/wiki/Count–min_sketch)[[2]](http://dimacs.rutgers.edu/~graham/pubs/papers/cmencyc.pdf)
* Count-Min-Log sketch (CML) [[1]](http://iswag-symposium.org/2015/pdfs/shortpaper1.pdf)[[2]](http://blog.guillaume-pitel.fr/2014/11/count-min-log-sketch-for-on-low-frequency/)
* Probabilistic Multiplicity Counting sketch (PMC) [[1]](https://wwwcn.cs.uni-duesseldorf.de/publications/publications/library/Lieven2010a.pdf)

Test details:

For each sketch I linearly added a new flow with equivalently linear events. So the first flow got 1 event inserted. The second flow for 2 events inserted, all the way up to 10k-th flow with 10k events inserted.

```
flow 1: 1 event
flow 2: 2 events
...
flow 10000: 10000 events
```
All three data structures were configured to have a size of 217KB (exactly 1739712 bits). 

A couple dozen runs yielded the following results (based on my unoptimized code esp. for PMC and CML)

```
CMS: 07s for 50005000 insertion (fill rate: 31%)
CML: 42s for 50005000 insertion (fill rate: 09%)
PMC: 18s for 50005000 insertion (fill rate: 54%)
```

CMS with ɛ: 0.0001, δ: 0.99 ([code](https://github.com/tylertreat/BoomFilters/blob/master/countmin.go)) ![CMS](https://dl.dropboxusercontent.com/u/7162902/cms.png)

Observe the biased estimation of CMS. CMS will never underestimate. In our case looking at the top border of the diagram we can see the there was a lot of overestimation.


CML with ɛ: 0.000025, δ: 0.99 (16-bit counters)  ([code](https://github.com/seiflotfy/count-min-log))![CML](https://dl.dropboxusercontent.com/u/7162902/cml.png)

Just like CMS, CML is also biased and will never underestimate. However unlike CMS the top border of the diagram is less noisy. Yet accuracy seems to be decreasing for the high counting flows.

PMC with (256x32) virtual metrices ([code](https://github.com/seiflotfy/pmc)) ![PMC](https://dl.dropboxusercontent.com/u/7162902/pmc.png) 

Unlike the previous two sketches. This sketch is unbiased, so underestimations exist. Also the estimate flow count increases with the actual flow count (linearly bigger errors). The drawback here is that PMC gets filled up very quickly which means at some point it will just have everything overestimated. It is recommended to know what the max num of different flows will be beforehand.

Bringing it all together ![ALL] (https://dl.dropboxusercontent.com/u/7162902/all.png)

So what do you think. If you are familiar with these algorithms or can propose a different benchmarking scenario, please comment. I might be able to work on that on a weekend. The code was all written in Go, feel free to suggest optimizations of fix any bugs found (links above respective plots).


