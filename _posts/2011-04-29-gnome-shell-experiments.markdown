---
layout: post
title: GNOME Shell Experiments
date: '2011-04-29 21:55:51'
---

So now that GNOME 3 is out, and I am excited about the future progress of the "<a href="http://live.gnome.org/ThreePointOne/Features/FindingAndReminding">Finding and Reminding</a>" feature. My design philosophy is that design should be an evolutionary process with multiple prototypes tested for effectiveness along the way, not a "design everything upfront" process.

Along with Federico Mena and Siegfried Gevatter, and Akshaj Gupta working with us as a SoC student, we have been working on rapid prototypes of our own "Finding and Reminding" ideas and also have been working on cleaning up of those prototypes.

We will refocus our work to assist the GNOME Shell team once their designs are complete. Until then I would like to invite people to play with my branch on gitorious (<a href="https://gitorious.org/gnome-shell-zeitgeist/gnome-shell-zeitgeist/commits/desktop">https://gitorious.org/gnome-shell-zeitgeist/gnome-shell-zeitgeist/commits/desktop</a>)

This branch adds 3 new features to GNOME-Shell:
<ul>
	<li><strong>Jumplists</strong>: (Right clicking on an app in the dash or the IconGrid opens a menu with the 4 Recently used files with the applications)</li>
	<li><strong>Search</strong>: (Searching now looks in Zeitgeist for all your most used documents mathcing your strings… This can be done via Tracker too and I have a zeitgeist-extension that pulls the search results from Tracker and sorts them via zeitgeist)</li>
	<li><strong>Library</strong> Tab: A vague implementation of the design ideas from the gnome wiki</li>
</ul>
<div><strong>Here are pictures and a video of what this branch can do...</strong></div>
<div><strong>
</strong></div>
<div>
<p style="text-align: center;"><em>Jumplists</em></p>
<p style="text-align: center;"><em><a href="http://geekyogre.com/content/images/2011/04/Screenshot-80.png"><img class="size-medium wp-image-1891  aligncenter" title="Screenshot-80" src="http://geekyogre.com/content/images/2011/04/Screenshot-80-300x187.png" alt="" width="300" height="187" /></a>
</em></p>

<p style="text-align: center;"><em>Library</em></p>
<p style="text-align: center;"><em><a href="http://geekyogre.com/content/images/2011/04/Screenshot-81.png"><img class="size-medium wp-image-1891  aligncenter" title="Screenshot-81" src="http://geekyogre.com/content/images/2011/04/Screenshot-81-300x187.png" alt="" width="300" height="187" /></a>
</em></p>

<p style="text-align: center;"><em>Search</em></p>
<p style="text-align: center;"><em><a href="http://geekyogre.com/content/images/2011/04/Screenshot-82.png"><img class="size-medium wp-image-1891  aligncenter" title="Screenshot-82" src="http://geekyogre.com/content/images/2011/04/Screenshot-82-300x187.png" alt="" width="300" height="187" /></a>
</em></p>

</div>
<p style="text-align: center;"></p>
<p style="text-align: center;"></p>
<p style="text-align: center;"></p>
<p style="text-align: center;"></p>

<p style="text-align: center;"><object style="height: 390px; width: 640px;" classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="100" height="100" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowScriptAccess" value="always" /><param name="src" value="http://www.youtube.com/v/hViWJ35GXr8?version=3" /><param name="allowfullscreen" value="true" /><embed style="height: 390px; width: 640px;" type="application/x-shockwave-flash" width="100" height="100" src="http://www.youtube.com/v/hViWJ35GXr8?version=3" allowscriptaccess="always" allowfullscreen="true"> </embed></object>


To test it you will need the latest Zeitgeist packages from from your distribution or get the source code from:
<ul>
	<li><strong>Engine</strong>: <a href="https://launchpad.net/zeitgeist">https://launchpad.net/zeitgeist</a> (the main engine)</li>
	<li><strong>Datahub</strong>: <a href="https://launchpad.net/zeitgeist-datahub">https://launchpad.net/zeitgeist-datahub</a> (the main logger)</li>
	<li><strong>FTS-Extension</strong>: <a href="https://launchpad.net/zeitgeihttp://bazaar.launchpad.net/%7Ezeitgeist-extensions/zeitgeist-extensions/trunk/download/head:/fts.py-20100602085111-i21bh1p60phaak4f-2/fts.pyst-datahub">http://bazaar.launchpad.net/~zeitgeist-extensions/zeitgeist-extensions/trunk/download/head:/fts.py-20100602085111-i21bh1p60phaak4f-2/fts.py</a> (place it in .local/share/zeitgeist/extensions)</li>
	<li><strong>Extra Loggers</strong>: If you want to log some extra stuff you can download other loggers from <a href="http://bazaar.launchpad.net/%7Ezeitgeist-dataproviders/zeitgeist-dataproviders/trunk/files">http://bazaar.launchpad.net/~zeitgeist-dataproviders/zeitgeist-dataproviders/trunk/files</a></li>
</ul>
Some nice ideas worth experimenting would be to replace some Zeitgeist stuff with Tracker stuff and test... I already started with some Zeitgeist extensions that make this possible.

This work is in no way what you should expect from the "Finding and Reminding" stuff that is being designed. With a lot of luck there might be some stuff pulled into the main design. But it would be nice to have feedback.

Play with it, tell me what's bothering you, or what you like at #gnome-shell-experiments on gimpnet (irc.gimp.org).
Let's encourage prototypes and testing. While prototypes does not mean the code will be used, it is a good way to have a more agile development and interactive design process, that could help out the GNOME Shell designers with their decisions.

If you've got ideas on how to improve GNOME shell's ability to "Find and Remind", send us your sketches, mockups, and ideas and we'll work with you to develop rapid prototypes and test your ideas and theories.

You can post them on <a href="http://live.gnome.org/GnomeShell/Experiments">http://live.gnome.org/GnomeShell/Experiments</a> or drop by #gnome-shell-experiments</p>