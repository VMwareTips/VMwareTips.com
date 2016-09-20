---
id: 1887
title: '[Security-announce] VMSA-2012-0016 VMware security updates for vSphere API and ESX Service Console'
date: 2012-12-20T10:32:47+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1887
permalink: /2012/12/20/security-announce-vmsa-2012-0016-vmware-security-updates-for-vsphere-api-and-esx-service-console/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 640
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
In our effort to provide our viewers with up to the minute information on VMware related news and topics, we’re posting the following Security Alert direct from the VMware Security Alert distribution.

<!--more-->

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;
  
**VMware Security Advisory**

Advisory ID:  VMSA-2012-0016
  
Synopsis:     VMware security updates for vSphere API and ESX Service Console
  
Issue date:   2012-11-15
  
Updated on:   2012-11-15 (initial advisory)
  
CVE numbers:

&#8212; vSphere API &#8212;
  
CVE-2012-5703

&#8212; bind (service console) &#8212;
  
CVE-2012-1033, CVE-2012-1667, CVE-2012-3817
  
</wbr></wbr>

&#8212; python (service console) &#8212;
  
CVE-2011-4940, CVE-2011-4944, CVE-2012-1150

&#8212; expat (service console) &#8212;
  
CVE-2012-0876, CVE-2012-1148

&#8212; nspr and nss (service console) &#8212;
  
CVE-2012-0441
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

**1. Summary**

VMware has updated the vSphere API to address a denial of service
  
vulnerability in ESX and ESXi.  VMware has also updated the ESX
  
Service Console to include several open source security updates.

**2. Relevant releases**

  * VMware ESXi 4.1 without patch ESXi410-201211401-SG
  * VMware ESX 4.1 without patches ESX410-201211401-SG, ESX410-201211402-SG, ESX410-201211405-SG, and ESX410-201211407-SG

**3. Problem Description**

a. VMware vSphere API denial of service vulnerability

The VMware vSphere API contains a denial of service
  
vulnerability.  This issue allows an unauthenticated user to
  
send a maliciously crafted API request and disable the host
  
daemon. Exploitation of the issue would prevent management
  
activities on the host but any virtual machines running on the
  
host would be unaffected.

VMware would like to thank Sebastian Tello of Core Security
  
Technologies for reporting this issue to us.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the name CVE-2012-5703 to this issue.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware         Product   Running   Replace with/
  
Product        Version   on        Apply Patch
  
=============  ========  =======   =================
  
vCenter        any       any       not affected

ESXi           5.1       ESXi      not affected
  
ESXi           5.0       ESXi      not affected
  
ESXi           4.1       ESXi      ESXi410-201211401-SG
  
ESXi           4.0       ESXi      not affected
  
ESXi           3.5       ESXi      not affected

ESX            4.1       ESX       ESX410-201211401-SG
  
ESX            4.0       ESX       not affected
  
ESX            3.5       ESX       not affected

b. Update to ESX service console bind packages

The ESX service console bind packages are updated to the
  
following versions:

bind-libs-9.3.6-20.P1.el5_8.2
  
bind-utils-9.3.6-20.P1.el5_8.2

These updates fix multiple security issues. The Common
  
Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>) has
  
assigned the names CVE-2012-1033, CVE-2012-1667, and
  
CVE-2012-3817 to these issues.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware         Product   Running   Replace with/
  
Product        Version   on        Apply Patch
  
=============  ========  =======   =================
  
ESXi           any       ESXi      not affected

ESX            4.1       ESX       ESX410-201211402-SG
  
ESX            4.0       ESX       patch pending
  
ESX            3.5       ESX       not applicable

c. Update to ESX service console python packages

The ESX service console Python packages are updated to the
  
following versions:

python-2.4.3-46.el5\_8.2.x86\_64
  
python-libs-2.4.3-46.el5\_8.2.x86\_64

These updates fix multiple security issues. The Common
  
Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>) has
  
assigned the names CVE-2011-4940, CVE-2011-4944, and
  
CVE-2012-1150 to these issues.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware         Product   Running   Replace with/
  
Product        Version   on        Apply Patch
  
=============  ========  =======   =================
  
ESXi           any       ESXi      not affected

ESX            4.1       ESX       ESX410-201211407-SG
  
ESX            4.0       ESX       no patch planned
  
ESX            3.5       ESX       not applicable

d. Update to ESX service console expat package

The ESX service console expat package is updated to
  
expat-1.95.8-11.el5_8.

This update fixes multiple security issues. The Common
  
Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>) has
  
assigned the names CVE-2012-0876 and CVE-2012-1148 to these
  
issues.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware         Product   Running   Replace with/
  
Product        Version   on        Apply Patch
  
=============  ========  =======   =================
  
ESXi           any       ESXi      not affected

ESX            4.1       ESX       ESX410-201211407-SG
  
ESX            4.0       ESX       no patch planned
  
ESX            3.5       ESX       not applicable

e. Update to ESX service console nspr and nss packages

This patch updates the ESX service console Netscape Portable
  
Runtime and Network Security Services RPMs to versions
  
nspr-4.9.1.4.el5_8 and nss-3.13.5.4.9834, respectively, to
  
resolve multiple security issues.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the name CVE-2012-0441 to this issue. This patch
  
also resolves a certificate trust issue caused by a fraudulent
  
DigiNotar root certificate.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware         Product   Running   Replace with/
  
Product        Version   on        Apply Patch
  
=============  ========  =======   =================
  
ESXi           any       ESXi      not affected

ESX            4.1       ESX       ESX410-201211405-SG
  
ESX            4.0       ESX       patch pending
  
ESX            3.5       ESX       not applicable

**4. Solution**

Please review the patch/release notes for your product and
  
version and verify the checksum of your downloaded file.

ESXi and ESX
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
<a href="http://downloads.vmware.com/go/selfsupport-download" target="_blank">http://downloads.vmware.com/go/selfsupport-download</a>

ESXi 4.1
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
Filename: ESXi410-201211001.zip
  
Build:    874690
  
md5sum:   f7da5cd52d3c314abc31fe7aef4e50d3
  
sha1sum:  a4d2232723717d896ff3b0879b0bdb3db823c0a1
  
<a href="http://kb.vmware.com/kb/2036257" target="_blank">http://kb.vmware.com/kb/2036257</a>
  
ESXi410-201211001 contains ESXi410-201211401-SG

ESX 4.1
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
Filename: ESX410-201211001.zip
  
Build:    874690
  
md5sum:   c167bccc388661e329fc494df13855c3
  
sha1sum:  a8766b2eff68813a262d21a6a6ebeaae62e58c98
  
<a href="http://kb.vmware.com/kb/2036254" target="_blank">http://kb.vmware.com/kb/2036254</a>
  
ESX410-201211001 contains ESX410-201211401-SG, ESX410-201211402-SG,
  
ESX410-201211405-SG, and ESX410-201211407-SG

**5. References**

&#8212; vSphere API &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5703" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5703</a>

&#8212; bind (service console) &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1033" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1033</a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1667" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1667</a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3817" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3817</a>

&#8212; python (service console) &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4940" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4940</a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4944" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4944</a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1150" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1150</a>

&#8212; expat (service console) &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0876" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0876</a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1148" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1148</a>

&#8212; nspr and nss (service console) &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0441" target="_blank">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0441</a>

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

6. Change log

2012-11-15 VMSA-2012-0016
  
Initial security advisory in conjunction with the release of ESX
  
4.1 P06 on 2012-11-15.