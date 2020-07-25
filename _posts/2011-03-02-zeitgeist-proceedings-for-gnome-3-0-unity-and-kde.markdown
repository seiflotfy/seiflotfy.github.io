---
layout: post
title: Zeitgeist proceedings for GNOME 3.0, Unity and KDE
date: '2011-03-02 20:30:29'
---

Currently the Zeitgeist team is back from a short hiatus after the successful hackfest, leading to a release of Zeitgeist and all the belonging modules as part of the 0.8 cycle on the 15th of March.

Other than being a technically successful cycle, the 0.8 for me personally was a successful in deployment and communication level:
<ul>
	<li>Lots of GNOME <strong>upstream</strong> integration has been done:
<ul>
	<li>gedit (<a href="https://bugzilla.gnome.org/show_bug.cgi?id=641774">https://bugzilla.gnome.org/show_bug.cgi?id=641774</a>)</li>
	<li>rhythmbox</li>
	<li>banshee</li>
	<li>totem (<a href="https://bugzilla.gnome.org/show_bug.cgi?id=640365">https://bugzilla.gnome.org/show_bug.cgi?id=640365</a>)</li>
</ul>
</li>
	<li>Initial GNOME Shell integration is looking good. (<a href="https://bugzilla.gnome.org/show_bug.cgi?id=640659">https://bugzilla.gnome.org/show_bug.cgi?id=640659</a>)</li>
	<li>Lots solid work has been done on the datahub and GNOME Activity Journal (it runs for David Richards)</li>
	<li>Initial concepts for Zeitgeist powered Gtk3 widgets have been set.</li>
</ul>
We started a new communication channel with GNOME developers and I am happy to say its going really well:
<ul>
	<li>We had some very insightful discussions with <a href="http://www.hadess.net/">Bastien Nocera</a> about the API.</li>
	<li>Jasper St. Pierre is the most patient guy on earth for helping me with us with our Git patches and reviewing our code for GNOME Shell constantly.</li>
	<li>Also the gedit guys are just plain awesome for being so approachable and helpful.</li>
</ul>
Also with Collabora putting me and Siegfried Gevatter on a payroll to work on Zeitgeist, allowed us to grow more confidence in our work and have even more fun working on growing the development community. Collabora, Federico and Michal Hruby have been a very important factor in our communication with GNOME and in return the GNOME community has been very accepting and cooperative with us, despite the "dramatic" past.

This new communication channel also helped us evolve into a more stable and committed team. With at least 20 hours per week from each developer, we already planned our occupations for the 0.9 development cycle starting 16th of March till 15th of June.

To ease the integration upstream one of the big highlights of the next cycles is that we are moving from <strong>lgpl3</strong> to <strong>lgpl2.1+</strong> for all Zeitgeist modules and libraries. I would like to officially thank Canonical for allowing us to do this move with libzeitgeist which is written and maintained by Canonical (authored by our own Kamstrup). The reasoning behind it is to allow smoother integration with GNOME upstream projects. I must say I am not surprised by their cooperation and on behalf of the team am very thankful for this amazing gesture by Canonical. libzeitgeist is being used by our totem and gedit upstream work.

[table id=1 /]

Looking at the table will help us internally know who to contact for what as well as for new comers who want to jump on board with development or just ask questions. Each module has its own maintainers and developers more or less. Example: Michal Hruby maintains the datahub, Manish maintains the mono bindings, Randy and Stefano co-maintain AJ. So governance wise things are becoming modular yet synchronized. Some very fun Telepathy &lt;-&gt; Zeitgeist work is under development so feel free to contact sjokkis on if your interested.

The rest can be seen in the table.

There is some surprises coming out on the Unity side that will be powered by zeitgeist. Its nice to see how Unity really makes full use of Zeitgeist.

Also one of my main work for this cycle is to have more upstream KDE work working too. We already have phonon upstream patches as well as Kate. The KDE community is very very approachable and take matters in their own hands which makes it easy for us to deploy there.

All in all there is a big journey this year ahead of us and we won't disappoint you.