---
layout: post
title: External plugin for Epiphany data pushing into Zeitgeist
date: '2009-05-04 00:53:22'
---

With D-Bus up and running we managed to write a quick plugin for epiphany that pushes visited websites with the timestamp to zeitgeist. This way we dont need to monitor the epiphany history file anymore! So here is the sample epiphany plugin <a href="http://pastebin.ca/1411644">code</a>.

We know have two options to log:
<ol>
	<li>We monitor applications from within Zeitgeist and log the activities. (Pro: One has a central dataprovider manager to enable/disable logging. Con: Resources)</li>
	<li>We allow applications to send its data to Zeitgeist. (Pro: less work for the Zeitgeist team to write dataprovider loggers and less resource consumption from the Zeitgeist side. Con: no central dataprovider manager)</li>
</ol>
What do you think?

P.S: Try out zeitgeist from our <a href="https://code.edge.launchpad.net/gnome-zeitgeist">bzr branch</a>. If interested join the <a href="https://edge.launchpad.net/~gnome-zeitgeist-users">mailinglist</a> (still pending) and file <a href="https://edge.launchpad.net/~gnome-zeitgeist-users">bugs</a>.