---
id: 1722
title: 'VMware Security Alert &#8211; [Security-announce] UPDATED VMSA-2012-0013.1 VMware vSphere and vCOps updates to third party libraries'
date: 2012-09-16T21:17:41+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1722
permalink: /2012/09/16/vmware-security-alert-security-announce-updated-vmsa-2012-0013-1-vmware-vsphere-and-vcops-updates-to-third-party-libraries/
redirect_from: /wp/2012/09/16/vmware-security-alert-security-announce-updated-vmsa-2012-0013-1-vmware-vsphere-and-vcops-updates-to-third-party-libraries/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "870"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
In our effort to provide our viewers with up to the minute information on VMware related news and topics, we&#8217;re posting the following Security Alert direct from the VMware Security Alert distribution.

<!--more-->

> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
                         
> VMware Security Advisory
> 
> Advisory ID: VMSA-2012-0013.1
  
> Synopsis: VMware vSphere and vCOps updates to third party libraries
  
> Issue date: 2012-08-30
  
> Updated on: 2012-09-13
  
> CVE numbers: &#8212; JRE &#8212;
                    
> See references
                
> &#8212; OpenSSL (userworld) &#8212;
                
> CVE-2010-4180, CVE-2010-4252, CVE-2011-0014,
                
> CVE-2011-4108, CVE-2011-4109, CVE-2011-4576,
                
> CVE-2011-4577, CVE-2011-4619, CVE-2012-0050
                
> &#8212; OpenSSL (service console) &#8212;
                
> CVE-2012-2110
                
> &#8212; kernel (service console) &#8212;
                
> CVE-2011-1833, CVE-2011-2484, CVE-2011-2496,
                
> CVE-2011-3188, CVE-2011-3209, CVE-2011-3363,
                
> CVE-2011-4110, CVE-2011-1020, CVE-2011-4132,
                
> CVE-2011-4324, CVE-2011-4325, CVE-2012-0207,
                
> CVE-2011-2699, CVE-2012-1583
                
> &#8212; Perl (service console) &#8212;
                
> CVE-2010-2761, CVE-2010-4410, CVE-2011-3597
                
> &#8212; libxm2 (service console) &#8212;
                
> CVE-2012-0841
                
> &#8212; glibc (service console) &#8212;
                
> CVE-2009-5029, CVE-2009-5064, CVE-2010-0830,
                
> CVE-2011-1089, CVE-2011-4609, CVE-2012-0864
                
> &#8212; GnuTLS (service console) &#8212;
                
> CVE-2011-4128, CVE-2012-1569, CVE-2012-1573
                
> &#8212; popt and rpm (service console) &#8212;
                
> CVE-2012-0060, CVE-2012-0061, CVE-2012-0815
                
> &#8212; Apache struts &#8212;
                
> CVE-2012-0393
  
> &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
  
> 1. Summary
> 
> VMware has updated several third party libraries in vSphere and vcOps
     
> to address multiple security vulnerabilities.
> 
> 2. Relevant releases
> 
> VMware vCenter 4.1 without Update 3
     
> VMware vCenter 4.0 without Update 4a
> 
> VMware vCenter Update Manager 4.1 without Update 3
     
> VMware vCenter Update Manager 4.0 without Update 4a
> 
> VMware ESX 4.1 without patches ESX410-201208101-SG, ESX410-201208102-SG,
           
> ESX410-201208103-SG, ESX410-201208104-SG, ESX410-201208105-SG,
           
> ESX410-201208106-SG, ESX410-201208107-SG
> 
> VMware ESX 4.0 without patches ESX400-201209401-SG,
           
> ESX400-201209402-SG, ESX400-201209404-SG
> 
> VMware ESXi 4.1 without patch ESXi410-201208101-SG
> 
> VMware vCOps 5.0.2 or earlier
> 
> 3. Problem Description
> 
> a. vCenter and ESX update to JRE 1.6.0 Update 31
> 
> The Oracle (Sun) JRE is updated to version 1.6.0_31, which
        
