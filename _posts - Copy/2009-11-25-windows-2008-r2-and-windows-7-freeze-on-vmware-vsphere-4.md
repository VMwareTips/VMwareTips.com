---
id: 1083
title: Windows 2008 R2 and Windows 7 Freeze on VMware vSphere 4
date: 2009-11-25T10:45:29+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1083
permalink: /2009/11/25/windows-2008-r2-and-windows-7-freeze-on-vmware-vsphere-4/
redirect_from: /wp/2009/11/25/windows-2008-r2-and-windows-7-freeze-on-vmware-vsphere-4/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "1"
ratings_score:
  - "3"
ratings_average:
  - "3"
aktt_tweeted:
  - "1"
views:
  - "19949"
dsq_thread_id:
  - "5156594885"
categories:
  - vSphere
tags:
  - freeze
  - vsphere 4
  - windows 2008 R2
  - windows 7
---
Although this issue has been resolved with vSphere 4 U1, for those of you that haven&#8217;t upgraded please be aware of a known issue with Windows 2008 R2 and Windows 7 where the guest operating system can freeze for a long period of time.  The issue is noted in <a href="http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1011709" target="_blank">VMware KB 1011709.</a>

The resolution is to either upgrade to U1 or to use the standard SVGA driver and not the one provided in the VMware Tools package.

> **VMware KB 1011709 Excerpt&#8230;**
> 
> To deselect the SVGA drivers installed with VMware Tools:
> 
> When you install VMware Tools, select VMware Tools Custom Install and deselect the SVGA driver.
> 
> Alternatively, remove the SVGA driver from the Device Manager after installing VMware Tools.