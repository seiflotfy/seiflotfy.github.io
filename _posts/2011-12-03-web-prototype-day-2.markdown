---
layout: post
title: Web Prototype day 2
date: '2011-12-03 04:10:36'
---

<blockquote><address><strong>This post is by no means meant to be criticism, but rather an opinion on raising questions we couldn't get answers to.</strong></address></blockquote>
So on day 2 I got Federico Mena and Garrett LeSage to try out my prototype. While we noticed some nice features there were also some very unclear ones too. Today we concentrated on the "Tabs" and "Top Panel", which is what is covered by the prototype.
<h2><strong>The Good:</strong></h2>
<ul>
	<li>Minimalism. It really is easy on the eyes in a way. Reducing the chaos of tabs is relaxing.</li>
	<li>Having a shrunk version of of the pages you got open in the "Pages" helps you navigate easier, than navigating via page titles. Its links switching apps in GNOME Shell pretty cool.,</li>
	<li>Blends in with the other designs of the core GNOME apps.</li>
</ul>
<h2><strong>The Unclear:</strong></h2>
<strong>Overview</strong>

A lot of usability is unclear. Let us take this "Pages" screen (from the wiki <a href="https://live.gnome.org/Design/Apps/Web">https://live.gnome.org/Design/Apps/Web</a>) as an example:

It is not clear which one are really the currently open pages and which one are the "Recent", since the "Recent" button is highlighted. We are not even sure if the upper one represents the currently open pages. If not then where are the tabs? If yes then based on the mockup there is this horizontal line splitting the view in two:

<a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-03-021730.png"><img class="alignnone size-full wp-image-2128" title="Screenshot at 2011-12-03 02:17:30" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-03-021730.png" alt="" width="487" height="376" /></a>

Our interpretation of these mock-ups which looked the following (keep in mind its a functional prototype which means some things are not fully implemented):

<a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-03-024001.png"><img class="alignnone size-full wp-image-2129" title="Screenshot at 2011-12-03 02:40:01" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-03-024001.png" alt="" width="484" height="303" /></a>

(the implementation doesn't show screenshots of recent stuff since its hard to query those, I replaced them with empty buttons).

So the way to differ according to the (real looking) mock-ups in the wiki is to give the upper section of the view a toolbar style. Seems fair and IMHO opinion it looks nice. Problem however is how distinguishable is it from the the lower "Recent" section? How big does this view get? If I have 20 tabs open that is a lot of scrolling to be done to find one of my open pages, and even more to be done to get to the "Recent" stuff (which is not opened anymore)...

That being said the lower recent section (the real recent stuff) has to be defined better. Is it:

a) going to represent "History": Bad idea because my history is huge and this won't even scale.

b)  just a predefined of maximum amount of recent pages. How do I find my History then?

<strong>Navigating through Pages:</strong>

While the mock ups introduce a new and very nice way for recognizing the websites you have open. It kinda takes you out of the focus. One thing I like about tabs is that I have what I am working on in Focus. And by just moving my eyes I can read the label of the tabs and decide if I want to navigate to a new tab or not. With the current mock up I would have to zoom out of my current page and back in. Not sure how good or bad this is.

As far as we could tell the designs are inspired by several other projects by Apple, litl, Pre, Chrome, etc... Some use tabs some don't... Honestly all of those that use tabs are more intuitive in our opinion. Maybe because I am used to them, this might change.

<strong>Creating new Pages:</strong>

How do I create pages? Based on the mock ups I will need to use the search bar as seen below.

<a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-03-0217181.png"><img class="alignnone size-full wp-image-2130" title="Screenshot at 2011-12-03 02:17:18" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-03-0217181.png" alt="" width="502" height="392" /></a>

How we understood it is the search bar will search through the history and open pages too to find what I want... This is just brilliant (and I am not being sarcastic). If I can't find what we are looking for in the History, there is a "Search" via Google (or anything else of your choice). This is very common for non-techies to now use the url bar and instead do the following:
<div id="_mcePaste">
<ul>
	<li>Always use the search entry next to the URL bar in Firefox</li>
	<li>Type "Gmail" or "Facebook" or "Youtube" or "cuevana" there, in the search entry</li>
	<li>Pick the first link from Google, which is "of course" the right one, and goes on with life</li>
