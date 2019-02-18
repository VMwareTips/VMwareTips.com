---
id: 1085
title: VMware vSphere 4.0 Update 1 Released
date: 2009-11-25T11:10:27+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=1085
permalink: /2009/11/25/vmware-vsphere-40-update-1-released/
redirect_from: /wp/2009/11/25/vmware-vsphere-40-update-1-released/
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
  - "8190"
categories:
  - vSphere
tags:
  - view 4
  - vsphere update 1
---
This is a couple days past due, but VMware has released Update 1 of their flagship vSphere product line.

One of the key drivers of this update is to provide support for VMware View 4 which was just released for download as well.

It also provides support for Windows 2008 R2 and Windows 7, for both as a Guest Operating System and base O/S for the vSphere Client.  This resolves the freeze issue in both of those O/S as discussed in my <a href="https://www.vmwaretips.com/wp/2009/11/25/windows-2008-r2-and-windows-7-freeze-on-vmware-vsphere-4/" target="_blank">previous article</a>.

Another hot update is the full support to utilize the pvSCSI adapter for your boot disk on Windows 2003 and Windows 2008.

Here are a few of the other items from the What&#8217;s New section of the Release Notes:

> **VMware vSphere 4.0 Update 1 ESX Release Notes
  
> What&#8217;s New**
> 
> **Enhanced Clustering Support for Microsoft Windows –** Microsoft Cluster Server (MSCS) for Windows 2000 and 2003 and Windows Server 2008 Failover Clustering is now supported on an VMware High Availability (HA) and Dynamic Resource Scheduler (DRS) cluster in a limited configuration. HA and DRS functionality can be effectively disabled for individual MSCS virtual machines as opposed to disabling HA and DRS on the entire ESX/ESXi host**.** Refer to the _<a href="http://www.vmware.com/pdf/vsphere4/r40_u1/vsp_40_u1_mscs.pdf" target="_blank">Setup for Failover Clustering and Microsoft Cluster Service</a>_ guide for additional configuration guidelines.
> 
> ****
> 
> **Improved vNetwork Distributed Switch Performance** **–** Several performance and usability issues have been resolved resulting in the following:
> 
>   * Improved performance when making configuration changes to a vNetwork Distributed Switch (vDS) instance when the ESX/ESXi host is under a heavy load
>   * Improved performance when adding or removing an ESX/ESXi host to or from a vDS instance
> 
> **Increase in vCPU per Core Limit** **–** The limit on vCPUs per core has been increased from 20 to 25. This change raises the supported limit only. It does not include any additional performance optimizations. Raising the limit allows users more flexibility to configure systems based on specific workloads and to get the most advantage from increasingly faster processors. The achievable number of vCPUs per core depends on the workload and specifics of the hardware. For more information see the _<a href="http://www.vmware.com/pdf/Perf_Best_Practices_vSphere4.0.pdf" target="_blank">Performance Best Practices for VMware vSphere 4.0</a>_ guide.
> 
> **Enablement of Intel Xeon Processor 3400 Series** – Support for the Xeon processor 3400 series has been added. For a complete list of supported third party hardware and devices, see the <a href="http://www.vmware.com/resources/compatibility/search.php" target="_blank">VMware Compatibility Guide</a>.
> 
> **Resolved Issues** **–** In addition, this release delivers a number of bug fixes that have been documented in the Resolved Issues section.

Updating your environment to U1 isn&#8217;t that difficult, for vCenter Server simply <a href="http://downloads.vmware.com/d/info/datacenter_downloads/vmware_vsphere_4/4" target="_blank">download</a> the installation files from VMware and install like any previous version.  Ensure that you choose the option to maintain your existing database, or else you&#8217;ll lose all of your data.

For updating your ESX hosts, simply use Update Manager or the Host Update Utility to perform these upgrades.

More information on Update 1 can be <a href="http://www.vmware.com/support/vsphere4/doc/vsp_esx40_u1_rel_notes.html" target="_blank">found here</a>.