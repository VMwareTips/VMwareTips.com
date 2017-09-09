---
id: 3410
title: 'New VMSA-2017-0012 &#8211; VMware VIX API VM Direct Access Function security issue'
date: 2017-07-27T10:53:21+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3410
permalink: /2017/07/27/security-announce-new-vmsa-2017-0012-vmware-vix-api-vm-direct-access-function-security-issue/
redirect_from: /wp/2017/07/27/security-announce-new-vmsa-2017-0012-vmware-vix-api-vm-direct-access-function-security-issue/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1742"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMSA-2017-0012
VMware VIX API VM Direct Access Function security issue
VMware Security Advisory

Advisory ID:	VMSA-2017-0012
Severity:	Important
Synopsis:	VMware VIX API VM Direct Access Function security issue
Issue date:	2017-07-27
Updated on:	2017-07-27 (Initial Advisory)
CVE numbers:	CVE-2017-4919

1. Summary
VMware VIX API allows for direct access to Guest Operating Systems (Guest OSs) by vSphere users with limited privileges.
2. Relevant Products
VMware vCenter Server
3. Problem Description
VMware VIX API VM Direct Access Function security issue  

The VMware VIX API has a functionality that allows for direct access to Guests OSs which is used by VMware Site Recovery Manager, VMware Update Manager, and VMware Infrastructure Navigator to manage Guest OSs. This functionality may be used by vSphere users with limited privileges to access a Guest OS without the need to authenticate.      

In order for vSphere users with limited privileges to use this functionality, they would need to have all three of the following privileges:         
               Virtual Machine -> Configuration -> Advanced            
               Virtual Machine -> Interaction ->                      
                                         Guest Operating System Management by VIX API                   
               Host -> Configuration -> Advanced Settings  

Workaround  
Workarounds that remove the direct access to Guest OSs by vSphere users with limited privileges are listed in VMware Knowledge Base article 2151027.  
These workarounds are not relevant for vSphere users that are fully privileged. Typically they already have alternate ways to access Guest OSs.  

VMware would like to thank Ofri Ziv and Itamar Tal of Guardicore for reporting this issue to us.  

The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2017-4919 to this issue.

Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
VMware Product
Product Version
Running on
Severity
Replace with/ Apply Patch
Mitigation/ Workaround
vCenter Server	6.5	Any	Important	N/A	KB 2151027
vCenter Server	6.0	Any	Important	N/A	KB 2151027
vCenter Server	5.5	Any	Important	N/A	KB 2151027

4. Solution

Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.

Apply the workaround listed in VMware Knowledge Base article 2151027.  

5. References

http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4919

VMware Knowledge Base article 2151027
https://kb.vmware.com/kb/2151027

6. Change log

2017-07-27 VMSA-2017-0012   
Initial security advisory providing a workaround on 2017-07-27.

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
