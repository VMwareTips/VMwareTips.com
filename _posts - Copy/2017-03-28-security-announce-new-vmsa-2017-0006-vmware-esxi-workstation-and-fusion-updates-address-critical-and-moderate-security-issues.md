---
id: 3388
title: 'New VMSA-2017-0006 VMware ESXi, Workstation and Fusion updates address critical and moderate security issues'
date: 2017-03-28T09:38:21+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3388
permalink: /2017/03/28/security-announce-new-vmsa-2017-0006-vmware-esxi-workstation-and-fusion-updates-address-critical-and-moderate-security-issues/
redirect_from: /wp/2017/03/28/security-announce-new-vmsa-2017-0006-vmware-esxi-workstation-and-fusion-updates-address-critical-and-moderate-security-issues/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "2350"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMSA-2017-0006
VMware ESXi, Workstation and Fusion updates address critical and moderate security issues
VMware Security Advisory

Advisory ID:	VMSA-2017-0006
Severity:	Critical
Synopsis:	VMware ESXi, Workstation and Fusion updates address critical and moderate security issues
Issue date:	2017-03-28
Updated on:	2017-03-28 (Initial Advisory)
CVE numbers:	CVE-2017-4902, CVE-2017-4903, CVE-2017-4904, CVE-2017-4905

1. Summary
   VMware ESXi, Workstation and Fusion updates address critical and moderate
   security issues.
2. Relevant Products
VMware ESXi (ESXi)  
VMware Workstation Pro / Player (Workstation)  
VMware Fusion Pro, Fusion (Fusion)
3. Problem Description
a. ESXi, Workstation, Fusion SVGA memory corruption

ESXi, Workstation, Fusion have a heap buffer overflow and uninitialized stack memory usage in SVGA. These issues may allow a guest to execute code on the host.

VMware would like to thank ZDI and Team 360 Security from Qihoo for reporting these issues to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifiers CVE-2017-4902 (heap issue) and CVE-2017-4903 (stack issue) to these issues.

Note: ESXi 6.0 is affected by CVE-2017-4903 but not by CVE-2017-4902.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
ESXi	6.5	ESXi	Critical	ESXi650-201703410-SG	None
ESXi	6.0 U3	ESXi	Critical	ESXi600-201703401-SG	None
ESXi	6.0 U2*	ESXi	Critical	KB 2149673	None
ESXi	6.0 U1*	ESXi	Critical	KB 2149672	None
ESXi	5.5	ESXi	N/A	Not affected	N/A
Workstation	12.x	Any	Critical	12.5.5	None
Fusion	8.x	OSX	Critical	8.5.6	None

* Additional ESXi 6.0 patches are provided for customers that are on ESXi 6.0 U1 or ESXi 6.0 U2.

b. ESXi, Workstation, Fusion XHCI uninitialized memory usage

The ESXi, Workstation, and Fusion XHCI controller has uninitialized memory usage. This issue may allow a guest to execute code on the host. The issue is reduced to a Denial of Service of the guest on ESXi 5.5.

VMware would like to thank ZDI and Team Sniper from Tencent Security for reporting this issue to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4904 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
ESXi	6.5	ESXi	Critical	ESXi650-201703410-SG	None
ESXi	6.0 U3	ESXi	Critical	ESXi600-201703401-SG	None
ESXi	6.0 U2*	ESXi	Critical	KB 2149673	None
ESXi	6.0 U1*	ESXi	Critical	KB 2149672	None
ESXi	5.5	ESXi	Moderate	ESXi550-201703401-SG	None
Workstation	12.x	Any	Critical	12.5.5	None
Fusion	8.x	OSX	Critical	8.5.6	None

* Additional ESXi 6.0 patches are provided for customers that are on ESXi 6.0 U1 or ESXi 6.0 U2.

c. ESXi, Workstation, and Fusion uninitialized memory usage

