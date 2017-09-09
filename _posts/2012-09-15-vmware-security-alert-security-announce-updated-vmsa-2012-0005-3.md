---
id: 1715
title: 'VMware Security Alert &#8211; [Security-announce] UPDATED VMSA-2012-0005.3 VMware vCenter Server, Orchestrator, Update Manager, vShield, vSphere Client, Workstation, Player, ESXi, and ESX address several security issues'
date: 2012-09-15T16:10:22+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1715
permalink: /2012/09/15/vmware-security-alert-security-announce-updated-vmsa-2012-0005-3-vmware-vcenter-server-orchestrator-update-manager-vshield-vsphere-client-workstation-player-esxi-and-esx-address-several-se-2/
redirect_from: /wp/2012/09/15/vmware-security-alert-security-announce-updated-vmsa-2012-0005-3-vmware-vcenter-server-orchestrator-update-manager-vshield-vsphere-client-workstation-player-esxi-and-esx-address-several-se-2/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1347"
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



> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
                    
> VMware Security Advisory
> 
> Advisory ID: VMSA-2012-0005.3
  
> Synopsis: VMware vCenter Server, Orchestrator, Update Manager,
                
> vShield, vSphere Client, Workstation, Player, ESXi, and
                
> ESX address several security issues
  
> Issue date: 2012-03-15
  
> Updated on: 2012-09-13
  
> CVE numbers: CVE-2012-1508, CVE-2012-1509, CVE-2012-1510,
                
> CVE-2012-1512, CVE-2012-1513, CVE-2012-1514,
                
> CVE-2011-3190, CVE-2011-3375, CVE-2012-0022,
                
> CVE-2010-0405
                
> &#8212; JRE &#8212;
                
> See references
   
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
  
> 1. Summary
> 
> VMware vCenter Server, Orchestrator, Update Manager, vShield, vSphere
     
> Client, Workstation, Player, ESXi, and ESX address several security
     
> issues
> 
> 2. Relevant releases
> 
> Workstation 7.1.4
> 
> Player 3.1.4
> 
> VMware vCenter Server 5.0
     
> VMware vCenter Server 4.1 Update 2 and earlier
     
> VMware vCenter Server 4.0 Update 3 and earlier
> 
> VMware vSphere Client 5.0
     
> VMware vSphere Client 4.1 Update 1 and earlier
> 
> VMware vCenter Orchestrator 4.2
     
> VMware vCenter Orchestrator 4.1 Update 1 and earlier
     
> VMware vCenter Orchestrator 4.0 Update 3 and earlier
> 
> VMware vShield Manager 4.1 Update 1
     
> VMware vShield Manager 1.0 Update 1
> 
> VMware Update Manager 5.0
> 
> ESXi 5.0 without patches ESXi500-201203101-SG, ESXi500-201112402-BG
     
> ESXi 4.1 without patch ESXi410-201110202-UG
     
> ESXi 4.0 without patch ESXi400-201110402-BG
> 
> ESX 4.1 without patch ESX410-201110201-SG, ESX410-201208101-SG
     
> ESX 4.0 without patch ESX400-201110401-SG
> 
> 3. Problem Description
> 
> a. VMware Tools Display Driver Privilege Escalation
> 
> The VMware XPDM and WDDM display drivers contain buffer overflow
      
> vulnerabilities and the XPDM display driver does not properly
      
> check for NULL pointers. Exploitation of these issues may lead
      
> to local privilege escalation on Windows-based Guest Operating
      
> Systems.
> 
> VMware would like to thank Tarjei Mandt for reporting theses
      
> issues to us.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
      
> has assigned the names CVE-2012-1509 (XPDM buffer overrun),
      
> CVE-2012-1510 (WDDM buffer overrun) and CVE-2012-1508 (XPDM null
      
> pointer dereference) to these issues.
> 
> Note: CVE-2012-1509 doesn&#8217;t affect ESXi and ESX.
> 
> Column 4 of the following table lists the action required to
      
> remediate the vulnerability in each release, if a solution is
      
> available.
> 
> VMware Product Running Replace with/
      
> Product \* Version on Apply Patch \**
      
> ============= ======== ======= =================
      
> vCenter any Windows not affected
> 
> Workstation 8.x any not affected
      
> Workstation 7.x any 7.1.5 or later
> 
> Player 4.x any not affected
      
