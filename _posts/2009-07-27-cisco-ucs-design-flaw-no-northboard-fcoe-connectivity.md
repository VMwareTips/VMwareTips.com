---
id: 935
title: Cisco UCS Design Flaw? No Northboard FCoE Connectivity
date: 2009-07-27T13:28:46+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=935
permalink: /2009/07/27/cisco-ucs-design-flaw-no-northboard-fcoe-connectivity/
redirect_from: /wp/2009/07/27/cisco-ucs-design-flaw-no-northboard-fcoe-connectivity/
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
  - "7198"
dsq_thread_id:
  - "5156595522"
categories:
  - Good Reading
  - Storage
tags:
  - cisco
  - fcoe
  - nexus
  - ucs
---
Today <a href="http://blog.scottlowe.org/2009/07/27/potential-ucs-issue-northbound-fcoe-connectivity/#comment-45247" target="_blank">Scott Lowe</a> wrote a post on his blog explaining how Cisco UCS lacks Northbound FCoE connectivity, explained here;

> I’m about halfway through the first day of Unified Computing System (UCS) training in San Jose, CA, and I’ve learned of what I think is a fairly significant limitation. The issue centers around what Cisco refers to as “northbound” traffic and how Fibre Channel over Ethernet (FCoE) is handled with northbound traffic.
> 
> Recall that a central part of UCS is the UCS 6100 series fabric interconnect. The 6100 series fabric interconnect has connectivity in two directions:
> 
>   * _Southbound_ connectivity is connectivity aimed back at the fabric extenders in the blade chassis themselves.
>   * _Northbound_ connectivity is connectivity headed outside the UCS to other systems and networks.
> 
> All southbound traffic is 10Gbps Ethernet with FCoE. Northbound traffic can be 10Gbps Ethernet or Fibre Channel, _but not FCoE_. Based on the information I’ve been given (and if I’m incorrect please let me know in the comments), you **cannot directly connect an FCoE-enabled storage array to a UCS**. Even if your storage array has native FCoE interfaces, you can’t plug them into the UCS 6100 series fabric interconnects because that’s considered northbound traffic and you can’t use FCoE with northbound traffic.
> 
> I have a feeling customers who have purchased storage arrays with FCoE interfaces with the intention of hooking the arrays up directly to a UCS are going to be a bit upset when this information becomes more widely known.
> 
> If I’m working from incorrect or incomplete information, please feel free to speak up in the comments.

At first I was extremely shocked to hear this, this is pretty big news and I would be upset as a customer if I wasn&#8217;t able to directly attach my FCoE-enabled storage array directly to the UCS Fabric Interconnect.

After doing some research of my own I found the following;

<!--more-->

> <p class="pSubhead2CMT" style="font-size: 9pt; font-style: normal; font-variant: normal; font-weight: bold; margin-left: 0pt; margin-right: 0pt; text-align: left; text-decoration: none; text-indent: 0pt; text-transform: none;">
>   Expansion Module Options for Cisco UCS 6100 Series Fabric Interconnects
> </p>
> 
> <div class="pBodyCMT" style="margin: 0pt 0pt 7pt; font-style: normal; font-variant: normal; font-weight: normal; text-align: left; text-decoration: none; text-indent: 0pt; text-transform: none;">
>   The Cisco UCS 6100 Series is equipped to support a number of expansion module options (Figure 4).
> </div>
> 
> <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
>   • Ethernet module that provides 6 ports of 10 Gigabit Ethernet using the SFP+ interface
> </p>
> 
> <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
>   • Fibre Channel plus Ethernet module that provides 4 ports of 10 Gigabit Ethernet using the SFP+ interface; and 4 ports of 1/2/4-Gbps native Fibre Channel connectivity using the SFP interface
> </p>
> 
> <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
>   • Fibre Channel module that provides 8 ports of 1/2/4-Gbps native Fibre Channel using the SFP interface for transparent connectivity with existing Fibre Channel networks
> </p>

