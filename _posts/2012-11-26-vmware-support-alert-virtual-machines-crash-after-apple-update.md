---
id: 1851
title: 'VMware Support Alert &#8211; Virtual Machines crash after Apple Update'
date: 2012-11-26T09:33:13+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1851
permalink: /2012/11/26/vmware-support-alert-virtual-machines-crash-after-apple-update/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1562"
dsq_thread_id:
  - "5156597910"
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

<img class="alignleft" style="margin: 0px 25px 5px 0px; border: 0px;" title="VMware Support Alert" src="http://blogs.vmware.com/tp/.a/6a00d8341c328153ef01543330c84d970c-pi" alt="VMware Support Alert" width="86" height="86" border="0" />

Recently Apple released an update for 2012 Macs named **MacBook Air and MacBook Pro Update 2.0**. The update includes graphics performance and reliability enhancements. It has been discovered that once users update to the latest release of MacBook Pro Update 2.0, there is breakage in the host display driver causing virtual machines to crash while using certain 3D applications. VMware engineering team is currently investigating this issue.

VMware Fusion users should refrain from applying this update.

VMware Fusion users who have already applied this update and are affected by this issue can work-around it by disabling the **Accelerate 3D Graphics** option under Virtual Machine > Settings > Display.

For further information, updates, and resolution to this issue, refer to KB article: <a href="http://kb.vmware.com/kb/2040249" target="_blank">Virtual machines fail while using 3D applications after applying Apple MacBook Air and MacBook Pro Update 2.0 (2040249)</a>.