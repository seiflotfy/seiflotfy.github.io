---
layout: post
title: Help with Mono for Zeitgeist
date: '2010-08-22 18:39:00'
---

At Zeitgeist we are finishing up some nice Tomboy and Banshee Addins.

Currently we are facing an issue with Mono DBus and we reached a new level of desperateness.

You need to have Zeitgeist running and installed as well as the latest 0.6.1 NDesk.DBus bindings.

I wrote a python script as as well as a Mono App to demo the problem we are facing.

Both app send the same request to the Zeitgeist DBus Interface and Zeitgeist acts upon it. Also using dbus-monitor  I can see that Zeitgeist is sending back the results. However the results dont make it to the Mono app although the python one gets them...

the input signature is nasty but again it doesnt matter since it gets invoked by both the mono and python app
<p style="padding-left: 30px;"><em>(xx)a(asaasay)a(assaasay)uuu</em></p>
<em> </em>the output signature is
<p style="padding-left: 30px;"><em>as</em></p>
Here are the two apps:

<strong><a href="http://pastebin.com/mwEdEZDs">Mono</a></strong>

<script src="http://pastebin.com/embed_js.php?i=mwEdEZDs"></script>
 The output:

<blockquote>
*** file:///home/seif/Desktop/test.py System.String[]
</blockquote>

<strong><a href="http://pastebin.com/SAqY0cvV">Python</a></strong>
 <script src="http://pastebin.com/embed_js.php?i=SAqY0cvV"></script>
The output:
<blockquote>*** file:///home/seif/Desktop/test.py
dbus.Array([dbus.String(u'note://tomboy/3ed87be0-2bee-4d02-9809-d1b06937d77a'), dbus.String(u'file:///home/seif/Downloads/dbus-explorer-0.5.tar.gz')], signature=dbus.Signature('s'))</blockquote>
You can see both outputs are not the same, somehow the mono app is not getting the replies back and as i said I can see in Zeitgeist that its being invoked by mono as well as the results being sent when looking in dbus-monitor.

If you want to try it yourself and help us make sure to replace the uri variables with one existing on your computer and that gets logged by Zeitgeist...
Thank you in advance for any help or tips

UPDATE <strong>PROBLEM SOLVED... I AM STUPID SOMETIMES
</strong>
