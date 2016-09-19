---
id: 457
title: HP MSA1500 Ruined My Customers Week
date: 2009-01-09T22:46:31+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=457
permalink: /2009/01/09/hp-msa1500-ruined-my-customers-week/
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
  - 10902
dsq_thread_id:
  - 5156589694
categories:
  - Storage
tags:
  - errors
  - esx
  - fibre
  - hp
  - msa1500
  - reservation
  - scsi
  - Storage
---
A customer of mine with a small ESX deployment ran into some major grief this week with their MSA1500.  Unfortunately for them, it took 3 days for them to pick up the phone and get hold of me. This isn&#8217;t the first time I&#8217;ve ran into a problem caused by an MSA1500, and it will not be the last.  Symptoms start out minimal, VMs appear to be running slow&#8230;systems unresponsive&#8230;then BOOM all out catastrophic failure!

<!--more-->

The problem is that the controller built into the MSA1500, it just was not made to support any throughput.  The sweet spot for these devices is 2 ESX hosts and a handful of Virtual Machines (0-15), anything more than that and you&#8217;ll be asking for trouble.

Here is some of the errors you should be expecting in your vmkernel and vmkwarning logs;

<p style="padding-left: 30px;">
  <em>Jan  9 22:13:13 groucho vmkernel: 0:01:32:55.713 cpu0:1146)Fil3: 9811: Max Timeout retries exceeded for caller 0x928f4b (status &#8216;Timeout&#8217;)<br /> Jan  9 22:13:13 groucho vmkernel: 0:01:32:55.713 cpu1:1087)VSCSI: 2803: Reset request on handle 8195 (0 outstanding commands)<br /> Jan  9 22:13:13 groucho vmkernel: 0:01:32:55.713 cpu1:1054)VSCSI: 3019: Resetting handle 8195 [0/0]<br /> Jan  9 12:15:25 groucho vmkernel: 2:18:31:13.494 cpu1:1037)WARNING: FS3: 4784: Reservation error: Timeout<br /> Jan  9 21:28:16 groucho vmkernel: 0:00:47:59.406 cpu1:1033)VSCSI: 2803: Reset request on handle 8192 (1 outstanding commands)<br /> Jan  9 21:28:16 groucho vmkernel: 0:00:47:59.406 cpu1:1054)VSCSI: 3019: Resetting handle 8192 [0/0]<br /> Jan  9 12:15:25 groucho vmkernel: 2:18:31:13.494 cpu1:1037)WARNING: FS3: 4784: Reservation error: Timeout<br /> Jan  9 15:36:08 groucho vmkernel: 2:21:51:56.008 cpu0:1034)VSCSI: 2803: Reset request on handle 8208 (3 outstanding commands)<br /> Jan  9 15:36:08 groucho vmkernel: 2:21:51:56.008 cpu1:1054)VSCSI: 3019: Resetting handle 8208 [0/0]<br /> Jan  9 20:40:49 groucho vmkernel: 0:00:00:02.483 cpu0:1024)CpuSched: 16758: Reset scheduler statistics<br /> Jan  9 20:40:50 groucho vmkernel: 0:00:00:10.004 cpu1:1035)World: vm 1064: 895: Starting world FS3ResMgr with flags 1<br /> Jan  8 07:58:05 groucho vmkernel: 1:14:13:57.304 cpu0:1034)VSCSI: 2803: Reset request on handle 8201 (1 outstanding commands)<br /> Jan  8 07:58:05 groucho vmkernel: 1:14:13:57.305 cpu1:1054)VSCSI: 3019: Resetting handle 8201 [0/0]</em>
</p>

So, what happens is the controller in the MSA simply chokes and slows everything down to a screeching halt. This of course does not play well with ESX.  The only way to resolve was to remote into each VM and shutdown, luckily SOME of them responded to the VMware Tools guest shutdown&#8230;only two out of the 14 needed to be forcefully killed (kill -9 <VMPID>).  After everything was down we shutdown the ESX hosts.  Then we proceeded to shutdown and restart the MSA (controller -> shelves -> shelves -> controller).  Once back online we powered on only 2 of the 3 ESX hosts, I do not want to create too much contention on the MSA and luckily those two hosts will still run all their VMs without a problem.  Next week sometime we will be migrating to an EVA they have laying around.

So, in the end what did we learn?   MSA = Good for Test and Labs &#8230; BAD for Production