---
layout: post
title: Zeitgeist Project related stuff!
date: '2009-08-07 02:00:40'
---

After a long break the team is somehow back on track! After going through Jono's "<a href="http://www.artofcommunityonline.org/">Art of Community</a>" (which I recommend everyone involved in open source to read), I realized i was burned out. When I wanted to start hacking again my Laptop let me down and broke on me. Thanks to the guys at Novell I should be getting a new one soon. Now for the more important part here are some points being tackled:
<ol>
	<li>After <a href="http://www.grillbar.org/wordpress/">Mikkel's blog post</a>, we are constructing the 0.3 release. Things were not so pesimistic we just needed to set some goals straight and at last we reached an excellent ontology for event representation (I will blog about that later).  If 0.3 works out well we will propose our ontology to tracker and Nepomuk thus taking away the storage pain and pushing for more cross desktop development. Now we need to finish some bugs and 3 blueprints :)</li>
	<li>Concerning storage Markus Korn implemented a flexible backend module that made it into trunk that will allow the user to choose which kind of database he/she wants to use for the storage.</li>
	<li>Hopefully I can introduce the idea of "expiring tags" in this release, thus automatically setting temporary associations between files, e.g: Imagine using google.com while working on Project A. This way google.com gets tags from Project A. Once you stop using them together for a little while the tags that were mapped form Project A to google.com will be deleted</li>
	<li>GNOME Zeitgeist (the journal UI) should be released soon too (forget what you see in trunk the performance and layout will be much better and detailed, just need a new lappy to work on it).</li>
	<li><a href="http://bloc.eurion.net/">Siegfried</a> my enslaved GSoC student did some kick ass work with the Shell integration. Watch <a href="http://www.youtube.com/watch?v=VyoD2v7QGCE">this</a> and <a href="http://www.youtube.com/watch?v=hEH4G9p5ens">that</a>.</li>
</ol>
Other interesting things happening in the zeitgeist universe would be:
<ol>
	<li>According to Markus Zeitgeist FS should be released soon.</li>
	<li>We have a little prototype of Feedgeist where we ignore the whole files and folders system but rather introduce a new way of dynamic file managment. We use topics where topics have criterias for files to be associated with it. For this we will be using Zeitgeist as well as Tracker. As in "GCDS" topic takes everything tagged or containing guadec, gcds, akademy, etc... and relates it to the topic. So topics are dynamic and its content increase and decrease dynamically. <a href="http://natanyellin.com">Natan Yellin</a> will be leading the development of this project.</li>
	<li>I kinda gave some people more cookie monster aka Teamgeist (A Collabora + Tracker + Zeitgeist hack) peaks and was happy with the positive feedback, especially <a href="http://castrojo.wordpress.com/">Jorge Castro</a> but I think it should stay censored :P. Also I will be meeting up with <a href="http://blog.karlitschek.de/">Frank Karlitschek</a> from KDE sometime within the next 2 weeks to discuss a possible  Teamgeist cooperation or integration with KDE's social desktop. After the 0.3 release it should get a lot of attention.</li>
	<li><a href="http://einalex.mayanna.org">Alex Gabrie</a>l will be working on a little extension for zeitgeist that exports events into a ical file so it coudl be easily viewd within any calendar application such as google's or evolution.</li>
</ol>
So its bedtime got me, cheers and good night!