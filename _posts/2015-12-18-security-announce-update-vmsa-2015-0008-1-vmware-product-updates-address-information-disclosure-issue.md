---
id: 2884
title: 'VMSA-2015-0008.1 &#8211; VMware product updates address information disclosure issue'
date: 2015-12-18T16:03:11+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=2884
permalink: /2015/12/18/security-announce-update-vmsa-2015-0008-1-vmware-product-updates-address-information-disclosure-issue/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 33853
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
        VMSA-2015-0008.1
      </td>
    </tr>
    
    <tr>
      <td>
        Synopsis:
      </td>
      
      <td>
        VMware product updates address information disclosure issue.
      </td>
    </tr>
    
    <tr>
      <td>
        Issue date:
      </td>
      
      <td>
        2015-11-18
      </td>
    </tr>
    
    <tr>
      <td>
        Updated on:
      </td>
      
      <td>
        2015-12-18
      </td>
    </tr>
    
    <tr>
      <td>
        CVE numbers:
      </td>
      
      <td>
        CVE-2015-3269 CVE-2015-5255
      </td>
    </tr>
  </table>
</div>

<div>
  <!--more-->
</div>

<div>
  <div id="m_segment_1447802578439">
    <div>
      <div>
        <div>
          <div>
            <div>
              <div>
                <strong>1. Summary</strong>
              </div>
              
              <div>
              </div>
              
              <div>
                VMware product updates address information disclosure issue.
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
              </div>
              
              <div>
                VMware vCenter Server 5.5 prior to version 5.5 update 3<br /> VMware vCenter Server 5.1 prior to version 5.1 update u3b<br /> VMware vCenter Server 5.0 prior to version 5.0 update u3e</p> 
                
                <p>
                  vCloud Director 5.6 prior to version 5.6.4<br /> vCloud Director 5.5 prior to version 5.5.3VMware Horizon View 6.0 prior to version 6.1<br /> VMware Horizon View 5.0 prior to version 5.3.4
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
              </div>
              
              <div>
                <strong>a. vCenter Server, vCloud Director, Horizon View information disclosure issue </strong>
              </div>
              
              <div>
                <p>
                  VMware products that use Flex BlazeDS may be affected by a flaw in the processing of XML External Entity (XXE) requests. A specially crafted XML request sent to the server could lead to unintended information be disclosed.
                </p>
                
                <p>
                  VMware would like to thank Matthias Kaiser of Code White GmbH for reporting this issue to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2015-3269 to this issue.
                </p>
                
                <p>
                  The product updates listed in the table below have also been determined to address a XML External Entity (XXE) Processing and Server Side Request Forgery vulnerability in Flex BlazeDS.
                </p>
                
                <p>
                  VMware would like to thank James Kettle of PortSwigger Web Security for reporting these issues to us.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2015-5255 to these issues.
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
                          vCenter Server
                        </td>
                        
                        <td>
                          6.0
                        </td>
                        
                        <td>
                          any
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
                          any
                        </td>
                        
                        <td>
                          5.5 update 3
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
                          any
                        </td>
                        
                        <td>
                          5.1 update u3b
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
                          any
                        </td>
                        
                        <td>
                          5.0 update u3e
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCloud Director
                        </td>
                        
                        <td>
                          5.6
                        </td>
                        
                        <td>
                          any
                        </td>
                        
                        <td>
                          5.6.4
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCloud Director
                        </td>
                        
                        <td>
                          5.5
                        </td>
                        
                        <td>
                          any
                        </td>
                        
                        <td>
                          5.5.3
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          Horizon View
                        </td>
                        
                        <td>
                          6.0
                        </td>
                        
                        <td>
                          any
                        </td>
                        
                        <td>
                          6.1
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          Horizon View
                        </td>
                        
                        <td>
                          5.3
                        </td>
                        
                        <td>
                          any
                        </td>
                        
                        <td>
                          5.3.4
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
              </div>
              
              <div>
                Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
              </div>
              
              <div>
                <p>
                  vCenter Server<br /> Downloads and Documentation: <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a>
                </p>
                
                <p>
                  vCloud Director For Service Providers<br /> Downloads and Documentation: <a href="https://www.vmware.com/support/pubs/vcd_pubs.html">https://www.vmware.com/support/pubs/vcd_pubs.html</a>
                </p>
                
                <p>
                  Horizon View 6.1, 5.3.4:<br /> Downloads: <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-610-GA&productId=492"><br /> https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-610-GA&productId=492</a> <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-534-PREMIER&productId=396"><br /> https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-534-PREMIER&productId=396</a>
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
              </div>
              
              <div>
                <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-3269">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-3269<br /> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5255</a>
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
                  2015-11-18 VMSA-2015-0008<br /> Initial security advisory
                </p>
                
                <p>
                  2015-12-18 VMSA-2015-0008.1<br /> Updated advisory to note these updates also address CVE-2015-5255
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>