---
id: 1102
title: Strange vCenter 4.0 U1 and ESXi 4.0 U1 SSL Issue
date: 2009-12-09T08:56:52+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=1102
permalink: /2009/12/09/strange-vcenter-40-u1-and-esxi-40-u1-ssl-issue/
redirect_from: /wp/2009/12/09/strange-vcenter-40-u1-and-esxi-40-u1-ssl-issue/
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
  - "4338"
dsq_thread_id:
  - "5156594782"
categories:
  - vSphere
tags:
  - error
  - esx
  - esxi
  - ssl
  - troubleshooting
  - vcenter
---
Last week I came across a problem that really stumped me, it even stumped the Tier-1 and Tier-2 support at VMware.  I&#8217;m posting the symptoms on here in a hope that someone else has experienced this issue and can share some light.

How about a little background on the environment, vCenter Server 4.0 U1 and multiple ESX(i) hosts (3.5, 4.0, 4.0 U1).   The vCenter Server as well as a number of ESXi 4.0 hosts were upgraded to U1 a couple days after it was released,  this problem however happened ~8 days after the upgrade.

**Symptom 1**: All ESX(i) hosts disconnect from vCenter Server, however, they are still online and no VMs went down.  Within 15 minutes all hosts appear to be reconnected.

**Symptom 2**: After the hosts reconnect, the ESX hosts appear to be functioning normally. However, the ESXi hosts display an error on the Overview tab as well as in the Events tab; &#8220;Unable to Synchronize with host that is unavailable.&#8221;

**Symptom 3**: Random VMotions start, for no apparent reason (DRS engaged, yet no constraints causing DRS to be invoked).  However, these VMotions fail at 10% due to the fact that the source and destination host is not available.

**Symptom 4**: /var/log/messages file displays errors with keywords: [VpxdVmomi] Error getting vpxa info: SSL Exception: Unexpected EOF From hosts, blacklisting showing up.   &#8212; I apologize for paraphrasing.

So, all this starts happening and I start investigating&#8230;.pulling logs, restarting vCenter, and just sit there stumped.  I did notice that the rui.crt on the vCenter server expired, but back in 2008.  I went ahead and renewed the certificate and even restarted the entire vCenter server.  No luck.  I engaged VMware Support and their Tier-1 and Tier-2 support were stumped,  nothing even showed up in their internal database on this issue.

Then it all disappeared.  Roughly 90 minutes after it started, the problem just went away and everything was good.

Have you seen this issue?  What were your troubleshooting steps?  Did you resolve it or figure out the resolution?