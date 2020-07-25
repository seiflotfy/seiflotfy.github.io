---
layout: post
title: GNOME Activity Journal 0.5.0 (Development Release) & New Data Providers
date: '2010-08-24 18:43:23'
---

The Activity Journal (powered by Zeitgeist) has been finally rolled out from what was in trunk. We reduced some of the functionality Randy developed in our development branch since we wanted a smaller scope of things to fix for now.

You can read more about the release on <a href="http://reflaction.info/?p=209">Thorsten's blog</a>.

Major UI changes is adding a toolbar (Hylke will kill us) but its just experimental until we find a more intuitive way of changing views as well as searching and redesigning the Pinned items.

<a href="http://geekyogre.com/content/images/2010/08/Screenshot-61.png"><img class="alignnone size-full wp-image-1513" title="Screenshot-61" src="http://geekyogre.com/content/images/2010/08/Screenshot-61.png" alt="" width="767" height="466" /></a>

<a href="http://geekyogre.com/content/images/2010/08/Screenshot-62.png"><img class="alignnone size-full wp-image-1514" title="Screenshot-62" src="http://geekyogre.com/content/images/2010/08/Screenshot-62.png" alt="" width="767" height="465" /></a>

<a href="http://geekyogre.com/content/images/2010/08/Screenshot-63.png"><img class="alignnone size-full wp-image-1515" title="Screenshot-63" src="http://geekyogre.com/content/images/2010/08/Screenshot-63.png" alt="" width="767" height="466" /></a>

<a href="http://geekyogre.com/content/images/2010/08/Screenshot-65.png"><img class="alignnone size-full wp-image-1516" title="Screenshot-65" src="http://geekyogre.com/content/images/2010/08/Screenshot-65.png" alt="" width="767" height="466" /></a>

<a href="http://geekyogre.com/content/images/2010/08/Screenshot-64.png"><img class="alignnone size-full wp-image-1517" title="Screenshot-64" src="http://geekyogre.com/content/images/2010/08/Screenshot-64.png" alt="" width="768" height="480" /></a>

<a href="http://geekyogre.com/content/images/2010/08/Screenshot-66.png"><img class="alignnone size-full wp-image-1518" title="Screenshot-66" src="http://geekyogre.com/content/images/2010/08/Screenshot-66.png" alt="" width="768" height="480" /></a>

<a href="http://geekyogre.com/content/images/2010/08/Screenshot-67.png"><img class="alignnone size-full wp-image-1519" title="Screenshot-67" src="http://geekyogre.com/content/images/2010/08/Screenshot-67.png" alt="" width="751" height="456" /></a>

We will work on more speed enhancements and optimizations.

This is a development release. Start filing bugs guys! Download from <a href="http://edge.launchpad.net/gnome-activity-journal/0.5.0/0.5.0/+download/gnome-activity-journal-0.5.0.tar.gz">here</a>.

Also we have support for several new data providers in Zeitgeist. They are still not released but will be soon. They don't reside in Zeitgeist process but within the applications as plugins, because who knows more about what an application is doing than the application itself?

So for now you can install them manually for your apps on downloading them from

<strong>bzr branch lp:zeitgeist-dataproviders </strong>for the following loggers:
<ul>
	<li>bzr</li>
	<li>chrome/chromium</li>
	<li>emacs</li>
	<li>eog</li>
	<li>firefox</li>
	<li>geany</li>
	<li>gedit</li>
	<li>rhythmbox</li>
	<li>tomboy</li>
	<li>vim</li>
</ul>
You can get the telepathy logger from

<strong>bzr branch lp:~mortenmjelva/zeitgeist-dataproviders/telepathy</strong>

<strong><span style="font-weight: normal;">The installation instructions are written inside...</span></strong>

Cheers

Seif

<strong>
</strong>