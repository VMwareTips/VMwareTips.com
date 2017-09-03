---
id: 1158
title: VMware vCenter Server 4.0 Update 2
date: 2010-06-10T21:14:11+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1158
permalink: /2010/06/10/vmware-vcenter-server-40-update-2/
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
  - "12724"
categories:
  - vCenter
  - vSphere
tags:
  - vcenter
  - vcenter server
  - vcenter server update 2
  - vsphere
  - vsphere update 2
---
VMware has just dropped the second major update bundle (Update 2) for their flagship virtualization management product, VMware vCenter server.  This update addresses a number of issues found since the release of Update 1 as well as a number of improvements, such as:

> **Guest Operating System Customization Improvements**: vCenter Server now supports customization of the following guest operating systems:
> 
>   * Windows XP Professional SP2 (x64) serviced by Windows Server 2003 SP2
>   * SLES 11 (x32 and x64)
>   * SLES 10 SP3 (x32 and x64)
>   * RHEL 5.5 Server Platform (x32 and x64)
>   * RHEL 5.4 Server Platform (x32 and x64)
>   * RHEL 4.8 Server Platform (x32 and 64)
>   * Debian 5.0 (x32 and x64)
>   * Debian 5.0 R1 (x32 and x64)
>   * Debian 5.0 R2 (x32 and x64)

Here are some of the key issues that are resolved in this update;

<!--more-->

> **Storage vMotion fails even if the destination datastore has sufficient disk space
  
>** Storage vMotion might fail even if the space available on the destination datastore is more than the moving disk space because the calculation considers the shared swap file size of the virtual machine as well. When the failure occurs, an error message similar to the following might be displayed in the **Migrate Virtual Machine** dialog box in the vSphere Client:  Insufficient disk space on datastore.
> 
> <p align="left">
>   Starting with this release, shared swap file space is not considered in calculating the required space in the destination datastore.
> </p>
> 
> <p align="left">
>   &#8212;
> </p>
> 
> **VirtualCenter stops responding while retrieving historical events
  
>** While retrieving historical events from VirtualCenter, the VirtualCenter Server Service might stop responding. An error message similar to the following might be written to the logs:
  
> Panic: Assert Failed: &#8220;pos != string::npos&#8221; @ d:/build/ob/bora-161137/bora/vim/lib/vmomi/soapVisitor.cpp:731
  
