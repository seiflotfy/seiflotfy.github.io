---
layout: post
title: Parental Control for GNOME 3.0
date: '2009-08-10 00:09:45'
---

So if everything goes according to plan Zeitgeist engine could be included as an optional module with the GNOME 2.28 release to enhance the Shell experience thanks to <a href="http://bloc.eurion.net/">Siegfried Gevatter(RainCT)</a>.

If it is so then I will also rework some of the Parental Control concepts I presented during GCDS! I see it as a very good marketing point (not for hackers).

The concept is simple: Parental Control subscribes to events from Zeitgeist. Since we deliver the source (Application) as well as the subject (Document, Website, Video, etc...), we trigger some keyword extractor as well as metadata extractor on the subject looking for specific strings that we have in a blacklist. If found in the blacklist we freeze source application and ask for password! If password is wrong then kill the application or do whatever (we can  set a dialog box or scripts that could be executed). Tracker could be used in this application!

The application should be simple and not really fancy schmancy as on UI wise... If you like the idea please contact the Zeitgeist team so we can work on it!