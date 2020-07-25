---
layout: post
title: More Software-Center with Zeitgeist for dessert
date: '2010-10-09 13:04:44'
---

So after some talk with the Software Center team I took matters into hand into making some of the ideas reality.

This time we wanted to make the "Recommended Applications" as seen in the following mock-up reality.

<img class="alignnone" title="mockup" src="https://wiki.ubuntu.com/SoftwareCenter?action=AttachFile&amp;do=get&amp;target=future-lobby.jpg" alt="" width="750" height="526" />

But how do we determine the recommendations... (Zeitgeist):
<ul>
	<li>Software Center asks Zeitgeist for most used mime-types within the last 30 days limited to 1000 events.</li>
	<li>Software Center looks for uninstalled applications that can handle these mime-types.</li>
	<li>Take first 3 results of the applications lists for each mime-type and set as recommendation (This has to be done more intelligently)</li>
</ul>
This now looks like

<a href="http://geekyogre.com/content/images/2010/10/Screenshot.png"><img class="alignnone size-full wp-image-1615" title="Screenshot" src="http://geekyogre.com/content/images/2010/10/Screenshot.png" alt="" width="716" height="515" /></a>

<a href="http://geekyogre.com/content/images/2010/10/Screenshot-1.png"><img class="alignnone size-full wp-image-1614" title="Screenshot-1" src="http://geekyogre.com/content/images/2010/10/Screenshot-1.png" alt="" width="710" height="513" /></a>

There are instructions on <a title="OMG!Ubuntu!" href="http://www.omgubuntu.co.uk/2010/10/more-zeitgeist-integration-in-software-center-shows-recommended-apps-based-on-usage/">OMG!Ubuntu!</a> how to get the branch...

Here is a little <a href="http://www.youtube.com/watch?v=V85oQ1ma16o">video</a> of it in action
<iframe title="YouTube video player" class="youtube-player" type="text/html" width="480" height="375" src="http://www.youtube.com/embed/V85oQ1ma16o?hd=1" frameborder="0"></iframe>

Lets hope the S-C and Design team are happy with this integration so I can clean it up and propose it for merging.