---
id: 1896
title: '[Security-announce] UPDATED VMSA-2012-0005.4 VMware vCenter Server, Orchestrator, Update Manager, vShield, vSphere Client, Workstation, Player, ESXi, and ESX address several security issues'
date: 2012-12-21T00:28:08+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1896
permalink: /2012/12/21/security-announce-updated-vmsa-2012-0005-4-vmware-vcenter-server-orchestrator-update-manager-vshield-vsphere-client-workstation-player-esxi-and-esx-address-several-security-issues/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 772
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

<div>
  <!--more-->
</div>

&#8211; &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;</wbr></wbr>

**                  VMware Security Advisory**

Advisory ID:  VMSA-2012-0005.4

Synopsis:     VMware vCenter Server, Orchestrator, Update Manager,

vShield, vSphere Client, Workstation, Player, ESXi, and

ESX address several security issues

Issue date:   2012-03-15

Updated on:   2012-12-20

CVE numbers:  CVE-2012-1508, CVE-2012-1509, CVE-2012-1510,

CVE-2012-1512, CVE-2012-1513, CVE-2012-1514,

CVE-2011-3190, CVE-2011-3375, CVE-2012-0022,

CVE-2010-0405

&#8212; JRE &#8212;

See references

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;</wbr></wbr>

**1. Summary**

VMware vCenter Server, Orchestrator, Update Manager, vShield, vSphere

Client, Workstation, Player, ESXi, and ESX address several security

issues

&nbsp;

**2. Relevant releases**

Workstation 7.1.4
  
Player 3.1.4
  
VMware vCenter Server 5.0

VMware vCenter Server 4.1 Update 2 and earlier

VMware vCenter Server 4.0 Update 3 and earlier
  
VMware vSphere Client 5.0

VMware vSphere Client 4.1 Update 1 and earlier
  
VMware vCenter Orchestrator 4.2

VMware vCenter Orchestrator 4.1 Update 1 and earlier

VMware vCenter Orchestrator 4.0 Update 3 and earlier

&nbsp;

VMware vShield Manager 4.1 Update 1

VMware vShield Manager 1.0 Update 1

&nbsp;

VMware Update Manager 5.0

&nbsp;

ESXi 5.0 without patches ESXi500-201203101-SG, ESXi500-201112402-BG

ESXi 4.1 without patch ESXi410-201110202-UG

ESXi 4.0 without patch ESXi400-201110402-BG

&nbsp;

ESX 4.1 without patch ESX410-201110201-SG, ESX410-201208101-SG

ESX 4.0 without patch ESX400-201110401-SG

&nbsp;

**3. Problem Description**

&nbsp;

a. VMware Tools Display Driver Privilege Escalation

&nbsp;

The VMware XPDM and WDDM display drivers contain buffer overflow

vulnerabilities and the XPDM display driver does not properly

check for NULL pointers. Exploitation of these issues may lead

to local privilege escalation on Windows-based Guest Operating

Systems.

&nbsp;

VMware would like to thank Tarjei Mandt for reporting theses

issues to us.

&nbsp;

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)

has assigned the names CVE-2012-1509 (XPDM buffer overrun),

CVE-2012-1510 (WDDM buffer overrun) and CVE-2012-1508 (XPDM null

pointer dereference) to these issues.

&nbsp;

Note: CVE-2012-1509 doesn&#8217;t affect ESXi and ESX.

&nbsp;

Column 4 of the following table lists the action required to

remediate the vulnerability in each release, if a solution is

available.

&nbsp;

VMware         Product   Running  Replace with/

Product \*      Version   on       Apply Patch \**

=============  ========  =======  =================

vCenter        any       Windows  not affected

Workstation    8.x       any      not affected

Workstation    7.x       any      7.1.5 or later

&nbsp;

Player         4.x       any      not affected

Player         3.x       any      3.1.5 or later

Fusion         4.x       Mac OS/X not affected

ESXi           5.0       ESXi     ESXi500-201112402-BG

ESXi           4.1       ESXi     ESXi410-201110202-UG

ESXi           4.0       ESXi     ESXi400-201110402-BG

ESXi           3.5       ESXi     not affected

