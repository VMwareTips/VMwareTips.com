---
id: 3294
title: VMSA-2016-0005.5 VMware product updates address critical and important security issues
date: 2016-11-22T12:57:20+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3294
permalink: /2016/11/22/security-announce-updated-vmsa-2016-0005-5-vmware-product-updates-address-critical-and-important-security-issues/
redirect_from: /wp/2016/11/22/security-announce-updated-vmsa-2016-0005-5-vmware-product-updates-address-critical-and-important-security-issues/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1619"
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
          <h5>
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-a.jpg"><img class="alignnone wp-image-3311" src="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-a.jpg" alt="vmsa-2016-0005.5-a" width="450" height="243" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-a.jpg 557w, http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-a-300x162.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </h5>
          
          <p>
            
          </p>
          
          <h5>
            1. Summary
          </h5>
          
          <p>
            VMware product updates address critical and important security issues
          </p>
          
          <p>
            &nbsp;
          </p>
          
          <div class="paragraphText parbase section">
            <div class="section-custom ">
              <div class="container-fluid">
                <div class="row">
                  <div class="col-md-12">
                    <p>
                      <b>2. Relevant Releases</b>
                    </p>
                    
                    <p>
                      vCenter Server 6.0 on Windows without workaround of KB 2145343
                    </p>
                    
                    <p>
                      vCenter Server 6.0 on Linux (VCSA) prior to 6.0.0b
                    </p>
                    
                    <p>
                      vCenter Server 5.5 prior to 5.5 U3d (on Windows), 5.5 U3 (VCSA)
                    </p>
                    
                    <p>
                      vCenter Server 5.1 prior to 5.1 U3b
                    </p>
                    
                    <p>
                      vCenter Server 5.0 prior to 5.0 U3e
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      vCloud Director prior to 8.0.1.1
                    </p>
                    
                    <p>
                      vCloud Director prior to 5.6.5.1
                    </p>
                    
                    <p>
                      vCloud Director prior to 5.5.6.1
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      vSphere Replication prior to 6.1.1
                    </p>
                    
                    <p>
                      vSphere Replication prior to 6.0.0.3
                    </p>
                    
                    <p>
                      vSphere Replication prior to 5.8.1.2
                    </p>
                    
                    <p>
                      vSphere Replication prior to 5.6.0.6
                    </p>
                    
                    <p>
                      vRealize Operations Manager 6.x (non-appliance version)
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      vRealize Infrastructure Navigator prior to 5.8.6
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      VMware Workstation prior to 11.1.3
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      VMware Player prior to 7.1.3
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <b>3. Problem Description</b>
                    </p>
                    
                    <p>
                      <b>a. Critical JMX issue when deserializing authentication credentials</b>
                    </p>
                    
                    <p>
                      The RMI server of Oracle JRE JMX deserializes any class when deserializing authentication credentials. This may allow a remote, unauthenticated attacker to cause deserialization flaws and execute their commands.
                    </p>
                    
                    <p>
                      <b>Workarounds CVE-2016-3427</b>
                    </p>
                    
                    <p>
                      <strong>vCenter Server</strong>
                    </p>
                    
                    <p>
                      Apply the steps of VMware Knowledge Base article 2145343 to vCenterServer 6.0 on Windows. See the table below for the specific vCenterServer 6.0 versions on Windows this applies to.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>vCloud Director</strong>
                    </p>
                    
                    <p>
                      No workaround identified
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>vSphere Replication</strong>
                    </p>
                    
                    <p>
                      No workaround identified
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>vRealize Operations Manager (non-appliance)</strong>
                    </p>
                    
                    <p>
                      The non-appliance version of vRealize Operations Manager (vROps), which can be installed on Windows and Linux has no default firewall. In order to remove the remote exploitation possibility, access to the following external ports will need to be blocked on the system where the non-appliance version of vROps is installed:
                    </p>
                    
                    <p>
                      &#8211; vROps 6.2.x: port 9004, 9005, 9006, 9007, 9008
                    </p>
                    
                    <p>
                      &#8211; vROps 6.1.x: port 9004, 9005, 9007, 9008
                    </p>
                    
                    <p>
                      &#8211; vROps 6.0.x: port 9004, 9005
                    </p>
                    
                    <p>
                      Note: These ports are already blocked by default in the applianceversion of vROps.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>vRealize Infrastructure Navigator</strong>
                    </p>
                    
                    <p>
                      No workaround identified
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-3427 to this issue.
                    </p>
                    
                    <p>
                      Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          
          <div class="comparisonTable section">
            <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-b.jpg"><img class="alignnone wp-image-3312" src="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-b.jpg" alt="vmsa-2016-0005.5-b" width="450" height="957" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-b.jpg 498w, http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-b-141x300.jpg 141w, http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-b-482x1024.jpg 482w" sizes="(max-width: 450px) 100vw, 450px" /></a>
          </div>
          
          <div class="comparisonTable section">
            * Remote and local exploitation is feasible on vCenter Server 6.0 and 6.0.0a for Windows. Remote exploitation is not feasible on vCenter Server 6.0.0b (and above) for Windows but local exploitation is. The local exploitation possibility can be removed by applying the steps of KB 2145343 to vCenter Server 6.0.0b (and above) for Windows or by updating to vCenter Server 6.0 U2a for Windows.
          </div>
          
          <div class="paragraphText parbase section">
            <div class="section-custom ">
              <div class="container-fluid">
                <div class="row">
                  <div class="col-md-12">
                    <p>
                      ** See VMSA-2015-0007 for details. vCenter Server 5.5 U3d, 5.1 U3d, and 5.0 U3g running on Windows address CVE-2016-3427 without the need to install the additional patch of KB 2144428 documented in VMSA-2015-0007.
                    </p>
                    
                    <p>
                      *** vSphere Replication is affected if its vCloud Tunneling Agent is running, which is not enabled by default. This agent is used in environments that replicate data between the cloud and an on-premise datacenter.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      b. Important VMware Workstation and Player for Windows host privilege escalation vulnerability.
                    </p>
                    
                    <p>
                      VMware Workstation and Player for Windows do not properly reference one of their executables. This may allow a local attacker on the host to elevate their privileges.
                    </p>
                    
                    <p>
                      VMware would like to thank Andrew Smith of Sword & Shield Enterprise Security for reporting this issue to us.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-2077 to this issue.
                    </p>
                    
                    <p>
                      Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
                    </p>
                    
                    <p>
                      <a href="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-c.jpg"><img class="alignnone wp-image-3313" src="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-c.jpg" alt="vmsa-2016-0005.5-c" width="450" height="338" srcset="http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-c.jpg 560w, http://vmwaretips.com/wp/wp-content/uploads/2016/11/vmsa-2016-0005.5-c-300x225.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
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
                      <b>4. Solution</b>
                    </p>
                    
                    <p>
                      Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>vCenter Server</strong>
                    </p>
                    
                    <p>
                      &#8212;&#8212;&#8212;&#8212;&#8211;
                    </p>
                    
                    <p>
                      Downloads and Documentation:
                    </p>
                    
                    <p>
                      https://www.vmware.com/go/download-vsphere
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>vCloud Director</strong>
                    </p>
                    
                    <p>
                      &#8212;&#8212;&#8212;&#8212;&#8212;
                    </p>
                    
                    <p>
                      Downloads and Documentation:
                    </p>
                    
                    <p>
                      https://www.vmware.com/go/download/vcloud-director
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>vSphere Replication</strong>
                    </p>
                    
                    <p>
                      &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
                    </p>
                    
                    <p>
                      Downloads and Documentation:
                    </p>
                    
                    <p>
                      https://my.vmware.com/web/vmware/get-download?downloadGroup=VR611
                    </p>
                    
                    <p>
                      https://my.vmware.com/web/vmware/get-download?downloadGroup=VR6003
                    </p>
                    
                    <p>
                      https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5812
                    </p>
                    
                    <p>
                      https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5606
                    </p>
                    
                    <p>
                      https://www.vmware.com/support/pubs/vsphere-replication-pubs.htm
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>vRealize Infrastructure Navigator</strong>
                    </p>
                    
                    <p>
                      &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
                    </p>
                    
                    <p>
                      Downloads and Documentation:https://my.vmware.com/web/vmware/details?downloadGroup=VIN_586&productId=542&rPId=11127
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>VMware Workstation</strong>
                    </p>
                    
                    <p>
                      &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
                    </p>
                    
                    <p>
                      Downloads and Documentation:
                    </p>
                    
                    <p>
                      https://www.vmware.com/go/downloadworkstation
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>VMware Player</strong>
                    </p>
                    
                    <p>
                      &#8212;&#8212;&#8212;&#8212;-
                    </p>
                    
                    <p>
                      Downloads and Documentation:https://www.vmware.com/go/downloadplayer
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <b>5. References</b>
                    </p>
                    
                    <p>
                      http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-3427
                    </p>
                    
                    <p>
                      http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2077
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>VMware Security Advisory VMSA-2015-0007</strong>
                    </p>
                    
                    <p>
                      http://www.vmware.com/security/advisories/VMSA-2015-0007.html
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>VMware Knowledge Base article 2145343</strong>
                    </p>
                    
                    <p>
                      kb.vmware.com/kb/2145343
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <strong>VMware Knowledge Base article 2144428</strong>
                    </p>
                    
                    <p>
                      kb.vmware.com/kb/2144428
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      <b>6. Change log </b>
                    </p>
                    
                    <p>
                      2016-05-17 VMSA-2016-0005
                    </p>
                    
                    <p>
                      Initial security advisory in conjunction with the release of VMware vCloud Director 8.0.1.1, 5.6.5.1, and 5.5.6.1, and vSphere Replication 6.0.0.3, 5.8.1.2, and 5.6.0.6 on 2016-05-17.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      2016-05-24 VMSA-2016-0005.1
                    </p>
                    
                    <p>
                      Updated security advisory in conjunction with the release of vSphere 5.1 U3d on 2016-05-24. vCenter Server 5.1 U3d running on Windows addresses CVE-2016-3427 without the need to install the additional patch.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      2016-05-27 VMSA-2016-0005.2
                    </p>
                    
                    <p>
                      Updated security advisory in conjunction with the release of vSphere Replication 6.1.1 on2016-05-26.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      2016-06-03 VMSA-2016-0005.3
                    </p>
                    
                    <p>
                      Updated security advisory in conjunction with the release of vRealize Infrastructure Navigator 5.8.6 on 2016-06-02.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      2016-06-14 VMSA-2016-0005.4
                    </p>
                    
                    <p>
                      Updated security advisory in conjunction with the release of vSphere 5.0 U3g on 2016-06-14. vCenter Server 5.0 U3g running on Windows addresses CVE-2016-3427 without the need to install the additional patch.
                    </p>
                    
                    <p>
                      &nbsp;
                    </p>
                    
                    <p>
                      2016-11-22 VMSA-2016-0005.5
                    </p>
                    
                    <p>
                      Updated security advisory in conjunction with the release of vSphere 6.0 U2a on 2016-11-22. vCenter Server 6.0 U2a running on Windows addresses CVE-2016-3427 without the need to install the additional patch.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>