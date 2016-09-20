---
id: 3206
title: 'NEW VMSA-2016-0014 &#8211; VMware ESXi, Workstation, Fusion, and Tools updates address multiple security issues'
date: 2016-09-13T11:45:09+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=3206
permalink: /2016/09/13/security-announce-new-vmsa-2016-0014-vmware-esxi-workstation-fusion-and-tools-updates-address-multiple-security-issues/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 566
dsq_thread_id:
  - 5157029064
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
## VMSA-2016-0014

### VMware ESXi, Workstation, Fusion, and Tools updates address multiple security issues

[<img class="alignnone wp-image-3215" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-1.jpg" alt="vmsa-2016-0014-1" width="450" height="368" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-1.jpg 738w, http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-1-300x246.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" />](http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-1.jpg)

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
            VMware ESXi, Workstation, Fusion, and Tools updates address multiple security issues
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
              ESXi
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
            <b>a. VMware Workstation heap-based buffer overflow vulnerabilities via Cortado ThinPrint </b>
          </p>
          
          <p>
            VMware Workstation contains vulnerabilities that may allow a Windows-based Virtual Machine (VM) to trigger a heap-based buffer overflow. Exploitation of these issues may lead to arbitrary code execution in VMware Workstation running on Windows.
          </p>
          
          <p>
            Exploitation is only possible if virtual printing has been enabled in VMware Workstation. This feature is not enabled by default. VMware Knowledge Base article <a href="https://kb.vmware.com/kb/2146810">2146810</a> documents the procedure for enabling and disabling this feature.
          </p>
          
          <p>
            VMware would like to thank E0DB6391795D7F629B5077842E649393 working with Trend Micro&#8217;s Zero Day Initiative for reporting this issue to us. The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-7081 to this issue.
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
            <a href="http://vmwaretips.com/wp/2016/09/13/security-announce-new-vmsa-2016-0014-vmware-esxi-workstation-fusion-and-tools-updates-address-multiple-security-issues/vmsa-2016-0014-2/"><img class="alignnone wp-image-3217" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-2.jpg" alt="vmsa-2016-0014-2" width="450" height="390" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-2.jpg 747w, http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-2-300x260.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </p>
          
          <p>
            <b>b. VMware Workstation memory corruption vulnerabilities via Cortado Thinprint</b>
          </p>
          
          <p>
            VMware Workstation contains vulnerabilities that may allow a Windows-based virtual machine (VM) to corrupt memory. This includes improper handling of EMF files (CVE-2016-7082), TrueType fonts embedded in EMFSPOOL (CVE-2016-7083), and JPEG2000 images (CVE-2016-7084) in tpview.dll. Exploitation of these issues may lead to arbitrary code execution in VMware   Workstation running on Windows.
          </p>
          
          <p>
            Exploitation is only possible if virtual printing has been enabled in VMware Workstation. This feature is not enabled by default. VMware Knowledge Base article <a href="https://kb.vmware.com/kb/2146810">2146810</a> documents the procedure for enabling and disabling this feature.
          </p>
          
          <p>
            VMware would like to thank Mateusz Jurczyk of Google&#8217;s Project Zero for reporting these   issues to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the   identifiers CVE-2016-7082, CVE-2016-7083, and CVE-2016-7084 to these issues.
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
  <div id="columncontainer1columncontainercomparisontable_9336_1057276705" class="rTable">
    <div class="rTableHeading">
    </div>
    
    <p>
      <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-3.jpg"><img class="alignnone wp-image-3218" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-3.jpg" alt="vmsa-2016-0014-3" width="450" height="389" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-3.jpg 742w, http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-3-300x259.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
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
            <b>c. VMware Tools NULL pointer dereference vulnerabilities</b>
          </p>
          
          <p>
            The graphic acceleration functions used in VMware Tools for OSX handle memory incorrectly. Two resulting NULL pointer dereference vulnerabilities may allow for local privilege escalation on Virtual Machines that run OSX.
          </p>
          
          <p>
            The issues can be remediated by installing a fixed version of VMware Tools on affected OSX   VMs directly. Alternatively the fixed version of Tools can be installed through ESXi or Fusion after first updating to a version of ESXi or Fusion that ships with a fixed version of VMware Tools.
          </p>
          
          <p>
            VMware would like to thank Dr. Fabien Duchene &#8220;FuzzDragon&#8221; and Jian Zhu for independently   reporting these issues to VMware.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the   identifiers CVE-2016-7079 and CVE-2016-7080 to these issues.
          </p>
          
          <p>
            Column 5 of the following table lists the action required to remediate the vulnerability in   each release, if a solution is available.
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
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-4.jpg"><img class="alignnone wp-image-3219" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-4.jpg" alt="vmsa-2016-0014-4" width="450" height="256" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-4.jpg 744w, http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-4-300x171.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </p>
          
          <p>
            *VMware Tools 10.0.9 can be downloaded independently and is also included in the following:
          </p>
          
          <ul>
            <li>
              ESXi 6.0 patch ESXi600-201608403-BG
            </li>
            <li>
              ESXi 5.5 patch ESXi550-201608102-SG
            </li>
            <li>
              Fusion 8.5.0
            </li>
          </ul>
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
            <b>d. VMware Workstation installer DLL hijacking issue</b>
          </p>
          
          <p>
            Workstation installer contains a DLL hijacking issue that exists due to some DLL files loaded by the application improperly. This issue may allow an attacker to load a DLL file of the attacker&#8217;s choosing that could execute arbitrary code.
          </p>
          
          <p>
            VMware would like to thank Stefan Kanthak, Anand Bhat, and Himanshu Mehta for independantly reporting this issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-7085 to this issue.
          </p>
          
          <p>
            Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
          </p>
          
          <p>
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-5.jpg"><img class="alignnone wp-image-3220" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-5.jpg" alt="vmsa-2016-0014-5" width="450" height="388" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-5.jpg 743w, http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-5-300x259.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
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
            <b>e. VMware Workstation installer insecure executable loading vulnerability</b>
          </p>
          
          <p>
            Workstation installer contains an insecure executable loading vulnerability that may allow an attacker to execute an exe file placed in the same directory as installer with the name &#8220;setup64.exe&#8221;. Successfully exploiting this issue may allow attackers to execute arbitrary code.
          </p>
          
          <p>
            VMware would like to thank Adam Bridge for reporting this issue to us.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-7086 to this issue.
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
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-6.jpg"><img class="alignnone wp-image-3221" src="http://vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-6.jpg" alt="vmsa-2016-0014-6" width="450" height="395" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-6.jpg 739w, http://www.vmwaretips.com/wp/wp-content/uploads/2016/09/vmsa-2016-0014-6-300x263.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </p>
          
          <p>
            <b>4. Solution</b>
          </p>
          
          <p>
            Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
          </p>
          
          <p>
            <b>VMware ESXi 6.0</b>
          </p>
          
          <p>
            Downloads: <a href="https://www.vmware.com/patchmgr/findPatch.portal">https://www.vmware.com/patchmgr/findPatch.portal</a>
          </p>
          
          <p>
            Documentation: <a href="https://kb.vmware.com/kb/2145816">https://kb.vmware.com/kb/2145816</a>
          </p>
          
          <p>
            <b>VMware ESXi 5.5</b>
          </p>
          
          <p>
            Downloads: <a href="https://www.vmware.com/patchmgr/findPatch.portal">https://www.vmware.com/patchmgr/findPatch.portal</a>
          </p>
          
          <p>
            Documentation: <a href="https://kb.vmware.com/kb/2144370">https://kb.vmware.com/kb/2144370</a>
          </p>
          
          <p>
            <b>VMware Workstation Pro 12.5.0</b>
          </p>
          
          <p>
            Downloads and Documentation: <a href="https://www.vmware.com/go/downloadworkstation">https://www.vmware.com/go/downloadworkstation</a>
          </p>
          
          <p>
            <b>VMware Workstation Player 12.5.0</b>
          </p>
          
          <p>
            Downloads and Documentation: <a href="https://www.vmware.com/go/downloadplayer">https://www.vmware.com/go/downloadplayer</a>
          </p>
          
          <p>
            <b>VMware Fusion 8.5.0</b>
          </p>
          
          <p>
            Downloads and Documentation: <a href="https://www.vmware.com/go/downloadfusion">https://www.vmware.com/go/downloadfusion</a>
          </p>
          
          <p>
            <b>VMware Tools 10.0.9</b>
          </p>
          
          <p>
            Downloads and Documentation: <a href="https://my.vmware.com/web/vmware/details?productId=491&downloadGroup=VMTOOLS1009">https://my.vmware.com/web/vmware/details?productId=491&downloadGroup=VMTOOLS1009</a>
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
            <b>5. References</b>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7081">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7081</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7082">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7082</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7083">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7083</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7084">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7084</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7079">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7079</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7080">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7080</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7085">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7085</a>
          </p>
          
          <p>
            <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7086" name="&lpos=content_security : 248">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-7086</a>
          </p>
          
          <p>
            <a href="https://kb.vmware.com/kb/2146810" name="&lpos=content_security : 249">https://kb.vmware.com/kb/2146810</a>
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
            <b>6. Change log</b>
          </p>
          
          <p>
            2016-09-13 VMSA-2016-0014 Initial security advisory in conjunction with the release of VMware Workstation 12.5.0 on 2016-09-13.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>