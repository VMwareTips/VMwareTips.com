---
id: 1162
title: VMware ESX(i) 4.0 Patch Bundle 06
date: 2010-05-28T08:43:33+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1162
permalink: /2010/05/28/vmware-esxi-40-patch-bundle-06/
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
  - 1185
dsq_thread_id:
  - 5156592685
categories:
  - vSphere
tags:
  - esx
  - esxi
  - patch
  - updates
  - vsphere
---
As handful of patches have just been released by VMware for their flagship bare-metal virtualization products ESX and ESXi.

With no surprise to me the majority of the patches are for ESX and relate to security flaws and vulnerabilities found within the Service Console.  Keep in mind these vulnerabilities in **no-way** mean the virtual machines being hosted are at risk. These patches are typically for underlying services that the Service Console rely on, such as openssl, java, gzip and ntp. Sometimes these patches also resolve issues on how the Service Console communicates with the vmkernel layer as well as system devices.

Two of the patch bundles for ESXi share some common fixes with it&#8217;s ESX brother which cover a NTP vulnerability, a shared interrupt issue between the vmkernel and _console_ as well as a patch that properly enables quiescing utilizing the Microsoft Windows VSS components found in Windows 2008 R2 and Windows 7.

More information on these patches can be found by reviewing the individual bundles;

**ESX 4.0 &#8211; <a href="http://kb.vmware.com/kb/1019491" target="_blank"><span>ESX400-201005001</span><br /> </a>**Includes 9 updates, including fixes for NTP, gzip, bind, vmkernel, krb5, webCenter, Expat, sudo and gcc.

**ESXi 4.0 &#8211; <span>ESXi400-201005001</span>
  
** Includes two updates, <span><a href="http://kb.vmware.com/kb/1021041" target="_blank"><strong>ESXi400-201005401-SG</strong></a> for the ESXi firmware and <strong><span><a href="http://kb.vmware.com/kb/1021042" target="_blank">ESXi400-201005402-BG</a></span> </strong>for VMware Tools.</span>

For updating your ESX(i) hosts, simply use Update Manager or <a href="http://www.vmware.com/patch/download/" target="_blank">download the patches</a> from the VMware website and use the Host Update Utility to perform these updates.