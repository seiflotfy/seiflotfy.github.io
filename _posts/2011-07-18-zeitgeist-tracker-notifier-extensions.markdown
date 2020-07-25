---
layout: post
title: Zeitgeist -> Tracker Notifier Extensions
date: '2011-07-18 18:58:18'
---

This is doing to be short. Via an extension to Zeitgeist (<strong>no Zeitgeist code modified</strong>), any application that pushes its events into Zeitgeist, Zeitgeist tells Tracker to index the subjects of these events. Why do you need it? Well simple:

Tracker does not really index all your files but rather the "Home" folder and the standard XDG directories (recursively). You can add more folder or documents to be monitored, however this is pretty expensive due to the nature of inotify sucking.

This is where Zeitgeist jumps in. We managed to get applications to tell Zeitgeist what they are doing (event) and to whom they are doing it to (subject) and via an extension we tell Tracker when a subject is modified or created. This way stuff that is outside the "monitored directories" are also indexed when you interact with them...

So if you have Tracker installed and want to get more out of it just install Zeitgeist too then:
<ul>
	<li>Download <a href="http://bazaar.launchpad.net/~zeitgeist-extensions/zeitgeist-extensions/trunk/download/head:/tracker.py-20110715235456-xl2g67v37jz9ersc-2/tracker.py">tracker.py</a> and add it to ~/.local/share/zeitgeist/extensions/</li>
	<li>Get some <a href="http://launchpad.net/zeitgeist-datasources/0.8/0.8.0/+download/zeitgeist-datasources-0.8.0.1.tar.gz">Zeitgeist loggers</a></li>
	<li>Have fun....</li>
</ul>