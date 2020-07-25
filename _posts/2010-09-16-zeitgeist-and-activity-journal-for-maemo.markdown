---
layout: post
title: Zeitgeist and Activity Journal for Maemo
date: '2010-09-16 12:30:15'
---

It is not news that we got Zeitgeist running on Maemo. It was a challenge to write data providers for maemo to push events in Zeitgeist. So we started off with Telepathy logging, since it is very developer friendly (thanks to their amazing observer stuff).

Right now we just log calls, sms and chats. With some help we will be able to log more stuff. We also have a geo-location extension for zeitgeist working that uses the native Maemo &amp; n900 API to attach locations to events.

Right now we have a simple UI "Maemo Activity Journal" (MAJ). The UI is heavily based on the concepts of Sezen and Unity. It shows logged activities from calls and conversations. We intend to do more stuff during the next week.

<a href="http://geekyogre.com/content/images/2010/09/Screenshot-20100916-115306.png"><img class="alignnone size-full wp-image-1576" title="Screenshot-20100916-115306" src="http://geekyogre.com/content/images/2010/09/Screenshot-20100916-115306.png" alt="" width="480" height="288" /></a>

<a href="http://geekyogre.com/content/images/2010/09/Screenshot-20100916-115328.png"><img class="alignnone size-full wp-image-1578" title="Screenshot-20100916-115328" src="http://geekyogre.com/content/images/2010/09/Screenshot-20100916-115328.png" alt="" width="480" height="288" /></a>

<a href="http://geekyogre.com/content/images/2010/09/Screenshot-20100916-1152011.png"><img class="alignnone size-full wp-image-1583" title="Screenshot-20100916-115201" src="http://geekyogre.com/content/images/2010/09/Screenshot-20100916-1152011.png" alt="" width="480" height="288" /></a>

We intend to show off more nice features and hope to work on the Meego version soon. Some of our ideas to improve the UX on Phones is:
<ul>
	<li>Sort Contact lists by recent/most used in (time and location)</li>
	<li>Change profile based on history... (Everday between 9 - 11 I turn my phone on silent, after a couple of times Zeitgeist recognizes the pattern and switches the profile automogaically)</li>
	<li>Show most visited places...</li>
	<li>Associate Contacts with other phone activities</li>
</ul>
A video will follow as soon as I find a way to make screencasts (VNC is too slow and load-applet  is buggy).