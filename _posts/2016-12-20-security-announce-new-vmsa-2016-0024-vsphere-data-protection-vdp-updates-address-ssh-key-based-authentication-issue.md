---
id: 3347
title: NEW VMSA-2016-0024 vSphere Data Protection (VDP) updates address SSH Key-Based authentication issue
date: 2016-12-20T12:01:45+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3347
permalink: /2016/12/20/security-announce-new-vmsa-2016-0024-vsphere-data-protection-vdp-updates-address-ssh-key-based-authentication-issue/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1882"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
VMware Security Advisory

Advisory ID: VMSA-2016-0024

Severity:    Critical

Synopsis:    vSphere Data Protection (VDP) updates address SSH Key-Based

authentication issue

Issue date:  2016-12-20

Updated on:  2016-12-20 (Initial Advisory)

CVE number:  CVE-2016-7456

&nbsp;

  1. Summary

&nbsp;

vSphere Data Protection (VDP) updates address SSH key-based

authentication issue

&nbsp;

<ol start="2">
  <li>
    Relevant Products
  </li>
</ol>

&nbsp;

vSphere Data Protection (VDP)

<!--more-->

&nbsp;

<ol start="3">
  <li>
    Problem Description
  </li>
</ol>

&nbsp;

  1. VDP SSH key-based authentication issue

&nbsp;

VDP contains a private SSH key with a known password that is configured

to allow key-based authentication. Exploitation of this issue may allow

an unauthorized remote attacker to log into the appliance with root

privileges.

&nbsp;

VMware would like to thank Marc Ströbel aka phroxvs from HvS-Consulting

for reporting this issue to VMware.

&nbsp;

The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org&source=gmail&ust=1482415763148000&usg=AFQjCNEwKavXRwsIPzp83WeqSXe2bkGlDw">cve.mitre.org</a>) has

assigned the identifier CVE-2016-7456 to this issue.

&nbsp;

Column 5 of the following table lists the action required to remediate

the vulnerability in each release, if a solution is available.

&nbsp;

VMware      Product    Running            Replace with/     Mitigation/

Product     Version    on       Severity  Apply Patch       Workaround

==========  =========  =======  ========  ================  ==========

VDP         6.1.x      VA       Critical  KB2147069         None

VDP         6.0.x      VA       Critical  KB2147069         None

VDP         5.8.x      VA       Critical  KB2147069         None

VDP         5.5.x      VA       Critical  KB2147069         None

&nbsp;

<ol start="4">
  <li>
    Solution
  </li>
</ol>

&nbsp;

Please review the patch/release notes for your product and version and

verify the checksum of your downloaded file.

&nbsp;

vSphere Data Protection

Downloads and Documentation:

<a href="http://kb.vmware.com/kb/2147069" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://kb.vmware.com/kb/2147069&source=gmail&ust=1482415763148000&usg=AFQjCNHIRSUt_7pT9JMHsDeIlStYCUmBZQ">http://kb.vmware.com/kb/2147069</a>

&nbsp;

<ol start="5">
  <li>
    References
  </li>
</ol>

&nbsp;

<a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7456" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org/cgi-bin/cvename.cgi?name%3DCVE-2016-7456&source=gmail&ust=1482415763148000&usg=AFQjCNGgM3F2foYGDaf6bjvJfqfYWCJgRA">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7456</a>

&nbsp;

&#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;

&nbsp;

<ol start="6">
  <li>
    Change log
  </li>
</ol>

&nbsp;

2016-12-20: VMSA-2016-0024

Initial security advisory in conjunction with the release of vSphere

Data Protection updates on 2016-12-20.