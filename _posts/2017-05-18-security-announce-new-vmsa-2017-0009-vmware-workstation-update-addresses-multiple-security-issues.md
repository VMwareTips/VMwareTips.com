---
id: 3400
title: 'New VMSA-2017-0009 &#8211; VMware Workstation update addresses multiple security issues'
date: 2017-05-18T22:55:42+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3400
permalink: /2017/05/18/security-announce-new-vmsa-2017-0009-vmware-workstation-update-addresses-multiple-security-issues/
redirect_from: /wp/2017/05/18/security-announce-new-vmsa-2017-0009-vmware-workstation-update-addresses-multiple-security-issues/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "2472"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMSA-2017-0009
VMware Workstation update addresses multiple security        issues
VMware Security Advisory

Advisory ID:	VMSA-2017-0009
Severity:	Important
Synopsis:	VMware Workstation update addresses multiple security issues
Issue date:	2017-05-18
Updated on:	2017-05-18 (Initial Advisory)
CVE numbers:	CVE-2017-4915, CVE-2017-4916

1. Summary
VMware Workstation update addresses multiple security issues
2. Relevant Products
VMware Workstation Pro/Player
3. Problem Description
a. VMware Workstation Insecure library loading vulnerability   

VMware Workstation Pro/Player contains an insecure library loading vulnerability via ALSA sound driver configuration files. Successful exploitation of this issue may allow unprivileged host users to escalate their privileges to root in a Linux host machine.    

VMware would like to thank Jann Horn of Google Project Zero for reporting this issue to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4915 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.

VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
VMware Workstation Pro	12.x	Linux	Important	12.5.6	None
VMware Workstation Player	12.x	Linux	Important	12.5.6	None


b. VMware Workstation NULL pointer dereference vulnerability  

VMware Workstation Pro/Player contains a NULL pointer dereference vulnerability that exists in the vstor2 driver. Successful exploitation of this issue may allow host users with normal user privileges to trigger a denial-of-service in a Windows host machine.  

VMware would like to thank Borja Merino for reporting this issue to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4916 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
VMware Workstation Pro	12.x	Windows	Moderate	12.5.6	None
VMware Workstation Player	12.x	Windows	Moderate	12.5.6	None


4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

VMware Workstation Pro 12.5.6  
Downloads and Documentation:
https://www.vmware.com/go/downloadworkstation
https://www.vmware.com/support/pubs/ws_pubs.html   

VMware Workstation Player 12.5.6   
Downloads and Documentation:  
https://www.vmware.com/go/downloadplayer
https://www.vmware.com/support/pubs/player_pubs.html

5. References

          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4915
          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4916

6. Change log

2017-05-18 VMSA-2017-0009 Initial security advisory in conjunction with the release of VMware Workstation Pro/Player 12.5.6 on 2017-05-18.

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
