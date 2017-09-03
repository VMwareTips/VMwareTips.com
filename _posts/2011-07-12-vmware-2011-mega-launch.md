---
id: 1355
title: vmware 2011 Mega Launch
date: 2011-07-12T09:00:54+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1355
permalink: /2011/07/12/vmware-2011-mega-launch/
ratings_users:
  - "1"
ratings_score:
  - "5"
ratings_average:
  - "5"
views:
  - "4780"
categories:
  - Cloud
  - Security
  - SRM
  - Storage
  - vCenter
  - VMware HA
  - vSphere
tags:
  - sdrs
  - site recovery manager
  - srm
  - storage drs
  - vaai
  - vasa
  - vcd
  - vcloud director
  - VMware
  - vsa
  - vshield
  - vsphere
  - vsphere 5
---
It is 9am Pacific Time on Tuesday, July 12th 2011 and I sure hope you&#8217;re tuned into the **vm**ware Mega Launch so greatly titled _&#8220;Raising the Bar, Part V&#8221;_. If you&#8217;re not watching the live broadcast, stop right here and tune into it by <a href="http://event.on24.com/r.htm?e=319982&s=1&k=82E09EE9B6FB6F29E31FB41998C23C79" target="_blank">clicking this link</a>, then come back and read this post.

Spoiler alert&#8230; reading beyond this point talks about amazing updates and new features from **vm**ware!

<!--more-->

This by far has to be the most exciting launch in the history of **vm**ware, not only are we getting an update to the vSphere product suite that has hundreds if not thousands of enhancements and new features, we&#8217;re also getting updates to other great products like vCloud Director, vShield and SRM.

In fact, there are so many changes and so much new great things to talk about I can&#8217;t do it all in one post. So I&#8217;ve decided that I will need to break these up into multiple posts, each with deep detail. I&#8217;ll release this posts as quickly as I can write them, but until I have them completed I want to provide you with some of the great core details from this mega launch.

So first off get ready for another new term from **vm**ware, Cloud Infrastructure and Management. To sum it up, CIM basically includes vSphere (ESXi), vCenter, vShield and vCloud Director as a single package/methodology called CIM. These are all of the building blocks necessary to build a robust, elastic and efficient hybrid cloud. I have a feeling we&#8217;re going to hear a lot about how vSphere 5 along with the other above mention products are the industry best pieces for running a Cloud Infrastructure.

<p style="text-align: center;">
  <a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/cim.png" rel="attachment wp-att-1376"><img class="aligncenter size-full wp-image-1376" title="CIM" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/cim.png" alt="" width="450" height="225" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/cim.png 528w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/cim-300x150.png 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
</p>

On a side tangent, there is so much discussion on the cloud you wouldn&#8217;t believe it. On an almost daily basis I&#8217;m meeting with customers to discuss their &#8220;Cloud Strategy&#8221;. Customers <span style="text-decoration: underline;">want</span> Hybrid Cloud computing and with these latest updates that I&#8217;m going to discuss I think we&#8217;re finally at a place where we truly can have application and data mobility, moving our workloads fluidly across our own data-centers in an automated load balanced fashion, from compute to now storage, as well as being pushed out to external hosting (cloud) providers for extreme elasticity as well as fault tolerant (BC/DR) infrastructure.

Ok, so lets get started on all of these updates!

**vSphere 5 (including ESXi 5.0)**
  
First off, everyone should already know but if you do not, there is no longer Classic ESX with the traditional Service Console. **vm**ware stated that version 4.1 would be their last release of the Classic ESX install and now with version 5.0 there is only ESXi.

_Performance &#8211;_ There have been a number of enhancements to the core **vm**ware enterprise hypervisor, in this latest release we&#8217;ll see _huge_ performance improvements to the vmkernel but as well as in Virtual Machine density. ESXi hosts can support up to 512 virtual machines on 160 logical CPUs with up to 2TB of RAM, while Virtual Machines can now scale to 32 vCPUs with 1000GB of Memory and have been tested to push 1,000,000 IOPs. What this basically means is there shouldn&#8217;t be any performance related reason why you cannot virtualize any workload. The most demanding workloads are being virtualized such as Oracle RAC, Microsoft SQL, SAP and Exchange 2010.

<p style="text-align: center;">
  <a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/perf.png" rel="attachment wp-att-1377"><img class="aligncenter size-full wp-image-1377" title="perf" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/perf.png" alt="" width="450" height="220" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/perf.png 618w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/perf-300x146.png 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
</p>

