---
id: 1898
title: 'VMware Support Alert &#8211; ALERT: Upgrading to View Agent 5.1.2 can result in performance issues'
date: 2012-12-21T06:32:34+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1898
permalink: /2012/12/21/vmware-support-alert-alert-upgrading-to-view-agent-5-1-2-can-result-in-performance-issues/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 790
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

<img class="asset asset-image at-xid-6a00d8341c328153ef01543330c84d970c alignleft" style="margin: 0px 25px 5px 0px; border: 0px;" title="VMware Support Alert" src="http://blogs.vmware.com/tp/.a/6a00d8341c328153ef01543330c84d970c-800wi" alt="VMware Support Alert" border="0" />

VMware has become aware of an issue that may occur when using a View 5.1.2 Agent on a physical machine, the View Connection Broker will repeatedly attempt to configure the agent which can cause a significant performance impact particularly in large scale environments. If you do not use VMware View to access Physical Machine based desktops, no workaround is required.

Symptoms may include:

  * In environments with multiple physical machines, significant slowdowns occur and you may see stability issues.
  * When attempting to use the View 5.1.2 Agent on a physical machine, the system slows down.

For further updates and more information on this alert, refer to KB article:
  
<a href="http://kb.vmware.com/kb/2041977" target="_blank">Performance issue when using View 5.1.2 Agent on Physical Machine based desktops (2041977)</a>.