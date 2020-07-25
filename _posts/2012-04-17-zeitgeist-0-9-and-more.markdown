---
layout: post
title: Zeitgeist 0.9 and more...
date: '2012-04-17 12:40:23'
---

Since the Zeitgeist team is kinda recovering from last month, and no one really feels like blogging, I am here to sum up what has been up the last 2 months. (Also I think a blog post from my side is long overdue)

<strong>Privacy Manager</strong>

A lot of users are scared of "logging", and since Zeitgeist is considered an event logger, we ended up having some users trying to disable Zeitgeist all in all breaking Unity searching and so on.
Fact is, if you want searching to be sorted properly, the search provider needs to know what files you recently or frequently used. Also some people want to have some of their stuff logged and others things not (blacklisting folders).
Activity Log Manager which we already had developed in python last year has been ported to Vala. This nifty tool allows you to blacklist application, folders, mime-types from being logged as well as the option to delete parts of your log. The port to Vala happened so we can patch it into the Settings Manager to give it an more integrated feel with the System in Ubuntu and Dawati.
It has received very good reviews and there are some very interesting new development efforts/ideas in the make (right now one in a state of flux which I hope I can get out of soon).

Here are some screenshots of the current stand of ALM

<a href="http://geekyogre.com/content/images/2012/04/Screenshot-from-2012-04-17-132735.png"><img class="alignnone  wp-image-2253" title="Screenshot from 2012-04-17 13:27:35" src="http://geekyogre.com/content/images/2012/04/Screenshot-from-2012-04-17-132735.png" alt="" width="446" height="338" /></a>

(dialog for deleting history)

<a href="http://geekyogre.com/content/images/2012/04/Screenshot-from-2012-04-17-132908.png"><img class="alignnone  wp-image-2255" title="Screenshot from 2012-04-17 13:29:08" src="http://geekyogre.com/content/images/2012/04/Screenshot-from-2012-04-17-132908.png" alt="" width="446" height="338" /></a>

(dialog for blacklisting folders and file types)

<a href="http://geekyogre.com/content/images/2012/04/Screenshot-from-2012-04-17-132953.png"><img class="alignnone  wp-image-2254" title="Screenshot from 2012-04-17 13:29:53" src="http://geekyogre.com/content/images/2012/04/Screenshot-from-2012-04-17-132953.png" alt="" width="446" height="338" /></a>

(dialog for blacklisting applications)

<a href="http://geekyogre.com/content/images/2012/04/Screenshot-from-2012-04-17-133100.png"><img class="alignnone  wp-image-2256" title="Screenshot from 2012-04-17 13:31:00" src="http://geekyogre.com/content/images/2012/04/Screenshot-from-2012-04-17-133100.png" alt="" width="361" height="250" /></a>

<strong>Zeitgeist 0.9</strong>

Last year we started porting Zeitgeist from python to Vala. Mostly for the sake of easier deployment as well as improving startup time. As a side effect also memory consumption decreased and during the development more optimizations have been made.
It was a very intense operation sponsored by Collabora and Canonical as well as the awesome unpaid Zeitgeist developers.
So a big thanks goes to Collabora, Canonical, Michal Hruby, Siegfried Gevatter, Manish Sinha, Mikkel Kamstrup, Trever Fischer, Stefano Candori, Moritz Neeb, as well as everyone else who tested Zeitgeist, provided bug reports or contributed in any other way.

We released some alphas and a beta. But now the real deal is out. We still have some nice optimization in the queue that we will release with the next Zeitgeist version. So don't hesitate to try it out.