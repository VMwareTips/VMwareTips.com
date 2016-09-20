---
id: 3034
title: 'UPDATE: VMSA-2016-0005.3 &#8211; VMware product updates address critical and important security issues'
date: 2016-06-03T15:22:46+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=3034
permalink: /2016/06/03/security-announce-update-vmsa-2016-0005-3-vmware-product-updates-address-critical-and-important-security-issues/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 8469
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
    <table>
      <tr>
        <th colspan="2">
          VMware Security Advisory
        </th>
      </tr>
      
      <tr>
        <td>
          Advisory ID:
        </td>
        
        <td>
          VMSA-2016-0005.3
        </td>
      </tr>
      
      <tr>
        <td>
          Synopsis:
        </td>
        
        <td>
          VMware product updates address critical and important security issues
        </td>
      </tr>
      
      <tr>
        <td>
          Issue date:
        </td>
        
        <td>
          2016-05-17
        </td>
      </tr>
      
      <tr>
        <td>
          Updated on:
        </td>
        
        <td>
          2016-06-03
        </td>
      </tr>
      
      <tr>
        <td>
          CVE numbers:
        </td>
        
        <td>
          CVE-2016-3427, CVE-2016-2077
        </td>
      </tr>
    </table>
  </div>
  
  <div>
  </div>
</div>

