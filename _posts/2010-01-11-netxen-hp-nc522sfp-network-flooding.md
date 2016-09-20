---
id: 1141
title: NetXen HP NC522SFP Network Flooding
date: 2010-01-11T18:49:25+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1141
permalink: /2010/01/11/netxen-hp-nc522sfp-network-flooding/
aktt_notify_twitter:
  - yes
ratings_users:
  - 2
ratings_score:
  - 8
ratings_average:
  - 4
aktt_tweeted:
  - 1
views:
  - 20248
dsq_thread_id:
  - 5156594677
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Networking
  - Storage
  - vSphere
tags:
  - 4.0.516
  - Bug
  - Bug 496013
  - esx
  - esxi
  - firmware
  - NC522SFP
  - network flood
  - NetXen
  - spanning tree
---
I had a very fun weekend. It started at 4am Saturday with a migration of ~125 virtual machines from an old AMD based environment to a new Intel Nehalem based environment. Who could&#8217;ve known that within a few hours all hell would&#8217;ve broken loose.

Enter in problem of network flooding from the NetXen based HP branded NC522SFP.  Because all of the 10GbE ports from the (9) new ESXi servers were creating thousands of pause frames on the Cisco Nexus 5020 switches, I thought originally that it was an issue on the switch.  Talks with Cisco revealed nothing.  We attempted to disconnect one of the connected ports (each ESXi host is dual connected into a pair of N5Ks using vPC) to remove a potential spanning tree loop&#8230;.no dice.

A reboot of the host resolved the problem, things appeared to be running normally and we decided to let it be and wait until Monday.

10 hours goes by, it is now Sunday morning and the problem returns.  First host loses storage (we&#8217;re doing NFS over 10GbE here), then two more&#8230;until all 9 in this cluster are pretty much toast.  I decide to open a ticket with VMware.  Wouldn&#8217;t you know, there is a potential known bug and resolution.

> <span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;"><strong>Bug 496013<br /> </strong></span><span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;"><br /> Description: Some NetXen based 10GbE cards using the unm_nic and nx_nic drivers sometime flood the network with pause frames causing the port to become disabled.</span>
> 
> <span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">Resolution: NetXen believes upgrading the firmware to version 4.0.516 will resolve the problem.</span>

<span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">I&#8217;ve gone ahead and patched 4 of the hosts with this new firmware, so far it has been stable (knock on wood).   I&#8217;ll let you know if something happens.</span>

<span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">Checking which version of the firmware you&#8217;re running is simple. From a command-line (ESX or ESXi hidden CLI), type ethtool -i <vmnic#> (replace vmnic# with the alias to the vmnic you&#8217;d like to check).  You should see output similar to:</span>

<p class="MsoNormal" style="margin: 0in 0in 0pt;">
  <span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">driver: nx_nic</span>
</p>

<p class="MsoNormal" style="margin: 0in 0in 0pt;">
  <span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">version: 4.0.301</span>
</p>

<p class="MsoNormal" style="margin: 0in 0in 0pt;">
  <span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">firmware-version: 4.0.406</span>
</p>

<p class="MsoNormal" style="margin: 0in 0in 0pt;">
  <span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">bus-info: 0000:07:00.0</span>
</p>

<p class="MsoNormal" style="margin: 0in 0in 0pt;">
  <p class="MsoNormal" style="margin: 0in 0in 0pt;">
    <p class="MsoNormal" style="margin: 0in 0in 0pt;">
      <strong><span style="color: #ff0000;">Update &#8211; Utility CD with firmware patch now included&#8230;<br /> </span></strong>
    </p>
    
    <p class="MsoNormal" style="margin: 0in 0in 0pt;">
      <span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">As you can see above, the firmware is out of date. To update the firmware you will need to boot from a Linux utility CD that has the appropriate driver, you then run a firmware update utility provided by HP.  To make this process easy I have created a bootable SLAX utility CD with the drivers pre-loaded. You can download the ISO from here (file temporarily removed). Once booted run the installer located in the root filesystem (ie: ./CP011471.scexe).</span>
    </p>
    
    <p class="MsoNormal" style="margin: 0in 0in 0pt;">
      <p class="MsoNormal" style="margin: 0in 0in 0pt;">
        <span style="font-size: 10pt; font-family: &quot;Arial&quot;,&quot;sans-serif&quot;;">Let me know if you have any questions.</span>
      </p>