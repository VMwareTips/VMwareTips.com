---
id: 3260
title: 'New VMSA-2016-0017 &#8211; VMware product updates address multiple information disclosure issues'
date: 2016-10-25T22:07:28+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3260
permalink: /2016/10/25/security-announce-new-vmsa-2016-0017-vmware-product-updates-address-multiple-information-disclosure-issues/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1636"
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
            VMSA-2016-0017
          </h2>
          
          <h3>
            VMware product updates address multiple information disclosure issues
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
          <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017a.jpg"><img class="alignnone wp-image-3267" src="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017a.jpg" alt="vmsa-2016-0017a" width="450" height="282" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017a.jpg 562w, http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017a-300x188.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
        </h5>
      </div>
    </div>
  </div>
</div>

<!--more-->

**1. Summary**

VMware product updates address information disclosure issues in VMware Fusion and VMware Tools running on Mac OS X.

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
            <b>a. VMware Tools Information disclosure issue in Mac OS X Virtual  Machines</b>
          </p>
          
          <p>
            An information disclosure vulnerability is present in VMware Tools running on Mac OS X VMs. Successful exploitation of this issue may allow a privileged local user on a system where System Integrity Protection (SIP) is enabled, to obtain kernel memory addresses to bypass the kASLR protection mechanism. SIP is default enabled in the latest versions of Mac OS X.
          </p>
          
          <p>
            There are no known workarounds for this issue.
          </p>
          
          <p>
            VMware would like to thank Marco Grassi (@marcograss) of KeenLab (@keen_lab), Tencent for reporting this issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-5328 to this issue.
          </p>
          
          <p>
            Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is   available.
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
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017b.jpg"><img class="alignnone wp-image-3268" src="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017b.jpg" alt="vmsa-2016-0017b" width="450" height="251" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017b.jpg 561w, http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017b-300x167.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </p>
          
          <p>
            * VMware Tools 10.1.0 can be downloaded independently and installed to resolve this issue.
          </p>
          
          <p>
            ** At the moment, no versions of ESXi and Fusion consume the latest version of VMware Tools i.e. 10.1.0. Remediation of this issue on ESXi and Fusion requires downloading and installation of VMware Tools 10.1.0.
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <b>b. VMware Fusion Information disclosure</b>
          </p>
          
          <p>
            An information disclosure vulnerability is present in VMware Fusion. Successful exploitation of this issue may allow a privileged local user on a system where System Integrity Protection (SIP) is enabled, to obtain kernel memory addresses to bypass the kASLR protection mechanism. SIP is default enabled in the latest versions of Mac OS X.
          </p>
          
          <p>
            There are no known workarounds for this issue.
          </p>
          
          <p>
            VMware would like to thank Marco Grassi (@marcograss) of KeenLab (@keen_lab), Tencent for reporting this issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-5329 to this issue.
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
</div>

<div class="paragraphText parbase section">
  <div class="section-custom ">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12">
          <p>
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017c.jpg"><img class="alignnone wp-image-3269" src="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017c.jpg" alt="vmsa-2016-0017c" width="450" height="139" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017c.jpg 558w, http://vmwaretips.com/wp/wp-content/uploads/2016/10/vmsa-2016-0017c-300x92.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </p>
          
          <p>
            <b>4. Solution</b>
          </p>
          
          <p>
            Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
          </p>
          
          <p>
            VMware Fusion 8.5
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
          </p>
          
          <p>
            Downloads and Documentation:
          </p>
          
          <p>
            <a href="https://www.vmware.com/go/downloadfusion">https://www.vmware.com/go/downloadfusion </a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            VMware Tools 10.1.0
          </p>
          
          <p>
            &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
          </p>
          
          <p>
            Downloads:
          </p>
          
          <p>
            <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VMTOOLS1010&productId=491">https://my.vmware.com/web/vmware/details?downloadGroup=VMTOOLS1010&productId=491</a>
          </p>
          
          <p>
            Documentation:
          </p>
          
          <p>
            <a href="http://pubs.vmware.com/Release_Notes/en/vmwaretools/1010/vmware-tools-1010-release-notes.html">http://pubs.vmware.com/Release_Notes/en/vmwaretools/1010/vmware-tools-1010-release-notes.html</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <b>5. References</b>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5328">CVE-2016-5328</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5329">CVE-2016-5329</a>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <b>6. Change log</b>
          </p>
          
          <p>
            2016-10-25 VMSA-2016-0017 Initial security advisory in conjunction with the release of  VMware Tools 10.1.0 on 2016-10-25.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>