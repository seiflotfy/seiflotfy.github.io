---
layout: post
title: Zeitgeist - from Python to Vala
date: '2011-11-03 18:46:17'
---

<img class="alignleft size-full wp-image-2091" title="zeitgeist" src="http://geekyogre.com/content/images/2011/11/zeitgeist.png" alt="" width="250" height="250" />

The title says it all... You can read the announcement on <a href="http://mhr3.blogspot.com/2011/11/news-from-zeitgeist-land.html">Michal Hruby's blog post</a>.  <strong>Zeitgeist</strong> has been ported <strong>from </strong><strong>Python to Vala</strong> with its latest 0.9 cycle

We started 2 weeks before the desktop summit and are now confident enough to go public alpha with our work. With the focus of the desktop environments shifting to mobiles and handhelds, we were dealing with some resistance in terms of deployments due to Python's slow start up times.  In terms of code and performance Zeitgeist is now in Vala.

For those who don't know <a href="http://en.wikipedia.org/wiki/Vala_(programming_language)">Vala</a>, its source-to-source compiled to C which is then compiled with a platform's standard C compiler, such as gcc.

It has a noticeable faster start-up time, and less memory consumption than before. A normal Zeitgeist instance that used to run for 2 days using 15-20 MB now uses around 3.5 - 7 MB (this is on my computer though).

Also Zeitgeist now allows you to read (not write) directly from the DB. We will be updating our wrapper libs to support reading from the DB directly soon... This means apps that retrieve data from the DB don't need to do it over D-Bus. However if you want to push an event into Zeitgeist you will have to do it over D-Bus. More or less you will retrieve your info faster now too...

The only thing not ported yet is the FTS extension but we managed to make it a stand-alone process that reads from the DB directly. We will have a nice awesome port soon so don't worry. We are also working on an alternative extension with the Tracker guys for the FTS.

The fun part is, all libs are still compatible which means <strong>WE DID  NOT BREAK THE API</strong>

All your current apps that use Zeitgeist should be able to run normally with this new release. Except for GAJ where we you need to grab the latest code from trunk.

For all you Git lovers another big surprise now is that we got some <a href="http://cgit.freedesktop.org/zeitgeist/zeitgeist/">mirror hosting on freedesktop.org</a> too. We have some manpower to keep launchpad and freedesktop in sync for a while. So for all Ubuntu fans keep using <a href="https://bugs.launchpad.net/zeitgeist">Launchpad</a>. For all you others use <a href="https://bugs.freedesktop.org/describecomponents.cgi?product=Zeitgeist">Bugzilla</a> :P

This Zeitgeist release has been sponsored by
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2011/11/collabora-logo-small.png"><img class="size-full wp-image-2089 aligncenter" title="collabora-logo-small" src="http://geekyogre.com/content/images/2011/11/collabora-logo-small.png" alt="" width="354" height="116" /></a></p>
<p style="text-align: center;"></p>
<p style="text-align: center;"><strong>AND</strong></p>
<p style="text-align: center;"><strong> </strong></p>
<p style="text-align: center;"><strong><a href="http://geekyogre.com/content/images/2011/11/6a00d8341fa10a53ef014e8c4fc502970d1.png"><img class="size-full wp-image-2090 aligncenter" title="6a00d8341fa10a53ef014e8c4fc502970d" src="http://geekyogre.com/content/images/2011/11/6a00d8341fa10a53ef014e8c4fc502970d1.png" alt="" width="330" height="44" /></a></strong></p>
<p style="text-align: center;"><strong>
</strong></p>


Last but not least I would like to thank the rest of the always awesome team for making this happen...

<strong>Now get it while its hot...<a href="http://launchpad.net/zeitgeist/0.9/0.9.0/+download/zeitgeist-0.8.99~alpha1.tar.bz2"> Zeitgeist 0.9 Alhpha</a></strong>

<strong>We have a little donation button on our website if you feel like donating something to the team <a href="http://zeitgeist-project.com/">http://zeitgeist-project.com/</a> for the next hackfest</strong>