---
id: 369
title: 'ESXi Free Edition &#038; The RCLI'
date: 2008-12-15T16:15:06+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=369
permalink: /2008/12/15/esxi-u3-allows-full-administration-via-rcli/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 3751
categories:
  - ESXi 3.5 Tips
  - VMware
tags:
  - esx
  - esxi
  - management
  - rcli
  - VMware
---
Well a few days back there were a lot of posts in regards to the Free Edition of ESXi and how in U3 the RCLI is now writable.  This unfortunately was a bug, per Duncan over at <a href="http://www.yellow-bricks.com/2008/12/16/update-free-esxi-and-the-rcli/" target="_blank">Yellow-Bricks</a> this was done unintentionally by the ESXi programmers attempting to resolve an API-related bug.   So, enjoy the writable RCLI while it last Free ESXi users, your next update will most likely remove the feature.

This only applies to customers who downloaded the free version of ESXi. VirtualCenter and VI (Foundation, Standard, Enterprise) customers are not affected.

For those of you that do not know what the RCLI is, here is an except from VMware;

**VMware Infrastructure Remote CLI**
  
The VMware Infrastructure Remote CLI provides a command-line interface for datacenter management from a remote server.