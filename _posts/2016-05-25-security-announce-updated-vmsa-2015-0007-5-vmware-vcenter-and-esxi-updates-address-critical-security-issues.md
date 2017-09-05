---
id: 3026
title: 'UPDATED VMSA-2015-0007.5 &#8211; VMware vCenter and ESXi updates address critical security issues'
date: 2016-05-25T00:47:05+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3026
permalink: /2016/05/25/security-announce-updated-vmsa-2015-0007-5-vmware-vcenter-and-esxi-updates-address-critical-security-issues/
redirect_from: /wp/2016/05/25/security-announce-updated-vmsa-2015-0007-5-vmware-vcenter-and-esxi-updates-address-critical-security-issues/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "9150"
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
          VMSA-2015-0007.5
        </td>
      </tr>
      
      <tr>
        <td>
          Synopsis:
        </td>
        
        <td>
          VMware vCenter and ESXi updates address critical security issues.
        </td>
      </tr>
      
      <tr>
        <td>
          Issue date:
        </td>
        
        <td>
          2015-10-01
        </td>
      </tr>
      
      <tr>
        <td>
          Updated on:
        </td>
        
        <td>
          2016-05-24
        </td>
      </tr>
      
      <tr>
        <td>
          CVE numbers:
        </td>
        
        <td>
          CVE-2015-5177 CVE-2015-2342 CVE-2015-1047
        </td>
      </tr>
    </table>
  </div>
  
  <div>
  </div>
</div>

