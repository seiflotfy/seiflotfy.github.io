---
layout: post
title: A snippet of the GNOME Zeitgeist Todo list
date: '2009-04-11 11:38:17'
tags:
- gnome
- zeitgeist
---

Since Alex Gabriel the maintainer of Mayanna is on vacation we got stuck with some issues! So while he is gone we started working on the old GNOME Zeitgeist again. The development is great. Me more or less absent because of work, Mr RainCT joined the developers during the week and almost finished the DBUS bindings. The code is cleaner. We have a daemon running and we are looking forward to write several UI's that communicate with the daemon! So whoever feels like writing in a UI in MONO, C, Vala or Javascript DBUS is there for you.

Here is a shor t snippet of our TODO List for the next couple of days:
<blockquote>TODO:

- Backend:
+ Add on Tracker support.
+ Extend DB to support location of usage
+ Auto Tagging e.g: tasks, locations, and relations.
+ Finish the D-Bus interface. (We need to insert items via DBUS , maybe patch up the datasink to have an insert in string tuples)
+ Reduce the amount of "changed" signals send.
+ Fix the Firefox DB detection (see comment in code).
+ Is RecentlyUsedDocuments the best place for text/plain files?

- Frontend:
+ Separate it from the backend and let it only use D-Bus for communication.
+ Do not show an item twice one beneath the other.
+ Use a generic CellRenderer to display stars for bookmarking instead of checkboxes!
+ create a bar displaying the related files to currently opened files (inspired by Gimmie)</blockquote>