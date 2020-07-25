---
layout: post
title: More from the world of Zeitgeist
date: '2009-09-24 22:14:08'
---

<span style="background-color: #ffffff;">More hacking on the GNOME Activity Journal during the openSuSE conference hack sessions with some of the Zeitgeist guys (also working with UX team from canonical and Jason Smith) got it looking like that.</span>

<span style="background-color: #ffffff;"><a href="http://geekyogre.com/content/images/2009/09/Screenshot-21.png"><img class="alignnone size-full wp-image-837" title="Screenshot-21" src="http://geekyogre.com/content/images/2009/09/Screenshot-21.png" alt="Screenshot-21" width="604" height="361" /></a></span>

It will be possible to change between this "Mail view" and the standard "Journal View" since this was just a rearrangement of widgets. Also we will add the option of using Tracker search thanks to Ivan Frade and the rest.

-----------------------------------------------------

We are preparing for the 0.3 release of the engine now. Things are shaping up and this release will be really really powerful. It consists of 6 blueprints:
<ul>
	<li>Monitoring Document Focus (needs merging and reviewing): We can log the focus of the documents and calculate how long these documents were focused.</li>
	<li>Data Context Relevancy (needs merging and reviewing): Using the Focus Monitor we  generate accurate context relevancy graphs. So based on how one switches between documents we generate contextual relationships between them.</li>
	<li>Event - Document separation (heavy development): Allows us to have a more flexible API and rely on Tracker for metadata and document storage. Using our storage is still possible though thanks to Markus Korn's exchangeable backend module.</li>
	<li>Symbolic access of data models (needs love and is a quick hack): We will  use the content- and source types defined in Nepomuk throughout Zeitgeist, never using string constants defined inside each logger class. HELLO KDE AND CROSS-DESKTOP</li>
	<li>Events RDF Ontology (Drafting) : We will introduce a whole new ontology based on "Happenings" to extend the possibilities of the semantic desktop.</li>
	<li>Revamp parts of the Zeitgeist API (good progress): With all this happening we need some new methods to provide more awesomeness.</li>
</ul>
-----------------------------------------------------

<span style="background-color: #ffffff;">Other news would be "TALKS" about integrating in KDE, since we are moving to the Nepomuk ontology.</span>

<span style="background-color: #ffffff;">Good night internet
</span>
<div id="_mcePaste" style="overflow: hidden; position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px;">
<table id="speclisting" class="listing sortable" border="0">
<tbody>
<tr>
<td><span class="specpriorityESSENTIAL">Essential</span></td>
<td><a title="Aggregating document events through window focus" href="https://blueprints.launchpad.net/zeitgeist/+spec/monitor-document-focus">monitor-document-focus</a></td>
<td><span class="sortkey">3</span> <span class="specstatusDRAFT">Drafting</span></td>
<td><span class="sortkey">7</span> <span class="specdeliveryGOOD">Good progress</span></td>
<td><a href="https://blueprints.launchpad.net/%7Eseif">Seif Lotfy</a></td>
<td><a href="https://blueprints.launchpad.net/zeitgeist/0.3">0.3</a></td>
</tr>
<tr>
<td><span class="sortkey">5</span> <span class="specpriorityESSENTIAL">Essential</span></td>
<td><a title="Symbollic Access of the Datamodel" href="https://blueprints.launchpad.net/zeitgeist/+spec/zeitgeist-symbollic-datamodel">zeitgeist-symbollic-datamodel</a></td>
<td><span class="sortkey">3</span> <span class="specstatusDRAFT">Drafting</span></td>
<td><span class="sortkey">5</span> <span class="specdeliverySTARTED">Started</span></td>
<td></td>
<td><a href="https://blueprints.launchpad.net/zeitgeist/0.3">0.3</a></td>
</tr>
<tr>
<td><span class="sortkey">5</span> <span class="specpriorityESSENTIAL">Essential</span></td>
<td><a title="Events RDF Ontology" href="https://blueprints.launchpad.net/zeitgeist/+spec/events-rdf-ontology">events-rdf-ontology</a></td>
<td><span class="sortkey">4</span> <span class="specstatusDISCUSSION">Discussion</span></td>
<td><span class="sortkey">3</span> <span class="specdeliveryNEEDSINFRASTRUCTURE">Needs Infrastructure</span></td>
<td><a href="https://blueprints.launchpad.net/%7Ekamstrup">Mikkel Kamstrup Erlandsen</a></td>
<td><a href="https://blueprints.launchpad.net/zeitgeist/0.3">0.3</a></td>
</tr>
<tr>
<td><span class="sortkey">5</span> <span class="specpriorityESSENTIAL">Essential</span></td>
<td><a title="How we describe events" href="https://blueprints.launchpad.net/zeitgeist/+spec/zeitgeist-event-describtion">zeitgeist-event-describtion</a></td>
<td><span class="sortkey">4</span> <span class="specstatusDISCUSSION">Discussion</span></td>
<td><span class="sortkey">3</span> <span class="specdeliveryNEEDSINFRASTRUCTURE">Needs Infrastructure</span></td>
<td><a href="https://blueprints.launchpad.net/%7Erainct">Siegfried Gevatter</a></td>
<td><a href="https://blueprints.launchpad.net/zeitgeist/0.3">0.3</a></td>
</tr>
<tr>
<td><span class="sortkey">4</span> <span class="specpriorityHIGH">High</span></td>
<td><a title="Data Context Relevancy Provider" href="https://blueprints.launchpad.net/zeitgeist/+spec/data-context-relevancy-provider">data-context-relevancy-provider</a> <span class="sprite branch" title="Branch is available"> </span></td>
<td><span class="sortkey">3</span> <span class="specstatusDRAFT">Drafting</span></td>
<td><span class="sortkey">7</span> <span class="specdeliveryGOOD">Good progress</span></td>
<td><a href="https://blueprints.launchpad.net/%7Eeinalex">Alexander Gabriel</a></td>
<td><a href="https://blueprints.launchpad.net/zeitgeist/0.3">0.3</a></td>
</tr>
<tr>
<td><span class="sortkey">1</span> <span class="specpriorityUNDEFINED">Undefined</span></td>
<td><a title="Revamped DBus API for the Zeitgesit Engine" href="https://blueprints.launchpad.net/zeitgeist/+spec/zeitgeist-revamp-engine-api">zeitgeist-revamp-engine-api</a></td>
<td><span class="sortkey">3</span> <span class="specstatusDRAFT">Drafting</span></td>
<td><span class="sortkey">5</span> <span class="specdeliverySTARTED">Started</span></td>
<td><a href="https://blueprints.launchpad.net/%7Ekamstrup">Mikkel Kamstrup Erlandsen</a></td>
<td><a href="https://blueprints.launchpad.net/zeitgeist/0.3">0.3</a></td>
</tr>
</tbody></table>
</div>