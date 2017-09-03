---
id: 268
title: 'Product Review : Sun VirtualBox'
date: 2008-11-02T10:16:55+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=268
permalink: /2008/11/02/product-review-sun-virtualbox/
ratings_users:
  - "3"
ratings_score:
  - "14"
ratings_average:
  - "4.67"
views:
  - "7350"
dsq_thread_id:
  - "5156596851"
categories:
  - Good Reading
tags:
  - hypervisor
  - mac
  - virtualbox
  - vmware server
  - vmware workstation
---
I never was really interested in Sun VirtualBox until I went to a Product Roadshow put on by Sun Microsystems about 2 weeks ago. As soon as I returned to my office I immediately download VirtualBox to see what all the hype was about.

<!--more-->

First I must tell you my main PC that I tested this product with was a HP x4600 workstation with a Dual Core Intel 3GHz processor and 3.5GB of RAM.  My primary O/S is Ubuntu 8.04.

Prior to using VirtualBox I had a VMware Workstation 6.5 Virtual Machine configured with 1.5GB of RAM running Windows XP Pro SP3, my VMDK is 30GB. I heavily used the host/guest interaction capability in Workstation, I often copied files from my Ubuntu desktop straight to the desktop of my Windows XP guest, using Workstations drag and drop feature, this feature is extremely useful. Thus, I immediately decided that I cannot compare VirtualBox to Workstation, as they are not in the same product category. Sun VirtualBox should be more compared to VMware Server.

First thing I noticed was the installation of VirtualBox, it was extremely easy and straight forward.  I didn&#8217;t run into the same issues I have had in the past with installing VMware Server (or Workstation for that matter). For Ubuntu I had the choice of using apt-get or downloading the deb file and using dpkg to install. Keep in mind that for Windows installations this would not be an issue, all three programs utilize MSI package installers to make it quick and easy. Another note is that VirtualBox is extremely lightweight, the download is only 32mb, compared to the mammoth 539mb file for VMware Server 2.0.  Also noted is the extensive O/S build list for VirtualBox, which is pretty much every O/S under the sun, including Mac.

After installation I was delighted to see that I could use my existing VMDK file and get up and running quickly.  I was installed, up and powered on with my existing VM within 5 minutes.  One thing I noticed immediately was how fast everything seemed. The GUI loaded quickly and I started my guest and switched to full screen mode, everything was extremely smooth and clean.  VMware Server has a web-based administration tool which can be sometimes quarky, loading the console of a VM doesn&#8217;t seem as quick as VirtualBox but in the end they both provide the same product.

Long story short, VirtualBox is an excellent type-2 hypervisor, it is ported to all major O/S distributions and I would highly recommend it if your looking for a small, quick and easy to use virtualization program.  VMware Server is also an excellent product but it just seems a little bulky for what it does, I&#8217;m also not impressed with the web-based administration introduced in version 2.0.

Although, if you need 3D graphics support, host/guest integration (VirtualBox & Server both have shared folders, I&#8217;m talking about drag and drop functionality), record/reply usage for development testing, etc. I would still recommend going with VMware Workstation 6.5.