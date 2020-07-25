---
layout: post
title: Gnome Zeitgeist status
date: '2008-11-28 23:30:30'
---

<p>A lot has been done on Gnome Zeitgeist lately. To sum up Zeitgeist now uses a sqlite database to store: Name, URI, Type, Timestamp, Count, Last usage.</p><p>
This means all provides write their data into a datasink which forwards them to a DB. When an amount of items are asked for the datasink collects them from the database and casts them according to type and forwards them to the UI. </p><p>
The speed is ok but has to be better! Natan Yellin is working on the cleaning up the gui code part while i am looking at the engine! I would really like having Alex Gravely looking at the code with us since alot of the code originates from him!</p><p>
As usual you can find the code in <a href="https://code.edge.launchpad.net/~gnome-doc-centric-playground/gnome-doc-centric-playground/gnome-journal-prototype">launchpad</a></p>