---
id: 778
title: 'VMware vCenter 2.5 -NOT- on SQL 2008'
date: 2009-05-09T12:49:59+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=778
permalink: /2009/05/09/vmware-vcenter-25-not-on-sql-2008/
aktt_notify_twitter:
  - yes
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
aktt_tweeted:
  - 0
views:
  - 3352
categories:
  - vCenter
tags:
  - database
  - sql
  - upgrade
  - vcenter
---
I had a situation this past week where a customer was attempting to upgrade their vCenter 2.5 U3 install to U4 and during the installer (just after where it asks for the DSN, Username and Password) it would error saying that it cannot connect.  This is where I come in.

After looking at their VMINST.LOG on the vCenter server, I see the following;

<p style="padding-left: 30px;">
  VMware VirtualCenter-build-147658: 05/05/09 22:15:25 Error returned while checking the Virtual Center database for jobs. This could be because the installer could not connect to the database pointed to by the DSN, or due to insufficient privileges to query the database.
</p>

This does not tell me very much, but the most common problem with this error is that the user they&#8217;re attempting to connect as does not have db\_owner rights on MSDB (needed only during install and upgrade).  So, I ask them to give the user db\_owner privilege and we try again.   No luck,  same exact error.

After a few hours of clicking, searching and twittering I ask them what version of SQL they are running &#8211; come to find out they have recently upgraded their SQL Server from 2005 to 2008 &#8212; BINGO!

Microsoft SQL 2008 is not supported in vCenter 2.5, however it will be supported in vCenter 4.0 &#8211; so I tell the customer they can either wait until 4.0 comes out to do the upgrade, or they will need to revert the 2008 database back to 2005&#8230;.which is a lot easier said than done.

Biggest Takeaway from this experience&#8230; VM Administrators need to work closely with their DBAs, do not allow upgrades of any part of the Virtual Eco-System that may take it out of support!  Also, check the Compatibility lists before doing any such upgrade.