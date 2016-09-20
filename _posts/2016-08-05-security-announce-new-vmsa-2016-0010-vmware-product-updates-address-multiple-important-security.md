---
id: 3111
title: 'New VMSA-2016-0010 &#8211; VMware product updates address multiple important security'
date: 2016-08-05T01:57:01+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=3111
permalink: /2016/08/05/security-announce-new-vmsa-2016-0010-vmware-product-updates-address-multiple-important-security/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 1737
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
  <strong>VMware Security Advisory</strong>
</div>

<div>
</div>

<div>
  Advisory ID: VMSA-2016-0010
</div>

<div>
  Severity:    Important
</div>

<div>
  Synopsis:    VMware product updates address multiple important security
</div>

<div>
  issues
</div>

<div>
  Issue date:  2016-08-04 (Initial Advisory)
</div>

<div>
  Updated on:  2016-08-04
</div>

<div>
  CVE number:  CVE-2016-5330, CVE-2016-5331
</div>

<div>
</div>

<div>
  <strong>1. Summary</strong>
</div>

<div>
</div>

<div>
  VMware product updates address a DLL hijacking issue in Windows-based
</div>

<div>
  VMware Tools and an HTTP Header injection issue in vCenter Server and ESXi.
</div>

<div>
  <!--more-->
</div>

<div>
</div>

<div>
  <strong>2. Relevant Products</strong>
</div>

<div>
</div>

<div>
      VMware vCenter Server
</div>

<div>
      VMware vSphere Hypervisor (ESXi)
</div>

<div>
      VMware Workstation Pro
</div>

<div>
      VMware Workstation Player
</div>

<div>
      VMware Fusion
</div>

<div>
      VMware Tools
</div>

<div>
</div>

<div>
  <strong>3. Problem Description</strong>
</div>

<div>
</div>

<div>
  a. DLL hijacking issue in Windows-based VMware Tools
</div>

<div>
</div>

<div>
</div>

<div>
  A DLL hijacking vulnerability is present in the VMware Tools &#8220;Shared
</div>

<div>
  Folders&#8221; (HGFS) feature
</div>

<div>
  running on Microsoft Windows. Exploitation of this issue may lead to
</div>

<div>
  arbitrary code execution
</div>

<div>
  with the privileges of the victim. In order to exploit this issue, the
</div>

<div>
  attacker would need write
</div>

<div>
  access to a network share and they would need to entice the local user into
</div>

<div>
  opening their document.
</div>

<div>
</div>

<div>
  There are no known workarounds for this issue.
</div>

<div>
</div>

<div>
  VMware would like to thank Yorick Koster of Securify B.V. for reporting
</div>

<div>
  this issue to us.
</div>

<div>
</div>

<div>
  The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org&source=gmail&ust=1471121784822000&usg=AFQjCNH7Z-sCXepSN9YEkYLhAz0huwIE2Q">cve.mitre.org</a>) has
</div>

<div>
  assigned the identifier
</div>

<div>
  CVE-2016-5330 to this issue.
</div>

<div>
</div>

<div>
  Column 5 of the following table lists the action required to remediate the
</div>

<div>
  vulnerability in each
</div>

<div>
  release, if a solution is available.
</div>

<div>
</div>

<div>
     VMware                     Product   Running                    Replace
</div>

<div>
  with/
</div>

<div>
     Product                    Version   on          Severity       Apply
</div>

<div>
  Patch*          Workaround
</div>

<div>
     ===============            =======   =======     ========
</div>

<div>
  =============        ==========
</div>

<div>
     ESXi***                      6.0   ESXi    Important
</div>

<div>
  ESXi600-201603102-SG  None
</div>

<div>
     ESXi***                      5.5   ESXi    Important
</div>

<div>
  ESXi550-201607102-SG  None
</div>

<div>
     ESXi***                      5.1   ESXi    Important
</div>

<div>
  ESXi510-201605102-SG  None
</div>

<div>
     ESXi***                      5.0   ESXi    Important
</div>

