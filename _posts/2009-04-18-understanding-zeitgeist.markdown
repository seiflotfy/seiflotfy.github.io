---
layout: post
title: Understanding Zeitgeist
date: '2009-04-18 00:34:51'
---

<strong>First things first...</strong>
<blockquote>Zeitgeist never intended to replace the hierarchical file-system. It is not doable. And it cannot replace the classic file browser either. Zeitgeist is more or less a layer over the file hierarchy to reduce browsing into folders etc. It is just an alternative experience of easily finding your files whatever type they may be.</blockquote>
<strong>This being said...</strong>

Zeitgeist is based on and works with chronologically logged  data of the users working with their personal computer.

Our focus currently is on supporting activity (files,websites,notes and mails) management by tagging (manually and automatically), chronological organizing and bookmarking. This is all provided by the current UI plus searching. An RDF model will also be developed to provide for interoperability. This way, Zeitgeist will reduce and ease the experience for going back to information already used thus orienting oneself in one’s information, resuming work and task switching.

This is already tackled by common desktop search engines, but they rather fail to find and present the user’s information in the context of their, possibly repeated, usages and exploit the thereby implicitly or explicitly established relationships.

The journaling data can be understood as providing extensions to or a generalization of the “recently used” information access method common to most operating systems, where extension is meant time‐wise and spans potentially all data types and information which one touches on one's desktop, including, for example, text documents, pictures, web resources, instant and email messages, but also contact information, calendar items and other information items related to planning.

As opposed to the intimacy expressed by many people, and in particular knowledge workers, interacting with their personal computing devices throughout the everyday and across private, professional and educational domains, today, it is striking to observe that this very personal computing environment is not really prepared and in fact offers only limited support in answering the central questions of orienting oneself: “What did I do?” (retrospective perspective), “What am I currently doing?” (current perspective, where ‘current’ turns out to be a very vague term), and “What have I planned for the future?” (prospective perspective).

<strong>Now the fun part...</strong>

The engine (in python :P ) is stable, we have a D-Bus interface working (thanks to Siegfried), running constantly for one day I have around 18 MB memory usage (logging and sending to UI via D-Bus). There is the classic Journal UI and a new "Project Viewer" based on project <a href="http://github.com/harokkar/gothenburg/blob/b8fef3b3a28b6fdad28320227acc8b93a5eb3519/resources/GothenburgGUI.png">Gothenburg</a> concept.

We fixed a lot of bugs and memory leaks and still on it but not many new features will be coming soon. <a href="http://jassmith.wordpress.com/">Jason Smith</a> is working on a new project in Mono that uses the Zeitgeist engine.

A first release could be soon. Just some fixes and tweaks...