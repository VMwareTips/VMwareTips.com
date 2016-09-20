---
id: 628
title: VMware vCenter 2.5 U4 Released
date: 2009-02-27T07:09:57+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=628
permalink: /2009/02/27/vmware-vcenter-25-u4-released/
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
  - 5484
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
tags:
  - vcenter
---
A few days ago VMware released vCenter 2.5 U4, the latest installment of their vCenter Server.  I have yet to upgrade my environment(s), but I will be planning to do so very soon.  There are two new enhancements to vCenter with this release, and a handful of updates.

<!--more-->

**What&#8217;s New**

  * **Guest Operating System Customization Improvements
  
** VirtualCenter now supports customization of Windows Server 2008 guest operating systems.
  * **Performance Overview Charts
  
** VirtualCenter 2.5 Update 4 introduces the Performance Overview plug-in, which provides a single view of key performance metrics for CPU, memory, disk, and network without having to navigate through multiple charts. The aggregated charts show high-level summaries of resource distribution. To install the Performance Overview plug-in, see <a href="http://vmwaretips.com/wp/2009/02/27/installing-the-performance-overview-plug-in-in-virtualcenter-25-update-4" target="_self">Installing the Performance Overview Plug-In in VirtualCenter 2.5 Update 4</a> (KB 1008296)

One of the biggest updates that effects me personally is the update to Storage VMotion;

  * **Storage VMotion Creates Temporary delta.vmdk Files Only for the Virtual Disks That Are Migrated
  
** In previous releases, if a virtual machine has more than one virtual disk and you want to move only some of the virtual disks to another datastore by using Storage VMotion, temporary <tt>delta.vmdk</tt> files are created for all virtual disks attached to the virtual machine. Starting with VirtualCenter 2.5 Update 4, during Storage VMotion, temporary <tt>delta.vmdk </tt>files are created only for the virtual disks that are migrated to another datastore.

This is a pretty big enhancement. With the current version, say you wanted to move a large backup VMDK to another datastore and you knew it would take a while to copy. SVMotion would actually snapshot all of the VMDK files for the Virtual Machine, migrate only the VMDK you chose to move then commit the snapshot.  This means your delta VMDK files would typically be pretty large for your active VMDK disks, taking unnecessary disk space and time to commit.

I&#8217;m curious if they&#8217;ve resolved the issue of not migrating the VM config (vmx). Currently if you SVMotion&#8217;d a VM and kept the destination the same as its source for the vmx file, it would error saying that it is not supported.

For the full listing of changes, read the <a href=" http://www.vmware.com/support/vi3/doc/vi3_vc25u4_rel_notes.html" target="_blank">vCenter 2.5 U4 release notes</a>.