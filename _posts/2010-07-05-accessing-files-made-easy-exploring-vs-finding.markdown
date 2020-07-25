---
layout: post
title: Accessing files made easy - Exploring vs Finding
date: '2010-07-05 17:16:35'
---

As part of the Elementary Project we are trying to find easy ways to access the documents, videos, notes, etc...

Recently I experienced second hand how painful accessing documents is while trying to get my grandmother and mother to open recent photos on my brothers computer. He also uses Ubuntu just like my mom. But he uses Do to do everything and his layout is very similar to mine (global-menu bar + docky).

Now my mom couldn't get around much and later she called me. I told her to open the Pictures Folder. This also took a while for her to figure out where to find it. If it was the normal panel layout it would have been easier for her. However for my grandma it still would have been a pain in the ass since she doesn't understand the concept of folders.

So lets take a simple use case. You want to access a document but don't know where it is exactly.

------------

This issue is already being tackled by Shell as seen here...

<a href="http://live.gnome.org/GnomeShell/Design/Whiteboards/FindingAndReminding?action=AttachFile&amp;do=get&amp;target=desktop-view.png"><img class="alignnone" title="Shell" src="http://live.gnome.org/GnomeShell/Design/Whiteboards/FindingAndReminding?action=AttachFile&amp;do=get&amp;target=desktop-view.png" alt="" width="614" height="461" /></a>

To reach this layout we need to click the following "Activities -&gt; Desktop -&gt; Documents". If you ask me this looks nice but is not intuitive enough. Why should one click on "Activities" if one wants to find a document. Clicking over 3 menus is sort of "exploring to find".

------------

Then you can see here how unity does it.

<a href="http://lh4.ggpht.com/_1QSDkzYY2vc/TCUCQ-JvcYI/AAAAAAAABVM/BJ0kHZDnILc/Workspace%201_033.png"><img class="alignnone" title="unity" src="http://lh4.ggpht.com/_1QSDkzYY2vc/TCUCQ-JvcYI/AAAAAAAABVM/BJ0kHZDnILc/Workspace%201_033.png" alt="" width="576" height="304" /></a>

Here you will have to click the (ubuntu logo -&gt; places -&gt; documents (if not found under All Files)). Again very simple but is this intuitive. Why would my grandmother click that logo? For me this is exploring.

Now i agree with both designs that the access should be embedded in the shell, it would be even harder for people to click and open a filebrowser (nautilus) to find their stuff. However after being put in this situation I differ in the execution of set concept.

We need to be able to say documents or music and have something on the screen that gives you quick access to them. At the elementary project we have been sturggeling to find a way to provide such experience in a well designed and good looking form. <a href="http://reflaction.info">Thorsten Prante</a> and I spent much time thinking of a way to make give access over finding. So at some point the agreed on using Sezen as a base for this and integrating it into the desktop (not nautilus) rather than having it as a standalone app.

Currently we are playing with the following designs.

<a href="http://elementary-project.com/abuse/sezenmenu.png"><img class="alignnone" title="sezen" src="http://elementary-project.com/abuse/sezenmenu.png" alt="" width="533" height="498" /></a>

and our GSoC student did this...

<a href="http://ubuntuone.com/p/8nn"><img class="alignnone" title="spanel" src="http://ubuntuone.com/p/8nn" alt="" width="608" height="380" /></a>

However we will rename Places to Library in that case. This should make things more obvious and accessible over 2 clicks "Library -&gt; Documents". Its not much exploring anymore as the before. The only point to be argued about is the naming, Places or Library? How can I name a button to hint me that "Documents" can be found under it?

-----------

Next we have a prototype implementation of a Sezen panel that looks more like this.

<a href="http://geekyogre.com/content/images/2010/07/Screenshot-16.png"><img class="alignnone size-full wp-image-1308" title="Screenshot-16" src="http://geekyogre.com/content/images/2010/07/Screenshot-16.png" alt="" width="614" height="384" /></a>

It gvies you access directly to your stuff. So if you tell someone go to documents its a one click destination. Not exploring but actually u will find it by looking at the screen.

Yet maybe its not "cool" enough. And navigating through with a keyboard could be a pain in the ass.

So we tried this...

<a href="http://a.yfrog.com/img692/8392/ps1d.png"><img class="alignnone" title="sezen" src="http://a.yfrog.com/img692/8392/ps1d.png" alt="" width="614" height="384" /></a>

Here it seems to cluttered.

This is a case where design and usability clash. I think its more usable to have "documents", "audio", etc. appear in the front yet it just looks to cluttered. When trying to reduce the clutter the intuitiveness is lost and thus usability suffers.

All in all this issue has been bothering me for days now. Please join us at #elementary and #zeitgeist on freenode to discuss this issue.

<strong>P.S: I know the panel is deprecated, this is just a brainstorm.</strong>