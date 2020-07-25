---
layout: post
title: One year Zeitgeist sponsorship by Collabora
date: '2011-12-07 22:21:44'
---

This month <a href="http://www.collabora.com/">Collabora</a> has been sponsering zeitgeist for one year, here is the story about how that came to be and what happened during that year.
<h3><strong>How I got in contact with Collabora?</strong></h3>
I met Rob McQueen, Phillippe Khalaf, Sjoerd and some from the Telepathy team during Gran Canaria Desktop summit. I needed help with an idea (Teamgeist) and a couple of months later I was introduced to Youness Alaoui (until this day I consider a very good and close friend) as well as Sumana Harihareswara (from whom I learned a lot about organizing).
<h3><strong>How I got sponsored?</strong></h3>
Collabora saw Zeitgeist as a promising technology and observed the development for a while. They wanted to leverage it in GNOME more. After I tried to do some work on GNOME Shell last year, I was approached by them and they offered to sponsor my work, integrating Zeitgeist into GNOME as well as work on Zeitgeist. They also put two of their developers, Abner Silva and JP Whiting, to work on the Zeitgeist Qt bindings for a while.
<h3><strong>What I did during the year?</strong></h3>
I mainly get sponsored for working on Zeitgeist and related stuff for GNOME and KDE  (development, bug fixing and specs definition). Some of the things I worked on were:
<ul>
	<li><strong>Zeitgeist extensions for GNOME Shell: </strong>The purpose of the extensions is to integrate some Zeitgeist experience into GNOME Shell. The experience comes in form of three extensions (you can grab the source from <a href="https://www.gitorious.org/gnome-shell-zeitgeist-extension">here</a>)</li>
</ul>
<ul>
	<li><em><strong>Jumplists: </strong></em>Displays the recently/most used files used with the apps  displayed in GNOME Shell. The extension has been uploaded to <a href="https://extensions.gnome.org/extension/33/jump-lists/">extensions.gnome.org</a></li>
</ul>
<p style="text-align: center;"><strong><a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-152852.png"><img class="size-full wp-image-2153" title="Screenshot at 2011-12-07 15:28:52" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-152852.png" alt="" width="461" height="288" /></a></strong></p>

<ul>
	<li style="text-align: left;"><strong><em>Journal</em></strong>: Zeitgeist based activity-history journal as a gnome-shell overview tab. It allows you to access you files via GNOME Shell and sorts them for you in chronological order. The extension has been uploaded to <a href="https://extensions.gnome.org/extension/33/jump-lists/">extensions.gnome.org</a></li>
</ul>
<p style="text-align: center;"><strong> <a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-162627.png"><img title="Screenshot at 2011-12-07 16:26:27" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-162627.png" alt="" width="461" height="288" /></a></strong></p>
<p style="text-align: center;"><strong></strong><a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-162608.png"><img class="size-full wp-image-2156" title="Screenshot at 2011-12-07 16:26:08" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-162608.png" alt="" width="461" height="288" /></a></p>

<ul>
	<li><em><strong>Search: </strong></em>Makes the Shell search via Zeitgeist and and categorize the results better. I will upload it to the extensions website when the highlighting issue is fixed.</li>
</ul>
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-153023.png"><img class="size-full wp-image-2154 aligncenter" title="Screenshot at 2011-12-07 15:30:23" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-153023.png" alt="" width="461" height="288" /></a></p>

