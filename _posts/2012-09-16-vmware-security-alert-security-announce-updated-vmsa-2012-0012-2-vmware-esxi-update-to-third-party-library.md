---
id: 1720
title: 'VMware Security Alert &#8211; [Security-announce] UPDATED VMSA-2012-0012.2 VMware ESXi update to third party library'
date: 2012-09-16T21:16:17+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1720
permalink: /2012/09/16/vmware-security-alert-security-announce-updated-vmsa-2012-0012-2-vmware-esxi-update-to-third-party-library/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 879
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
> Advisory ID: VMSA-2012-0012.2
  
> Synopsis: VMware ESXi update to third party library
  
> Issue date: 2012-07-12
  
> Updated on: 2012-09-13
  
> CVE number: CVE-2010-4008, CVE-2011-0216, CVE-2011-1944,
                 
> CVE-2011-2834, CVE-2011-3905, CVE-2011-3919,
                 
> CVE-2012-0841
> 
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
  
> 1. Summary
> 
> VMware ESXi update addresses several security issues.
> 
> 2. Relevant releases
> 
> ESXi 5.0 without patch ESXi500-201207101-SG
     
> ESXi 4.1 without patch ESXi410-201208101-SG
     
> ESXi 4.0 without patch ESXi400-201209401-SG
> 
> 3. Problem Description
> 
> a. ESXi update to third party component libxml2
> 
> The libxml2 third party library has been updated which addresses
      
> multiple security issues.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
      
> has assigned the names CVE-2010-4008, CVE-2011-0216, CVE-2011-1944,
      
> CVE-2011-2834, CVE-2011-3905, CVE-2011-3919 and CVE-2012-0841 to
      
> these issues.
> 
> The following table lists what action remediates the vulnerability
      
> (column 4) if a solution is available.
> 
> VMware Product Running Replace with/
      
> Product Version on Apply Patch
      
> ========== ======== ======== =================
      
> vCenter any Windows not affected
> 
> hosted * any any not affected
> 
> ESXi 5.0 any ESXi500-201207101-SG
      
> ESXi 4.1 any ESXi410-201208101-SG
      
> ESXi 4.0 any ESXi400-201209401-SG
      
> ESXi 3.5 any patch pending
> 
> ESX any any not applicable
> 
> * hosted products are VMware Workstation, Player, ACE, Fusion.
> 
> Note: &#8220;patch pending&#8221; means that the product is affected, but no
           
> patch is currently available. The advisory will be updated
           
> when a patch is available.
> 
> 4. Solution
> 
> Please review the patch/release notes for your product and
     
> version and verify the checksum of your downloaded file.
> 
> ESXi
     
> &#8212;-
     
> http://downloads.vmware.com/go/selfsupport-download
> 
> ESXi 5.0
     
> &#8212;&#8212;&#8211;
     
> Patch: ESXi500-201207001
     
> md5sum: 01196c5c1635756ff177c262cb69a848
     
> sha1sum: 85936f5439100cd5fb55c7add574b5b3b937fe86
     
> http://kb.vmware.com/kb/2020571
     
> ESXi500-201207001 contains ESXi500-201207101-SG
> 
> ESXi 4.1
     
> &#8212;&#8212;&#8211;
     
> File: update-from-esxi4.1-4.1_update03.zip
     
> md5sum: b35267e3c96a8ebd2e3acac09538cdf5
     
> sha1sum: 2b2d456e89964528f25c01ae5d84edbd2bbcdefb
     
> http://kb.vmware.com/kb/2020373
     
> update-from-esxi4.1-4.1_update03 contains ESXi410-201208101-SG
> 
> ESXi 4.0
     
> &#8212;&#8212;&#8211;
     
> File: ESXi400-201209001
     
> md5sum: 8ea463e3814f147ab0889a733e66b9f0
     
> sha1sum: f9526a0936975fa4b7cbdf588cd4c119d95973c9
     
> http://kb.vmware.com/kb/2019662
     
> ESXi400-201209001 contains ESXi400-201209401-SG
> 
> 5. References
> 
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-4008
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-0216
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-1944
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-2834
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3905
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3919
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0841
> 
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
> 
> 6. Change log
> 
> 2012-07-12 VMSA-2012-0012
> 
> Initial security advisory in conjunction with the release of a patch
     
> for ESXi 5.0 on 2012-07-12.
> 
> 2012-08-30 VMSA-2012-0012.1
> 
> Updated Relevant Releases, Problem Description, and Solution
     
> sections to include information regarding updates for ESXi in
     
> conjunction with the release of vSphere 4.1 U3 on 2012-08-30.
> 
> 2012-09-12 VMSA-2012-0012.2
> 
> Updated security advisory in conjunction with the release of
     
> vSphere 4.0 U4a on 2012-09-12 and ESX 4.0 patches on 2012-09-13.
     
> Removed CVE-2010-4494 and CVE-2011-2821 since these CVEs are not
     
> relevant to ESXi.
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
  
> \___\___\___\___\___\___\___\___\___\___\___\___\___\___\_____
  
> Security-announce mailing list
  
> Security-announce@lists.vmware.com
  
> http://lists.vmware.com/mailman/listinfo/security-announce