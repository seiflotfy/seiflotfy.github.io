---
layout: post
title: 2 Release Announcements (Zeitgeist + GAJ)
date: '2010-01-20 01:20:22'
---

Thanks to the Zeitgeist Project Team we have 2 good news today
<h2>GNOME Activity Journal 0.3.2 - Luciana's Tricycle</h2>
<span style="font-weight: normal; font-size: 13px;">On behalf of the Zeitgeist Project team, after 1 year, 3 months, and 9 days since the first prototype, I am proud to announce the first development release of GNOME Activity Journal, codenamed "Luciana's Tricycle".</span>

<strong>What is GNOME Activity Journal?
</strong>

GNOME Activity Journal is not a File Browser but an Activity Browser. It uses the Zeitgeist Framework to display what you did, and introduces a better way to quickly find the things you were doing.

<strong>Where?</strong>

Downloads: <a href="http://edge.launchpad.net/gnome-activity-journal/0.3/0.3.2/+download/gnome-activity-journal-0.3.2.tar.gz">http://edge.launchpad.net/gnome-activity-journal/0.3/0.3.2/+download/gnome-activity-journal-0.3.2.tar.gz</a>
About Zeitgeist: <a href="http://zeitgeist-project.com">http://zeitgeist-project.com</a>
Wiki: <a href="http://live.gnome.org/GnomeActivityJournal">http://live.gnome.org/GnomeActivityJournal</a>

<strong>Features:</strong>
<ul>
	<li>Pretty layout</li>
	<li>Pinning (marking) items</li>
	<li>Calendar slider (quickly move forwards/back in time)</li>
	<li>Preview tooltips</li>
</ul>
<strong>Experimental:</strong>
<ul>
	<li>Tracker-based search</li>
</ul>
<strong>Features in progress for future releases:
</strong>
<ul>
	<li>Display web browsing history in the journal</li>
	<li>Search and interaction</li>
	<li>Tags</li>
	<li>Detailed single-day view showing relationships between files</li>
	<li>Removing activities from the journal</li>
</ul>
<strong>Call for translators:</strong>

<strong><span style="font-weight: normal;">The project is still very low on translations. We'd really appreciate translation contributions so more people will be able to start using Zeitgeist.</span></strong>

Cheers
Seif Lotfy

<strong>------------------------------------------------------------------------------------------------</strong>
<h2>Zeitgeist 0.3.2 - Shadowy Rumble</h2>
On behalf of the Zeitgeist Project team, I am pleased to announce the immediate availability of Zeitgeist 0.3.2. This is the third development release, leading up to what will be our stable 0.4 series. It introduces bug fixes and other performance optimizations to work with GNOME Activity Journal.

<strong>What is Zeitgeist?</strong>

Zeitgeist is an event-logging framework for desktop and mobile devices. Applications can push events into the log, and anyone can query the log via the rich query API. The logged events are semantically categorized and can come from any sort of activity, such as file usage, communications, and browsing history, etc. The Zeitgeist engine is a user-level service and does not have a GUI. It is intended to support dedicated journaling applications aand deep integration with other desktop components.

<strong>Where?</strong>

Downloads: <a href="https://launchpad.net/zeitgeist/+download">https://launchpad.net/zeitgeist/+download</a>

<a href="https://launchpad.net/zeitgeist/+download"></a>About Zeitgeist:<a href=" http://zeitgeist-project.com"> http://zeitgeist-project.com</a>

Wiki: <a href="http://live.gnome.org/Zeitgeist">http://live.gnome.org/Zeitgeist</a>

<strong>News since 0.3.1</strong>
<ul>
	<li>Added FindEvents, optimized shorthand for GetEvents(FindEventIds(...)).</li>
	<li> Fixed DeleteEvents and make it ignore bad requests.</li>
	<li> Fixed GetEvents not to raise an exception when called with an empty list.</li>
	<li> ZeitgeistClient.get_version() now returns a Python list.</li>
	<li> Some code refactoring, documentation changes and other little fixes.</li>
</ul>
Cheers,

Seif Lotfy