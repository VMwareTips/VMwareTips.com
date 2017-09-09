---
id: 3372
title: 'New VMSA-2017-0003 VMware Workstation update addresses multiple security issues'
date: 2017-03-09T21:49:13+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3372
permalink: /2017/03/09/security-announce-new-vmsa-2017-0003-vmware-workstation-update-addresses-multiple-security-issues/
redirect_from: /wp/2017/03/09/security-announce-new-vmsa-2017-0003-vmware-workstation-update-addresses-multiple-security-issues/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1465"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---

VMSA-2017-0003
VMware Workstation update addresses multiple security         issues
VMware Security Advisory

Advisory ID:	VMSA-2017-0003
Severity:	Important
Synopsis:	VMware Workstation update addresses multiple security issues
Issue date:	2017-03-09
Updated on:	2017-03-09 (Initial Advisory)
CVE numbers:	CVE-2017-4898, CVE-2017-4899, CVE-2017-4900

1. Summary
VMware Workstation update addresses multiple security issues
2. Relevant Products
VMware Workstation Pro/Player
3. Problem Description
a. VMware Workstation DLL loading vulnerability   

VMware Workstation Pro/Player contains a DLL loading vulnerability that occurs due to the "vmware-vmx" process loading DLLs from a path defined in the local environment-variable. Successful exploitation of this issue may allow normal users to escalate privileges to System in the host machine where VMware Workstation is installed.       

VMware would like to thank Ivil for reporting this issue to us.   

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4898 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.

VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
VMware Workstation Pro	12.x	Windows	Important	12.5.3	None
VMware Workstation Player	12.x	Windows	Important	12.5.3	None


b. VMware Workstation SVGA driver vulnerability    

VMware Workstation Pro/Player contains a security vulnerability that exists in the SVGA driver. An attacker may exploit this issue to crash the VM or trigger an out-of-bound read.       

Note: This issue can be triggered only when the host has no graphics card or no graphics drivers are installed.       

VMware would like to thank Marco Grassi (@marcograss) of KeenLab (@keen_lab) Tencent for reporting this issue to us. The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4899 to this issue.  

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
VMware Workstation Pro	12.x	Windows	Moderate	12.5.3	None
VMware Workstation Player	12.x	Windows	Moderate	12.5.3	None


c. VMware Workstation NULL pointer dereference vulnerability  

VMware Workstation Pro/Player contains a NULL pointer dereference vulnerability that exists in the SVGA driver. Successful exploitation of this issue may allow attackers with normal user privileges to crash their VMs.      

VMware would like to thank Saar Amar (@AmarSaar) for reporting this issue to us. The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4900 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
VMware Workstation Pro	12.x	Windows	Moderate	12.5.3	None
VMware Workstation Player	12.x	Windows	Moderate	12.5.3	None


4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

VMware Workstation Pro 12.5.3  
Downloads and Documentation:
https://www.vmware.com/go/downloadworkstation
https://www.vmware.com/support/pubs/ws_pubs.html   

VMware Workstation Player 12.5.3    
Downloads and Documentation:  
https://www.vmware.com/go/downloadplayer
https://www.vmware.com/support/pubs/player_pubs.html

5. References

          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4898  
          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4899
          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4900

6. Change log

2017-03-09 VMSA-2017-0003 Initial security advisory in conjunction with the release of VMware Workstation Pro/Player 12.5.3 on  2017-03-09.

7. Contact

E-mail list for product security notifications and announcements:
http://lists.vmware.com/cgi-bin/mailman/listinfo/security-announce

This Security Advisory is posted to the following lists:
security-announce@lists.vmware.com
bugtraq@securityfocus.com
fulldisclosure@seclists.org

E-mail: security@vmware.com
PGP key at: https://kb.vmware.com/kb/1055

VMware Security Advisories
http://www.vmware.com/security/advisories

Consolidated list of VMware Security Advisories
http://kb.vmware.com/kb/2078735

VMware Security Response Policy
https://www.vmware.com/support/policies/security_response.html

VMware Lifecycle Support Phases
https://www.vmware.com/support/policies/lifecycle.html

Twitter
https://twitter.com/VMwareSRC
