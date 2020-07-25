---
layout: post
title: Some Zeitgeist news
date: '2009-07-02 00:18:06'
---

The last 3 weeks were a pain in the ass concerning Zeitgeist. However it was very productive and dynamic. We finished implementing the new DB design and got it running.

David Barth helped us a lot with organizing the transfer to the new engine that was designed by Mikkel (the XESAM dude). And all the dataproviders were modified accordingly thanks to Markus Korn.

One of the things that got me jumping up and down like a child is when Alex Graveley (Tomboy and Gimmie) told me he was considering building Gimmie again using the Zeitgeist engine (I guess that won't happen though he seems to busy). I will look into that at some point after October.

As for our vague roadmap:

Zeitgeist engine 0.1 and GNOME Zeitgeist 0.1:
<blockquote>We froze development and are only fixing bugs for a 0.1 release:

We currently cover the use cases with the engine and UI:
<ol>
	<li> What did I do in any time period.</li>
	<li> Search activities by tags etc...</li>
	<li> Allow application push their events in Zeitgeist(engine)</li>
	<li> Get most used Documents and websites within any time period</li>
	<li> Bookmark and Tag Documents</li>
	<li> Allow applications to subscribe to events form Zeitgeist(engine)</li>
</ol>
We will be releasing on Friday hopefully.</blockquote>
Zeitgeist engine 0.2 and GNOME Zeitgeist 0.2:
<blockquote>0.2 Release should be in a month it will be a more or less extending the API and UI.

We intend to cover: (All these points are possible but need to be covered by the API)
<ol>
	<li> What applications were used in any time period</li>
	<li>Bookmark/Tag applications</li>
	<li>Most used applications in any time period</li>
	<li>Most occurring events (reading/writing or visiting)</li>
	<li>Bookmark/Tag events</li>
</ol>
Of course all that needs some refurnishing from the UI side. So the current UI is not our final implementation while the engine wont be seeing major changes until 2.28</blockquote>
After GNOME 2.28 we intend to go a little further by first logging events from online applications and exporting all our dataproviders to be extensions residing in the applications themselves. For that we will need some support form the GNOME developers to extend their apps if possible with plugins. This will allow us then to:

Know how long an activity on an document lasted which then would allow us to:
<ul>
	<li>Auto Tag intersecting events and their documents</li>
	<li>Create relationships between items</li>
	<li>Restore a full state of a computer (which docs and apps were open)</li>
</ul>
Also my GSoC student "RainCT", who is amazingly proficient at making me feel redundant (I will be blogging about that topic soon), has done amazing progress with the engine, API as well as the Shell integration. He has become one of the most important people in the team. Canonical or Google I recommend hiring the little dude!

I think I should mention that Shane Fagan is working on a new KDE UI.

Federico, Thorsten and me are working on the slides for our GUADEC talks. Pretty exciting shit!

However I will be taking 2 weeks off after GUADEC since I have been actively working on Zeitgeist since last October (almost everyday). I need to focus on my exams and the new Zeitgeist extension "Codename Cookie Monster"(we still need a better name) that I will be designing the backend of it with Alex Gabriel from Mayanna and Natan.