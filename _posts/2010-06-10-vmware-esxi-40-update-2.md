---
id: 1160
title: VMware ESX(i) 4.0 Update 2
date: 2010-06-10T21:10:02+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1160
permalink: /2010/06/10/vmware-esxi-40-update-2/
aktt_notify_twitter:
  - yes
ratings_users:
  - 2
ratings_score:
  - 8
ratings_average:
  - 4
aktt_tweeted:
  - 1
views:
  - 5572
categories:
  - vSphere
tags:
  - esx
  - esxi
  - u2
  - update 2
  - vsphere
---
You&#8217;ve guessed it, VMware has released Update 2 of their flagship bare-metal virtualization product ESX and ESXi. This update addresses a number of issues found since the release of Update 1 as well as a number of enhancements, such as:

> **Enablement of Fault Tolerance Functionality for Intel Xeon 56xx Series processors—** vSphere 4.0 Update 1 supports the Intel Xeon 56xx Series processors without Fault Tolerance. vSphere 4.0 Update 2 enables Fault Tolerance functionality for the Intel Xeon 56xx Series processors.
> 
> **Enablement of Fault Tolerance Functionality for Intel i3/i5 Clarkdale Series and Intel Xeon 34xx Clarkdale Series processors—** vSphere 4.0 Update 1 supports the Intel i3/i5 Clarkdale Series and Intel Xeon 34xx Clarkdale Series processors without Fault Tolerance. vSphere 4.0 Update 2 enables Fault Tolerance functionality for the Intel i3/i5 Clarkdale Series and Intel Xeon 34xx Clarkdale Series processors.
> 
> **Enablement of IOMMU Functionality for AMD Opteron 61xx and 41xx Series processors—** vSphere 4.0 Update 1 supports the AMD Opteron 61xx and 41xx Series processors without input/output memory management unit (IOMMU). vSphere 4.0 Update 2 enables IOMMU functionality for the AMD Opteron 61xx and 41xx Series processors.
> 
> **Enhancement of the esxtop/resxtop utility****—** vSphere 4.0 Update 2 includes an enhancement of the performance monitoring utilities, <tt>esxtop </tt>and <tt>resxtop</tt>. The <tt>esxtop</tt>/<tt>resxtop</tt> utilities now provide visibility into the performance of NFS datastores in that they display the following statistics for NFS datastores: <tt>Reads/s</tt>, <tt>writes/s</tt>, <tt>MBreads/s</tt>, <tt>MBwrtn/s</tt>, <tt>cmds/s</tt>, <tt>GAVG/s</tt>(guest latency).
> 
> **Additional Guest Operating System Support**— ESX/ESXi 4.0 Update 2 adds support for Ubuntu 10.04. For a complete list of supported guest operating systems with this release, see the <a href="http://www.vmware.com/resources/compatibility/search.php" target="_blank"><em>VMware Compatibility Guide</em></a>.

<!--more-->

Here are some of the key issues that are resolved in this update;

> <p align="left">
>    <strong>Upgrade of VMware Tools breaks Microsoft SQL Server functionality<br /> </strong>Some third-party software programs, such as Microsoft SQL Server, don&#8217;t share atl71.dll. Therefore, the software doesn&#8217;t increase the .dll reference count during installation. As part a major VMware Tools upgrade, while uninstalling ATL71, the shared library atl71.dll is removed if its sharing reference count reaches 0. As a result, Microsoft SQL Server functionality might break. 
> </p>
> 
> &#8212;
> 
> <p align="left">
>   <strong>When using vSphere Client to access the console of a virtual machine that uses a NetXen NX3031 network interface controller (NIC), the system fails, leading to a purple screen<br /> </strong>When the NetXen NX3031 NIC resides on a relatively high memory location (possibly above 512GB), the system becomes unresponsive as it tries to access an address that is out of range. For example, this issue might occur if the system has a physical memory of 96GB but the memory map configuration generates addresses beyond the 512GB memory location.
> </p>
> 
> A message similar to the following is logged before the system becomes unresponsive: <3>nommu\_map\_single: overflow a31407ad5a+54 of device mask 7fffffffff
> 
> The following is an example of a backtrace of this issue:
  
> 0x4100c00e7338:[0x41801d1984bf]nommu\_map\_single+0x4e stack: 0x0
  
