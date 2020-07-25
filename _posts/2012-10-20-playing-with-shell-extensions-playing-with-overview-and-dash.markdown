---
layout: post
title: Playing with Shell extensions (playing with overview and dash)
date: '2012-10-20 01:13:07'
---

Today I worked on hiding the workspace switcher if "dynamic-workspaces" is switched off (via tweak-tool) and the number of workspaces is set to one only.  So if you apply these settings your overview will look as follows.

<a href="http://geekyogre.com/content/images/2012/10/Screenshot-from-2012-10-20-014915.png"><img class="wp-image-2350 aligncenter" title="Screenshot from 2012-10-20 01:49:15" src="http://geekyogre.com/content/images/2012/10/Screenshot-from-2012-10-20-014915.png" alt="" width="461" height="288" /></a>

Pretty clean huh? This patch is now upstream (merged into master) for everybody to enjoy :D

So I noticed less clutter with this patch, and the motivation to try to reduce the clutter even more as well as play with the extension hooks got me hacking more.

I am a big fan of the sidebar since it reduces movement when coming from the top left (after hovering over activities) to move the mouse along the left edge of the screen to open a new app or change apps. But somehow I still get the feeling that left is out of place for me sometimes.

So I came up with an idea (and although I know its wrong and I deserve being stabbed for it):

Why not move the dash into the MessageTray. So I started writing an extension to do so (very early stages). This extension allows me to open new apps and browse through my apps as well as change windows (Windows style :P) by just hovering to the bottom of the screen, so it pops up.

<a href="http://geekyogre.com/content/images/2012/10/Screenshot-from-2012-10-20-012451.png"><img class="wp-image-2351 aligncenter" title="Screenshot from 2012-10-20 01:24:51" src="http://geekyogre.com/content/images/2012/10/Screenshot-from-2012-10-20-012451.png" alt="" width="461" height="288" /></a>

clicking on the "show apps" or "journal" icons takes me to the overview with the proper page selected. (So clicking on "show apps" opens the overview with the application selection)

<a href="http://geekyogre.com/content/images/2012/10/Screenshot-from-2012-10-20-011925.png"><img class="wp-image-2352 aligncenter" title="Screenshot from 2012-10-20 01:19:25" src="http://geekyogre.com/content/images/2012/10/Screenshot-from-2012-10-20-011925.png" alt="" width="461" height="288" /></a>

And when going to "Activities" directly, it looks much more peaceful:

<a href="http://geekyogre.com/content/images/2012/10/Screenshot-from-2012-10-20-011839.png"><img class="wp-image-2353 aligncenter" title="Screenshot from 2012-10-20 01:18:39" src="http://geekyogre.com/content/images/2012/10/Screenshot-from-2012-10-20-011839.png" alt="" width="461" height="288" /></a>

The bad thing is that it mixes notifications with applications. So I am thinking of having some sort of separator.

What do you guys think?

Keep in mind this is just hacks and nothing discussed with designers. I am just playing with ideas here and will try to make an extension out of this if people like the concept and have some feedback on how to improve it.