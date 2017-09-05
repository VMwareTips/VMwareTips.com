---
id: 825
title: Upgrade VMware vCenter 2.5 to 4.0 Video
date: 2009-06-01T21:09:58+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=825
permalink: /2009/06/01/upgrade-vmware-vcenter-25-to-40-video/
redirect_from: /wp/2009/06/01/upgrade-vmware-vcenter-25-to-40-video/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "2"
ratings_score:
  - "10"
ratings_average:
  - "5"
aktt_tweeted:
  - "1"
views:
  - "14224"
dsq_thread_id:
  - "5156595815"
categories:
  - vCenter
  - vSphere
tags:
  - upgrade
  - vcenter
  - video
  - vsphere
---
During an upgrade of vCenter 2.5 to 4.0 at a customer site I decided it would be a good idea to record the steps required.  In this video you will see how to upgrade VMware vCenter 2.5 to vCenter 4.0 that uses a Microsoft SQL database.  The steps are trivial and I have done more than a handful of these on customers production servers.

The most important thing is to follow the best practices, give your ODBC user db_owner privledge on the MSDB and vCenter database prior to any install or upgrade &#8211; then remove the privledge after the installer is complete.  Also make sure that IIS or any other webserver is disabled.

<p style="text-align: center;">
  <a href="http://vmwaretips.com/presentations/vc4upgrade/" target="_blank"><img class="size-full wp-image-847 aligncenter" src="http://vmwaretips.com/wp/wp-content/uploads/2009/06/upgrade_vcenter_ad.png" alt="" width="360" height="277" srcset="http://vmwaretips.com/wp/wp-content/uploads/2009/06/upgrade_vcenter_ad.png 360w, http://vmwaretips.com/wp/wp-content/uploads/2009/06/upgrade_vcenter_ad-300x230.png 300w" sizes="(max-width: 360px) 100vw, 360px" /></a>
</p>