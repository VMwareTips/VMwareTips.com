---
id: 3396
title: 'Updated VMSA-2017-0008.2-VMware Unified Access Gateway, Horizon View and Workstation updates resolve multiple security vulnerabilities'
date: 2017-04-19T13:21:20+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3396
permalink: /2017/04/19/security-announce-updated-vmsa-2017-0008-2-vmware-unified-access-gateway-horizon-view-and-workstation-updates-resolve-multiple-security-vulnerabilities/
redirect_from: /wp/2017/04/19/security-announce-updated-vmsa-2017-0008-2-vmware-unified-access-gateway-horizon-view-and-workstation-updates-resolve-multiple-security-vulnerabilities/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "2126"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMSA-2017-0008.2
VMware Unified Access Gateway, Horizon View and Workstation updates resolve multiple security vulnerabilities
VMware Security Advisory

Advisory ID:	VMSA-2017-0008.2
Severity:	Critical
Synopsis:	VMware Unified Access Gateway, Horizon View and Workstation updates resolve multiple security vulnerabilities
Issue date:	2017-04-18
Updated on:	2017-04-21
CVE numbers:	CVE-2017-4907, CVE-2017-4908, CVE-2017-4909, CVE-2017-4910, CVE-2017-4911, CVE-2017-4912, CVE-2017-4913

1. Summary
VMware Unified Access Gateway, Horizon View and Workstation updates resolve multiple security vulnerabilities
2. Relevant Products
VMware Unified Access Gateway (formerly called Access Point)  
VMware Horizon View      
VMware Horizon View Client for Windows
VMware Workstation Pro / Player (Workstation)
3. Problem Description
a. Unified Access Gateway and Horizon View heap buffer-overflow vulnerability

VMware Unified Access Gateway and Horizon View contain a heap buffer-overflow vulnerability which may allow a remote attacker to execute code on the security gateway.

VMware would like to thank Claudio Moletta (redr2e) for reporting this issue to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4907 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
Unified Access Gateway*	2.9.x	N/A	Not affected	N/A	N/A
Unified Access Gateway*	2.8.x, 2.7.x, 2.5.x	Any	Critical	2.8.1	None
Horizon View	7.x	Any	Critical	7.1.0	None
Horizon View	6.x	Any	Critical	6.2.4	None

*Formerly called Access Point.

b. Multiple heap-based buffer overflow issues via Cortado ThinPrint

VMware Workstation and Horizon View Client contain multiple heap buffer-overflow vulnerabilities in JPEG2000 and TrueType Font (TTF) parsers in the TPView.dll. On Workstation, this may allow a guest to execute code or perform a Denial of Service on the Windows OS that runs Workstation. In the case of a Horizon View Client, this may    allow a View desktop to execute code or perform a Denial of Service on the Windows OS that runs the Horizon View Client.

Exploitation is only possible if virtual printing has been enabled. This feature is not enabled by default on Workstation but it is enabled by default on Horizon View.

VMware would like to thank Ke Liu of Tencent's Xuanwu Lab and Gogil of STEALIEN working with ZDI for reporting these issues to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifiers CVE-2017-4908 (JPEG2000) and CVE-2017-4909 (TTF) to these issues.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
Horizon View Client for Windows	4.x	Windows	Critical	4.4.0	None
Workstation	12.x	Windows	Critical	12.5.3	None


c. Multiple out-of-bounds read/write issues via Cortado ThinPrint

VMware Workstation and Horizon View Client contain multiple out-of-bounds read/write vulnerabilities in JPEG2000 and TrueType Font (TTF) parsers in the TPView.dll. On Workstation, this may allow a guest to execute code or perform a Denial of Service on the Windows OS that runs Workstation. In the case of a Horizon View Client, this may allow a View desktop to execute code or perform a Denial of Service on the Windows OS that runs the Horizon View Client.

Exploitation is only possible if virtual printing has been enabled. This feature is not enabled by default on Workstation but it is enabled by default on Horizon View.

VMware would like to thank Ke Liu of Tencent's Xuanwu Lab and Giwan Go of STEALIEN working with ZDI for reporting these issues to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifiers CVE-2017-4910 (JPEG2000), CVE-2017-4911 (JPEG2000) and CVE-2017-4912 (TTF) to these issues.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
Horizon View Client for Windows	4.x	Windows	Critical	4.4.0	None
Workstation	12.x	Windows	Critical	12.5.3	None


d. Integer overflow vulnerability via Cortado ThinPrint

VMware Workstation and Horizon Client contain an integer-overflow vulnerability in the True Type Font parser in the TPView.dll. On Workstation, this may allow a guest to execute code or perform a Denial of Service on the Windows OS that runs Workstation. In the case of a Horizon View Client, this may allow a View desktop to execute  code or perform a Denial of Service on the Windows OS that runs the Horizon View Client.

Exploitation is only possible if virtual printing has been enabled. This feature is not enabled by default on Workstation but it is enabled by default on Horizon View.

VMware would like to thank Ke Liu of Tencent's Xuanwu Lab for reporting this issue to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4913 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
Horizon View Client for Windows	4.x	Windows	Critical	4.4.0	None
Workstation	12.x	Windows	Critical	12.5.3	None


4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

VMware Unified Access Gateway 2.9  
Downloads and Documentation:
https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-APPS-710-ADV&productId=643&rPId=15408    
http://pubs.vmware.com/accesspoint-29/index.jsp       

VMware Unified Access Gateway 2.8.1
Downloads and Documentation:  
https://my.vmware.com/group/vmware/details?downloadGroup=VIDM_ONPREM_28&productId=577&rPId=13519
http://pubs.vmware.com/accesspoint-28/index.jsp        

VMware Horizon View 7.1.0
Downloads and Documentation:  
https://my.vmware.com/web/vmware/info/slug/desktop_end_user_computing/vmware_horizon/7_1
https://www.vmware.com/support/pubs/view_pubs.html       

VMware Horizon View 6.2.4  
Downloads and Documentation:  
https://my.vmware.com/web/vmware/info/slug/desktop_end_user_computing/vmware_horizon/6_2
https://www.vmware.com/support/pubs/view_pubs.html

VMware Workstation Pro 12.5.3  
Downloads and Documentation:  
https://www.vmware.com/go/downloadworkstation  
https://www.vmware.com/support/pubs/ws_pubs.html  

VMware Workstation Player 12.5.3  
Downloads and Documentation:  
https://www.vmware.com/go/downloadplayer  
https://www.vmware.com/support/pubs/player_pubs.html

VMware Horizon View Client 4.4.0
Downloads and Documentation:
https://my.vmware.com/web/vmware/info/slug/desktop_end_user_computing/vmware_horizon_clients/4_0
5. References

http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4907  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4908  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4909  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4910  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4911  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4912  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4913

6. Change log

2017-04-18 VMSA-2017-0008  
Initial security advisory in conjunction with the release of VMware Horizon View 6.2.4 on 2017-04-18.

2017-04-19 VMSA-2017-0008.1
Corrected the VMware Horizon View Client for Windows version.

2017-04-21 VMSA-2017-0008.2
Updated security advisory to clarify the Unified Access Gateway and Horizon View affected versions.

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
