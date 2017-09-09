---
id: 656
title: VMware ESX 3.5 Update 4 Released
date: 2009-03-30T23:58:02+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=656
permalink: /2009/03/30/vmware-esx-35-update-4-released/
redirect_from: /wp/2009/03/30/vmware-esx-35-update-4-released/
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
  - "11107"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
tags:
  - esx
  - esxi
  - patch
  - update
  - vcenter
---
<span style="color: #000000;">VMware has released the latest update to its ESX(i) 3.5 flagship product, <em>Update 4</em>.  It is strongly recommended that you upgrade to <a href="http://vmwaretips.com/wp/2009/02/27/vmware-vcenter-25-u4-released/">VMware vCenter 2.5 Update 4</a> prior to upgrading your ESX hosts.  Updates such as this one typically include a number of system improvements and also all of the patches available in-between it and the previous update available. </span><span style="color: #000000;">Numerous driver additions and updates have been added to this update roll-up, including;</span>



  * **<span style="color: #000000;">Expanded Support for Enhanced vmxnet Adapter</span>**
  * **<span style="color: #000000;">Enablement of Intel Xeon Processor 5500 Series</span>**
  * **<span style="color: #000000;">QLogic Fibre Channel Adapter Driver Update</span>**
  * **<span style="color: #000000;">Emulex Fibre Channel Adapter Driver Update</span>**
  * **<span style="color: #000000;">LSI megaraid_sas and mptscsi Storage Controller Driver Update</span>**
  * **<span style="color: #000000;">Newly Supported Guest Operating Systems</span>** 
      * <span style="color: #000000;">SUSE Linux Enterprise Server 11</span>
      * <span style="color: #000000;">SUSE Linux Enterprise Desktop 11</span>
      * <span style="color: #000000;">Ubuntu 8.10 Desktop and Server Editions</span>
      * <span style="color: #000000;">Windows Preinstallation Environment 2.0</span>
  * **<span style="color: #000000;">Newly Supported Management Agents</span>**
  * **<span style="color: #000000;">Newly Supported I/O Devices</span>** 
      * <span style="color: #000000;"><strong>SAS Controllers and SATA Controllers</strong></span> 
          * <span style="color: #000000;">PMC 8011 (for SAS and SATA drives)</span>
          * <span style="color: #000000;">Intel ICH9 </span>
          * <span style="color: #000000;">Intel ICH10 </span>
          * <span style="color: #000000;">CERC 6/I SATA/SAS Integrated RAID Controller (for SAS and SATA drivers) </span>
          * <span style="color: #000000;">HP Smart Array P700m Controller</span>
      * <span style="color: #000000;"><strong>Network Cards</strong></span> 
          * HP NC375i Integrated Quad Port Multifunction Gigabit Server Adapter
          * HP NC362i Integrated Dual port Gigabit Server Adapter
          * Intel 82598EB 10 Gigabit AT Network Connection
          * HP NC360m Dual 1 Gigabit/NC364m Quad 1 Gigabit
          * Intel Gigabit CT Desktop Adapter
          * Intel 82574L Gigabit Network Connection
          * Intel 10 Gigabit XF SR Dual Port Server Adapter
          * Intel 10 Gigabit XF SR Server Adapter
          * Intel 10 Gigabit XF LR Server Adapter
          * Intel 10 Gigabit CX4 Dual Port Server Adapter
          * Intel 10 Gigabit AF DA Dual Port Server Adapter
          * Intel 10 Gigabit AT Server Adapter
          * Intel 82598EB 10 Gigabit AT CX4 Network Connection
          * NetXtreme BCM5722 Gigabit Ethernet
          * NetXtreme BCM5755 Gigabit Ethernet
          * NetXtreme BCM5755M Gigabit Ethernet
          * NetXtreme BCM5756 Gigabit Ethernet
      * **Onboard Management Processors** 
          * IBM system management processor (iBMC)
      * **Storage Arrays** 
          * SUN StorageTek 2530 SAS Array
          * Sun Storage 6580 Array
          * Sun Storage 6780 Array

 I wanted to just give you a high-level overview of the updates in this release, all of the gory details can be found in the <a href="http://www.vmware.com/support/vi3/doc/vi3_esx35u4_rel_notes.html" target="_blank">full release notes</a>.