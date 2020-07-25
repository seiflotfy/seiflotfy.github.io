---
layout: post
title: Yet Another Zeitgeist Rant
date: '2009-07-15 21:35:15'
---

Well first of all I am happy that we finally released the 0.2 of Zeitgeist engine (check out my GSoC student's blog). It took us 9 months :P.

Now to clarify some issues concerning Tracker and Zeitgeist collaborations that have been discussed during GUADEC and that might confuse people, I will sum them up in points:

Tracker, Zeitgeist and Nepomuk are not the same. Nepomuk is an ontology used to describe Data. Tracker 0.7 (not the old 0.6) is an indexer and storage (which should have another title) . It is very efficient and uses the Nepomuk ontology. Zeitgeist is an event logging framework that provides cross application awareness. The reason why Zeitgeist was not able to use Tracker form the start was that neither the Nepomuk ontology nor Tracker supported the idea of storing an Event as an entity of its own (storing the history of the documents into themselves would not have done the job). Now several ways were discussed howto join forces and here are a few doable at the moment:
<ul>
	<li>Zeitgeist could notify Tracker about important events so Tracker could index those Targets (optimizing the queue).</li>
	<li>Zeitgeist stores all its data into the Tracker storage (except events until an ontology that satisfies the needs of all three projects (Nepomuk, Tracker and Zeitgeist) has been reached)</li>
	<li>Zeitgeist could use information Tracker has about URI's of interest.</li>
	<li>Tracker could use the dynamic tags (to be implemented sooner than you think) and set them somehow as relations between documents.</li>
</ul>
That being said the focus of some of the team members has gone to the Shell to provide a journal view as well as better integration by October. Also we are cooking a new dynamic "File Browser" based on Natan Yellin's mockups and Sebastian Faubel's "Organize Framework" vision (@David Siegel: It will rock your world :P).

Now during the hackfest I managed to prototype "Teamgeist" aka "Cookie Monster" creating application awareness over p2p. Instead of using a torrentish protocol, Robert McQueen from Collabora set it up to use telepathy tubes, also some Tracker magic with the help of John Carr has been done there too.  We set up a little UI and voila. I will uplaod a demo soon but here is what some people had to say:

Federico Mena (Novell):
<blockquote>W00T! oh my god! you just invented twitter for real work!</blockquote>
Robert McQueen (Collabora):
<blockquote>This project is an awesome demonstration of how GNOME's new technologies can be combined to achieve completely new UI concepts - it has the potential to change the way teams work together on the free desktop.</blockquote>
Rob Taylor (Codethink):
<blockquote>AWSOME</blockquote>
ANONYMOUS (Don't know why):
<blockquote>Are you shitting me! This is freaky!</blockquote>