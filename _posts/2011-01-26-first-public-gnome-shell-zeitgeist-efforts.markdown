---
layout: post
title: First public GNOME Shell Zeitgeist efforts
date: '2011-01-26 02:54:52'
---

Its been a while since I posted about my work on Shell + Zeitgeist

Well my last implementation was pretty much a proof of concept and since Shell did not support async searching I had to load all the Zeitgeist stuff on Shell startup. It was a HACK.

With the help of "magcius"'s async work and other on the shell channel now I am ready to have people try out my work. Sadly I am shitty with Git, so for now I will upload my whole js directory for GNOME Shell and hope someone can help me clean it up. Tomorrow I will bug the ppl on #gnome-shell to help me create a patch out of it. This is how it looks like now...

<a href="http://geekyogre.com/content/images/2011/01/Screenshot.png"><img class="alignnone size-large wp-image-1743" title="Screenshot" src="http://geekyogre.com/content/images/2011/01/Screenshot-1024x576.png" alt="" width="614" height="346" /></a>

And also <a href="http://www.youtube.com/watch?v=jRPNTWU_4iU">here is a video</a> (GNOME Shells screencast recorder really makes things slower)

<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="480" height="385" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="src" value="http://www.youtube.com/v/jRPNTWU_4iU?fs=1&amp;hl=en_US" /><param name="allowfullscreen" value="true" /><embed type="application/x-shockwave-flash" width="480" height="385" src="http://www.youtube.com/v/jRPNTWU_4iU?fs=1&amp;hl=en_US" allowscriptaccess="always" allowfullscreen="true"></embed></object>

Whats missing is to get this ROCK SOLID and test out the async calls and breaking set calls in case new results come in.

Tomorrow I will clean up my "Desktop" category  and provide you with an updated version of...

<a href="http://geekyogre.com/content/images/2010/12/Screenshot1.png"><img class="alignnone size-large wp-image-1696" title="Screenshot" src="http://geekyogre.com/content/images/2010/12/Screenshot1-1024x640.png" alt="" width="614" height="384" /></a>

Get the js directory here... .<a href="http://geekyogre.com/content/images/2011/01/js.tar.gz">js.tar</a> and replace it with the js directory in gnome-shell/js

P.S: me and Git don't get along at all :(