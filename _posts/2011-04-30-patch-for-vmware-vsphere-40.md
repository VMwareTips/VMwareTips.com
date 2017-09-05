---
id: 1327
title: Patch for vmware vSphere 4.0
date: 2011-04-30T09:40:09+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1327
permalink: /2011/04/30/patch-for-vmware-vsphere-40/
redirect_from: /wp/2011/04/30/patch-for-vmware-vsphere-40/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "1866"
dsq_thread_id:
  - "5156593614"
categories:
  - vSphere
tags:
  - esx
  - esxi
  - patch
  - update
  - vsphere
---
**vm**ware has recently released a patch for their vSphere 4.0 product line, which affects both ESX and ESXi.

Details from **vm**ware;

> **<span style="font-family: 'Arial','sans-serif'; color: #666666; font-size: 9pt;">We are pleased to inform you that a new VMware ESX 4.0 Patch is available as of April 28, 2011. </span>**<span style="font-family: 'Arial','sans-serif'; color: #666666; font-size: 9pt;"></p> 
> 
> <p>
>   Improvements included in this patch:</span>
> </p>
> 
> <ul type="disc">
>   <li class="MsoNormal" style="MARGIN: 0in 0in 0pt; COLOR: #666666; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in">
>     <span style="font-family: 'Arial','sans-serif'; font-size: 9pt; mso-fareast-font-family: 'Times New Roman';">An update for the Certificate Revocation List (CRL) to revoke an RSA key that HP uses for code signing certain software components</span>
>   </li>
>   <li class="MsoNormal" style="MARGIN: 0in 0in 0pt; COLOR: #666666; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in">
>     <span style="font-family: 'Arial','sans-serif'; font-size: 9pt; mso-fareast-font-family: 'Times New Roman';">Remediation of a denial of service possibility. By sending malicious network traffic an attacker could exhaust the available sockets which would prevent further connections to the host</span>
>   </li>
>   <li class="MsoNormal" style="MARGIN: 0in 0in 0pt; COLOR: #666666; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in">
>     <span style="font-family: 'Arial','sans-serif'; font-size: 9pt; mso-fareast-font-family: 'Times New Roman';">Refinements in handling of shared folders</span>
>   </li>
> </ul>
> 
> <p>
>   <span style="font-family: 'Arial','sans-serif'; color: #666666; font-size: 9pt;">Detailed information regarding resolved and known issues and enhancements can be found at ESX 4.0 Patch Release Notes</span>
> </p>
> 
> <ul type="disc">
>   <li class="MsoNormal" style="MARGIN: 0in 0in 0pt; COLOR: #666666; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l1 level1 lfo2; tab-stops: list .5in">
>     <span style="font-family: 'Arial','sans-serif'; font-size: 9pt; mso-fareast-font-family: 'Times New Roman';"><a href="http://kb.vmware.com/kb/1037260" target="_blank">http://kb.vmware.com/kb/1037260</a></span>
>   </li>
>   <li class="MsoNormal" style="MARGIN: 0in 0in 0pt; COLOR: #666666; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l1 level1 lfo2; tab-stops: list .5in">
>     <span style="font-family: 'Arial','sans-serif'; font-size: 9pt; mso-fareast-font-family: 'Times New Roman';"><a href="http://kb.vmware.com/kb/1037261" target="_blank">http://kb.vmware.com/kb/1037261</a></span>
>   </li>
> </ul>
> 
> <p>
>   <span style="font-family: 'Arial','sans-serif'; color: #666666; font-size: 9pt; mso-fareast-font-family: Calibri; mso-fareast-theme-font: minor-latin; mso-ansi-language: EN-US; mso-fareast-language: EN-US; mso-bidi-language: AR-SA;">VMware ESX 4.0 Patch is available for download at:<br /> Download VMware ESX 4.0 Patch <a href="http://www.vmware.com/patch/download/" target="_blank"><span style="color: #269cd7;">http://www.vmware.com/patch/download/</span></a>.</p> 
>   
>   <p>
>     Thanks,
>   </p>
>   
>   <p>
>     VMware vSphere Product Management Team </span>
>   </p></blockquote> 
>   
>   <p>
>     One of the patches included (ESX400-201104401-SG for ESX and ESXi400-201104401-SG for ESXi) resolves a couple different issues, one updates the Certification Revocation List (CRL) to revoke a key that HP uses for code-signing certain software components. HP server contains a new key pair and has re-signed the affected software components with the new key. What this means is that if you apply this patch on a HP server and you are using specific HP management agents (like the HP Management Agent for VMware ESX 4.x) you will need to download the software with the updated key and re-install it.
>   </p>
>   
>   <p>
>     The other fix within the above mentioned patch resolves a potential denial of service attack against the vmkernel over it&#8217;s management interface. When an attacker exhausts all available sockets the ESX(i) host will become inaccessible via vCenter or the vSphere client. Virtual Machines will continue to run and have network connectivity, but the ESX(i) host may need to be rebooted in order to be able to connect to the machine again. The ESX(i) system might intermittently lose connectivity caused by applications that do not correctly close sockets. If this occurs, an error message similar to the following might be written to the vpxa log file:<br /> <tt>socket() returns -1 (Cannot allocate memory)</tt><br /> An error message similar to the following might be written to the VMkernel log file:<br /> <tt>socreate(type=2, proto=17) failed with error 55</tt><br /> The Common Vulnerabilities and Exposures Project (cve.mitre.org) has assigned the name <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1758" target="_blank"><span style="color: #3399cc;">CVE-2011-1785</span></a> to this issue. More information on this patch can be found in <a title="KB 1037258" href="http://kb.vmware.com/kb/1037258" target="_blank"><span style="color: #3399cc;">KB 1037258</span></a> (ESX) and <a title="KB 1037259" href="http://kb.vmware.com/kb/1037259" target="_blank"><span style="color: #3399cc;">KB 1037259</span></a> (ESXi).
>   </p>
>   
>   <p>
>     Another patch, specific to ESXi (ESXi400-201104402-BG), has also been released. The only information on this patch can be found in <a title="KB 1037553" href="http://kb.vmware.com/kb/1037553" target="_blank"><span style="color: #3399cc;">KB 1037553</span></a> which states &#8220;This patch improves the way shared folders are handled.&#8221;.
>   </p>