<div>
  <div id="m_segment_1463436007665">
    <div>
      <div>
        <div>
          <div>
            <div>
              <div>
                <strong>1. Summary</strong>
              </div>
              
              <div>
                VMware product updates address critical and important security issues.
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
                <!--more-->
              </div>
              
              <div>
                <strong>2. Relevant Releases</strong>
              </div>
              
              <div>
                <p>
                     vCenter Server 6.0 on Windows without workaround of KB 2145343<br /> vCenter Server 6.0 on Linux (VCSA) prior to 6.0.0b<br /> vCenter Server 5.5 prior to 5.5 U3d (on Windows), 5.5 U3 (VCSA)<br /> vCenter Server 5.1 prior to 5.1 U3b<br /> vCenter Server 5.0 prior to 5.0 U3e
                </p>
                
                <p>
                  vCloud Director prior to 8.0.1.1<br /> vCloud Director prior to 5.6.5.1<br /> vCloud Director prior to 5.5.6.1
                </p>
                
                <p>
                  vSphere Replication prior to 6.1.1<br /> vSphere Replication prior to 6.0.0.3<br /> vSphere Replication prior to 5.8.1.2<br /> vSphere Replication prior to 5.6.0.6
                </p>
                
                <p>
                  vRealize Operations Manager 6.x (non-appliance version)
                </p>
                
                <p>
                  vRealize Infrastructure Navigator prior to 5.8.6
                </p>
                
                <p>
                  VMware Workstation prior to 11.1.3
                </p>
                
                <p>
                  VMware Player prior to 7.1.3
                </p>
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
                <strong>3. Problem Description</strong>
              </div>
              
              <div>
                <p>
                  a. Critical JMX issue when deserializing authentication credentials
                </p>
                
                <p>
                  The RMI server of Oracle JRE JMX deserializes any class when<br /> deserializing authentication credentials. This may allow a remote,<br /> unauthenticated attacker to cause deserialization flaws and execute<br /> their commands.
                </p>
                
                <p>
                  Workarounds CVE-2016-3427
                </p>
                
                <p>
                  vCenter Server<br /> Apply the steps of VMware Knowledge Base article 2145343 to vCenter<br /> Server 6.0 on Windows. See the table below for the specific vCenter<br /> Server 6.0 versions on Windows this applies to.
                </p>
                
                <p>
                  vCloud Director<br /> No workaround identified
                </p>
                
                <p>
                  vSphere Replication<br /> No workaround identified
                </p>
                
                <p>
                  vRealize Operations Manager (non-appliance)<br /> The non-appliance version of vRealize Operations Manager (vROps),<br /> which can be installed on Windows and Linux has no default<br /> firewall. In order to remove the remote exploitation possibility,<br /> access to the following external ports will need to be blocked on<br /> the system where the non-appliance version of vROps is installed:<br /> &#8211; vROps 6.2.x: port 9004, 9005, 9006, 9007, 9008<br /> &#8211; vROps 6.1.x: port 9004, 9005, 9007, 9008<br /> &#8211; vROps 6.0.x: port 9004, 9005<br /> Note: These ports are already blocked by default in the appliance<br /> version of vROps.
                </p>
                
                <p>
                  vRealize Infrastructure Navigator<br /> No workaround identified
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has<br /> assigned the identifier CVE-2016-3427 to this issue.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to remediate<br /> the vulnerability in each release, if a solution is available.
                </p>
                
                <div>
                  <div>
                    <table border="0">
                      <tr>
                        <td>
                          VMware
                        </td>
                        
                        <td>
                          Product
                        </td>
                        
                        <td>
                          Running
                        </td>
                        
                        <td>
                          Replace with/
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          Product
                        </td>
                        
                        <td>
                          Version
                        </td>
                        
                        <td>
                          on
                        </td>
                        
                        <td>
                          Apply Patch
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          6.0
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          6.0.0b + KB 2145343 *
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          6.0
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          6.0.0b
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          5.5
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          (5.5 U3b + KB 2144428 **) or 5.5 U3d
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          5.5
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.5 U3
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          5.1
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          (5.1 U3b + KB 2144428 **) or 5.1 U3d
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          5.1
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.1 U3b
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          5.0
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          5.0 U3e + KB 2144428 **
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          5.0
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.0 U3e
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCloud Director
                        </td>
                        
                        <td>
                          8.0.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          8.0.1.1
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCloud Director
                        </td>
                        
                        <td>
                          5.6.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.6.5.1
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCloud Director
                        </td>
                        
                        <td>
                          5.5.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.5.6.1
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vSphere Replication
                        </td>
                        
                        <td>
                          6.1.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          6.1.1 ***
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vSphere Replication
                        </td>
                        
                        <td>
                          6.0.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          6.0.0.3 ***
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vSphere Replication
                        </td>
                        
                        <td>
                          5.8.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.8.1.2 ***
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vSphere Replication
                        </td>
                        
                        <td>
                          5.6.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.6.0.6 ***
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vROps non-appliance
                        </td>
                        
                        <td>
                          6.x
                        </td>
                        
                        <td>
                          All
                        </td>
                        
                        <td>
                          Apply workaround
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vROps appliance
                        </td>
                        
                        <td>
                          6.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          Not affected
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vRealize Infrastructure Navigator
                        </td>
                        
                        <td>
                          5.8.x
                        </td>
                        
                        <td>
                          All
                        </td>
                        
                        <td>
                          5.8.6
                        </td>
                      </tr>
                    </table>
                  </div>
                </div>
                
                <p>
                  * Remote and local exploitation is feasible on vCenter Server 6.0 and<br /> 6.0.0a for Windows. Remote exploitation is not feasible on vCenter<br /> Server 6.0.0b (and above) for Windows but local exploitation is. The<br /> local exploitation possibility can be removed by applying the steps<br /> of KB 2145343 to vCenter Server 6.0.0b (and above) for Windows.
                </p>
                
                <p>
                  ** See VMSA-2015-0007 for details.<br /> vCenter Server 5.5 U3d and 5.1 U3d running on Windows addresses<br /> CVE-2016-3427 without the need to install the additional patch<br /> of KB 2144428 documented in VMSA-2015-0007.<br /> *** vSphere Replication is affected if its vCloud Tunneling Agent<br /> is running, which is not enabled by default. This agent is used<br /> in environments that replicate data between the cloud and an<br /> on-premise datacenter.<br /> b. Important VMware Workstation and Player for Windows host privilege<br /> escalation vulnerability.
                </p>
                
                <p>
                  VMware Workstation and Player for Windows do not properly reference<br /> one of their executables. This may allow a local attacker on the host<br /> to elevate their privileges.
                </p>
                
                <p>
                  VMware would like to thank Andrew Smith of Sword & Shield Enterprise<br /> Security for reporting this issue to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org)<br /> has assigned the identifier CVE-2016-2077 to this issue.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to<br /> remediate the vulnerability in each release, if a solution is available.
                </p>
                
                <div>
                  <div>
                    <table border="0">
                      <tr>
                        <td>
                          VMware
                        </td>
                        
                        <td>
                          Product
                        </td>
                        
                        <td>
                          Running
                        </td>
                        
                        <td>
                          Replace with/
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          Product
                        </td>
                        
                        <td>
                          Version
                        </td>
                        
                        <td>
                          on
                        </td>
                        
                        <td>
                          Apply Patch
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware Workstation
                        </td>
                        
                        <td>
                          12.x.x
                        </td>
                        
                        <td>
                          Any
                        </td>
                        
                        <td>
                          not affected
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware Workstation
                        </td>
                        
                        <td>
                          11.x.x
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          11.1.3
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware Workstation
                        </td>
                        
                        <td>
                          11.x.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          not affected
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware Player
                        </td>
                        
                        <td>
                          12.x.x
                        </td>
                        
                        <td>
                          Any
                        </td>
                        
                        <td>
                          not affected
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware Player
                        </td>
                        
                        <td>
                          7.x.x
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          7.1.3
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware Player
                        </td>
                        
                        <td>
                          7.x.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          not affected
                        </td>
                      </tr>
                    </table>
                  </div>
                </div>
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
              </div>
              
              <div>
                <strong>4. Solution</strong>
              </div>
              
              <div>
                <p>
                     Please review the patch/release notes for your product and<br /> version and verify the checksum of your downloaded file.
                </p>
                
                <p>
                  vCenter Server<br /> &#8212;&#8212;&#8212;&#8212;&#8211;<br /> Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a>
                </p>
                
                <p>
                  vCloud Director<br /> &#8212;&#8212;&#8212;&#8212;&#8212;<br /> Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/download/vcloud-director">https://www.vmware.com/go/download/vcloud-director</a>
                </p>
                
                <p>
                  vSphere Replication<br /> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-<br /> Downloads and Documentation:<br /> <a href="https://my.vmware.com/web/vmware/get-download?downloadGroup=VR611">https://my.vmware.com/web/vmware/get-download?downloadGroup=VR611</a><br /> <a name="&lpos=content : 8" href="https://my.vmware.com/web/vmware/get-download?downloadGroup=VR6003"></a>https://my.vmware.com/web/vmware/get-download?downloadGroup=VR6003<br /> <a href="https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5812">https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5812</a><br /> <a href="https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5606">https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5606</a><br /> <a href="https://www.vmware.com/support/pubs/vsphere-replication-pubs.html">https://www.vmware.com/support/pubs/vsphere-replication-pubs.htm</a>
                </p>
                
                <p>
                  vRealize Infrastructure Navigator<br /> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<br /> Downloads and Documentation:<br /> <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VIN_586&productId=542&rPId=11127">https://my.vmware.com/web/vmware/details?downloadGroup=VIN_586&productId=542&rPId=11127</a>
                </p>
                
                <p>
                  VMware Workstation<br /> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-<br /> Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/downloadworkstation">https://www.vmware.com/go/downloadworkstation</a>
                </p>
                
                <p>
                  VMware Player<br /> &#8212;&#8212;&#8212;&#8212;-<br /> Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/downloadplayer">https://www.vmware.com/go/downloadplayer</a>
                </p>
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
                <strong>5. References</strong>
              </div>
              
              <div>
                <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-3427">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-3427</a><br /> <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2077">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2077</a>VMware Security Advisory VMSA-2015-0007<br /> <a href="http://www.vmware.com/security/advisories/VMSA-2015-0007.html">http://www.vmware.com/security/advisories/VMSA-2015-0007.html</a>VMware Knowledge Base article 2145343<br /> <a href="https://kb.vmware.com/kb/2145343">kb.vmware.com/kb/2145343</a></p> 
                
                <p>
                  VMware Knowledge Base article 2144428<br /> <a href="https://kb.vmware.com/kb/2144428">kb.vmware.com/kb/2144428</a>
                </p>
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
              </div>
              
              <div>
                <strong>6. Change log</strong>
              </div>
              
              <div>
                <p>
                     2016-05-17 VMSA-2016-0005<br /> Initial security advisory in conjunction with the release of VMware<br /> vCloud Director 8.0.1.1, 5.6.5.1, and 5.5.6.1, and vSphere<br /> Replication 6.0.0.3, 5.8.1.2, and 5.6.0.6 on 2016-05-17.
                </p>
                
                <p>
                  2016-05-24 VMSA-2016-0005.1<br /> Updated security advisory in conjunction with the release of vSphere<br /> 5.1 U3d on 2016-05-24. vCenter Server 5.1 U3d running on<br /> Windows addresses CVE-2016-3427 without the need to install the<br /> additional patch.
                </p>
                
                <p>
                  2016-05-27 VMSA-2016-0005.2<br /> Updated security advisory in conjunction with the release of vSphere<br /> Replication 6.1.1 on 2016-05-26.
                </p>
                
                <p>
                  2016-06-03 VMSA-2016-0005.3<br /> Updated security advisory in conjunction with the release of vRealize<br /> Infrastructure Navigator 5.8.6 on 2016-06-02.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>