---
id: 1968
title: '[Security-announce] UPDATED: VMSA-2013-0001.1 &#8211; VMware vSphere security updates for the authentication service and third party libraries'
date: 2013-02-08T12:13:41+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1968
permalink: /2013/02/08/security-announce-updated-vmsa-2013-0001-1-vmware-vsphere-security-updates-for-the-authentication-service-and-third-party-libraries/
redirect_from: /wp/2013/02/08/security-announce-updated-vmsa-2013-0001-1-vmware-vsphere-security-updates-for-the-authentication-service-and-third-party-libraries/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1209"
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

<!--more-->&#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;</wbr></wbr>

VMware Security Advisory

Advisory ID: VMSA-2013-0001.1
  
Synopsis:    VMware vSphere security updates for the authentication
  
service and third party libraries
  
Issue date:  2013-01-31
  
Updated on:  2013-02-07
  
CVE numbers: &#8212; vSphere authentication &#8212;
  
CVE-2013-1405
  
&#8212; libxml2 &#8212;
  
CVE-2011-3102, CVE-2012-2807
  
&#8212; bind (service console) &#8212;
  
CVE-2012-4244
  
&#8212; xslt (service console) &#8212;
  
CVE-2011-1202, CVE-2011-3970, CVE-2012-2825,
  
CVE-2012-2870, CVE-2012-2871
  
&#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;</wbr></wbr>

1. Summary

VMware vSphere security updates for the authentication service and
  
third party libraries

2. Relevant releases

&#8211; vCenter Server 4.1 without Update 3a
  
&#8211; vCenter Server 4.0 without Update 4b

&#8211; vSphere Client 4.1 without Update 3a
  
&#8211; vSphere Client 4.0 without Update 4b

&#8211; ESXi 4.1 without patch ESXi410-201301401-SG
  
&#8211; ESX 4.1 without patches ESX410-201301401-SG, ESX410-201301402-SG,
  
ESX410-201301403-SG, and ESX410-201301405-SG

&#8211; ESXi 4.0 without patches ESXi400-201302401-SG and
  
ESXi400-201302403-SG
  
&#8211; ESX 4.0 without patch ESX400-201302401-SG

3. Problem Description

a. VMware vSphere client-side authentication memory corruption
  
vulnerability

VMware vCenter Server, vSphere Client, and ESX contain a
  
vulnerability in the handling of the management authentication
  
protocol. To exploit this vulnerability, an attacker must
  
convince either vCenter Server, vSphere Client or ESX to
  
interact with a malicious server as a client. Exploitation of
  
the issue may lead to code execution on the client system.

To reduce the likelihood of exploitation, vSphere components
  
should be deployed on an isolated management network.

The Common Vulnerabilities and Exposures Project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the name CVE-2013-1405 to this issue.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware            Product     Running     Replace with/
  
Product           Version     on          Apply Patch
  
==============    =======     =======     =================
  
vCenter Server    5.1         Windows     not affected
  
vCenter Server    5.0         Windows     not affected
  
vCenter Server    4.1         Windows     4.1 Update 3a
  
vCenter Server    4.0         Windows     4.0 Update 4b
  
VirtualCenter     2.5         Windows     patch pending

vSphere Client    5.1         Windows     not affected
  
vSphere Client    5.0         Windows     not affected
  
vSphere Client    4.1         Windows     4.1 Update 3a **
  
vSphere Client    4.0         Windows     4.0 Update 4b **
  
VI-Client         2.5         Windows     patch pending

hosted *          any         any         not affected

ESXi              5.1         ESXi        not affected
  
ESXi              5.0         ESXi        not affected
  
ESXi              4.1         ESXi        ESXi410-201301401-SG
  
ESXi              4.0         ESXi        ESXi400-201302401-SG
  
ESXi400-201302403-SG (vSphere client)
  
ESXi              3.5         ESXi        patch pending

ESX               4.1         ESX         ESX410-201301401-SG
  
ESX               4.0         ESX         ESX400-201302401-SG (includes vSphere client)
  
ESX               3.5         ESX         patch pending

