---
id: 3071
title: New VMSA-2016-0008 VMware vRealize Log Insight addresses important and moderate security issues
date: 2016-06-09T22:18:29+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3071
permalink: /2016/06/09/security-announce-new-vmsa-2016-0008-vmware-vrealize-log-insight-addresses-important-and-moderate-security-issues/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 7079
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
          VMSA-2016-0008
        </td>
      </tr>
      
      <tr>
        <td>
          Synopsis:
        </td>
        
        <td>
          VMware vRealize Log Insight addresses important and moderate security issues.
        </td>
      </tr>
      
      <tr>
        <td>
          Issue date:
        </td>
        
        <td>
          2016-06-09
        </td>
      </tr>
      
      <tr>
        <td>
          Updated on:
        </td>
        
        <td>
          2016-06-09
        </td>
      </tr>
      
      <tr>
        <td>
          CVE numbers:
        </td>
        
        <td>
          CVE-2016-2081, CVE-2016-2082
        </td>
      </tr>
    </table>
  </div>
</div>

<div>
  <div id="m_segment_1465500052328">
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
                VMware vRealize Log Insight addresses important and moderate security issues.
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
                VMware vRealize Log Insight prior to 3.3.2
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
                a. Important stored cross-site scripting issue in VMware vRealize Log Insight
              </div>
              
              <div>
                <p>
                  VMware vRealize Log Insight contains a vulnerability that may allow for a stored cross-site scripting attack. Exploitation of this issue may lead to the hijack of an authenticated user&#8217;s session.
                </p>
                
                <p>
                  VMware would like to thank Lukasz Plonka for reporting this issue to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-2081 to this issue.
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
                          Replace with/Apply Patch
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vRealize Log Insight
                        </td>
                        
                        <td>
                          3.x
                        </td>
                        
                        <td>
                          Virtual Appliance
                        </td>
                        
                        <td>
                          3.3.2
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vRealize Log Insight
                        </td>
                        
                        <td>
                          2.x
                        </td>
                        
                        <td>
                          Virtual Appliance
                        </td>
                        
                        <td>
                          3.3.2
                        </td>
                      </tr>
                    </table>
                  </div>
                </div>
                
                <p>
                  b. Moderate cross-site request forgery issue in VMware vRealize Log Insight
                </p>
                
                <p>
                  VMware vRealize Log Insight contains a vulnerability that may allow for a cross-site request forgery attack. Exploitation of this issue may lead to an attacker replacing trusted content in the Log Insight UI without the user’s authorization.
                </p>
                
                <p>
                  VMware would like to thank Lukasz Plonka for reporting this issue to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2016-2082 to this issue.
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
                          Replace with/Apply Patch
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vRealize Log Insight
                        </td>
                        
                        <td>
                          3.x
                        </td>
                        
                        <td>
                          Virtual Appliance
                        </td>
                        
                        <td>
                          3.3.2
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          VMware vRealize Log Insight
                        </td>
                        
                        <td>
                          2.x
                        </td>
                        
                        <td>
                          Virtual Appliance
                        </td>
                        
                        <td>
                          3.3.2
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
                  VMware vRealize Log Insight 3.3.2<br /> Downloads and Documentation:<br /> <a href="https://my.vmware.com/en/web/vmware/info/slug/infrastructure_operations_management/vmware_vrealize_log_insight/3_3">Download VMware vRealize Log Insight</a>
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
                  <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2081">CVE-2016-2081</a><br /> <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2082">CVE-2016-2082</a>
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
                2016-06-09 VMSA-2016-0008 Initial security advisory in conjunction with the release of VMware vRealize Log Insight 3.3.2 on 2016-06-09.
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>