---
layout: post
title: Playing with contextual relevancies in Zeitgeist (week 1)
date: '2009-10-19 13:15:32'
---

So @Zeitgeist we took the liberty of experimenting of monitoring the document(window) focus of the user.

This is something I have been working on for  long long time. To cut it short. When monitoring the focus of items (items being websites, documents, notes, mostly anything), <em>with time</em> one can detect patters of document activities. We have some kind of directed adjacency matrix. If you are familiar with graph theories this is how it is calculated.  Every document is a <strong>node</strong> while every switch of focus becomes a <strong>vertex</strong>. The vertex holds the timestamp (possible also the GPS location) of the focus switch from a document to another. This matrix will be an essential part of the 0.3 version of the engine.

The benefits of this feature are:
<ol>
	<li> <strong>Calculating "Focus life" of a document/application and tags</strong>: Think of instead of most used as in (how many times opened) you can now as for most focused (how long was it in the main focus). This feature could be used to sort search results for Tracker and other stuff. The focus lifetime of a document will be calculated by taking the absolute value of  "the timestamps of incoming vertices and subtracting them from timestamp of the outgoing".</li>
	<li><strong>Determining Contextual relevancies of Documents:</strong> So there are somethings that a users usually uses together in context over time. Let us say every time I work on <em>tutorial.c</em> I switch focus between it and <em>http://library.gnome.org/devel/gtk-tutorial/2.17/.</em> Over time some habits can be detected and connections between URIs can be set. Right now I can ask <strong>"get me all documents that i switched from or to while working on X"</strong> this results into a little graph. We can also ask <strong>"get me all documents that i  indirectly switched from or to (over max. n nodes) while working on X" </strong>which will allow me to widen the radius of activities around a documents thus resulting into more potentially related files. This feature might be also used for GNOME Do. Another idea is to revive the old Dashboard.</li>
</ol>
Currently a vertex with one time focus switch between documents is ignored for filtering issues. Later we will use the lifetime of the documents to calculate if the documents contextual relationship could be considered spam or not. This can be relaized in a scenario where while working on my paper i changed the music. The music in now contextually related to the paper, however we can filter it out if we notice that there was a quick switch of focus back to the document. making the focus on the music only 1 second or 2. There will be other means of filtering the contextual relevancies using meta-data provided by Tracker.

The prototype is done and now needs to be cleaned up for the integration into the framework. Rob Taylor from Codethink encouraged us to build a UI that I am using to display the results. To test this feature I deleted all my history from every applications to benchmark how the little hack will learn. Here are some results of URIs that are contextually related over 1 week.

(+ is the currently focused document and  - are the most used switched from/to documents)
<blockquote>---
+ http://geekyogre.com
- http://geekyogre.com/wp-admin/post.php
- http://geekyogre.com/wp-admin/
- http://mail.google.com
---
+ http://facebook.com
- https://login.facebook.com/login.php?login_attempt1
- http://www.facebook.com/home.php?
- http://geekyogre.com
---
+ http://twitter.com
- http://twitter.com/direct_messages/sent
- http://twitter.com/#sent
- http://twitter.com/seiflotfy
---
+ https://blueprints.edge.launchpad.net/zeitgeist
- https://blueprints.edge.launchpad.net/~zeitgeist
- https://blueprints.edge.launchpad.net/zeitgeist/+spec/set-filter-results
- https://blueprints.launchpad.net/zeitgeist
---
+ http://www.youtube.com
- http://www.youtube.com/seiflotfy</blockquote>
For a little display here is the <a href="http://geekyogre.com/content/images/seilo.png">graph</a> generated for the first example. 0 being http://geekyogre.com and the nodes form/to the 3 vertices with the highest weights pointing to from it are displayed in the results.

So we are experimenting a lot and I would like to know you opinion on this research. So keep in mind that this is jut 1 week history.