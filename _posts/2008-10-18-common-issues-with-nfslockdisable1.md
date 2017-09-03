---
id: 105
title: Common issues with NFS.LockDisable=1
date: 2008-10-18T09:53:12+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=105
permalink: /2008/10/18/common-issues-with-nfslockdisable1/
views:
  - "11923"
ratings_users:
  - "2"
ratings_score:
  - "10"
ratings_average:
  - "5"
dsq_thread_id:
  - "5156597488"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - NetApp
  - Storage
  - VMware
  - VMware HA
tags:
  - corrupt
  - esx
  - esx350-200808401-bg
  - lock
  - locking
  - NetApp
  - nfs
  - nfs.lock
  - patch
  - vmwareHA
---
<span style="color: #888888;">After seeing a mention on Scott Lowe&#8217;s blog (<a href="http://blog.scottlowe.org/2008/10/18/important-note-regarding-vmware-over-nfs/" target="_blank">blog.scottlowe.org</a>) and on Storage Monkeys Blog (<a href="http://blogs.storagemonkeys.com/index.php/2008/10/important-note-regarding-vmware-over-nfs/" target="_blank">blogs.storagemonkeys.com</a>) I&#8217;ve decided to discuss the issue(s) that I&#8217;ve came across in regards to disabling NFS Locking with the NFS.LockDisable=1 function.</span>

<!--more-->

<span style="color: #888888;">As the problem can arise from many different circumstances, the majority of feedback I&#8217;m receiving appears to be caused by a VMware HA failover (either intentional or unintentional). Thus, I would like to discuss VMware HA and how it works (based on my experience and knowledge).<br /> </span>

<span style="color: #888888;">But before that, let me mention that the end result of having NFS.LockDisable set to 1 is that Virtual Machines <strong><span style="text-decoration: underline;">can</span></strong> become corrupt (Windows VMs blue screen and give NTFS errors / Linux guests are more resilient and could potentially be fixed by a fsck, but you should always have a good backup regardless). This is caused by the fact that multiple ESX hosts can start the same VMX at the same time. Ok, lets continue&#8230;</span>

<span style="color: #888888;">From what I can see when you configure VMware HA the first (4) nodes configured are marked as primary, every host after the fourth is considered a backup node. In the event of a HA fail-over the primary nodes will all attempt to start the VMs that were running on the failed node. It appears they rely on the VM locking to determine if the VM is actually down or not. So what this means is regardless of Isolation Response the VM can actually be powered on multiple times. In fact, in the couple times this has happened to me I had the same running VM on up to (3) hosts at once.</span>

<span style="color: #888888;">You can also see some strange behaviors in VirtualCenter, such as the number of Virtual Machines registered in each host will jump up and down within seconds. I would look at the summary of one of my hosts and see the Virtual Machine count go from 20 to 35 to 28 to 40 and so on.</span>

<span style="color: #888888;">The only true way to clear this up is from the service console to do the following;</span>

  1. <span style="color: #888888;">Run a <em>vmware-cmd -l</em> on each of your hosts within the cluster. </span> 
      * <span style="color: #888888;">Output this data to a file so you can sort it later (ie: <em>vmware-cmd -l > host1). </em></span>
  2. <span style="color: #888888;">Sort those host files together into one master file (ie: <em>sort host1 host2 host3 > masterVMlist</em>).</span>
  3. <span style="color: #888888;">View the master VM list and determine which VMX files are registered multiple times. </span> 
      * <span style="color: #888888;">Now this is the tricky part, if you have tons of hosts within a cluster it will take some time to actually find where they are really located, but you do know which ones are registered multiple times. Knowing the list of multi-registered VMX files, you could potentially create a script that ssh&#8217;s to each of your ESX hosts and runs a <em>vmware-cmd -l</em><em> </em> grepping for the VMX file, then returning a code notifying you if its there or not. Since I only had (4) nodes on the cluster that failed this wasn&#8217;t necessary for me.</span>
  4. <span style="color: #888888;">You can run a <em>ps aux | grep VMX-FILE</em> on the hosts where they are registered to determine the PID.</span>
  5. <span style="color: #888888;">Use <em>kill -9 PID</em> to remove the running VM. Magically it will become unregistered on the invalid hosts.</span>

<span style="color: #888888;">Ok, so in closing I do not want to put all the blame on VMware HA, it is actually a combination of NFS.LockDisable=1 and what happens because of that that causes the potential corruption. The same result can occur by manually registering and starting the same VMX on multiple hosts (as with disabling locking it removes the that added layer of security).</span>

<span style="color: #888888;"><strong>It is extremely important that you enable NFS Locking by changing NFS.LockDisable back to the default setting of 0. You should also install VMware Patch <span style="text-decoration: underline;">ESX350-200808401-BG</span>. I discuss the fix of this issue in another posting, which can be <a href="http://vmwaretips.com/wp/?p=48">found here.</a></strong></span>