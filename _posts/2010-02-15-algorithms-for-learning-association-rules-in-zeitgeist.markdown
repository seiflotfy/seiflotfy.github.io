---
layout: post
title: Algorithms for learning association rules in Zeitgeist
date: '2010-02-15 04:33:27'
---

With the framework being in a stable form now and <a href="http://eurion.net">Siegfrieds</a> work on a "dataprovider register" (he will blog about it soon i hope) I decided to take a stab at something new that has not really been used on the desktop before except in GNOME-Do.
However what we are doing is a bit more complicated.
With Zeitgeist knowing about your activities and events i tried to apply the classic "A Priori" Algorithm to detect associated files based on usage.
Unlike our current implementation of finding files related to other  explicit given files. This one looks at a whole timerange and creates sets of files used together. It is kind of like detecting usage patterns.

Taken from wikipedia here is a little example:

<blockquote>A large supermarket tracks sales data by SKU (item), and thus is able to know what items are typically purchased together. Apriori is a moderately efficient way to build a list of frequent purchased item pairs from this data. Let the database of transactions consist of the sets {1,2,3,4}, {2,3,4}, {2,3}, {1,2,4}, {1,2,3,4}, and {2,4}. Each number corresponds to a product such as "butter" or "water". The first step of Apriori to count up the frequencies, called the supports, of each member item separately:
Item	Support
1      | 3
2      | 6
3      | 4
4      | 5
We can define a minimum support level to qualify as "frequent," which depends on the context. For this case, let min support = 3. Therefore, all are frequent. The next step is to generate a list of all 2-pairs of the frequent items. Had any of the above items not been frequent, they wouldn't have been included as a possible member of possible 2-item pairs. In this way, Apriori prunes the tree of all possible sets..
Item	Support
{1,2} | 3
{1,3} | 2
{1,4} | 3
{2,3} | 4
{2,4} | 5
{3,4} | 3
This is counting up the occurrences of each of those pairs in the database. Since minsup=3, we don't need to generate 3-sets involving {1,3}. This is due to the fact that since they're not frequent, no supersets of them can possibly be frequent. Keep going:
Item	Support
{1,2,4} | 3
{2,3,4} | 3
<strong>
In much larger datasets, especially those with huge numbers of items present in low quantities and small numbers of items present in large quantities, the gains made by pruning the possible pairs tree like this can be very large</strong>.</blockquote>

Now imagine the supermarket being all files on ur computer and the transactions being sets of events happening to the files per 30 minutes.

Using this we will be able to determine alot of cool associations between files and with some <a href="http://codethink.co.uk">Tracker</a> magic we could do this on a metadata level.

Now i pushed the implementation with this test case and another into a branch waiting for the team to review it and expose it properly over D-Bus. The test cases work though which kinda gets me excited to work on new algorithms and generate adaptive transaction since right now i assume every 30 minutes is a transaction. I have a lot of ideas and also I will be applying two other algorithms <strong>Winepi and Minepi</strong> to compare results.

Expect some cool stuff to come up soon...
Releases of the engine and GAJ are being prepared...
Cheers