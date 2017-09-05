---
id: 414
title: NetApp SnapManager for Virtual Infrastructure and VIBE
date: 2008-12-23T18:00:19+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=414
permalink: /2008/12/23/netapp-snapmanager-for-virtual-infrastructure-and-vibe/
redirect_from: /wp/2008/12/23/netapp-snapmanager-for-virtual-infrastructure-and-vibe/
ratings_users:
  - "1"
ratings_score:
  - "5"
ratings_average:
  - "5"
views:
  - "8751"
aktt_notify_twitter:
  - 'yes'
dsq_thread_id:
  - "5156589546"
categories:
  - 'Backup &amp; Recovery'
  - NetApp
  - Storage
tags:
  - backup
  - esx
  - NetApp
  - smvi
  - snapshot
  - vibe
---
So, I&#8217;ve already had a couple <a href="http://vmwaretips.com/wp/2008/12/05/netapp-snapshots-in-esx-take-2/" target="_blank">posts</a> including some shell scripts that I wrote that will quiesce your Virtual Machines then initiate a NetApp level snapshot.  Some have noted (including myself) how they are not the best tools for getting the job done&#8230;.mind you, they worked for me and my purpose, but they were lacking.  I&#8217;m not going to get into what they were lacking, but lets just leave it at that (definietly not a commercial product). Luckily for us, NetApp has released a new product called <a href="http://www.netapp.com/us/products/management-software/snapmanager-virtual.html" target="_blank">SnapManager for Virtual Infrastructure</a> (SMVI) which a lot of people have already discussed in the blogging world.  This is another tool of the SnapManager series which automates the snapshot process for your application, including system quiescing (VM snapshots) and also integration with SnapMirror (if your using it).  Tons of information on SMVI can be found on the links at the bottom of this blog.

OK &#8212; so lets take it a step further, say you don&#8217;t want to fork out the money for SMVI, what can you do?  Well, NetApp released on its <a href="http://now.netapp.com/NOW/download/tools/vibe/" target="_blank">NOW ToolChest</a> (support subscription required) a tool called VIBE, Virtual Infrastructure Backup Engine.

<!--more-->

VIBE is a free tool which operates exactly as SMVI, the only catch is that you do not get the pretty GUI that SMVI gives you.  VIBE is completely text based via either Perl or compiled EXE (Perl for Linux or EXE for Windows), and I&#8217;m actually running it on my vCenter server nightly at Midnight.  VIBE interacts with vCenter to grab all of your datastore and VM information and to actually kick off the VM level snapshot.  VIBE then interacts with your NetApp FAS to kick off the NetApp level snapshot and any SnapMirror syncs.

Initial configuration is a little tricky, all of the commands can be seen by running _vibe &#8211;help_. I first ran it manually from the command line, then I took all of my configuration options and put them into a config file. You can specify a config file to use by running _vibe &#8211;config <filename>_.  This makes it extremely easy to automate.

<p style="padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-help.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-help.png" alt="vibe-help.png" width="400" />&#8211; Screenshot of VIBE &#8211;help</a>
</p>

Here are some screenshots on how I am using it.  I&#8217;ve been using it for about a week now without one problem.  I must warn though, VIBE is not directly supported by NetApp, it is only supported via Professional Services.  With this said, once you get it working there should be no reason why you need support.

<p style="padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-schedule-1.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-schedule-1.png" alt="vibe-schedule-1.png" width="400" />&#8211; Here is my Scheduled Task to run my VIBE Batch Job<br /> </a>
</p>

<p style="padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-schedule-2.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-schedule-2.png" alt="vibe-schedule-2.png" width="400" />&#8211; As you can see I am running it nightly at 12:05AM<br /> </a>
</p>

<p style="padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-batch.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-batch.png" alt="vibe-batch.png" width="400" />&#8211; The Batch job is nothing more than kicking off the VIBE executable and specifying a config file to us for the settings. Also note that I am not specifying a path to VIBE, this is because the user running this task has the VIBE path in its environment</a>
</p>

<p style="padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-config.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-config.png" alt="vibe-config.png" width="400" />&#8211; Here is the config file, nothing more than the vCenter user and password, along with the NetApp FAS login and password and the datastore names I want to backup. VIBE does all the hard work in finding the volume names and VM locations</a>
</p>

<p style="padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-snaps.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vibe-snaps.png" alt="vibe-snaps.png" width="400" />&#8211; Here is my final product, FAS level snapshots complete with VM<br /> quiescing because VIBE integrates with vCenter. If you noticed the names are different it is because I changed them</a>
</p>

Alright, thats pretty much it.  Easy to implement and use, and best of all &#8211; it is FREE :)

ref: <a href="http://www.yellow-bricks.com/2008/03/11/snapshot-manager-for-vi3-netapp/" target="_blank">Yellow-Bricks.com discussion on SMVI</a>
  
ref: <a href="http://vmetc.com/2008/06/08/understanding-netapp-snapmanager-for-virtual-infrastructure/" target="_blank">VM /ETC discussion on SMVI</a>