* hosted products are VMware Workstation, Player, ACE, Fusion.

** To remediate CVE-2013-1405, customers must apply updates to
  
all components of the authentication service.  First,
  
customers should update vCenter Server or ESXi/ESX as
  
appropriate to ensure that the updated vSphere Client is
  
downloaded.  Then, the vSphere client can be updated using
  
any one of the following methods:

&#8211; Run the installer that ships with vCenter Server
  
&#8211; Follow the client installation link on the vCenter Server
  
welcome page
  
&#8211; Follow the client installation link on the ESXi/ESX
  
Server welcome page

b. Update to ESX/ESXi libxml2 userworld and service console

The ESX/ESXi userworld libxml2 library has been updated to
  
resolve multiple security issues. Also, the ESX service console
  
libxml2 packages are updated to the following versions:

libxml2-2.6.26-2.1.15.el5_8.5
  
libxml2-python-2.6.26-2.1.15.<wbr>el5_8.5</wbr>

These updates fix multiple security issues. The Common
  
Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>) has
  
assigned the names CVE-2011-3102 and CVE-2012-2807 to these
  
issues.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware          Product   Running  Replace with/
  
Product         Version   on       Apply Patch
  
==============  ========  =======  =================
  
ESXi            5.1       ESXi     patch pending
  
ESXi            5.0       ESXi     patch pending
  
ESXi            4.1       ESXi     ESXi410-201301401-SG
  
ESXi            4.0       ESXi     no patch planned
  
ESXi            3.5       ESXi     no patch planned

ESX             4.1       ESX      ESX410-201301405-SG
  
ESX             4.0       ESX      no patch planned
  
ESX             3.5       ESX      no patch planned

c. Update to ESX service console bind packages

The ESX service console bind packages are updated to the
  
following versions:

bind-libs-9.3.6-20.P1.el5_8.2
  
bind-utils-9.3.6-20.P1.el5_8.2

These updates fix a security issue. The Common Vulnerabilities
  
and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>) has assigned the name
  
CVE-2012-4244 to this issue.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware          Product   Running  Replace with/
  
Product         Version   on       Apply Patch
  
==============  ========  =======  =================
  
ESXi            any       ESXi     not applicable

ESX             4.1       ESX      ESX410-201301402-SG
  
ESX             4.0       ESX      patch pending
  
ESX             3.5       ESX      not applicable

d. Update to ESX service console libxslt package

The ESX service console libxslt package is updated to version
  
libxslt-1.1.17-4.el5_8.3 to resolve multiple security issues.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the names CVE-2011-1202, CVE-2011-3970,
  
CVE-2012-2825, CVE-2012-2870, and CVE-2012-2871 to these issues.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware          Product   Running  Replace with/
  
Product         Version   on       Apply Patch
  
==============  ========  =======  =================
  
ESXi            any       ESXi     not applicable

ESX             4.1       ESX      ESX410-201301403-SG
  
ESX             4.0       ESX      not affected
  
ESX             3.5       ESX      not applicable

4. Solution

Please review the patch/release notes for your product and
  
version and verify the checksum of your downloaded file.

vCenter Server 4.1 Update 3a
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
The download for vCenter Server includes vSphere Update Manager,
  
vSphere Client, and vCenter Orchestrator.

Download link:
  
<a href="https://downloads.vmware.com/d/info/datacenter_cloud_infrastructure/vmware_vsphere/4_1" target="_blank">https://downloads.vmware.com/<wbr>d/info/datacenter_cloud_<wbr>infrastructure/vmware_vsphere/<wbr>4_1</wbr></wbr></wbr></a>

Release Notes:
  
<a href="https://www.vmware.com/support/vsphere4/doc/vsp_vc41_u3a_rel_notes.html" target="_blank">https://www.vmware.com/<wbr>support/vsphere4/doc/vsp_vc41_<wbr>u3a_rel_notes.html</wbr></wbr></a>

vCenter Server 4.0 Update 4b
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
The download for vCenter Server includes vSphere Update Manager,
  
vSphere Client, and vCenter Orchestrator.

Download link:
  
