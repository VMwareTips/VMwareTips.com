---
id: 1233
title: 'Advisory &#8211; ESX 4.1 + HP FLEX-10 + Broadcom bnx2x = Bad News'
date: 2010-11-11T13:39:50+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1233
permalink: /2010/11/11/advisory-esx-41-hp-flex-10-broadcom-bnx2x-bad-news/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 6441
dsq_thread_id:
  - 5156594291
categories:
  - Networking
  - vSphere
tags:
  - beacon probing
  - bnx2x
  - broadcom
  - dcc
  - esx 4.1
  - flex-10
  - hp
  - virtual connect
---
Two local customers have ran into the same situation in the past month&#8230;.both are running on a HP c-Class blade infrastructure leveraging Virtual Connect/FLEX-10 as well as on-board Broadcom 10G cards leveraging the bnx2x driver &#8211; this mixed with ESX(i) 4.1 is an almost lethal combination.

Random network drops, port flapping, dropped packets&#8230;.not good for a virtual infrastructure. Luckily HP is aware of the issue and has released <a href="http://h20000.www2.hp.com/bizsupport/TechSupport/Document.jsp?objectID=c02476622" target="_blank">Advisory <span class="goog_qs-tidbit goog_qs-tidbit-0">c02476622</span></a> which states;

> <p style="margin-top: 0px; margin-bottom: 2ex;">
>   The Broadcom bnx2x VMware ESX Driver Version 1.54 does not function with HP Virtual Connect Device Control Channel (DCC) and SmartLink features on ProLiant and Integrity server blades configured with the NC532m or the NC532i adapter running firmware version 2.2.6. After installing or upgrading VMware ESX/ESXi 4.1 the following functionality is either not installed or is lost:
> </p>
> 
> <div class="para" style="margin-top: 0px; margin-bottom: 2ex;">
>   <ol style="list-style-type: decimal;">
>     <li>
>       New installation &#8211; DCC and SmartLink functionality is unavailable in an HP Virtual Connect environment with the NC532m or NC532i Network Adapters after installing VMware ESX/ESXi 4.1.
>     </li>
>     <li>
>       Upgrade installation &#8211; If the bnx2x Asynchronous Driver Update CD version 1.52 was previously installed on a VMware ESX/ESXi 4.0 host, DCC/SmartLink capabilities will be lost after upgrading to VMware ESX/ESXi 4.1, which will overwrite the bnx2x driver version 1.52 with version 1.54 that is included with the base VMware ESX/ESXi 4.1operating system.
>     </li>
>     <li>
>       Network failover &#8211; ProLiant and Integrity server blades hosting VMware ESX/ESXi 4.1 may lose network failover capabilities that use the VMware ESX NIC teaming failover policy (vSwitch setting) &#8220;Link Status only.&#8221;
>     </li>
>   </ol>
> </div>

There is a work-around that leverages VMware Beacon Probing but honestly this has been a hit/miss type work-around.  In my opinion, stick with ESX 4.0 until HP works out the issue with the firmware/driver.