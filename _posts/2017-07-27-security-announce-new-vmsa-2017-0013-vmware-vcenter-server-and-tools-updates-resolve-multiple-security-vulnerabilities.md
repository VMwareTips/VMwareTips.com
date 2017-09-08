---
id: 3412
title: 'New VMSA-2017-0013 &#8211; VMware vCenter Server and Tools updates resolve multiple security vulnerabilities'
date: 2017-07-27T20:53:37+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3412
permalink: /2017/07/27/security-announce-new-vmsa-2017-0013-vmware-vcenter-server-and-tools-updates-resolve-multiple-security-vulnerabilities/
redirect_from: /wp/2017/07/27/security-announce-new-vmsa-2017-0013-vmware-vcenter-server-and-tools-updates-resolve-multiple-security-vulnerabilities/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1833"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMSA-2017-0013
VMware vCenter Server and Tools updates resolve multiple  security vulnerabilities
VMware Security Advisory

Advisory ID:	VMSA-2017-0013
Severity:	Moderate
Synopsis:	VMware vCenter Server and Tools updates resolve multiple security vulnerabilities
Issue date:	2017-07-27
Updated on:	2017-07-27 (Initial Advisory)
CVE numbers:	CVE-2017-4921, CVE-2017-4922, CVE-2017-4923, CVE-2015-5191

1. Summary
VMware vCenter Server and Tools updates resolve multiple security vulnerabilities
2. Relevant Products
VMware vCenter Server  
VMware Tools
3. Problem Description
a. Insecure library loading through LD_LIBRARY_PATH  

VMware vCenter Server contains an insecure library loading issue that occurs due to the use of LD_LIBRARY_PATH variable in an unsafe manner. Successful exploitation of this issue may allow unprivileged host users to load a shared library that may lead to privilege escalation.      

Note: In order to exploit this issue an attacker should be able to trick the admin to execute wrapper scripts from a world writable directory.      

VMware would like to thank Thorsten Tüllmann, researcher at Karlsruhe Institute of Technology for reporting this issue to us.     

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4921 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
vCenter Server	6.5	VA	Moderate	6.5 U1	None
vCenter Server	6.5	Windows	N/A	Not affected	N/A
vCenter Server	6.0	Any	N/A	Not affected	N/A
vCenter Server	5.5	Any	N/A	Not affected	N/A


b. Information disclosure via service startup script

VMware vCenter Server contains an information disclosure issue due to the service startup script using world writable directories as temporary storage for critical information. Successful exploitation of this issue may allow unprivileged host users to access certain critical information when the service gets restarted.     

VMware would like to thank Thorsten Tüllmann, researcher at Karlsruhe Institute of Technology for reporting this issue to us.     

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4922 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
vCenter Server	6.5	VA	Moderate	6.5 U1	None
vCenter Server	6.5	Windows	N/A	Not affected	N/A
vCenter Server	6.0	Any	N/A	Not affected	N/A
vCenter Server	5.5	Any	N/A	Not affected	N/A


c. Information disclosure via vCenter Server Appliance file-based backup feature

VMware vCenter Server contains an information disclosure vulnerability. This issue may allow plaintext credentials to be obtained when using the vCenter Server Appliance file-based backup feature.      

VMware would like to thank Joe Womack of Expedia for reporting this issue to us.

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4923 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
vCenter Server	6.5	VA	Moderate	6.5 U1	None
vCenter Server	6.5	Windows	N/A	Not affected	N/A
vCenter Server	6.0	Any	N/A	Not affected	N/A
vCenter Server	5.5	Any	N/A	Not affected	N/A


d. Local privilege escalation in VMware Tools

VMware Tools contains multiple file system races in libDeployPkg, related to the use of hard-coded paths under /tmp. Successful exploitation of this issue may result in a local privilege escalation.      

VMware would like to thank Florian Weimer and Kurt Seifried of Red Hat Product Security for reporting this issue to us.     

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2015-5191 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Workaround
VMware Tools	10.0.x, 9.x	Linux	Moderate	10.0.9 and above	None


4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

VMware vCenter Server 6.5 U1
Downloads:
https://my.vmware.com/web/vmware/details?downloadGroup=VC65U1&productId=614&rPId=17343
Documentation:
https://docs.vmware.com/en/VMware-vSphere/index.html

VMware Tools 10.0.9
Downloads and Documentation:  
        https://my.vmware.com/web/vmware/details?productId=491&
        downloadGroup=VMTOOLS1009

5. References

          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4921  
          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4922  
          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4923  
          http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5191

6. Change log

2017-07-27 VMSA-2017-0013  
Initial security advisory in conjunction with the release of VMware vCenter Server 6.5 U1 on 2017-07-27.

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

VMware Security & Compliance Blog  
https://blogs.vmware.com/security

Twitter
https://twitter.com/VMwareSRC