> Player 3.x any 3.1.5 or later
> 
> Fusion 4.x Mac OS/X not affected
> 
> ESXi 5.0 ESXi ESXi500-201112402-BG
      
> ESXi 4.1 ESXi ESXi410-201110202-UG
      
> ESXi 4.0 ESXi ESXi400-201110402-BG
      
> ESXi 3.5 ESXi not affected
> 
> ESX 4.1 ESX ESX410-201110201-SG
      
> ESX 4.0 ESX ESX400-201110401-SG
      
> ESX 3.5 ESX not affected
> 
> * Remediation for VMware View is described in VMSA-2012-0004.
> 
> ** Notes on updating VMware Guest Tools:
> 
> After the update or patch is applied, VMware Guest Tools must
        
> be updated in any pre-existing Windows-based Guest Operating
        
> System. The XPDM and WDDM drivers are part of Tools.
> 
> Windows-Based Virtual Machines that have moved to Workstation
        
> 8 or Player 4 from a lower version of Workstation or Player
        
> are affected unless:
> 
> &#8211; They were moved from Workstation 7.1.5 or Player 3.1.5,
> 
> AND
> 
> &#8211; The Tools version was updated before the move.
> 
> Windows-Based Virtual Machines that have moved to Fusion 4
        
> from a lower version of Fusion are affected.
> 
> b. vSphere Client internal browser input validation vulnerability
> 
> The vSphere Client has an internal browser that renders html
      
> pages from log file entries. This browser doesn&#8217;t properly
      
> sanitize input and may run script that is introduced into the
      
> log files. In order for the script to run, the user would need
      
> to open an individual, malicious log file entry. The script
      
> would run with the permissions of the user that runs the vSphere
      
> Client.
> 
> VMware would like to thank Edward Torkington for reporting this
      
> issue to us.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
      
> has assigned the name CVE-2012-1512 to this issue.
> 
> In order to remediate the issue, the vSphere Client of the
      
> vSphere 5.0 Update 1 release or the vSphere 4.1 Update 2 release
      
> needs to be installed. The vSphere Clients that come with
      
> vSphere 4.0 and vCenter Server 2.5 are not affected.
> 
> c. vCenter Orchestrator Password Disclosure
> 
> The vCenter Orchestrator (vCO) Web Configuration tool reflects
      
> back the vCenter Server password as part of the webpage. This
      
> might allow the logged-in vCO administrator to retrieve the
      
> vCenter Server password.
> 
> VMware would like to thank Alexey Sintsov from Digital Security
      
> Research Group for reporting this issue to us.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
      
> has assigned the name CVE-2012-1513 to this issue.
> 
> VMware Product Running Replace with/
      
> Product Version on Apply Patch
      
> ============= ======= ======= =================
      
> vCO 4.2 Windows vCO 4.2 Update 1
      
> vCO 4.1 Windows vCO 4.1 Update 2
      
> vCO 4.0 Windows vCO 4.0 Update 4
> 
> d. vShield Manager Cross-Site Request Forgery vulnerability
> 
> The vShield Manager (vSM) interface has a Cross-Site Request
      
> Forgery vulnerability. If an attacker can convince an
      
> authenticated user to visit a malicious link, the attacker may
      
> force the victim to forward an authenticated request to the
      
> server.
> 
> VMware would like to thank Frans Pehrson of Xxor AB
      
> (www.xxor.se) and Claudio Criscione for independently reporting
      
> this issue to us
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
      
> has assigned the name CVE-2012-1514 to this issue.
> 
> VMware Product Running Replace with/
      
> Product Version on Apply Patch
      
> ============= ======= ======= =================
      
> vSM 5.0 Linux not affected
      
> vSM 4.1 Linux vSM 4.1.0 Update 2
      
> vSM 4.0 Linux vSM 1.0.1 Update 2
> 
> e. vCenter Update Manager, Oracle (Sun) JRE update 1.6.0_30
> 
> Oracle (Sun) JRE is updated to version 1.6.0_30, which addresses
      
> multiple security issues that existed in earlier releases of
      
> Oracle (Sun) JRE.
> 
> Oracle has documented the CVE identifiers that are addressed in
      
> JRE 1.6.0\_29 and JRE 1.6.0\_30 in the Oracle Java SE Critical
      
> Patch Update Advisory of October 2011. The References section
      
> provides a link to this advisory.
> 
> Column 4 of the following table lists the action required to
      
