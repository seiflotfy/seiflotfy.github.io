---
layout: post
title: New thoughts on GNOME-Zeitgeist
date: '2009-02-20 09:40:50'
tags:
- clutter
- gnome
- hacking
- logging
- python
- zeitgeist
---

After a not so perfect exam I decided to go crazy on Zeitgeist. Here are my new thoughts:

<strong>1. Clutter</strong>: First I decided to fiddle around with clutter ending up with <a href="http://geekyogre.com/content/images/2009/02/out.ogv">THIS</a>. So now I learned more about clutter and decided to give Zeitgeist a nice alternative UI. Most probably Kalle Perrsons <a href="http://dl.getdropbox.com/u/107961/zg-spacetravel.png">mock up</a>. The concept will is zooming into each day only showing 5 days at a time. Its pretty simple.
<strong></strong>

<strong>2. More data providers</strong>: Problem is, for me to log the activity, the application used to edit or open the file has to insert its data into gtk RecentlyUsed. Most GNOME applications do that. However some of the applications I use don't, e.g: Eclipse, VLC, Firefox and Rhytmbox. We will write plugins for them if we find the file (mostly XML or SQLite) with its usage history. Once found we will drop a file monitor taken from "Gimmie" on it and scan for changes to notify Zeitgeist to log. It is done with Tomboy already (Just copied it from Gimmie). We will be applying this mechanism on the current Firefox and Evolution plugin. Soon Rhythmbox and Pidgin plugins will be written. Once done we can start working on a ........
<strong></strong>

<strong>3. GTK Bar</strong>: My idea would be implementing a bottom bar (I will call it activity-bar) displaying the timeline of my day, which I can scroll through. This could actually replace my task bar. This is just an idea though! A little search bar on the side wouldn't hurt. There will be an icon to open a more sophisticated view of your activity history (the current Zeitgeist view). One should be able to quick tag data/activities in the activity-bar.
<strong></strong>

<strong>4. Tags</strong>: Tagging in Zeitgeist works like charm. Even the most common tags are displayed as filters on the top bar. However tagging itself can be a pain in the ass. We need to be able to multi select items and tag them all together.

<span class="status-body"><span class="entry-content"><strong>5. Automatic tagging:</strong><em><strong> </strong></em>Wouldn't it be neat if once could set up some kind of task manager that can get activated. During the time its running every activity should be tagged with the task name, until its deactivated. Even activities should have their blacklists like in relationships to prevent tagging some unrelated items.
</span></span>
<span class="status-body"><span class="entry-content"><strong>6. Nautilus tagging:</strong><em><strong> </strong></em>It would be cool if one could tag items from Nautilus and write them into the Zeitgeist database.</span></span>

<strong>7. Related Items</strong>: We were thinking of how one could define relationships between Data. We came up with three categories of relationships:
<ul>
	<li><em><strong>Tags:</strong> </em>Items sharing the same tags are definitely related.</li>
	<li><strong><em>RDF:</em></strong> After reading about <a href="http://www.organise-fw.org/">Organise Framwork</a> I got in contact with Sebastian Faubel and I was impressed. We hit it off really well and are currently planing a workshop in Nuernberg to work somehow on finding an intersection point for both Projects. If we can feed the data we collected with RDF, figuring out relationships should be easy as hell.</li>
	<li><em><strong>Behaviour based relationships:</strong></em> Will not write about it here<span class="status-body"><span class="entry-content"> since it is part of my BSc Thesis and Thorsten's PhD work. But it is possible...
</span></span></li>
</ul>
<span class="status-body"><span class="entry-content">Another feature should be a blacklist to determine that some items should not be related. No one wants to see porn and work together in one window.</span></span>
<span class="status-body"><span class="entry-content"><em><strong></strong></em></span></span>

<span class="status-body"><span class="entry-content"><strong>8. Plugin Manager:</strong> We need to be able to activate/deactivate data providers thus enabling/disabling logging.</span></span>

<strong>9. Provide GNOME Do with our logs:</strong> By now everyone is using or heard of GNOME Do and with docky rocking I thought why only provide the user with applications and songs why not use Zeitgeist to figure out which docs and websites have been used lately and display them in the dock. Thus making a point 3 irrelevant.

<strong>10. Time machine functionality:</strong> Why not store the first occurrence of an editable file and then for every following activity of this file store the "diff", making it easy to restore any kind of editable file by applying the patches sequentially from the first occurrence till the timestamp. I know there are projects like wizbit out there tackling this issue, but they do more complex stuff. For these purposes i think its enough!

<a href="http://www.gnome.org/~federico/">Federico</a> has been helping us out alot lately and I hope we can find some time to give him a better demonstration of what Zeitgeist can do soon.

As for now I will leave you with my thoughts and call my girlfriend :)