<div>
  ESXi500-201606102-SG  None
</div>

<div>
     VMware Workstation Pro       12.1.x    Any       Important       12.1.1
</div>

<div>
                None
</div>

<div>
     VMware Workstation Player    12.1.x    Any       Important       8.1.1
</div>

<div>
                None
</div>

<div>
     VMware Fusion                8.1.x     Mac OS X   Important      8.1.1
</div>

<div>
                None
</div>

<div>
     VMware Tools                 10.0.5    Windows    Important
</div>

<div>
  10.0.6**              None
</div>

<div>
</div>

<div>
  * After the update or patch is applied, VMware Tools must also be updated
</div>

<div>
  in any
</div>

<div>
  Windows-based guests that include the &#8220;Shared Folders&#8221; (HGFS) feature to
</div>

<div>
  resolve
</div>

<div>
  CVE-2016-5330.
</div>

<div>
</div>

<div>
  ** VMware Tools can be downloaded independently and installed to resolve
</div>

<div>
  this issue.
</div>

<div>
</div>

<div>
  *** Successfully exploiting this issue requires installation of &#8220;Shared
</div>

<div>
  Folders&#8221; component (HGFS
</div>

<div>
  feature) which does not get installed in &#8220;custom/typical&#8221; installation of
</div>

<div>
  VMware Tools on
</div>

<div>
  Windows VM running on ESXi.
</div>

<div>
</div>

<div>
</div>

<div>
  b. HTTP Header injection issue in vCenter Server and ESXi
</div>

<div>
</div>

<div>
  vCenter Server and ESXi contain an HTTP header injection vulnerability due
</div>

<div>
  to lack of input
</div>

<div>
  validation. An attacker can exploit this issue to set arbitrary HTTP
</div>

<div>
  response headers and
</div>

<div>
  cookies, which may allow for cross-site scripting and malicious redirect
</div>

<div>
  attacks.
</div>

<div>
</div>

<div>
  There are no known workarounds for this issue.
</div>

<div>
</div>

<div>
  VMware would like to thank Vladimir Ivanov, Andrey Evlanin, Mikhail
</div>

<div>
  Stepankin, Artem
</div>

<div>
  Kondratenko, Arseniy Sharoglazov of Positive Technologies, Matt Foster of
</div>

<div>
  Netcraft Ltd,
</div>

<div>
  Matthias Deeg of SySS GmbH, Eva Esteban Molina of A2secure? and Ammarit
</div>

<div>
  Thongthua for
</div>

<div>
  independently reporting this issue to us.
</div>

<div>
</div>

<div>
</div>

<div>
</div>

<div>
  The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org&source=gmail&ust=1471121784822000&usg=AFQjCNH7Z-sCXepSN9YEkYLhAz0huwIE2Q">cve.mitre.org</a>) has
</div>

<div>
  assigned the identifier
</div>

<div>
  CVE-2016-5331 to this issue.
</div>

<div>
</div>

<div>
</div>

<div>
</div>

<div>
  Column 5 of the following table lists the action required to remediate the
</div>

<div>
  vulnerability in each release, if a solution is available.
</div>

<div>
</div>

<div>
      VMware            Product   Running                    Replace with/
</div>

<div>
     Product            Version   on         Severity        Apply Patch
</div>

<div>
           Workaround
</div>

<div>
     ===============    =======   =======    ========        =============
</div>

<div>
           ==========
</div>

<div>
     vCenter Server    6.0     Any        Important        6.0 U2
</div>

<div>
         None
</div>

<div>
     vCenter Server    5.x     Any           n/a           not affected
</div>

<div>
         None
</div>

<div>
     ESXi                6.0     ESXi    Important
</div>

<div>
  ESXi600-201603101-SG     None
</div>

<div>
     ESXi                5.x     ESXi          n/a           not affected
</div>

<div>
           None
</div>

<div>
</div>

<div>
  <strong>4. Solution</strong>
</div>

<div>
</div>

<div>
  Please review the patch/release notes for your product and version and
</div>

<div>
  verify the
