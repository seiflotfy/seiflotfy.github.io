---
layout: post
title: 'Docky: mastering the art of jump lists with Zeitgeist'
date: '2010-12-19 15:24:00'
---

As an avid docky user (sometimes I switch to AWN depending on my mood), I got very used to the jumplists. But at some point I was not satisfied with what I hacked before, since it was based on the early 0.3 Zeitgeist API. I decided to revisit it and fixed the following:
<ol>
	<li>Refresh jump list upon application activity, allowing a more real-time change of the jump list, instead of updating every 5 minutes.</li>
	<li>Detect duplicate names of items in the jump lists and extend those with the path to the items.</li>
	<li>Exclude unreachable items in jump list, such as files on an unmounted USB.</li>
	<li>Open items with the respected application instead of the default.</li>
	<li>Populate jump lists for folders recursively.</li>
</ol>
For me its now much more usable and I am pretty happy with it. With the upcoming Zeitgeist 0.7 release there will be major speed improvements. With the 0.8 release we will be able to detect where files moved to. This way the Docky + Zeitgeist experience will just rock.

The code of this update is being reviewed by Rico and I will try to bring these features to both GNOME Shell and Unity ASAP.

Here are some screenshots and a video...

<a href="http://geekyogre.com/content/images/2010/12/Screenshot2.png"><img class="alignnone size-medium wp-image-1704" title="Screenshot" src="http://geekyogre.com/content/images/2010/12/Screenshot2-300x187.png" alt="" width="300" height="187" /></a> <a href="http://geekyogre.com/content/images/2010/12/Screenshot-11.png"><img class="alignnone size-medium wp-image-1705" title="Screenshot-1" src="http://geekyogre.com/content/images/2010/12/Screenshot-11-300x187.png" alt="" width="300" height="187" /></a>

<a href="http://geekyogre.com/content/images/2010/12/Screenshot-2.png"><img class="alignnone size-medium wp-image-1706" title="Screenshot-2" src="http://geekyogre.com/content/images/2010/12/Screenshot-2-300x187.png" alt="" width="300" height="187" /></a>

<a href="http://www.youtube.com/watch?v=3I6pO7fKJnU"><strong>And you can watch the video here</strong></a>

<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="480" height="385" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="src" value="http://www.youtube.com/v/3I6pO7fKJnU?fs=1&amp;hl=en_US" /><param name="allowfullscreen" value="true" /><embed type="application/x-shockwave-flash" width="480" height="385" src="http://www.youtube.com/v/3I6pO7fKJnU?fs=1&amp;hl=en_US" allowscriptaccess="always" allowfullscreen="true"></embed></object>