ESX            4.1       ESX      ESX410-201110201-SG

ESX            4.0       ESX      ESX400-201110401-SG

ESX            3.5       ESX      not affected

&nbsp;

* Remediation for VMware View is described in VMSA-2012-0004.

&nbsp;

** Notes on updating VMware Guest Tools:

&nbsp;

After the update or patch is applied, VMware Guest Tools must

be updated in any pre-existing Windows-based Guest Operating

System. The XPDM and WDDM drivers are part of Tools.

&nbsp;

Windows-Based Virtual Machines that have moved to Workstation

8 or Player 4 from a lower version of Workstation or Player

are affected unless:

&nbsp;

&#8211; They were moved from Workstation 7.1.5 or Player 3.1.5,

&nbsp;

AND

&nbsp;

&#8211; The Tools version was updated before the move.

&nbsp;

Windows-Based Virtual Machines that have moved to Fusion 4

from a lower version of Fusion are affected.

&nbsp;

b. vSphere Client internal browser input validation vulnerability

The vSphere Client has an internal browser that renders html

pages from log file entries. This browser doesn&#8217;t properly

sanitize input and may run script that is introduced into the

log files. In order for the script to run, the user would need

to open an individual, malicious log file entry. The script

would run with the permissions of the user that runs the vSphere

Client.

&nbsp;

VMware would like to thank Edward Torkington for reporting this

issue to us.

&nbsp;

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)

has assigned the name CVE-2012-1512 to this issue.

&nbsp;

In order to remediate the issue, the vSphere Client of the

vSphere 5.0 Update 1 release or the vSphere 4.1 Update 2 release

needs to be installed. The vSphere Clients that come with

vSphere 4.0 and vCenter Server 2.5 are not affected.

&nbsp;

c. vCenter Orchestrator Password Disclosure

&nbsp;

The vCenter Orchestrator (vCO) Web Configuration tool reflects

back the vCenter Server password as part of the webpage. This

might allow the logged-in vCO administrator to retrieve the

vCenter Server password.

&nbsp;

VMware would like to thank Alexey Sintsov from Digital Security

Research Group for reporting this issue to us.

&nbsp;

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)

has assigned the name CVE-2012-1513 to this issue.

&nbsp;

VMware         Product  Running    Replace with/

Product        Version  on         Apply Patch

=============  =======  =======    =================

vCO            4.2      Windows    vCO 4.2 Update 1

vCO            4.1      Windows    vCO 4.1 Update 2

vCO            4.0      Windows    vCO 4.0 Update 4

&nbsp;

d. vShield Manager Cross-Site Request Forgery vulnerability

&nbsp;

The vShield Manager (vSM) interface has a Cross-Site Request

Forgery vulnerability. If an attacker can convince an

authenticated user to visit a malicious link, the attacker may

force the victim to forward an authenticated request to the

server.

&nbsp;

VMware would like to thank Frans Pehrson of Xxor AB

(<a href="http://www.xxor.se/" target="_blank">www.xxor.se</a>) and Claudio Criscione for independently reporting

this issue to us

&nbsp;

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)

has assigned the name CVE-2012-1514 to this issue.

&nbsp;

VMware         Product  Running    Replace with/

Product        Version  on         Apply Patch

=============  =======  =======    =================

vSM            5.0      Linux      not affected

vSM            4.1      Linux      vSM 4.1.0 Update 2

vSM            4.0      Linux      vSM 1.0.1 Update 2

&nbsp;

e. vCenter Update Manager, Oracle (Sun) JRE update 1.6.0_30

&nbsp;

Oracle (Sun) JRE is updated to version 1.6.0_30, which addresses

multiple security issues that existed in earlier releases of

Oracle (Sun) JRE.

&nbsp;

Oracle has documented the CVE identifiers that are addressed in

JRE 1.6.0\_29 and JRE 1.6.0\_30 in the Oracle Java SE Critical

Patch Update Advisory of October 2011. The References section

provides a link to this advisory.

&nbsp;

Column 4 of the following table lists the action required to

remediate the vulnerability in each release, if a solution is

available.

&nbsp;