<div>
  <div id="m_segment_1443209629904">
    <div>
      <div>
        <div>
          <div>
            <div>
              <div>
                <strong>1. Summary</strong>
              </div>
              
              <div>
                <p>
                  VMware vCenter and ESXi updates address critical security issues.
                </p>
                
                <p>
                  NOTE: See section 3.b for a critical update on an incomplete fix for the JMX RMI issue.
                </p>
                
                <p>
                  <!--more-->
                </p>
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
                <strong>2. Relevant Releases</strong>
              </div>
              
              <div>
              </div>
              
              <div>
                VMware ESXi 5.5 without patch ESXi550-201509101-SG<br /> VMware ESXi 5.1 without patch ESXi510-201510101-SG<br /> VMware ESXi 5.0 without patch ESXi500-201510101-SGVMware vCenter Server 6.0 prior to version 6.0.0b<br /> VMware vCenter Server 5.5 prior to version 5.5 update 3<br /> VMware vCenter Server 5.1 prior to version 5.1 update u3b<br /> VMware vCenter Server 5.0 prior to version 5.0 update u3e
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
              </div>
              
              <div>
                <strong>3. Problem Description</strong>
              </div>
              
              <div>
              </div>
              
              <div>
                a. VMware ESXi OpenSLP Remote Code ExecutionVMware ESXi contains a double free flaw in OpenSLP&#8217;s SLPDProcessMessage() function. Exploitation of this issue may allow an unauthenticated attacker to remotely execute code on the ESXi host.VMware would like to thank Qinghao Tang of QIHU 360 for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2015-5177 to this issue.</p> 
                
                <p>
                  Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
                </p>
                
                <div>
                  <div>
                    <table border="0">
                      <tr>
                        <td>
                          VMware Product
                        </td>
                        
                        <td>
                          Product Version
                        </td>
                        
                        <td>
                          Running on
                        </td>
                        
                        <td>
                          Replace with/ Apply Patch
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          ESXi
                        </td>
                        
                        <td>
                          6.0
                        </td>
                        
                        <td>
                          ESXi
                        </td>
                        
                        <td>
                          not affected
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          ESXi
                        </td>
                        
                        <td>
                          5.5
                        </td>
                        
                        <td>
                          ESXi
                        </td>
                        
                        <td>
                          ESXi550-201509101-SG *
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          ESXi
                        </td>
                        
                        <td>
                          5.1
                        </td>
                        
                        <td>
                          ESXi
                        </td>
                        
                        <td>
                          ESXi510-201510101-SG
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          ESXi
                        </td>
                        
                        <td>
                          5.0
                        </td>
                        
                        <td>
                          ESXi
                        </td>
                        
                        <td>
                          ESXi500-201510101-SG
                        </td>
                      </tr>
                    </table>
                  </div>
                </div>
                
                <p>
                  * <em>Customers who have installed the complete set of ESXi 5.5 U3 Bulletins, please review VMware KB 2133118. KB 2133118 documents a known non-security issue and provides a solution.</em>b. VMware vCenter Server JMX RMI Remote Code Execution
                </p>
                
                <p>
                  VMware vCenter Server contains a remotely accessible JMX RMI service that is not securely configured. An unauthenticated remote attacker who is able to connect to the service may be able to use it to execute arbitrary code on the vCenter Server. A local attacker may be able to elevate their privileges on vCenter Server.
                </p>
                
                <p>
                  vCenter Server Appliance (vCSA) 5.1, 5.5 and 6.0 has remote access to the JMX RMI service (port 9875) blocked by default.
                </p>
                
                <p>
                  VMware would like to thank Doug McLeod of 7 Elements Ltd and an anonymous researcher working through HP&#8217;s Zero Day Initiative for reporting this issue to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2015-2342 to this issue.
                </p>
                
                <p>
                  CRITICAL UPDATE
                </p>
                
                <p>
                  VMSA-2015-0007.2 and earlier versions of this advisory documented that CVE-2015-2342 was addressed in vCenter Server 5.0 U3e, 5.1 U3b, and 5.5 U3. Subsequently, it was found that the fix for CVE-2015-2342 in vCenter Server 5.0 U3e, 5.1 U3b, and 5.5 U3/U3a/U3b running on Windows was incomplete and did not address the issue.
                </p>
                
                <p>
                  In order to address the issue on these versions of vCenter Server Windows, an additional patch must be installed. This additional patch is available from VMware Knowledge Base (KB) article 2144428. Alternatively, on vSphere 5.5 updating to vCenter Server 5.5 U3d running on Windows will remediate the issue.
                </p>
                
                <p>
                  In case the Windows Firewall is enabled on the system that has vCenter Server Windows installed, remote exploitation of CVE-2015-2342 is not possible. Even if the Windows Firewall is enabled, users are advised to install the additional patch in order to remove the local privilege elevation.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
                </p>
                
                <div>
                  <div>
                    <table border="0">
                      <tr>
                        <td>
                          VMware Product
                        </td>
                        
                        <td>
                          Product Version
                        </td>
                        
                        <td>
                          Running on
                        </td>
                        
                        <td>
                          Replace with/ Apply Patch
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          6.0
                        </td>
                        
                        <td>
                          Any
                        </td>
                        
                        <td>
                          6.0.0b and above
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          5.5
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          (5.5 U3/U3a/U3b + KB *) or 5.5 U3d
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          5.5
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.5 U3 and above
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          5.1
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          (5.1 U3b + KB *) or 5.1 U3d
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
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
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          5.0
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          5.0 U3e + KB *
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
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
                    </table>
                  </div>
                </div>
                
                <p>
                  * An additional patch provided in VMware KB article 2144428 must be installed on vCenter Server Windows 5.0 U3e, 5.1 U3b, 5.5 U3, 5.5 U3a, and 5.5 U3b in order to remediate CVE-2015-2342.<br /> This patch is not needed when updating to 5.1 U3d or 5.5 U3d, or when installing 5.1 U3d or 5.5 U3d.
                </p>
                
                <p>
                  c. VMware vCenter Server vpxd denial-of-service vulnerability
                </p>
                
                <p>
                  VMware vCenter Server does not properly sanitize long heartbeat messages. Exploitation of this issue may allow an unauthenticated attacker to create a denial-of-service condition in the vpxd service.
                </p>
                
                <p>
                  VMware would like to thank the Google Security Team for reporting this issue to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2015-1047 to this issue.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
                </p>
                
                <div>
                  <div>
                    <table border="0">
                      <tr>
                        <td>
                          VMware Product
                        </td>
                        
                        <td>
                          Product Version
                        </td>
                        
                        <td>
                          Running on
                        </td>
                        
                        <td>
                          Replace with/ Apply Patch
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          6.0
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
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          5.5
                        </td>
                        
                        <td>
                          Any
                        </td>
                        
                        <td>
                          5.5u2
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          5.1
                        </td>
                        
                        <td>
                          Any
                        </td>
                        
                        <td>
                          5.1u3
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vCenter Server
                        </td>
                        
                        <td>
                          5.0
                        </td>
                        
                        <td>
                          Any
                        </td>
                        
                        <td>
                          5.0u3e
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
                  Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.<br /> vCenter Server<br /> Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a>ESXi<br /> Downloads:<br /> <a href="https://www.vmware.com/patchmgr/findPatch.portal">https://www.vmware.com/patchmgr/findPatch.portal</a>
                </p>
                
                <p>
                  Documentation:<br /> <a href="http://kb.vmware.com/kb/2110247">http://kb.vmware.com/kb/2110247</a><br /> <a href="http://kb.vmware.com/kb/2114875">http://kb.vmware.com/kb/2114875</a><br /> <a href="http://kb.vmware.com/kb/2120209">http://kb.vmware.com/kb/2120209</a>
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
                <p>
                  <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5177">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5177</a><br /> <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-2342">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-2342</a><br /> <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-1047">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-1047</a>
                </p>
                
                <p>
                  <a href="http://kb.vmware.com/kb/2133118">http://kb.vmware.com/kb/2133118</a><br /> <a href="http://kb.vmware.com/kb/2144428">http://kb.vmware.com/kb/2144428</a>
                </p>
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
                <strong>6. Change log</strong>
              </div>
              
              <div>
              </div>
              
              <div>
                2015-10-01 VMSA-2015-0007<br /> Initial security advisory in conjunction with ESXi 5.0, 5.1 patches and VMware vCenter Server 5.1 u3b, 5.0 u3e on 2015-10-01.2015-10-06 VMSA-2015-0007.1<br /> Updated security advisory in conjunction with the release of ESXi 5.5 U3a on 2015-10-06. Added a note to section 3.a to alert customers to a non-security issue in ESXi 5.5 U3 that is addressed in ESXi 5.5 U3a.2015-10-20 VMSA-2015-0007.2<br /> Updated security advisory to reflect that CVE-2015-2342 is fixed in an earlier vCenter Server version (6.0.0b) than originally reported (6.0 U1) and that the port required to exploit the vulnerability is blocked in the appliance versions of the software (5.1 and above).2016-02-12 VMSA-2015-0007.3<br /> Updated security advisory to add that an additional patch is required on vCenter Server 5.0 U3e, 5.1 U3b and 5.5 U3/U3a/U3b running on Windows to remediate CVE-2015-2342.</p> 
                
                <p>
                  2016-04-27 VMSA-2015-0007.4<br /> Updated security advisory to add that vCenter Server 5.5 U3d running on Windows addresses CVE-2105-2342 without the need to install the additional patch.
                </p>
                
                <p>
                  2016-05-24 VMSA-2015-0007.5<br /> Updated security advisory to add that vCenter Server 5.1 U3d running on Windows addresses CVE-2105-2342 without the need to install the additional patch.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>