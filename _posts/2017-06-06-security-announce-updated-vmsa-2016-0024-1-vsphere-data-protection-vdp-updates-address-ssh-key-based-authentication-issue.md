---
id: 3402
title: 'Updated VMSA-2016-0024.1 &#8211; vSphere Data Protection (VDP) updates address SSH Key-Based authentication issue'
date: 2017-06-06T12:21:28+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3402
permalink: /2017/06/06/security-announce-updated-vmsa-2016-0024-1-vsphere-data-protection-vdp-updates-address-ssh-key-based-authentication-issue/
redirect_from: /wp/2017/06/06/security-announce-updated-vmsa-2016-0024-1-vsphere-data-protection-vdp-updates-address-ssh-key-based-authentication-issue/
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
VMSA-2016-0024.1
vSphere Data Protection (VDP) updates address SSH Key-Based authentication issue
VMware Security Advisory

Advisory ID:	VMSA-2016-0024.1
Severity:	Critical
Synopsis:	vSphere Data Protection (VDP) updates address SSH Key-Based authentication issue
Issue date:	2016-12-20
Updated on:	2017-06-06
CVE numbers:	CVE-2016-7456

1. Summary
vSphere Data Protection (VDP) updates address SSH key-based authentication issue
2. Relevant Products
vSphere Data Protection (VDP)
3. Problem Description
VDP SSH key-based authentication issue

VDP contains a private SSH key with a known password that is configured to allow key-based authentication. Exploitation of this issue may allow an unauthorized remote attacker to log into the appliance with root privileges.

VMware would like to thank Marc Ströbel aka phroxvs from HvS-Consulting for reporting this issue to VMware.  

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-7456 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
VDP	6.1.x	VA	Critical	6.1.4	KB2147069
VDP	6.0.x	VA	Critical	6.0.5	KB2147069
VDP	5.8.x	VA	Critical	KB2147069	None
VDP	5.5.x	VA	Critical	KB2147069	None

4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

vSphere Data Protection 6.1.4  
Downloads and Documentation:  
https://my.vmware.com/group/vmware/details?productId=491&downloadGroup=VDP614   https://www.vmware.com/support/pubs/vdr_pubs.html  

vSphere Data Protection 6.0.5  
Downloads and Documentation:  
https://my.vmware.com/group/vmware/details?productId=491&downloadGroup=VDP60_5   https://www.vmware.com/support/pubs/vdr_pubs.html  

vSphere Data Protection 5.8.x & 5.5.x  
Downloads and Documentation:  
http://kb.vmware.com/kb/2147069

5. References
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7456
6. Change log

2016-12-20: VMSA-2016-0024
Initial security advisory in conjunction with the release of vSphere Data Protection updates on 2016-12-20.

2017-06-06: VMSA-2016-0024.1
Security advisory update in conjunction with the release of vSphere Data Protection 6.0.5 fixes.

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

Twitter
https://twitter.com/VMwareSRC
