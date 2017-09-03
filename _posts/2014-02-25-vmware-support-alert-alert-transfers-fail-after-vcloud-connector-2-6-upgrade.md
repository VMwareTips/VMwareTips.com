---
id: 2273
title: 'VMware Support Alert &#8211; ALERT: Transfers fail after vCloud Connector 2.6 upgrade'
date: 2014-02-25T12:27:08+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2273
permalink: /2014/02/25/vmware-support-alert-alert-transfers-fail-after-vcloud-connector-2-6-upgrade/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "975"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMware has become aware of an issue wherein after upgrading to vCloud Connector 2.6, a change to the permissions on the staging directory causes transfers to fail.

A newly installed vCloud Connector node has read/write/execute permissions for user, group, and other on the staging directory (777). When upgrading the node to vCloud Connector 2.6, these permissions are incorrectly set to 755. This removes the write permission for other, which in this instance references the admin user.

For details and updates on this issue refer to KB article: <a href="http://bit.ly/1etIvMj" target="_blank">Cannot access the transfer directory after upgrading to vCloud Connector 2.6 (2073208)</a>