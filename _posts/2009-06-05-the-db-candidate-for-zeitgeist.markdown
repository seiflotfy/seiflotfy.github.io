---
layout: post
title: Candidate for the new Zeitgeist DB
date: '2009-06-05 22:11:58'
---

At last we  have a candidate for the DB. After the <a href="http://xesam.org/main/FrontPage">Xesam</a> dude (<a href="http://www.grillbar.org/wordpress/">Mikkel Kamstrup Erlandsen</a>) joined the team he took my last proposal of a new DB design and did his voodoo to end up with.

<img class="alignnone size-full wp-image-688" title="zeitgeist-2" src="http://geekyogre.com/content/images/2009/06/zeitgeist-2.jpeg" alt="zeitgeist-2" width="829" height="310" />

Again please forgive me for using UML class diagram tools for designing the DB.

<a href="http://live.gnome.org/action/edit/GnomeZeitgeist/DatabaseDesign">Here</a> you can read more and get into details. I will try to finish the implementation until monday leaving the current interface unharmed.

Xesam as described by their page is:
<blockquote>short for <em>eXtEnsible Search And Metadata</em> and is an umbrella project with the purpose of providing unified APIs and specs for desktop search- and metadata services. We are collaborating with several projects such as <a class="http" href="http://tracker-project.org/">Tracker</a>, <a class="http" href="http://strigi.sf.net/">Strigi</a>, <a class="http" href="http://beagle-project.org/">Beagle</a>, <a class="http" href="http://pinot.berlios.de/">Pinot</a>, <a class="http" href="http://recoll.org/">Recoll</a>, and <a class="http" href="http://nepomuk-kde.semanticdesktop.org/">Nepomuk-KDE</a>.</blockquote>
This will allow us to use annotation as tags, bookmarks,and custom comments. Also its a good preparation for a optional Tracker backend as well as co-operation with other FLOSS Projects involved with RDF semantics while still being a project of our own. I am worried however how it is going to scale. But I guess nothing that some indexing and tweaking wont fix.