<a href="https://downloads.vmware.com/d/info/datacenter_cloud_infrastructure/vmware_vsphere/4_0" target="_blank">https://downloads.vmware.com/<wbr>d/info/datacenter_cloud_<wbr>infrastructure/vmware_vsphere/<wbr>4_0</wbr></wbr></wbr></a>

Release Notes:
  
<a href="https://www.vmware.com/support/vsphere4/doc/vsp_vc40_u4b_rel_notes.html" target="_blank">https://www.vmware.com/<wbr>support/vsphere4/doc/vsp_vc40_<wbr>u4b_rel_notes.html</wbr></wbr></a>

ESXi and ESX
  
&#8212;&#8212;&#8212;&#8212;
  
<a href="https://my.vmware.com/web/vmware/downloads" target="_blank">https://my.vmware.com/web/<wbr>vmware/downloads</wbr></a>

ESXi 4.1
  
&#8212;&#8212;&#8211;
  
File: ESXi410-201301001.zip
  
Build: 975799
  
md5sum: 3543d3f16a1f1b1369dcdb5c25fa71<wbr>06
  
sha1sum: cced12e87838a3b037c9ec99d84908<wbr>09c61fe883
  
<a href="http://kb.vmware.com/kb/2041332" target="_blank">http://kb.vmware.com/kb/<wbr>2041332</wbr></a>
  
ESXi410-201301001 contains ESXi410-201301401-SG</wbr></wbr>

ESX 4.1
  
&#8212;&#8212;-
  
File: ESX410-201301001.zip
  
Build: 977344
  
md5sum: 0219dbcbcc6fafe8bf33695682c865<wbr>8d
  
sha1sum: 2eab9d56ac81f7d2d00c15b155bd93<wbr>c36b0e03c3
  
<a href="http://kb.vmware.com/kb/2041331" target="_blank">http://kb.vmware.com/kb/<wbr>2041331</wbr></a>
  
ESX410-201301001 contains ESX410-201301401-SG, ESX410-201301402-SG,
  
ESX410-201301403-SG, and ESX410-201301405-SG</wbr></wbr>

ESXi 4.0
  
&#8212;&#8212;&#8211;
  
File: ESXi400-201302001.zip
  
md5sum: 03dc9246239dd449bf21a122e7b1bc<wbr>f3
  
sha1sum: 276346a186c068c1fdbf19e1b753b8<wbr>a2dbc8c89c
  
<a href="http://kb.vmware.com/kb/2041344" target="_blank">http://kb.vmware.com/kb/<wbr>2041344</wbr></a>
  
ESXi400-201302001 contains ESXi400-201302401-SG and
  
ESXi400-201302403-SG</wbr></wbr>

ESX 4.0
  
&#8212;&#8212;-
  
File: ESX400-201302001.zip
  
Build: 987598
  
md5sum: 2a883e737c3cde990fe4792c64c32f<wbr>cd
  
sha1sum: 92c3b13ab3fdee73c335d5e8b41159<wbr>f546def199
  
<a href="http://kb.vmware.com/kb/2041343" target="_blank">http://kb.vmware.com/kb/<wbr>2041343</wbr></a>
  
ESX400-201302001 contains ESX400-201302401-SG</wbr></wbr>

5. References

&#8212; vSphere authentication &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1405" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2013-1405</wbr></a>
  
&#8212; libxml2 &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3102" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2011-3102</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-2807" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-2807</wbr></a>
  
&#8212; bind (service console) &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-4244" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-4244</wbr></a>
  
&#8212; xslt (service console) &#8212;
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-1202" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2011-1202</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3970" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2011-3970</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-2825" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-2825</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-2870" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-2870</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-2871" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-2871</wbr></a>

&#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;</wbr></wbr>

6. Change log

2013-01-31 VMSA-2013-0001
  
Initial security advisory in conjunction with the release of
  
vCenter 4.1 Update 3a and ESX 4.1 patches on 2013-01-31.

2013-02-07 VMSA-2013-0001.1
  
Updated security advisory to include vCenter 4.0 Update 4b and
  
patches for ESX 4.0.