---
id: 2723
title: '[Security-announce] UPDATE : VMSA-2015-0003.9 &#8211; VMware product updates address critical information disclosure issue in JRE.'
date: 2015-07-02T20:05:28+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2723
permalink: /2015/07/02/security-announce-update-vmsa-2015-0003-9-vmware-product-updates-address-critical-information-disclosure-issue-in-jre/
redirect_from: /wp/2015/07/02/security-announce-update-vmsa-2015-0003-9-vmware-product-updates-address-critical-information-disclosure-issue-in-jre/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "6037"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
### VMware product updates address critical information disclosure issue in JRE

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
          VMSA-2015-0003.9
        </td>
      </tr>
      
      <tr>
        <td>
          Synopsis:
        </td>
        
        <td>
          VMware product updates address critical information disclosure issue in JRE
        </td>
      </tr>
      
      <tr>
        <td>
          Issue date:
        </td>
        
        <td>
          2015-04-02
        </td>
      </tr>
      
      <tr>
        <td>
          Updated on:
        </td>
        
        <td>
          2015-07-02
        </td>
      </tr>
      
      <tr>
        <td>
          CVE numbers:
        </td>
        
        <td>
          CVE-2014-6593, for other CVEs see JRE reference
        </td>
      </tr>
    </table>
  </div>
  
  <div>
  </div>
</div>

