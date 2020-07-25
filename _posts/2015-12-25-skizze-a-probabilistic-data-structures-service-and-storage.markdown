---
layout: post
title: Skizze - A probabilistic data-structures service and storage (Alpha)
date: '2015-12-25 09:53:21'
tags:
- kde
- go
- algorithms
- big-data
---

At my [day job](https://xamarin.com/insights) we deal with a lot of incoming data for our product, which requires us to be able to calculate histograms and other statistics on the data-stream as fast as possible.

One of the best tools for this is Redis, which will give you 100% accuracy in O(1) (except for its [HyperLogLog](https://en.wikipedia.org/wiki/HyperLogLog) implementation which is a probabilistic data-structure). All in all Redis does a great job.
The problem with Redis for me personally is that, when using it for 100 of millions of counters, I could end up with Gigabytes of memory.

I also tend to use [Top-K](http://rank.cs.columbia.edu), which is not implemented in Redis but via Lua scripting can be built on top of the ZSet data-structure. The Top-K data-structure is used to keep track of the top "k" heavy hitters in a stream without having to keep track all "n" flows (k < n), with a O(1) complexity.

Anyhow, dealing with a massive amount of data the interest is most of the time in heavy hitters, that could be estimated while using less memory with an O(1) complexity for reading and writing (that is if you don't care about a count being 124352435 or 124352011 because on the UI of an app you will be showing "over 124 Million"). 

There are a lot of algorithms floating around and used to solve counting, frequency, membership and top-k problems, which in practice are implemented and used as part of a data-stream pipeline where stuff is counted, merged then stored.

**I couldn't find a one-stop-shop service to fire & forget my data at.**

Basically in need of a solution where I can set up sketches to answer cardinality, frequency, membership as well as ranking queries about my data-stream (without having to reimplement the algorithm in a pipeline embedded in storm, spark, etc...) led to the development of **Skizze** (which is in alpha state).

##What is Skizze?

**[Skizze](https://github.com/seiflotfy/skizze)** ([ˈskɪt͡sə]: german for sketch) is a probabilistic data-structures (sketch) service & store to deal with all problems around counting and sketching using probabilistic data-structures. (https://github.com/seiflotfy/skizze)

Unlike a Key-Value store, Skizze does not store values, but rather appends values to sketches, to solve frequency and cardinality queries in near O(1) time, with minimal memory footprint.

##Which data structures are supported?
Currently the following data structures are supported:

- **HyperLogLog++** to query cardinality of values in the sketch.
- **Count-Min-Log Sketch** to query frequency of values in the sketch.
- **Top-K** to list the top k values in the sketch.
- **Bloom Filter** query membership of a value in the sketch.
- **Dictionary** to 100% accurately query membership and frequency of values in the sketch.

##What are upcoming data structures
Soon we intend to implement/integrate the following sketches:

* [**Count-min Sketch**](https://github.com/dustin/go-probably) frequency counting with merging ability
* [**Hokusai**](https://github.com/dgryski/hokusai) the exponential histogram extension to Count-min Sketch
* [**Probabilistic Multiplicity Counting**](https://github.com/seiflotfy/pmc) similar to Count-min Sketch
* [**Self-learning Bitmaps**](https://github.com/seiflotfy/s-bitmap) cardinality counting like HLL++

##How to use?
Skizze runs as a single service for now, and exposes a [Restful API](https://github.com/seiflotfy/skizze/blob/master/docs/API.md).

##Who helped out?
I'd like to thank the following contributors who helped develop this project:

* [Manuel Barkhau](https://github.com/mbarkhau/) (coding all over the place)
* [Martin Pinto-Bazurco](https://github.com/martinpinto/) (coding all over the place)
* [Damian Gryski](https://github.com/dgryski) (provided me with good reading material and reusable code)
* [Keith Ballinger](http://keithba.net/) (implementing the standard dictionary)

##What else?
The project is in **alpha** state, and we intend to improve it in every possible way, e.g:

* **Benchmarks** to test data structures against each other.
* **Referencing** algorithms, instead of copying into the local source (once Go 1.6's vendoring lands)
* **Storage** currently Skizze writes to disc after n seconds or m operations. Soon I'd like to be able to write only dirty segments of the sketch to disc (in case a sketch is large e.g: 1 GB).

Feel free to open issues or help out with more specs development of the project on GitHub. All input appreciated.
