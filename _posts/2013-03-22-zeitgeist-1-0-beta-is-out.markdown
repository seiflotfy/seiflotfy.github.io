---
layout: post
title: Zeitgeist 1.0 Beta is out
date: '2013-03-22 05:09:26'
---

<center>![](/content/images/2014/Jan/index.jpeg)</center>

So finally we have rolled out Zeitgeist 1.0 beta...

With Zeitgeist 1.0 we  are introducing libzeitgeist2, a Vala port of the previously independent libzeitgeist library. The new libzeitgeist2 comes with 3 big improvements over libzeitgeist:
<ul>
	<li><span style="line-height: 13px;">Maintained internally by the Zeitgeist team since it is part of the internal datamodel we used.</span></li>
	<li>Has direct read support. This way when querying Zeitgeist for data there is no more round-trips and less serialization which improves most queries by almost 100% and sometimes even more. Writing is still done over D-Bus.</li>
	<li>GObject Introspection support. So now it can be used with almost any language.</li>
</ul>
The engine itself is also faster and has seen a lots of bug fixes.  Zeitgeist datahub package is now part of the Zeitgeist Framework package. This should be convenient for packagers.

Over the weekend some of us will be porting apps in GNOME using Zeitgeist to libzeitgeist2 and actually patch some existing apps to have better sorting.

I would like to thank the whole Zeitgeist team for getting this far, and the people who helped us get there. Also we are looking into porting libQzeitgeist to depend on libzeitgeist2 for less future maintenance efforts (please contact Trever Fischer - tdfischer on irc) if you are interested. We have a very interesting KDE application in mind at the moment that would make use of kde-telepathy, nepomuk and libqzeitgeist.

We are hanging out on #zeitgeist on freenode and for  the latest Zeitgeist, just check out our fdo git repo ==&gt; <a href="http://cgit.freedesktop.org/zeitgeist/zeitgeist">http://cgit.freedesktop.org/zeitgeist/zeitgeist</a>

&nbsp;