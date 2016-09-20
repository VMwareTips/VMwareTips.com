---
id: 527
title: 'ESX Patches &#8211; Resolve SAN LUN Issue'
date: 2009-02-02T16:53:05+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=527
permalink: /2009/02/02/esx-patches-resolve-san-lun-issue/
aktt_notify_twitter:
  - yes
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
aktt_tweeted:
  - 1
views:
  - 4263
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Storage
tags:
  - esx
  - esxi
  - patch
---
In a previous <a href="http://vmwaretips.com/wp/2009/01/12/issue-vmware-esxesxi-san-io-failure/" target="_blank">article</a> I discuss how an ESX host can halt if LUN metadata updates are done the same time a LUN path fails.  Thankfully VMware has released a patch for this problem, along with a few others.  I strongly suggest you to upgrade if your running VMware ESX 3.5 U3 and block level storage.

<!--more-->

  * ESX350-200901401-SG &#8211; PATCH &#8211; Security &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006651" target="new">KB 1006651</a> &#8211; Updates VMkernel VMX hostd. But most important fix that this patch contains definitely is: <!--Eng PR 356915, KB 1008130-->VMware ESX and ESXi 3.5 U3 I/O failure on SAN LUNs, and LUN queue is blocked indefinitely. For a full description of this issue, see 
    
    <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1008130" target="_blank">http://kb.vmware.com/kb/1008130</a>.
  * ESX350-200901402-SG &#8211; PATCH &#8211; Security &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006652" target="new">KB 1006652</a> &#8211; Security Update to ESX Scripts
  * ESX350-200901404-BG &#8211; PATCH &#8211; Critical &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006654" target="new">KB 1006654</a> &#8211; Updates VMware Tools
  * ESX350-200901405-BG &#8211; PATCH &#8211; General &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006655" target="new">KB 1006655</a> &#8211; Updates VMware-esx-lnxcfg
  * ESX350-200901406-BG &#8211; PATCH &#8211; General &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006656" target="new">KB 1006656</a> &#8211; Updates Kernel Source and VMNIX
  * ESX350-200901407-BG &#8211; PATCH &#8211; General &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006657" target="new">KB 1006657</a> &#8211; Updates Pegasus
  * ESX350-200901408-BG &#8211; PATCH &#8211; Critical &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006658" target="new">KB 1006658</a> &#8211; Updates SATA Drivers
  * ESX350-200901409-SG &#8211; PATCH &#8211; Security &#8211;<a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006659" target="new">KB 1006659</a> &#8211; SNMP Security Update
  * ESX350-200901410-SG &#8211; PATCH &#8211; Security &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006660" target="new">KB 1006660</a> &#8211; Security Update for libxml2

There’s one “patch” released for ESXi (installable and embedded) 3.5:

  * ESXe350-200901401-O-SG &#8211; PATCH &#8211; Security &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006661" target="new">KB 1006661</a> &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1006662" target="new">KB 1006662</a> &#8211; <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/kb/1007058" target="new">KB 1007058</a> &#8211; Firmware Update
  
    If you are using SRM in combination with ESX be sure to read the <a href="http://kb.vmware.com/kb/1006661" target="_blank">KB1006661</a> cause this patch contains several fixes related to SRM.

There’s also a whole bunch of 3.0.x patches released, so if you’re still running 3.0.x be sure to look into these new patches.

Thanks to <a href="http://www.yellow-bricks.com/2009/01/31/patches-for-35/" target="_blank">Duncan</a> where I grabbed the above table.