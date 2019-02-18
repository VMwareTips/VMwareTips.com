---
id: 658
title: VMware Enhanced VMotion Compatibility (EVC)
date: 2009-03-31T00:13:04+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=658
permalink: /2009/03/31/vmware-enhanced-vmotion-compatibility-evc/
redirect_from: /wp/2009/03/31/vmware-enhanced-vmotion-compatibility-evc/
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
  - "21146"
dsq_thread_id:
  - "5156757026"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
tags:
  - esx
  - esxi
  - evc
  - vcenter
  - vmotion
---
I recently ran into a situation with a customer where they needed to add another host to their cluster.  Problem is, their original hosts had single core AMD Opteron processors (Opteron 285) and the host they wanted to purchase came with either a Dual-Core or Quad-Core Opteron.  The customer was scared about the VMotion Compatibility between their older AMD hosts and the newer hosts they would be purchasing&#8230;.so much that they wanted me to find them an old single-core system. I know EVC is nothing new, I&#8217;ve been enabling it when needed for almost 8 months now.  You may run into a situation where your customer (or boss) is a little hesitant in enabling this advanced feature. But rest assured, VMware has <a href="http://kb.vmware.com/kb/1003212" target="_blank">KB 1003212</a> to answer all your questions.



Well, with a little bit of convincing and by showing the customer <a href="http://kb.vmware.com/kb/1003212" target="_blank">VMware KB Article 1003212</a> I was able to enable Enhanced VMotion Compatibility (EVC) on their vCenter cluster.

There are a few things you should know about EVC. First off, it is fully supported by VMware and the CPU Manufacturers. Just as long as your running ESX 3.5 U2+ (and vCenter 2.5 U2), you can enable EVC on your cluster. This means that all CPUs on your hosts within a given cluster must be in one of the charts listed in the KB Article. As you can see, support for the new Intel Nehalem processors has been added in ESX 3.5 U4.

Also remember, VMotion is currently not possible between Intel and AMD processors, so all nodes in your cluster must be from the same manufacturer.  Exciting changes in technology are happening and hopefully we will see this limitation lifted (I thought I&#8217;d never be able to say that).

Finally, one last thing you must know about EVC &#8212; because it really does nothing more than what CPU masking has done in ESX 2+, all of the Virtual Machines in the cluster you wish to enable EVC on need to be powered off. I strongly suggest reading the <a href="http://kb.vmware.com/kb/1003212" target="_blank">KB article</a> for more information.