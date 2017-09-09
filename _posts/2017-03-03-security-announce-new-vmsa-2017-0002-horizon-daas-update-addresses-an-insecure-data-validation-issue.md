---
id: 3370
title: 'New VMSA-2017-0002 Horizon DaaS update addresses an insecure data validation issue'
date: 2017-03-03T01:02:10+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3370
permalink: /2017/03/03/security-announce-new-vmsa-2017-0002-horizon-daas-update-addresses-an-insecure-data-validation-issue/
redirect_from: /wp/2017/03/03/security-announce-new-vmsa-2017-0002-horizon-daas-update-addresses-an-insecure-data-validation-issue/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1496"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMSA-2017-0002
Horizon DaaS update addresses an insecure data validation issue
VMware Security Advisory

Advisory ID:	VMSA-2017-0002
Severity:	Moderate
Synopsis:	Horizon DaaS update addresses an insecure data validation issue
Issue date:	2017-03-02
Updated on:	2017-03-02 (Initial Advisory)
CVE numbers:	CVE-2017-4897

1. Summary
   Horizon DaaS update addresses an insecure data validation issue
2. Relevant Products
VMware Horizon DaaS
3. Problem Description
a. Horizon DaaS insecure data validation

Horizon DaaS contains a vulnerability that exists due to insufficient validation of data. An attacker may exploit this issue by tricking DaaS client users into connecting to a malicious server and sharing all their drives and devices. Successful exploitation of this vulnerability requires a victim to download a specially crafted RDP file through DaaS client by clicking on a malicious link.       

VMware would like to thank Ahmad Ashraff of Aura Information Security for reporting this issue to us.   

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4897 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
Horizon DaaS	6.1.x	All	Moderate	7.0.0	None

4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

VMware Horizon DaaS   
Downloads:
https://my.vmware.com/web/vmware/info/slug/desktop_end_user_computing/vmware_horizon_daas/7_0
Documentation:   
https://www.vmware.com/support/pubs/horizon-daas-platform-pubs.html

5. References
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4897

6. Change log

2017-03-02 VMSA-2017-0002 Initial security advisory in conjunction with the release of VMware Horizon DaaS 7.0.0 on 2017-03-02.

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
