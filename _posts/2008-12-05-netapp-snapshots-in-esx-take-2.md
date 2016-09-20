---
id: 321
title: 'NetApp Snapshots in ESX &#8211; Take 2'
date: 2008-12-05T11:36:24+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=321
permalink: /2008/12/05/netapp-snapshots-in-esx-take-2/
ratings_users:
  - 2
ratings_score:
  - 8
ratings_average:
  - 4
views:
  - 13083
dsq_thread_id:
  - 5156597430
categories:
  - 'Backup &amp; Recovery'
  - ESX 3.5 Tips
  - NetApp
  - Storage
  - VMware
tags:
  - backup
  - esx
  - NetApp
  - script
  - snapshot
  - VMware
---
Alright, well I finally set aside some time to sit and think about my [script that runs my snapshots](http://vmwaretips.com/wp/2008/09/12/netapp-snapshots-in-esx/) (VMware Snapshots then NetApp Snapshots then remove VMware Snapshot).   The problem with my current script is that if you have multiple VMware Snapshots they all get removed&#8230; which IMO maybe isn&#8217;t a bad thing (since your not suppose to keep snapshots for that long), but I can see in some environments it may not be a good thing.

<!--more-->

So, thanks to a comment posted by Hajo Ehlers (no website or email address left), he made me think about using the VCB utilities built into ESX to remove a specific snapshot.  What is nice about the VCB utility is that you can get a SsId (Snapshot ID) for each snapshot created on the VM.  So after grabbing this SsId you can remove your snapshot with that ID (rather than removing all of them).

Here is the new script, as you can see the creation portion of the snapshot is the same.  I attempted to use the vcbSnapshot utility to create these, but I found on my SUSE 10 guests they would fail (pre-freeze script failure).  I&#8217;m not having this problem with the vim-cmd utility, so I will stick with it.

One thing you must know is that you can either pass the username and password for the VCB utility from the command-line or you can just put it in the <span style="text-decoration: underline;">/etc/vmware/backuptools.conf</span> file. Also, just like with the original script I am assuming you have set up SSH authorized keys for your ESX hosts and your NetApp filer.

<p style="padding-left: 30px;">
  <span style="color: #0000ff;">#!/bin/sh -x<br /> <em><strong> #set path and date</strong></em><br /> DATE=`date +%m.%d.%G.%H%M`<br /> PATH=$PATH:/bin:/usr/bin</span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #0000ff;">echo &#8220;Creating VMware Snapshots&#8221;<br /> <em><strong>#create local host snapshot</strong></em><br /> for i in `vmware-vim-cmd vmsvc/getallvms | sed &#8216;1d&#8217; | awk &#8216;{print $1}&#8217;`<br /> do<br /> vmware-vim-cmd vmsvc/snapshot.create $i Nightly Netapp.Snapshot.$DATE<br /> done</span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #0000ff;"><em><strong>#create remote host snapshot</strong></em><br /> for i in `ssh </span><span style="color: #0000ff;"><esx-host></span><span style="color: #0000ff;"> vmware-vim-cmd vmsvc/getallvms | sed &#8216;1d&#8217; | awk &#8216;{print $1}&#8217;`<br /> do<br /> ssh <esx-host> vmware-vim-cmd vmsvc/snapshot.create $i Nightly Netapp.Snapshot.$DATE<br /> done</span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #0000ff;"><em><strong>#this schedule is ran nightly so effectively I have 8 days work of nightly backups</strong></em><br /> echo &#8220;Creating NetApp snapshots&#8221;<br /> ssh <netapp-host> snap delete vol154 vmsnap.9<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap rename vol154 vmsnap.8 vmsnap.9<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap rename vol154 vmsnap.7 vmsnap.8<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap rename vol154 vmsnap.6 vmsnap.7<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap rename vol154 vmsnap.5 vmsnap.6<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap rename vol154 vmsnap.4 vmsnap.5<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap rename vol154 vmsnap.3 vmsnap.4<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap rename vol154 vmsnap.2 vmsnap.3<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap rename vol154 vmsnap.1 vmsnap.2<br /> ssh </span><span style="color: #0000ff;"><netapp-host></span><span style="color: #0000ff;"> snap create vol154 vmsnap.1<br /> </span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #0000ff;">echo &#8220;Removing VMware Snapshots&#8221;<br /> <em><strong>#REMOVE SNAPS FROM LOCAL HOST</strong></em><br /> for i in `vcbVmName -h localhost -s Any:* | grep moref`<br /> <strong><em>#the above command grabs the MoRef ID for each Virtual Machine</em></strong><br /> do<br /> for p in `vcbSnapshot -h localhost -f $i Nightly |grep SsId`<br /> <strong><em>#the above command grabs the SsId for each snapshot named Nightly on every Virtual Machine</em></strong><br /> do<br /> vcbSnapshot -h localhost -d $i $p<br /> <strong><em>#the above command removes the SsId from the MoRef ID</em></strong><br /> done<br /> done</span>
</p>

<p style="padding-left: 30px;">
  <span style="color: #0000ff;"><em><strong>#REMOVE SNAPS FROM REMOTE HOST</strong></em><br /> for i in `ssh <esx-server> vcbVmName -h localhost -s Any:* | grep moref`<br /> do<br /> for p in `ssh </span><span style="color: #0000ff;"><esx-server></span><span style="color: #0000ff;"> vcbSnapshot -h localhost -f $i Nightly |grep SsId`<br /> do<br /> ssh </span><span style="color: #0000ff;"><esx-server></span><span style="color: #0000ff;"> vcbSnapshot -h localhost -d $i $p<br /> done<br /> done</span>
</p>