---
id: 3404
title: 'New VMSA-2017-0010 &#8211; vSphere Data Protection (VDP) updates address multiple security issues'
date: 2017-06-06T12:21:30+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3404
permalink: /2017/06/06/security-announce-new-vmsa-2017-0010-vsphere-data-protection-vdp-updates-address-multiple-security-issues/
redirect_from: /wp/2017/06/06/security-announce-new-vmsa-2017-0010-vsphere-data-protection-vdp-updates-address-multiple-security-issues/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "3276"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMSA-2017-0010
vSphere Data Protection (VDP) updates address multiple security issues.
VMware Security Advisory

Advisory ID:	VMSA-2017-0010
Severity:	Critical
Synopsis:	vSphere Data Protection (VDP) updates address multiple security issues.
Issue date:	2017-06-06
Updated on:	2017-06-06 (Initial Advisory)
CVE numbers:	CVE-2017-4914, CVE-2017-4917

1. Summary
vSphere Data Protection (VDP) updates address multiple security issues
2. Relevant Products
vSphere Data Protection (VDP)
3. Problem Description
a. VDP Java deserialization issue

VDP contains a deserialization issue. Exploitation of this issue may allow a remote attacker to execute commands on the appliance.

VMware would like to thank Tim Roberts, Arthur Chilipweli, and Kelly Correll from NTT Security for reporting this issue to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4914 to this issue.  

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
VDP	6.1.x	VA	Critical	6.1.4	None
VDP	6.0.x	VA	Critical	6.0.5	None
VDP	5.8.x	VA	Critical	6.0.5	None
VDP	5.5.x	VA	Critical	6.0.5	None

b. VDP locally stores vCenter Server credentials

VDP locally stores vCenter Server credentials using reversible encryption. This issue may allow plaintext credentials to be obtained.

VMware would like to thank Marc Ströbel aka phroxvs from HvS-Consulting for reporting this issue to VMware.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4917 to this issue.  

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
VDP	6.1.x	VA	Critical	6.1.4	None
VDP	6.0.x	VA	Critical	6.0.5	None
VDP	5.8.x	VA	Critical	6.0.5	None
VDP	5.5.x	VA	Critical	6.0.5	None


4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

vSphere Data Protection (VDP) 6.1.4
Downloads and Documentation:
https://my.vmware.com/group/vmware/details?productId=491&downloadGroup=VDP614
https://www.vmware.com/support/pubs/vdr_pubs.html

vSphere Data Protection (VDP) 6.0.5
Downloads and Documentation:  
https://my.vmware.com/group/vmware/details?productId=491&downloadGroup=VDP60_5
https://www.vmware.com/support/pubs/vdr_pubs.html      

5. References

http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4914  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4917  

6. Change log

2017-06-06 VMSA-2017-0010  
Initial security advisory in conjunction with the release of VMware vSphere Data Protection 6.0.5 on 2017-06-06.

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