> You can restart VirtualCenter, but it might fail again if you attempt to retrieve historical data.
> 
> &#8212;
> 
> <p align="left">
>   <strong>Selecting the Power Management option of a virtual machine that has five or more network adapters results in an error<br /> </strong>On the vSphere Client, selecting the <strong>Power Management </strong>option of a virtual machine that has five or more network adapters might result in the following error message:<br /> Index was out of range. Must be non-negative and less than the size of the collection.<br /> Parameter name: index
> </p>
> 
> <p align="left">
>   &#8212;
> </p>
> 
> <p align="left">
>   <strong>vCenter Server 4.0 cannot manage a ESX 3.x host if the VirtualCenter 2.5.x license server FQDN has a non-standard suffix<br /> </strong>If the fully qualified domain name (FQDN) of the VirtualCenter 2.5.x license server ends with .local or .eng instead of a standard suffix such as .com or .net, access to items such as <strong>Advanced Settings </strong>in the <strong>vCenter Server Settings </strong>window might fail with an Enter a valid license server error message.
> </p>
> 
> vCenter Server 4.0 U2 can be configured with a license server even if the FQDN has a non-standard suffix.
> 
> <p align="left">
>   &#8212;
> </p>
> 
> <p align="left">
>   <strong>Virtual machine starts on the host it was registered on, even if it is scheduled to start on another host<br /> </strong>On an ESX host, when scheduling to power on a virtual machine, you have the option to select another host on which the virtual machine should be deployed. A virtual machine might start on the host it was registered on, even if it is scheduled to start on another host.
> </p>
> 
> <p align="left">
>   &#8212;
> </p>
> 
> <p align="left">
>   <strong>You cannot mount an ISO or local CD-ROM device on a virtual machine when default ports in vCenter Server 4.0 are changed</strong><br /> If you change the default HTTP or HTTPS ports (80 and 443) of vCenter Server 4.0, an attempt to mount an ISO or CD-ROM device on a virtual machine might fail with an error message similar to the following: A connection to the host could not be established
> </p>
> 
> <p align="left">
>   This issue is resolved in this release. Starting with this release, you can mount ISO or CD-ROM devices even if you change the vCenter Server default ports.
> </p>
> 
> <p align="left">
>   &#8212;
> </p>
> 
> <p align="left">
>   <strong>Host CPU and Host Memory statistics might not be displayed for all virtual machines<br /> </strong>If the vCenter Server inventory has more than one virtual machine, in the vSphere Client Datastores view, Host CPU and Host Memory statistics are displayed only for the first virtual machine in the list.
> </p>
> 
> <p align="left">
>   &#8212;
> </p>
> 
> <p align="left">
>   <strong>Ejecting a CD from a virtual machine causes vCenter Server to stop responding<br /> </strong>If you use the Lab Manager UI to eject a CD from a virtual machine while a provisioning operation is in progress on the vCenter Server, the VMware VirtualCenter Server Service might stop responding. A Panic: Win32 invalid parameter error message might be written to the vpxd.log.
> </p>
> 
> <p align="left">
>   &#8212;
> </p>
> 
> <p align="left">
>   <strong>ESX hosts are disconnected from vCenter Server if enumeration of attached datastores takes a long time<br /> </strong>When you perform I/O intensive operations such as taking multiple snapshots of virtual machines, hostd takes a long time to respond, and as a result, the ESX host might become disconnected from the vCenter Server. You might observe that the vdf command (or any command for querying the datastores) takes a long time to run. Errors might not be written to the logs as the operation eventually completes. However, the vpxd log marks the host and virtual machines as disconnected.
> </p>
> 
> <p align="left">
>   &#8212;
> </p>
> 
> <p align="left">
>   <strong>vMotion times out if the virtual machine swap file is located on the local storage<br /> </strong>If the vswap file of a virtual machine running memory intensive operations is located on the local storage, a vMotion operation that you perform on the virtual machine might time out. The vCenter Server might display an operation timed out error message for the virtual machine migration operation, even if the migration completes.
> </p>
> 
> <p align="left">
>   This issue might still occur. However, starting with this release, the timeout value is configurable. Earlier the timeout value was hardcoded. Add the following parameters to the vpxa.cfg file on the ESX host:
> </p>
> 
> <p align="left">
>   <config><br /> ..<br /> <vpxa><br /> ..<br /> <vmotion><br /> <vmIdAcquireTimeout><New timeout value in seconds></vmIdAcquireTimeout><br /> </vmotion><br /> ..<br /> </vpxa><br /> ..<br /> </config>
> </p>
> 
> <p align="left">
>   &#8212;
> </p>
> 
> <p align="left">
>   <strong>Unable to set preferred path for a fixed Policy within path management when vSphere Client is connected to the vCenter Server<br /> </strong>When you try to change the preferred path of a storage device set to a fixed policy with multiple paths, the vSphere Client might display the following error message: Unable to cast object of type &#8216;LogicalUnitPolicy&#8217; to type &#8216;FixedLogicalUnitPolicy&#8217;
> </p>
> 
> <div>
>   <span style="font-family: Corbel; font-size: small;"><span style="font-family: Corbel; font-size: small;">&#8212;</span></span>
> </div>
> 
> **ESX hosts might stop responding if their IP address is changed by applying host profiles
  
>** If ESX hosts are added to vCenter Server by using IP addresses, and the IP addresses of these ESX hosts are changed by applying host profiles, the hosts might stop responding. The applying host profile operation might time out and the ESX Server hosts remain in the non responsive mode until the ESX hosts are disconnected and reconnected to the vCenter Server.

<p align="left">
  There are actually dozens of other <a href="http://www.vmware.com/support/vsphere4/doc/vsp_vc40_u2_rel_notes.html#resolvedissues" target="_blank">resolved issues</a>, I highly recommend reading the <a href="http://www.vmware.com/support/vsphere4/doc/vsp_vc40_u2_rel_notes.html" target="_blank">release notes</a> for this update and then upgrading as soon as you can fit it into your update schedule. Updating your environment to U2 isn’t that difficult, for vCenter Server simply <a href="http://downloads.vmware.com/d/info/datacenter_downloads/vmware_vsphere_4/4" target="_blank"><span style="color: #40748c;">download</span></a> the installation files from VMware and install like any previous version.  Please make sure you create a consistent backup of the vCenter database before trying any upgrade procedure. During vCenter Server U2 installation ensure that you choose the option to maintain your existing database, or else it will wipe your vCenter database.
</p>