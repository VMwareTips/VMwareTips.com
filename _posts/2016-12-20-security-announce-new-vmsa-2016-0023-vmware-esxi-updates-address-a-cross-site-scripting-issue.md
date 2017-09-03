---
id: 3343
title: NEW VMSA-2016-0023 VMware ESXi updates address a cross-site scripting issue
date: 2016-12-20T08:01:29+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3343
permalink: /2016/12/20/security-announce-new-vmsa-2016-0023-vmware-esxi-updates-address-a-cross-site-scripting-issue/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1946"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
<div>
  VMware Security Advisory
</div>

<div>
</div>

<div>
  Advisory ID: VMSA-2016-0023
</div>

<div>
  Severity:    Important
</div>

<div>
  Synopsis:    VMware ESXi updates address a cross-site
</div>

<div>
               scripting issue
</div>

<div>
</div>

<div>
  Issue date:  <span class="aBn" tabindex="0" data-term="goog_1837638970"><span class="aQJ">2016-12-20</span></span>
</div>

<div>
  Updated on:  <span class="aBn" tabindex="0" data-term="goog_1837638971"><span class="aQJ">2016-12-20</span></span> (Initial Advisory)
</div>

<div>
  CVE number:  CVE-2016-7463
</div>

<div>
</div>

<div>
  1. Summary
</div>

<div>
</div>

<div>
     VMware ESXi updates address a cross-site scripting issue.
</div>

<div>
</div>

<div>
  2. Relevant Releases
</div>

<div>
</div>

<div>
     VMware vSphere Hypervisor (ESXi)
</div>

<div>
</div>

<!--more-->

<div>
</div>

<div>
  3. Problem Description
</div>

<div>
</div>

<div>
     a. Host Client stored cross-site scripting issue
</div>

<div>
</div>

<div>
     The ESXi Host Client contains a vulnerability that may allow for
</div>

<div>
     stored cross-site scripting (XSS). The issue can be introduced by
</div>

<div>
     an attacker that has permission to manage virtual machines through
</div>

<div>
     ESXi Host Client or by tricking the vSphere administrator to import
</div>

<div>
     a specially crafted VM. The issue may be triggered on the system
</div>

<div>
     from where ESXi Host Client is used to manage the specially crafted
</div>

<div>
     VM.
</div>

<div>
</div>

<div>
     VMware advises not to import VMs from untrusted sources.
</div>

<div>
</div>

<div>
     VMware would like to thank Caleb Watt (@calebwatt15) for reporting
</div>

<div>
     this issue to us.
</div>

<div>
</div>

<div>
     The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org&source=gmail&ust=1482336058924000&usg=AFQjCNHfhPYk3pU_C6sRcqN7Ty4WUYYB0w">cve.mitre.org</a>) has
</div>

<div>
     assigned the identifier CVE-2016-7463 to this issue.
</div>

<div>
</div>

<div>
     Column 4 of the following table lists the action required to
</div>

<div>
     remediate the vulnerability in each release, if a solution is
</div>

<div>
     available.
</div>

<div>
</div>

<div>
     VMware  Product Running             Replace with/
</div>

<div>
     Product Version on       Severity    Apply Patch*        Workaround
</div>

<div>
     ======= ======= =======  ========   =============        ==========
</div>

<div>
     ESXi     6.5    ESXi    N/A        not affected           N/A
</div>

<div>
     ESXi     6.0    ESXi    Important  ESXi600-201611102-SG   None
</div>

<div>
     ESXi     5.5    ESXi    Important  ESXi550-201612102-SG   None
</div>

<div>
</div>

<div>
     *The fling version which resolves this issue is 1.13.0.
</div>

<div>
</div>

<div>
  4. Solution
</div>

<div>
</div>

<div>
     Please review the patch/release notes for your product and
</div>

<div>
     version and verify the checksum of your downloaded file.
</div>

<div>
</div>

<div>
     ESXi 6.0
</div>

<div>
     &#8212;&#8212;&#8212;&#8212;-
</div>

<div>
     Downloads:
</div>

<div>
     <a href="https://www.vmware.com/patchmgr/findPatch.portal" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/patchmgr/findPatch.portal&source=gmail&ust=1482336058924000&usg=AFQjCNHqwfLWDR1ox2KBnumUqV2N7yuSJg">https://www.vmware.com/<wbr />patchmgr/findPatch.portal</a>
</div>

<div>
     Documentation:
</div>

<div>
     <a href="http://kb.vmware.com/kb/2145815" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://kb.vmware.com/kb/2145815&source=gmail&ust=1482336058924000&usg=AFQjCNEjB4RNx2mNJwYF4IChAN15R-CcOw">http://kb.vmware.com/kb/<wbr />2145815</a>
</div>

<div>
</div>

<div>
     ESXi 5.5
</div>

<div>
     &#8212;&#8212;&#8212;&#8212;
</div>

<div>
     Downloads:
</div>

<div>
     <a href="https://www.vmware.com/patchmgr/findPatch.portal" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/patchmgr/findPatch.portal&source=gmail&ust=1482336058924000&usg=AFQjCNHqwfLWDR1ox2KBnumUqV2N7yuSJg">https://www.vmware.com/<wbr />patchmgr/findPatch.portal</a>
</div>

<div>
     Documentation:
</div>

<div>
     <a href="http://kb.vmware.com/kb/2148194" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://kb.vmware.com/kb/2148194&source=gmail&ust=1482336058924000&usg=AFQjCNFJcSl3_jiXTRbfKnoT8DlPnvKgqw">http://kb.vmware.com/kb/<wbr />2148194</a>
</div>

<div>
</div>

<div>
</div>

<div>
  5. References
</div>

<div>
</div>

<div>
     <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7463" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org/cgi-bin/cvename.cgi?name%3DCVE-2016-7463&source=gmail&ust=1482336058924000&usg=AFQjCNEfSzXq9FlYAznlHmvw5UnNRgk-vg">http://cve.mitre.org/cgi-bin/<wbr />cvename.cgi?name=CVE-2016-7463</a>
</div>

<div>
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr />&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr />&#8212;&#8212;&#8212;&#8211;
</div>

<div>
</div>

<div>
  6. Change log
</div>

<div>
</div>

<div>
     <span class="aBn" tabindex="0" data-term="goog_1837638972"><span class="aQJ">2016-12-20</span></span> VMSA-2016-0023
</div>

<div>
     Initial security advisory in conjunction with the release of VMware
</div>

<div>
     ESXi 5.5 patches on <span class="aBn" tabindex="0" data-term="goog_1837638973"><span class="aQJ">2016-12-20</span></span>.
</div>