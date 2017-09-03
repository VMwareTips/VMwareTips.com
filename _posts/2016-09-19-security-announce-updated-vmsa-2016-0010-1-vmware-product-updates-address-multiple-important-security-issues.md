---
id: 3223
title: '[Security-announce] Updated VMSA-2016-0010.1- VMware product updates address multiple important security issues'
date: 2016-09-19T12:24:43+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3223
permalink: /2016/09/19/security-announce-updated-vmsa-2016-0010-1-vmware-product-updates-address-multiple-important-security-issues/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1687"
dsq_thread_id:
  - "5156841551"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
<div class="paragraphText parbase section">
  <div class="section-custom ">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12">
          <h2>
            VMSA-2016-0010.1
          </h2>
          
          <h3>
            VMware product updates address multiple important security issues
          </h3>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="comparisonTable section">
  <div id="columncontainer1columncontainercomparisontable" class="rTable">
    <div class="rTableHeading">
      <div class="rTableHead" data-heading="headingOne">
        <h5>
          VMware Security Advisory
        </h5>
      </div>
      
      <div class="rTableHead" data-heading="headingTwo">
        <h5>
           <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-a.jpg"><img class="alignnone wp-image-3230" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-a.jpg" alt="vmsa20160010-1-a" width="450" height="289" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-a.jpg 745w, http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-a-300x192.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
        </h5>
      </div>
    </div>
  </div>
</div>

<!--more-->

<div class="paragraphText parbase section">
  <div class="section-custom ">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12">
          <h5>
            1. Summary
          </h5>
          
          <p>
            VMware product updates address a DLL hijacking issue in Windows-based<br /> VMware Tools and an HTTP Header injection issue in vCenter Server and ESXi.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="paragraphText parbase section">
  <div class="section-custom ">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12">
          <h5>
            2. Relevant Products
          </h5>
          
          <ul>
            <li>
              VMware vCenter Server
            </li>
            <li>
              VMware vSphere Hypervisor (ESXi)
            </li>
            <li>
              VMware Workstation Pro
            </li>
            <li>
              VMware Workstation Player
            </li>
            <li>
              VMware Fusion
            </li>
            <li>
              VMware Tools
            </li>
          </ul>
          
          <h5>
            3. Problem Description
          </h5>
          
          <p>
            <b>a. DLL hijacking issue in Windows-based VMware Tools  </b>
          </p>
          
          <p>
            A DLL hijacking vulnerability is present in the VMware Tools &#8220;Shared Folders&#8221; (HGFS) feature running on Microsoft Windows. Exploitation of this issue may lead to arbitrary code execution with the privileges of the victim. In order to exploit this issue, the attacker would need write access to a network share and they would need to entice the local user into opening their document.
          </p>
          
          <p>
            There are no known workarounds for this issue.
          </p>
          
          <p>
            VMware would like to thank Yorick Koster of <a href="https://securify.nl/">Securify B.V.</a> for reporting this issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-5330 to this issue.
          </p>
          
          <p>
            Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
          </p>
          
          <p>
            &nbsp;
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="comparisonTable section">
</div>

<div class="paragraphText parbase section">
  <div class="section-custom ">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12">
          <p>
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-b.jpg"><img class="alignnone wp-image-3231" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-b.jpg" alt="vmsa20160010-1-b" width="450" height="646" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-b.jpg 560w, http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-b-209x300.jpg 209w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </p>
          
          <p>
            <b>*</b> After the update or patch is applied, VMware Tools must also be updated in any Windows-based guests that include the &#8220;Shared Folders&#8221; (HGFS) feature to resolve CVE-2016-5330.
          </p>
          
          <p>
            <b>**</b> VMware Tools can be downloaded independently and installed to resolve this issue.
          </p>
          
          <p>
            <b>***</b> Successfully exploiting this issue requires installation of &#8220;Shared Folders&#8221; component (HGFS feature) which does not get installed in &#8220;custom/typical&#8221; installation of VMware Tools on Windows VM running on ESXi.
          </p>
          
          <p>
            <b>b. HTTP Header injection issue in vCenter Server and ESXi</b>
          </p>
          
          <p>
            vCenter Server and ESXi contain an HTTP header injection vulnerability due to lack of input validation. An attacker can exploit this issue to set arbitrary HTTP response headers and cookies, which may allow for cross-site scripting and malicious redirect attacks.
          </p>
          
          <p>
            There are no known workarounds for this issue.
          </p>
          
          <p>
            VMware would like to thank Vladimir Ivanov, Andrey Evlanin, Mikhail Stepankin, Artem Kondratenko, Arseniy Sharoglazov of Positive Technologies, Matt Foster of Netcraft Ltd, Matthias Deeg of SySS GmbH, Eva Esteban Molina of <a href="https://www.a2secure.com/">A2secure</a> and Ammarit Thongthua for independently reporting this issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-5331 to this issue.
          </p>
          
          <p>
            Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="comparisonTable section">
  <div id="columncontainer1columncontainercomparisontable_9323" class="rTable">
    <div class="rTableHeading">
    </div>
    
    <p>
      <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-c.jpg"><img class="alignnone wp-image-3232" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-c.jpg" alt="vmsa20160010-1-c" width="451" height="310" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-c.jpg 561w, http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa20160010-1-c-300x206.jpg 300w" sizes="(max-width: 451px) 100vw, 451px" /></a>
    </p>
    
    <div class="rTableBody">
    </div>
  </div>
