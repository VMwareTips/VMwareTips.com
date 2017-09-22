---
id: 2036
title: 'VMware Support Alert &#8211; ALERT: Login issue after updating to vCenter 5.1 Update 1'
date: 2013-04-29T05:57:08+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2036
permalink: /2013/04/29/vmware-support-alert-alert-login-issue-after-updating-to-vcenter-5-1-update-1/
redirect_from: /wp/2013/04/29/vmware-support-alert-alert-login-issue-after-updating-to-vcenter-5-1-update-1/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "966"
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

<img class="asset asset-image at-xid-6a00d8341c328153ef01543330c84d970c alignleft" style="margin: 0px 25px 5px 0px; border: 0px;" title="VMware Support Alert" src="http://blogs.vmware.com/tp/.a/6a00d8341c328153ef01543330c84d970c-800wi" alt="VMware Support Alert" width="86" height="86" border="0" />

VMware has become aware of an issue that may occur after upgrading to vCenter Server 5.1 Update 1.

Specifically:

  * You are unable to log in using the vSphere Web Client or domain username/password credentials via the vSphere Client.

This issue can occur if the specified vCenter Server login domain user account is associated with a large number of domain groups and multiple domains are configured as SSO identity sources. The precise number of groups at which this issue can occur varies due to the nature of Active Directory internals. However, it is more likely to occur once domain-group membership for an account exceeds 19.

<span style="color: #ff0000;">Customers with SSO configured with multiple domain-based identity sources along with vCenter Server domain user accounts that are associated with a large number of groups should not upgrade to vCenter Server 5.1 Update 1.</span>

We urge you to read the official KB article for more details and/or updates:
  
<a href="http://kb.vmware.com/kb/2050941" target="_blank">Cannot log in to vCenter Server using the domain username/password credentials via the vSphere Web Client/vSphere Client after upgrading to vCenter Server 5.1 Update 1 (2050941)</a>.

<img src="http://feeds.feedburner.com/~r/SupportInsiderAlerts/~4/3XIFYtAcFLM" alt="" width="1" height="1" />

&nbsp;