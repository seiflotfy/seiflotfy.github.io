---
layout: post
title: GNOME Activity Journal gets major performance improvements
date: '2010-09-06 00:55:00'
---

One of the big issues we had in with the Activity Journal was startup time and navigation time. After Michal Hruby kept nagging us on fixing the issue (we used him as the benchmarking measurement and performance profiling), Siegfried and I started working on these issues.

First Siegfried managed to fix the startup time by creating an extension for Zeitgeist that populates the histogram in the bottom. Querying events for 90 in days in one query per day makes itself noticeable, so his approach of a dedicated API from zeitgeist was the best solution. However it did not improve the navigation time.

After 2 days of work motivated by the romantic dinner Michal wants to buy me to fix the issue, we reached our goal. Here is what I did to improve the navigation:
<ul>
	<li>Apply singleton pattern on GIO Files on each URI to reduce initializing a new ones for each event.</li>
	<li>Lazy loading of UI elements. So if the category is not collapsed we don't draw the elements.</li>
	<li>Redraw only days that changed.</li>
	<li>Unparent reuse gtk widgets when navigating.</li>
</ul>
Now the speed improvement is really remarkable. Here is a quick comparison. Each row represents the time in seconds to load a day view.

<a href="http://geekyogre.com/content/images/2010/09/aj-times.png"><img class="alignnone size-full wp-image-1561" title="aj-times" src="http://geekyogre.com/content/images/2010/09/aj-times.png" alt="" width="519" height="500" /></a>

The new Activity Journal is at least 7.3 times faster than what we released last week. Funny enough even the memory consumption is less, due to the singeltons and lazy loading.

<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="480" height="385" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="src" value="http://www.youtube.com/v/vW6UWksC2ps?fs=1&amp;hl=en_US" /><param name="allowfullscreen" value="true" /><embed type="application/x-shockwave-flash" width="480" height="385" src="http://www.youtube.com/v/vW6UWksC2ps?fs=1&amp;hl=en_US" allowscriptaccess="always" allowfullscreen="true"></embed></object>
<h2><a href="http://www.youtube.com/watch?v=vW6UWksC2ps">For a quick video check out this video</a></h2>
There will be a new release soon with the speed enhancements. Hope you like it.

Cheers

Seif