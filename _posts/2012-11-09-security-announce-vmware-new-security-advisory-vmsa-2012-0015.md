---
id: 1840
title: '[Security-announce] VMware new security advisory VMSA-2012-0015'
date: 2012-11-09T14:55:11+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1840
permalink: /2012/11/09/security-announce-vmware-new-security-advisory-vmsa-2012-0015/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 850
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
In our effort to provide our viewers with up to the minute information on VMware related news and topics, we’re posting the following Security Alert direct from the VMware Security Alert distribution.

<!--more-->&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

VMware Security Advisory
  
Advisory ID: VMSA-2012-0015
  
Synopsis:    VMware Hosted Products and OVF Tool address security issues
  
Issue date:  2012-11-08
  
Updated on:  2012-11-08 (initial advisory) CVE number:  CVE-2012-5458, CVE-2012-5459 and CVE-2012-3569

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

1. Summary

  *  VMware Hosted products and OVFTool patches address several security issues.

2. Relevant releases

  *  OVF Tool 2.1
  * Workstation 8.0.4
  * Player 4.0.4

3. Problem Description

  1. VMware Workstation and Player Weak permissions on process threads vulnerability. Certain processes when created have weak security permissions assigned. It is possible to commandeer these process threads, which could result in Elevation of Privilege in the context of the host.VMware would like to thank Derek Soeder of Cylance, Inc. for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-5458 to this issue. 
    Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
    
    VMware         Product   Running   Replace with/Product        Version   on        Apply Patch
  
    =============  ========  =======   =================
  
    vCenter        any       Windows   not affected
  
    Workstation    9.x       any       not affected
  
    Workstation    8.x       Windows   8.0.5
  
    Workstation    8.x       Linux     not affected
  
    Player         5.x       any       not affected
  
    Player         4.x       Windows   4.0.5 or later
  
    Player         4.x       Linux     not affected
  
    Fusion         any       Mac       not affected
  
    ESXi           any       ESXi      not affected
  
    ESX            any       ESX       not affected</li> 
    
      * VMware Workstation and Player DLL binary planting vulnerability. Workstation and Player have a binary planting vulnerability. An attacker who can write their malicious executable to a system folder on the host, may be able to run code under certain circumstances.VMware would like to thank Derek Soeder of Cylance, Inc. for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-5459 to this issue. 
        Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
        
        VMware         Product   Running   Replace with/Product        Version   on        Apply Patch
  
        =============  ========  =======   =================
  
        vCenter        any       Windows   not affected
  
        Workstation    9.x       any       not affected
  
        Workstation    8.x       Windows   8.0.5
  
        Workstation    8.x       Linux     not affected
  
        Player         5.x       any       not affected
  
        Player         4.x       Windows   4.0.5 or later
  
        Player         4.x       Linux     not affected
  
        Fusion         any       Mac       not affected
  
        ESXi           any       ESXi      not affected
  
        ESX            any       ESX       not affected</li> 
        
          * VMware OVF Tool format string vulnerability.The OVFTool has a format string vulnerability. Exploitation of this issue may lead to code execution. In order to exploit the issue, the attacker would need to trick the user into loading their malicious OVF file.It is recommended that only OVF files from trusted sources should be used. 
            VMware would like to thank Jeremy Brown of Microsoft for reporting this issue to us.
            
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-3569 to this issue.
            
            Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
            
            VMware         Product   Running   Replace with/ Product        Version   on        Apply Patch
  
            =============  ========  =======   =================
  
            vCenter        any       Windows   not affected
  
            OVF Tool       3.x       any       not affected
  
            OVF Tool       2.1       Windows   OVF Tool 3.0.1
  
            OVF Tool       2.1       Linux/Mac not affected
  
            OVF Tool       2.0       any       not affected
  
            Workstation    9.x       any       not affected
  
            Workstation    8.x       Windows   8.0.5
  
            Workstation    8.x       Linux     not affected
  
            Player         5.x       any       not affected
  
            Player         4.x       Windows   4.0.5 or later
  
            Player         4.x       Linux     not affected
  
            Fusion         any       Mac       not affected
  
            ESXi           any       ESXi      not affected
  
            ESX            any       ESX       not affected
            
            Note: Workstation, Player and the vSphere Web Client (part of vCenter Server) use the OVF Tool to load OVF files. Other products, including vCenter Server (except vSPhere Web Client), ESX, and vCloud Director do not use the OVF Tool to parse OVF files.</li> 
            
              * SolutionPlease review the patch/release notes for your product and version and verify the checksum of your downloaded file.OVF Tool 3.0.1
  
                &#8212;&#8212;&#8212;&#8212;
  
                <https://www.vmware.com/support/developer/ovf/></p> 
                VMware Workstation 8.0.5
  
                &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
                <https://www.vmware.com/go/downloadworkstation>
                
                Release notes:
  
                [https://www.vmware.com/support/ws80/doc/releasenotes\_workstation\_805.html](https://www.vmware.com/support/ws80/doc/releasenotes_workstation_805.html)
  
                Player 4.0.5
  
                &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
                <http://www.vmware.com/go/downloadplayer>
                
                Release notes:
  
                <https://www.vmware.com/support/player40/doc/releasenotes_player405.html>
                
                &nbsp;</li> 
                
                  * References
  
                    [In our effort to provide our viewers with up to the minute information on VMware related news and topics, we’re posting the following Security Alert direct from the VMware Security Alert distribution.

<!--more-->&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

VMware Security Advisory
  
Advisory ID: VMSA-2012-0015
  
Synopsis:    VMware Hosted Products and OVF Tool address security issues
  
Issue date:  2012-11-08
  
Updated on:  2012-11-08 (initial advisory) CVE number:  CVE-2012-5458, CVE-2012-5459 and CVE-2012-3569

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

1. Summary

  *  VMware Hosted products and OVFTool patches address several security issues.

2. Relevant releases

  *  OVF Tool 2.1
  * Workstation 8.0.4
  * Player 4.0.4

3. Problem Description

  1. VMware Workstation and Player Weak permissions on process threads vulnerability. Certain processes when created have weak security permissions assigned. It is possible to commandeer these process threads, which could result in Elevation of Privilege in the context of the host.VMware would like to thank Derek Soeder of Cylance, Inc. for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-5458 to this issue. 
    Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
    
    VMware         Product   Running   Replace with/Product        Version   on        Apply Patch
  
    =============  ========  =======   =================
  
    vCenter        any       Windows   not affected
  
    Workstation    9.x       any       not affected
  
    Workstation    8.x       Windows   8.0.5
  
    Workstation    8.x       Linux     not affected
  
    Player         5.x       any       not affected
  
    Player         4.x       Windows   4.0.5 or later
  
    Player         4.x       Linux     not affected
  
    Fusion         any       Mac       not affected
  
    ESXi           any       ESXi      not affected
  
    ESX            any       ESX       not affected</li> 
    
      * VMware Workstation and Player DLL binary planting vulnerability. Workstation and Player have a binary planting vulnerability. An attacker who can write their malicious executable to a system folder on the host, may be able to run code under certain circumstances.VMware would like to thank Derek Soeder of Cylance, Inc. for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-5459 to this issue. 
        Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
        
        VMware         Product   Running   Replace with/Product        Version   on        Apply Patch
  
        =============  ========  =======   =================
  
        vCenter        any       Windows   not affected
  
        Workstation    9.x       any       not affected
  
        Workstation    8.x       Windows   8.0.5
  
        Workstation    8.x       Linux     not affected
  
        Player         5.x       any       not affected
  
        Player         4.x       Windows   4.0.5 or later
  
        Player         4.x       Linux     not affected
  
        Fusion         any       Mac       not affected
  
        ESXi           any       ESXi      not affected
  
        ESX            any       ESX       not affected</li> 
        
          * VMware OVF Tool format string vulnerability.The OVFTool has a format string vulnerability. Exploitation of this issue may lead to code execution. In order to exploit the issue, the attacker would need to trick the user into loading their malicious OVF file.It is recommended that only OVF files from trusted sources should be used. 
            VMware would like to thank Jeremy Brown of Microsoft for reporting this issue to us.
            
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-3569 to this issue.
            
            Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
            
            VMware         Product   Running   Replace with/ Product        Version   on        Apply Patch
  
            =============  ========  =======   =================
  
            vCenter        any       Windows   not affected
  
            OVF Tool       3.x       any       not affected
  
            OVF Tool       2.1       Windows   OVF Tool 3.0.1
  
            OVF Tool       2.1       Linux/Mac not affected
  
            OVF Tool       2.0       any       not affected
  
            Workstation    9.x       any       not affected
  
            Workstation    8.x       Windows   8.0.5
  
            Workstation    8.x       Linux     not affected
  
            Player         5.x       any       not affected
  
            Player         4.x       Windows   4.0.5 or later
  
            Player         4.x       Linux     not affected
  
            Fusion         any       Mac       not affected
  
            ESXi           any       ESXi      not affected
  
            ESX            any       ESX       not affected
            
            Note: Workstation, Player and the vSphere Web Client (part of vCenter Server) use the OVF Tool to load OVF files. Other products, including vCenter Server (except vSPhere Web Client), ESX, and vCloud Director do not use the OVF Tool to parse OVF files.</li> 
            
              * SolutionPlease review the patch/release notes for your product and version and verify the checksum of your downloaded file.OVF Tool 3.0.1
  
                &#8212;&#8212;&#8212;&#8212;
  
                <https://www.vmware.com/support/developer/ovf/></p> 
                VMware Workstation 8.0.5
  
                &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
                <https://www.vmware.com/go/downloadworkstation>
                
                Release notes:
  
                [https://www.vmware.com/support/ws80/doc/releasenotes\_workstation\_805.html](https://www.vmware.com/support/ws80/doc/releasenotes_workstation_805.html)
  
                Player 4.0.5
  
                &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
                <http://www.vmware.com/go/downloadplayer>
                
                Release notes:
  
                <https://www.vmware.com/support/player40/doc/releasenotes_player405.html>
                
                &nbsp;</li> 
                
                  * References
  
](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5458) [In our effort to provide our viewers with up to the minute information on VMware related news and topics, we’re posting the following Security Alert direct from the VMware Security Alert distribution.

<!--more-->&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

VMware Security Advisory
  
Advisory ID: VMSA-2012-0015
  
Synopsis:    VMware Hosted Products and OVF Tool address security issues
  
Issue date:  2012-11-08
  
Updated on:  2012-11-08 (initial advisory) CVE number:  CVE-2012-5458, CVE-2012-5459 and CVE-2012-3569

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

1. Summary

  *  VMware Hosted products and OVFTool patches address several security issues.

2. Relevant releases

  *  OVF Tool 2.1
  * Workstation 8.0.4
  * Player 4.0.4

3. Problem Description

  1. VMware Workstation and Player Weak permissions on process threads vulnerability. Certain processes when created have weak security permissions assigned. It is possible to commandeer these process threads, which could result in Elevation of Privilege in the context of the host.VMware would like to thank Derek Soeder of Cylance, Inc. for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-5458 to this issue. 
    Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
    
    VMware         Product   Running   Replace with/Product        Version   on        Apply Patch
  
    =============  ========  =======   =================
  
    vCenter        any       Windows   not affected
  
    Workstation    9.x       any       not affected
  
    Workstation    8.x       Windows   8.0.5
  
    Workstation    8.x       Linux     not affected
  
    Player         5.x       any       not affected
  
    Player         4.x       Windows   4.0.5 or later
  
    Player         4.x       Linux     not affected
  
    Fusion         any       Mac       not affected
  
    ESXi           any       ESXi      not affected
  
    ESX            any       ESX       not affected</li> 
    
      * VMware Workstation and Player DLL binary planting vulnerability. Workstation and Player have a binary planting vulnerability. An attacker who can write their malicious executable to a system folder on the host, may be able to run code under certain circumstances.VMware would like to thank Derek Soeder of Cylance, Inc. for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-5459 to this issue. 
        Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
        
        VMware         Product   Running   Replace with/Product        Version   on        Apply Patch
  
        =============  ========  =======   =================
  
        vCenter        any       Windows   not affected
  
        Workstation    9.x       any       not affected
  
        Workstation    8.x       Windows   8.0.5
  
        Workstation    8.x       Linux     not affected
  
        Player         5.x       any       not affected
  
        Player         4.x       Windows   4.0.5 or later
  
        Player         4.x       Linux     not affected
  
        Fusion         any       Mac       not affected
  
        ESXi           any       ESXi      not affected
  
        ESX            any       ESX       not affected</li> 
        
          * VMware OVF Tool format string vulnerability.The OVFTool has a format string vulnerability. Exploitation of this issue may lead to code execution. In order to exploit the issue, the attacker would need to trick the user into loading their malicious OVF file.It is recommended that only OVF files from trusted sources should be used. 
            VMware would like to thank Jeremy Brown of Microsoft for reporting this issue to us.
            
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-3569 to this issue.
            
            Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
            
            VMware         Product   Running   Replace with/ Product        Version   on        Apply Patch
  
            =============  ========  =======   =================
  
            vCenter        any       Windows   not affected
  
            OVF Tool       3.x       any       not affected
  
            OVF Tool       2.1       Windows   OVF Tool 3.0.1
  
            OVF Tool       2.1       Linux/Mac not affected
  
            OVF Tool       2.0       any       not affected
  
            Workstation    9.x       any       not affected
  
            Workstation    8.x       Windows   8.0.5
  
            Workstation    8.x       Linux     not affected
  
            Player         5.x       any       not affected
  
            Player         4.x       Windows   4.0.5 or later
  
            Player         4.x       Linux     not affected
  
            Fusion         any       Mac       not affected
  
            ESXi           any       ESXi      not affected
  
            ESX            any       ESX       not affected
            
            Note: Workstation, Player and the vSphere Web Client (part of vCenter Server) use the OVF Tool to load OVF files. Other products, including vCenter Server (except vSPhere Web Client), ESX, and vCloud Director do not use the OVF Tool to parse OVF files.</li> 
            
              * SolutionPlease review the patch/release notes for your product and version and verify the checksum of your downloaded file.OVF Tool 3.0.1
  
                &#8212;&#8212;&#8212;&#8212;
  
                <https://www.vmware.com/support/developer/ovf/></p> 
                VMware Workstation 8.0.5
  
                &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
                <https://www.vmware.com/go/downloadworkstation>
                
                Release notes:
  
                [https://www.vmware.com/support/ws80/doc/releasenotes\_workstation\_805.html](https://www.vmware.com/support/ws80/doc/releasenotes_workstation_805.html)
  
                Player 4.0.5
  
                &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
                <http://www.vmware.com/go/downloadplayer>
                
                Release notes:
  
                <https://www.vmware.com/support/player40/doc/releasenotes_player405.html>
                
                &nbsp;</li> 
                
                  * References
  
                    [In our effort to provide our viewers with up to the minute information on VMware related news and topics, we’re posting the following Security Alert direct from the VMware Security Alert distribution.

<!--more-->&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

VMware Security Advisory
  
Advisory ID: VMSA-2012-0015
  
Synopsis:    VMware Hosted Products and OVF Tool address security issues
  
Issue date:  2012-11-08
  
Updated on:  2012-11-08 (initial advisory) CVE number:  CVE-2012-5458, CVE-2012-5459 and CVE-2012-3569

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

1. Summary

  *  VMware Hosted products and OVFTool patches address several security issues.

2. Relevant releases

  *  OVF Tool 2.1
  * Workstation 8.0.4
  * Player 4.0.4

3. Problem Description

  1. VMware Workstation and Player Weak permissions on process threads vulnerability. Certain processes when created have weak security permissions assigned. It is possible to commandeer these process threads, which could result in Elevation of Privilege in the context of the host.VMware would like to thank Derek Soeder of Cylance, Inc. for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-5458 to this issue. 
    Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
    
    VMware         Product   Running   Replace with/Product        Version   on        Apply Patch
  
    =============  ========  =======   =================
  
    vCenter        any       Windows   not affected
  
    Workstation    9.x       any       not affected
  
    Workstation    8.x       Windows   8.0.5
  
    Workstation    8.x       Linux     not affected
  
    Player         5.x       any       not affected
  
    Player         4.x       Windows   4.0.5 or later
  
    Player         4.x       Linux     not affected
  
    Fusion         any       Mac       not affected
  
    ESXi           any       ESXi      not affected
  
    ESX            any       ESX       not affected</li> 
    
      * VMware Workstation and Player DLL binary planting vulnerability. Workstation and Player have a binary planting vulnerability. An attacker who can write their malicious executable to a system folder on the host, may be able to run code under certain circumstances.VMware would like to thank Derek Soeder of Cylance, Inc. for reporting this issue to us.The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-5459 to this issue. 
        Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
        
        VMware         Product   Running   Replace with/Product        Version   on        Apply Patch
  
        =============  ========  =======   =================
  
        vCenter        any       Windows   not affected
  
        Workstation    9.x       any       not affected
  
        Workstation    8.x       Windows   8.0.5
  
        Workstation    8.x       Linux     not affected
  
        Player         5.x       any       not affected
  
        Player         4.x       Windows   4.0.5 or later
  
        Player         4.x       Linux     not affected
  
        Fusion         any       Mac       not affected
  
        ESXi           any       ESXi      not affected
  
        ESX            any       ESX       not affected</li> 
        
          * VMware OVF Tool format string vulnerability.The OVFTool has a format string vulnerability. Exploitation of this issue may lead to code execution. In order to exploit the issue, the attacker would need to trick the user into loading their malicious OVF file.It is recommended that only OVF files from trusted sources should be used. 
            VMware would like to thank Jeremy Brown of Microsoft for reporting this issue to us.
            
            The Common Vulnerabilities and Exposures project (cve.mitre.org) has assigned the name CVE-2012-3569 to this issue.
            
            Column 4 of the following table lists the action required to remediate the vulnerability in each release, if a solution is available.
            
            VMware         Product   Running   Replace with/ Product        Version   on        Apply Patch
  
            =============  ========  =======   =================
  
            vCenter        any       Windows   not affected
  
            OVF Tool       3.x       any       not affected
  
            OVF Tool       2.1       Windows   OVF Tool 3.0.1
  
            OVF Tool       2.1       Linux/Mac not affected
  
            OVF Tool       2.0       any       not affected
  
            Workstation    9.x       any       not affected
  
            Workstation    8.x       Windows   8.0.5
  
            Workstation    8.x       Linux     not affected
  
            Player         5.x       any       not affected
  
            Player         4.x       Windows   4.0.5 or later
  
            Player         4.x       Linux     not affected
  
            Fusion         any       Mac       not affected
  
            ESXi           any       ESXi      not affected
  
            ESX            any       ESX       not affected
            
            Note: Workstation, Player and the vSphere Web Client (part of vCenter Server) use the OVF Tool to load OVF files. Other products, including vCenter Server (except vSPhere Web Client), ESX, and vCloud Director do not use the OVF Tool to parse OVF files.</li> 
            
              * SolutionPlease review the patch/release notes for your product and version and verify the checksum of your downloaded file.OVF Tool 3.0.1
  
                &#8212;&#8212;&#8212;&#8212;
  
                <https://www.vmware.com/support/developer/ovf/></p> 
                VMware Workstation 8.0.5
  
                &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
                <https://www.vmware.com/go/downloadworkstation>
                
                Release notes:
  
                [https://www.vmware.com/support/ws80/doc/releasenotes\_workstation\_805.html](https://www.vmware.com/support/ws80/doc/releasenotes_workstation_805.html)
  
                Player 4.0.5
  
                &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;
  
                <http://www.vmware.com/go/downloadplayer>
                
                Release notes:
  
                <https://www.vmware.com/support/player40/doc/releasenotes_player405.html>
                
                &nbsp;</li> 
                
                  * References
  
](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5458)](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5459) <http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3569>
                  * Change log
  
                    2012-11-08 VMSA-2012-0015
  
                    Initial security advisory in conjunction with the release of Workstation 8.0.5 and Player 4.0.5 on 2012-11-06.&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-
                  * Contact
  
                    E-mail list for product security notifications and announcements:
  
                    <http://lists.vmware.com/cgi-bin/mailman/listinfo/security-announce>This Security Advisory is posted to the following lists:
  
                    * security-announce at lists.vmware.com
  
                    * bugtraq at securityfocus.com
  
                    * full-disclosure at lists.grok.org.ukE-mail:  security at vmware.com
  
                    PGP key at: <http://kb.vmware.com/kb/1055></p> 
                    VMware Security Advisories
  
                    <http://www.vmware.com/security/advisories>
                    
                    VMware security response policy
  
                    <http://www.vmware.com/support/policies/security_response.html>
                    
                    General support life cycle policy
  
                    <http://www.vmware.com/support/policies/eos.html>
                    
                    VMware Infrastructure support life cycle policy
  
                    <http://www.vmware.com/support/policies/eos_vi.html></li> </ol> 
                    
                    Copyright 2012 VMware Inc.  All rights reserved.