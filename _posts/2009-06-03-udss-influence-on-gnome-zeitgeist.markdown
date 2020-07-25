---
layout: post
title: UDS's influence on GNOME Zeitgeist
date: '2009-06-03 15:50:35'
---

Last week, Siegfried (my GSoC student) and I, attended UDS. I would have loved more from the Zeitgeist team to be there but sadly it did not work out.

It was my first time to meet Siegfried. He was pretty shy at the beginning but started coming out as a jerk later on when he made my heart skip some beats with a stupid blue screen of death game. But I was very pleased to meet him and had an amazing productive time with him. I also got to meet the Do Crew and Canonical's newly formed User Experience Team, who showed a lot of support for GNOME Zeitgeist and helped promoting it.

Before UDS, GNOME Zeitgeist was getting some good attention, but sadly we never got directions from anybody concerning the engine. All of the Developers are actually students so our time and resources are limited. This however all changed during UDS. Thanks to David Barth and Emmet Hikory who took the time to sit down with us to understand Zeitgeist, thus setting new directions for the Zeitgeist "Service" as well as a strategy to avoid any political problems (sorry guys I am a Mono fan boy, but sadly the 2 other maintainers in the Team aren't, so no worries the only language the engine would be ported to would be C). And for the first time we have a semi roadmap, thanks to the UNR team Milo, which we never got to set up since we were busy developing and going with the flow.

We successfully managed to split the engine (Zeitgeist) and UI (GNOME Zeitgeist) into two different packages as well as projects, Making development, debugging and deployment more focused. Several UIs over Zeitgeist are being developed thus we are creating one team Zeitgeist Desktop eXperience short Zeitgeist-DX to manage the UI's being developed by the team and working close with  Canonical User Experience Team and Jason Smith.

The engine is our current focus now so we can finish the Shell integration as well as deliver it for the Karmic release to work with Projects such as UNR and the Parental Control. For UNR we are going to provide it with most used or interesting Data to the current moment or work-flow. Parental Control will be able to use Zeitgeist to monitor the child's current activity and inform the parents by mail or whatever they want. Another thing we will be doing is a bzr extension (if any1 wants to git extension feel free to go crazy :P). Natan is working on an optional (for those who use Tracker) backend that uses Tracker stored data information.

My next blog post will about the current changes that are to be done on the Zeitgeist engine as well as a ranking library we David Siegel suggested to write to provide applications with currently relevant Data.

Thanks UDS and every1 who participated it was one amazing and productive week.