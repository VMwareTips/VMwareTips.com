---
id: 2003
title: 'VMware Support Alert &#8211; VMware ALERT: PowerPath/VE 5.7 fails to load on VMware vSphere version 5.1'
date: 2013-03-18T10:13:07+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2003
permalink: /2013/03/18/vmware-support-alert-vmware-alert-powerpathve-5-7-fails-to-load-on-vmware-vsphere-version-5-1/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1025"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
In our effort to provide our viewers with up to the minute information on VMware related news and topics, we&#8217;re posting the following Special Alert direct from VMware Support Insider.

 <img class="asset asset-image at-xid-6a00d8341c328153ef01543330c84d970c alignleft" style="border: 0px; margin: 5px;" title="Alert" src="http://blogs.vmware.com/tp/.a/6a00d8341c328153ef01543330c84d970c-800wi" alt="Alert" width="86" height="86" border="0" />VMware has become aware of an issue where PowerPath/VE 5.7 fails to load on VMware vSphere version 5.1

VMware and EMC have identified 2 issues in vSphere 5.1 that affect customers with PowerPath/VE.

  1. Provisioning failed. View admin UI showed “Configuration failure: Cannot open the disk
  2. PowerPath Persistent settings in /etc/vmware/esx.conf are not persisted across upgrade and reboot

VMware and EMC have identified a fix for this issue. For customers using PowerPath/VE, VMware recommends not upgrading to vSphere 5.1 until EMC has released PowerPath/VE 5.7 P02 and VMware has released a patch.

For updates and the more information on this issue, refer to Knowledgebase article:
  
<a href="http://kb.vmware.com/kb/2034796" target="_blank">PowerPath/VE 5.7 fails to load on VMware vSphere version 5.1 (2034796)</a>.

&nbsp;