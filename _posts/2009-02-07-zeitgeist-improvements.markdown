---
layout: post
title: Zeitgeist improvements
date: '2009-02-07 14:23:52'
tags:
- gnome
- pythonm-mockup
- zeitgeist
---

To sum up we finally added evolution sent mail support! Though a bit buggy it is still pretty usable. Firefox now also takes ur bookmarks into Zeitgeist. I created a new mockup of how i would like the UI to be. This will require clutter so stay tuned for the UI makeover! Here is a quick dirty ugly mockup

<a class="tt-flickr tt-flickr-Medium" title="rect3414" href="http://www.flickr.com/photos/8097354@N02/3260437580/"><img class="alignnone" src="http://farm4.static.flickr.com/3503/3260437580_4bd8944bc7.jpg" alt="rect3414" width="500" height="321" /></a>

Another cool feature I am working on is the relationship managment! After talking to <a href="http://davebsd.com/">David Siegel</a> he introduced me to predix. I did not start implementing it yet into Zeitgeist. I got in contact with my friend Diego from school and we started looking for an algorithm that can determin data relationships and behaviour patterns based on a timeline of uniformly distributed data activities. We both agreed on "<a href="http://en.wikipedia.org/wiki/A_priori_(statistics)">A priori"</a> being the best solution however Diego started implementing his own idea of "temprature based" relationships. As in the closer the events to each other the higher the possibility of them of being related. This was then extended by a frequency/priority variable. Its stil lnot very stable but its a good start! It managed to figure out that youtube, facebook and my bankaccount have a relationships ( I usually check them in specidifc time intervals but not in that same order )

That is it for now got to study.

<img src="file:///home/seif/Documents/rect3414.png" alt="" />