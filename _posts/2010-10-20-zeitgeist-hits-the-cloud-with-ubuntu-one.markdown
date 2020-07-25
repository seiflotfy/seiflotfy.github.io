---
layout: post
title: Zeitgeist hits the Cloud with Ubuntu One
date: '2010-10-20 21:36:54'
---

I love me a challenge. Today with the help of his awesomeness <a href="http://kryogenix.org/days/">Stuart Langridge</a> (from the Ubuntu One team) we hacked together a little Zeitgeist extension for all cloud lovers.

In short it allows you to have all your events on the cloud to sync them between computers. Not only that but you can actually access the desktop couch DB instead of the Zeitgeist DB for simple querying.

There is a lot of potential for Events being stored on a cloud and having devices synced (Who did I chat with on my netbook can be answered over on your desktop). <a href="http://kryogenix.org/days/2010/10/20/storing-zeitgeist-data-in-desktopcouch">Stuart wrote a nice post about the adventure. Check it out.</a>

<strong>Zeitgeist does not depend on Desktop Couch so no worries. It is an external process triggered by a Zeitgeist extension that monitors Zeitgeist activities and pushes them into Desktop Couch.</strong>