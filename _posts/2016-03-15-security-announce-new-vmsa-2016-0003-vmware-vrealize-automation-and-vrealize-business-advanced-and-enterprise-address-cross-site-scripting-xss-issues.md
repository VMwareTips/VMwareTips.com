---
id: 2976
title: 'NEW VMSA-2016-0003 &#8211; VMware vRealize Automation and vRealize Business Advanced and Enterprise address Cross-Site Scripting (XSS) issues'
date: 2016-03-15T12:40:18+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2976
permalink: /2016/03/15/security-announce-new-vmsa-2016-0003-vmware-vrealize-automation-and-vrealize-business-advanced-and-enterprise-address-cross-site-scripting-xss-issues/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 28030
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
### VMware vRealize Automation and vRealize Business Advanced and Enterprise address Cross-Site Scripting (XSS) issues.

<div>
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
            VMSA-2016-0003
          </td>
        </tr>
        
        <tr>
          <td>
            Synopsis:
          </td>
          
          <td>
            VMware vRealize Automation and vRealize Business Advanced and Enterprise address Cross-Site Scripting (XSS) issues.
          </td>
        </tr>
        
        <tr>
          <td>
            Issue date:
          </td>
          
          <td>
            2016-03-15
          </td>
        </tr>
        
        <tr>
          <td>
            Updated on:
          </td>
          
          <td>
            2016-03-15 (Initial Advisory)
          </td>
        </tr>
        
        <tr>
          <td>
            CVE numbers:
          </td>
          
          <td>
            CVE-2015-2344, CVE-2016-2075
          </td>
        </tr>
      </table>
    </div>
  </div>
</div>

<div>
  <div id="m_segment_1458004736602">
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
                VMware vRealize Automation and vRealize Business Advanced and Enterprise address Cross-Site Scripting (XSS) issues.
              </div>
              
              <div>
                <!--more-->
              </div>
            </div>
          </div>
          
          <div>
            <div>
              <div>
              </div>
              
              <div>
                <strong>2. Relevant Releases</strong>
              </div>
              
              <div>
                VMware vRealize Automation 6.x prior to 6.2.4<br /> VMware vRealize Business Advanced and Enterprise 8.x prior to 8.2.5
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
                a. Important Stored Cross-Site Scripting (XSS) issue in VMware vRealize AutomationVMware vRealize Automation contains a vulnerability that may allow for a Stored Cross-Site Scripting (XSS) attack. Exploitation of this issue may lead to the compromise of a vRA user&#8217;s client workstation.</p> 
                
                <p>
                  VMware would like to thank would like to thank Lukasz Plonka for reporting this issue to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2015-2344 to this issue.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
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
                          VMware vRealize Automation
                        </td>
                        
                        <td>
                          7.x
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
                          VMware vRealize Automation
                        </td>
                        
                        <td>
                          6.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          6.2.4
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vRealize Automation
                        </td>
                        
                        <td>
                          5.x
                        </td>
                        
                        <td>
                          Windows
                        </td>
                        
                        <td>
                          Not Affected
                        </td>
                      </tr>
                    </table>
                  </div>
                </div>
                
                <p>
                  b. Important Stored Cross-Site Scripting (XSS) issue in vRealize Business Advanced and Enterprise
                </p>
                
                <p>
                  VMware vRealize Business Advanced and Enterprise contains a vulnerability that may allow for a Stored Cross-Site Scripting (XSS) attack. Exploitation of this issue may lead to the compromise of a vRB user&#8217;s client workstation.
                </p>
                
                <p>
                  VMware would like to thank Alvaro Trigo Martin de Vidales of Deloitte Spain for reporting this issue to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-2075 to this issue.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
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
                          VMware vRealize Business Advanced and Enterprise
                        </td>
                        
                        <td>
                          8.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          8.2.5
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vRealize Business Advanced and Enterprise
                        </td>
                        
                        <td>
                          7.x
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
                          VMware vRealize Business Advanced and Enterprise
                        </td>
                        
                        <td>
                          6.x
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          Not Affected
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
                  Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
                </p>
                
                <p>
                  VMware vRealize Automation 6.2.4<br /> <a href="https://my.vmware.com/web/vmware/info/slug/infrastructure_operations_management/vmware_vrealize_automation/6_2">Downloads and Documentation</a>
                </p>
                
                <p>
                  VMware vRealize Business Advanced and Enterprise 8.2.5<br /> <a href="https://my.vmware.com/web/vmware/info/slug/infrastructure_operations_management/vmware_vrealize_business/8_2">Downloads and Documentation</a>
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
                <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-2344">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-2344</a><br /> <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2075">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2075</a>
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
                2016-03-15 VMSA-2016-0003 Initial security advisory in conjunction with the release of VMware vRealize Automation 6.2.4 and VMware vRealize Business Advanced and Enterprise 8.2.5 on 2016-03-15.
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>