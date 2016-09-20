---
id: 1274
title: VMware vSphere 4.1 U1 Released
date: 2011-02-11T19:08:11+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1274
permalink: /2011/02/11/vmware-vsphere-41-u1-released/
ratings_users:
  - 2
ratings_score:
  - 9
ratings_average:
  - 4.5
views:
  - 4480
categories:
  - vSphere
tags:
  - esx
  - esxi
  - upgrade
  - vcenter
  - VMware
  - vsphere
  - vsphere 4.1
  - vsphere 4.1 U1
---
Yesterday, February 10th, VMware made available for general consumption U1 to their vSphere 4.1 product line. This update includes all prior patches as well as a number of new enhancements to the vSphere product suite.

This release provides the following improvements, I&#8217;ve included some notes along with the high-level updates:

**VMware ESX/ESXi**

  * Support for up to 160 logical processors 
      * Prepared for the release of the Westmere-EX processor
  * Inclusion of additional drivers 
      * 3ware and Neterion drives are now included
  * Enablement of Intel Trusted Execution Technology (ESXi only) 
      * More information on this can be found in <a href="http://kb.vmware.com/kb/1033811" target="_blank">KB 1033811</a> 
  * Additional guest operating system support 
      * Provides support for RHEL 6, RHEL 5.6, SLES 11 SP1 for VMware, Ubuntu 10.10, and Solaris 10 Update 9 guest operating systems
  * Bug and security fixes 
      * A listing of resolved issues can be found in the <a href="http://www.vmware.com/support/vsphere4/doc/vsp_esxi41_u1_rel_notes.html#resolvedissues" target="_blank">release notes</a>

**VMware vCenter**

  * Additional guest operating system customization support 
      * Windows 7 SP1, Windows Server 2008 R2 SP1, RHEL 6, RHEL5.5
  * Additional vCenter Server database support 
      * SQL 2008 R2, SQL 2005 SP3, Oracle 11g R2, DB2 9.7.2
  * Bug and security fixes 
      * A listing of resolved issues can be found in the <a href="http://www.vmware.com/support/vsphere4/doc/vsp_vc41_u1_rel_notes.html#resolvedissues" target="_blank">release notes</a>

**VMware vCenter Update Manager**

  * The VMware vCenter Update Manager Utility to help users reconfigure the setup of Update Manager.
  * Bug and security fixes.

**VMware vCenter Orchestrator**

  * Bug Fixes

For additional details regarding the new fixes and improvements, please refer to the following release notes:
  
<a href="http://www.vmware.com/support/vsphere4/doc/vsp_esx41_u1_rel_notes.html" target="_blank"><span style="color: #269cd7;">VMware ESX</span></a>
  
<a href="http://www.vmware.com/support/vsphere4/doc/vsp_esxi41_u1_rel_notes.html" target="_blank"><span style="color: #269cd7;">VMware ESXi </span></a>
  
<a href="http://www.vmware.com/support/vsphere4/doc/vsp_vc41_u1_rel_notes.html" target="_blank"><span style="color: #269cd7;">VMware vCenter</span></a>

VMware vSphere 4.1 Update 1 is available for <a href="http://downloads.vmware.com/d/info/datacenter_downloads/vmware_vsphere_4/4_0" target="_blank"><span style="color: #269cd7;">download</span></a> from the VMware website as well as through VMware Update Manager (for your ESX and ESXi hosts). Keep in mind, the only way you can switch from ESX to ESXi is to do a fresh install. I&#8217;d highly recommend using Host Profiles to make this migration quicker and easier.

Jason Boche has already noted one potential issue with using VMware Update Manager (VUM) to upgrade from 4.1 to 4.1 U1, check that out <a href="http://www.boche.net/blog/index.php/2011/02/11/vsphere-4-1-update-1-upgrade-file-issues/" target="_blank">here</a>.