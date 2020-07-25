---
layout: post
title: My Take on Zeitgeist and GAJ not being in GNOME (A Personal Rant)
date: '2010-06-11 16:19:01'
---

<strong>Rejection reasons for GAJ:</strong>

<strong> </strong>

<strong>
<ul>
	<li><span style="font-weight: normal;"><strong>
<p style="display: inline !important;"><span style="font-weight: normal;"><strong> </strong></span></p>

</strong><strong>The original design idea is one we want to see happen during the GNOME 3 development.</strong>

</span></li>
</ul>
</strong>

<strong> </strong>

<strong> </strong>

<span style="font-weight: normal;">And what is the current idea... Sorry but it is EXACTLY the same features. Browsing Activity through time and finding associations using Zeitgeist and Searching, Tagging and Bookmarking using Tracker. The reasoning here is to vague...</span>
<ul>
	<li><span style="font-weight: normal;"><strong>
<p style="display: inline !important;"><span style="font-weight: normal;"><strong> </strong></span></p>

</strong><strong>needs more integration with the rest of the desktop and the overall.</strong><strong> </strong>

<strong> </strong>

</span></li>
</ul>
<span style="font-weight: normal;">You mean integrating Zeitgeist not GAJ... GAJ is a UI so do you want us to provide GAJ widgets like Empathy does with its widgets?</span>
<ul>
	<li><span style="font-weight: normal;"><strong>GNOME design; right now, it feels too much like a standalone application.</strong></span></li>
</ul>
<span style="font-weight: normal;">It took us a lot of effort to get it looking the way it does now and I believe it Truly blends in with the Desktop. Hylke Bons did some amazing designs. And sorry it is not like we came out with a surprise design and implementation. We worked in the open. We blogged about the development. You could have told us it looks to "standalone"... Empathy is a standalone app AFAIK. I somewhat agree that GAJ might feel out of place in GS, it feels more like a G2. That is partly because of the highly themed environment GS sports, anything that is not native to GS will feel out of place there actually.</span>
<ul>
	<li><span style="font-weight: normal;"><strong>The team might need to work a bit more closely with other GNOME teams for the integration.</strong></span></li>
</ul>
<span style="font-weight: normal;">Integrate a UI??? Again this makes no sense at all... Again you seem to not be able to differentiate between Zeitgeist and GAJ...</span>

<strong>Rejection reasons of Zeitgeist:</strong>
<ul>
	<li><span style="font-weight: normal;"><strong>Not needed since GNOME Activity Journal is not approved. If another module will need it for 3.0, this decision will get revisited.</strong></span></li>
</ul>
<span style="font-weight: normal;">I don't know any official module that use Tracker yet. However it is a blessed dependency, which makes A LOT of sense to me, since it encouraged us to write Tracker extensions and make it a GAJ dependency. How do you expect people to depend on something that is not blessed. We will be shipping out shit loads of plugins soon so maybe you will revisit this decision (Thank you GSoC for Michal Hruby).</span>

<span style="font-weight: normal;"><strong> </strong></span>

<strong> </strong>

<strong>
<p style="display: inline !important;">These being official reason, I know there are a lot of other reasons that could have played a role:</p>

</strong>
<ul>
	<li><span style="font-weight: normal;"><strong>Zeitgeist in Launchpad.</strong></span></li>
</ul>
<span style="font-weight: normal;">A lot of people hold a grudge against us for that but hey its free, open source and wont bite you. Sorry but GNOME's infrastructure from my point of view just doesn't match launchpad. I am not talking Bazaar vs Git. But the whole Management System.</span>
<ul>
	<li><span style="font-weight: normal;"><strong>Not integrating with Shell.</strong></span></li>
</ul>
<span style="font-weight: normal;">We want to but there were many problems in the way that we managed to put aside. Yet we need to find the time. If anyone wants to integrate into Shell contact us. But as long as we are not blessed it makes it hard for us. It make sense to integrate Zeitgeist into Shell and give it functionality but it makes no sense to reject GAJ for that. GAJ will offer more Zeitgeist functionality than Shell... More detailed browsing is one example.</span>
<ul>
	<li><span style="font-weight: normal;"><strong>Our high affiliation with Ubuntu and Canonical.</strong></span></li>
</ul>
<span style="font-weight: normal;">Their mentality about encouraging development and innovation ACROSS the desktop. Yes *apparently* Canonical did its fair share of *mean* stuff but hey lately they have been amazingly nice and supportive. Plus all our devs use Ubuntu. </span><span style="font-weight: normal;"><strong> </strong></span>

<strong> </strong>

<strong>
<p style="display: inline !important;"><span style="font-weight: normal;">Canonical hired our lead architect and payed him to write libzeitgeist a C Wrapper around our DBus interface. It would make perfect sense for other GNOME projects to look at it... Thank you Canonical</span></p>

</strong>
<ul>
	<li><span style="font-weight: normal;"><strong>Our professional image</strong></span></li>
</ul>
<span style="font-weight: normal;">Yes I am over enthusiastic but why should my team suffer from that. Zeitgeist has 5 core devs and 3 contributing devs. We all make sure that we are having fun and every1 established his role in the team to offer the best possible combination. Our code is reliable. We hunt all bugs out and are very stable and efficient even though written in python.</span>

---

For now we will live with the downstream, ISV and community projects that embraced us, ask GNOME people to help us get things right, with the Zeitgeist and GAJ inclusion for 3.2...