VMware         Product  Running     Replace with/

Product        Version  on          Apply Patch

=============  =======  =======     =================

vCenter        5.0      Windows     See VMSA-2012-0013

vCenter        4.1      Windows     See VMSA-2012-0013

vCenter        4.0      Windows     not applicable **

VirtualCenter  2.5      Windows     not applicable **

&nbsp;

Update Manager 5.0      Windows     Update Manager 5.0 Update 1

Update Manager 4.1      Windows     not applicable **

Update Manager 4.0      Windows     not applicable **

&nbsp;

hosted *       any      any         not affected

&nbsp;

ESXi           any      ESXi        not applicable

&nbsp;

ESX            4.1      ESX         See VMSA-2012-0013

ESX            4.0      ESX         not applicable **

ESX            3.5      ESX         not applicable **

&nbsp;

* hosted products are VMware Workstation, Player, ACE, Fusion.

&nbsp;

** this product uses the Oracle (Sun) JRE 1.5.0 family

&nbsp;

f. vCenter Server Apache Tomcat update 6.0.35

&nbsp;

Apache Tomcat has been updated to version 6.0.35 to address

multiple security issues.

&nbsp;

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)

has assigned the names CVE-2011-3190, CVE-2011-3375,

CVE-2011-4858, and CVE-2012-0022 to these issues.

&nbsp;

&nbsp;

VMware         Product  Running     Replace with/

Product        Version  on          Apply Patch

=============  =======  =======     =================

vCenter        5.0      Windows     vCenter 5.0 Update 1

vCenter        4.1      Windows     vCenter 4.1 Update 3

vCenter        4.0      Windows     vCenter 4.0 Update 4a

VirtualCenter  2.5      Windows     not applicable **

hosted *       any      any         not affected

ESXi           any      ESXi        not applicable

ESX            4.1      ESX         ESX410-201208101-SG

ESX            4.0      ESX         ESX400-201209401-SG

ESX            3.5      ESX         not applicable **

&nbsp;

* hosted products are VMware Workstation, Player, ACE, Fusion.

&nbsp;

** this product uses the Apache Tomcat 5.5 family

&nbsp;

g. ESXi update to third party component bzip2

&nbsp;

The bzip2 library is updated to version 1.0.6, which resolves a

security issue.

&nbsp;

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)

has assigned the name CVE-2010-0405 to this issue.

&nbsp;

VMware         Product  Running     Replace with/

Product        Version  on          Apply Patch

=============  =======  =======    =================

vCenter        any      Windows    not affected

hosted *       any      any        not affected

ESXi           5.0      ESXi       ESXi500-201203101-SG

ESXi           4.1      ESXi       not affected

ESXi           4.0      ESXi       not affected

ESXi           3.5      ESXi       not affected

ESX            any      ESX        not applicable

&nbsp;

* hosted products are VMware Workstation, Player, ACE, Fusion.

&nbsp;

**4. Solution**

&nbsp;

Please review the patch/release notes for your product and version

and verify the checksum of your downloaded file.

VMware Workstation 7.1.5

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;

<a href="http://www.vmware.com/go/downloadworkstation" target="_blank">http://www.vmware.com/go/<wbr>downloadworkstation</wbr></a>

&nbsp;

Release notes:

<a href="https://www.vmware.com/support/ws71/doc/releasenotes_ws715.html" target="_blank">https://www.vmware.com/<wbr>support/ws71/doc/releasenotes_<wbr>ws715.html</wbr></wbr></a>

&nbsp;

VMware Workstation for Windows 32-bit and 64-bit with VMware Tools

md5sum: 40a0a39377a6ba804d5e76e59449d5<wbr>1f</wbr>

sha1sum: 25462e18bf9439876c63948415f7ba<wbr>7b09baa8e6</wbr>

&nbsp;

VMware Workstation for Linux 32-bit with VMware Tools

md5sum: 9c9b4d7a749f1baa485f26e6f366c0<wbr>70</wbr>

sha1sum: 31033424656b8eaaa814f3e9c3b5b9<wbr>c5c53b783b</wbr>

&nbsp;

VMware Workstation for Linux 64-bit with VMware Tools