> addresses multiple security issues. Oracle has documented the
        
> CVE identifiers that are addressed by this update in the Oracle
        
> Java SE Critical Patch Update Advisory of February 2012.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============= ======= ======= =================
          
> vCenter 5.0 Windows patch pending
          
> vCenter 4.1 Windows vCenter 4.1 Update 3
          
> vCenter 4.0 Windows not applicable **
          
> VirtualCenter 2.5 Windows not applicable **
> 
> Update Manager 5.0 Windows patch pending
          
> Update Manager 4.1 Windows not applicable **
          
> Update Manager 4.0 Windows not applicable **
> 
> hosted * any any not affected
> 
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208101-SG
          
> ESX 4.0 ESX not applicable **
          
> ESX 3.5 ESX not applicable **
> 
> * hosted products are VMware Workstation, Player, ACE, Fusion.
> 
> ** this product uses the Oracle (Sun) JRE 1.5.0 family
> 
> b. vCenter Update Manager update to JRE 1.5.0 Update 36
> 
> The Oracle (Sun) JRE is updated to 1.5.0_36 to address multiple
        
> security issues. Oracle has documented the CVE identifiers that
        
> are addressed in JRE 1.5.0_36 in the Oracle Java SE Critical
        
> Patch Update Advisory for June 2012.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============= ======== ======= =================
          
> vCenter 5.0 Windows not applicable **
          
> vCenter 4.1 Windows not applicable **
          
> vCenter 4.0 Windows vCenter 4.0 Update 4a
          
> VirtualCenter 2.5 Windows patch pending
> 
> Update Manager 5.0 Windows not applicable **
          
> Update Manager 4.1 Windows Update Manager 4.1 Update 3
          
> Update Manager 4.0 Windows Update Manager 4.0 Update 4a
> 
> hosted * any any not affected
> 
> ESXi any ESXi not affected
> 
> ESX 4.1 ESX not applicable **
          
> ESX 4.0 ESX ESX400-201209401-SG
          
> ESX 3.5 ESX patch pending
> 
> * hosted products are VMware Workstation, Player, ACE, Fusion.
> 
> ** this product uses the Oracle (Sun) JRE 1.6.0 family
> 
> c. Update to ESX/ESXi userworld OpenSSL library
> 
> The ESX/ESXi userworld OpenSSL library is updated from version
        
> 0.9.8p to version 0.9.8t to resolve multiple security issues.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
        
> has assigned the names CVE-2010-4180, CVE-2010-4252,
        
> CVE-2011-0014, CVE-2011-4108, CVE-2011-4109, CVE-2011-4576,
        
> CVE-2011-4577, CVE-2011-4619, and CVE-2012-0050 to these issues.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============== ======== ======= =================
          
> ESXi 5.0 ESXi patch pending
          
> ESXi 4.1 ESXi ESXi410-201208101-SG
          
> ESXi 4.0 ESXi patch pending
          
> ESXi 3.5 ESXi patch pending
> 
> ESX 4.1 ESX ESX410-201208101-SG
          
> ESX 4.0 ESX patch pending
          
> ESX 3.5 ESX patch pending
> 
> d. Update to ESX service console OpenSSL RPM
> 
> The service console OpenSSL RPM is updated to version
        
> 0.9.8e-22.el5_8.3 to resolve a security issue.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
        
> has assigned the name CVE-2012-2110 to this issue.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============== ======== ======= =================
          
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208103-SG
          
> ESX 4.0 ESX ESX400-201209401-SG
          
> ESX 3.5 ESX not applicable
> 
> e. Update to ESX service console kernel
> 
> The ESX service console kernel is updated to resolve multiple
        
> security issues.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
        
> has assigned the names CVE-2011-1833, CVE-2011-2484,
        
> CVE-2011-2496, CVE-2011-3188, CVE-2011-3209, CVE-2011-3363,
        
> CVE-2011-4110, CVE-2011-1020, CVE-2011-4132, CVE-2011-4324,
        
> CVE-2011-4325, CVE-2012-0207, CVE-2011-2699, and CVE-2012-1583
        
