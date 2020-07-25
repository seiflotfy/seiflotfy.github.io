---
layout: post
title: Rocking with Zeitgeist
date: '2010-04-05 01:35:24'
---

I must say I am very excited about the new developments happening in the Zeitgeist World... I have no idea where to start but here goes nothing.

Our new hacker Morten Mjelva took it as his duty to cook up the telepathy logger....... WOW it works like charm thanks to the support of Danni, Sjoerd and the guys from Collabora, it is always a pleasure to work with them. Zeitgeist now logs when messages were sent/received and when dialogs were opened/closed. This led to a chain reaction of new developments. Morten is a amazing.  We immediately sat down and started rethinking our association algorithms. 3 days later we rewrote it to make it 5 times faster and much more accurate thanks to Laszlo Pandy's suggestions to use "sliding windows" instead of "transactions". Yesterday we hooked it up with AJ and in the "More Information" Window.  We then put in the "Relevant Items" option and the results are better than we expected :)

Randy is restructuring AJ to support stuff like chats/websites and other non file-based activities.

Here are 2 Pictures of our first try to get AJ to show the contacts we chatted with (in this case Hylke) and related items, and another one viewing just items related to an html file

(KEEP IN MIND THIS IS A 2 MINUTE HACK)

<a href="http://geekyogre.com/content/images/2010/04/Screenshot-ZG.png"><img class="alignnone size-full wp-image-1132" title="Screenshot-ZG" src="http://geekyogre.com/content/images/2010/04/Screenshot-ZG.png" alt="" width="659" height="431" /></a>

<a href="http://geekyogre.com/content/images/2010/04/Screenshot-4.png"><img class="alignnone size-full wp-image-1133" title="Screenshot-4" src="http://geekyogre.com/content/images/2010/04/Screenshot-4.png" alt="" width="653" height="428" /></a>

This being said I forgot to announce the intense cooperation with the Elementary Project. Guys look out for it because it really takes simplicity and design to another level. Daniel Fore aka DanRabbit designed and started hacking on Dash... A simple yet elegant semi-semantic file browser. Thanks to Randy's zeitgeist-sharp lib the integration with Dash is going to be a breeze. It is still in an early stage but  the integration till now will be a nice top bar that i intend to infect with Zeitgeist+Tracker sweetness (congrats on the 0.8 guys), as seen here..

<img class="alignnone" title="Dash2" src="http://fc03.deviantart.net/fs71/f/2010/088/6/4/Search_Filter_Bar_by_DanRabbit.png" alt="" width="480" height="330" />

It is based on Thorsten Prante's approach to change what I was doing with <a href="http://geekyogre.com/2010/03/reviving-gimmie-using-zeitgeist-meet-sezen/">Sezen</a> to include Tracker search and make it standalone search app as seen here...

<img class="alignnone" title="Sezen" src="http://img683.yfrog.com/img683/5826/gt1l.png" alt="" width="658" height="462" />

And ofcouse the big zeitgeist magic in form 0f a sidebar showing related files to the selected one, as seen here...

<img title="Dash1" src="http://fc07.deviantart.net/fs70/f/2010/093/f/4/Dash_Context_Pane_Concept_by_DanRabbit.png" alt="" width="480" height="330" />

The sidebar already has a little python prototype that just proves the concept. I started hacking it today to be able to view associated files/contacts/etc based on the zeitgeist algorithms. It is a very simple hack and kinda reminds me of <a href="http://nat.org/dashboard/">Nat Friedmans's Dashboard</a>. But this is purely context driven. "What do I usually do while chatting with Hylke within the last 2 weeks" was the query of the following demo. You can see how quick associations are calculated.

<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="400" height="300" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowfullscreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="src" value="http://vimeo.com/moogaloop.swf?clip_id=10678237&amp;server=vimeo.com&amp;show_title=1&amp;show_byline=1&amp;show_portrait=0&amp;color=&amp;fullscreen=1" /><embed type="application/x-shockwave-flash" width="400" height="300" src="http://vimeo.com/moogaloop.swf?clip_id=10678237&amp;server=vimeo.com&amp;show_title=1&amp;show_byline=1&amp;show_portrait=0&amp;color=&amp;fullscreen=1" allowscriptaccess="always" allowfullscreen="true"></embed></object>

P.S: <strong>Watch the video in HD if possible to understand the context</strong>. Also I cant type when excited :) <a href="http://vimeo.com/10678237">http://vimeo.com/10678237</a>

Now the hardcore stuff...

Randy Barlow started hacking a zeitgeist-sharp lib and wrote a plugin for banshee. When he is back I will post the pictures here...

Besides the association algorithms being implemented the rockstars Markus and Mikkel have finished drafting and implementing our ontology. Ladies and gentlemen the first initiative for a "Zeitgeist Event Ontology" or better yet ZEO can be seen <a href="http://bazaar.launchpad.net/~zeitgeist/zeitgeist/ontology_definition/annotate/head:/extra/ontology/zg.trig">here</a>. This work deserves a post on its own since it will allow some crazy types of associations.

Our youngest star Siegfried (our GSoC student from last year) is coordinating the Zeitgeist 0.3.3 release due the next 2 weeks at max. Stay tuned... because shortly after that GAJ will e out with a new release.