> 0x4100c00e7598:[0x41801d26f745]unm\_nic\_xmit\_frame+0x4d8 stack: 0x4100c00e75c8 0x4100c00e7688:[0x41801d1a1609]process\_tx_queue+0x874 stack: 0x41000b884600
> 
> &#8212;
> 
> <p align="left">
>   <strong>PAE-enabled SMP Windows 2000 virtual machines stop responding<br /> </strong>A Physical Address Extension (PAE) enabled multiprocessor Windows 2000 virtual machine might stop responding on reboot, or fail randomly.
> </p>
> 
> &#8212;
> 
> <p align="left">
>   <strong>Dropped frames can be incorrectly reported by Qlogic drivers for fibre channel host bus adapters (HBAs)<br /> </strong>Storage arrays returning less data than expected (an underrun condition) are incorrectly reported by the Qlogic driver as having dropped frames with a SCSI status of Busy instead of an underrun condition with the original SCSI status. This issue is resolved in this release. The Qlogic driver reports SCSI status correctly and does not report dropped frames.
> </p>
> 
> &#8212;
> 
> **Windows guest operating systems earlier than Windows Vista might lose connectivity when used in conjunction with the vmxnet3 virtual network interface card
  
>** Network Driver Interface Specification (NDIS) is part of the networking architecture used in Microsoft Windows operating systems. The NDIS transport driver might hold, indefinitely, the buffers received by vmxnet3 drivers, thereby running out of buffers to receive.
> 
> &#8212;
> 
> <p align="left">
>   <strong>Virtual machines connected to a vNetwork Distributed Switch (vDS) might be disconnected after a failover<br /> </strong>vDS virtual machine port changes persist the port configuration every five minutes. Since virtual machine port changes are not persisted immediately, virtual machines can lose network connectivity after a failover event if they have been configured to link to a vDS less than five minutes before the failover.
> </p>
> 
> &#8212;
> 
> <p align="left">
>   <strong>A virtual machine fails to respond or power on when its network interface card (NIC) is attached to a port group with a name that exceeds 50 characters<br /> </strong>This issue is resolved in this release. Port group names now cannot be changed to a name that exceeds 50 characters. Previously assigned port group names that exceed 50 characters are not accessible by virtual machines.
> </p>
> 
> &#8212;
> 
> **An issue in the timer emulation causes timer interrupts to be delivered to the guest operating system at an excessive rate
  
>** This issue has been observed after a vMotion migration when a virtual machine has been up for a relatively long time, such as for one hundred days.
> 
> &#8212;
> 
> **Installing ESX on a system with more than eight network interface cards (NICs) might cause the system to become unresponsive
  
>** When you use the text mode method to install VMware ESX on a system that has more than 8 NICs, the installer might stop responding and display an error similar to the following:
  
> An error has occurred during your ESX installation. &#8216;NicSetup&#8217; object has no attribute &#8216;scrollDisplay&#8217;
> 
> &#8212;
> 
> <p align="left">
>   <strong>Speed and duplex settings for a NIC might not be retained after ESX/ESXi host reboots<br /> </strong>When the speed and duplex settings for a NIC are manually set and the ESX/ESXi host is rebooted, the values set for the speed and duplex settings might not be retained. After reboot, the network adapter might auto-negotiate its speed and duplex settings.
> </p>
> 
> &#8212; 
> 
> **Virtual machines running 64-bit Windows Server 2003 or 64-bit Windows XP guest operating systems might report an incorrect CPU frequency
  
>** The CPU frequency reported by 64-bit Windows 2003 and 64-bit Windows XP guest operating systems when run in a virtual machine might be inaccurate. In the virtual machine, QueryPerformanceCounter might run at a rate that is higher than the frequency reported by QueryPerformanceFrequency.
> 
> <span style="font-family: Arial,Arial; font-size: x-small;"><span style="font-family: Arial,Arial; font-size: x-small;"></span></span>

<span style="font-family: Arial,Arial; font-size: x-small;"><span style="font-family: Arial,Arial; font-size: x-small;"><span style="font-family: Courier New,Courier New; font-size: x-small;"><span style="font-family: Courier New,Courier New; font-size: x-small;"><span style="font-family: Arial,Arial; font-size: x-small;"><span style="font-family: Arial,Arial; font-size: x-small;"><span style="font-family: Arial,Arial; font-size: x-small;"><span style="font-family: Arial,Arial; font-size: x-small;"><span style="font-family: Lucida Sans Unicode;">This is just a small subset of the fixes found in VMware ESX(i) 4.0 Update 2, I strongly urge you to read the full <a href="http://www.vmware.com/support/vsphere4/doc/vsp_esx40_u2_rel_notes.html" target="_blank">release notes</a> as a problem you&#8217;re currently experiencing could be resolved by a simply update. For updating your ESX hosts, simply use Update Manager or download the bits from <a href="http://downloads.vmware.com/d/details/esx40u2/ZHcqYmRoZWViZHR3ZA==" target="_blank">VMware.com</a> and use the Host Update Utility to perform these upgrades.</span></span></span></span></span></span></span></span></span>