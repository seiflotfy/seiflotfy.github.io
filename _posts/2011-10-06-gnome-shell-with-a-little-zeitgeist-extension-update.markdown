---
layout: post
title: GNOME Shell with a little Zeitgeist (Extension update)
date: '2011-10-06 22:00:58'
---

So I finally managed to finish all Zeitgeist extensions I wanted for GNOME Shell...
<h2><strong>Journal</strong></h2>
The first extensions adds the "Journal" overview which allows you to navigate through your Recently Used stuff categorized by type of files (documents/videos/music/other/...) as well as type of interaction (recent/frequent/new). This is something Akshay Gupta, Federico Mena and me have been working on and we will be working on it more in the coming weeks to fix and improve the view...

<a href="http://geekyogre.com/content/images/2011/10/Screenshot-at-2011-10-06-222200.png"><img class="alignnone size-full wp-image-2027" title="Screenshot at 2011-10-06 22:22:00" src="http://geekyogre.com/content/images/2011/10/Screenshot-at-2011-10-06-222200.png" alt="" width="768" height="480" /></a>
<h2>Zeitgeist-Search</h2>
One of the most annoying things about the Shell search is the semi-random order of results we get for matching applications (see <a href="https://bugzilla.gnome.org/show_bug.cgi?id=623372">https://bugzilla.gnome.org/show_bug.cgi?id=623372</a>)

Also the search in recently used could be improved by categorizing them by types (documents/videos/etc..)

<a href="http://geekyogre.com/content/images/2011/10/Screenshot-at-2011-10-06-222907.png"><img class="alignnone size-full wp-image-2028" title="Screenshot at 2011-10-06 22:29:07" src="http://geekyogre.com/content/images/2011/10/Screenshot-at-2011-10-06-222907.png" alt="" width="768" height="480" /></a>
<h2><strong>Jump-lists</strong></h2>
Last but not least I managed to finish a jump-list extension that is pretty nifty and works like charm. Basically if your application reports to Zeitgeist what it is doing (install datap sources from <a href="https://code.launchpad.net/~zeitgeist-dataproviders/zeitgeist-datasources/trunk">https://code.launchpad.net/~zeitgeist-dataproviders/zeitgeist-datasources/trunk</a>) you will have the awesome functionality of being able to right click on an app and retrieving the 4 recent items used with it as well as other 3 frequent items used.

<a href="http://geekyogre.com/content/images/2011/10/Screenshot-at-2011-10-06-223848.png"><img title="Screenshot at 2011-10-06 22:38:48" src="http://geekyogre.com/content/images/2011/10/Screenshot-at-2011-10-06-223848.png" alt="" width="768" height="480" /></a>
<h2>Where to get it?</h2>
Simple just get it from my git repo (<a href="https://github.com/seiflotfy/gnome-shell-zeitgeist-extension">https://github.com/seiflotfy/gnome-shell-zeitgeist-extension</a>) by doing

<strong>git clone git://github.com/seiflotfy/gnome-shell-zeitgeist-extension.git</strong>

<strong><span style="color: #ff0000;">YOU NEED ZEITGEIST TO RUN THIS make sure that both zeitgeist-daemon and zeitgeist-datahub are running</span></strong>
<h2><strong>
</strong></h2>
<h2>Credits...</h2>
Thanks to Federico and Akshay for their amazing work and Jasper St. Pierre and Colin Walters for guiding me through the unconventional methods to get this running. Also thanks to Collabora for sponsoring my efforts...

<a href="http://www.youtube.com/watch?v=spUkEu46TjU">Here is a video demo of the 3 extensions</a> or <strong>download it from <a href="http://dl.dropbox.com/u/7162902/shell-20111006-3.webm">here</a></strong>

<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="640" height="480" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="src" value="http://www.youtube.com/v/spUkEu46TjU?version=3&amp;hl=en_US&amp;hd=1" /><param name="allowfullscreen" value="true" /><embed type="application/x-shockwave-flash" width="640" height="480" src="http://www.youtube.com/v/spUkEu46TjU?version=3&amp;hl=en_US&amp;hd=1" allowscriptaccess="always" allowfullscreen="true"></embed></object>