> to these issues.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============== ======== ======= =================
          
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208101-SG
          
> ESX 4.0 ESX ESX400-201209401-SG *
          
> ESX 3.5 ESX not applicable
> 
> * The service console kernel update on ESX 4.0 addresses
         
> CVEs that are labeled important. These are CVE-2012-0207,
         
> CVE-2011-2699, and CVE-2012-1583.
> 
> f. Update to ESX service console Perl RPM
> 
> The ESX service console Perl RPM is updated to
        
> perl-5.8.8.32.1.8999.vmw to resolve multiple security issues.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
        
> has assigned the names CVE-2010-2761, CVE-2010-4410, and
        
> CVE-2011-3597 to these issues.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============== ======== ======= =================
          
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208107-SG
          
> ESX 4.0 ESX patch pending
          
> ESX 3.5 ESX not applicable
> 
> g. Update to ESX service console libxml2 RPMs
> 
> The ESX service console libmxl2 RPMs are updated to
        
> libxml2-2.6.26-2.1.15.el5_8.2 and
        
> libxml2-python-2.6.26-2.1.15.el5_8.2 to resolve a security
        
> issue.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
        
> has assigned the name CVE-2012-0841 to this issue.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============== ======== ======= =================
          
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208102-SG
          
> ESX 4.0 ESX ESX400-201209402-SG
          
> ESX 3.5 ESX not applicable
> 
> h. Update to ESX service console glibc RPM
> 
> The ESX service console glibc RPM is updated to version
        
> glibc-2.5-81.el5_8.1 to resolve multiple security issues.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
        
> has assigned the names CVE-2009-5029, CVE-2009-5064,
        
> CVE-2010-0830, CVE-2011-1089, CVE-2011-4609, and CVE-2012-0864
        
> to these issue.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============== ======== ======= =================
          
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208104-SG
          
> ESX 4.0 ESX patch pending
          
> ESX 3.5 ESX not applicable
> 
> i. Update to ESX service console GnuTLS RPM
> 
> The ESX service console GnuTLS RPM is updated to version
        
> 1.4.1-7.el5_8.2 to resolve multiple security issues.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
        
> has assigned the names CVE-2011-4128, CVE-2012-1569, and
        
> CVE-2012-1573 to these issues.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============== ======== ======= =================
          
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208106-SG
          
> ESX 4.0 ESX ESX400-201209401-SG
          
> ESX 3.5 ESX not applicable
> 
> j. Update to ESX service console popt, rpm, rpm-libs,
        
> and rpm-python RPMS
> 
> The ESX service console popt, rpm, rpm-libs, and rpm-python RPMS
        
> are updated to the following versions to resolve multiple
        
> security issues:
           
> &#8211; popt-1.10.2.3-28.el5_8
           
> &#8211; rpm-4.4.2.3-28.el5_8
           
> &#8211; rpm-libs-4.4.2.3-28.el5_8
           
> &#8211; rpm-python-4.4.2.3-28.el5_8
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
        
> has assigned the name CVE-2012-0060, CVE-2012-0061, and
        
> CVE-2012-0815 to these issues.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============== ======== ======= =================
          
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208105-SG
          
> ESX 4.0 ESX ESX400-201209404-SG
          
> ESX 3.5 ESX not applicable
> 
> k. Vulnerability in third party Apache Struts component
> 
> The version of Apache Struts in vCenter Operations has been
        
> updated to 2.3.4 which addresses an arbitrary file overwrite
        
> vulnerability. This vulnerability allows an attacker to create
        
> a denial of service by overwriting arbitrary files without
        
> authentication. The attacker would need to be on the same network
        
> as the system where vCOps is installed.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org) has
        
> assigned the name CVE-2012-0393 to this issue.
> 
> Note: Apache struts 2.3.4 addresses the following issues as well:
        
> CVE-2011-5057, CVE-2012-0391, CVE-2012-0392, CVE-2012-0394. It
        