<ul>
	<li><strong>El Loco:  </strong>A Tool to browse you activities at a current Location. Go on the map and click on the town or street and you will be able to see what/who you interacted with there. It is pretty unique in what it offers but needs more UI design, since until now it served primarily a demo application, Ted Gould and I ported it to Gtk3 (<a href="https://code.launchpad.net/~seif/+junk/ellocco">https://code.launchpad.net/~seif/+junk/ellocco</a>) as well as to Qt (<a href="https://code.launchpad.net/~seif/+junk/qt-lav">https://code.launchpad.net/~seif/+junk/qt-lav</a>).</li>
</ul>
<div style="text-align: center;"><a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-203441.png"><img class="alignnone size-full wp-image-2161" title="Screenshot at 2011-12-07 20:34:41" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-203441.png" alt="" width="461" height="288" /></a></div>
<ul>
	<li><strong></strong><strong>Activity Log Manager: </strong>Due to popular demand we needed to hack on a privacy tool. Along side Manish Sinha, JP Lacerda, Stefano Candori and Siegfried Gevatter, we developed ALM. It is a graphical user interface which lets you easily control what gets logged by Zeitgeist. It supports setting up blacklists according to several criteria (such as application or file types), temporarily stopping all logging as well as deleting recent events. ALM will be seeing deeper integration into Ubuntu and hopefully GNOME too soon. You can grab the code from <a href="https://code.launchpad.net/activity-log-manager">here</a>.</li>
</ul>
<div style="text-align: center;"> <a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-205710.png"><img class="alignnone size-full wp-image-2180" title="Screenshot at 2011-12-07 20:57:10" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-205710.png" alt="" width="225" height="195" /></a> <a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-211641.png"><img class="alignnone size-full wp-image-2183" title="Screenshot at 2011-12-07 21:16:41" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-211641.png" alt="" width="224" height="195" /></a> <strong style="font-size: 15px;"><a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-211915.png"><img title="Screenshot at 2011-12-07 21:19:15" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-211915.png" alt="" width="222" height="195" /></a></strong></div>
<ul>
	<li><strong>Gedit Dashboard: </strong>Michal Hruby's idea during the hackfest has become reality, after Hylke Bons and I spent almost a month working on it from scratch. The idea was to have a "Google Chrome"-like dashboard for gedit as well as a quick search. The patient and kind Gedit folks helped me clean up the code and now its part of gedit-plugins. This is my favorite plugin for gedit now. You can get it from <a href="http://git.gnome.org/browse/gedit-plugins/">http://git.gnome.org/browse/gedit-plugins</a>.</li>
</ul>
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-212521.png"><img title="Screenshot at 2011-12-07 21:25:21" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-212521.png" alt="" width="461" height="288" /></a></p>
<p style="text-align: center;"><a style="text-align: center;" href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-212521.png"><img title="Screenshot at 2011-12-07 21:25:21" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-212521.png" alt="" width="461" height="288" /></a></p>

<ul>
	<li><strong>libqzeitgeist (now maintained by the amazing Trever Fischer): </strong>libqzeitgeist was developed by Abner Silva and JP Whiting. It allows easier development for KDE apps. It is used in Trever's <a href="https://projects.kde.org/projects/kde/kde-runtime/repository/show?rev=tdfischer%2Fzeitgeist-activity-manager">plugin for KDE Activity Manager</a> to push events directly into Zeitgeist. Trever is now maintaining the library and added QML support. You can find the work <a href="http://quickgit.kde.org/?p=libqzeitgeist.git&amp;a=summary">here</a>.</li>
</ul>
<ul>
	<li><strong>Zeitgeist Engine: </strong>Of course since all the previous work is powered by Zeitgeist we had to work on getting Zeitgeist better and better. They sponsored my development and maintenance with the team for the 0.7 and 0.8 series and  backed up our GNOME sponsored hack-fest. The biggest accomplishment was done when <em><strong>we ported Zeitgeist to Vala</strong></em>, resulting in less memory consumption and much better start-up times.</li>
</ul>
<ul>
	<li><strong>Epiphany Zeitgeist History (under development): </strong>I am working on patching Epiphany to use Zeitgeist as it main storage for History and "Frecency Search". The Epiphany guys already have a history rewrite branch in which I am sneaking in some code to replace their SQLite back-end. In the end its less code then what they have :P</li>
</ul>
<ul>
	<li><strong>Gtk-RecentManager (worked on designing the API with Federico, Siegfried and Michal Hruby): </strong>One of the tasks that emerged during the Desktop Summit was replacing the Gtk.RecentManager logic (which has some flaws). We started designing and <a href="https://live.gnome.org/GTK+/GtkRecentManagerAndZeitgeist">discussing the issues at hand on LGO</a>. Implementation is now being done by Siegfried and Federico.</li>
</ul>
<h3>What is next?</h3>
Collabora currently also sponsors Siegfried Gevatter for his work on Zeitgeist since last March. I will be trying to do some more GNOME related work. Currently I am trying to work on prototypes for the GNOME Design team to help them evaluate their designs. I will also be experimenting with some internal Zeitgeist algorithms stuff soon. I don't really know what is next. But I hope we can go further into integrating more with GNOME applications and becoming a blessed GNOME module.
<h3>Fun fact?</h3>
I used GAJ to write down my Zeitgeist development hours for Collabora. Pretty helpful tool. I can tell how long a file was open and how many times I modified it.
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-011550.png"><img class="size-full wp-image-2198" title="Screenshot at 2011-12-07 01:15:50" src="http://geekyogre.com/content/images/2011/12/Screenshot-at-2011-12-07-011550.png" alt="" width="461" height="288" /></a></p>