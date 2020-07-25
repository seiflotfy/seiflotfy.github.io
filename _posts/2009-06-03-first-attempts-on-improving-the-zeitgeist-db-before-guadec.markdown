---
layout: post
title: First attempts on improving the Zeitgeist DB before GUADEC
date: '2009-06-03 21:33:06'
---

During UDS we changed the DB a bit to store the applications that were used for the activities. allowing us to bookmark applications, and detemrining most used ones.

Well here is the current Zeitgeist DB (pretty simple and stupid)

<img class="size-full wp-image-679 alignnone" title="zeitgeist" src="http://geekyogre.com/content/images/2009/06/zeitgeist.jpeg" alt="zeitgeist" width="550" height="321" />

Natan has suggested improving the tag table. After some thought i decided to give it a shot on hopefully the rest of the Zeitgeist team agrees with me on this table. Working with INTEGERS instead of STRINGS should improve performance as well as disk space. But take a look first.

<a href="http://geekyogre.com/content/images/2009/06/zeitgeist-new.jpeg" target="_blank"><img class="alignnone size-full wp-image-680" title="zeitgeist-new" src="http://geekyogre.com/content/images/2009/06/zeitgeist-new.jpeg" alt="zeitgeist-new" width="1041" height="527" /></a>

Here are the major features the new design would bring with it.
<ol>
	<li>The timetable should be able to differentiate between event types: Activities (things the user does) Notifications (Other peoples activities (sending you an email) that could trigger your attention and lead to new activities (Replying the mail or sending a tweet)) Maybe we could use the notify-osd to capture notficaitons of interest.</li>
	<li>Giving every registered application its own table to store specific info about a a uri (example position of the item in UNR) or Shell specific rankings.</li>
	<li>Allowing opening data from a timestamp with the Application that was used back then.</li>
</ol>
Any suggestions now are welcome. We will be developing it during next week to be done on saturday. I will then write a little API Doc for applications to use Zeitgeist. Current functions will not be replaced we will just add new ones.