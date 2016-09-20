---
id: 3159
title: 'NEW VMSA-2016-0013 &#8211; VMware Identity Manager and vRealize Automation updates address multiple security issues'
date: 2016-08-23T19:28:26+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=3159
permalink: /2016/08/23/security-announce-new-vmsa-2016-0013-vmware-identity-manager-and-vrealize-automation-updates-address-multiple-security-issues/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 1259
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
  <div>
    <div>
      <div>
        <h2>
          VMSA-2016-0013
        </h2>
        
        <h3>
          VMware Identity Manager and vRealize Automation updates address multiple security issues
        </h3>
      </div>
    </div>
  </div>
</div>

<div>
  <div id="columncontainer1columncontainercomparisontable">
    <div>
      <div data-heading="headingOne">
        <h5>
          VMware Security Advisory
        </h5>
      </div>
      
      <div data-heading="headingTwo">
        <h5>
          <span style="font-size: 13px; font-weight: normal;">Advisory ID: </span><span style="font-size: 13px; font-weight: normal;">VMSA-2016-0013<br /> </span><span style="font-size: 13px; font-weight: normal;">Severity: </span><span style="font-size: 13px; font-weight: normal;">Important<br /> </span><span style="font-size: 13px; font-weight: normal;">Synopsis: </span><span style="font-size: 13px; font-weight: normal;">VMware Identity Manager and vRealize Automation updates address multiple security issues<br /> </span><span style="font-size: 13px; font-weight: normal;">Issue date: </span><span style="font-size: 13px; font-weight: normal;">2016-08-23<br /> </span><span style="font-size: 13px; font-weight: normal;">Updated on: </span><span style="font-size: 13px; font-weight: normal;">2016-08-23 (Initial Advisory)<br /> </span><span style="font-size: 13px; font-weight: normal;">CVE numbers: </span><span style="font-size: 13px; font-weight: normal;">CVE-2016-5335, CVE-2016-5336</span>
        </h5>
      </div>
    </div>
  </div>
</div>

<div>
  <div>
    <div>
      <div>
        <div>
          <h5>
            1. Summary
          </h5>
          
          <p>
            VMware Identity Manager and vRealize Automation updates address multiple security issues
          </p>
          
          <p>
            <!--more-->
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

<div>
  <h5>
    2. Relevant Products
  </h5>
  
  <ul>
    <li>
      VMware Identity Manager
    </li>
    <li>
      vRealize Automation
    </li>
  </ul>
  
  <h5>
    3. Problem Description
  </h5>
  
  <p>
    <strong>a. VMware Identity Manager local privilege escalation vulnerability  </strong>
  </p>
  
  <p>
    VMware Identity Manager and vRealize Automation both contain a vulnerability that may allow for a local privilege escalation. Exploitation of this issue may lead to an attacker with access to a low-privileged account to escalate their privileges to that of root.
  </p>
  
  <p>
    The Common Vulnerabilities and Exposures project (cve.mitre.org) has reserved the identifier CVE-2016-5335 for this issue.
  </p>
  
  <p>
    Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
  </p>
  
  <p>
    <a href="http://vmwaretips.com/wp/2016/08/23/security-announce-new-vmsa-2016-0013-vmware-identity-manager-and-vrealize-automation-updates-address-multiple-security-issues/vmsa-2016-0013a/" rel="attachment wp-att-3170"><img class="alignnone  wp-image-3170" title="vmsa-2016-0013a" src="http://vmwaretips.com/wp/wp-content/uploads/2016/08/vmsa-2016-0013a.png" alt="" width="440" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2016/08/vmsa-2016-0013a.png 769w, http://www.vmwaretips.com/wp/wp-content/uploads/2016/08/vmsa-2016-0013a-300x192.png 300w" sizes="(max-width: 769px) 100vw, 769px" /></a>
  </p>
</div>

<div>
  <div id="columncontainer1columncontainercomparisontable_933633835">
    <div data-heading="headingOne">
      <h5>
        <strong style="font-size: 13px;">b. vRealize Automation remote code execution vulnerability</strong>
      </h5>
    </div>
  </div>
</div>

<div>
  <p>
    vRealize Automation contains a vulnerability that may allow for remote code execution. Exploitation of this issue may lead to an attacker gaining access to a low-privileged account on the appliance.
  </p>
  
  <p>
    The Common Vulnerabilities and Exposures project (cve.mitre.org) has reserved the identifier CVE-2016-5336 for this issue.
  </p>
  
  <p>
    Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
  </p>
</div>

<div>
  <div id="columncontainer1columncontainercomparisontable_9323">
    <div data-heading="headingOne">
      <h5>
        <span style="font-size: 13px; font-weight: normal;"><a href="http://vmwaretips.com/wp/2016/08/23/security-announce-new-vmsa-2016-0013-vmware-identity-manager-and-vrealize-automation-updates-address-multiple-security-issues/vmsa-2016-0013b/" rel="attachment wp-att-3171"><img class="alignnone  wp-image-3171" title="vmsa-2016-0013b" src="http://vmwaretips.com/wp/wp-content/uploads/2016/08/vmsa-2016-0013b.png" alt="" width="440" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2016/08/vmsa-2016-0013b.png 762w, http://www.vmwaretips.com/wp/wp-content/uploads/2016/08/vmsa-2016-0013b-300x148.png 300w" sizes="(max-width: 762px) 100vw, 762px" /></a> </span>
      </h5>
    </div>
  </div>
</div>

<div>
  <p>
    <strong>4. Solution</strong>
  </p>
  
  <p>
    Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
  </p>
  
  <p>
    VMware Identity Manager 2.7
  </p>
  
  <p>
    &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
  </p>
  
  <p>
    <a name="&lpos=content_security : 229" href="https://my.vmware.com/en/web/vmware/info/slug/desktop_end_user_computing/vmware_identity_manager/2_7"></a>Downloads and Documentation
  </p>
  
  <p>
    &nbsp;
  </p>
  
  <p>
    vRealize Automation 7.1
  </p>
  
  <p>
    &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
  </p>
  
  <p>
    <a name="&lpos=content_security : 230" href="https://my.vmware.com/group/vmware/info/slug/infrastructure_operations_management/vmware_vrealize_automation/7_1#product_downloads"></a>Downloads and Documentation
  </p>
  
  <p>
    &nbsp;
  </p>
  
  <p>
    <strong>5. References</strong>
  </p>
  
  <p>
    <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5335">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5335</a>
  </p>
  
  <p>
    <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5336">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5336</a>
  </p>
  
  <p>
    <a href="https://kb.vmware.com/kb/2146585">https://kb.vmware.com/kb/2146585</a>
  </p>
  
  <p>
    &nbsp;
  </p>
  
  <p>
    <strong>6. Change log</strong>
  </p>
  
  <p>
    2016-08-23 VMSA-2016-0013 Initial security advisory in conjunction with the release of vRealize Automation 7.1 on 2016-08-23.
  </p>
</div>