</div>

<div>
  checksum of your downloaded file.
</div>

<div>
</div>

<div>
  vCenter Server
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
</div>

<div>
  Downloads and Documentation:
</div>

<div>
  <a href="https://www.vmware.com/go/download-vsphere" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/go/download-vsphere&source=gmail&ust=1471121784822000&usg=AFQjCNE23zcRtAeHsiNla6_DGAxOw0IoIg">https://www.vmware.com/go/<wbr>download-vsphere</wbr></a>
</div>

<div>
</div>

<div>
  ESXi 6.0
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;-
</div>

<div>
  Downloads:
</div>

<div>
  <a href="https://www.vmware.com/patchmgr/findPatch.portal" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/patchmgr/findPatch.portal&source=gmail&ust=1471121784822000&usg=AFQjCNGGR_KzGbzMFjEks1Feocp-buws2g">https://www.vmware.com/<wbr>patchmgr/findPatch.portal</wbr></a>
</div>

<div>
  Documentation:
</div>

<div>
  <a href="http://kb.vmware.com/kb/2142192" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://kb.vmware.com/kb/2142192&source=gmail&ust=1471121784822000&usg=AFQjCNEH4IYkYeOIR4wtbuElW4ld6gpZ2g">http://kb.vmware.com/kb/<wbr>2142192</wbr></a> (CVE-2016-5331)
</div>

<div>
  <a href="http://kb.vmware.com/kb/2142193" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://kb.vmware.com/kb/2142193&source=gmail&ust=1471121784822000&usg=AFQjCNGywoGX6CSV1PFlO6SPsjOzqTRwTg">http://kb.vmware.com/kb/<wbr>2142193</wbr></a> (CVE-2016-5330)
</div>

<div>
</div>

<div>
  ESXi 5.5
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;
</div>

<div>
  Downloads:
</div>

<div>
  <a href="https://www.vmware.com/patchmgr/findPatch.portal" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/patchmgr/findPatch.portal&source=gmail&ust=1471121784822000&usg=AFQjCNGGR_KzGbzMFjEks1Feocp-buws2g">https://www.vmware.com/<wbr>patchmgr/findPatch.portal</wbr></a>
</div>

<div>
  Documentation:
</div>

<div>
  <a href="http://kb.vmware.com/kb/2144370" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://kb.vmware.com/kb/2144370&source=gmail&ust=1471121784822000&usg=AFQjCNEYUX_TJyWaoi8IBfpPAEFV20S2ug">http://kb.vmware.com/kb/<wbr>2144370</wbr></a>
</div>

<div>
</div>

<div>
  ESXi 5.1
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8211;
</div>

<div>
  Downloads:
</div>

<div>
  <a href="https://www.vmware.com/patchmgr/findPatch.portal" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/patchmgr/findPatch.portal&source=gmail&ust=1471121784822000&usg=AFQjCNGGR_KzGbzMFjEks1Feocp-buws2g">https://www.vmware.com/<wbr>patchmgr/findPatch.portal</wbr></a>
</div>

<div>
  Documentation:
</div>

<div>
  <a href="http://kb.vmware.com/kb/2141434" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://kb.vmware.com/kb/2141434&source=gmail&ust=1471121784822000&usg=AFQjCNHLWN4bxqug6irJWEoLJUQZ8xzuOg">http://kb.vmware.com/kb/<wbr>2141434</wbr></a>
</div>

<div>
</div>

<div>
  ESXi 5.0
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;
</div>

<div>
  Downloads:
</div>

<div>
  <a href="https://www.vmware.com/patchmgr/findPatch.portal" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/patchmgr/findPatch.portal&source=gmail&ust=1471121784822000&usg=AFQjCNGGR_KzGbzMFjEks1Feocp-buws2g">https://www.vmware.com/<wbr>patchmgr/findPatch.portal</wbr></a>
</div>

<div>
  Documentation:
</div>

