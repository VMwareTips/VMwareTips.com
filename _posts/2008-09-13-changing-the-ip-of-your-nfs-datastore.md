---
id: 30
title: Changing the IP of your NFS Datastore
date: 2008-09-13T08:49:00+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=30
permalink: /2008/09/13/changing-the-ip-of-your-nfs-datastore/
views:
  - "23734"
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
dsq_thread_id:
  - "5156596634"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - NetApp
  - Storage
  - VMware
tags:
  - datastore
  - ip
  - nfs
  - svmotion
---
I&#8217;ve ran into some issues today trying to change the IP address of my NFS Datastore. Our filer has a nice 10GbE interface that I&#8217;m not using, so my thought was to put my hosts into Maintenance Mode one at a time, remove the old datastore and connect the new one&#8230;which is essentially the same exact mount but going over a different interface. Boy was I wrong&#8230;

<!--more-->

VMotion uses the datastore location path, not the datastore name to do it&#8217;s migrations. Basically VC thought this was a completly new datastore, even appended (1) after it. I verified this by looking at the datastores inventory and noticed they listed both, even showed that they were different paths;

datastore = netfs://0.0.0.0//vol/vol1/vm1
  
datastore (1) = netfs://1.1.1.1//vol/vol1/vm1

So, it looks like I&#8217;ll be forced to do a SVMotion on all my data to be able to use this new 10GbE interface.

I also have a ticket open with VMware, just to make sure. I&#8217;ll let you know if I find out different.

**Update** &#8212; Well if you&#8217;re looking to avoid any downtime you will be forced to use SVMotion to migrate your data to a new datastore. There are some tricks you can use depending on your storage vendor, for example with NetApp you can use flexclones then write a script to unregister and re-register your VMX files. For me, I just took a long weekend and moved everything over. I must tell you that SVMotion for NFS is NOT supported (yet), but we all know it works :)