<div>
  <div id="m_segment_1427993906580">
    <div>
      <div>
        <strong>1. Summary</strong>
      </div>
      
      <div>
        VMware product updates address critical information disclosure issue in JRE.
      </div>
      
      <div>
        <!--more-->
      </div>
    </div>
    
    <div>
      <div>
        <strong>2. Relevant Releases</strong>
      </div>
      
      <div>
        Horizon View 6.x or 5.x<br /> Horizon Workspace Portal Server 2.1 or 2.0<br /> Horizon DaaS Platform 6.1.4 or 5.4.5<br /> vCloud Networking and Security prior to 5.5.4.1<br /> vCloud Connector 2.7<br /> vCloud Usage Meter 3.3
      </div>
      
      <div>
        vCenter Site Recovery Manager prior to 5.5.1.5
      </div>
      
      <div>
        vCenter Server 6.0, 5.5, 5.1 or 5.0
      </div>
      
      <div>
        vRealize Operations Manager 6.0
      </div>
      
      <div>
        vCenter Operations Manager 5.8.x or 5.7.x
      </div>
      
      <div>
        vCenter Support Assistant 5.5.1.x
      </div>
      
      <div>
        vRealize Application Services 6.2 or 6.1
      </div>
      
      <div>
        vCloud Application Director 6.0
      </div>
      
      <div>
        vRealize Automation 6.2 or 6.1
      </div>
      
      <div>
        vCloud Automation Center 6.0.1
      </div>
      
      <div>
        vSphere Replication prior to 5.8.0.2, 5.6.0.3 or 5.5.1.5
      </div>
      
      <div>
        vRealize Automation 6.2.x or 6.1.x
      </div>
      
      <div>
        vRealize Code Stream 1.1 or 1.0
      </div>
      
      <div>
        vFabric Postgres 9.3.6.0, 9.2.10.0 or 9.1.15.0
      </div>
      
      <div>
        vRealize Hyperic 5.8.x, 5.7.x or 5.0.x
      </div>
      
      <div>
        vSphere AppHA Prior to 1.1.x
      </div>
      
      <div>
        vSphere Big Data Extensions 2.1 and 2.0
      </div>
      
      <div>
        vCenter Chargeback Manager 2.7 or 2.6
      </div>
      
      <div>
        vRealize Business Adv/Ent 8.1 or 8.0
      </div>
      
      <div>
        vRealize Business Standard prior to 1.1.x or 1.0.x
      </div>
      
      <div>
        NSX for vSphere 6.1
      </div>
      
      <div>
        NSX for Multi-Hypervisor  prior to 4.2.4
      </div>
      
      <div>
        vCloud Director prior to 5.5.3
      </div>
      
      <div>
        vCloud Director Service Providers prior to 5.6.4.1
      </div>
      
      <div>
        vRealize Configuration Manager 5.7.x or 5.6.x
      </div>
      
      <div>
        vRealize Orchestrator 6.0, 5.5 or 5.1.3.1
      </div>
      
      <div>
        vRealize Infrastructure 5.8 or 5.7
      </div>
      
      <div>
        vRealize Log Insight 2.5, 2.0, 1.5 or 1.0
      </div>
      
      <div>
        vSphere Management Assistant 5.5 or 5.1
      </div>
      
      <div>
        vSphere Update Manager 6.0, 5.5, 5.1 or 5.0
      </div>
      
      <div>
        EVO:RAIL prior to 1.2.1
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
          a. Oracle JRE Update
        </div>
        
        <div>
          <p>
            Oracle JRE is updated in VMware products to address a critical security issue that existed in earlier releases of Oracle JRE.
          </p>
          
          <p>
            VMware products running JRE 1.7 Update 75 or newer and JRE 1.6 Update 91 or newer are not vulnerable to CVE-2014-6593, as documented in the Oracle Java SE Critical Patch Update Advisory of January 2015.
          </p>
          
          <p>
            This advisory also includes the other security issues that are addressed  in JRE 1.7 Update 75 and JRE 1.6 Update 91. The References section provides a link to the JRE advisory.
          </p>
          
          <p>
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the identifier CVE-2014-6593 to this issue. This issue is also known as &#8220;SKIP&#8221; or &#8220;SKIP-TLS&#8221;.
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
                    Apply Patch**
                  </td>
                </tr>
                
                <tr>
                  <td>
                    Horizon View
                  </td>
                  
                  <td>
                    6.x
                  </td>
                  
                  <td>
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
                    5.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.3.4
                  </td>
                </tr>
                
                <tr>
                  <td>
                    Horizon Workspace Portal Server
                  </td>
                  
                  <td>
                    2.1, 2.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    2.1.1
                  </td>
                </tr>
                
                <tr>
                  <td>
                    Horizon DaaS Platform
                  </td>
                  
                  <td>
                    6.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    6.1.4
                  </td>
                </tr>
                
                <tr>
                  <td>
                    Horizon DaaS Platform
                  </td>
                  
                  <td>
                    5.4
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.4.5
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCloud Networking and Security
                  </td>
                  
                  <td>
                    5.5
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.5.4.1*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCloud Connector
                  </td>
                  
                  <td>
                    2.7
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    2.7.1*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCloud Usage Meter
                  </td>
                  
                  <td>
                    3.3
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    3.3.3*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Site Recovery Manager
                  </td>
                  
                  <td>
                    5.5.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.5.1.5***
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Site Recovery Manager
                  </td>
                  
                  <td>
                    5.1.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    patch pending***
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Site Recovery Manager
                  </td>
                  
                  <td>
                    5.0.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    patch pending***
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
                    6.0.0a
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
                    Update 2e
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
                    Update 3a
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
                    Update 3d
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Operations Manager
                  </td>
                  
                  <td>
                    6.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111898">KB2111898</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Operations Manager
                  </td>
                  
                  <td>
                    5.8.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111172">KB2111172</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Operations Manager
                  </td>
                  
                  <td>
                    5.7.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111172">KB2111172</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Support Assistant
                  </td>
                  
                  <td>
                    5.5.1.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    6.0
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Application Services
                  </td>
                  
                  <td>
                    6.2
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111981">KB2111981</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Application Services
                  </td>
                  
                  <td>
                    6.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111981">KB2111981</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCloud Application Director
                  </td>
                  
                  <td>
                    6.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111981">KB2111981</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCloud Application Director
                  </td>
                  
                  <td>
                    5.2
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111981">KB2111981</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Automation
                  </td>
                  
                  <td>
                    6.2
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111658">KB2111658</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Automation
                  </td>
                  
                  <td>
                    6.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111658">KB2111658</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCloud Automation Center
                  </td>
                  
                  <td>
                    6.0.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111658">KB2111658</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Code Stream
                  </td>
                  
                  <td>
                    1.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111658">KB2111658</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Code Stream
                  </td>
                  
                  <td>
                    1.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111658">KB2111658</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vPostgres
                  </td>
                  
                  <td>
                    9.3.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    9.3.6.0
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vPostgres
                  </td>
                  
                  <td>
                    9.2.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    9.2.10.0
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vPostgres
                  </td>
                  
                  <td>
                    9.1.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    9.1.15.0
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Replication
                  </td>
                  
                  <td>
                    5.8.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.8.0.2
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Replication
                  </td>
                  
                  <td>
                    5.6.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.6.0.3
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Replication
                  </td>
                  
                  <td>
                    5.5.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.5.1.5
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Replication
                  </td>
                  
                  <td>
                    5.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    patch pending
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Hyperic
                  </td>
                  
                  <td>
                    5.8
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111337">KB2111337</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Hyperic
                  </td>
                  
                  <td>
                    5.7
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111337">KB2111337</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Hyperic
                  </td>
                  
                  <td>
                    5.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111337">KB2111337</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere AppHA
                  </td>
                  
                  <td>
                    1.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111336">KB2111336</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Big Data Extensions
                  </td>
                  
                  <td>
                    2.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2116604">KB2116604</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Big Data Extensions
                  </td>
                  
                  <td>
                    2.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2116604">KB2116604</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Data Protection
                  </td>
                  
                  <td>
                    6.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    patch pending*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Data Protection
                  </td>
                  
                  <td>
                    5.8
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    patch pending*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Data Protection
                  </td>
                  
                  <td>
                    5.5
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    patch pending*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Data Protection
                  </td>
                  
                  <td>
                    5.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    patch pending*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Chargeback Manager
                  </td>
                  
                  <td>
                    2.7
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2112011">KB2112011</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Chargeback Manager
                  </td>
                  
                  <td>
                    2.6
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2113178">KB2113178</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Business Adv/Ent
                  </td>
                  
                  <td>
                    8.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2112258">KB2112258</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Business Adv/Ent
                  </td>
                  
                  <td>
                    8.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2112258">KB2112258</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Business Standard
                  </td>
                  
                  <td>
                    6.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111802">KB2111802</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Business Standard
                  </td>
                  
                  <td>
                    1.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111802">KB2111802</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Business Standard
                  </td>
                  
                  <td>
                    1.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111802">KB2111802</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    NSX for vSphere
                  </td>
                  
                  <td>
                    6.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    6.1.4*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    NSX for Multi-Hypervisor
                  </td>
                  
                  <td>
                    4.2.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    4.2.4*
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
                  </td>
                  
                  <td>
                    5.5.3*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCloud Director For Service Providers
                  </td>
                  
                  <td>
                    5.6.4
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.6.4.1*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vCenter Application Discovery Manager
                  </td>
                  
                  <td>
                    7.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    patch pending*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Configuration Manager
                  </td>
                  
                  <td>
                    5.7.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111670">KB2111670</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Configuration Manager
                  </td>
                  
                  <td>
                    5.6
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111670">KB2111670</a>
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Infrastructure Navigator
                  </td>
                  
                  <td>
                    5.8
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.8.4*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Infrastructure Navigator
                  </td>
                  
                  <td>
                    5.7
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2111334">KB2111334</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Orchestrator
                  </td>
                  
                  <td>
                    6.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2112028">KB2112028</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Orchestrator
                  </td>
                  
                  <td>
                    5.5
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2112028">KB2112028</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Orchestrator
                  </td>
                  
                  <td>
                    5.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.1.3.1*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Log Insight
                  </td>
                  
                  <td>
                    2.5
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2113235">KB2113235</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Log Insight
                  </td>
                  
                  <td>
                    2.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2113235">KB2113235</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Log Insight
                  </td>
                  
                  <td>
                    1.5
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2113235">KB2113235</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vRealize Log Insight
                  </td>
                  
                  <td>
                    1.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    <a href="http://kb.vmware.com/kb/2113235">KB2113235</a>*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Management Assistant
                  </td>
                  
                  <td>
                    5.5.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.5.0.4
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Management Assistant
                  </td>
                  
                  <td>
                    5.1.x
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    5.1.0.3
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Update Manager
                  </td>
                  
                  <td>
                    6.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    6.0.0a*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Update Manager
                  </td>
                  
                  <td>
                    5.5
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    Update 2e*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Update Manager
                  </td>
                  
                  <td>
                    5.1
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    Update 3a*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    vSphere Update Manager
                  </td>
                  
                  <td>
                    5.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    Update 3d*
                  </td>
                </tr>
                
                <tr>
                  <td>
                    EVO:RAIL
                  </td>
                  
                  <td>
                    1.2.0
                  </td>
                  
                  <td>
                  </td>
                  
                  <td>
                    1.2.1*
                  </td>
                </tr>
              </table>
            </div>
          </div>
          
          <p>
            *     The severity of critical is lowered to important for this product as is not considered Internet facing<br /> **   Knowledge Base (KB) articles provides details of the patches and how to install them.<br /> *** vCenter Site Recovery Manager 5.0, 5.1, and 5.5 itself do not include JRE but they include the vSphere Replication appliance  which has JRE. vCenter Site Recovery 5.8 and 6.0 do not include JRE nor the vSphere Replication appliance.
          </p>
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
          <strong></strong>Please review the patch/release notes for your product and version and verify the checksum of your downloaded file.
        </div>
        
        <div>
          Horizon View 6.1, 5.3.4:<br /> Downloads:<br /> <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-610-GA&productId=492">https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-610-GA&productId=492</a><br /> <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-534-PREMIER&productId=396">https://my.vmware.com/web/vmware/details?downloadGroup=VIEW-534-PREMIER&productId=396</a></p> 
          
          <p>
            VMware Workspace Portal 2.1.1<br /> Download:<br /> <a href="https://my.vmware.com/web/vmware/details?downloadGroup=HZNWS211&productId=501&rPId=7586">https://my.vmware.com/web/vmware/details?downloadGroup=HZNWS211&productId=501&rPId=7586</a><br /> Documentation:<br /> <a href="https://www.vmware.com/support/horizon_workspace/doc/wp_release_notes_211.html">https://www.vmware.com/support/horizon_workspace/doc/wp_release_notes_211.html</a>
          </p>
          
          <p>
            Horizon DaaS Platform 6.1.4<br /> Download: <a href="https://my.vmware.com/web/vmware/details?downloadGroup=HORIZON-DAAS-610-BIN&productId=405&rPId=6527">https://my.vmware.com/web/vmware/details?downloadGroup=HORIZON-DAAS-610-BIN&productId=405&rPId=6527</a>
          </p>
          
          <p>
            Horizon DaaS Platform 5.4.5<br /> Download: <a href="https://my.vmware.com/web/vmware/details?downloadGroup=HORIZON-DAAS-ONPREM-540&productId=398&rPId=5214">https://my.vmware.com/web/vmware/details?downloadGroup=HORIZON-DAAS-ONPREM-540&productId=398&rPId=5214</a>
          </p>
          
          <p>
            vCloud Networking and Security 5.5.4.1<br /> Download: <a href="https://my.vmware.com/web/vmware/details?productId=360&rPId=7625&downloadGroup=VCNS5541">https://my.vmware.com/web/vmware/details?productId=360&rPId=7625&downloadGroup=VCNS5541</a><br /> Documentation: <a href="https://www.vmware.com/support/vshield/doc/releasenotes_vshield_5541.html">https://www.vmware.com/support/vshield/doc/releasenotes_vshield_5541.html</a>
          </p>
          
          <p>
            vCloud Connector 2.7.1<br /> Downloads and Documentation:<br /> <a href="http://www.vmware.com/support/hybridcloud/doc/hybridcloud_271_rel_notes.html">http://www.vmware.com/support/hybridcloud/doc/hybridcloud_271_rel_notes.html</a>
          </p>
          
          <p>
            vCloud Usage Meter 3.3.3<br /> <a href="download: https://my.vmware.com/en/group/vmware/get-download?downloadGroup=UMSV333">Download: https://my.vmware.com/en/group/vmware/get-download?downloadGroup=UMSV333</a>
          </p>
          
          <p>
            vCenter Site Recovery Manager 5.5.1.5<br /> Downloads:<br /> <a href="https://my.vmware.com/web/vmware/details?downloadGroup=SRM5515&productId=357&rPId=7774">https://my.vmware.com/web/vmware/details?downloadGroup=SRM5515&productId=357&rPId=7774  </a>
          </p>
          
          <p>
            Documentation:<br /> <a href="https://www.vmware.com/support/srm/srm-releasenotes-5-5-1.html">https://www.vmware.com/support/srm/srm-releasenotes-5-5-1.html</a>
          </p>
          
          <p>
            vCenter Server 6.0, 5.5, 5.1, 5.0<br /> Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a>
          </p>
          
          <p>
            vRealize Operations Manager 6.0.1<br /> Downloads and Documentation: <a href="http://kb.vmware.com/kb/2111898">http://kb.vmware.com/kb/2111898</a>
          </p>
          
          <p>
            vCenter Support Assistant 6.0<br /> Downloads and Documentation:<br /> <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VCSA600&productId=491">https://my.vmware.com/web/vmware/details?downloadGroup=VCSA600&productId=491</a>
          </p>
          
          <p>
            vRealize Application Services 6.2, 6.1<br /> Downloads and Documentation: <a href="http://kb.vmware.com/kb/2111981">http://kb.vmware.com/kb/2111981</a>
          </p>
          
          <p>
            NSX for vSphere 6.1<br /> Downloads and Documentation: <a href="https://my.vmware.com/web/vmware/details?productId=417&downloadGroup=NSX-V-614">https://my.vmware.com/web/vmware/details?productId=417&downloadGroup=NSX-V-614</a>
          </p>
          
          <p>
            NSX for Multi-Hypervisor 4.2.4<br /> Downloads and Documentation: <a href="https://my.vmware.com/web/vmware/info/slug/networking_security/vmware_nsx/4_x">https://my.vmware.com/web/vmware/info/slug/networking_security/vmware_nsx/4_x</a>
          </p>
          
          <p>
            vCloud Application Director 6.0<br /> Downloads and Documentation: <a href="http://kb.vmware.com/kb/2111981">http://kb.vmware.com/kb/2111981</a>
          </p>
          
          <p>
            vCloud Director for Service Providers 5.6.4.1<br /> Downloads and Documentation: <a href="https://www.vmware.com/support/pubs/vcd_sp_pubs.html">https://www.vmware.com/support/pubs/vcd_sp_pubs.html</a>
          </p>
          
          <p>
            vCenter Operations Manager  5.8.5, 5.7.4<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111172">http://kb.vmware.com/kb/2111172</a>
          </p>
          
          <p>
            vCloud Automation Center 6.0.1.2<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111658">http://kb.vmware.com/kb/2111658</a>
          </p>
          
          <p>
            vSphere Replication 5.8.0.2, 5.6.0.3, 5.5.1.5<br /> Downloads:<br /> <a href="https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5802">https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5802</a><br /> <a href="https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5603">https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5603</a><br /> <a href="https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5515">https://my.vmware.com/web/vmware/get-download?downloadGroup=VR5515</a>
          </p>
          
          <p>
            Documentation:<br /> <a href="http://kb.vmware.com/kb/2112025">http://kb.vmware.com/kb/2112025</a><br /> <a href="http://kb.vmware.com/kb/2112022">http://kb.vmware.com/kb/2112022</a>
          </p>
          
          <p>
            vRealize Automation 6.2.1, 6.1.1<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111658">http://kb.vmware.com/kb/2111658</a>
          </p>
          
          <p>
            vRealize Code Stream 1.1, 1.0<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111658">http://kb.vmware.com/kb/2111658</a>
          </p>
          
          <p>
            vFabric Postgres<br /> Downloads<br /> <a href="https://my.vmware.com/group/vmware/details?downloadGroup=VFPG_936&productId=373&rPId=7787">https://my.vmware.com/group/vmware/details?downloadGroup=VFPG_936&productId=373&rPId=7787<br /> </a><a href="https://my.vmware.com/group/vmware/details?downloadGroup=VFPG_92_10&productId=325&rPId=7788">https://my.vmware.com/group/vmware/details?downloadGroup=VFPG_92_10&productId=325&rPId=7788<br /> </a><a href="https://my.vmware.com/group/vmware/details?downloadGroup=VFPG_91_15&productId=274&rPId=7789">https://my.vmware.com/group/vmware/details?downloadGroup=VFPG_91_15&productId=274&rPId=7789<br /> </a><br /> vRealize Hyperic 5.8.4, 5.7.2, 5.0.3<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111337">http://kb.vmware.com/kb/KB2111337</a>
          </p>
          
          <p>
            vSphere AppHA 1.1.1<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111336">http://kb.vmware.com/kb/2111336</p> 
            
            <p>
              </a>vSphere Big Data Extensions 2.1 and 2.0<br /> Downloads and Documentation: <a href="http://kb.vmware.com/kb/2116604">http://kb.vmware.com/kb/2116604</a>
            </p>
            
            <p>
              vCenter Chargeback Manager 2.7<br /> Downloads and Documentation: <a href="http://kb.vmware.com/kb/2112011">http://kb.vmware.com/kb/2112011</a>
            </p>
            
            <p>
              vCenter Chargeback Manager 2.6<br /> Downloads and Documentation: <a href="http://kb.vmware.com/kb/2113178">http://kb.vmware.com/kb/2113178</a>
            </p>
            
            <p>
              vRealize Business Adv/Ent 8.1, 8.0<br /> Downloads and Documentation: <a href="http://kb.vmware.com/kb/2112258">http://kb.vmware.com/kb/2112258</a>
            </p>
            
            <p>
              vRealize Business Standard 6.0, 1.1 , 1.0<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111802">http://kb.vmware.com/kb/2111802</a>
            </p>
            
            <p>
              vCenter Configuration Manager 5.7.3<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111670">http://kb.vmware.com/kb/2111670</a>
            </p>
            
            <p>
              vRealize Infrastructure Navigator 5.8.4<br /> Download:<br /> <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VIN_584&productId=476">https://my.vmware.com/web/vmware/details?downloadGroup=VIN_584&productId=476</a>
            </p>
            
            <p>
              vRealize Infrastructure Navigator 5.7<br /> Downloads and Documentation:<br /> <a href="http://kb.vmware.com/kb/2111334">http://kb.vmware.com/kb/2111334</a>
            </p>
            
            <p>
              vRealize Orchestrator 6.0, 5.5<br /> Downloads and Documentation: <a href="http://kb.vmware.com/kb/2112028">http://kb.vmware.com/kb/2112028</a>
            </p>
            
            <p>
              vRealize Orchestrator 5.1.3.1<br /> Download: <a href="https://my.vmware.com/group/vmware/get-download?downloadGroup=VSP51-VCL-VCOVA-51U3A">https://my.vmware.com/group/vmware/get-download?downloadGroup=VSP51-VCL-VCOVA-51U3A</a><br /> Documentation: <a href="https://www.vmware.com/support/pubs/orchestrator_pubs.html">https://www.vmware.com/support/pubs/orchestrator_pubs.html</a>
            </p>
            
            <p>
              vSphere Management Assistant 5.5.0.4<br /> Download: <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VMA550&productId=352">https://my.vmware.com/web/vmware/details?downloadGroup=VMA550&productId=352</a><br /> Documentation: <a href="http://kb.vmware.com/kb/2112648">http://kb.vmware.com/kb/2112648</a>
            </p>
            
            <p>
              vSphere Management Assistant 5.1.0.3<br /> Download: <a href="https://my.vmware.com/web/vmware/details?downloadGroup=VSP510-VMA-510&productId=285">https://my.vmware.com/web/vmware/details?downloadGroup=VSP510-VMA-510&productId=285</a><br /> Documentation: <a href="http://kb.vmware.com/kb/2112647">http://kb.vmware.com/kb/2112647</a>
            </p>
            
            <p>
              vSphere Update Manager 6.0, 5.5, 5.1, 5.0<br /> Downloads and Documentation:<br /> <a href="https://www.vmware.com/go/download-vsphere">https://www.vmware.com/go/download-vsphere</a>
            </p>
            
            <p>
              EVO:RAIL 1.2.1<br /> Downloads and Documentation:<br /> <a href="https://my.vmware.com/group/vmware/details?productId=442&downloadGroup=EVORAIL1_2_1">https://my.vmware.com/group/vmware/details?productId=442&downloadGroup=EVORAIL1_2_1</a>
            </p></div> </div> </div> 
            
            <div>
              <div>
                <div>
                </div>
                
                <div>
                  <strong>5. References</strong>
                </div>
                
                <div>
                  <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-6593">http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-6593</a></p> 
                  
                  <p>
                    Oracle Java SE Critical Patch Update Advisory of January 2015<br /> <a href="http://www.oracle.com/technetwork/topics/security/cpujan2015-1972971.html">http://www.oracle.com/technetwork/topics/security/cpujan2015-1972971.html</a></div> </div> </div> 
                    
                    <div>
                      <div>
                        <div>
                        </div>
                        
                        <div>
                        </div>
                        
                        <div>
                          <strong>6. Change log</strong>
                        </div>
                        
                        <div>
                          <p>
                            2015-04-02 VMSA-2015-0003<br /> Initial security advisory in conjunction with the release of VMware Horizon View 6.1, 5.3.4; vCenter Operations Manager 5.8.5; vCenter Operations Manager 5.7.4; vCloud Automation Center 6.0.1.2; vSphere Replication 5.8.0.2, 5.6.0.3; vRealize Automation 6.2.1, 6.1.1; vRealize Code Stream 1.1, 1.0; vRealize Hyperic 5.8.4, 5.7.2, 5.0.3; vSphere AppHA 1.1.1; vRealize Business Standard 1.1.1, 1.0.1; vRealize Configuration Manager prior to 5.7.3; vRealize Infrastructure 5.7, 5.8.4 Patches released on 2015-04-02.
                          </p>
                          
                          <p>
                            2015-04-09 VMSA-2015-0003.1<br /> Updated security advisory in conjunction with the release of VMware Horizon DaaS Platform 6.1.4, 5.4.5; vRealize Operations Manager 6.0; vRealize Application Services 6.2; vRealize Application Services 6.1; vCloud Application Director 6.0; vCenter Chargeback Manager 2.7, 2.6; vCloud Director For Service Providers 5.6.4.1; vRealize Log Insight 2.5, 2.0, 1.5, 1.0 Patches released on 2015-04-09
                          </p>
                          
                          <p>
                            2015-04-13 VMSA-2015-0003.2<br /> Updated Security advisory in conjunction with the release of vRealize Business Adv/Ent 8.1, 8.0 Patches released on 2015-04-13.
                          </p>
                          
                          <p>
                            2015-04-16 VMSA-2015-0003.3<br /> Updated Security advisory in conjunction with the release of vCloud Connector 2.7.1; vCloud Usage Meter 3.3.3; vCenter Server 6.0, 5.5; vSphere Update Manager 6.0, 5.5 patches released on 2015-04-16.
                          </p>
                          
                          <p>
                            2015-04-17 VMSA-2015-0003.4<br /> Updated Security advisory in conjunction with the release of vCenter Site Recovery Manager 5.5.1.5 patches released on 2015-04-16.
                          </p>
                          
                          <p>
                            2015-04-23 VMSA-2015-0003.5<br /> Updated Security advisory in conjunction with the release of NSX for Multi-Hypervisor 4.2.4 and vFabric Postgres 9.3.6.0, 9.2.10.0 or 9.1.15.0 patches released on 2015-04-23.<br /> 2015-04-30 VMSA-2015-0003.6<br /> Updated Security advisory in conjunction with the release of vCloud Networking and Security 5.5.4.1, vCenter Server 5.1 Update 3a, vCenter Server 5.0 Update 3d, vRealize Orchestrator 5.1.3.1, vSphere Update Manager 5.1 Update 3a and vSphere Update Manager 5.0 Update 3d patches released on 2015-04-30.
                          </p>
                          
                          <p>
                            2015-05-07 VMSA-2015-0003.7<br /> Updated Security advisory in conjunction with the release of vCenter Support Assistant 6.0, vSphere Big Data Extensions 2.1 and 2.0, NSX for vSphere 6.1.4 patches released on 2015-05-07.
                          </p>
                          
                          <p>
                            2015-05-08 VMSA-2015-0003.8<br /> Updated Security advisory in conjunction with the release of vSphere Management Assistant 5.5 and 5.1 patches released on 2015-05-08.
                          </p>
                          
                          <p>
                            2015-07-02 VMSA-2015-0003.9<br /> Updated Security advisory in conjunction with the release of EVO:RAIL 1.2.1 patches released on 2015-07-02.
                          </p>
                        </div>
                      </div>
                    </div>
                    
                    <div>
                      <div>
                        <div>
                        </div>
                        
                        <div>
                          <strong>7. Contact</strong>
                        </div>
                        
                        <div>
                          E-mail list for product security notifications and announcements:<br /> <a href="http://lists.vmware.com/cgi-bin/mailman/listinfo/security-announce">http://lists.vmware.com/cgi-bin/mailman/listinfo/security-announce</a></p> 
                          
                          <p>
                            This Security Advisory is posted to the following lists:
                          </p>
                          
                          <ul>
                            <li>
                              security-announce at lists.vmware.com
                            </li>
                            <li>
                              bugtraq at securityfocus.com
                            </li>
                            <li>
                              fulldisclosure at seclists.org
                            </li>
                          </ul>
                          
                          <p>
                            E-mail: security at vmware.com<br /> PGP key at: <a href="http://kb.vmware.com/kb/1055">http://kb.vmware.com/kb/1055</a>
                          </p>
                          
                          <p>
                            VMware Security Advisories<br /> <a href="http://www.vmware.com/security/advisories">http://www.vmware.com/security/advisories</a>
                          </p>
                          
                          <p>
                            VMware Security Response Policy<br /> <a href="https://www.vmware.com/support/policies/security_response.html">https://www.vmware.com/support/policies/security_response.html</a>
                          </p>
                          
                          <p>
                            VMware Lifecycle Support Phases<br /> <a href="https://www.vmware.com/support/policies/lifecycle.html">https://www.vmware.com/support/policies/lifecycle.html</a>
                          </p>
                          
                          <p>
                            Twitter<br /> <a href="https://twitter.com/VMwareSRC">https://twitter.com/VMwareSRC</a>
                          </p>
                        </div>
                      </div>
                    </div></div> </div> 
                    
                    <p>
                      &nbsp;
                    </p>