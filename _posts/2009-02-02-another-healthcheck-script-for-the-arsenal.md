---
id: 522
title: Another HealthCheck script for the Arsenal
date: 2009-02-02T16:37:01+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=522
permalink: /2009/02/02/another-healthcheck-script-for-the-arsenal/
redirect_from: /wp/2009/02/02/another-healthcheck-script-for-the-arsenal/
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
  - "3174"
dsq_thread_id:
  - "5156590162"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
tags:
  - healthcheck
  - perl toolkit
  - powershell
  - script
  - vima
---
In the VTMN Communities, William Lam, created a new HealthCheck script that I will be definietely adding to my HealthCheck Arsenal.  More information on the script and its usage can be found in the <a href="http://communities.vmware.com/docs/DOC-9420" target="_blank">VTMN Communities</a> posting.

The script reports on the following:

  * **vCenter Build/Release**
  * **ESX/ESXi Build/Release**
  * **Cluster(s) Name/Statistics (Hosts,CPU and MEM availabity, HA,DRS and DPM enabled)**
  * **ESX/ESXi Hardware configuration (NICs/HBAs)**
  * **ESX/ESXi State**
  * **ESX/ESXi Config (WIP)**
  * **ESX/ESXi Datastore summary**
  * **Virtual Machines summary**
  * **VM Storage summary**
  * **VM Network summary**
  * **VM w/Snapshots**
  * **VM w/RDMs**
  * **VM w/NPIV enabled**
  * **VM w/connected CD-ROMs**
  * **VM w/connected Floppys**

For more details, please take a look at the sample report located at <a href="http://engineering.ucsb.edu/%7Eduonglt/vmware/sample_health_report.html" target="_blank">here</a><span class="jive-link-external">. </span>The requirements for this script are: vCenter 2.5, ESX(i) 3.5, VI-Perl Toolkit or VIMA.

Just like <a href="http://www.yellow-bricks.com/2009/02/01/new-vmware-healthcheck-script/" target="_blank">Duncan</a> states, this script can be compared to the <a href="http://www.ivobeerens.nl/?p=256" target="_blank">PowerShell HealthCheck</a> scripts and the <a onclick="javascript:pageTracker._trackPageview('/outbound/article/sourceforge.net');" href="http://sourceforge.net/projects/esxhealthscript/">Service Console</a> script.