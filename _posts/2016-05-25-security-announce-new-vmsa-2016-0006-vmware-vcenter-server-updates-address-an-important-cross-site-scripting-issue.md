---
id: 3024
title: NEW VMSA-2016-0006 VMware vCenter Server updates address an important cross-site scripting issue
date: 2016-05-25T00:21:16+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=3024
permalink: /2016/05/25/security-announce-new-vmsa-2016-0006-vmware-vcenter-server-updates-address-an-important-cross-site-scripting-issue/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 8685
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
          VMSA-2016-0006
        </td>
      </tr>
      
      <tr>
        <td>
          Synopsis:
        </td>
        
        <td>
          VMware vCenter Server updates address an important cross-site scripting issue
        </td>
      </tr>
      
      <tr>
        <td>
          Issue date:
        </td>
        
        <td>
          2016-05-24
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
          CVE-2016-2078
        </td>
      </tr>
    </table>
  </div>
  
  <div>
  </div>
</div>

<div>
  <div id="m_segment_1464132679330">
    <div>
      <div>
        <div>
          <div>
            <div>
              <div>
                <strong>1. Summary</strong>
              </div>
              
              <div>
                VMware vCenter Server updates address an important cross-site scripting issue.
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
              </div>
              
              <div>
                vCenter Server 6.0 prior to 6.0 update 2<br /> vCenter Server 5.5 prior to 5.5 update 3d<br /> vCenter Server 5.1 prior to 5.1 update 3d
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
                a. Reflected cross-site scripting issue through flash parameter injectionThe vSphere Web Client contains a reflected cross-site scripting vulnerability<br /> that occurs through flash parameter injection. An attacker can exploit this issue<br /> by tricking a victim into clicking a malicious link.VMware would like to thank John Page aka hyp3rlinx for reporting this issue to us.</p> 
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has<br /> assigned the identifier CVE-2016-2078 to this issue.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to remediate<br /> the vulnerability in each release, if a solution is available.
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
                          6.0 U2*
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
                          Not Affected
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
                          5.5 U3d*
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
                          Not Affected
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
                          5.1 U3d*
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
                          Not Affected
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
                          Any
                        </td>
                        
                        <td>
                          Not Affected
                        </td>
                      </tr>
                    </table>
                  </div>
                </div>
                
                <address>
                    *Client side component of the vSphere Web Client does not need to be updated<br /> to remediate CVE-2016-2078. Updating the vCenter Server is sufficient to<br /> remediate this issue. 
                </address>
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
              </div>
              
              <div>
                   Please review the patch/release notes for your product and<br /> version and verify the checksum of your downloaded file.vCenter Server<br /> &#8212;&#8212;&#8212;&#8212;&#8211;<br /> Downloads and Documentation:<br /> https://www.vmware.com/go/download-vsphere
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
              </div>
              
              <div>
                <strong>5. References</strong>
              </div>
              
              <div>
              </div>
              
              <div>
                http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2078
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
              </div>
              
              <div>
                2016-05-24 VMSA-2016-0006<br /> Initial security advisory in conjunction with the release of VMware<br /> vCenter Server 5.1 U3d on 2016-05-24.
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>