> remediate the vulnerability in each release, if a solution is
      
> available.
> 
> VMware Product Running Replace with/
      
> Product Version on Apply Patch
      
> ============= ======= ======= =================
      
> vCenter 5.0 Windows patch pending
      
> vCenter 4.1 Windows See VMSA-2012-0013
      
> vCenter 4.0 Windows not applicable **
      
> VirtualCenter 2.5 Windows not applicable **
> 
> Update Manager 5.0 Windows Update Manager 5.0 Update 1
      
> Update Manager 4.1 Windows not applicable **
      
> Update Manager 4.0 Windows not applicable **
> 
> hosted * any any not affected
> 
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX See VMSA-2012-0013
      
> ESX 4.0 ESX not applicable **
      
> ESX 3.5 ESX not applicable **
> 
> * hosted products are VMware Workstation, Player, ACE, Fusion.
> 
> ** this product uses the Oracle (Sun) JRE 1.5.0 family
> 
> f. vCenter Server Apache Tomcat update 6.0.35
> 
> Apache Tomcat has been updated to version 6.0.35 to address
      
> multiple security issues.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
      
> has assigned the names CVE-2011-3190, CVE-2011-3375,
      
> CVE-2011-4858, and CVE-2012-0022 to these issues.
> 
> VMware Product Running Replace with/
      
> Product Version on Apply Patch
      
> ============= ======= ======= =================
      
> vCenter 5.0 Windows vCenter 5.0 Update 1
      
> vCenter 4.1 Windows vCenter 4.1 Update 3
      
> vCenter 4.0 Windows vCenter 4.0 Update 4a
      
> VirtualCenter 2.5 Windows not applicable **
> 
> hosted * any any not affected
> 
> ESXi any ESXi not applicable
> 
> ESX 4.1 ESX ESX410-201208101-SG
      
> ESX 4.0 ESX ESX400-201209401-SG
      
> ESX 3.5 ESX not applicable **
> 
> * hosted products are VMware Workstation, Player, ACE, Fusion.
> 
> ** this product uses the Apache Tomcat 5.5 family
> 
> g. ESXi update to third party component bzip2
> 
> The bzip2 library is updated to version 1.0.6, which resolves a
      
> security issue.
> 
> The Common Vulnerabilities and Exposures project (cve.mitre.org)
      
> has assigned the name CVE-2010-0405 to this issue.
> 
> VMware Product Running Replace with/
      
> Product Version on Apply Patch
      
> ============= ======= ======= =================
      
> vCenter any Windows not affected
> 
> hosted * any any not affected
> 
> ESXi 5.0 ESXi ESXi500-201203101-SG
      
> ESXi 4.1 ESXi not affected
      
> ESXi 4.0 ESXi not affected
      
> ESXi 3.5 ESXi not affected
> 
> ESX any ESX not applicable
> 
> * hosted products are VMware Workstation, Player, ACE, Fusion.
> 
> 4. Solution
> 
> Please review the patch/release notes for your product and version
     
> and verify the checksum of your downloaded file.
> 
> VMware Workstation 7.1.5
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
     
> http://www.vmware.com/go/downloadworkstation
> 
> Release notes:
     
> https://www.vmware.com/support/ws71/doc/releasenotes_ws715.html
> 
> VMware Workstation for Windows 32-bit and 64-bit with VMware Tools
     
> md5sum: 40a0a39377a6ba804d5e76e59449d51f
     
> sha1sum: 25462e18bf9439876c63948415f7ba7b09baa8e6
> 
> VMware Workstation for Linux 32-bit with VMware Tools
     
> md5sum: 9c9b4d7a749f1baa485f26e6f366c070
     
> sha1sum: 31033424656b8eaaa814f3e9c3b5b9c5c53b783b
> 
> VMware Workstation for Linux 64-bit with VMware Tools
     
> md5sum: 482b8b2890f75488addfc31418031864
     
> sha1sum: b1f73650f70c94249e5add5d9516d0e45c4ae87d
> 
> VMware Player 3.1.5
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
     
> http://www.vmware.com/go/downloadplayer
> 
> Release notes:
     
> https://www.vmware.com/support/player31/doc/releasenotes_player315.html
> 
> VMware Player for 32-bit and 64-bit Windows
     
> md5sum: fcc91227963e58efcb63fb791d2fd813
     
> sha1sum: d39d9da694c22530a7fa701e3ded6cccdc3ea390
> 
> VMware Player for 32-bit Linux
     
