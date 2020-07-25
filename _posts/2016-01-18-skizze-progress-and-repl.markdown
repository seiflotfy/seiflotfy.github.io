---
layout: post
title: Skizze progress and REPL
featured: true
date: '2016-01-18 17:41:43'
tags:
- big-data
- data-science
---

<img src="http://i.imgur.com/9z47NdA.png" align="center" height="190" width="600">
<br>
Over the last 3 weeks, based on feedback we proceeded fledging out the concepts and the code behind [Skizze](https://github.com/skizzehq/skizze).
[Neil Patel](https://medium.com/@njpatel/) suggested the following:

***
*So I've been thinking about the server API. I think we want to choose one thing and do it as well as possible, instead of having six ways to talk to the server. I think that helps to keep things sane and simple overall.*

*Thinking about usage, I can only really imagine Skizze in an environment like [ours](https://xamarin.com/insights), which is high-throughput. I think that is it's 'home' and we should be optimising for that all day long.*

*Taking that into account, I believe we have two options:*

1. *We go the gRPC route, provide .proto files and let people use the existing gRPC tooling to build support for their favourite language. That means we can happily give Ruby/Node/C#/etc devs a real way to get started up with Skizze almost immediately, piggy-backing on the gRPC docs etc.*

2. *We absorb the Redis Protocol. It does everything we need, is very lean, and we can (mostly) easily adapt it for what we need to do. The downside is that to get support from other libs, there will have to be actual libraries for every language. This could slow adoption, or it might be easy enough if people can reuse existing REDIS code. It's hard to tell how that would end up.*

*gRPC is interesting because it's built already for distributed systems, across bad networks, and obviously is bi-directional etc. Without us having to spend time on the protocol, gRPC let's us easily add features that require streaming. Like, imagine a client being able to listen for changes in count/size and be notified instantly. That's something that gRPC is built for right now.*

*I think gRPC is a bit verbose, but I think it'll pay off for ease of third-party lib support and as things grow.*

*The CLI could easily be built to work with gRPC, including adding support for streaming stuff etc. Which could be pretty exciting.*
***
That being said, we gave Skizze [a new home](https://github.com/skizzehq/), where based on feedback we developed .proto files and started rewriting big chunks of the code.

We added a new wrapper called "domain" which represents a stream. It wraps around Count-Min-Log, Bloom Filter, Top-K and HyperLogLog++, so when feeding it values it feeds all the sketches. Later we intend to allow attaching and detaching sketches from "domains" (We need a better name).

We also implemented a gRPC API which should allow easy wrapper creation in other languages.

Special thanks go to [Martin Pinto](https://twitter.com/martinpintob) for helping out with unit tests and [Soren Macbeth](http://dopeness.org) for thorough feedback and ideas about the "domain" concept.
Take a look at our initial REPL work there:
![click for GIF](/content/images/2016/08/MBCY64aaKL.gif)
