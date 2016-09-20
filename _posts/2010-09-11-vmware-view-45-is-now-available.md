---
id: 1219
title: VMware View 4.5 is Now Available
date: 2010-09-11T10:31:56+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1219
permalink: /2010/09/11/vmware-view-45-is-now-available/
aktt_notify_twitter:
  - yes
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
aktt_tweeted:
  - 1
views:
  - 2645
categories:
  - View
tags:
  - cache
  - efd
  - EMC
  - Storage
  - view
---
One week after the finish of VMworld 2010 _US Edition_ VMware drops one of the most anticipated releases of their flagship desktop virtualization product, VMware View 4.5.

Before I get into the details of what&#8217;s new in this major dot release one must ponder why this release goes against the VMware version standards that were placed when vSphere 4.0 was released.  How come this version isn&#8217;t 4.1? Or furthermore how come vSphere 4.1 isn&#8217;t vSphere 4.5 &#8212; there were definitely enough enhancements for vS 4.1 to be a major release.

<!--more-->

Anyways it is what it is and perhaps we could expect something even greater from the vSphere family before it&#8217;s next major version (5.0), which has been hinted in this <a href="http://www.youtube.com/watch?v=H5aAYOy2RPE" target="_blank">YouTube</a> (at 1:32) video showing the upcoming iPad vSphere Management App.

So now back to our regularly scheduled program&#8230;.what&#8217;s new in View 4.5:

  * **View Client with Local Mode**&#8211; Provides the industry&#8217;s first integrated offline and server-hosted solution for desktop virtualization, addressing BYOPC use cases.
  * **Full Windows 7 support**&#8211; Provides full support for Windows 7. With View 4.5 and ThinApp 4.6, organizations can migrate to Windows 7 at half the cost and time.
  * **View Client for Mac OS X** &#8211; Enables Mac users to access hosted Windows virtual desktops, extending the BYOPC use cases to Mac users.
  * **Integrated Application Assignment**&#8211; Simplifies the delivery of ThinApp applications to end-users using the View Administrator console.
  * **Rich Graphical Dashboards** &#8211; Simplifies management and monitoring through improved reporting and diagnostics.
  * **Role Based Administration** &#8211; Distributes IT tasks to the right administrator.
  * **Integration with Microsoft SCOM and PowerShell** &#8211; Enables integration into existing management infrastructure to further simplify the management of View virtual desktops, as described in the new <a href="http://vmware.com/pdf/view45_integration_guide.pdf" target="_blank">VMware View Integration Guide</a>.
  * **Support for vSphere 4.1 and vCenter 4.1**&#8211; Delivers integration with the most widely-deployed desktop virtualization platform in the industry. Takes advantage of optimizations for View virtual desktops.
  * **Increased scalability** &#8211; Allows you to deploy 10,000 virtual desktops per pod and use this modular architecture to scale out across your organization. For more information, see the <a href="http://vmware.com/pdf/view45_architecture_planning.pdf" target="_blank">VMware View Architecture Planning Guide</a>.
  * **Tiered storage support** &#8211; Reduces the cost and increases the performance of storage by enabling you to take advantage of multiple storage tiers, including high performance and locally attached storage.
  * **Lowest Cost Reference Architectures**&#8211; VMware has worked with partners such as Dell, HP, Cisco, NetApp, and EMC to provide prescriptive reference architectures to enable you to deploy a scalable and cost-effective desktop virtualization solution.

So I&#8217;d like to focus on one of these enhancements as I feel it provides one of the greatest reasons to go to View 4.5 as well as some game-changing design considerations, **Tiered Storage Support**.

The concept behind Tiered Storage Support is to effectively separate your desktop replicas from your linked clones. So if you&#8217;re thinking&#8230;why does it matter? Let&#8217;s dive a little deeper into why this is such a critical feature.

Say you have a 1,000 desktop virtual environment running on View 4.0, lets also say that these desktops require ~20 IOPs/user and that your storage array is utilizing 15k RPM fibre-channel disks. You would roughly need 111 drives to meet the IO load for these users (250 for SATA), and that&#8217;s not even calculating RAID or Hot Spares for that matter &#8211; we&#8217;re just using raw numbers to keep this simple.

So taking that previous paragraph into consideration, lets say we upgrade to View 4.5 and can now place that replica on an EFD tier. On average an EFD drive will handle ~3,500 IOP/s &#8211; taking this into mind we can effectively meet the IO needs of our 1,000 desktop users with 6 EFD drives&#8230;that&#8217;s right 6!

Just imagine the cost savings, not only CAPEX but OPEX from all power/cooling savings. EFD for replicas and SATA for linked clone and deltas &#8212; doesn&#8217;t get much more efficient than that&#8230;.or does it?  Check out <a href="http://virtualgeek.typepad.com/virtual_geek/2010/05/emc-unified-storage-next-generation-efficiency-details.html" target="_blank">this really cool blog post</a> from Chad Sakac on what EMC is doing with EFD drives to effectively achieve 2TB of additional Read/Write cache on their mid-range storage array.