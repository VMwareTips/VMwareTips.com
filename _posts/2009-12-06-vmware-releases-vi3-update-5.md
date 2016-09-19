---
id: 1090
title: VMware Releases VI3 Update 5
date: 2009-12-06T11:43:29+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1090
permalink: /2009/12/06/vmware-releases-vi3-update-5/
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
  - 3743
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - vCenter
tags:
  - esx
  - esxi
  - update
  - vcenter
  - vi3
  - virtual infrastructure
---
Sometime yesterday ESX(i) Update 5 finally hit VMware Update Manager, about 2 days after the official announcement and release on the VMware website. This announcement includes updates for ESX, ESXi and vCenter Server. In addition to Update 5 being released there were about 20 additional updates made available for ESX(i), including 16 which were marked as critical.

The following information provides highlights of some of the enhancements available in this release of VMware ESX Server, this information can be found in the VMware ESX(i) 3.5 U5 <a href="http://www.vmware.com/support/vi3/doc/vi3_esx35u5_rel_notes.html" target="_blank">Release Notes</a>:

> **Enablement of Intel Xeon Processor 3400 Series**– Support for the Intel Xeon processor 3400 series has been added. Support includes Enhanced VMotion capabilities. For additional information on previous processor families supported by Enhanced VMotion, see <a href="http://kb.vmware.com/kb/1003212" target="_blank">Enhanced VMotion Compatibility (EVC) processor support</a> (KB 1003212).
> 
> **Driver Update for Broadcom bnx2 Network Controller**– The driver for bnx2 controllers has been upgraded to version 1.6.9. This driver supports bootcode upgrade on bnx2 chipsets and requires <tt>bmapilnx</tt> and <tt>lnxfwnx2</tt>tools upgrade from Broadcom. This driver also adds support for Network Controller &#8211; Sideband Interface (NC-SI) for SOL (serial over LAN) applicable to Broadcom NetXtreme 5709 and 5716 chipsets.
> 
> **Driver Update for LSI SCSI and SAS Controllers** – The driver for LSI SCSI and SAS controllers is updated to version 2.06.74. This version of the driver is required to provide a better support for shared SAS environments.
> 
> **Newly Supported Guest Operating Systems** – Support for the following guest operating systems has been added specifically for this release:
> 
> For more complete information about supported guests included in this release, see the VMware Compatibility Guide: <a href="http://www.vmware.com/resources/compatibility/search.php?deviceCategory=software" target="_blank">http://www.vmware.com/resources/compatibility/search.php?deviceCategory=software</a>.
> 
>   * Windows 7 Enterprise (32-bit and 64-bit)
>   * Windows 7 Ultimate (32-bit and 64-bit)
>   * Windows 7 Professional (32-bit and 64-bit)
>   * Windows 7 Home Premium (32-bit and 64-bit)
>   * Windows 2008 R2 Standard Edition (64-bit)
>   * Windows 2008 R2 Enterprise Edition (64-bit)
>   * Windows 2008 R2 Datacenter Edition (64-bit)
>   * Windows 2008 R2 Web Server (64-bit)
>   * Ubuntu Desktop 9.04 (32-bit and 64-bit)
>   * Ubuntu Server 9.04 (32-bit and 64-bit)
> 
> **Newly Supported Management Agents** – See <a href="http://www.vmware.com/support/esx25/doc/sys_mgmt_links.html" target="_blank">VMware ESX Server Supported Hardware Lifecycle Management Agents</a> for current information on supported management agents.
> 
> **Newly Supported Network Cards –**This release of ESX Server supports HP NC375T (NetXen) PCI Express Quad Port Gigabit Server Adapter.
> 
> **Newly Supported SATA Controllers** – This release of ESX Server supports the Intel Ibex Peak SATA AHCI controller.

In addition to the enhancements found in ESX(i) 3.5 U5, there is also one lonely enhancement made to vCenter Server 2.5 U5:

> **Support for High Consolidation in VMware HA Clusters**&#8211; VirtualCenter 2.5 Update 5 includes significant performance and scalability improvements to VMware HA. Use VirtualCenter 2.5 Update 5 for environments with more than 35 virtual machines per host in an HA cluster.
  
> For information on the ESX Server host settings required for this scalability improvement, see <a href="http://kb.vmware.com/kb/1012002" target="_blank">ESX Server host settings required for environments with up to 80 virtual machines per host in an HA Cluster</a> (KB 1012002).

Updating your ESX servers can and should be done with VMware Update Manager. To upgrade your vCenter Server installation you&#8217;ll need to download the installation ISO or ZIP from the <a href="http://downloads.vmware.com/d/details/vc250u5/dGViZHd0QGJkZXBo" target="_blank">VMware website</a> and perform an in-place upgrade. Be sure to create a backup of your vCenter Server database then follow the steps in the <a href="http://www.vmware.com/pdf/vi3_35/esx_3/r35u2/vi3_35_25_u2_installation_guide.pdf" target="_blank">Installation Guide</a>.