> md5sum: c96867c8093d23065bed7e71e020bb19
     
> sha1sum: 4156bdfb7f679114671b416d178028fdc4d3beb4
> 
> VMware Player for 64-bit Linux
     
> md5sum: 1ec954f1baaf6a60e451979b5e88f2d6
     
> sha1sum: a253a486d6c6848620de200ef1837ced903daa1c
> 
> vCenter Server 5.0 Update 1
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
> 
> The download for vCenter Server includes vSphere Update Manager,
     
> vSphere Client, and vCenter Orchestrator
> 
> Download link:
> 
> http://downloads.vmware.com/d/info/datacenter\_cloud\_infrastructure/vmware_v
  
> sphere/5_0
> 
> Release Notes:
     
> vSphere vCenter Server
> 
> https://www.vmware.com/support/pubs/vsphere-esxi-vcenter-server-pubs.html
     
> https://www.vmware.com/support/pubs/vum_pubs.html
> 
> File: VMware-VIMSetup-all-5.0.0-639890.iso
     
> md5sum:f860ac4b618e2562ebffa2318446fa5b
     
> sha1sum:62830e3061b983e98944ae6d9d3b2e820cebe270
> 
> File: VMware-VIMSetup-all-5.0.0-639890.zip
     
> md5sum:a8bdde277aeeffc382ec210acf510479
     
> sha1sum:0b675a47349fdc09104c62ad84bd302846213fc8
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
> vCenter Server 4.0 Update 4
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
> 
> The download for vCenter Server includes vCenter Orchestrator.
> 
> Download link:
> 
> http://downloads.vmware.com/d/info/datacenter\_cloud\_infrastructure/vmware_v
  
> sphere/4_0
> 
> Release Notes:
> 
> http://downloads.vmware.com/support/pubs/vs\_pages/vsp\_pubs\_esx40\_vc40.html
> 
> File: VMware-VIMSetup-all-4.0.0-502539.iso
     
> md5sum: b418ff3d394f91b418271b6b93dfd6bd
     
> sha1sum: 56c2ec60f8b8a734a8312d9e38d5d70cd20c0927
> 
> File: VMware-VIMSetup-all-4.0.0-502539.zip
     
> md5sum: 2acfadde1ec0cd6d37063d87246d6942
     
> sha1sum: ea1f3a3cb178f23fc2cf49bfc1450d10e5f699f8
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
> vShield Manager 4.1.0 Update 2
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
> 
> The download for VMware vShield App contains vShield Manager
> 
> Download link:
     
> http://www.vmware.com/download/download.do?downloadGroup=VSHIELD_APP10U2
> 
> Release Notes:
> 
> https://www.vmware.com/support/vshield/doc/releasenotes\_vshield\_410U2.html
> 
> File: VMware-vShield-Manager-upgrade-bundle-4.1.0U2-576124.tar.gz
     
> md5sum:9a80fc347bc4a19ad0fd4c9fcb4ab475
     
> sha1sum:f5780c1615da0493d0955a1343876c4111d85203
> 
> vShield Zones 1.0 Update 2
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
     
> The download for VMware vShield Zones contains vShield Manager
> 
> Download link:
     
> http://www.vmware.com/download/download.do?downloadGroup=ZONES10U2
> 
> Release Notes
     
> https://www.vmware.com/support/vsz/doc/releasenotes\_vsz\_10U2.html
> 
> File: VMware-vShieldZones-1.0U2-638154.exe
     
> md5sum:73515f4732c3a1ecc91ef21a504ca6d9
     
> sha1sum:ed4d858e1c05f54679ba99b739270c054efaf63e
> 
> ESXi and ESX
     
> &#8212;&#8212;&#8212;&#8212;
> 
> Download link:
     
> http://downloads.vmware.com/go/selfsupport-download
> 
> ESXi 5.0
     
> &#8212;&#8212;&#8211;
     
> File: update-from-esxi5.0-5.0_update01
     
> md5sum: 55c25bd990e2881462bc5b66fb5f6c39
     
> sha1sum: ecd871bb09b649c6c8c13de82d579d4b7dcadc88
     
> http://kb.vmware.com/kb/2011432
     
> update-from-esxi5.0-5.0_update01 contains ESXi500-201203101-SG
> 
> File: ESXi500-201112001
     
