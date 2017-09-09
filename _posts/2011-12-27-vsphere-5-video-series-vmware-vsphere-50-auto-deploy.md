---
id: 1459
title: 'vSphere 5 Video Series &#8211; VMware vSphere 5.0 Auto Deploy'
date: 2011-12-27T14:58:55+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1459
permalink: /2011/12/27/vsphere-5-video-series-vmware-vsphere-50-auto-deploy/
redirect_from: /wp/2011/12/27/vsphere-5-video-series-vmware-vsphere-50-auto-deploy/
ratings_users:
  - "6"
ratings_score:
  - "28"
ratings_average:
  - "4.67"
views:
  - "4395"
dsq_thread_id:
  - "5156598098"
categories:
  - vCenter
  - vSphere
tags:
  - auto deploy
  - dhcp
  - EMC
  - fdm
  - gpxe
  - ha
  - powercli
  - powerpath
  - tftp
  - vcenter
  - vcloud
  - vCSA
  - vsphere 5
---
<center>
</center>

Happy Holidays! This video is a continuation of my vSphere 5 Video Series, in this video I cover how to properly leverage VMware vSphere 5.0 Auto Deploy to automatically deploy ESXi hosts in your infrastructure. Auto Deploy is a new feature found in the Enterprise Plus edition of vSphere 5, it allows administrators to deploy stateless images that are deployed via gPXE directly to the RAM of the host. That&#8217;s right, ESXi hosts do not require a local HDD/USB/SDCARD to operate as they can simply download their image and configuration (via Host Profile) into RAM and automatically be placed in their correct vCenter Server datacenter/cluster or folder.

<p style="text-align: left; ">
  <a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/imagebuild.png"><img class="aligncenter" title="Image BUilder" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/imagebuild.png" alt="" width="410" /></a><br /> As shown above, PowerCLI is used to create an ESXi Image Profile, this image includes the base ESXi installation as well as any additional drivers, third-party integration or plug-in that you would like to include. That Image Profile is then attached to a Deployment Rule that is also created within PowerCLI. The deployment rule dictates what Image Profile is to be used, what host(s) are tied to the deployment rule and some other configuration specifics such as, which Host Profile to attach after the host has been added to vCenter as well as which vCenter DC/Cluster/Folder to add the host to. For example, you can leverage the same Image Profile but have different Deployment Rules based on DRS Cluster.
</p>

<p style="text-align: left; ">
  For those of you that would like to know a little more about how Auto Deploy functions under the covers, there are basically five core components when it comes to Auto Deploy. There is the actual Auto Deploy server (1) which is essentially a web server that pushes an ESXi Image Profile to the server, this is driven by the Rules Engine (2) which is accessed/configured via PowerCLI along with the Image Builder. There is a requirement for a TFTP Server (3) which will store the gPXE bootloader (4) and push it to potential ESXi hosts that are led to it by a DHCP Server (5). Once gPXE is booted it is notified to grab the ESXi Image and Configuration from the Auto Deploy server.
</p>

<p style="text-align: left; ">
  In the video I cover everything that is needed for Auto Deploy to work, including to installation of vCenter Server and the associated Auto Deploy service as well as PowerCLI and creation of the Image Profile and Deployment Rule. By the end of the video you should have a firm understanding of how to leverage Auto Deploy in your environment to its full potential. I even include steps on how to slipstream third party vendor packages into your ESXi Image Profile, including; EMC PowerPath/VE, the VMware vCloud Director agent and the VMware Fault Domain Manager agent (vmware-fdm) which is required for VMware HA to properly function.
</p>

<p style="text-align: left; ">
  For reference, the EMC PowerPath/VE 5.7 vibs can be downloaded from <a href="powerlink.emc.com" target="_blank">EMC Powerlink</a>, the VMware vCloud Director agent can be copied from your vCloud Director server from the /opt/vmware/vcloud-director/agent folder and the vmware-fdm agent can be grabbed directly from the vCenter Server by adding http://<vcenter-server>/vSphere-HA-depot as an esxsoftwaredepot in PowerCLI.
</p>

<p style="text-align: left; ">
  
</p>

