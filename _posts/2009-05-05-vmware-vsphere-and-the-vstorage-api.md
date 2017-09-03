---
id: 773
title: VMware vSphere and the vStorage API
date: 2009-05-05T09:26:25+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=773
permalink: /2009/05/05/vmware-vsphere-and-the-vstorage-api/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
aktt_tweeted:
  - "1"
views:
  - "9576"
dsq_thread_id:
  - "5156595987"
categories:
  - NetApp
  - Storage
  - vSphere
tags:
  - NetApp
  - vmware data recovery
  - vmware view
  - vsphere
  - vstorage
---
During my trip to Palo Alto for the VMware vSphere Launch I met with some NetApp engineers at their Executive Briefing Center in Sunnyvale.  This was perhaps one of my favorite meetings while in the Bay Area that week.

There are going to be a lot of exciting things coming with the GA release of vSphere, one of the biggest in my opinion will be with vStorage API&#8217;s, which will allow vSphere to offload tasks to the storage subsystem.

I was told by NetApp that in vSphere when you initiate a Clone of a Virtual Machine or Deploy from Template, this process will be sent to your FAS system to process, rather than it happening at the ESX host level as it traditionally was done.

Other things that will be sent to the storage system include De-Duplication (if your storage supports it), commands sent by VMware Data Recovery and also automated provisioning in VMware View can be offloaded.  For VMware View, NetApp provided the example of their <a href="http://blogs.netapp.com/virtualization/2009/01/rapid-cloning-u.html" target="_blank">Rapid Cloning Utility</a> and how it already integrates with the VI Client &#8211; the new release will be a lot more streamlined since it will use vStorage API calls.

So, what does all of this mean?  It shows that VMware is working close with the hardware vendors to truly build a Virtual Eco-System, and it shows a lot of exciting new potential that vSphere will bring. Pushing storage related processes back to the storage subsystem will not only increase the speed of these transactions, but it will also relieve a lot of CPU and I/O from the ESX hosts.