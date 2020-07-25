---
layout: post
title: Zeitgeist on its way into KDE
date: '2011-06-06 20:35:17'
---

<a href="http://trueg.wordpress.com/2011/06/06/randa-and-ontologies-and-whatnot/">You can read about it here...</a>

The basic structure of events as understood by both projects Nepomuk and Zeitgeist are different.

Nepomuk looks at events as an "activity on a subject" with a duration with a start and end. Zeitgeist on the other hand looks as an event as an entitiy in time. So Open and Close are 2 different events for Zeitgeist while in Nepomuk their are properties of an Event.

Yet this did not stand in our way. We reached a solution where no side had to compromise but only purely collaborate.

To cut it short...
<ol>
	<li>Zeitgeist and Nepomuk worked on extending NUAO for the Shared Desktop Ontology</li>
	<li>Zeitgeist will still use its own ontology but map everything into NUAO before pushing into Nepomuk. Our internal DB will be kept for our own reasons. It is encouraged that developers who want to ask for events to interact with Nepomuk though. Yet it will be possible to interact with Zeitgeist (we can search over Nepomuk via an extension)</li>
	<li>Here is the structure for the implementation.<a href="http://trueg.files.wordpress.com/2011/06/zeitgeist-nepomuk-kde-integration.png"><img class="alignnone" src="http://trueg.files.wordpress.com/2011/06/zeitgeist-nepomuk-kde-integration.png" alt="" width="765" height="332" /></a></li>
	<li>We got this more or less working... <strong>without having to change Zeitgeist code! </strong>This is all done over Zeitgeist extensions, leaving Nepomuk and Zeitgeist unchanged.</li>
</ol>
I must say this was a great week. Sebastian Trueg, Ivan Cukic and Trever Fischer just made it happen. And I am glad we are moving forward.

P.S: I am here with Ryan Lortie. KDE has been holding us hostage in a room because we are GNOMErs :P (kidding). No honestly it was very productive and having Zeitgeist and dconf now in adoption by KDE is just a good example of cross desktop collaboration.