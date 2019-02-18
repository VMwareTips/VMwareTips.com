---
id: 326
title: Virtualizing your DMZ
date: 2008-12-05T17:46:51+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=326
permalink: /2008/12/05/virtualizing-your-dmz/
redirect_from: /wp/2008/12/05/virtualizing-your-dmz/
ratings_users:
  - "3"
ratings_score:
  - "13"
ratings_average:
  - "4.33"
views:
  - "26478"
dsq_thread_id:
  - "5156562579"
categories:
  - Networking
  - Security
  - VMware
tags:
  - dmz
  - forrester
  - gartner
  - portgroup
  - virtualizing
  - vswitch
  - vulnerability
---
Today I got into a heated discussion with a &#8220;_Virtualization Expert_&#8221; at Gartner today about the risks associated with virtualizing your DMZ, primarily into the same environment as your non-DMZ servers.

As you can see in my diagram below, this is my plan;  Create a completely isolated vSwitch with dedicated NICs for my DMZ portgroup, which is separated from the vSwitch that contains my Service Console, VMKernel and other Virtual Machine portgroup.

[singlepic id="46" w="320" h="240" mode="watermark" float="center" ]

The discussion I got into this afternoon was that this was still a security risk, and presented a vulnerability to potentially all my other Virtual Machines on the host.   Frankly, I just don&#8217;t see it.  The only risk I could potentially ever see is if one of the guests in the DMZ portgroup was compromised, it could potentially affect other systems within that vSwitch &#8212; there should be no way it could cross talk to the other portgroups on other vSwitches in this system.  Right?  The Gartner engineer kept bringing up how someone could attack that vSwitch and gain access to the system to compromise it&#8230;then he kept giving examples about how this happened in Hyper-V (which has nothing to do with ESX).

So, I&#8217;m leaving this open&#8230;what is your opinion?  Regardless of Intrusion Protection Systems and Intrusion Detection Systems and Firewalls, etc. &#8212;  How strong is a vSwitch?  Can someone that hacks a guest within an isolated vSwitch (one with no Service Console on it) gain access to your host?

Are these so-called _Experts_ at firms like Gartner and Forrester really **_Experts_**?

You tell me&#8230;.