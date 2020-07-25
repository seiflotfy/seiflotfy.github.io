---
layout: post
title: Zeitgeist 1.0 almost there (call for hackers)
date: '2013-01-02 18:01:59'
---

So after 4 years of development Zeitgeist is reaching 1.0. The Zeitgeist team has reached a big goal/milestone :D

<strong>What's new?</strong>
<ol>
	<li><strong>New libzeitgeist2</strong>: instead of libzeitgeist which was developed and hosted on Launchpad now reuse and expose our own internal Vala components. When comparing libzeitgeist2 to libzeitgeist we can see over <strong>65% less code</strong> (thanks to Vala) with<strong> 90% compatibilty </strong>with libzeitgeist. (libqzeitgeist not affected)</li>
	<li><strong>GObject Introspection support</strong></li>
	<li><strong>Faster performance</strong>
<ul>
	<li>Testing with 100k events DB here are some plots, those are peromances of synapse and standard time based queries where the yellow bars are 0.9.5 release and green bars represent "master". Shorter bars are better.</li>
	<li><a href="http://geekyogre.com/content/images/2013/01/synapse_unlimited.png"><img class="alignnone  wp-image-3209" alt="synapse_unlimited" src="http://geekyogre.com/content/images/2013/01/synapse_unlimited.png" width="583" height="97" /></a> <a href="http://geekyogre.com/content/images/2013/01/timerange_always.png"><img class="alignnone  wp-image-3208" alt="timerange_always" src="http://geekyogre.com/content/images/2013/01/timerange_always.png" width="583" height="97" /></a> <a href="http://geekyogre.com/content/images/2013/01/timerange_interval.png"><img class="alignnone  wp-image-3207" alt="timerange_interval" src="http://geekyogre.com/content/images/2013/01/timerange_interval.png" width="583" height="97" /></a></li>
</ul>
</li>
	<li><strong>Smaller DB size</strong>: With a very small modification to the main table (primary keys), SQlite created some automatic indices that cover what we need so now instead of 34 indices we only need 25.</li>
	<li><strong>Lots of bug fixes</strong></li>
</ol>
<strong>What now?</strong>

Well if you want to help out roll out this release. We could use some packaging, testing and porting of apps. We won't be able to release until the latest Vala has been released due to some bug fixes concerning the gir generator. But all in all it looks like an exciting release.