---
id: 20
title: NetApp Snapshots in ESX
date: 2008-09-12T14:32:23+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=20
permalink: /2008/09/12/netapp-snapshots-in-esx/
redirect_from: /wp/2008/09/12/netapp-snapshots-in-esx/
views:
  - "18131"
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
aktt_notify_twitter:
  - 'yes'
dsq_thread_id:
  - "5156596569"
categories:
  - 'Backup &amp; Recovery'
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - NetApp
  - Storage
  - VMware
tags:
  - NetApp
  - script
  - snapshot
  - ssh
  - vimsh
---
**<span style="color: #ff0000;">UPDATE: I have re-written this script for enhancements, these can be found on the post titled <em>&#8220;<a href="http://vmwaretips.com/wp/2008/12/05/netapp-snapshots-in-esx-take-2/">NetApp Snapshots in ESX &#8211; Take 2</a>&#8220;</em></span>**

Many of you NetApp/ESX users should know by now that SnapManager for VI has been released. Many of you should also know that NetApp&#8217;s costs of licensing such tools can be fairly pricey. For those of us that can&#8217;t afford or justify the purchase of SMVI, I give to you a very handy script that I wrote&#8230;.



This script will first create quiesced VMware ESX Snapshots, then connect to your NetApp FAS and kick off a snapshot creation.

> _There is one prerequisite and that is to enable password-less SSH access from your ESX host and into your filer. Please look up the post &#8216;**<a href="http://vmwaretips.com/wp/2009/01/16/ssh-from-an-esx-host-into-netapp-ontap/" target="_blank">SSH from an ESX host into NetApp OnTap</a>&#8216;** for more information on how to do this. Another would be if you have multiple ESX servers, you need to enable password-less SSH access into those machines as well. Please look up the post &#8216;<a href="http://vmwaretips.com/wp/2009/01/16/ssh-from-esx-host-to-esx-host-with-no-password/" target="_blank"><strong>SSH from ESX to ESX</strong></a>&#8216; for more information on how to do this._

The script is very basic, I will include it below and go over each line and what they do.

> _<span style="text-decoration: underline;">#first we set which shell to use, adding -x to /bin/sh will enable verbose output</span>_
> 
> <span style="color: #ff0000;">#!/bin/sh -x</span>
> 
> _<span style="text-decoration: underline;"># set path and date, this will be used to idenify your snapshots in case of failure</span>_
> 
> <span style="color: #ff0000;">DATE=`date +%m.%d.%G.%H%M`<br /> PATH=$PATH:/bin:/usr/bin</span>
> 
> _<span style="text-decoration: underline;">#now we will use a for-do-done loop to get the VM ID&#8217;s and create a snapshot.<br /> #vmware-vim-cmd vmsvc/getallvms will retreive ALL virtual machines on that host<br /> #piping it to sed and awk will let us grab JUST the VM ID</span>_
> 
> <span style="color: #ff0000;">for i in `vmware-vim-cmd vmsvc/getallvms | sed &#8216;1d&#8217; | awk &#8216;{print $1}&#8217;`</span>
> 
> <span style="text-decoration: underline;"><em>#Now we will do the do loop with the VM ID&#8217;s we grabbed.<br /> #vmware-vim-cmd vmsvc/snapshot.create will let us create snapshots<br /> #$i is the VM ID we grabbed<br /> #The first string after the VM ID is the Snapshot Name<br /> #Second string is the Snapshot Description, see how we&#8217;re using $DATE<br /> </em></span>
> 
> <span style="color: #ff0000;">do<br /> vmware-vim-cmd vmsvc/snapshot.create $i Nightly Netapp.Snapshot.$DATE true<br /> done</span>
> 
> <span style="text-decoration: underline;"><em>#Now we can create our NetApp snapshots &#8211; Here I keep one week worth of snapshots<br /> #Taken once per day that means I need 7 snaps and the 8th is deleted<br /> #So first we will delete the 8th, then rename the others in reverse order, then create a new one </em></span>
> 
> <span style="color: #ff0000;">ssh <netapp> snap delete <volume> vmsnap.8<br /> ssh <netapp> snap rename <volume> vmsnap.7 vmsnap.8<br /> ssh <netapp> snap rename <volume> vmsnap.6 vmsnap.7<br /> ssh <netapp> snap rename <volume> vmsnap.5 vmsnap.6<br /> ssh <netapp> snap rename <volume> vmsnap.4 vmsnap.5<br /> ssh <netapp> snap rename <volume> vmsnap.3 vmsnap.4<br /> ssh <netapp> snap rename <volume> vmsnap.2 vmsnap.3<br /> ssh <netapp> snap rename <volume> vmsnap.1 vmsnap.2<br /> ssh <netapp> snap create <volume> vmsnap.1</span>
> 
> <span style="text-decoration: underline;"><em>#Finally we will go back and remove those VMware snapshots using vmware-vim-cmd</em></span>
> 
> <span style="color: #ff0000;">for i in `vmware-vim-cmd vmsvc/getallvms | sed &#8216;1d&#8217; | awk &#8216;{print $1}&#8217;`<br /> do<br /> vmware-vim-cmd vmsvc/snapshot.removeall $i<br /> done</span>

If you have multiple ESX hosts you can use the do loop statement to SSH into them and create/remove snapshots.

> <span style="text-decoration: underline;"><em>#Same script as above, but we will SSH into the host and run the command remotely<br /> <span style="font-style: normal;"><em>#To generate snapshots&#8230;.</em></span></em></span>
> 
> <span style="color: #ff0000;">for i in `ssh dpcrcvmesx2 vmware-vim-cmd vmsvc/getallvms | sed &#8216;1d&#8217; | awk &#8216;{print $1}&#8217;`<br /> do<br /> ssh dpcrcvmesx2 vmware-vim-cmd vmsvc/snapshot.create $i Nightly Netapp.Snapshot.$DATE includeMemory<br /> done</span>
> 
> _<span style="text-decoration: underline;">#To remove snapshots&#8230;<br /> </span><span style="font-style: normal;"><span style="color: #ff0000;">for i in `ssh dpcrcvmesx2 vmware-vim-cmd vmsvc/getallvms | sed &#8216;1d&#8217; | awk &#8216;{print $1}&#8217;`<br /> do<br /> ssh dpcrcvmesx2 vmware-vim-cmd vmsvc/snapshot.removeall $i<br /> done</span></span>
  
>_ 

I&#8217;ve included the script in this post so you can download it. You may have noticed that the script will remove all of your snapshots, frankly I do not like this but I have yet to hear from VMware support on how to effectively use the vmsvc/snapshot.remove function. If you know how to do this please email me or comment and I&#8217;ll be sure to give you proper recognition.

One last thing to do after you write your script is to put it in the crontab of your server, crontab is similar to the Scheduled Tasks function of Windows, it allows you to run programs/scripts at select times. It is extremely flexible!

> crontab -e (this edits your existing crontab)
> 
> The following shows my crontab, I run my script at Midnight and 12:00PM every day, I also output the results of the job to a log file (that gets written over each time).
> 
> **[root@dpcrcvmesx1 .ssh]# crontab -l
  
> 0 0,12 \* \* * /usr/sbin/vmnfssnap > /var/log/vmnfssnap 2>&1**

There are thousands of different ways you can do this, but this is how we do it at my job and it works without error. Hopefully this encourages you to look into all the different ways you can use scripting with VMware ESX to maintain and manage your system.