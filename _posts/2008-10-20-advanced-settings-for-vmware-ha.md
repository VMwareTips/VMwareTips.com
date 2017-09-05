---
id: 125
title: Advanced Settings for VMware HA
date: 2008-10-20T16:24:15+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=125
permalink: /2008/10/20/advanced-settings-for-vmware-ha/
redirect_from: /wp/2008/10/20/advanced-settings-for-vmware-ha/
views:
  - "31653"
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
dsq_thread_id:
  - "5156596784"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - VMware
  - VMware HA
tags:
  - aam
  - esx
  - vmwareHA
---
<span style="color: #888888;"><span style="color: #888888;">After discussing the issue(s) about NFS.LockDisable and how those problems may be generated (ie: VMware HA initiation), a few comments came in about VMware HA and how the default settings may not fit their specific needs.</span></span>

<span style="color: #888888;"><!--more--></span>

<span style="color: #888888;"><span style="color: #888888;">Well, here are some Advanced Settings that you can change from within your Cluster.</span></span>

<p style="padding-left: 30px;">
  <span style="color: #888888;"><strong><span style="color: #888888;">das.AllowNetwork</span></strong><strong><span style="color: #888888;"> </span><span style="font-weight: normal;"><span style="color: #888888;">By default the Service Console portgroup is used for failure detection. By entering in </span><em><span style="color: #888888;">das.AllowNetwork</span></em><span style="color: #888888;"> you can specify an additional portgroup to use.</span></span></strong></span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #888888;"><strong><span style="color: #888888;">das.isolationAddress</span></strong><strong><span style="color: #888888;"> </span><span style="font-weight: normal;"><span style="color: #888888;">By default VMware HA nodes check heartbeats of other nodes . When this heartbeat is lost the suspected Isolated nodes then pings its Service Console gateway by default to check that it is truly isolated. By using the </span><em><span style="color: #888888;">das.isolationAddress</span></em><span style="color: #888888;"> command, you can add additional IP addresses for the server to check. These IPs must be on the Service Console portgroup, or in the portgroup you&#8217;ve added for </span><em><span style="color: #888888;">das.AllowNetwork</span></em></span></strong></span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #888888;"><strong><span style="color: #888888;">das.failureDetectionTime<br /> </span> <span style="font-weight: normal;"><span style="color: #888888;">This is the time required before VMware HA considers a host to be Isolated.</span></span></strong><strong><span style="color: #888888;"> </span><span style="font-weight: normal;"><span style="color: #888888;">Default setting is 14 seconds, this can be changed to a setting that will better fit your needs.</span></span></strong></span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #888888;"><strong><span style="font-weight: normal;"><strong><span style="color: #888888;">das.failureDetectionInterval<br /> </span> <span style="font-weight: normal;"><span style="color: #888888;">This is the rate of monitoring between VMware HA nodes, think of this as a heartbeat check.</span></span><span style="color: #888888;"><br /> </span> <span style="font-weight: normal;"><span style="color: #888888;">Default setting is 1 second, if you feel that this is just too often you can change it.</span></span></strong></span></strong></span>
</p>

<span style="color: #888888;"><span style="color: #888888;">VMware HA events are captured in the vpxa.log file on each VMware ESX host. DasHostIsolatedEvent is the syntax left in the log file when an Isolation happens.</span></span>

<span style="color: #888888;"><span style="color: #888888;">If you&#8217;re having problems with configuring VMware HA, you can check the /var/log/vmware/aam/aam_config_util_*.log files. These logs include all your necessary information for installing, configuring and connecting to other HA nodes.</span></span>

<span style="color: #888888;"><span style="color: #888888;">If it comes down to it, you can remove the HA software from the ESX node by doing the following;</span></span>

<p style="padding-left: 30px;">
  <span style="color: #888888;"><span style="color: #888888;">[root@dpcrc_vmdevsap1 aam]# </span><strong><span style="color: #888888;">rpm -qa |grep aam<br /> </span> </strong><span style="color: #888888;">VMware-aam-haa-2.2.0-1 <<< should be listed if installed<br /> VMware-aam-vcint-2.2.0-1 <<< should be listed if installed<br /> [root@dpcrc_vmdevsap1 aam]# </span><strong><span style="color: #888888;">rpm -e VMware-aam-haa-2.2.0-1 VMware-aam-vcint-2.2.0-1</span></strong></span>
</p>

<span style="color: #888888;"><span style="color: #888888;">This will do a clean uninstall of the VMware HA software, you can then Reconfigure for VMware HA from within VirtualCenter.</span></span>

<span style="color: #888888;">Also, Duncan Epping over at yellow-bricks.com has a complete listing of Advanced VMware HA settings, you can check those out at <a href="http://www.yellow-bricks.com/2008/10/06/update-ha-advanced-options-2/" target="_blank">http://www.yellow-bricks.com/2008/10/06/update-ha-advanced-options-2/</a></span>