---
id: 3146
title: 'NEW VMSA-2016-0012 &#8211; VMware Photon OS OVA default public ssh key'
date: 2016-08-15T23:22:41+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3146
permalink: /2016/08/15/security-announce-new-vmsa-2016-0012-vmware-photon-os-ova-default-public-ssh-key/
redirect_from: /wp/2016/08/15/security-announce-new-vmsa-2016-0012-vmware-photon-os-ova-default-public-ssh-key/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1580"
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
          VMSA-2016-0012
        </h2>
        
        <h3>
          VMware Photon OS OVA default public ssh key
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
          VMware Security Advisory<span style="font-size: 0.83em; font-weight: normal;"> </span>
        </h5>
      </div>
    </div>
    
    <div>
      <div>
        <div>
          Advisory ID: VMSA-2016-0012
        </div>
      </div>
      
      <div>
        <div>
          Severity: Important
        </div>
      </div>
      
      <div>
        <div>
          Synopsis: VMware Photon OS OVA default public ssh key
        </div>
      </div>
      
      <div>
        <div>
          Issue date: 2016-08-15
        </div>
      </div>
      
      <div>
        <div>
          Updated on: 2016-08-15 (Initial Advisory)
        </div>
      </div>
      
      <div>
        <div>
          CVE numbers: CVE-2016-5333<span style="font-size: 0.83em;"> </span>
        </div>
      </div>
    </div>
  </div>
</div>

<div>
  <h5>
    1. Summary
  </h5>
  
  <p>
    VMware Photon OS OVA contains a default public ssh key.<!--more-->
  </p>
</div>

<div>
  <div>
    <div>
      <div>
        <div>
          <h5>
            2. Relevant Products
          </h5>
          
          <ul>
            <li>
              VMware Photon OS OVA 1.0
            </li>
          </ul>
          
          <h5>
            3. Problem Description
          </h5>
          
          <p>
            a. VMware Photon OS OVA default public ssh key
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            A public ssh key used in the Photon OS build environment was inadvertently left in the original Photon OS 1.0 OVAs. This issue would have allowed anyone with the corresponding private key to access any Photon OS system built from the original 1.0 OVAs.
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            The issue was discovered internally and the original OVAs have been replaced by updated OVAs. All instances of the corresponding private key have been deleted within VMware.
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            Customers that have downloaded a Photon OS 1.0 OVA before August 14, 2016 should review the Photon OS OVAs release notes for the workaround or should download a new OVA and replace all existing instances with new instances built from the updated Photon OS 1.0 OVAs. These release notes also document a test for when an OVA is affected.
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            This issue is only present in the original Photon OS 1.0 OVAs and is not present in other Photon OS deliverables.
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-5333 to this issue.
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            Column 5 of the following table lists the action required to remediate the vulnerability in each release, if a solution is   available.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

<div>
  <div id="columncontainer1columncontainercomparisontable_933633835">
    <div>
      <div data-heading="headingOne">
        <h5>
          VMware Product
        </h5>
        
        <div>
          Photon OS OVA
        </div>
      </div>
      
      <div data-heading="headingTwo">
        <h5>
          Product Version
        </h5>
        
        <div>
          1.0
        </div>
      </div>
      
      <div data-heading="headingThree">
        <h5>
          Running on
        </h5>
        
        <div>
          Linux
        </div>
      </div>
      
      <div data-heading="headingFour">
        <h5>
          Severity
        </h5>
        
        <div>
          Important
        </div>
      </div>
      
      <div data-heading="headingFive">
        <h5>
          Replace with/ Apply Patch*
        </h5>
        
        <div>
          Updated Photon OS OVAs 1.0
        </div>
      </div>
      
      <div data-heading="headingFive">
        <h5>
          Workaround
        </h5>
        
        <div>
          <div id="columncontainer1columncontainercomparisontable_933633835">
            See Photon OS Release Notes
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<div>
  <div>
    <div>
      <div>
        <div>
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>4. Solution</strong>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.<br /> VMware Photon OS 1.0 OVA
          </p>
          
          <p>
            OVA Download
          </p>
          
          <p>
            <a name="&lpos=content_security : 229" href="https://github.com/vmware/photon/wiki/Downloading-Photon-OS"></a>https://github.com/vmware/photon/wiki/Downloading-Photon-OS
          </p>
          
          <p>
            Release Notes
          </p>
          
          <p>
            <a name="&lpos=content_security : 230" href="https://github.com/vmware/photon/blob/master/CHANGELOG.md"></a>https://github.com/vmware/photon/blob/master/CHANGELOG.md
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>5. References</strong>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <a name="&lpos=content_security : 231" href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5333"></a>CVE-2016-5332
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <a name="&lpos=content_security : 232" href="https://github.com/vmware/photon/blob/master/CHANGELOG.md"></a>Photon OS OVA Release Notes
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            <strong>6. Change log</strong>
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <p>
            2016-08-15 VMSA-2016-0012
          </p>
          
          <p>
            Initial security advisory in conjunction with the release of updated Photon OS 1.0 OVAs
          </p>
          
          <p>
            on 2016-08-15.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>