</ul>
</div>
The only corner case I see here is if I know the URL. How does this work? Do I really need to go through Google. Is there no easy way to create a new page (please don't tell me menus).

As for the sorting according to the wiki will be done wither via recent or frequent and will the results will be either presented as a grid or linearly... Its still on the Tod o list.

<strong>Closing</strong><strong> new Pages:</strong>

<strong> </strong><strong> </strong>

There was no obvious way but I guess having a small x on the corner of a page button to close it would make sense. So no biggie.
<p style="font-weight: bold;"><strong>Viewing a page:</strong></p>
Its pretty standard and the reduced noise in the panel makes it comfortable however it still feels like wasted space﻿. While I agree with Mathias Hasselmann on the principal of the flaws that he addressed in the following illustration,

<a href="http://taschenorakel.de/files/gnome-web/gnome-web-mockup-flaws.png"><img class="alignnone" style="border-style: initial; border-color: initial;" title="Web Flaws" src="http://taschenorakel.de/files/gnome-web/gnome-web-mockup-flaws.png" alt="" width="614" height="461" /></a>

he must have not gone through the whole wiki... When you click on the Facebook label it will expand into a URL bar. Not sure what to think of this idea. The button on the VERY right is confusing. It is supposed to be a share button but since there is so much empty space I expected it to be a close button. The panel does not give the impression of a real panel. However this might change since a URL bar might replace it indefinitely due to some comments by the WebKit-Gtk team on "phishing".

<strong>Last comments:</strong>

I still can't make up my mind on the design whether it is good or bad. It has potential but needs to be tested through, before it is decided that its going to be the "<strong>Web browser for GNOME". </strong>In a lot of way the ideas make sense but they don't seem practical all the time. Visually appealing does not always make the functionality usable. I know some other ideas emerged during the Desktop Summit by Hylke Bons and Garrett LeSage on an alternative view for Epiphany.

<a href="https://github.com/hbons/guadec-designs/raw/master/blog/overview.png"><img class="alignnone" title="Web2" src="https://github.com/hbons/guadec-designs/raw/master/blog/overview.png" alt="" width="605" height="336" />
</a>What I like about this is I understand it from the first look. I know how to create a new page how to navigate through stuff etc... However I do miss the thumbnails from the Web design a bit. And again where is my URL bar? Yet I LOVE THE SIDEBAR. You can check out more of the duos work <a href="https://github.com/hbons/guadec-designs">here</a>.

I think (my stupid opinion) it is to early to decide that "Web" should be the new Web browser for GNOME. I can not see where "Web" will offer me something better than Chrome or Firefox other than integration with the GNOME platform. Web won't make me ditch Epiphany. But if Epiphany is gone I am not sure I want switch to Web yet. It is missing the Umpf! :P

That being said I am done with the first phase of prototyping and you can get my code from git (you kinda need Zeitgeist for the history part since I don't feel like hacking a DB for a prototype). You can grab the prototype from <a href="https://github.com/seiflotfy/gnome-prototypes">https://github.com/seiflotfy/gnome-prototypes</a>... Again I need to underline that <strong>the implementation is a prototype which means limited (very limited) functionality to just play with the designs. The code will not be maintained and will be thrown away.</strong>

<strong>
</strong>
<h2><a href="http://dl.dropbox.com/u/7162902/shell-20111203-6.webm"><strong>Here is also a video</strong></a></h2>
<div><strong>
</strong></div>
<div><strong>
</strong></div>
<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="640" height="480" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="src" value="http://www.youtube.com/v/Et7YVxDlkEM?version=3&amp;hl=en_US&amp;hd=1" /><param name="allowfullscreen" value="true" /><embed type="application/x-shockwave-flash" width="640" height="480" src="http://www.youtube.com/v/Et7YVxDlkEM?version=3&amp;hl=en_US&amp;hd=1" allowscriptaccess="always" allowfullscreen="true"></embed></object>