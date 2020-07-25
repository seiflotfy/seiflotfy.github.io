---
layout: post
title: OMG! Current Iteration
date: '2010-08-20 22:35:00'
---

<div>

<span style="font-family: arial, helvetica, sans-serif;">So to show you guys feedback on what we are doing in OMG! I would first like to introduce you to the "professional" alternative <a href="http://projecthamster.wordpress.com/2010/08/18/gnome-achievements-the-alternative/">GNOME Achievements</a> that is being developed by the project hamster guys.</span>

<span style="font-family: arial, helvetica, sans-serif;">While the 2 projects are the same in a way they differ in other areas, especially in the trophy specifications. We are not out to compete but i tried to see that my team surrenders development on our engine but for somehow its hard to slow them down. </span>

<span style="font-family: arial, helvetica, sans-serif;">The 2 projects also differ in their development processes and tools. We use Mono (Vala port is there too) they use Python. They host on git we use launchpad. Our development is more agile and evolutionary (several iterations and public development and reports) they are more planned and structured.</span>

<span style="font-family: arial, helvetica, sans-serif;">I advise you to look at their work... that being said...</span>

<span style="font-family: arial, helvetica, sans-serif;">I tried to assemble a small new team to work on OMG! because the Zeitgeist team is very busy with development for Unity and GNOME integration (<a href="http://mhr3.blogspot.com/">Michal Hruby</a> will be releasing Sezen this weekend), and the new GAJ will follow on monday.</span>
<h2 style="font-size: 1.5em;"><span style="font-family: arial, helvetica, sans-serif; font-size: x-large;"><strong>Current Development Iteration:</strong></span></h2>
<h3 style="font-size: 1.17em;"><span style="font-family: arial, helvetica, sans-serif; font-size: large;"><strong>Team</strong></span></h3>
<span style="font-family: arial, helvetica, sans-serif;">Meanwhile our development will continue. Currently the team consists of:</span>
<ol>
	<li><span style="font-family: arial, helvetica, sans-serif;"><a href="http://manishtech.wordpress.com">Manish Sinha</a> (Daemon and Specs development)</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">Chris Szikszoy (Daemon and Specs development)</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">Adam Zimmerman (UI Design)</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;"><a href="http://kilianvalkhof.com/">Kilian Valkhof</a> (UI Desing &amp; Development)</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;"><a href="http://www.lamalex.net/">Alex Launi</a> (Code inspection and review)</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;"><a href="http://davidnielsen.wordpress.com/">David Nielsen</a> (UI design &amp; API design)</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">Me (General spanking and a bit of this and that)</span></li>
