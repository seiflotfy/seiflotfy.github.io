---
layout: post
title: Howto install Hauppauge WinTV HVR 1100 under Ubuntu(Jaunty)
date: '2009-04-20 11:42:43'
---

<p class="line874">This howto is for installing Hauppuage WinTV HVR 1100 under Ubuntu  "might work for other wintv cards" no guarantee though...</p>
<p class="line862">I used this froum its in french though --&gt; <a class="http" href="http://forum.ubuntu-fr.org/viewtopic.php?id=73834&amp;p=1">http://forum.ubuntu-fr.org/viewtopic.php?id=73834&amp;p=1</a></p>
<p class="line874">Here we go first check if your card got detected</p>

<blockquote>
<p class="line874">lspci</p>
</blockquote>
<ul></ul>
<p class="line874">you should get something like:</p>

<blockquote>
<p class="line874">0000:00:12.0 Multimedia controller:Philips Semiconductors SAA7133 Video Broadcast Decoder (rev d1)         Subsystem: Hauppauge computer works Inc.: Unknown device 6701         Flags: bus master, medium devsel, latency 32, IRQ 12         Memory at eb101000 (32-bit, non-prefetchable) [size=2K]         Capabilities: [40] Power Management version 2</p>
</blockquote>
<ul></ul>
<p class="line874">first make sure you have the packacges required for the configuration of the card, open a console and type:</p>

<blockquote>
<p class="line874">sudo apt-get install build-essential mercurial linux-headers-`uname -r` dvb-utils</p>
</blockquote>
<ul></ul>
<p class="line874">then get the v4l-dvb files:</p>

<blockquote>
<p class="line874">cd /opt/ hg clonehttp://linuxtv.org/hg/v4l-dvb cd v4l-dvb</p>
<p class="line874">make sudo make install</p>
<p class="line874">sudo -s</p>
</blockquote>
<ul></ul>
<p class="line874">then modprobe:</p>

<blockquote>
<p class="line874">sudo modprobe -r saa7134-alsa saa7134-dvb saa7134 &amp;&amp; sudo modprobe saa7134 card=101 &amp;&amp; sudo modprobe saa7134-dvb echo "saa7134-dvb" &gt;&gt; /etc/modules</p>
</blockquote>
<ul></ul>
<p class="line874">now  get the firmware compatible with your card from <a class="http" href="http://thadathil.net:8000/dvb/">http://thadathil.net:8000/dvb/</a> then "sudo" copy it to /lib/firmware</p>

<blockquote>
<p class="line874">sudo reboot</p>
</blockquote>
<ul></ul>
<p class="line874">I think that was it use scantv or mythtv to scan for channels i will write a tutorial as soon as i get to it</p>