---
layout: post
title: Zeitgeist 0.3 and BEYOND
date: '2009-12-01 21:51:04'
---

<strong>At last Zeitgeist Framework 0.3 is out!!!!!!!!</strong>

You can check out the release statement <a href="http://mail.gnome.org/archives/gnome-announce-list/2009-December/thread.html">here</a>.

It was by far our most difficult and challenging release. And thanks to the amazing team and the hackfest it was possible. I really can not express how happy I am working with such talented developers such as Markus, Mikkel, Siegfried, Alex and others. You guys rock and never have I had so much fun working with anyone on any project before.

Big big thanks to Youness Alaoui (Collabora) and Jason Smith for their harsh criticism towards our last API and their help on improving it.

Also a big thanks to <a href="http://www.harihareswara.net/">Sumana Harihareswara</a> (Collabora) for helping and inspiring us to improve out game and development management!

The 0.3 release is a big milestone in the the zeitgeist development since we intend not to break the API anymore (only if critical) plus the new architecture allows us to extend the possibilities of the framwork without breaking our Core or the API.

Some extensions (or as we call them Smack-ins) are already in the works, e.g:
<ul>
	<li><strong>Teamgeist</strong> (thanks to Collabora) which will allow real-time activity awareness of team members. (Under heavy development)</li>
	<li><strong>Location monitor </strong>will use libchamplain to add an annotation to every event to track the location of your activities. This will enable queries such as "What did I do on my way from Amsterdam to Prague?"</li>
	<li><strong>Focus monitor</strong> that will answer queries such as "How long did document  x have focus within any time period" or "Which documents do i usually swtich to/from from/to x". (Just needs porting)</li>
	<li><strong>Relevancy model </strong>will be able to determine which documents are usually used together. (Prototyped before)</li>
	<li><strong>Synapse </strong>will allow some bad ass Tracker+Zeitgeist queries to answer some really mean queries such as "most opened documents in Christmas"</li>
</ul>
While the global gtk.Recentlyused data provider still exists we  also started writing plugins for various applications that push from the application into Zeitgeist whenever an activity takes place. During the course of developing 0.4 we will deprecate the some thing in the gtk.Recentlyused dataprovider. We already have various dataproviders such as:
<ul>
	<li>bzr</li>
	<li>totem</li>
	<li>gedit (when did i open/close modify a document)</li>
	<li>rhythmbox</li>
	<li>firefox</li>
	<li>eog</li>
</ul>
of course there is more to come from there.

We will be focusing now on delivering the UI and the Teamgeist module soon.

THANKS TO EVERYONE WHO CONTRIBUTED