---
layout: post
title: My first Mozilla contributions
date: '2013-01-02 18:44:42'
---

<center>![](http://mozorg.cdn.mozilla.net/media/img/sandstone/header-mozilla-stone.png)</center>

As of beginning of December I started contributing to the Mozilla community... I must say amazing people and amazing environment.

I was invited by <a href="http://www.joshmatthews.net/">Josh Matthews</a> and <a href="http://davidwboswell.wordpress.com/">David W. Boswell</a> to a Mozillians meeting. The first task I took upon myself was getting new contributors mentioned with every release. With the help of the others I went around pinging people and a couple of days later we reached the consensus that we will be linking to a blog post on <a href="http://blog.mozilla.org/community/category/spotlight/">http://blog.mozilla.org/community/category/spotlight/</a> from the release note with every release.

We will be using a set of premature scripts I am working on to detect new contributors to a release as well as the contribution rate (code and bugs which is inspired by my GNOME fellow Andre Klapper). Those can be found <a href="https://github.com/seiflotfy/mozcctools">https://github.com/seiflotfy/mozcctools</a> (nothing special they just spit out JSON stats, will automate them this weekend).

And last but not least. After an interesting call with the super dad himself, <a href="http://www.nbcnews.com/technology/ingame/super-dad-hacks-video-game-transforms-hero-his-daughter-1C7040451">Mike Hoye</a>, I took a challenge upon myself to hack a tool that does the following:

Enter a a keyword, and it will spit out Mozillians that are affiliated with this keyword based on their code commits and bug reports.

It took me around 60 minutes to hack the tool using Zeitgeist and the Full Text Indexer extension. Basically importing the last 120k code commits and indexing the commit message. I will publish the code soon. After that I spent 30 minutes with Josh and Mike playing with it testing the results. Mike Hoye has some great ideas on how to deploy such a tool (Bugzilla included), and hopefully I can show off the cleaned up code in the following days.

I am thinking of deploying such a tool for the KDE and GNOME community sites to find ways to directly contact hackers based on keywords.

All in all the Mozilla contribution experience is really fun, and while not hacking on Firefox or B2G I am having fun developing tools for enabling the community.