</ol>
<span style="font-family: arial, helvetica, sans-serif;">We are open for anyone to come join the Team.</span>
<h3 style="font-size: 1.17em;"><span style="font-family: arial, helvetica, sans-serif; font-size: large;">Daemon</span></h3>
<span style="font-family: arial, helvetica, sans-serif;">Manish is really rocking the daemon. <a href="http://live.gnome.org/OMG">He will be updating the specs here</a> as he develops. We used to register our trophies over DBus however now Trophies are registered the same way the GNOME Achievement guys do it. (Yeah we stole that part :P)</span>
<h3 style="font-size: 1.17em;"><span style="font-family: arial, helvetica, sans-serif; font-size: large;">UI</span></h3>
<span style="font-family: arial, helvetica, sans-serif;">Adam Zimmerman contacted me with a very nice UI design and documentation to it. We are basing our development on that.</span>
<blockquote><span style="font-family: arial, helvetica, sans-serif; font-size: medium;"><strong>SUMMARY (IF YOU DON'T WANT TO READ EVERYTHING BELOW)</strong></span>

<span style="font-family: arial, helvetica, sans-serif;">Trophies can be displayed like a trophy case layout or in a list view. Users can change the zoom or display style (trophy case, scout badges), and share their achievements on blogs, social networks, or as a picture. Any trophy can be "un-accomplished" or hidden if the user wishes. A hints section shows one installed application and one not-installed application where more trophies can be earned. New applications are rotated in daily, at random. The hints section has buttons to open/switch to/highlight the installed application, to install an application shown in the hint, and to learn more about it before installing.</span>

<span style="font-family: arial, helvetica, sans-serif; font-size: medium;"><strong>MOCKUP DETAILS</strong></span>

<span style="font-family: arial, helvetica, sans-serif;"><strong>TROPHIES (first mockup page)</strong></span>

<span style="font-family: arial, helvetica, sans-serif;"><strong><a href="http://geekyogre.com/content/images/2010/08/trophies.png"><img class="alignnone size-full wp-image-1431" title="trophies" src="http://geekyogre.com/content/images/2010/08/trophies.png" alt="" width="498" height="340" /></a></strong></span>

<span style="font-family: arial, helvetica, sans-serif;">The Trophies tab is the main display case for all the trophies that have been earned. The trophy icons' layout imitates the way one might arrange trophies in a display case in real-life.</span>

<span style="font-family: arial, helvetica, sans-serif;">The View menu would include a menu option to switch the trophy case style. The default style would be glass shelves with a reflection of the trophy icons as if they were sitting on top. There is an implementation of a similar idea in the GCstar collection manager; a screenshot can be found at  http://www.gcstar.org/images/screenshots/MoviesGlass.png . The trophies' titles would be shown on the front face of the shelf, like a label. The View menu would also contain an option to turn these titles on or off. (Another style choice would be a fabric background, like a scout displaying merit badges.)</span>

<span style="font-family: arial, helvetica, sans-serif;">Also in the View menu would be an option for switching to a list view. The list view would me more like a vertical list of large (48x48?) trophy icons and their names; it would not be like the list view in Nautilus. </span>

<span style="font-family: arial, helvetica, sans-serif;">Users could drag the trophy icons to reorder them. Additionally, the View menu would include menu items for sorting the trophies and for grouping the trophies (both usable in either view, with slightly different implementations). Useful Sort options would be (1) trophy name and (2) date the trophy was unlocked. Useful Group By options would be (1) application, (2) date (today, this week, last week, this month, last month, this year, older), (3) unlock action (e.g., trophies for running a program a certain number of times would be grouped together, and trophies for changing an option in a program would be in another group).</span>

<span style="font-family: arial, helvetica, sans-serif;">The status bar always includes a count of how many trophies have been achieved (there's likely a prettier way to display this). While the Trophies tab is active, a zoom slider is shown (this would probably require the trophy icons to be svg instead of png or some other bitmap format).</span>

<span style="font-family: arial, helvetica, sans-serif;">On the toolbar are two buttons, both for displaying accomplishments elsewhere. The Share button (which should be renamed "Share Online" to avoid confusion) would bring up a window to display trophies in various forms online such as a blog widget, in a profile on Facebook/Ubuntu Forums/etc., or a post or status update on Twitter/Identica/Facebook/a blog/etc. Mainly, this would share either trophy lists (graphical, text, or both) or a count of trophies. The user could choose to share only the selected trophies instead of the whole lot. Kevin VanDine just published a blog post about <a href="../../libgwibber">libgwibber</a> (which could be useful) here.</span>

<span style="font-family: arial, helvetica, sans-serif;">The Take a Picture button would export a picture of the display case with the current view settings (zoom, sort, background, etc.). Click one of the trophies to see what would happen when a trophy is selected.</span>

<span style="font-family: arial, helvetica, sans-serif;">(This will take you to the Trophies Detail mockup page.)</span>

<span style="font-family: arial, helvetica, sans-serif;"><strong>TROPHIES DETAIL (second mockup page)</strong></span>

<span style="font-family: arial, helvetica, sans-serif;"><strong><a href="http://geekyogre.com/content/images/2010/08/trophies_detail.png"><img class="alignnone size-full wp-image-1432" title="trophies_detail" src="http://geekyogre.com/content/images/2010/08/trophies_detail.png" alt="" width="498" height="340" /></a></strong></span>

<span style="font-family: arial, helvetica, sans-serif;">A box containing details of a trophy opens, showing a larger icon (128x128?), the trophy title, a description of how the trophy was unlocked, any humorous comments included by the trophy creator, the date and (perhaps) time the trophy was unlocked, trophy hiding options, and a button to reset the trophy. It might make more sense to have this box always open (and just blank when nothing is selected) instead of dynamically resizing the display case.</span>

<span style="font-family: arial, helvetica, sans-serif;">The trophy hiding options and the Forget I Unlocked This Trophy button would be available when multiple trophies are selected. Trophies hidden "everywhere, including from me" would be accessible by choosing "Show hidden trophies" from the View menu. The user may prefer not to show certain trophies for various reasons: they don't want others to know they're using a certain app (e.g., BitTorrent) or using their computer in a certain way (e.g., late at night or checking e-mail too often); or they don't like the title or icon of the trophy (e.g., one commenter suggested a trophy called "Serial Killer" for killing a frozen application 10 times; I don't want to have to explain that I'm really not a Jack the Ripper wannabe). </span>

<span style="font-family: arial, helvetica, sans-serif;">The Forget I Unlocked This Trophy button could be useful if the trophy was unlocked by someone borrowing the computer, or the user might have other reasons for "starting over" on a trophy. If the user clicks this button, a dialog would slide over the middle of the toolbar, saying, "You removed 3 trophies from your history; they will again be available for you to unlock. If you don't want to see the trophy anymore, you may hide it instead. Undo?" (like GMail does when you delete an email). An easy-to-use undo option is preferable over annoying the user with confirmation dialogs.</span>

<span style="font-family: arial, helvetica, sans-serif;">Click on the tab labeled "Get More" to show the interface for hints.</span>

<span style="font-family: arial, helvetica, sans-serif;"><strong>GET MORE (third mockup page)</strong></span>

<span style="font-family: arial, helvetica, sans-serif;"><a href="http://geekyogre.com/content/images/2010/08/get_more.png"><img class="alignnone size-full wp-image-1433" title="get_more" src="http://geekyogre.com/content/images/2010/08/get_more.png" alt="" width="498" height="340" /></a></span>

<span style="font-family: arial, helvetica, sans-serif;">The Get More tab would list two applications at a time: one installed application that doesn't have all its trophies achieved, and one not-currently-installed application that has a trophy to achieve. The applications are chosen at random and rotated out every day or so.</span>

<span style="font-family: arial, helvetica, sans-serif;">This would help the user to preserve the reward and surprise of unexpectedly unlocking a new trophy, yet still allow them to get help if they're stuck. Both sections would display the app's 48x48 icon, the app's title, and a brief, easy-to-understand description of the app. </span>
<ul>
	<li><span style="font-family: arial, helvetica, sans-serif;">The Run it now! button would run the application; it would change to "Switch to it!" if the application is already running, or "Where is it?" if the application doesn't have a window for its main interface (e.g. a panel applet, indicator, or icon in the notification area).</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">If the user clicked "Where is it?" the effect would be to dim the rest of the screen and show a red arrow pointing to the applet, indicator, icon, etc. The not-currently-installed application has two buttons.</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">The Install it! button would run the install command(s), asking permission from the user if the install requires adding or activating a PPA or other repository.</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">The Learn more button would show the application in the Ubuntu Software Center (or open a browser with the relevant OMG! Ubuntu blog post if it's not in the standard repositories).</span></li>
</ul>
</blockquote>
<span style="font-family: arial, helvetica, sans-serif;">After a discussion about an app-centric trophy view Adam came up with the following two mockups:</span>
<blockquote><span style="font-family: arial, helvetica, sans-serif;"><span style="line-height: normal; border-collapse: collapse;">I had a few ideas for viewing trophies by app:
</span></span>
<ol>
	<li style="margin-left: 15px;"><span style="font-family: arial, helvetica, sans-serif;">Keep it in the Trophies tab and add a "Group By" option for "Group By App" to the View menu.</span></li>
	<li style="margin-left: 15px;"><span style="font-family: arial, helvetica, sans-serif;">Keep it in the Trophies tab and add a "Show Apps" option in the View menu.</span></li>
	<li style="margin-left: 15px;"><span style="font-family: arial, helvetica, sans-serif;">Add an Apps tab—I think I like this approach best. It would be very similar to the Trophies tab setup. You could share or export this display just like you could with the one on the Trophies tab. The details area would also show details about an app when you click on an app icon or title.</span></li>
</ol>
<span style="font-family: arial, helvetica, sans-serif;">Here is a quick mockup of how this could look in either the Trophies tab or the Apps tab (it's similar to what I visualize for the list view with the Group By setting on):</span>

<span style="font-family: arial, helvetica, sans-serif;"><a href="http://geekyogre.com/content/images/2010/08/By-App1.png"><img class="alignnone size-full wp-image-1468" title="By App" src="http://geekyogre.com/content/images/2010/08/By-App1.png" alt="" width="488" height="274" /></a></span>

<span style="font-family: arial, helvetica, sans-serif;">(Tomboy is collapsed so its trophies are hidden)</span>
<span style="font-family: arial, helvetica, sans-serif;"> Trophies that aren't specifically related to any app come under a miscellaneous section, titled "General" or something. Also, I think if a trophy is related to more than one app (e.g., a trophy for working in gedit for a half hour while playing music in Banshee), it would show up under both apps.</span>

<span style="font-family: arial, helvetica, sans-serif;">Here's an alternate version with buttons for opening/switching to/highlighting an app (just like in the "Get More" tab):</span>

<span style="font-family: arial, helvetica, sans-serif;"><a href="http://geekyogre.com/content/images/2010/08/By-App-with-Buttons1.png"><img class="alignnone size-full wp-image-1469" title="By App with Buttons" src="http://geekyogre.com/content/images/2010/08/By-App-with-Buttons1.png" alt="" width="489" height="274" /></a></span>

<span style="font-family: arial, helvetica, sans-serif;">However, I think those buttons are better placed in the details section shown when the user selects an app, like the next mockup shows. (The mockups above aren't very good at telling the user they can select an app by its icon or name, so that would need some tweaking.)</span>

<span style="font-family: arial, helvetica, sans-serif;"><a href="http://geekyogre.com/content/images/2010/08/App-Details.png"><img class="alignnone size-full wp-image-1470" title="App Details" src="http://geekyogre.com/content/images/2010/08/App-Details.png" alt="" width="341" height="425" /></a></span></blockquote>
<span style="font-family: arial, helvetica, sans-serif;">So with that me and Kilian Valkhof will be implementing the UI using pygtk and Webkit (I have to get rid of my current UI).</span>

<span style="font-family: arial, helvetica, sans-serif; font-size: large;"><strong>Trophies</strong></span>

<span style="font-family: arial, helvetica, sans-serif;">I started working on a set of trophies in a service that uses Zeitgeist to award based on activities. Some simple cases that work are:</span>
<ul>
	<li><span style="font-family: arial, helvetica, sans-serif;">Tomboy Amateur: Edited 5 Tomboy Notes.</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">Tomboy Experienced User: Edited 15 Tomboy Notes</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">Tomboy Addict: Use at least Tomboy Note per day for 7 days in a row.</span></li>
</ul>
<span style="font-family: arial, helvetica, sans-serif;">This also works for Rhythmbox, Banshee and gedit at the moment (It is copy pasting the same code)</span>
<span style="font-family: arial, helvetica, sans-serif;"> Currently finishing a more advanced trophy set:</span>
<ul>
	<li><span style="font-family: arial, helvetica, sans-serif;">Jonoholic: Listen to all Severed Fifth songs from the new album</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">Jono Wannabe: (surprise) </span></li>
</ul>
<span style="font-family: arial, helvetica, sans-serif;">While many people disagree with the idea behind a trophy or achievement system there is at least to thinks that stand up for it:</span>
<ul>
	<li><span style="font-family: arial, helvetica, sans-serif;">Learning aid: Allow people to explore the system and use Applications. Give them the feeling of accomplishing something. Especially for kids.</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">Behavior monitor and control: The not so fun side would be awarding trophies for weird behavior: </span>
<ul>
	<li><span style="font-family: arial, helvetica, sans-serif;">Weirdo: Have the computer running for 8 hours without screensaver going on.</span></li>
	<li><span style="font-family: arial, helvetica, sans-serif;">Pervert: Watch 5 pornos in 24 hours.</span></li>
</ul>
</li>
</ul>
<span style="font-family: arial, helvetica, sans-serif; font-size: large;"><strong>What now?</strong></span>

<span style="font-family: arial, helvetica, sans-serif;">If you want to develop with a fun team please come on #omg!  on freenode and contact us. It is a small code base for everyone to have fun with.  Also we need a new name for OMG! so feel free to comment and suggest...</span>

</div>