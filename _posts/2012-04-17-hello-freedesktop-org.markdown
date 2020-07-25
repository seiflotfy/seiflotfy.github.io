---
layout: post
title: 'Zeitgeist: Hello Freedesktop.org'
date: '2012-04-17 15:11:48'
---

For as long as Zeitgeist has existed it has been hosted on Launchpad. We made use of almost every Launchpad feature and grew to love Bazaar. The tight integration between Bazaar and Launchpad should be a taken as a grand example to the community, and the the team hacking on Launchpad and Bazaar has been always very responsive, supportive and above all incredibly approachable. The Zeitgeist team hosted all of its projects on Launchpad which made our development process very agile. I really need to thank the Launchpad team for hosting the project from its inception.

During the course of the last 3 and half years, Launchpad served us well and allowed us to handle:
<ul>
	<li>ca. 748 unique bugs reported</li>
	<li>ca. 231 merges</li>
	<li>ca. 53 code contributions</li>
</ul>
We hope that many other great projects will find a valuable home on Launchpad. Without Launchpad, Zeitgeist would have not reached the level it has now.
<p style="text-align: left;">But time changes and projects grow. The Zeitgeist team has a stable developer base of minimum 7 people putting several hours a week into Zeitgeist development and deployment. With these efforts comes the need of a vendor neutral platform hosted and serviced in a way that serves the interest of the project best.</p>
<p style="text-align: left;">Due to the deployment efforts being made to get Zeitgeist integrated with applications, our developers got more and more exposed to git. A stream of developers expressed their desire to work with us, however they were very uncomfortable or unfamiliar with bazaar and Launchpad, due to the popularity of git. That is something we do not understand in the core team, but still something we respect and will act on.</p>
We couldn't find a good direct replacement for Launchpad honestly, but since Bugzilla is something like the defacto standard for most people we decided to host Zeitgeist on Freedesktop.org (I must admit in-patch commenting in Bugzilla is sweeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeet).
<p style="text-align: left;">We needed to wait until we finished the 0.9 release of Zeitgeist as well as narrow down the bugs to be less then 10 to make the transition as smooth as possible.</p>
<p style="text-align: left;">Now that Zeitgeist 0.9 is released, all our development will take place on Freedesktop.org and will be mirrored to launchpad, this means no code will be pushed directly to Launchpad, but rather Launchpad will pull from the git repositories. There the Zeitgeist Ubuntu guys (including me) will be syncing bugs and keeping everything intact. So bugs reported in Launchpad will be ported to FDO. But not the other way around.</p>
<p style="text-align: left;">We did not turn our backs on Launchpad, its just time for us to remove any barriers to getting the widest adoption of and contributions to Zeitgeist</p>
<p style="text-align: left;">On the road toward Zeigeist 1.0, FDO will be a great home for the project and we look forward to many great new contributions.</p>
<p style="text-align: left;">So please feel free to have a look at:
<a href="http://cgit.freedesktop.org/zeitgeist/">http://cgit.freedesktop.org/zeitgeist/</a></p>
<p style="text-align: left;">P.S: I would like to thank Trever Fisher and Manish Sinha for their efforts porting the code base.</p>