md5sum: 482b8b2890f75488addfc314180318<wbr>64</wbr>

sha1sum: b1f73650f70c94249e5add5d9516d0<wbr>e45c4ae87d</wbr>

&nbsp;

VMware Player 3.1.5

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

<a href="http://www.vmware.com/go/downloadplayer" target="_blank">http://www.vmware.com/go/<wbr>downloadplayer</wbr></a>

&nbsp;

Release notes:

<a href="https://www.vmware.com/support/player31/doc/releasenotes_player315.html" target="_blank">https://www.vmware.com/<wbr>support/player31/doc/<wbr>releasenotes_player315.html</wbr></wbr></a>

&nbsp;

VMware Player for 32-bit and 64-bit Windows

md5sum: fcc91227963e58efcb63fb791d2fd8<wbr>13</wbr>

sha1sum: d39d9da694c22530a7fa701e3ded6c<wbr>ccdc3ea390</wbr>

&nbsp;

VMware Player for 32-bit Linux

md5sum: c96867c8093d23065bed7e71e020bb<wbr>19</wbr>

sha1sum: 4156bdfb7f679114671b416d178028<wbr>fdc4d3beb4</wbr>

&nbsp;

VMware Player for 64-bit Linux

md5sum: 1ec954f1baaf6a60e451979b5e88f2<wbr>d6</wbr>

sha1sum: a253a486d6c6848620de200ef1837c<wbr>ed903daa1c</wbr>

&nbsp;

vCenter Server 5.0 Update 1

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;

&nbsp;

The download for vCenter Server includes vSphere Update Manager,

vSphere Client, and vCenter Orchestrator

&nbsp;

Download link:

&nbsp;

<a href="http://downloads.vmware.com/d/info/datacenter_cloud_infrastructure/vmware_v" target="_blank">http://downloads.vmware.com/d/<wbr>info/datacenter_cloud_<wbr>infrastructure/vmware_v</wbr></wbr></a>

sphere/5_0

&nbsp;

Release Notes:

vSphere vCenter Server

&nbsp;

<a href="https://www.vmware.com/support/pubs/vsphere-esxi-vcenter-server-pubs.html" target="_blank">https://www.vmware.com/<wbr>support/pubs/vsphere-esxi-<wbr>vcenter-server-pubs.html</wbr></wbr></a>

<a href="https://www.vmware.com/support/pubs/vum_pubs.html" target="_blank">https://www.vmware.com/<wbr>support/pubs/vum_pubs.html</wbr></a>

&nbsp;

File: VMware-VIMSetup-all-5.0.0-<wbr>639890.iso</wbr>

md5sum:<wbr>f860ac4b618e2562ebffa2318446fa<wbr>5b</wbr></wbr>

sha1sum:<wbr>62830e3061b983e98944ae6d9d3b2e<wbr>820cebe270</wbr></wbr>

&nbsp;

File: VMware-VIMSetup-all-5.0.0-<wbr>639890.zip</wbr>

md5sum:<wbr>a8bdde277aeeffc382ec210acf5104<wbr>79</wbr></wbr>

sha1sum:<wbr>0b675a47349fdc09104c62ad84bd30<wbr>2846213fc8</wbr></wbr>

&nbsp;

vCenter Server 4.1 Update 3

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;

The download for vCenter Server includes vSphere Update Manager,

vSphere Client, and vCenter Orchestrator

&nbsp;

Download link

&nbsp;

<a href="http://downloads.vmware.com/d/info/datacenter_cloud_infrastructure/vmware_v" target="_blank">http://downloads.vmware.com/d/<wbr>info/datacenter_cloud_<wbr>infrastructure/vmware_v</wbr></wbr></a>

sphere/4_1

&nbsp;

Release Notes

<a href="https://www.vmware.com/support/vsphere4/doc/vsp_vc41_u3_rel_notes.html" target="_blank">https://www.vmware.com/<wbr>support/vsphere4/doc/vsp_vc41_<wbr>u3_rel_notes.html</wbr></wbr></a>

&nbsp;

VMware-VIMSetup-all-4.1.0-<wbr>816786.iso   </wbr>

