---
id: 1709
title: 'VMware Security Alert &#8211; [Security-announce] UPDATED VMSA-2012-0003.1 VMware VirtualCenter Update and ESX 3.5 patch update JRE'
date: 2012-09-15T16:07:26+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1709
permalink: /2012/09/15/vmware-security-alert-security-announce-updated-vmsa-2012-0003-1-vmware-virtualcenter-update-and-esx-3-5-patch-update-jre-2/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 738
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
> Advisory ID: VMSA-2012-0003.1
  
> Synopsis: VMware VirtualCenter Update and ESX 3.5 patch update JRE
  
> Issue date: 2012-03-08
  
> Updated on: 2012-09-13
  
> CVE numbers: See references
   
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
> 
> 1. Summary
> 
> VMware VirtualCenter Update 6b and ESX 3.5 patch update JRE.
> 
> 2. Relevant releases
> 
> VirtualCenter 2.5 previous to Update 6b
> 
> ESX 3.5 without patch ESX350-201203401-SG
> 
> 3. Problem Description
> 
> a. VirtualCenter and ESX, Oracle (Sun) JRE update 1.5.0_32
> 
> Oracle (Sun) JRE is updated to version 1.5.0_32, which addresses
      
> multiple security issues that existed in earlier releases of Oracle
      
> (Sun) JRE.
> 
> Oracle has documented the CVE identifiers that are addressed in
      
> JRE 1.5.0_32 in the Oracle Java SE Critical Patch Update Advisory of
      
> October 2011.
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
      
> vCenter 4.0 Windows see VMSA-2012-0013
      
> VirtualCenter 2.5 Windows VirtualCenter 2.5 Update 6b
> 
> hosted * any any not affected
> 
> ESXi any ESXi not affected
> 
> ESX 4.1 ESX not applicable **
      
> ESX 4.0 ESX see VMSA-2012-0013
      
> ESX 3.5 ESX ESX350-201203401-SG
> 
> * hosted products are VMware Workstation, Player, ACE, Fusion.
> 
> ** this product uses the Oracle (Sun) JRE 1.6.0 family
> 
> 4. Solution
> 
> VMware Virtual Center 2.5 Update 6b
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
     
> Version 2.5 Update 6b
     
> Build Number 598800
     
> Release Date 2012/03/08
     
> Type Product Binaries
> 
> http://www.vmware.com/download/download.do?downloadGroup=VC250U6B
> 
> vCenter Server DVD image &#8211; English only version
     
> File type: iso
     
> MD5SUM: 085f7bddd2adf2c4ba5bd066271e2b06
     
> SHA1SUM: 019ff0a67d150d0a3dbdac53bfde0b0eb69f9bfd
> 
> vCenter Server as a Zip file &#8211; English only version
     
> File type: zip
     
> MD5SUM: ee15ae73a66dd9dbc27fada476656aeb
     
> SHA1SUM: a5c25d114d42f1aae11d7c741587cf57caff72a3
> 
> VMware vCenter Converter BootCD for vCenter Server
     
> File type: .zip
     
> Version: 4.0.3
     
> MD5SUM: e49e0ff0f2563196cc5d4b5c471cd666
> 
> VMware vCenter Converter CLI for Linux platform
     
> File type: .tar.gz
     
> Version: 4.0.3
     
> MD5SUM: 30d1f5e58a6cad8dacd988908305bc1c
> 
> ESX 3.5
     
> &#8212;&#8212;-
> 
> ESX350-201203401-BG
     
> http://downloads.vmware.com/go/selfsupport-download
     
> md5sum: 07743c471ce46de825c36c2277ccd500
     
> sha1sum: cb77e6f820e1015311bf2386b240fd84f0ad04dd
     
> http://kb.vmware.com/kb/2009155
> 
> 5. References
> 
> Oracle Java SE Critical Patch Update Advisory of October 2011
> 
> http://www.oracle.com/technetwork/topics/security/javacpuoct2011-443431.htm
  
> l
> 
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
> 
> 6. Change log
> 
> 2012-03-08 VMSA-2012-0003
     
> Initial security advisory in conjunction with the release of
     
> VirtualCenter Update 6b and patches for ESX 3.5 and ESXi 3.5 on
     
> 2012-03-08.
> 
> 2012-09-12 VMSA-2012-0003.1
     
> Updated security advisory in conjunction with the release of
     
> vSphere 4.0 U4a on 2012-09-12 and ESX 4.0 patches on 2012-09-13.
> 
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
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
> 
> \___\___\___\___\___\___\___\___\___\___\___\___\___\___\_____
  
> Security-announce mailing list
  
> Security-announce@lists.vmware.com
  
> http://lists.vmware.com/mailman/listinfo/security-announce