---
layout: post
title: Hello GlobaLeaks
date: '2011-08-22 14:30:34'
---

While my opinion might be debatable, I think whistleblowing can help countries all over the world keep an eye out and judge the private companies and government entities that run countries. Also, the whisleblowing process (while protecting the anonymity of the whistleblower) needs to be transparent.

Up untill now there was no open-source platform to do so.

That is until I found out about GlobaLeaks, a group of young talented thinkers, hackers, journalists that are working on a safe, secure, transparent and depyloable whisleblowing platform.
I got in contact with some of them during the Jan 25 revolution. I will be working with them in my freetime, helping them build a developer community. Here is a public message they prepared for me to blog about.
<blockquote>Hey,

I'm writing to tell everyone about a new project that we've been hacking on for quite some time. We're really excited about it and it's called GlobaLeaks. GlobaLeaks is three things - it is first a project for creating software and for having discussion, it is secondly a collection of software for use by anyone interested in whistleblowing and it is third a collection of best practices for anyone interested in creating a whistleblowing platform.

What we have created is a Free and thus Open Source Whistleblowing platform. While the idea was born out of inspiration from the whole *leaks phenomenon it has developed to become something that focuses mainly on true whisleblowing.

During our research we discovered an incredible ecosystem of whistleblowing organizations and software to support whistleblowers and the rest of that ecosystem. There are people who have been active in this field for more than twenty years and are still active. A long term example is http://www.pcaw.co.uk/ - some of the long time whistleblowing advocates don't even consider WikiLeaks as whistleblowing. While we believe WikiLeaks is important, we think there is much more to whistleblowing beyond the WikiLeaks model as it is currently known.

We believe in the value of a range of activities and believe that tools such as the GlobaLeaks suite of software will empower people to stand up anonymously while making a change in their local context.
The true power of GlobaLeaks is to be able to impact and enforce change on a very local level, but before I go into doing any more pitching on why GlobaLeaks is so cool let me tell you a bit more about what it is.
Basically it is a web application, running as a Tor Hidden Service (https://www.torproject.org/docs/hidden-services.html.en). The fact that it runs as a Hidden Service protects the location of the server running the software. It also adds a layer of end-to-end encryption and authentication so any client connecting does not need to rely on legacy technology such as SSL/TLS authentication.

Any person running a GlobaLeaks node is called the node maintainer. By running the node as a Hidden Service he also is not required to register any domain names or static ip address because data is being transmitted over the Tor network; because this is a hidden service, there is no concern about Exit Node sniffing - the entire connection is encrypted, authenticated and anonymized. The node maintainer is has their identity protected and they do not need to expose themselves to possible retaliation.
Usually hidden serivices are only accessible from the Tor network, but what we have developed (based on Aaaron Swartz's Tor2web) is tor2web 2.0 that allows people coming from the normal web to visit hidden services. This means that a hidden service can reach a much wider audience.

A GlobaLeaks node is setup by somebody who has interest in motivating the citizens of that particular context into actively participating towards spotting mispractice and corruption.
Their role will be that of selecting targets responsible for analysing the material that is passed through their node. They will be knowledgable of that particular context so they will know who will be mostly interested in receiving and analysing the data. How they choose the targets is very important. The targets must be as much diversified as possible and with conflicting interests.

For example I will choose a left wing party and a right wing one, a certain labour union and also their opponent. This way their conflict of interest incentivizes targets in providing a more objective analysis of the material (e.x. some will be interested in confirming the facts whereas others will be interested in discrediting them).

A whisleblowers accesses the GL node using a Tor enabled browser to guarantee their anonymity. They upload the material and a notification is sent to the targets with a random time delay to avoid correlation attacks.

The target receives what is called a leank (leak link). This link is unique to their profile and after a certain amount of clicks it expires. They can access it either through Tor or through tor2web.
Leanks, in a later stage of development, will provide a way to have bi-directional communications (messaging) between the leaker and the targets.

The Leaker will be given a sort of Leak-Receipt-ID that allows him to come back and see the status of his submission, the list of people who downloaded it, if there are questions by targets and eventually requests for further information regarding the material.

GL will be delivered as a .exe/.app/.bin self-contained application that can be installed with just a click. The local activist will not require much training to configure and manage it.
Usability and ease of use are paramount. Target selection should be easily done even by a non technical crowd.

So this is basically it. We are currently looking for more developers interested in working on this project. Hopefully this breif description sparked your curiousity and you are interested in
knowing more.

Currently no code has been released publicly :(. What we have is a very rough prototype that we are quite ashamed of showing you. Yet the view of what globaleaks should be is very solid and are very open to suggestions and participation from all of the Open Source community.

So...
You should subscribe to our mailing list:
http://globaleaks.org/mailman/listinfo/people_globaleaks.org
You can join us on IRC:
irc.oftc.net #globaleaks

And please come and hack with us.

A Random GlobaLeaks Contributor</blockquote>