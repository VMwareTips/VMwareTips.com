---
id: 2788
title: 'VMworld Day 1 &#8211; Quick Review'
date: 2015-09-01T01:49:12+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=2788
permalink: /2015/09/01/vmworld-day-1-quick-review/
redirect_from: /wp/2015/09/01/vmworld-day-1-quick-review/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "25317"
dsq_thread_id:
  - "5156597593"
categories:
  - VMworld
tags:
  - bonneville
  - cloud foundry
  - cloud native apps
  - cna
  - containers
  - coreos
  - docker
  - EVO
  - k8
  - mesos
  - microvisor
  - pacific
  - pcf
  - photon
  - pivotal
  - vcloud air
  - VMworld
---
There&#8217;s already a ton of great bloggers out there that are getting into deep in-depth reviews of their first day of VMworld 2015, so I&#8217;m going to take a difference approach. I&#8217;m simply going to provide you with a quick highlight of the announcements that have come out of the VMworld machine, if there&#8217;s something that sparked you interest you can Google to find out more about it, hit your favorite social site, or even hit me up and I&#8217;ll be more than happy to chat about it with you.

The theme of VMworld 2015 is _&#8220;Ready for Any&#8221;_.  Focused on being ready for any challenge around speed, innovation, productivity, etc.  And VMware is dedicated to helping their customers to be ready for four key things; _Run_ &#8211; be ready to run any applications, _Build_ &#8211; traditional applications and cloud native applications, _Deliver_ &#8211; any application to any device, and _Secure_ &#8211; by accelerating networking and security from the datacenter to the device. Ultimately VMware&#8217;s goal has been to provide Freedom, Flexibility and Choice.

<span style="text-decoration: underline;"><strong>Big Announcements</strong></span>
  
1. _<a href="http://www.vmware.com/company/news/releases/vmw-newsfeed/VMware-Unveils-the-Easiest-Way-to-Deploy-and-Operate-the-Software-Defined-Data-Center-at-Scale/1984725" target="_blank">VMware EVO SDDC</a>_ (previously EVO:Rack) &#8211; Zero to SDDC in 2 Hours, including vSphere, VSAN, NSX, vRealize Suite and more. Can run at extremely large scale, includes physical infrastructure management and deployment (think deploying ESXi and managing physical spine/leaf switching). Complete SDLC.

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/vmware-evo-sddc.jpg" alt="vmware-evo-sddc" width="480" />

2. _<a href="http://www.vmware.com/company/news/releases/vmw-newsfeed/VMware-Extends-Unified-Hybrid-Cloud-Platform,-Empowers-Customers-to-Innovate-Faster/1984569" target="_blank">vCloud Air</a>_ &#8211; Tons of things here. First, Project Skyscraper, which are new capabilities in vCloud Air that will enable customers to extend their data center to the public cloud and seamlessly operate across boundaries while providing enterprise-level security and business continuity. VMware demonstrated live workload migration through Cross-Cloud vMotion and Content Sync across a private cloud and vCloud Air. One of the technologies that helped enable this for vCloud Air was the deployment of VMware NSX (providing Intelligent Routing, Strong Encryption, WAN Acceleration, VXLan Extensions and Direct Connect). vCloud Air Object Storage was also announced, with options available Powered by Google as well as EMC. Their first DBaaS offering, vCloud Air SQL is now available as part of an Early Access Program. A new pricing model for DRaaS (DR OnDemand) and Site Recovery Manager Air (SRM SaaS) will be in Early Access soon.  They also demonstrated their Backend as a Service offerings, which are provided by strategic partners. Here they highlighted the capabilities of <a href="http://vcloud.vmware.com/service-offering/backend-as-a-service" target="_blank">Kinvey</a>.

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/unifiedhybridcloud.jpg" alt="unifiedhybridcloud" width="480" />

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/vcansx.jpg" alt="vcansx" width="480" />

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/vcavmotion.jpg" alt="vcavmotion" width="480" />

3. _<a href="http://www.vmware.com/company/news/releases/vmw-newsfeed/VMware-Previews-vSphere-Integrated-Containers-and-Photon-Platform-to-Accelerate-Cloud-Native-Apps-in-the-Enterprise/1984726" target="_blank">Cloud Native Applications</a>_ &#8211; This is another area of big waves, and served as the official public announcement of was as previously known as Project Bonneville/Pacific and the previously released Photon/Lightwave. Just like the title mentioned, this is all about deploying and running Cloud Native Applications. If you don&#8217;t know what this means I recommend checking out <a href="http://12factor.net/" target="_blank">The Twelve-Factor App</a>. These new 3rd Platform style applications are powered by those fancy buzz-word open source projects like Docker, Mesos, K8 and CoreOS. Developers do version control with tools like GitHub, and they push out their development landscapes with tools like Vagrant.  It&#8217;s a crazy new world out there :)

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/photonplatform.jpg" alt="photonplatform" width="480" />

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/whatsinphotonplatform.jpg" alt="whatsinphotonplatform" width="480" />

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/cnademo.jpg" alt="cnademo" width="480" />

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/cnaoptions.jpg" alt="cnaoptions" width="480" />

<img src="https://www.vmwaretips.com/wp/wp-content/gallery/vmworld2015/photondistro.jpg" alt="photondistro" width="480" />

Two sum up Cloud Native Apps there are two methods of deployment. In a mixed-mode, which uses the traditional vSphere product along with vSphere Integrated Containers (VIC). VIC is a Controller (Photon Controller) along with VMFork (Project Fargo) and the Photon OS to create what&#8217;s being called a jeVM (Just Enough VM). The developer would make their request to the Photon Controller, which in turn instantly (VMFork) creates a new virtual machine that uses the Photon OS as the Guest OS and creates your single container per-VM. This concept of a single container per VM is a little sacrilegious in the container world but it actually does provide some great benefits around security and networking. One last note about VIC is that it&#8217;s great for smaller deployments as it can share the same ESXi servers you currently use today.

Are you interested in massively doing containers? Well this is where the Photon Platform might be best for you.  The Photon Platform takes what I talked about above in VIC but runs it all on top of a extremely thin, powerful and fast micro-visor (think hypervisor, but lean and mean). To take it a step further, say you don&#8217;t want to build your own unstructured PaaS (using the buzz-word open source projects above) and just want to set it and forget it&#8230;.go with the Pivotal Cloud Foundry and Photon Platform bundle.

Need more help making sense of it all&#8230;check out <a href="http://vmware.com/go/cnaguide" target="_blank">http://vmware.com/go/cnaguide</a>.

Well there you go&#8230;.a (somewhat) quick review of Day 1. Good night and we&#8217;ll see you all tomorrow morning at 9am!