</div>

<div class="paragraphText parbase section">
  <div class="section-custom ">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12">
          <p>
            <b>4. Solution</b>
          </p>
          
          <p>
            Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
          </p>
          
          <p>
            <strong>vCenter Server</strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
          </p>
          
          <p>
            Downloads and Documentation:
          </p>
          
          <p>
            <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>ESXi 6.0  </strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;-
          </p>
          
          <p>
            Downloads:
          </p>
          
          <p>
            <a href="https://www.vmware.com/patchmgr/findPatch.portal">https://www.vmware.com/patchmgr/findPatch.portal</a>
          </p>
          
          <p>
            Documentation:
          </p>
          
          <p>
            <a href="http://kb.vmware.com/kb/2142192">http://kb.vmware.com/kb/2142192</a> (CVE-2016-5331)
          </p>
          
          <p>
            <a href="http://kb.vmware.com/kb/2142193">http://kb.vmware.com/kb/2142193</a> (CVE-2016-5330)
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>ESXi 5.5 </strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;
          </p>
          
          <p>
            Downloads:
          </p>
          
          <p>
            <a href="https://www.vmware.com/patchmgr/findPatch.portal">https://www.vmware.com/patchmgr/findPatch.portal</a>
          </p>
          
          <p>
            Documentation:
          </p>
          
          <p>
            <a href="http://kb.vmware.com/kb/2144370">http://kb.vmware.com/kb/2144370</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>ESXi 5.1   </strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8211;
          </p>
          
          <p>
            Downloads:
          </p>
          
          <p>
            <a href="https://www.vmware.com/patchmgr/findPatch.portal">https://www.vmware.com/patchmgr/findPatch.portal</a>
          </p>
          
          <p>
            Documentation:
          </p>
          
          <p>
            <a href="http://kb.vmware.com/kb/2141434">http://kb.vmware.com/kb/2141434</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>ESXi 5.0</strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;
          </p>
          
          <p>
            Downloads:
          </p>
          
          <p>
            <a href="https://www.vmware.com/patchmgr/findPatch.portal">https://www.vmware.com/patchmgr/findPatch.portal</a>
          </p>
          
          <p>
            Documentation:
          </p>
          
          <p>
            <a href="http://kb.vmware.com/kb/2144027">http://kb.vmware.com/kb/2144027</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>VMware Workstation Pro 12.1.1</strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
          </p>
          
          <p>
            Downloads and Documentation:
          </p>
          
          <p>
            <a href="https://www.vmware.com/go/downloadworkstationpro">https://www.vmware.com/go/downloadworkstationpro</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>VMware Workstation Player 12.1.1  </strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
          </p>
          
          <p>
            Downloads and Documentation:
          </p>
          
          <p>
            <a href="https://www.vmware.com/go/downloadplayer">https://www.vmware.com/go/downloadplayer</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>VMware Fusion 8.1.1  </strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
          </p>
          
          <p>
            Downloads and Documentation:
          </p>
          
          <p>
            <a href="https://www.vmware.com/go/downloadfusion">https://www.vmware.com/go/downloadfusion</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>VMware Tools 10.0.6</strong>
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
          </p>
          
          <p>
            Downloads:
          </p>
          
          <p>
            <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VMTOOLS1006&productId=491">https://my.vmware.com/web/vmware/details?downloadGroup=VMTOOLS1006&productId=491</a>
          </p>
          
          <p>
            Documentation:
          </p>
          
          <p>
            <a href="http://pubs.vmware.com/Release_Notes/en/vmwaretools/1006/vmware-tools-1006-release-notes.html">http://pubs.vmware.com/Release_Notes/en/vmwaretools/1006/vmware-tools-1006-release-notes.html</a>
          </p>
          
          <p>
            <b>5. References</b>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5330" name="&lpos=content_security : 248">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5330</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5331" name="&lpos=content_security : 249">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5331</a>
          </p>
          
          <p>
            <b>6. Change log</b>
          </p>
          
          <p>
            2016-08-04 VMSA-2016-0010 Initial security advisory in conjunction with the release of VMware ESXi 5.5 patches on 2016-08-04.
          </p>
          
          <p>
            2016-09-19 VMSA-2016-0010.1 Updated security advisory to clarify the affected versions of VMware tools.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>