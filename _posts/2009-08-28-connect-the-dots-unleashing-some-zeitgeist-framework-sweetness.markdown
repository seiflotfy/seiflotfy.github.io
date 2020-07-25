---
layout: post
title: Connect the dots! (Unleashing some Zeitgeist Framework sweetness)
date: '2009-08-28 02:01:48'
---

<span style="background-color: #ffffff;">There are 3 types of relationships between items:</span>
<ol>
	<li><strong>Content</strong>: Lets say two documents have the same content "Hello World" thus there is a probabilty that they are about the same topic. This could be done using indexers and keywords extractors like <a href="http://projects.gnome.org/tracker/">Tracker</a> Indexer.</li>
	<li><strong>Metadata</strong>: Tags, mimetypes, etc... are all data that describe the uniqueness of an URI. Data sharing the same tags or "Artist name" or even exist in the same folder are related over these attributes. This area is very well covered by <a href="http://projects.gnome.org/tracker/">Tracker</a> as well as <a href="http://www.organise-fw.org">Organise FW</a>'s "Path Projection".</li>
	<li><strong>Context</strong>: Well there are some things where content is hard to compare such as Websites and Videos. One can extract the metadata, but what if they show no relationships? However the context of the usage they were used in is somehow related. Let's assume I visited Will Smith's profile on IMDB (y)  and somehow then started watching Prince of Bel Air (x). There are a lot of instances where I also watched PoBA(x) too such as work while editing work.py (z). Now to be able to determine which of my activities lead to watching PoBA(x) I need something that can look at PoBA as a single node and look for URI activities that lead to using it as well as URI activities that were initiated by the usage of PoBA. The intensity of the relationship can be determined with the number of times these activities were undertaken in any given time period. This set of nodes(URIs) around PoBA we called activity neighborhoods.</li>
</ol>
The rest of this post will cover point 3.
<blockquote>BTW the following images are actually plotted by a Zeitgeist framework extension developed by <a title="Alexander Gabriel" href="http://einalex.mayanna.org" target="_blank">Alexander Gabriel</a> and me in an attempt to implement related items for Gnome Shell and Gnome Zeitgeist.</blockquote>
Activity neighborhoods can be of any degree. By degree I mean the sequence of nodes(URIs) that could possibly lead to the acitviy(x). A relationship of N0(<em>x</em>)  can be seen as the set of items that directly lead to the usage <em>x</em> as well as URIs acitvites initiated by the usage of <em>x</em>.
<blockquote>10:01 edited <em>y</em>

10:04 opened <em>x</em>

10:05 watched <em>z</em>

10:06 edited <em>x</em></blockquote>
The neighbourhood N0(<em>x</em>) = { -: [<em>y</em>,<em>z</em>], +:[<em>z</em>] }. This shows that <em>z</em> was used once before and after <em>x </em>and <em>y</em> was only used before <em>x </em>making <em>z </em>more relevant to <em>x </em>for now.
<blockquote>"-" stands for incoming and "+" stands for outgoing</blockquote>
N0(<em>z</em>) = { -: [<em>x</em>], +:[<em>x</em>]} we cat see the relationship over 0 nodes.  -N0(<em>z</em>) are the incoming URIs and +N0(<em>z</em>) are the outgoing URIs.

but what if we say N2(<em>z</em>) ??? With this we want all items that
<ul>
	<li><span style="background-color: #ffffff;">either directly lead to or the items that lead to the items that lead to <em>z</em> </span></li>
	<li><span style="background-color: #ffffff;">the items were initiated by <em>z</em> or items that initiated to the usage of the items that lead to the usage of <em>z</em></span></li>
</ul>
It's very easy
<blockquote>N1(<em>z</em>) = N0(<em>z</em>) + ( N0(<em>e</em>)  ) where <em>e</em> is an element in N1(<em>z</em>)

=====&gt;          N1(<em>z</em>) = { -:[-N0(<em>z</em>) + <em>y</em>] , +:[N0(<em>z</em>)]}

<span style="background-color: #ffffff;">=====&gt;          N1(<em>z</em>) = { -:[x, <em>y</em>] , +:[x]}</span></blockquote>
<span style="background-color: #ffffff;">So enough theory lets connect the dots. The following images are plot of trees and graphs mapping my current Zeitgeist DB. </span>

<span style="background-color: #ffffff;">The nodes in the plots represent URIs and the arrows represent absolute events on URIs before or following the node attached to.
</span>

<span style="background-color: #ffffff;">So first lets demo No("Bad Boys"), here bad boys is presented by "0":</span>

<span style="background-color: #ffffff;"><a href="http://geekyogre.com/content/images/2009/08/badboysD1.png"><img class="alignnone size-full wp-image-799" title="badboysD1" src="http://geekyogre.com/content/images/2009/08/badboysD1.png" alt="badboysD1" width="732" height="359" /></a></span>

This shows us that items 1-10 followed the usage of 0 while 11-12 were followed by 0. However 2,7,8 and 10 were also again used before 0.

<span style="background-color: #ffffff;">Now for N1("Bad Boys"):</span>

<span style="background-color: #ffffff;"><a href="http://geekyogre.com/content/images/2009/08/badboysD21.png"><img class="alignnone size-full wp-image-801" title="badboysD2" src="http://geekyogre.com/content/images/2009/08/badboysD21.png" alt="badboysD2" width="748" height="278" /></a>
</span>

<span style="background-color: #ffffff;">You can see here that everything leads over maximum 1 Node to "0". And only 12 of them lead directly to 0.</span>

<span style="background-color: #ffffff;"> </span><span style="background-color: #ffffff;">The numbers in the plots don't really match since the traversing differs from N0 to N1, however if you take a good look the amount of directly incoming and outgoing arrows to/from "0" is still the same! 10 outgoing and 12 incoming!</span>

Currently the arrows have a low weight because the history of my current netbook is less than a week plus we only cover open/save events. Tomorrow we will implement window focus events to make things more dynamic. Once we can set weights of the arrows with the duration of the event to start or the lifetime of the items we can filter and prioritize the related nodes.

Right now all items in a small cycle with high weightend arrows are considered definite relationships!

<span style="background-color: #ffffff;">Now for a more bad ass plot of my todays activities :)</span>

<span style="background-color: #ffffff;"><a href="http://geekyogre.com/content/images/2009/08/graph.svg">graph</a>
</span>

<span style="background-color: #ffffff;">
</span>

<span style="background-color: #ffffff;">
</span>

<span style="background-color: #ffffff;">
</span>