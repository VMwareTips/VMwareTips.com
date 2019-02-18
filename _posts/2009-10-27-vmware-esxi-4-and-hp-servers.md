---
id: 1063
title: VMware ESXi 4 and HP Servers
date: 2009-10-27T13:21:12+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=1063
permalink: /2009/10/27/vmware-esxi-4-and-hp-servers/
redirect_from: /wp/2009/10/27/vmware-esxi-4-and-hp-servers/
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
  - "13385"
dsq_thread_id:
  - "5156594977"
categories:
  - Storage
  - vSphere
tags:
  - cim
  - esxi
  - hp
  - sd card
  - usb flash
---
I&#8217;m proud to say that HP has full support for ESXi 4 installed on SD or USB Flash memory.  They even offer the installable ISO pre-built with their CIM providers, <a href="https://h20392.www2.hp.com/portal/swdepot/displayProductInfo.do?productNumber=HPVM06" target="_blank">available here</a>. There is a catch though, they only support their approved SD or USB Flash memory&#8230;.sorry, but you cannot BYOF (Bring Your Own Flash).  This is reflected on their <a href="https://h20392.www2.hp.com/portal/swdepot/displayProductInfo.do?productNumber=HPVM06" target="_blank">download page</a>:

> **<span style="font-size: x-small; font-family: Arial;">HP VMware ESXi 4.0 solution requires the following: </span>**
> 
> ****
> 
>   * VMware ESXi 4.0 free downloadable product. To upgrade your license to Enterprise Plus, purchase HP VMware ESXi 4 product 571979-B21.
>   * HP ESXi 4 CIM Providers.
>   * Registration on VMware ESXi hypervisor web page to obtain permanent license serial number.
>   * Acquire your choice of HP supported and qualified media &#8211; any HP supported hard drive, USB or SD Flash devices listed below.
> <span style="font-size: x-small; font-family: Arial;">Please note that all devices will need to be imaged for ESXi 4.0.</span>
> 
> **Information about HP supported SD card and USB Flash drive:** 
> 
> <ul type="disc">
>   <span style="font-size: x-small; font-family: Arial;"></p> 
>   
>   <li>
>     <strong><span style="text-decoration: underline;">Supported SD card**:</span></strong><br /> HP 4GB SD Flash Media<br /> HP Part Number 580387-B21<br /> [spare kit part number 583306-001]
>   </li>
>   <li>
>     <strong><span style="text-decoration: underline;">Supported USB Flash Drive**: </span></strong><br /> HP 4GB USB Flash Media Drive Key<br /> HP Part Number 580385-B21<br /> [Spare kit part number 583307-001]
>   </li>
>   <p>
>     </span></ul> 
>     
>     <ul>
>       <span style="font-size: x-small; font-family: Arial;"><em>*Must be purchased separately.<br /> **<strong>HP VMware ESXi 4.0 does not support any other USB or SD flash devices</strong></em><br /> </span>
>     </ul></blockquote> 
>     
>     <p>
>       Seems simple, doesn&#8217;t it?   Actually it works great and I have put a few dozen servers into production with this method, the best part is no more local HDD which saves even more power!
>     </p>
>     
>     <p>
>       One question I often get is,  why do you need a 4GB drive, I though ESXi was only 32MB?  Well, even though it is true that ESXi is only 32MB you still need adequate space for the VI Client, VMware Tools (all Operating systems) and upgrade space (for future ESXi patches and releases).  Using a 4GB drive ensures that you&#8217;ll have enough space for everything.
>     </p>
>     
>     <p>
>       There is one problem currently that I am facing, HP has both the SD Card and USB Flash Drive on back-order and there is no expected ETA for either of them!  This has delayed a major project I&#8217;m working on and I&#8217;ve had to resort to using temporary &#8220;junk&#8221; USB drives to get the customer by in the mean time.
>     </p>
>     
>     <p>
>       If someone from HP is reading this, PLEASE get your OEM to produce some new ones ASAP!
>     </p>