_Image Builder_ &#8211; this is a new utility built upon PowerCLI that allows you to create custom ESXi builds, it allows you to inject ESXi VIBs, Driver VIBs and OEM VIBs to create an installable or PXE boot-able (I&#8217;ll explain why shortly) ESXi image. If you&#8217;re unaware of what a VIB is, it stands for **vm**ware Infrastructure Bundle and you can think of it almost as a <a href="http://en.wikipedia.org/wiki/RPM_Package_Manager" target="_blank">RPM</a> bundle.

<p style="text-align: center;">
  <a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/imagebuild.png" rel="attachment wp-att-1378"><img class="aligncenter size-full wp-image-1378" title="imagebuild" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/imagebuild.png" alt="" width="450" height="280" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/imagebuild.png 626w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/imagebuild-300x186.png 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
</p>

_Auto Deploy_ &#8211; Think UCS Service Profile but at the O/S level. There isn&#8217;t any hardware abstraction for moving an existing ESXi image between different hardware, but with Auto Deploy you can quickly and easily create stateless ESXi servers with no disk dependency. To sum it up, you PXE boot your server, the ESXi image is loaded into host memory from the Auto Deploy server, its configuration is applied using an answer file as well as host profile and that host is then connected/placed into vCenter. Hose something? A simple reboot will give you a fresh ESXi image in a matter of minutes. Need to expand your cluster? Bring up another host and add it to the cluster within minutes.

_vCenter Virtual Appliance (VCVA) &#8211;_ Whoo Hoo! Looks like that <a href="http://communities.vmware.com/community/vmtn/beta/vcserver_linux" target="_blank">Tech Preview</a> of vCenter Server on Linux finally hit GA! **vm**ware has released with vSphere 5 a virtual appliance of vCenter Server that is based on Linux! This also includes a feature rich browser based vSphere Client completely built on Adobe Flex, this is not a replacement for the traditional installed vSphere Client but it is a nice move forward in vSphere management. Ahhh, do you remember the MUI? :)

_High Availability (HA) Completely Rewritten &#8211;_ Way too much to discuss here, but a complete rewrite to the core HA functionality has happened. HA can now leverages multiple communication paths between agents (referred to as FDM or Fault Domain Manager) including network and storage (datastore). HA agents no longer use a Primary/Secondary methodology, during cluster creation a single Master is chosen and each remaining host is a Slave.

<a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vmha.png" rel="attachment wp-att-1379"><img class="aligncenter size-full wp-image-1379" title="vmha" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vmha.png" alt="" width="278" height="376" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vmha.png 278w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/vmha-221x300.png 221w" sizes="(max-width: 278px) 100vw, 278px" /></a>

_VMFS5 &#8211;_ Oh my! 64TB datastores anyone with a single easy to use 1M block size? You got it! Along with VAAI 2.0 which includes two new block primitives, Thin Provision Stun (finally!) and Space Reclaim. NFS also doesn&#8217;t need to feel left out because we now have Full Clone, Extended Stats and Space Reservation for NFS datastores. We also have a new API called VASA, vStorage APIs for Storage Awareness which will provide a number of enhancements such as profile-driven storage (think EMC FAST-VP being integrated with vSphere). Quickly back to VAAI 2.0, Thin Provision Stun will protect your virtual machines if your datastore runs out of space and Space Reclaim will use SCSI UNMAP instead of WRITE ZERO to remove space, this will allow the array to release those blocks of data back to the free pool.

<p style="text-align: center;">
  <a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/storprof.png" rel="attachment wp-att-1380"><img class="aligncenter size-full wp-image-1380" title="storprof" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/storprof.png" alt="" width="449" height="202" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/storprof.png 734w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/storprof-300x134.png 300w" sizes="(max-width: 449px) 100vw, 449px" /></a>
</p>

_Storage DRS (SDRS) &#8211;_ DRS load balancing Virtual Machines across hosts is to SDRS performing Storage vMotion on VMDKs for better performance, capacity utilization, etc. This also includes initial placement as well as allowing affinity based rules for VMDKs. SDRS can monitor for capacity utilization as well as I/O metrics (latency) and dynamically balance your VMDKs across multiple datastores.

<p style="text-align: center;">
  <img class="aligncenter size-full wp-image-1381" title="sdrs" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/sdrs.png" alt="" width="450" height="252" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/sdrs.png 711w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/sdrs-300x168.png 300w" sizes="(max-width: 450px) 100vw, 450px" />
</p>

_Storage vMotion &#8211;_ Snapshot support!  As well as being able to move around Linked Clones. There has also been some core enhancements to make things faster and more consistent.

