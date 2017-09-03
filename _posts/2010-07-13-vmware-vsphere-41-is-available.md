---
id: 1206
title: VMware vSphere 4.1 is Available!
date: 2010-07-13T00:46:55+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1206
permalink: /2010/07/13/vmware-vsphere-41-is-available/
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
  - "2658"
categories:
  - vCenter
  - vSphere
tags:
  - esx
  - esxi
  - upgrade
  - vcenter
  - VMware
  - vsphere
---
Just about an hour ago VMware lifted the NDA on VMware vSphere 4.1 and made available all of the information on this latest release as well as the bits for download available to the public.

I will be covering a more in-depth review on this latest release really soon but I did want my readers to know that the bits are available for download from the VMware website.

<a href="http://downloads.vmware.com/d/info/datacenter_downloads/vmware_vsphere_4/4" target="_blank">http://downloads.vmware.com/d/info/datacenter_downloads/vmware_vsphere_4/4</a>

The upgrade to ESX(i) 4.1 should be relatively easy by using traditional update methods such as VMware Update Manager (VUM).  However, the upgrade to vCenter Server 4.1 is more of a migration since it will only support a full 64-bit environment. Still don&#8217;t fret, a vCenter server migration is pretty simple just make sure you have a FULL backup of your vCenter Server database.

Also a little FYI&#8230;.rumor has it that this will be the final build containing a full ESX install (Service Console). Today might be a good day to start planning that migration to ESXi.