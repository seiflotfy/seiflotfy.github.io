---
layout: post
title: 'Zeitgeist: The Road to Maverick Meerkat'
date: '2010-05-15 12:35:50'
---

<span style="color: #333333;">Just like last year Zeitgeist developers were present at UDS...
It was amazing I will write about the UDS exprience in another blogpost.
I think my favorite moment was Mark announcing Unity and using Zeitgeist for file management on the desktop. Although Mikkel knew about it (he works for Canonical), it took the rest of the team by surprise. It is very nice to feel appreciated. And I think i speak on behalf of the whole team when I say "Thank you Ubuntu and Canonical for giving us a chance".</span>

<span style="color: #333333;">This being said, working with Ubuntu and Canonical is in  an honor and we need to provide them with something stable and maintainable. To cut to the point here is a list of how we should proceed within the next couple of months:</span>

<strong><span style="color: #333333;">Zeitgeist Core:</span></strong>

<span style="color: #333333;">We need to focus on providing a good product. We had and still have good ideas but we need to look into setting limits for a short period of time.</span>
<ul>
	<li><span style="color: #ff0000;">Feature Freeze set date</span><span style="color: #333333;">: We should freeze any set of features we have in a queue... maybe we should set a deadline for discussing any new ideas someone might want to add to Zeitgeist. IMHO we should freeze after the current blueprints. New features mean new API methods means new bugs and more maintenance on a short term. Which leads us to the second point.</span></li>
	<li><span style="color: #ff0000;">Bug fixing</span><span style="color: #333333;">: We need to fix every bug in our list. There is not much left an to be honest, we did do a good job on that so lets focus on working them all off.</span></li>
	<li><span style="color: #ff0000;">QA</span><span style="color: #333333;">: By far the most important point. If we want to be taken seriously and deploy on a larger scale we need to prove we are stable. One of the obstacles we have is that we are written in python. For the hardcore fanatic developers it is a no go. However IF we can prove that we are: </span>
<ul>
	<li><em><span style="color: #333333;">STABLE</span></em><span style="color: #333333;">: Fix all bugs. Nothing should crash etc...</span></li>
	<li><em><span style="color: #333333;">MEMORY EFFICIENT</span></em><span style="color: #333333;">: We should look into where we can reduce memory consumption and maybe not loading all libs or init everything on startup. Mikkel suggested looking into SQLite caching.</span></li>
	<li><em><span style="color: #333333;">PERFORMANCE EFFICIENT</span></em><span style="color: #333333;">: I think we are good in that department but still we should go over it again.</span></li>
	<li><em><span style="color: #333333;">RELIABLE</span></em><span style="color: #333333;">: We might be stable by delivering results but we need to be reliable by delivering the expected. This means writing lots and lots of Tests. we should try reaching 200 test. There is no such thing as a redundant test.</span></li>
	<li><em><span style="color: #333333;">MAINTAINABLE</span></em><span style="color: #333333;">: Clean up code. Try to split big big big methods into smaller methods to make it readable and maintainable. I know it collides with performance but I think we should reach some middle ground there.</span></li>
</ul>
	</li><li><span style="color: #ff0000;">Documentation</span><span style="color: #333333;">: Look into having reliable documentation. Just like unit tests there in no such thing as too much documentation. If we can document a method or a variable then we should do it. It will make life easier for us to maintain each others modules and methods. Also the online documentation has to be always up to date, a nightly build from trunk would be awesome.</span></li>
</ul><ul></ul>


<strong><span style="color: #333333;">Deployment:</span></strong>

<span style="color: #333333;">Now we need to integrate more with the desktop more. So IMHO we should set and focus on a couple of deployment opportunities. We will try to use the libzeitgeist as much as possible to assist Mikkel with bug tracking as well looking more into C code and stabilizing it. So back to some deployment opportunities, I wouldn't mind coordinating those things.</span>
<ul>
	<li><span style="color: #ff0000;">GAJ</span><span style="color: #333333;">: we should stabilize it for GNOME 3 (even though we did not make it in) or the next Ubuntu Release. Randy﻿ (tehk) is doing some nice work with that.</span></li>
	<li><span style="color: #ff0000;">Ubuntu Music Store</span><span style="color: #333333;">: *secret for now* :P</span></li>
	<li><span style="color: #ff0000;">Windicators and Indicators</span><span style="color: #333333;">: Look into Michal's (mhr3) recentlyused stuff in AWN and deploy it as an indicator or windicators for different applications.</span></li>
</ul>
<strong><span style="color: #333333;">Community:</span></strong>

<span style="color: #333333;">Part of being Ubuntu upstream we need to look at our community that surrounds us. There is a big amount of enthusiastic developers that have nice ideas of how to integrate Zeitgeist into the Desktop Experience. To reach out to the community and developers we set up some tools to ease the development and contribution to Zeitgeist. Launchpad is our main development infrastructure thus it is easy to cooperate and get in contact with us:</span>
<ul>
	<li><span style="color: #ff0000;">The main Project page</span><span style="color: #333333;">: </span><a href="https://edge.launchpad.net/zeitgeist-project"><span style="color: #333333;">https://edge.launchpad.net/zeitgeist-project</span></a><span style="color: #333333;"> . You will have a quick access to all kind of Zeitgeist related project such as GAJ etc...</span></li>
	<li><span style="color: #ff0000;">PPA for Engine</span><span style="color: #333333;">: </span><a href="https://edge.launchpad.net/~zeitgeist/+archive/ppa"><span style="color: #333333;">https://edge.launchpad.net/~zeitgeist/+archive/ppa</span></a></li>
	<li><span style="color: #ff0000;"><span style="color: #333333;"><span style="color: #ff0000;">Data Providers</span>: </span><a href="https://edge.launchpad.net/zeitgeist-dataproviders"><span style="color: #333333;">https://edge.launchpad.net/zeitgeist-dataproviders</span></a><span style="color: #333333;"> .</span><span style="color: #333333;"> </span><span style="color: #333333;">While Zeitgeist comes with a standard recentlyused monitor, we have another set of data providers that are either not supported by the recentlyused manager, such as tomboy and rhythmbox, or allow us to get more info through them than through recently used maanger. We need to finish an installer package for our dataproviders and update it on a constant basis with every dataprovider release or update. Installation of data providers should be straight forward.</span></span></li>
	<li><span style="color: #ff0000;">Documentation</span><span style="color: #333333;">: </span><a href="http://zeitgeist-project.com/docs/trunk/"><span style="color: #333333;">http://zeitgeist-project.com/docs/trunk/</span></a><span style="color: #333333;"> is a documentation with a few tutorials and examples.</span></li>
	<li><span style="color: #ff0000;">Mailing List</span><span style="color: #333333;">: you can always contact us on </span><span style="color: #333333;">dev &lt;at&gt; zeitgeist-project &lt;dot&gt; com</span></li>
	<li><span style="color: #ff0000;"><span style="color: #ff0000;">IRC</span><span style="color: #000000;"><span style="color: #333333;">:</span><span style="color: #888888;"><span style="color: #333333;"> </span><span style="color: #333333;">just join us at #zeitgeist on irc.freenode.net</span></span></span></span></li>
</ul>
<span style="color: #000000;">These are interesting times ahead, and the Zeitgeist team is psyched like never before...</span>