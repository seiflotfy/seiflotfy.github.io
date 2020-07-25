---
layout: post
title: A brief preview of Zeitgeist Framework 0.3
date: '2009-11-19 12:19:03'
---

<span style="text-decoration: underline;"><strong><span style="color: #ff0000;">Zeitgeist framework 0.3</span></strong></span> not the GNOME Activity Journal

Something that might be as a shock to some other devs is that we decided not to store annotations and bookmarks within Zeitgeist. This should be done in <strong>Tracker</strong>. Zeitgeist answers only <strong>WHEN AND HOW DATA WAS ACESSED!</strong> We store a journal of how some metadata looked like at the event  but nothing compared to Tracker since we don't store our metadata . We will be working very closely with Tracker from now on since 0.7 has been  for a GNOME 2.30. Congrats to the Tracker Devs.

Zeitgeist 0.3 will be a development preview for the 0.9 and 1.0 version that we intend to propose for GNOME inclusion. We won't be breaking APIs from now on unless its curcial.

Features:
<ul>
	<li><span style="color: #ff0000;"><strong>Journal of all the user activities</strong></span> that allows you to ask for a subjournal of any timeperiod for mimetypes, applications, subjects(docs/websites/...), events(opened, closed, focused modied and saved)</li>
	<li><strong><span style="color: #ff0000;">Most Used</span></strong> mimetypes, applications, subjects(docs/websites/...), event types(opened, closed, focused modied and saved) in any timeperiod.</li>
	<li><strong><span style="color: #ff0000;">Payloads</span></strong> can be stored to to each event. Just like in git and bzr where users add a note to each commit. It should be aloud to add payloads to each event, e.g: the reason the document was changed that way.</li>
	<li>Provide <strong><span style="color: #ff0000;">Overall Focus Lifetime</span></strong> of applications and documents within any timeperiod.</li>
	<li>(IMPLEMENTED BUT MISSING DBUS BINDINGS) <strong><span style="color: #ff0000;">Get most focused to docs/apps from docs/apps</span></strong> and vice verse within any timeperiods.</li>
	<li>(IMPLEMENTED BUT MISSING DBUS BINDINGS)<strong><span style="color: #ff0000;"> Subcribe to events</span></strong> from the Journal.</li>
</ul>
With have a good API to support these features and I would like to suggest applications dumping their history into Zeitgeist if possible instead of maintaining their own history.
For a technical overview of the improvements over 0.2:
<ul>
	<li>stable codebase</li>
	<li>very clean modular architecture that allows easy improvements and maintanance</li>
	<li>open  for new relevancy algortihms</li>
	<li>better performance and more memory effcient</li>
	<li>clean and structured DBus API. no more weird hashes and structs</li>
	<li>less logging from our side since now extension for apps exists like Markus's amazing firefox plugin that send events to zeitgeist.</li>
</ul>
We are undergoing some last bug fixes and cleanups. A release will be out soon.