<p style="text-align: left; ">
  <span>If you&#8217;d like to watch the how-to video it is located at the top of this post, it is 30 minutes in length but it does cover a lot of content so make sure you have enough time to watch it. Also, I suggest watching the video in full-screen mode by clicking the icon on the bottom right of the video. If for whatever reason the video isn’t displaying, you can also use the following link to view; </span><a href="http://youtu.be/1IJchZBEaFc" target="_blank">http://youtu.be/1IJchZBEaFc</a>
</p>

<p style="text-align: left; ">
  If you&#8217;re not into watching the video here are the necessary steps in raw form if you just want to deploy it and get it over with;
</p>

>   1. Install VMware vCenter Server (Windows or <a href="http://vmwaretips.com/wp/2011/10/13/vsphere-5-video-series-install-vcenter-50-in-around-5-minutes/" target="_blank">vCSA</a>)
>   2. Install VMware vSphere Auto Deploy (or activate Auto Deploy in <a href="http://vmwaretips.com/wp/2011/10/13/vsphere-5-video-series-install-vcenter-50-in-around-5-minutes/" target="_blank">vCSA</a>)
>   3. Install VMware PowerCLI
>   4. Download TFTP Boot Zip and place files on TFTP Server
>   5. Create ESXi Image Profile with PowerCLI 
>       1. connect-viserver <vcenter-server-fqdn>
>       2. add-esxsoftwaredepot &#8220;<path-to-esxi-zip>&#8221;
>       3. add-esxsoftwaredepot &#8220;<path-to-vcloud-director-agent-zip>&#8221;
>       4. add-esxsoftwaredepot &#8220;<path-to-emc-powerpath/ve-zip>&#8221;
>       5. add-esxsoftwaredepot &#8220;http://<vcenter-server-fqdn>/vSphere-HA-depot&#8221;
>       6. new-esximageprofile -cloneprofile &#8220;ESXi-5.0.0-<buildnumber>-standard&#8221; -name &#8220;<ImageProfileName>&#8221;
>       7. add-esxsoftwarepackage -imageprofile &#8220;<ImageProfileName>&#8221; -softwarepackage vmware-fdm
>       8. add-esxsoftwarepackage -imageprofile &#8220;<ImageProfileName>&#8221; -softwarepackage vcloud-agent
>       9. add-esxsoftwarepackage -imageprofile &#8220;<ImageProfileName>&#8221; -softwarepackage powerpath.lib.esx
>      10. add-esxsoftwarepackage -imageprofile &#8220;<ImageProfileName>&#8221; -softwarepackage powerpath.cim.esx
>      11. add-esxsoftwarepackage -imageprofile &#8220;<ImageProfileName>&#8221; -softwarepackage powerpath.plugin.esx
>   6. Create Deployment Rule with PowerCLI 
>       1. new-deployrule -name &#8220;<DeployRuleName>&#8221; -item &#8220;<ImageProfileName>&#8221; -AllHosts
>       2. add-deployrule -name &#8220;<DeployRuleName>&#8221;
>   7. Export Image Profile to ZIP Bundle 
>       1. export-esximageprofile -imageprofile &#8220;<ImageProfileName>&#8221; -exporttobundle -filepath &#8220;<path-and-filename-for-zip>&#8221;
>   8. Create DHCP Static Reservation for ESXi Host 
>       1. Include DHCP Option 66 which is the TFTP Server fqdn or IP
>       2. Include DHCP Option 67 which is the gPXE boot image (undionly.kpxe.vmw-hardwired)
>   9. Boot ESXi Host
>  10. New ESXi Host will be booted and automatically added to vCenter Server, you now have an option of configuring and creating a Host Profile. If you want to use the Host Profile you created for future ESXi Hosts you must do the following within PowerCLI 
>       1. new-deployrule -name &#8220;<DeployRuleName>&#8221; -item &#8220;<ImageProfileName>&#8221;,<HostProfileName>,<DRS-ClusterName> -pattern <optional, but could be mac or model based>
>       2. add-deployrule -deployrule &#8220;<DeployRuleName>&#8221;

<div>
  I know that seems a little confusing, but it is actually quite simpler than it looks.  You should be able to have the entire thing done during a lunch break :).
</div>

<div>
</div>