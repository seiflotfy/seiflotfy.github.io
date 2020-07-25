---
layout: post
title: OMG! Trophy Case (Mockup)
date: '2010-08-18 00:35:36'
---

While I managed to get a set of developers working on the OMG! backend, I took the initiative to mock-up the Trophy Case (OMG! Awards Viewer). It is my very first self made mock-up so please have mercy...
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2010/08/OMG.png"><img class="size-full wp-image-1415 aligncenter" title="OMG" src="http://geekyogre.com/content/images/2010/08/OMG.png" alt="" width="631" height="446" /></a></p>
<p style="text-align: left;">With the current development speed I think I can have it hacked in (Gtk) by tomorrow and will plan the Cairo version with some of the Docky developers...</p>
<p style="text-align: left;">So to sum it up:</p>

<ul>
	<li>We have the the backend reaching a good beta soon (it will get a zeitgeist soft-dependency for now to store when the awards were given to the user and how)</li>
	<li>We have our first set of trophies:
<ul>
	<li>Evaluating Tomboy usage</li>
	<li>Evaluating gedit usage</li>
	<li>Evaluating Totem usage</li>
	<li>Evaluating listening to Severed Fifth</li>
	<li>some more to come...</li>
</ul>
</li>
	<li>The mock-up is up and we are ready to hack...</li>
</ul>
Since we are working using an agile development process  and the new team is rocking, any modifications wanted or new requirements can still be developed, so feel free to state your opinion.

---

In other news... We are down to 16 bugs in Zeitgeist. Michal Hruby ported the datahub process of zeitgeist to Vala... making the overall consumption of Zeitgeist and all its processes around 10 MB maximum all in all. But under normal usage with Docky and Activity Journal its looks like this...

<a href="http://geekyogre.com/content/images/2010/08/Screenshot-System-Monitor.png"><img class="alignnone size-full wp-image-1418" title="Screenshot-System Monitor" src="http://geekyogre.com/content/images/2010/08/Screenshot-System-Monitor.png" alt="" width="652" height="404" /></a>

The Activity Journal is reaching a stable now so a release is sometime in the next 2-3 days...