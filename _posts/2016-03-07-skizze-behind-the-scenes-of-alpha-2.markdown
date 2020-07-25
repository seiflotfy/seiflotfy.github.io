---
layout: post
title: 'Skizze: Behind the Scenes of Alpha 2'
featured: true
date: '2016-03-07 19:40:57'
tags:
- big-data
- data-science
- data-engineering
- iot
---

Based on the feedback we got for our [initial alpha release](http://seif.codes/skizze-a-probabilistic-data-structures-service-and-storage/), we worked on improving [Skizze](https://github.com/skizzehq/skizze) and moving the project forward.

To recap, Skizze is a sketch data store to deal with all problems around counting and sketching using probabilistic data-structures.

My old time hacking buddy [Neil Patel](https://twitter.com/njpatel), who is also [Xamarin Insights](http://xamarin.com/insights) Technical Lead and Architect, [blogged](https://njp.io/skizze-alpha-release/) about the latest release, and also provided some background on why Skizze exists, and how to get started.

This second alpha focuses mainly on improving development and operating experience. It is an early alpha so don't expect much, but hopefully now it is easier to run and experiment with.
In this post I wanted to highlight a couple of features and ideas we have for Skizze:

### Domains

As Neil mentioned in his post, we have a clear definition of Domains now:

<blockquote style="font-size: 13px;"> One of the first pieces of feedback we got with the initial release was: "My data needs all four Sketches and I'm sending the values four times to the server!". Which is a fair point, in most cases the stream of values you have, you almost always want all four kinds of questions answered. Domains help solve this problem.
When you create a Domain, behind the scenes, Skizze creates all four sketches of the same name. From then on, as you add values to that domain, they automatically get multiplexed into each Sketch that belongs to it.
</blockquote>

Here is a small Mockup of how flow looks like.
![](/content/images/2016/08/Skizze.png)

### Persistence
One of the main new features is the introduction of an initial functioning **persistence** functionality, which is done via AOF (Append Only File) [inspired by Redis](https://redislabs.com/ebook/redis-in-action/part-2-core-concepts-2/chapter-4-keeping-data-safe-and-ensuring-performance/4-1-persistence-options/4-1-2-append-only-file-persistence):

<blockquote style="font-size: 13px;">In basic terms, append-only log files keep a record of data changes that occur by writing each change to the end of the file. In doing this, anyone could recover the entire dataset by replaying the append-only log from the beginning to the end - 
<footer>— <a href="https://redislabs.com/ebook/redis-in-action/part-2-core-concepts-2/chapter-4-keeping-data-safe-and-ensuring-performance/4-1-persistence-options/4-1-2-append-only-file-persistence#sthash.NgLjrHQq.dpuf">Redis-Labs: 4.1.2 Append-only file persistence</a>
</blockquote>

In our case we record all incoming (write) requests (serialised protobuf) to the AOF. This is all done in a go routine.
Upon restart we replay them again. Currently this might be a bit slow, which is why we intend to add support for snapshotting to allow quicker startup/restoring.

While we do intend to add clustering in the future, for now we are focusing on making [Skizze](https://github.com/skizzehq/skizze) work reliably on one machine. All feedback or support on implementing better persistence is welcome. 

### Initial throughput benchmarks
We also focused on improving the throughput complexity/speed. Thanks to [Damian Gryski](https://github.com/dgryski/)'s tips, this was achieved by using:

* [faster hashing algorithms](https://github.com/dgryski/go-farm)
* [faster random number generators](https://github.com/dgryski/go-pcgr)
* [smarter multi-hashing tricks](http://www.eecs.harvard.edu/~michaelm/postscripts/rsa2008.pdf).

And although often when working in a high-throughput environment, beefier machines are expected, benchmarking on a standard low tier VM offering should be a good reference point. To benchmark our throughput speed we used the lowest Digital Ocean Tier (5$/month) </td>
<table style="width:100%">
  <tr>
    <td><b>Memory</b></td>
    <td>512MB Ram</td>
  </tr>
  <tr>
    <td><b>Disk</b></td>
    <td>20GB SSD</td>
  </tr>
  <tr>
    <td><b>OS</b></td>
    <td> Ubuntu 14.04</td>
  </tr>
  <tr>
    <td><b>CPU</b></td>
    <td> Intel(R) Xeon(R) CPU E5-2630L v2 @ 2.40GHz (1Core)</td>
  </tr>
</table>
<p>
Our benchmark scenario is 1 Domain with 4 sketches, CML, BloomFilter, Top-K (tracking the top 100) and HyperLogLog++ (disregards the expected capacity). The error rate is set to 1% with an expected 1000000 values capacity. The domain is subject to **10 million** insertions (**unique: 349902**) in a **Zipf (1.1)** distribution. The following are our insertions benchmark results.

<table style="width:100%">
  <tr>
    <td><b>batch size</b></td>
    <td><b>elapsed time</b></td> 
    <td><b>values per second</b></td>
  </tr>
  <tr>
    <td>1000</td>
    <td>34s</td> 
    <td>285714</td>
  </tr>
  <tr>
    <td>10000</td>
    <td>29s</td> 
    <td>333333</td>
  </tr>
  <tr>
    <td>100000</td>
    <td>26s</td> 
    <td>370370</td>
  </tr>
</table>

We will be attempting to improve the throughput with every release.
I will follow up with a blog post on the "querying" accuracy, speed and resource consumption soon.


### What's next?

There is still a lot to be done, and we appreciate every kind of support. For the next alpha #3 release we are focusing on:

* **Adding support for Snapshots**: have snapshots of the sketches dumped to disk (while clearing the AOF), so upon restart the sketches are loaded from disk, and the delta is replayed from AOF
* **Threshold functionality**: providing 100% accuracy as long as capacity under specific threshold..
* **Improving AOF**: increase AOF read and write speed.
* **Fix bugs**: there are always bugs to fix. :D

For alpha #n we are playing with the following ideas:

* **Histograms**: by automatically partitioning sketches and domains in intervals we can answer frequency, cardinality and memberships queries via merging over the sketches for a given time range. In some cases like the Count-Min-Sketch we will be using [Hokusai](http://www.auai.org/uai2012/papers/231.pdf) concept for histograms.
* **Metrics**: unlike domains which can only deal with "strings" metrics will be similar but dealing with "numbers". We want to introduce t-digest, running means, running medians, etc...

### Shout outs!

A big thank you to this release's contributors:

* [Martin Pinto](http://github.com/martinpinto)
* [Arne Bahlo](https://arne.me)
* [Manuel Barkhau](http://github.com/mbarkhau)

Please feel free to open an [issue](https://github.com/skizzehq/skizze/issues), or join us for a chat in our channel on the [Gophers Slack](https://blog.gopheracademy.com/gophers-slack-community/) on **#skizze**.