ESXi, Workstation, and Fusion have uninitialized memory usage. This issue may lead to an information leak.   

VMware would like to thank ZDI and Team Sniper from Tencent Security for reporting this issue to us.  

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4905 to this issue.  

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
ESXi	6.5	ESXi	Moderate	ESXi650-201703410-SG	None
ESXi	6.0 U3	ESXi	Moderate	ESXi600-201703401-SG	None
ESXi	6.0 U2*	ESXi	Moderate	KB 2149673	None
ESXi	6.0 U1*	ESXi	Moderate	KB 2149672	None
ESXi	5.5	ESXi	Moderate	ESXi550-201703401-SG	None
Workstation	12.x	Any	Moderate	12.5.5	None
Fusion	8.x	OSX	Moderate	8.5.6	None

* Additional ESXi 6.0 patches are provided for customers that are on ESXi 6.0 U1 or ESXi 6.0 U2.

4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

VMware ESXi 6.5  
Downloads:  
https://my.vmware.com/group/vmware/patch
Documentation:  
http://kb.vmware.com/kb/2149573

VMware ESXi 6.0 patch on top of ESXi 6.0 U3
Downloads:
https://my.vmware.com/group/vmware/patch
Documentation:   
http://kb.vmware.com/kb/2149569

VMware ESXi 6.0 patch on top of ESXi 6.0 U2  
Downloads:  
https://my.vmware.com/web/vmware/details?productId=491&downloadGroup=ESXI60U2  
(Click on the above link and scroll down to ESXi600-201703003 Offline Bundle)
Documentation:  
http://kb.vmware.com/kb/2149673  

VMware ESXi 6.0 patch on top of ESXi 6.0 U1  
Downloads:  
https://my.vmware.com/web/vmware/details?productId=491&downloadGroup=ESXI60U1B
(Click on the above link and scroll down to ESXi600-201703002 Offline Bundle)
Documentation:  
http://kb.vmware.com/kb/2149672

VMware ESXi 5.5   
Downloads:
https://my.vmware.com/group/vmware/patch
Documentation:   
http://kb.vmware.com/kb/2149577

VMware Workstation Pro 12.5.5
Downloads and Documentation:  
https://www.vmware.com/go/downloadworkstation  
https://www.vmware.com/support/pubs/ws_pubs.html  

VMware Workstation Player 12.5.5  
Downloads and Documentation:  
https://www.vmware.com/go/downloadplayer  
https://www.vmware.com/support/pubs/player_pubs.html

VMware Fusion Pro / Fusion 8.5.6  
Downloads and Documentation:  
https://www.vmware.com/go/downloadfusion  
https://www.vmware.com/support/pubs/fusion_pubs.html

5. References
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4902  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4903  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4904  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4905

VMware Knowledge Base article 2149673  
http://kb.vmware.com/kb/2149673

VMware Knowledge Base article 2149672  
http://kb.vmware.com/kb/2149672

6. Change log

2017-03-28 VMSA-2017-0006  
Initial security advisory in conjunction with the release of ESXi patches and VMware Workstation Pro/Player 12.5.5 and VMware Fusion Pro, Fusion 8.5.6 on 2017-03-28.

7. Contact

E-mail list for product security notifications and announcements:
http://lists.vmware.com/cgi-bin/mailman/listinfo/security-announce

This Security Advisory is posted to the following lists:
security-announce@lists.vmware.com
bugtraq@securityfocus.com
fulldisclosure@seclists.org

E-mail: security@vmware.com
PGP key at:
https://kb.vmware.com/kb/1055

VMware Security Advisories
http://www.vmware.com/security/advisories

VMware Security Response Policy
https://www.vmware.com/support/policies/security_response.html

VMware Lifecycle Support Phases
https://www.vmware.com/support/policies/lifecycle.html

VMware Security & Compliance Blog  
https://blogs.vmware.com/security

Twitter
https://twitter.com/VMwareSRC
