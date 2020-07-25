---
layout: post
title: Zeitgeist Log Manager (Mockup) - Giving Control to the User
date: '2010-09-03 13:17:50'
---

Blacklisting stuff from being logged, has been a feature in Zeitgeist for a long time now. Yet we never came to develop a UI for it.

So upon popular demand we started to mockup this feature.
<p style="text-align: left;">The UI is simple and straight forward. (I sketched it using <a href="http://pencil.evolus.vn/en-US/Home.aspx">Pencil</a>)</p>
<p style="text-align: left;">It uses much from what Sezen has to offer, in this case we use the same categories and the searching functionality. So when you search the categories with results get highlighted to allow you to control the logging of the results.</p>
<p style="text-align: left;"><a href="http://geekyogre.com/content/images/2010/09/Untitled-Page3.png"><img class="alignnone size-full wp-image-1548" title="Untitled Page" src="http://geekyogre.com/content/images/2010/09/Untitled-Page3.png" alt="" width="690" height="557" /></a></p>
<p style="text-align: left;"></p>

<ul>
	<li>You can go toggle <strong>Incognito</strong> mode by setting <strong>Logger Status </strong>to inactive. This will block everything from getting logged in Zeitgeist.</li>
	<li>Under General you can choose which <strong>Applications</strong> you want to log. In this case I am allowing Firefox to be logged but disabling Cheese and Banshee. The application lists will be pulled from the what has been logged by Zeitgeist as well as the applications installed. The option to add new applications to be logged manually is also possible through the add and remove buttons. Same applies for <strong>Directories</strong>.</li>
</ul>
<a href="http://geekyogre.com/content/images/2010/09/Untitled-Page22.png"><img class="alignnone size-full wp-image-1552" title="Untitled Page2" src="http://geekyogre.com/content/images/2010/09/Untitled-Page22.png" alt="" width="690" height="557" /></a>
<ul>
	<li>The Documents/Music/Videos/Websites/People/Notes and Other Categories all use the same widget layout. You can enable and disable logging for all items of types of each category. In this case by toggling the <strong>Allow Logging Documents</strong> and controlling single items from a list populated by manually adding items using the <strong>Add</strong> Button. <strong>Remove</strong> Button on the other hand will ask you to remove all instances for all time. We will think of  a way to delete single instances but for now it can be done over the Activity Journal.</li>
</ul>
This is just some initial mockups. If you want to join the development please join #zeitgeist on irc.freenode.net and don't hesitate to ask for guidance. If you have a better idea for mockups please don't hesitate to present it to us.