md5sum: c1fd9189783e615fec4864ff6b8c86<wbr>bd</wbr>

sha1sum: 38c03ac195939bd23da666b9ee98ef<wbr>7c9c912a55</wbr>

&nbsp;

VMware-VIMSetup-all-4.1.0-<wbr>816786.zip</wbr>

md5sum: d20705520fc4b5bccd71b060283e5b<wbr>59</wbr>

sha1sum: ea2a84544cd6cd29447c4ce905111e<wbr>7dfc62f4cd</wbr>

&nbsp;

vCenter Server 4.0 Update 4

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;

&nbsp;

The download for vCenter Server includes vCenter Orchestrator.

&nbsp;

Download link:

&nbsp;

<a href="http://downloads.vmware.com/d/info/datacenter_cloud_infrastructure/vmware_v" target="_blank">http://downloads.vmware.com/d/<wbr>info/datacenter_cloud_<wbr>infrastructure/vmware_v</wbr></wbr></a>

sphere/4_0

&nbsp;

Release Notes:

&nbsp;

<a href="http://downloads.vmware.com/support/pubs/vs_pages/vsp_pubs_esx40_vc40.html" target="_blank">http://downloads.vmware.com/<wbr>support/pubs/vs_pages/vsp_<wbr>pubs_esx40_vc40.html</wbr></wbr></a>

&nbsp;

File: VMware-VIMSetup-all-4.0.0-<wbr>502539.iso</wbr>

md5sum: b418ff3d394f91b418271b6b93dfd6<wbr>bd</wbr>

sha1sum: 56c2ec60f8b8a734a8312d9e38d5d7<wbr>0cd20c0927</wbr>

&nbsp;

File: VMware-VIMSetup-all-4.0.0-<wbr>502539.zip</wbr>

md5sum: 2acfadde1ec0cd6d37063d87246d69<wbr>42</wbr>

sha1sum: ea1f3a3cb178f23fc2cf49bfc1450d<wbr>10e5f699f8</wbr>

&nbsp;

vCenter Server 4.0 Update 4a

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

The download for vCenter Server includes vSphere Update Manager,

vSphere Client, and vCenter Orchestrator

&nbsp;

Download link

&nbsp;

<a href="http://downloads.vmware.com/d/info/datacenter_cloud_infrastructure/vmware_v" target="_blank">http://downloads.vmware.com/d/<wbr>info/datacenter_cloud_<wbr>infrastructure/vmware_v</wbr></wbr></a>

sphere/4_0

&nbsp;

Release Notes

<a href="https://www.vmware.com/support/vsphere4/doc/vsp_vc40_u4a_rel_notes.html" target="_blank">https://www.vmware.com/<wbr>support/vsphere4/doc/vsp_vc40_<wbr>u4a_rel_notes.html</wbr></wbr></a>

&nbsp;

VMware-VIMSetup-all-4.0.0-<wbr>818020.iso</wbr>

md5sum: aa362485d8a9d4ad9dc4a647aba670<wbr>1e</wbr>

sha1sum: c37c1e0983e5b3011a1d27fa586021<wbr>50427dc466</wbr>

&nbsp;

VMware-VIMSetup-all-4.0.0-<wbr>818020.zip</wbr>

md5sum: 531af0519e4c36fafab990447b5519<wbr>8b</wbr>

sha1sum: 8fb39414d034127de0052adf00e335<wbr>6cc04593ed</wbr>

vShield Manager 4.1.0 Update 2

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;

&nbsp;

The download for VMware vShield App contains vShield Manager

&nbsp;

Download link:

<a href="http://www.vmware.com/download/download.do?downloadGroup=VSHIELD_APP10U2" target="_blank">http://www.vmware.com/<wbr>download/download.do?<wbr>downloadGroup=VSHIELD_APP10U2</wbr></wbr></a>

&nbsp;

Release Notes:

&nbsp;

<a href="https://www.vmware.com/support/vshield/doc/releasenotes_vshield_410U2.html" target="_blank">https://www.vmware.com/<wbr>support/vshield/doc/<wbr>releasenotes_vshield_410U2.<wbr>html</wbr></wbr></wbr></a>

