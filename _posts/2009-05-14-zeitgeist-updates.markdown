---
layout: post
title: Zeitgeist updates
date: '2009-05-14 10:49:17'
---

Well after a loooooooong week on Zeitgeist here are some issues we are facing.

<strong>Engine:</strong>
<p style="margin-bottom: 0in;">At the moment the engine is very stable and very small modifications are happening (a little DB change and tagging issues). We will be exporting all Dataproviders into their own package making the engine a standalone of its own (could also ease up integration with other projects). Before GUADEC however 3 new features will be implemented:</p>

<ol>
	<li>Timemachine: We had it in one of our 	first revisions but I had to take it out. Well it will be back with 	a respective Nautlius plugin to open an editable file form a 	specific timestamp.</li>
	<li>Predicting data related to the current 	activity and predicting intensity of future activities (Got that 	from school.</li>
	<li>Blacklisting data from being logged 	(donkey porn :P)</li>
</ol>
<strong>UI:</strong>

Now this is an issue of its own. Our current Gtk UI works with the engine via DBus and we don't intend to change that. Unlike the Engine the UI really needs some changes and concepts. We modified a lot and are facing some usability issues that <a href="http://davebsd.com/">David Siegel</a> pointed out on a mail.
<blockquote>You need to think about how people will use it! You ask "how do you intend of viewing all your activities?" but this is an INVALID question. People aren't interested in a view of all of their activities -- only geeks and people hacking GNOME Zeitgeist are interested in that. Users only want to accomplish their objectives, not play around with G-Z and get a big overview.</blockquote>
I got 3 poker buddies and 2 girls from the building who are very limited computer users for a test drive:
<ol>
	<li>When they look back in time they 	already know what they are looking for as in what type it is, for 	them having so many items is pretty scary and messy making scrolling 	up and down very hard to find what they want.</li>
	<li>They would only like to view a 	sequence of activities when they find what they need "X" 	(maybe an optional timeline around an item in a new view) maybe to 	find someting they did while working on "X"</li>
	<li>They dislike the too many buttons</li>
	<li>only one girl and one guy were 	able to work with tags (sometimes i am disappointed in germans) and 	loved it, however tags should be easier modifiable</li>
	<li>one of them preferred a vertical 	timeline with the as in days above each other for easier scrolling 	another one preferred one day per per view</li>
	<li>all liked the searching but they thought it is stupid to view 	several instances on several dates (was working on it that way for 	later reversioing)</li>
</ol>
So concerning point 1) I tried to change the view a bit and grouped the data in it by type.

<!-- 		@page { margin: 0.79in } 		P { margin-bottom: 0.08in } -->

<a href="http://geekyogre.com/content/images/2009/05/screenshot-gnome-zeitgeist.png"><img class="alignnone size-medium wp-image-651" title="screenshot-gnome-zeitgeist" src="http://geekyogre.com/content/images/2009/05/screenshot-gnome-zeitgeist-300x119.png" alt="" width="300" height="119" /></a> <a href="http://geekyogre.com/content/images/2009/05/screenshot-gnome-zeitgeist-1.png"><img class="alignnone size-medium wp-image-652" title="screenshot-gnome-zeitgeist-1" src="http://geekyogre.com/content/images/2009/05/screenshot-gnome-zeitgeist-1-300x119.png" alt="" width="300" height="119" /></a>

as opposed to the old view which allowed you to track the actual history of your activities.

<a href="http://geekyogre.com/content/images/2009/05/screenshot-gnome-zeitgeist-2.png"><img class="alignnone size-medium wp-image-653" title="screenshot-gnome-zeitgeist-2" src="http://geekyogre.com/content/images/2009/05/screenshot-gnome-zeitgeist-2-300x145.png" alt="" width="300" height="145" /></a>

I see the usage of both. When the rest of them team had a look at it you could see the real difference between them. Those working on documentation and filing bugs preferred the grouped one while the hackers all preferred the sequential view. Thus both have to be there but which one per default? This point is actually very important in my opinion.

<strong>NEXT WEEK:</strong>

So in 10 days I will be at UDS meeting up with RainCT (my enslaved GSoC student), David and the Do gang, to discuss further issues and release a roadmap for Zeitgeist. Really looking forward to it.