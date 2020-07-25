---
layout: post
title: 'Gnome Journal Update #6'
date: '2008-11-10 21:41:43'
tags:
- gnome
- journal
- linux
- mayanna
- ogrenizer
- timeline
---

I managed to get Firefox history at last. After some issues with SQLite locks, copying the places.sqlite and work on it was the solution. Still it takes too long to display them!The good thing about the code is that both UI and engine are seperated. Another cool thing is now automatically when one writes a new dataprovider it can autmatically be filtered. Next on the list is improving performance and memory consumption(although its waaaaaaaaay better than gimmie/mayanna).

Features:
<ol>
	<li>Firefox now enabled</li>
	<li>Cleaned up code</li>
	<li>Enabled Drag and Drop</li>
</ol>
Issues:
<ol>
	<li> Refreshing the view or loading lots of items takes too much time!</li>
	<li>Bookmarking is still disabled</li>
</ol>
I will upload the changes as soon as I turn on my laptop!

*Update its all up on <a href="https://code.edge.launchpad.net/gnome-doc-centric-playground">launchpad </a>or just go <strong><em>bzr branch lp:gnome-doc-centric-playground</em></strong>