&nbsp;

File: VMware-vShield-Manager-<wbr>upgrade-bundle-4.1.0U2-576124.<wbr>tar.gz</wbr></wbr>

md5sum:<wbr>9a80fc347bc4a19ad0fd4c9fcb4ab4<wbr>75</wbr></wbr>

sha1sum:<wbr>f5780c1615da0493d0955a1343876c<wbr>4111d85203</wbr></wbr>

vShield Zones 1.0 Update 2

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;

The download for VMware vShield Zones contains vShield Manager

&nbsp;

Download link:

<a href="http://www.vmware.com/download/download.do?downloadGroup=ZONES10U2" target="_blank">http://www.vmware.com/<wbr>download/download.do?<wbr>downloadGroup=ZONES10U2</wbr></wbr></a>

&nbsp;

Release Notes

<a href="https://www.vmware.com/support/vsz/doc/releasenotes_vsz_10U2.html" target="_blank">https://www.vmware.com/<wbr>support/vsz/doc/releasenotes_<wbr>vsz_10U2.html</wbr></wbr></a>

&nbsp;

File: VMware-vShieldZones-1.0U2-<wbr>638154.exe</wbr>

md5sum:<wbr>73515f4732c3a1ecc91ef21a504ca6<wbr>d9</wbr></wbr>

sha1sum:<wbr>ed4d858e1c05f54679ba99b739270c<wbr>054efaf63e</wbr></wbr>

ESXi and ESX

&#8212;&#8212;&#8212;&#8212;

&nbsp;

Download link:

<a href="http://downloads.vmware.com/go/selfsupport-download" target="_blank">http://downloads.vmware.com/<wbr>go/selfsupport-download</wbr></a>

&nbsp;

ESXi 5.0

&#8212;&#8212;&#8211;

File: update-from-esxi5.0-5.0_<wbr>update01</wbr>

md5sum: 55c25bd990e2881462bc5b66fb5f6c<wbr>39</wbr>

sha1sum: ecd871bb09b649c6c8c13de82d579d<wbr>4b7dcadc88</wbr>

<a href="http://kb.vmware.com/kb/2011432" target="_blank">http://kb.vmware.com/kb/<wbr>2011432</wbr></a>

update-from-esxi5.0-5.0_<wbr>update01 contains ESXi500-201203101-SG</wbr>

&nbsp;

File: ESXi500-201112001

md5sum: 107ec1cf6ee1d5d5cb8ea5c05b05cc<wbr>10</wbr>

sha1sum: aff63c8a170508c8c0f21a60d1ea75<wbr>ef1922096d</wbr>

<a href="http://kb.vmware.com/kb/2007672" target="_blank">http://kb.vmware.com/kb/<wbr>2007672</wbr></a>

ESXi500-201112001 contains ESXi500-201112402-BG

&nbsp;

Note: subsequent ESXi releases are cumulative and

ESXi500-201203101-SG includes the security fixes that are

present in ESXi500-201112402-BG

ESXi 4.1

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;

update-from-esxi4.1-4.1_<wbr>update02</wbr>

md5sum: 57e34b500ce543d778f230da1d44e4<wbr>12</wbr>

sha1sum: 52f4378e2f1a29c908493182ccbde9<wbr>1d58b4112f</wbr>

<a href="http://kb.vmware.com/kb/2002341" target="_blank">http://kb.vmware.com/kb/<wbr>2002341</wbr></a>

update-from-esxi4.1-4.1_<wbr>update02 contains ESXi410-201110202-UG</wbr>

&nbsp;

ESXi 4.0

&#8212;&#8212;&#8211;

File: ESXi400-201110001

md5sum: fd47b5e2b7ea1db79a2e0793d4c9d9<wbr>d3</wbr>

sha1sum: 759d4fa6da6eb49f41def68e3bd66e<wbr>80c9a7032b</wbr>

<a href="http://kb.vmware.com/kb/1039199" target="_blank">http://kb.vmware.com/kb/<wbr>1039199</wbr></a>

ESXi400-201110001 contains ESXi400-201110402-BG

&nbsp;

ESX 4.1

&#8212;&#8212;-