<div>
  <a href="http://kb.vmware.com/kb/2144027" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://kb.vmware.com/kb/2144027&source=gmail&ust=1471121784822000&usg=AFQjCNH5BitPtE9wJGKsgcURoW0Peh0mMw">http://kb.vmware.com/kb/<wbr>2144027</wbr></a>
</div>

<div>
</div>

<div>
  VMware Workstation Pro 12.1.1
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8211;</wbr>
</div>

<div>
  Downloads and Documentation:
</div>

<div>
  <a href="https://www.vmware.com/go/downloadworkstationpro" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/go/downloadworkstationpro&source=gmail&ust=1471121784822000&usg=AFQjCNFiYb6ZnO9-Wzub2jLMerfBnBzWDQ">https://www.vmware.com/go/<wbr>downloadworkstationpro</wbr></a>
</div>

<div>
</div>

<div>
  VMware Workstation Player 12.1.1
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr>&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;</wbr>
</div>

<div>
  Downloads and Documentation:
</div>

<div>
  <a href="https://www.vmware.com/go/downloadplayer" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/go/downloadplayer&source=gmail&ust=1471121784822000&usg=AFQjCNFJop9RotuI4e6UHHinRwcz1nvmyg">https://www.vmware.com/go/<wbr>downloadplayer</wbr></a>
</div>

<div>
</div>

<div>
  VMware Fusion 8.1.1
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
</div>

<div>
  Downloads and Documentation:
</div>

<div>
  <a href="https://www.vmware.com/go/downloadfusion" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://www.vmware.com/go/downloadfusion&source=gmail&ust=1471121784822000&usg=AFQjCNF4hiEhLzXdT3w2wxCjK8kRKxb6TQ">https://www.vmware.com/go/<wbr>downloadfusion</wbr></a>
</div>

<div>
</div>

<div>
  VMware Tools 10.0.6
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
</div>

<div>
  Downloads:
</div>

<div>
  <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VMTOOLS1006&productI" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://my.vmware.com/web/vmware/details?downloadGroup%3DVMTOOLS1006%26productI&source=gmail&ust=1471121784822000&usg=AFQjCNEeY8alsW0qjwggKE_n-7_cEKbSzg">https://my.vmware.com/web/<wbr>vmware/details?downloadGroup=<wbr>VMTOOLS1006&productI</wbr></wbr></a>
</div>

<div>
  d=491
</div>

<div>
  Documentation:
</div>

<div>
  <a href="http://pubs.vmware.com/Release_Notes/en/vmwaretools/1006/vmware-tools-1006-" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://pubs.vmware.com/Release_Notes/en/vmwaretools/1006/vmware-tools-1006-&source=gmail&ust=1471121784822000&usg=AFQjCNGithF5hzbbnY0zzJBGbsjj4e9gSg">http://pubs.vmware.com/<wbr>Release_Notes/en/vmwaretools/<wbr>1006/vmware-tools-1006-</wbr></wbr></a>
</div>

<div>
  release-notes.html
</div>

<div>
</div>

<div>
</div>

<div>
  <strong>5. References</strong>
</div>

<div>
</div>

<div>
      <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5330" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org/cgi-bin/cvename.cgi?name%3DCVE-2016-5330&source=gmail&ust=1471121784822000&usg=AFQjCNEvAjfTbzcO53C8r2tdPMreTkFGmw">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2016-5330</wbr></a>
</div>

<div>
      <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5331" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org/cgi-bin/cvename.cgi?name%3DCVE-2016-5331&source=gmail&ust=1471121784822000&usg=AFQjCNGJoEUGCx-IpV_bXjHlTkjvXAeI9Q">http://cve.mitre.org/cgi-bin/<wbr>cvename.cgi?name=CVE-2016-5331</wbr></a>
</div>

<div>
</div>

<div>
  <strong>6. Change log</strong>
</div>

<div>
</div>

<div>
     2016-08-04 VMSA-2016-0010 Initial security advisory in conjunction with
</div>

<div>
  the release of
</div>

<div>
     VMware ESXi 5.5 patches on 2016-08-04.
</div>

<div>
</div>