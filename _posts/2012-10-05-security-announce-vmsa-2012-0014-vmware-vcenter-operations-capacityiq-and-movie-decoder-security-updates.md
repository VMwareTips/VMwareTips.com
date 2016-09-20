---
id: 1753
title: '[Security-announce] VMSA-2012-0014 VMware vCenter Operations, CapacityIQ, and Movie Decoder security updates'
date: 2012-10-05T00:07:31+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1753
permalink: /2012/10/05/security-announce-vmsa-2012-0014-vmware-vcenter-operations-capacityiq-and-movie-decoder-security-updates/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 756
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

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;
  
VMware Security Advisory

Advisory ID:  VMSA-2012-0014
  
Synopsis: VMware vCenter Operations, CapacityIQ, and Movie Decoder
  
security updates
  
Issue date:   2012-10-04
  
Updated on:   2012-10-04 (initial advisory)
  
CVE numbers:  CVE-2012-4897, CVE-2012-5050, CVE-2012-5051
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;
  
1. Summary

VMware has provided an upgrade path for vCenter Operations and
  
CapacityIQ and an update for Movie Decoder.  These updates address
  
multiple security vulnerabilities.

2. Relevant releases

vCenter Operations prior to 5.0.x
  
vCenter CapacityIQ 1.5.x
  
Movie Decoder prior to 9.0

3. Problem Description

a. VMware Movie Decoder Installer binary planting vulnerability

The installer of the VMware Movie Decoder has a binary planting
  
vulnerability. An attacker who can write their malicious
  
executable to the same folder as where the installer of the
  
Movie Decoder is located may be able to run their code when the
  
installation is started.

VMware would like to thank Mitja Kolsek of ACROS Security for
  
reporting this issue to us.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the name CVE-2012-4897 to this issue.

VMware          Product   Running   Replace with/
  
Product         Version   on        Apply Patch
  
=============   =======   =======   =================
  
Movie Decoder   7.x       Windows   Movie Decoder 9.0
  
Movie Decoder   6.x       Windows   Movie Decoder 9.0
  
Movie Decoder   5.x       Windows   Movie Decoder 9.0

b. vCenter Operations cross-site scripting vulnerability

The vCenter Operations server contains a cross-site scripting
  
vulnerability that allows an attacker to steal an
  
administrator&#8217;s session cookie.  To exploit this vulnerability,
  
the attacker must convince the administrator to click on a
  
malicious link.

VMware would like to thank Alexander Minozhenko of ERPScan for
  
reporting this issue to us.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the name CVE-2012-5050 to this issue.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware          Product   Running   Replace with/
  
Product         Version   on        Apply Patch
  
=============   =======   =======   =================
  
vCOps           5.0.x     any       not affected
  
vCops           1.0.x     any       affected, update to vCOps 5.0.x

c. vCenter CapacityIQ path traversal vulnerability

vCenter CapacityIQ contains a path traversal vulnerability that
  
allows unauthenticated attackers to download arbitrary files.

VMware would like to thank Alexander Minozhenko of ERPScan for
  
reporting this issue to us.

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank">cve.mitre.org</a>)
  
has assigned the name CVE-2012-5051 to this issue.

Column 4 of the following table lists the action required to
  
remediate the vulnerability in each release, if a solution is
  
available.

VMware          Product   Running   Replace with/
  
Product         Version   on        Apply Patch
  
=============   =======   =======   =================
  
vCOps           5.0.x     any       not affected
  
CapacityIQ      1.5.x     any       affected, update to vCOps 5.0.x

4. Solution

Please review the patch/release notes for your product and version
  
and verify the checksum of your downloaded file.

vCenter Operations 5.0.x
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
  
Download link
  
<a href="https://my.vmware.com/web/vmware/info/slug/infrastructure_operations_management/vmware_vcenter_operations/5_0" target="_blank">https://my.vmware.com/web/<wbr>vmware/info/slug/<wbr>infrastructure_operations_<wbr>management/vmware_vcenter_<wbr>operations/5_0</wbr></wbr></wbr></wbr></a>

Release Notes
  
<a href="https://www.vmware.com/support/pubs/vcops-pubs.html" target="_blank">https://www.vmware.com/<wbr>support/pubs/vcops-pubs.html</wbr></a>

Movie Decoder 9.0
  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
  
Download link
  
<a href="https://my.vmware.com/web/vmware/info/slug/desktop_end_user_computing/vmware_workstation/9_0#drivers_tools" target="_blank">https://my.vmware.com/web/<wbr>vmware/info/slug/desktop_end_<wbr>user_computing/vmware_<wbr>workstation/9_0#drivers_tools</wbr></wbr></wbr></a>

5. References
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-4897" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-4897</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5050" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-5050</wbr></a>
  
<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5051" target="_blank">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2012-5051</wbr></a>

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;

6. Change log

2012-10-04 VMSA-2012-0014
  
Initial security advisory in conjunction with the release of Movie
  
Decoder 9.0 on 2012-10-04.

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8211;

7. Contact

E-mail list for product security notifications and announcements:
  
<a href="http://lists.vmware.com/cgi-bin/mailman/listinfo/security-announce" target="_blank">http://lists.vmware.com/cgi-<wbr>bin/mailman/listinfo/security-<wbr>announce</wbr></wbr></a>

This Security Advisory is posted to the following lists:

* security-announce at <a href="http://lists.vmware.com/" target="_blank">lists.vmware.com</a>
  
* bugtraq at <a href="http://securityfocus.com/" target="_blank">securityfocus.com</a>
  
* full-disclosure at <a href="http://lists.grok.org.uk/" target="_blank">lists.grok.org.uk</a>

E-mail: security at <a href="http://vmware.com/" target="_blank">vmware.com</a>
  
PGP key at: <a href="http://kb.vmware.com/kb/1055" target="_blank">http://kb.vmware.com/kb/1055</a>

VMware Security Advisories
  
<a href="http://www.vmware.com/security/advisories" target="_blank">http://www.vmware.com/<wbr>security/advisories</wbr></a>

VMware security response policy
  
<a href="http://www.vmware.com/support/policies/security_response.html" target="_blank">http://www.vmware.com/support/<wbr>policies/security_response.<wbr>html</wbr></wbr></a>

General support life cycle policy
  
<a href="http://www.vmware.com/support/policies/eos.html" target="_blank">http://www.vmware.com/support/<wbr>policies/eos.html</wbr></a>

VMware Infrastructure support life cycle policy
  
<a href="http://www.vmware.com/support/policies/eos_vi.html" target="_blank">http://www.vmware.com/support/<wbr>policies/eos_vi.html</wbr></a>

Copyright 2012 VMware Inc. All rights reserved.</wbr></wbr></wbr></wbr></wbr></wbr></wbr></wbr>