---
id: 3082
title: NEW VMSA-2016-0009 VMware vCenter Server updates address an important reflective cross-site scripting issue
date: 2016-06-14T22:56:35+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=3082
permalink: /2016/06/14/security-announce-new-vmsa-2016-0009-vmware-vcenter-server-updates-address-an-important-reflective-cross-site-scripting-issue/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 6284
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
          VMSA-2016-0009
        </td>
      </tr>
      
      <tr>
        <td>
          Synopsis:
        </td>
        
        <td>
          VMware vCenter Server updates address an important reflective cross-site scripting issue
        </td>
      </tr>
      
      <tr>
        <td>
          Issue date:
        </td>
        
        <td>
          2016-06-14
        </td>
      </tr>
      
      <tr>
        <td>
          Updated on:
        </td>
        
        <td>
          2016-06-14 (Initial Advisory)
        </td>
      </tr>
      
      <tr>
        <td>
          CVE numbers:
        </td>
        
        <td>
          CVE-2015-6931
        </td>
      </tr>
    </table>
  </div>
</div>

<div>
  <div id="m_segment_1465946106673">
    <div>
      <div>
        <div>
          <div>
            <div>
              <div>
              </div>
              
              <div>
                <strong>1. Summary</strong>
              </div>
              
              <div>
                VMware vCenter Server updates address an important refelctive<br /> cross-site scripting issue.
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
                vCenter Server 5.5 prior to 5.5 update 2d<br /> vCenter Server 5.1 prior to 5.1 update 3d<br /> vCenter Server 5.0 prior to 5.0 update 3g
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
                <p>
                     a. Important vCenter Server reflected cross-site scripting issue
                </p>
                
                <p>
                  The vSphere Web Client contains a reflected cross-site scripting<br /> vulnerability due to a lack of input sanitization. An attacker can<br /> exploit this issue by tricking a victim into clicking a malicious<br /> link.
                </p>
                
                <p>
                  VMware would like to thank Matt Schmidt for reporting this issue to<br /> us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has<br /> assigned the identifier CVE-2015-6931 to this issue.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to<br /> remediate the vulnerability in each release, if a solution is<br /> available.
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
                          Any
                        </td>
                        
                        <td>
                          not affected
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
                          Any
                        </td>
                        
                        <td>
                          5.5 U2d *
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
                          Any
                        </td>
                        
                        <td>
                          5.1 U3d *
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
                          5.0 U3g *
                        </td>
                      </tr>
                    </table>
                  </div>
                </div>
                
                <p>
                  * The client side component of the vSphere Web Client does not need<br /> to be updated to remediate CVE-2015-6931. Updating the vCenter<br /> Server is sufficient to remediate this issue.
                </p>
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
                <strong>4. Solution</strong>
              </div>
              
              <div>
                <p>
                  Please review the patch/release notes for your product and<br /> version and verify the checksum of your downloaded file.
                </p>
                
                <p>
                  vCenter Server<br /> &#8212;&#8212;&#8212;&#8212;&#8212;&#8211;<br /> Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a>
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
                  <strong><a name="&lpos=content : 6" href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-6931"></a></strong>http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-6931
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
                <p>
                  2016-06-14 VMSA-2016-0009<br /> Initial security advisory in conjunction with the release of VMware<br /> vCenter Server 5.0 U3g on 2016-06-14.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>