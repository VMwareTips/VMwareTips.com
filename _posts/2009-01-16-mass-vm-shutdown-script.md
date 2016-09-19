---
id: 478
title: Mass VM Shutdown Script
date: 2009-01-16T14:05:32+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=478
permalink: /2009/01/16/mass-vm-shutdown-script/
aktt_notify_twitter:
  - yes
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
aktt_tweeted:
  - 1
views:
  - 16238
dsq_thread_id:
  - 5156589852
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
tags:
  - maintenance
  - mass shutdown
  - powershell
  - script
  - ssh
---
Well, if you haven&#8217;t already figured out I&#8217;m big on shell scripts and Unix/Linux in general, so when my company informed me that they needed to bring down one of our NetApp FAS clusters for system maintenance, the wheels in my head started turning.  I&#8217;m sorry this isn&#8217;t in our beloved Powershell scripting language, but I&#8217;m old school and needed to write a shell based script to gracefully shutdown all my virtual machines.

<!--more-->

I know there are other ways to do this, but I really don&#8217;t want to wake up at 3AM on Sunday to do it.  So below is my shell script, which I&#8217;ve scheduled in cron on one of my ESX 3.5 hosts.

<p style="padding-left: 30px;">
  <span style="color: #ff0000;">#!/bin/sh -x<br /> <span style="color: #3366ff;"># set path and date</span><br /> DATE=`date +%m.%d.%G.%H%M`<br /> PATH=$PATH:/bin:/usr/bin:/usr/sbin</span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #ff0000;">date<br /> echo &#8220;Attempting graceful shutdown of Virtual Machines on host dpcrc-vmdevsap1&#8230;&#8221;</span><br /> <span style="color: #3366ff;"># start for loop to grab VMIDs then send power.shutdown requests using vim 3 seconds apart</span><br /> <span style="color: #ff0000;">for i in `vmware-vim-cmd vmsvc/getallvms | sed &#8216;1d&#8217; | awk &#8216;{print $1}&#8217;`<br /> do<br /> vmware-vim-cmd vmsvc/power.shutdown $i<br /> sleep 3<br /> done<br /> echo &#8220;Successfully sent shutdown sequence to Virtual Machines on host dpcrc-vmdevsap1&#8221;</span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #ff0000;">date<br /> echo &#8220;Attempting graceful shutdown of Virtual Machines on host dpcrc-vmdevsap2&#8230;&#8221;</span><br /> <span style="color: #3366ff;"># in this for loop I&#8217;m connecting via ssh to my other esx host(s), you can multiply this for<br /> # as many hosts as you have.  I have 8 I need to do but I&#8217;m leaving them out for simplicity<br /> # in the blog.  Please remember to have your other ESX hosts ssh keys in the authorized key file<br /> # of the host your starting the script from</span><br /> <span style="color: #ff0000;">for i in `ssh dpcrc-vmdevsap2 vmware-vim-cmd vmsvc/getallvms | sed &#8216;1d&#8217; | awk &#8216;{print $1}&#8217;`<br /> do<br /> ssh dpcrc-vmdevsap2 vmware-vim-cmd vmsvc/power.shutdown $i<br /> sleep 3<br /> done<br /> echo &#8220;Successfully sent shutdown sequence to Virtual Machines on host dpcrc-vmdevsap2&#8221;</span>
</p>

Here is the cron so you can see exactly when I&#8217;m running this;

<p style="padding-left: 30px;">
  <span style="color: #ff0000;">50 3 18 1 0 /usr/sbin/massvmshutdown > /var/log/massvmshutdown 2>&1</span>
</p>

As you can see, I&#8217;m running this at 03:50 on 1/18 and the 0 day of the week (Sunday).  I did this so just in case if I forget to remove it from the cron, it will not run again until 1/18 falls on a Sunday (2015). Also I am outputting std out to a log file so I can review it after.

One big thing that this script would require is the ability to SSH from one ESX host to another, without be prompted for a password.  I covered how to do this in another blog post, <a href="http://vmwaretips.com/wp/2009/01/16/ssh-from-esx-host-to-esx-host-with-no-password/" target="_blank">which can be found here.</a>