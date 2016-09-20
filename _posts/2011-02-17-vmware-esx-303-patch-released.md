---
id: 1286
title: VMware ESX 3.0.3 Patch Released
date: 2011-02-17T00:26:55+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=1286
permalink: /2011/02/17/vmware-esx-303-patch-released/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 1039
categories:
  - VMware
tags:
  - esx
  - esx 3.0
  - patch
  - patches
  - update
  - vi3
  - vmware vi3
---
For those of you still running the VI 3.0 suite of **vm**ware products will be happy to know that **vm**ware hasn&#8217;t forgotten about you. There was a recent release of version 3.0.3 for ESX which pretty much covers some vulnerabilities in the service console. The biggest piece of this patch is the fact that it will be required if you plan on obtaining upgrades after June 1, 2011. The reason for this is because the secure key RPM needs to be updated, which is included in the 3.0.3 patch bundle, more information on this can be found in <a href="http://kb.vmware.com/kb/1031235" target="_blank">KB 1031235</a>.

Here is some more information from the release notes;

Improvements included in this patch:

  * The service console RPM for krb5 is updated to krb5-libs-1.2.7-72. The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2010-1321 to the security issue that this update addresses.
  * The service console RPMs for Samba are updated to samba-3.0.9-1.3E.18vmw,
  
    samba-common-3.0.9-1.3E.18vmw, and samba-client-3.0.9-1.3E.18vmw versions. The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the names CVE -2009-2906,
  
    CVE-2010-2063, and CVE-2010-3069 to the security issues that this update addresses.
  * To continue applying patches on ESX 3.0.3 hosts, you must update the secure key RPM
  
    before June 1, 2011. This patch updates the secure key.

Detailed information regarding resolved and known issues and enhancements can be found at ESX 3.0.3 Patch Release Notes:

  * <a onclick="onClickUnsafeLink(event);" href="http://kb.vmware.com/kb/1031234" target="_blank"><span style="color: #0068cf;">http://kb.vmware.com/kb/1031234</span></a>
  * <a onclick="onClickUnsafeLink(event);" href="http://kb.vmware.com/kb/1031235" target="_blank"><span style="color: #0068cf;">http://kb.vmware.com/kb/1031235</span></a>
  * <a onclick="onClickUnsafeLink(event);" href="http://kb.vmware.com/kb/1031238" target="_blank"><span style="color: #0068cf;">http://kb.vmware.com/kb/1031238</span></a>

VMware ESX 3.0.3 Patch is available for download at <a onclick="onClickUnsafeLink(event);" href="http://www.vmware.com/patch/download/" target="_blank"><span style="color: #0068cf;">http://www.vmware.com/patch/download/</span></a>.