---
layout: post
title: 'Teamgeist: Zeitgeist + Telepathy'
date: '2009-10-07 16:49:57'
---

So yet another blog post about Zeitgeist. :P

During GCDS I went looking for some Telepathy hackers. I got Rob McQueen, John Carr, Federico and others in one room brainstorming a collaboartion platform using Zeitgeist + Telepathy. By the end of the night the prototype worked.

Now Collabora has put Youness Alaoui from aMSN fame and Sumana Harihareswara to lead the project management and development. It is being developed very close to our 0.3 release due less than a month. But let me just explain a bit of how it will be and some use cases:
<blockquote>
<p style="margin-top: 0.4em; margin-right: 0px; margin-bottom: 0.5em; margin-left: 0px; line-height: 1.5em;">So the very high-level use-case is: you're working on a project with a group (one could say a team) and you basically want everyone to have some indication of what other people are doing which is relevant to the project you're working on.</p>
<p style="margin-top: 0.4em; margin-right: 0px; margin-bottom: 0.5em; margin-left: 0px; line-height: 1.5em;">You would give teamgeist some search query which would match zeitgeist events that are relevant to the project. Then the various users join a room which has a d-bus tube and the teamgeist/zeitgeist combination would forward the various events to this room so other people can keep track of them. (The UI for example could show a timeline of what people are/were working on).</p>
<p style="margin-top: 0.4em; margin-right: 0px; margin-bottom: 0.5em; margin-left: 0px; line-height: 1.5em;">Another interesting thing would be that when there are events referring to certain files it would be easy for the other users to get the updated version of the file (or it would automagically be downloaded). Or for users to add a local file to the project, such that teamgeist would update its filters to signal future events on that file to others.</p>
<p style="margin-top: 0.4em; margin-right: 0px; margin-bottom: 0.5em; margin-left: 0px; line-height: 1.5em;">This would also allow workflow management for teams as well as statistics of the work such as which were the most used files in this team etc...</p>
</blockquote>
<p style="margin-top: 0.4em; margin-right: 0px; margin-bottom: 0.5em; margin-left: 0px; line-height: 1.5em;">We are looking forward to implement a more simple API which will be mostly proposed by Jason Smith and Youness. Let us see how far we can get with this. You can read the specs <a href="http://wiki.zeitgeist-project.com/Teamgeist">here</a>.</p>