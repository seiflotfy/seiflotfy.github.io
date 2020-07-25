---
layout: post
title: 'Zeitgeist: Playing with Berkeley DB'
date: '2012-06-20 15:02:12'
---

While doing some scaling optimization the Zeitgeist team decided to give Berkeley DB a try. But porting from SQLite to Berkeley is not easy. However thanks to the Berkeley SQL API porting one can use the SQLite queries. All we did was change the Makefile and add a new vapi (which is a straight copy of the sqlite3.vapi but with dbsql.h as a referenced header instead of sqlite3.h).
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2012/06/timerange_interval.png"><img class="alignnone size-medium wp-image-2298" title="timerange_interval" src="http://geekyogre.com/content/images/2012/06/timerange_interval-300x50.png" alt="" width="300" height="50" /></a></p>
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2012/06/timerange_always.png"><img class="alignnone size-medium wp-image-2297" title="timerange_always" src="http://geekyogre.com/content/images/2012/06/timerange_always-300x50.png" alt="" width="300" height="50" /></a></p>
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2012/06/synapse_unlimited.png"><img class="alignnone size-medium wp-image-2296" title="synapse_unlimited" src="http://geekyogre.com/content/images/2012/06/synapse_unlimited-300x50.png" alt="" width="300" height="50" /></a></p>
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2012/06/synapse.png"><img class="alignnone size-medium wp-image-2295" title="synapse" src="http://geekyogre.com/content/images/2012/06/synapse-300x50.png" alt="" width="300" height="50" /></a></p>
<p style="text-align: center;"><a href="http://geekyogre.com/content/images/2012/06/jumplists.png"><img class="alignnone size-medium wp-image-2294" title="jumplists" src="http://geekyogre.com/content/images/2012/06/jumplists-300x112.png" alt="" width="300" height="112" /></a></p>
The results are not good though. But maybe its because we need to optimize the queries a bit more. Nevertheless you will find the code on freedesktop under the branchname berkeley tonight.

If you like a challenge, try to optimize the Berkeley optimization yourself, but be aware this is not for beginners and it may break you DB.

To build it make sure you get Berkeley db (on Debian and Ubuntu):
<ul>
	<li>sudo apt-get install libdb-sql-dev</li>
</ul>
<div>Get the latest Zeitgeist trunk code and create a new branch:</div>
<ul>
	<li>git clone <a href="git://anongit.freedesktop.org/zeitgeist/zeitgeist">git://anongit.freedesktop.org/zeitgeist/zeitgeist</a></li>
	<li>git checkout -b "testing-berkeley"</li>
</ul>
<div>Download the following <a href="http://pastebin.com/raw.php?i=Nz7suEe1">patch</a> and apply (make sure you replace path to patch):</div>
<div>
<ul>
	<li>git am --signoff &lt; /path/to/patch</li>
</ul>
Download the following <a href="http://pastebin.com/raw.php?i=U5md2vUn">vapi</a> and place it into:
<ul>
	<li>cp /path/to/vapi /usr/share/vala/vapi/dbsql.vapi</li>
</ul>
</div>
<div>Configure and compile Zeitgeist:
<ul>
	<li>sh autogen.sh --prefix=/usr/ --disable-fts &amp;&amp; make</li>
</ul>
Now run it and make sure you are NOT using the default datapath:
<ul>
	<li>ZEITGEIST_DATA_PATH=/home/seif/.local/share/zeitgeist-bdb/ src/zeitgeist-daemon --replace --log-level=debug --no-datahub</li>
</ul>
</div>
you will find a generate_events.py script in the zeitgeist tools folder as well as other benchmarking scripts. Feel free to poke around.