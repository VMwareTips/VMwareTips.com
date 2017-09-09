---
id: 974
title: 'vCenter Chargeback Uninstallation &#8211; Rogue Plug-in'
date: 2009-08-21T15:11:44+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=974
permalink: /2009/08/21/vcenter-chargeback-uninstallation-rogue-plug-in/
redirect_from: /wp/2009/08/21/vcenter-chargeback-uninstallation-rogue-plug-in/
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
  - "4341"
dsq_thread_id:
  - "5156592333"
categories:
  - vCenter
  - vSphere
tags:
  - vcenter chargeback
  - vsphere plug-in
---
Doing a proof of concept of VMware vCenter Chargeback, install and usage went great and product does everything you&#8217;d expect it to do. Although I&#8217;d would&#8217;ve liked to seen tighter integration with the vSphere Client, hopefully we can see this in the 1.5 or 2.0 release!

<a rel="attachment wp-att-975" href="http://vmwaretips.com/wp/wp-content/uploads/2009/08/vwcb-plugin.png"><img class="alignright size-medium wp-image-975" style="border: 1px solid black; margin: 3px;" title="chargeback-plugin" src="http://vmwaretips.com/wp/wp-content/uploads/2009/08/vwcb-plugin-300x137.png" alt="" width="300" height="137" srcset="http://vmwaretips.com/wp/wp-content/uploads/2009/08/vwcb-plugin-300x137.png 300w, http://vmwaretips.com/wp/wp-content/uploads/2009/08/vwcb-plugin.png 944w" sizes="(max-width: 300px) 100vw, 300px" /></a>Well, POC was finished and time to uninstall.  Should be pretty easy, Delete from Disk the Virtual Appliance you installed and delete the database. However, if you forget one crucial step you&#8217;ll end up with a rogue plug-in in your vSphere Client!

Oh No! The vCenter Chargeback plug-in is still there! What do we do?!

<a rel="attachment wp-att-976" href="http://vmwaretips.com/wp/wp-content/uploads/2009/08/vwcb-info.png"><img class="alignleft size-medium wp-image-976" style="border: 1px solid black; margin: 3px;" title="chargeback-info" src="http://vmwaretips.com/wp/wp-content/uploads/2009/08/vwcb-info-262x300.png" alt="" width="262" height="300" srcset="http://vmwaretips.com/wp/wp-content/uploads/2009/08/vwcb-info-262x300.png 262w, http://vmwaretips.com/wp/wp-content/uploads/2009/08/vwcb-info.png 442w" sizes="(max-width: 262px) 100vw, 262px" /></a>Well, the step you need to do prior to removing the Virtual Appliance is to uncheck the _Register As VI Client Plugin_ box in the vCenter Server settings screen (Settings->vCenter Servers->Edit).  Once you do this, the plug-in will be removed from the vCenter server and you can continue with the removal of the Virtual Appilance and back-end database.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

_*click on photos to enlarge_