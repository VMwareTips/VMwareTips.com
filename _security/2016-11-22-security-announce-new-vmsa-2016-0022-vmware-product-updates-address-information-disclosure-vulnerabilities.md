---
id: 3296
title: VMSA-2016-0022 VMware product updates address information disclosure vulnerabilities
date: 2016-11-22T14:38:47+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3296
permalink: /2016/11/22/security-announce-new-vmsa-2016-0022-vmware-product-updates-address-information-disclosure-vulnerabilities/
redirect_from: /wp/2016/11/22/security-announce-new-vmsa-2016-0022-vmware-product-updates-address-information-disclosure-vulnerabilities/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1960"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
##### [<img class="alignnone wp-image-3305" src="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-a.jpg" alt="vmsa-2016-0022-a" width="450" height="307" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-a.jpg 558w, http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-a-300x205.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" />](http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-a.jpg)



##### 1. Summary

VMware vCenter Server, vSphere Client, and vRealize Automation updates address information disclosure vulnerabilities.

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
              VMware vSphere Client
            </li>
            <li>
              vRealize Automation
            </li>
          </ul>
          
          <h5>
            3. Problem Description
          </h5>
          
          <p>
            <b>a. vSphere Client XML External Entity vulnerability<br /> </b>
          </p>
          
          <p>
            The vSphere Client contains an XML External Entity (XXE) vulnerability. This issue can lead to information disclosure if a vSphere Client user is tricked into connecting to a malicious instance of vCenter Server or ESXi.
          </p>
          
          <p>
            There are no known workarounds for this issue.
          </p>
          
          <p>
            VMware would like to thank Vladimir Ivanov, Andrey Evlanin, Mikhail   Stepankin, Artem Kondratenko, Arseniy Sharoglazov of Positive Technologies for reporting this issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-7458 to this issue.
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
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-b.jpg"><img class="alignnone wp-image-3306" src="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-b.jpg" alt="vmsa-2016-0022-b" width="451" height="196" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-b.jpg 559w, http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-b-300x130.jpg 300w" sizes="(max-width: 451px) 100vw, 451px" /></a>
          </p>
          
          <p>
            * In order to remediate the vulnerability, the vSphere Client will need to be uninstalled and re-installed. A fixed version of the vSphere Client can be obtained from:
          </p>
          
          <ul>
            <li>
              vCenter Server 6.0 U2a
            </li>
            <li>
              vCenter Server 5.5 U3e
            </li>
            <li>
              VMware Knowledge Base article 2089791
            </li>
          </ul>
          
          <p>
            The build numbers of the fixed client versions may be found in VMware Knowledge Base article 2089791.
          </p>
          
          <p>
            <b>b. vCenter Server XML External Entity vulnerability<br /> </b>
          </p>
          
          <p>
            vCenter Server contains an XML External Entity (XXE) vulnerability in the Log Browser, the Distributed Switch setup, and the Content Library. A specially crafted XML request issued to the server by an  authorized user may lead to unintended information disclosure.
          </p>
          
          <p>
            There are no known workarounds for this issue.
          </p>
          
          <p>
            VMware would like to thank Vladimir Ivanov, Andrey Evlanin, Mikhail Stepankin, Artem Kondratenko, Arseniy Sharoglazov of Positive Technologies, and Lukasz Plonka for independently for reporting this  issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-7459 to this issue.
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
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-c.jpg"><img class="alignnone wp-image-3307" src="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-c.jpg" alt="vmsa-2016-0022-c" width="450" height="252" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-c.jpg 568w, http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-c-300x168.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </p>
          
          <p>
            <b>c. vCenter Server and vRealize Automation XML External Entity vulnerability<br /> </b>
          </p>
          
          <p>
            vCenter Server and vRealize Automation contain an XML External Entity (XXE) vulnerability in the Single Sign-On functionality. A specially crafted XML request issued to the server may lead to a Denial of Service or to unintended information disclosure.
          </p>
          
          <p>
            There are no known workarounds for this issue.
          </p>
          
          <p>
            VMware would like to thank Vladimir Ivanov, Andrey Evlanin, Mikhail Stepankin, Artem Kondratenko, Arseniy Sharoglazov of Positive Technologies for reporting this issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-7460 to this issue.
          </p>
          
          <p>
            Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
          </p>
          
          <p>
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-d.jpg"><img class="alignnone wp-image-3308" src="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-d.jpg" alt="vmsa-2016-0022-d" width="450" height="369" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-d.jpg 557w, http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0022-d-300x246.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
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
            <b>4. Solution</b>
          </p>
          
          <p>
            Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
          </p>
          
          <p>
            <b>vCenter Server</b>
          </p>
          
          <p>
            Downloads and Documentation:
          </p>
          
          <p>
            <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a>
          </p>
          
          <p>
            <b>vRealize Automation</b>
          </p>
          
          <p>
            Downloads and Documentation:
          </p>
          
          <p>
            <a href="https://my.vmware.com/web/vmware/info/slug/infrastructure_operations_management/vmware_vrealize_automation/6_2">https://my.vmware.com/web/vmware/info/slug/infrastructure_operations_management/vmware_vrealize_automation/6_2</a>
          </p>
          
          <p>
            <b>5. References</b>
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
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7458">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7458</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7459">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7459</a>
          </p>
          
          <p>
            <a href="https://kb.vmware.com/kb/2089791">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7460</a>
          </p>
          
          <p>
            <a href="https://kb.vmware.com/kb/2089791">VMware Knowledge Base article 2089791<br /> </a>
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
          <p>
            <b>6. Change log</b><br /> 2016-11-22 VMSA-2016-0022
          </p>
          
          <p>
            Initial security advisory in conjunction with the release of vSphere 6.0 U2a on 2016-11-22.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>