---
layout: post
title: Zeitgeist scalability & efficiency bootcamp results
date: '2012-05-15 22:37:52'
---

As <a href="http://wm161.net/2012/05/15/zeitgeist-optimizations/">Trever blogged yesterday</a>, the Zeigeist team has been busy with tweaking the DB and the engine. During that process tools and benchmarks have been developed to make the tweaking and testing more interesting. Trever will be blogging about that tomorrow so make sure to check his blog.

Our end goal is  trying to scale the engine to be able to handle a few billion events just as fast as it can handle a few hundred thousand. While we are not there yet we managed to have some pretty nice stable results for the first iteration. A lot of results show more than <strong>100% speed enhancement</strong>. In other words a lot of queries from our standard benchmarks now consume more than <strong>50% less time to execute</strong>. Here are some graphs of our benchmarks.

<strong>Green indicates the 0.9 release</strong>

<strong>Yellow indicates the new trunk</strong>

Most notable performance enhancement is querying Zeitgeist with a specified timeframe (from data x to date y).

<a href="http://geekyogre.com/content/images/2012/05/timerange_interval.png"><img class="alignnone  wp-image-2280" title="timerange_interval" src="http://geekyogre.com/content/images/2012/05/timerange_interval.png" alt="" width="972" height="162" /></a>

&nbsp;

Same queries with an open timeframe also improved

<a href="http://geekyogre.com/content/images/2012/05/timerange_always.png"><img class="alignnone  wp-image-2281" title="timerange_always" src="http://geekyogre.com/content/images/2012/05/timerange_always.png" alt="" width="972" height="162" /></a>

&nbsp;

We also have a copy of the Synapse queries benchmarked

<a href="http://geekyogre.com/content/images/2012/05/synapse.png"><img class="alignnone  wp-image-2282" title="synapse" src="http://geekyogre.com/content/images/2012/05/synapse.png" alt="" width="972" height="162" /></a>

<a href="http://geekyogre.com/content/images/2012/05/synapse_unlimited.png"><img class="alignnone  wp-image-2283" title="synapse_unlimited" src="http://geekyogre.com/content/images/2012/05/synapse_unlimited.png" alt="" width="972" height="162" /></a>

The queries here are typical queries used to extract info from Zeitgeist. So right now the team is really happy with the initial results. For Synapse on my local DB (over a year old), all my synapse queries perform under 0.08 seconds. We still can get more out of this. The trick here was improving our indexes and our sql query generator.

Next month we will be going through another iteration.

&nbsp;

&nbsp;