---
layout: post
title: 'Gnome Journal Update #5'
date: '2008-11-09 19:33:57'
tags:
- gnome
- journal
- linux
- mayanna
- ogrenizer
- timeline
---

I assume this is update 5 thus #5

So the filters are working pretty well! All functional and every dataprovider will be automatically included into the filters list. I still have to work on the refreshing view thingie but all in all pretty stable. The issue concerning me is that when to much data is provided e.g. Firefox history (couple of thousand on my PC) it could take too long to create and view the items! The Firefox Dataprovider is in the code, however will not be displayed, since inserting over 3000 items makes the whole thing take too long to start up and filter out! Plus somehow Firefox blocks usage of the sqlite database while running.

Features:
<ol>
	<li> Filter works perfectly</li>
	<li>Firefox DataProvider included into code but disabled</li>
</ol>
Issues:
<ol>
	<li> Refreshing the view or loading lots of items takes too much time!</li>
	<li>Bookmarking is still disabled</li>
</ol>
As for hacking updates Natan Yellin set up a bzr branch on launchpad. Have a look here. To copy this branch open a terminal and go:<strong><em> bzr branch lp:gnome-doc-centric-playground</em></strong>

If someone can reach Federico please tell him to contact me :P