_vSphere Storage Appliance (VSA) &#8211;_ It is what it sounds like, a virtual storage appliance that allows SMB customers to use local disk on the ESXi host presented out as an NFS datastore to the vSphere Cluster. There is replication technology behind it so if you do lose an ESXi host you will not lose data nor will you lose connectivity to your virtual machines. This is meant for up to 3 ESXi hosts and is really tailored for the SMB or ROBO market.

<p style="text-align: center;">
  <a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vsa.png" rel="attachment wp-att-1382"><img class="aligncenter size-full wp-image-1382" title="vsa" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vsa.png" alt="" width="450" height="316" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vsa.png 713w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/vsa-300x210.png 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
</p>

There is so much more in vSphere 5, but like I said I wanted to just give a brief overview at this time.

**Site Recovery Manager 5**
  
_Host Based Replication &#8211;_ New feature within SRM5, no longer is SAN storage/replication required for SRM. You can now replicate your data host based for disaster recovery scenarios in your virtual environment. Key takeaways, replication between heterogeneous datastores and it is managed as a property of the virtual machine. Powered-off VMs are not replicated, non-critical data (logs, etc) are not replicated. Physical RDMs are not supported. Snapshots work, snapshot is replicated, but VM is recovered with collapse snapshots. Fault Tolerant, Linked Clones and VM Templates are not supported.

_Automated Failback &#8211;_ Replication is automatically reversed and with a single click you can failback your virtual machines from your disaster site to your production site. This is huge! You have no idea how much of a pain it is to failback a site with SRM, unless you&#8217;re using the <a href="http://virtualgeek.typepad.com/virtual_geek/2008/08/a-few-technic-2.html" target="_blank">EMC plug-in</a> :)

_Misc &#8211;_ Completely new interface, still within the vSphere Client as a plug-in but now you can manage it all from a single UI, no need to use two clients or a linked mode vCenter.

**vCloud Director 1.5** 
  
Tons of new APIs within vCloud Director 1.5, including vCloud Orchestration via a vCenter Orchestrator module. Supported for Linked Clones is a huge leap forward, you can now deploy vApps in a matter of seconds with minimal storage consumption. Microsoft SQL is now supported as a back-end database which will make standing up a vCD instance in your lab a lot easier because you won&#8217;t need to worry about an Oracle database :). There is also support for federated multi-vClouds by linking vCD instances as well as enhanced vShield integration specifically around IPSec VPN.

<a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/linkedclone.png" rel="attachment wp-att-1383"><img class="aligncenter size-full wp-image-1383" title="linkedclone" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/linkedclone.png" alt="" width="257" height="303" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/linkedclone.png 257w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/linkedclone-254x300.png 254w" sizes="(max-width: 257px) 100vw, 257px" /></a>

Are you still awake? 1170+ words into this post and I&#8217;m still not complete&#8230;.and this is just the _brief_ overview! Whew!!  **vm**ware you really outdid yourself!

<span><strong>vShield 5</strong><br /> <em>vShield Edge</em> &#8211; provides us with true multi-tenant site separation complete with VPN capabilities, DHCP, Stateful Firewall and now Static Routing within vShield Edge 5.0.</span>

<p style="text-align: center;">
  <a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vshield.png" rel="attachment wp-att-1385"><img class="aligncenter size-full wp-image-1385" title="vshield" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vshield.png" alt="" width="450" height="343" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vshield.png 576w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/vshield-300x229.png 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
</p>

_vShield App &#8211;_ gives us layer2/3 protection with VM-level enforcement now with group based policies found in vShield App 5.0 as well as enabling multiple trust zones on the same vSphere cluster. Layer 2 protection coupled with APIs enable automatic quarantining of compromised VMs.

_vShield Data Security_ &#8211; is a new member of the vShield family that allows you to monitor virtual machines continuously and completely transparent to the VM for compliance such as PCI, PHI, PII and HIPAA to name a few.

<p style="text-align: center;">
  <a href="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vsds.png" rel="attachment wp-att-1384"><img class="aligncenter size-full wp-image-1384" title="vsds" src="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vsds.png" alt="" width="450" height="279" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/07/vsds.png 669w, http://vmwaretips.com/wp/wp-content/uploads/2011/07/vsds-300x186.png 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>
</p>

_vShield Manager &#8211;_ Enterprise roles found in Manager 5.0 now provide the separation of duties required by some security and compliance standards.

So there you have it&#8230;. a brief 1706 word blog post covering just the high-level details of the **vm**ware mega launch. Like I said earlier, I&#8217;m going to try to focus in on some deep-dive details on some of the major topics above. But until then, read up as much as you can on the **vm**ware website and hopefully relatively soon the bits will be available for public consumption so you can get all of this great fresh new code in your lab!