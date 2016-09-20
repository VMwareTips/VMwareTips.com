---
id: 2988
title: NEW VMSA-2016-0004 VMware product updates address a critical security issue in the VMware Client Integration Plugin
date: 2016-04-14T12:28:13+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=2988
permalink: /2016/04/14/security-announce-new-vmsa-2016-0004-vmware-product-updates-address-a-critical-security-issue-in-the-vmware-client-integration-plugin/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 20443
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
### VMware product updates address a critical security issue in the VMware Client Integration Plugin

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
            VMSA-2016-0004
          </td>
        </tr>
        
        <tr>
          <td>
            Synopsis:
          </td>
          
          <td>
            VMware product updates address a critical security issue in the VMware Client Integration Plugin
          </td>
        </tr>
        
        <tr>
          <td>
            Issue date:
          </td>
          
          <td>
            2016-04-14
          </td>
        </tr>
        
        <tr>
          <td>
            Updated on:
          </td>
          
          <td>
            2016-04-14 (Initial Advisory)
          </td>
        </tr>
        
        <tr>
          <td>
            CVE numbers:
          </td>
          
          <td>
            CVE-2016-2076
          </td>
        </tr>
      </table>
    </div>
  </div>
</div>

<div>
  <div id="m_segment_1460568368853">
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
                <p>
                     VMware vCenter Server, vCloud Director (vCD), vRealize Automation (vRA)<br /> Identity Appliance, and the Client Integration Plugin (CIP) updates address<br /> a critical security issue.
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
                <p>
                     vCenter Server 6.0 prior to 6.0 U2<br /> vCenter Server 5.5 U3a, U3b, U3c
                </p>
                
                <p>
                  vCloud Director 5.5.5
                </p>
                
                <p>
                  vRealize Automation Identity Appliance 6.2.4
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
                     a. Critical VMware Client Integration Plugin incorrect session handling
                </p>
                
                <p>
                  The VMware Client Integration Plugin does not handle session content<br /> in a safe way. This may allow for a Man in the Middle attack or Web<br /> session hijacking in case the user of the vSphere Web Client visits<br /> a malicious Web site.
                </p>
                
                <p>
                  The vulnerability is present in versions of CIP that shipped with:<br /> &#8211; vCenter Server 6.0 (any 6.0 version prior to 6.0 U2)<br /> &#8211; vCenter Server 5.5 U3a, U3b, U3c<br /> &#8211; vCloud Director 5.5.5<br /> &#8211; vRealize Automation Identity Appliance 6.2.4
                </p>
                
                <p>
                  In order to remediate the issue, both the server side (i.e. vCenter<br /> Server, vCloud Director, and vRealize Automation Identity Appliance)<br /> and the client side (i.e. CIP of the vSphere Web Client) will need<br /> to be updated.
                </p>
                
                <p>
                  The steps to remediate the issue are as follows:
                </p>
                
                <p>
                  A) Install an updated version of:<br /> &#8211; vCenter Server<br /> &#8211; vCloud Director<br /> &#8211; vRealize Automation Identity Appliance
                </p>
                
                <p>
                  B) After step A), update the Client Integration Plugin on the system<br /> from which the vSphere Web Client is used.<br /> Updating the plugin on vSphere and vRA Identity Appliance is<br /> explained in VMware Knowledge Base article 2145066.<br /> Updating the plugin on vCloud Director is initiated by a prompt<br /> when connecting the vSphere Web Client to the updated version of<br /> vCloud Director.
                </p>
                
                <p>
                  The Common Vulnerabilities and Exposures project (cve.mitre.org) has<br /> assigned the identifier CVE-2016-2076 to this issue.
                </p>
                
                <p>
                  Column 4 of the following table lists the action required to remediate the<br /> vulnerability in each release, if a solution is available.
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
                          any
                        </td>
                        
                        <td>
                          6.0 U2 *
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCenter Server
                        </td>
                        
                        <td>
                          5.5 U3a &#8211; U3c
                        </td>
                        
                        <td>
                          any
                        </td>
                        
                        <td>
                          5.5 U3d *
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
                          not affected
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
                          not affected
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
                          not affected **
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
                          not affected
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vCloud Director
                        </td>
                        
                        <td>
                          5.5.5
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          5.5.6 *
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          vRA Identity Appliance
                        </td>
                        
                        <td>
                          7.x
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
                          vRA Identity Appliance
                        </td>
                        
                        <td>
                          6.2.4
                        </td>
                        
                        <td>
                          Linux
                        </td>
                        
                        <td>
                          6.2.4.1 *
                        </td>
                      </tr>
                      
                      <tr>
                        <td>
                          Client Integration Plugin
                        </td>
                        
                        <td>
                          see text above
                        </td>
                        
                        <td>
                          Windows, Mac OS
                        </td>
                        
                        <td>
                          see item B above
                        </td>
                      </tr>
                    </table>
                  </div>
                </div>
                
                <p>
                  * After installing the updated version, the Client Integration Plugin<br /> will need to be updated on all systems from which the vSphere Web<br /> Client is used to connect to vCenter Server, vCloud Director and<br /> vRealize Automation Identity Manager.
                </p>
                
                <p>
                  ** vCloud Director 8.0.0 did not ship with a vulnerable CIP version, and<br /> vCloud Director 8.0.1 shipped with the updated version of the CIP.
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
                  vCenter Server
                </p>
                
                <p>
                  Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a><br /> <a href="http://pubs.vmware.com/Release_Notes/en/vsphere/55/vsphere-vcenter-server-55u3d-release-notes.html">http://pubs.vmware.com/Release_Notes/en/vsphere/55/vsphere-vcenter-server-55u3d-release-notes.htm</a>l
                </p>
                
                <p>
                  vCloud Director 5.5.6
                </p>
                
                <p>
                  Downloads and Documentation:<br /> <a name="&lpos=content : 7" href="https://www.vmware.com/go/download/vcloud-director"></a>https://www.vmware.com/go/download/vcloud-director<br /> <a href="http://pubs.vmware.com/Release_Notes/en/vcd/556/rel_notes_vcloud_director_556.html">http://pubs.vmware.com/Release_Notes/en/vcd/556/rel_notes_vcloud_director_556.html</a>
                </p>
                
                <p>
                  VMware vRealize Automation 6.2.4.1
                </p>
                
                <p>
                  Downloads and Doumentation:<br /> <a href="https://my.vmware.com/web/vmware/info/slug/infrastructure_operations_management/vmware_vrealize_automation/6_2">https://my.vmware.com/web/vmware/info/slug/infrastructure_operations_management/vmware_vrealize_automation/6_2<br /> </a>  (select &#8220;Go to Downloads&#8221; and scroll down to &#8220;Security Update&#8221;)<br /> <a href="http://pubs.vmware.com/Release_Notes/en/vra/vrealize-automation-624-release-notes.html">http://pubs.vmware.com/Release_Notes/en/vra/vrealize-automation-624-release-notes.html</a>
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
                     <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2076">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2076</a>
                </p>
                
                <p>
                  VMware Knowledge Base article 2145066<br /> <a href="https://kb.vmware.com/kb/2145066">kb.vmware.com/kb/2145066</a>
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
                     2016-04-14 VMSA-2016-0004<br /> Initial security advisory in conjunction with the release of VMware<br /> vSphere 5.5 U3d and vCloud Director 5.5.6 on 2016-04-14.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>