> was found that these do not affect vCOps.
> 
> VMware would like to thank Alexander Minozhenko from ERPScan for
        
> reporting this issue to us.
> 
> Column 4 of the following table lists the action required to
        
> remediate the vulnerability in each release, if a solution is
        
> available.
> 
> VMware Product Running Replace with/
          
> Product Version on Apply Patch
          
> ============ ======== ======= =================
          
> vCOps 5.0.2 Windows vCOps 5.0.3
          
> vCOps 5.0.2 Linux vCOps 5.0.3
          
> vCOps 1.0.x any affected, update to vCOps 5.0.3
> 
> vCO 4.2 Windows not affected
          
> vCO 4.1 Windows see VMSA-2011-0005 *
          
> vCO 4.0 Windows see VMSA-2011-0005 *
> 
> * Update releases for vCO that came out in 2011 and that are
            
> documented in VMSA-2011-0005, already address the Apache struts
            
> CVEs listed above.
> 
> 4. Solution
> 
> Please review the patch/release notes for your product and
     
> version and verify the checksum of your downloaded file.
> 
> vCenter Server 4.1 Update 3
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
     
> The download for vCenter Server includes vSphere Update Manager,
     
> vSphere Client, and vCenter Orchestrator
> 
> Download link
> 
> http://downloads.vmware.com/d/info/datacenter\_cloud\_infrastructure/vmware_v
  
> sphere/4_1
> 
> Release Notes
     
> https://www.vmware.com/support/vsphere4/doc/vsp\_vc41\_u3\_rel\_notes.html
> 
> VMware-VIMSetup-all-4.1.0-816786.iso
     
> md5sum: c1fd9189783e615fec4864ff6b8c86bd
     
> sha1sum: 38c03ac195939bd23da666b9ee98ef7c9c912a55
> 
> VMware-VIMSetup-all-4.1.0-816786.zip
     
> md5sum: d20705520fc4b5bccd71b060283e5b59
     
> sha1sum: ea2a84544cd6cd29447c4ce905111e7dfc62f4cd
> 
> vCenter Server 4.0 Update 4a
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
     
> The download for vCenter Server includes vSphere Update Manager,
     
> vSphere Client, and vCenter Orchestrator
> 
> Download link
> 
> http://downloads.vmware.com/d/info/datacenter\_cloud\_infrastructure/vmware_v
  
> sphere/4_0
> 
> Release Notes
     
> https://www.vmware.com/support/vsphere4/doc/vsp\_vc40\_u4a\_rel\_notes.html
> 
> VMware-VIMSetup-all-4.0.0-818020.iso
     
> md5sum: aa362485d8a9d4ad9dc4a647aba6701e
     
> sha1sum: c37c1e0983e5b3011a1d27fa58602150427dc466
> 
> VMware-VIMSetup-all-4.0.0-818020.zip
     
> md5sum: 531af0519e4c36fafab990447b55198b
     
> sha1sum: 8fb39414d034127de0052adf00e3356cc04593ed
> 
> ESXi and ESX
     
> &#8212;&#8212;&#8212;&#8212;
     
> http://downloads.vmware.com/go/selfsupport-download
> 
> ESXi 4.1
     
> &#8212;&#8212;&#8211;
     
> File: update-from-esxi4.1-4.1_update03.zip
     
> md5sum: b35267e3c96a8ebd2e3acac09538cdf5
     
> sha1sum: 2b2d456e89964528f25c01ae5d84edbd2bbcdefb
     
> http://kb.vmware.com/kb/2020373
     
> update-from-esxi4.1-4.1_update03 contains ESXi410-201208101-SG
> 
> ESX 4.1
     
> &#8212;&#8212;-
     
> File: update-from-esx4.1-4.1_update3.zip
     
> md5sum: a4a45aba880d64210badade8d7c81904
     
> sha1sum: 4ed1ef2b56fa30deec999916367ab278dc5b1840
     
> http://kb.vmware.com/kb/2020362
     
> update-from-esx4.1-4.1_update03 contains ESX410-201208101-SG,
     
