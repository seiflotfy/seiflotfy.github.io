---
layout: post
title: The week merging Mayanna & Zeitgeist !
date: '2009-04-01 02:25:59'
---

Mayanna was supposed to be a fork of Gimmie, Alex Gabriel and me started together (very creative name which is basically my girlfriends and his girlfriends name put together May + Anna). We then decided to write from scratch and started designing! While i still felt I couldn't just leave the Gimmie code behind I started taking it apart looking for all the memory leaks and fixing it, while Alex continued on Mayanna! During the struggle to free the Gimmie code of memory leaks ,during the time I worked on Thorsten Prante's Journaling System(Context Drive), and going through Federico's Jorunal Idea, I prototyped a quick mayanna journal. I then contacted Throsten again and at some point we ended up with Zeitgeist. While I stayed in good contact with Alex Gabriel I always found it interesting how his ideas were actually being realized!

So here it is. Mayanna is a kick ass engine with Zeitgeist as its main plugin. To sum it up here is what it will look like. To put it in a nutshell: Mayanna is a very generic plugin engine.

All Dataproviders from Zeitgeist will be ported to Mayanna and will run as separated processes communicating with a hub where the data from the providers are then written in the database. Zeitgeist which is another plugin will talk to the hub requesting items from other plugins (in this case data providers). The hub will throw the items in Zeitgeists datasink to modify the UI if necessary. Now all that is actually happening without the use of D-Bus. We will the wrap some D-Bus around the Zeitgeist plugin for other apps to take advantage of the journal system.
Right now I am porting the data providers and modifying the database where necessary to make Mayanna optimal for Zeitgeist! Alex is working on making searching as flexible as possible. We are intending to make plugins easy writeable and create a two way communication between the data providers and the loggers. Example: If I bookmark a website in Zeitgeist it should be bookmarked in Firefox and Epiphany too.
Another thing that will happen is modifying the database of old Zeitgeist and then merge Mayanna+Zeitgeist. We want to differentiate between Activities and Events.
Activities happen because the user initiates them, e.g: Reading mail, editing text or watching movies.
Events happen and the user can't prevent them from happening, e.g: Receiving mail, RSS, files on my disk being modified by other over the network, Contacts on the IM logging in and out, and receiving Skype calls.

This allows the user to view 3 separate timelines. Own activities, events (allowing the user to catch up on things he/she missed), and both together. We should be done within 2 weeks maximum with the merge.

Hopefully Natan can continue working on Zeitgeist within the next week while I am preparing the whole porting. So in case something goes wrong we still have the old code to rely on. I added some little experimental feature where I try to show data related to the item selected in the timeline.