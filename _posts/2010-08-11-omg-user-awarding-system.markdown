---
layout: post
title: OMG! User Awarding System
date: '2010-08-11 20:55:37'
---

Taken from the <a href="http://live.gnome.org/OMG">GNOME Wiki</a>

The idea being OMG! is to have a central user awarding system where users collect trophies based on their activities and experience on the desktop environment. e.g:
<ul>
	<li>For installing "Banshee" the user gets awarded with the "Banshee Discovery Trophy".</li>
	<li>For working with Cheese for 30 minutes the user gets awarded with "Photogenic Trophy".</li>
	<li>For Editing 100 documents using "gedit" the user gets awarded with "Badass Trophy"</li>
</ul>
<h2 id="OMG.21_Basics">OMG! Basics</h2>
OMG! is a little daemon. Applications communicate with it over DBus. As an awarding system awards users are awarded with trophies: A trophy consists of:
<ul>
	<li>ID: String generated automatically from the Title + "-" + Application</li>
	<li>Title: String with the title of the trophy</li>
	<li>Description: String with a more detailed description of WHY the user got the trophy</li>
	<li>Application: String with the path to the application executable</li>
	<li>Timestamp: Integer with a Timestamp of when it was awarded.</li>
	<li>Icon Path: String with the path to the Icon for the Trophy</li>
	<li>Status: A boolean describing if the Trophy is awarded unlocked or is locked until the requirements are fulfilled</li>
	<li>Priority: Integer from 0 - 2 describing how relevantly big the achievement is.</li>
</ul>
Applications are responsible for awarding their own trophies. OMG! is only a trophy collection and a notification system for that. It is intended to build another little Zeitgeist based application to monitor and evaluate activities to award users. Also achievements will be stored in Zeitgeist to show them in GAJ and allow applications to query their own awards.
<h2 id="OMG.21_Simple_API">OMG! Simple API</h2>
Thus the API is very straight forward
<ul>
	<li><strong>RegisterTrophy (String Title, String Description, String Application, String IconPath, Integer Priority)</strong>: No Return
<ul>
	<li><em>OMG.RegisterTrophy("Welcome Rug", "You ran OMG! for the first time", "application://omg", "", 0)</em></li>
</ul>
</li>
	<li><strong>AwardTrophy (String Title, String Application)</strong>: No Return
<ul>
	<li><em>MG.AwardTrophy("Welcome Rug", "application://omg" )</em></li>
</ul>
</li>
	<li><strong>DeleteTrophy (String Title, String Application)</strong>: No Return
<ul>
	<li><em>OMG.DeleteTrophy( "Welcome Rug", "application://omg" )</em></li>
</ul>
</li>
	<li><strong>GetTrophies ( )</strong>: Returns an Array of Trophies (String Title, String Description, String Application, Integer Timestamp, String IconPath, Boolean Status, Integer Priority.
<ul>
	<li><em>OMG.GetTrophies()</em></li>
</ul>
</li>
</ul>
<h2 id="OMG.21_Concept">OMG! Concept</h2>
<ul>
	<li>Applications should have the possibility to register their trophies over DBus and not statically define them upfront</li>
	<li>Applications know most about their activities thus they should hand out the awards and trace the activity of the user or allow Zeitgeist to track it for them</li>
	<li>Awards will be logged by Zeitgeist to have a timeline option around "When did I achieve something"</li>
	<li>More to come...</li>
</ul>
<h2 id="OMG.21_Code">OMG! Code</h2>
<ul>
	<li><a href="https://edge.launchpad.net/omg">https://edge.launchpad.net/omg</a></li>
	<li>bzr branch lp:omg</li>
</ul>
Also there is another similar development happening from the Hamster Project side and we hope to merge sooner or later...