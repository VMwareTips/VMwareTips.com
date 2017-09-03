---
id: 1441
title: 'vSphere 5 Video Series &#8211; Install vCenter 5.0 in Around 5 Minutes'
date: 2011-10-13T01:30:55+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1441
permalink: /2011/10/13/vsphere-5-video-series-install-vcenter-50-in-around-5-minutes/
ratings_users:
  - "4"
ratings_score:
  - "20"
ratings_average:
  - "5"
views:
  - "2480"
dsq_thread_id:
  - "5156598255"
categories:
  - vCenter
  - vSphere
tags:
  - auto deploy
  - composer
  - db2
  - drs
  - esx
  - esxi
  - ha
  - heartbeat
  - image builder
  - installation
  - linked-mode
  - oracle
  - sql
  - update manager
  - vcenter
  - vCSA
  - vdi
  - video
  - view
  - vsa
  - vsphere 4
  - vsphere 5
  - vsphere storage appliance
---
In this video we&#8217;re going to cover the installation, configuration and usage of the VMware vCenter 5.0 Server Appliance (vCSA). The vCSA is a brand new production ready Virtual Appliance that allows you to stand up vCenter Server in literally a few minutes. Once you watch the video you&#8217;re going to be like, &#8220;_Hey Rick, that was more than 5 minutes!&#8221;_.  For that I do apologize, but when you do watch it you will realize we&#8217;re doing a lot more than just installing vCenter 5.0.

First a little disclaimer. vCSA is not for everyone, but in my opinion it should definitely be looked at and should be leveraged wherever it can. vCSA is obviously the direction of where the vCenter Server product is going and hopefully relatively soon it should be at par with its Windows based big brother.

So, why isn&#8217;t it for everyone?

As of right now it does not have support for integration with VMware Update Manager (VUM), VMware vCenter Linked-Mode, VMware vSphere Storage Appliance (vSA), VMware vCenter Heartbeat and VMware View Composer. Another concern you may have is that it&#8217;s embedded database option (based on DB2) is limited to 5 Hosts and 50 Virtual Machines. Think of the embedded option to be similar to the SQL Express Option in vCenter Server for Windows, great for POC, Demo, Test and extremely small SMB situations, but not practical for production. The final nail in the coffin might be that it only supports Oracle to offer external DB functionality.

Some of those constraints are not going to be avoidable, for example if you require more than 1,000 hosts or 10,000 powered on virtual machines you&#8217;re obviously going to need Linked-Mode and the Windows based vCenter Server. If you&#8217;re looking to deploy a VDI solution based on VMware View, you&#8217;re going to need the Windows based vCenter Server as well. But, if you&#8217;re like the majority of VMware vSphere customers, have less than 1,000 hosts, are confident in VMware DRS and HA to protect your vCSA and are OK with the fact that you need Oracle for the external database (which you can <a href="http://www.vmware.com/support/policies/oracle-support.html" target="_blank">virtualize</a> as well)&#8230;.the vCSA **<span style="text-decoration: underline;">might</span>** be for you!

One last thing I wanted to comment on was VMware Update Manager, in my opinion the lack of VUM support for the vCSA might not be that big of an issue, and here&#8217;s why; With the introduction of vSphere 5.0, VMware also introduced a few new features, Auto Deploy and Image Builder. These features tied together with Host Profiles truly enable the concept of stateless ESXi. My thought is, if you need to update your ESXi host, simply update the Auto Deploy rule and reboot the machine. Upon the next boot it will automatically be updated and configured properly.  Obviously VUM does a lot more than just ESXi patching, but again, for the majority of vSphere customers they&#8217;d be just fine with Auto Deploy.

So have a view of this video to see just how easy it is. I have sped up some portions of the video, specifically the loading of the vSphere Client as well as the deployment of the vCSA OVF template. Also, I suggest watching the video in full-screen mode by clicking the icon on the bottom right of the video. If for whatever reason the video isn’t displaying, you can also use the following link to view; <a href="http://youtu.be/o2f1b1vYSis" target="_blank">http://youtu.be/o2f1b1vYSis</a>