> ESX410-201208102-SG, ESX410-201208103-SG, ESX410-201208104-SG,
     
> ESX410-201208105-SG, ESX410-201208106-SG, ESX410-201208107-SG
> 
> ESX 4.0
     
> &#8212;&#8212;-
     
> File: ESX400-201209001
     
> md5sum: 7faa79ea8d458e994db308933424a0ee
     
> sha1sum: 8f798a233cc28b203c3c8e0d44a1287af6c1ceb8
     
> http://kb.vmware.com/kb/2019661
     
> ESX400-201209001 contains ESX400-201209401-SG,
     
> ESX400-201209402-SG, ESX400-201209404-SG
> 
> vCOps 5.0.3
     
> &#8212;&#8212;&#8212;&#8211;
     
> Download link
> 
> https://my.vmware.com/web/vmware/info/slug/infrastructure\_operations\_manage
  
> ment/vmware\_vcenter\_operations/5_0
> 
> Release Notes
     
> https://www.vmware.com/support/pubs/vcops-pubs.html
> 
> 5. References
> 
> &#8212; JRE &#8212;
     
> Oracle Java SE Critical Patch Update Advisory of February 2012
> 
> http://www.oracle.com/technetwork/topics/security/javacpufeb2012-366318.htm
  
> l
> 
> Oracle Java SE Critical Patch Update Advisory for June 2012
> 
> http://www.oracle.com/technetwork/topics/security/javacpujun2012-1515912.ht
  
> ml
> 
> &#8212; OpenSSL (userworld) &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-4180
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-4252
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-0014
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4108
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4109
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4576
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4577
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4619
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0050
> 
> &#8212; OpenSSL (service console) &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-2110
> 
> &#8212; kernel (service console) &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-1833
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-2484
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-2496
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3188
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3209
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3363
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4110
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-1020
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4132
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4324
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4325
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0207
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-2699
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1583
> 
> &#8212; Perl (service console) &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-2761
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-4410
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3597
> 
> &#8212; libxm2 (service console) &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0841
> 
> &#8212; glibc (service console) &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2009-5029
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2009-5064
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-0830
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-1089
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4609
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0864
> 
> &#8212; GnuTLS (service console) &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-4128
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1569
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1573
> 
> &#8212; popt and rpm (service console) &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0060
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0061
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0815
> 
> &#8212; Apache struts &#8212;
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0393
> 
> &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
> 
> 6. Change log
> 
> 2012-08-30 VMSA-2012-0013
     
> Initial security advisory in conjunction with the release of
     
> vSphere 4.1 U3 and vCOps 5.0.3 on 2012-08-30.
> 
> 2012-09-12 VMSA-2012-0013.1
     
> Updated security advisory in conjunction with the release of
     
> vSphere 4.0 U4a on 2012-09-12 and ESX 4.0 patches on 2012-09-13.
> 
> &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
> 
> 7. Contact
> 
> E-mail list for product security notifications and announcements:
     
> http://lists.vmware.com/cgi-bin/mailman/listinfo/security-announce
> 
> This Security Advisory is posted to the following lists:
> 
> * security-announce at lists.vmware.com
     
> * bugtraq at securityfocus.com
     
> * full-disclosure at lists.grok.org.uk
> 
> E-mail: security at vmware.com
     
> PGP key at: http://kb.vmware.com/kb/1055
> 
> VMware Security Advisories
     
> http://www.vmware.com/security/advisories
> 
> VMware security response policy
     
> http://www.vmware.com/support/policies/security_response.html
> 
> General support life cycle policy
     
> http://www.vmware.com/support/policies/eos.html
> 
> VMware Infrastructure support life cycle policy
     
> http://www.vmware.com/support/policies/eos_vi.html
> 
> Copyright 2012 VMware Inc. All rights reserved.
  
> \___\___\___\___\___\___\___\___\___\___\___\___\___\___\_____
  
> Security-announce mailing list
  
> Security-announce@lists.vmware.com
  
> http://lists.vmware.com/mailman/listinfo/security-announce