<p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
  So, no FCoE support on those expansion modules which is surprising.. however, it could be by design. I wouldn&#8217;t necessary want to attach my SAN directly to the fabric interconnect, but with the addition of a Nexus 5000 I could push FCoE direct to the Fabric Interconnect, thus avoiding unnecessary fibre connections.   I do find it funny though that the Nexus 5000 has full FCoE support (Northbound and Southbound), look at their expansion module offerings;
</p>

<p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
  <blockquote>
    <p class="pSubhead1CMT" style="font-size: 10pt; font-style: normal; font-variant: normal; font-weight: bold; margin-left: 0pt; margin-right: 0pt; text-align: left; text-decoration: none; text-indent: 0pt; text-transform: none;">
      Expansion Module Options for the Cisco Nexus 5000 Series
    </p>
    
    <div class="pBodyCMT" style="margin: 0pt 0pt 7pt; font-style: normal; font-variant: normal; font-weight: normal; text-align: left; text-decoration: none; text-indent: 0pt; text-transform: none;">
      The Cisco Nexus 5000 Series is equipped to support expansion modules that can be used to increase the number of 10 Gigabit Ethernet/FCoE ports or connect to Fibre Channel SANs with 4/2/1-Gbps Fibre Channel switch ports, or both. The Cisco Nexus 5010 supports one expansion module, and the Cisco Nexus 5020 supports any combination of two modules from the following offerings (Figure 4):
    </div>
    
    <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
      • Ethernet module that provides 6 10 Gigabit Ethernet/FCoE ports using the SFP+ interface
    </p>
    
    <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
      • Fibre Channel plus Ethernet module that provides 4 10 Gigabit Ethernet/FCoE ports using the SFP+ interface, and 4 ports of 4/2/1-Gbps native Fibre Channel connectivity using the SFP interface
    </p>
    
    <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
      • ·Fibre Channel module that provides 8 ports of 4/2/1-Gbps native Fibre Channel using the SFP interface for transparent connectivity with existing Fibre Channel networks
    </p>
  </blockquote>
  
  <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
    Hopefully someone from Cisco can explain why UCS was designed this way, feel free to comment on my blog or on <a href="http://blog.scottlowe.org/2009/07/27/potential-ucs-issue-northbound-fcoe-connectivity/#comment-45247" target="_blank">Scott Lowe</a>&#8216;s.
  </p>
  
  <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
    <strong>UPDATE: </strong>A lot of chatter has been going on in Twitter and on Scott&#8217;s post. It sounds like FCoE will be supported in UCS with a future software upgrade.  Also interestingly enough, you cannot directly attach a FC device into the Fabric Interconnect. UCS operates all FC functions in NPIV mode, not FC switch mode. This means you need to uplink to a fibre channel switch, like an MDS (or N5K).  Check out <a href="http://blog.scottlowe.org/2009/07/27/potential-ucs-issue-northbound-fcoe-connectivity/" target="_blank">Scott&#8217;s post</a> for all the comments.
  </p>
  
  <p class="pBulletCMT" style="font-style: normal; font-variant: normal; font-weight: normal; margin-bottom: 3pt; margin-right: 0pt; margin-top: 0pt; text-decoration: none; text-transform: none;">
    <strong>UPDATE 01/10/2011:</strong> With UCS Manager v1.4 now released supports direct attached storage, including direct FC connected storage, direct Ethernet connected storage (iSCSI/NFS) as well as FCoE connected storage. Dave Alexander has a great write-up on his <a href="http://www.unifiedcomputingblog.com/?p=187" target="_blank">blog</a>. Steve Chambers also has a great write-up on his <a href="http://viewyonder.com/2010/12/20/ciscoucs-1-4-is-here/" target="_blank">blog</a> reviewing all of the great new updates in UCSM 1.4. One thing that I&#8217;m disappointed to not see yet is northbound FCoE support, don&#8217;t get me wrong having direct connect storage is amazing but say you have multiple UCS domains within a single datacenter, you&#8217;ll still need to connect dedicated IP and SAN fabrics to each Fabric Interconnect.
  </p>