---
layout: post
title: Zeitgeist Project to go for stable release cycles
date: '2011-02-11 13:03:31'
---

I think the title says it all. With the Zeitgeist deployment progressing, we see more soft &amp; hard - dependencies on the Zeitgeist modules. Currently we plan 2 releases ahead based on the amount of bugs and blueprints we have open.

The core modules of Zeitgeist now consist of:
<ul>
	<li>Zeitgeist Engine (the core that accepts events and allows other processes to query it)</li>
	<li>Zeitgeist Datahub (the fallback logging process that pushes events into the engine)</li>
</ul>
Then we have the wrapper around our D-Bus API:
<ul>
	<li>python-zeitgeist</li>
	<li>libzeitgeist</li>
	<li>libzeitgeist-sharp</li>
	<li>libqzeitgeist</li>
	<li>libzeitgeist-js</li>
</ul>
And last but not least comes:
<ul>
	<li>Zeitgeist Dataproviders (A set of plugins for various applications that allow you to send events from the applications directly to Zeitgeist)</li>
</ul>
Sadly all those modules till now do not have the same version number. This makes it very hard for downstream projects to package and find dependencies. Also upstream need to now what they need something to depend on.

So to get to the point we decided to release ALL MODULES together 4 times a year.

The dates of the releases are more or less static:
<ul>
	<li>15th March</li>
	<li>15th June</li>
	<li>15th September</li>
	<li>15th December</li>
</ul>
Also all of the releases will follow the same version schema. So with the next releases we will be all bumped to 0.8.x where the "x" represents module internal fixes.

We will be setting up a <a href="http://wiki.zeitgeist-project.com">wikipage</a> with more details next week.By then also all <a href="http://zeitgeist-project.com/development/documentation/">API documentations </a>will then be found on our <a href="http://zeitgeist-project.com/">website</a>.