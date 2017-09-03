---
id: 775
title: 'VMware ESX 3.5, Patch ESX350-200904401-BG: Updates vmkernel vmx hostd etc'
date: 2009-05-05T19:43:39+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=775
permalink: /2009/05/05/vmware-esx-35-patch-esx350-200904401-bg-updates-vmkernel-vmx-hostd-etc/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "1"
ratings_score:
  - "5"
ratings_average:
  - "5"
aktt_tweeted:
  - "1"
views:
  - "3934"
dsq_thread_id:
  - "5156595978"
categories:
  - ESX 3.5 Tips
tags:
  - esx
  - patch
---
VMware recently released a patch, ESX350-200904401-BG which resolves a number of issues, which can be found in <a href="http://kb.vmware.com/kb/1010126" target="_blank">KB1010126</a>.

The biggest fix that has affected me lately is, &#8220;Fixes an issue where an unsuccessful online consolidation might cause a virtual machine to fail and become unusable because of a CID mismatch.&#8221;

I recently ran into some problems with some virtual machines that have high I/O failing during the commit of a snapshot, I discussed this in an earlier post which can be found <a href="http://vmwaretips.com/wp/2009/04/14/committing-snapshots-generates-a-content-id-mismatch-error/" target="_blank">here</a>.

I&#8217;d highly recommend anyone running ESX 3.5 to apply this update as it resolves a lot of known issues that can affect VM performance and stability.  Always remember to follow proper patching procedures, thoroughly test the patch install and verify before placing production Virtual Machines back on the host.