> md5sum: 107ec1cf6ee1d5d5cb8ea5c05b05cc10
     
> sha1sum: aff63c8a170508c8c0f21a60d1ea75ef1922096d
     
> http://kb.vmware.com/kb/2007672
     
> ESXi500-201112001 contains ESXi500-201112402-BG
> 
> Note: subsequent ESXi releases are cumulative and
     
> ESXi500-201203101-SG includes the security fixes that are
     
> present in ESXi500-201112402-BG
> 
> ESXi 4.1
     
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
     
> update-from-esxi4.1-4.1_update02
     
> md5sum: 57e34b500ce543d778f230da1d44e412
     
> sha1sum: 52f4378e2f1a29c908493182ccbde91d58b4112f
     
> http://kb.vmware.com/kb/2002341
     
> update-from-esxi4.1-4.1_update02 contains ESXi410-201110202-UG
> 
> ESXi 4.0
     
> &#8212;&#8212;&#8211;
     
> File: ESXi400-201110001
     
> md5sum: fd47b5e2b7ea1db79a2e0793d4c9d9d3
     
> sha1sum: 759d4fa6da6eb49f41def68e3bd66e80c9a7032b
     
> http://kb.vmware.com/kb/1039199
     
> ESXi400-201110001 contains ESXi400-201110402-BG
> 
> ESX 4.1
     
> &#8212;&#8212;-
     
> File: update-from-esx4.1-4.1_update3.zip
     
> md5sum: a4a45aba880d64210badade8d7c81904
     
> sha1sum: 4ed1ef2b56fa30deec999916367ab278dc5b1840
     
> http://kb.vmware.com/kb/2020362
     
> update-from-esx4.1-4.1_update03 contains ESX410-201208101-SG
> 
> update-from-esx4.1-4.1_update02
     
> md5sum: 96189a6de3797e28b153f89e01d5a15b
     
> sha1sum: b1823d39d0e4536a421fb933f02380bae7ee7a5d
     
> http://kb.vmware.com/kb/2002303
     
> update-from-esx4.1-4.1_update02 contains ESX410-201110201-SG
> 
> ESX 4.0
     
> &#8212;&#8212;-
     
> File: ESX400-201209001
     
> md5sum: 7faa79ea8d458e994db308933424a0ee
     
> sha1sum: 8f798a233cc28b203c3c8e0d44a1287af6c1ceb8
     
> http://kb.vmware.com/kb/2019661
     
> ESX400-201209001 contains ESX400-201209401-SG
> 
> File: ESX400-201110001
     
> md5sum: 0ce9cc285ea5c27142c9fdf273443d78
     
> sha1sum: fdb5482b2bf1e9c97f2814255676e3de74512399
     
> http://kb.vmware.com/kb/1036392
     
> ESX400-201110001 contains ESX400-201110401-SG
> 
> 5. References
> 
> Oracle Java SE Critical Patch Update Advisory of October 2011
> 
> http://www.oracle.com/technetwork/topics/security/javacpuoct2011-443431.htm
  
> l
> 
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1508
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1509
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1510
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1512
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1513
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1514
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3190
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3375
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0022
     
> http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-0405
> 
> &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;
> 
> 6. Change log
> 
> 2012-03-15 VMSA-2012-0005
> 
> Initial security advisory in conjunction with the release of
     
> vSphere 5.0 Update 1, Orchestrator 4.2 Update 1, Update Manager 5.0
     
> Update 1, vShield 1.0 Update 2, and ESXi and ESX 5.0 patches on
     
> 2012-03-15.
> 
> 2012-06-13 VMSA-2012-0005.1
> 
> Updated Relevant Releases, Problem Description, and Solution
     
> sections to include information regarding updates for Workstation 7
     
> in conjunction with the release of Workstation 7.1.6 on 2012-06-13.
> 
> 2012-08-30 VMSA-2012-0005.2
> 
> Updated Relevant Releases, Problem Description, and Solution
     
> sections to include information regarding updates for ESX, ESXi,
     
> and vCenter Server in conjunction with the release of vSphere 4.1 U3
     
> on 2012-08-30.
> 
> 2012-09-12 VMSA-2012-0005.3
> 
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
  
> \___\___\___\___\___\___\___\___\___\___\___\___\___\___\_____
  
> Security-announce mailing list
  
> Security-announce@lists.vmware.com
  
> http://lists.vmware.com/mailman/listinfo/security-announce