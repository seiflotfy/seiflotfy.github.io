---
layout: post
title: Zeitgeist's journey in the land of KDE
date: '2011-05-22 00:57:01'
---

First I have to say until now it has been amazing. Why you may ask?
<ul>
	<li>libQZeitgeist moved to KDE repositories thanks to my SoC student and already well established rockstar "Trever Fischer"</li>
	<li>Consensus around the integration of Zeitgeist in KDE from the both sides of Nepomuk and Zeitgeist devs</li>
	<li>The awesome Nepomuk team</li>
</ul>
So what are our plans for KDE...

Well Zeitgeist is not only a storage as much as it is also a logic and framework for event processing. Event processing varies from:
<ul>
	<li>Allowing/disallowing events from being logged.</li>
	<li>Attaching geolocation to events</li>
	<li>Prevent duplicate logging</li>
	<li>Global incognitos</li>
	<li>etc...</li>
</ul>
So our idea is to have Zeitgeist into Nepomuk. HOW? The process will be (KDE runtime) activity manager pushing to Zeitgeist for event evaluation, then Zeitgeist forwarding the events Nepomuk. A good scenario to understand why this is needed is:

You dont want something from folder XXX to be logged. How do you do that?
<ul>
	<li>Nepomuk is a storage.</li>
	<li>When the event is captured by the activity manager pushing to Zeitgeist where Zeitgeist will have a set of rules like (don't log anything from XXX) and will evaluate.</li>
	<li>Then Zeitgeist decides if it should be pushed or not.</li>
	<li>(Zeitgeist will also keep its own DB since its pretty compact and useful for some cool zeitgeist features like calculating "what files are related to what" in runtime.)</li>
</ul>
When is this all gonna happen?

Well I am going to Randa 2011 and so is Trever from the Zeitgeist team and we will be meeting with the Nepomuk guys. And discuss these ideas further as well as have it implemented.

So the todo list for the week will be:
<ul>
	<li>Zeitgeist extension that uses FTS search from Nepomuk and sorts using Zeitgeist <strong>(DONE)</strong></li>
	<li>Zeitgeist extension that pushes into Nepomuk (mapping our events to their event representation)</li>
	<li>Zeitgeist extension that pulls from Nepomuk (forwarding their events)</li>
	<li>Zeitgeist extension that annotates activity ids to events</li>
	<li>Patch the Activity Manager to send to Zeitgeist</li>
</ul>
Trever has some working code for some of the tasks but no testing environment yet. So...

<strong>We have one week and it will happen </strong>