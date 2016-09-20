---
id: 1892
title: '[Security-announce] VMSA-2012-0018 VMware security updates for vCSA and ESXi'
date: 2012-12-20T23:55:26+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1892
permalink: /2012/12/20/security-announce-vmsa-2012-0018-vmware-security-updates-for-vcsa-and-esxi/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 497
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

**VMware Security Advisory**

Advisory ID:  VMSA-2012-0018
  
Synopsis:     VMware security updates for vCSA and ESXi
  
Issue date:   2012-12-20
  
Updated on:   2012-12-20 (initial advisory)
  
CVE numbers:
  
&#8212;&#8212;&#8212;&#8212;- vCSA &#8212;&#8212;&#8212;&#8212;&#8212;
  
CVE-2012-6324, CVE-2012-6325

&#8212;&#8212;&#8212;&#8212;- glibc &#8212;&#8212;&#8212;&#8212;&#8211;
  
CVE-2009-5029, CVE-2009-5064, CVE-2010-0830, CVE-2011-1089, CVE-2011-4609, CVE-2012-0864, CVE-2012-3404, CVE-2012-3405, CVE-2012-3406, CVE-2012-3480

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8211;

**1. Summary**

VMware has updated vCenter Server Appliance (vCSA) and ESX to address multiple security vulnerabilities

**2. Relevant releases**

vCenter Server Appliance 5.1 without Patch 1
  
vCenter Server Appliance 5.0 without Update 2

VMware ESXi 5.1 without patch ESXi510-201212101
  
VMware ESXi 5.0 without patch ESXi500-201212101

**3. Problem Description**

a. vCenter Server Appliance directory traversal

The vCenter Server Appliance (vCSA) contains a directory
  
traversal vulnerability that allows an authenticated
  
remote user to retrieve arbitrary files. Exploitation of
  
this issue may expose sensitive information stored on the
  
server.

VMware would like to thank Alexander Minozhenko from ERPScan for
  
reporting this issue to us.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the name CVE-2012-6324 to this issue.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware          Product   Running  Replace with/
  
Product         Version   on       Apply Patch
  
==============  ========  =======  =================
  
vCSA            5.1       Linux    vCSA 5.1 Patch 1
  
vCSA            5.0       Linux    vCSA 5.0 Update 2

b. vCenter Server Appliance arbitrary file download

The vCenter Server Appliance (vCSA) contains an XML parsing
  
vulnerability that allows an authenticated remote user to
  
retrieve arbitrary files.  Exploitation of this issue may
  
expose sensitive information stored on the server.

VMware would like to thank Alexander Minozhenko from ERPScan for
  
reporting this issue to us.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the name CVE-2012-6325 to this issue.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware          Product   Running  Replace with/
  
Product         Version   on       Apply Patch
  
==============  ========  =======  =================
  
vCSA            5.1       Linux    not affected
  
vCSA            5.0       Linux    vCSA 5.0 Update 2

c. Update to ESX glibc package

The ESX glibc package is updated to version glibc-2.5-81.el5_8.1
  
to resolve multiple security issues.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the names CVE-2009-5029, CVE-2009-5064,
  
CVE-2010-0830, CVE-2011-1089, CVE-2011-4609, CVE-2012-0864
  
CVE-2012-3404, CVE-2012-3405, CVE-2012-3406 and CVE-2012-3480
  
to these issues.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware          Product   Running  Replace with/
  
Product         Version   on       Apply Patch
  
==============  ========  =======  =================
  
ESXi            5.1       ESXi     ESXi510-201212101
  
ESXi            5.0       ESXi     ESXi500-201212101
  
ESXi            4.1       ESXi     no patch planned
  
ESXi            4.0       ESXi     no patch planned
  
ESXi            3.5       ESXi     not applicable

ESX             any       ESX      not applicable

**4. Solution**

Please review the patch/release notes for your product and
  
version and verify the checksum of your downloaded file.

ESXi and ESX
  
&#8212;&#8212;&#8212;&#8212;
  
The download for ESXi includes vCenter Server Appliance.

<a href="https://downloads.vmware.com/go/selfsupport-download" target="_blank">https://downloads.vmware.com/<wbr>go/selfsupport-download</wbr></a>

ESXi 5.1
  
<a href="http://kb.vmware.com/kb/2035775" target="_blank">http://kb.vmware.com/kb/<wbr>2035775</wbr></a>

ESXi 5.0
  
<a href="http://kb.vmware.com/kb/2033751" target="_blank">http://kb.vmware.com/kb/<wbr>2033751</wbr></a>

**5. References**

&#8212;&#8212;&#8212;&#8212;- vCSA &#8212;&#8212;&#8212;&#8212;&#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-6324" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-6324</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-6325" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-6325</wbr></a>
  
&#8212;&#8212;&#8212;&#8212;- glibc &#8212;&#8212;&#8212;&#8212;&#8211;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2009-5029" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2009-5029</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2009-5064" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2009-5064</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-0830" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2010-0830</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-1089" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2011-1089</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4609" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2011-4609</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0864" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-0864</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3404" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-3404</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3405" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-3405</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3406" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-3406</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3480" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-3480</wbr></a>

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8211;

6. Change log

2012-12-20 VMSA-2012-0018
  
Initial security advisory in conjunction with the release of
  
vSphere 5.1 Patch 1 and vSphere 5.0 Update 2 on 2012-12-20.
  
</wbr></wbr></wbr></wbr>