File: update-from-esx4.1-4.1_<wbr>update3.zip</wbr>

md5sum: a4a45aba880d64210badade8d7c819<wbr>04</wbr>

sha1sum: 4ed1ef2b56fa30deec999916367ab2<wbr>78dc5b1840</wbr>

<a href="http://kb.vmware.com/kb/2020362" target="_blank">http://kb.vmware.com/kb/<wbr>2020362</wbr></a>

update-from-esx4.1-4.1_<wbr>update03 contains ESX410-201208101-SG</wbr>

&nbsp;

update-from-esx4.1-4.1_<wbr>update02</wbr>

md5sum: 96189a6de3797e28b153f89e01d5a1<wbr>5b</wbr>

sha1sum: b1823d39d0e4536a421fb933f02380<wbr>bae7ee7a5d</wbr>

<a href="http://kb.vmware.com/kb/2002303" target="_blank">http://kb.vmware.com/kb/<wbr>2002303</wbr></a>

update-from-esx4.1-4.1_<wbr>update02 contains ESX410-201110201-SG</wbr>

&nbsp;

ESX 4.0

&#8212;&#8212;-

File: ESX400-201209001

md5sum: 7faa79ea8d458e994db308933424a0<wbr>ee</wbr>

sha1sum: 8f798a233cc28b203c3c8e0d44a128<wbr>7af6c1ceb8</wbr>

<a href="http://kb.vmware.com/kb/2019661" target="_blank">http://kb.vmware.com/kb/<wbr>2019661</wbr></a>

ESX400-201209001 contains ESX400-201209401-SG

&nbsp;

File: ESX400-201110001

md5sum: 0ce9cc285ea5c27142c9fdf273443d<wbr>78</wbr>

sha1sum: fdb5482b2bf1e9c97f2814255676e3<wbr>de74512399</wbr>

<a href="http://kb.vmware.com/kb/1036392" target="_blank">http://kb.vmware.com/kb/<wbr>1036392</wbr></a>

ESX400-201110001 contains ESX400-201110401-SG

&nbsp;

**5. References**

&nbsp;

Oracle Java SE Critical Patch Update Advisory of October 2011

&nbsp;

&nbsp;

<a href="http://www.oracle.com/technetwork/topics/security/javacpuoct2011-443431.htm" target="_blank">http://www.oracle.com/<wbr>technetwork/topics/security/<wbr>javacpuoct2011-443431.htm</wbr></wbr></a>

l

&nbsp;

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1508" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-1508</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1509" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-1509</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1510" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-1510</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1512" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-1512</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1513" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-1513</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1514" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-1514</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3190" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2011-3190</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3375" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2011-3375</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0022" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-0022</wbr></a>

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-0405" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2010-0405</wbr></a>

&nbsp;

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;</wbr></wbr>

&nbsp;

**6. Change log**

&nbsp;

2012-03-15 VMSA-2012-0005

Initial security advisory in conjunction with the release of

vSphere 5.0 Update 1, Orchestrator 4.2 Update 1, Update Manager 5.0

Update 1, vShield 1.0 Update 2, and ESXi and ESX 5.0 patches on

2012-03-15.

&nbsp;

2012-06-13 VMSA-2012-0005.1

&nbsp;

Updated Relevant Releases, Problem Description, and Solution

sections to include information regarding updates for Workstation 7

in conjunction with the release of Workstation 7.1.6 on 2012-06-13.

&nbsp;

2012-08-30 VMSA-2012-0005.2

&nbsp;

Updated Relevant Releases, Problem Description, and Solution

sections to include information regarding updates for ESX, ESXi,

and vCenter Server in conjunction with the release of vSphere 4.1 U3

on 2012-08-30.

&nbsp;

2012-09-12 VMSA-2012-0005.3

&nbsp;

Updated security advisory in conjunction with the release of

vSphere 4.0 U4a on 2012-09-12 and ESX 4.0 patches on 2012-09-13.

&nbsp;

2012-12-20 VMSA-2012-0005.4

&nbsp;

Updated security advisory in conjunction with the release of

vSphere 5.0 Update 2 on 2012-12-20.