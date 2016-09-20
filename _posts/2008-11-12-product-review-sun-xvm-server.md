---
id: 275
title: 'Product Review : Sun xVM Server'
date: 2008-11-12T11:40:01+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=275
permalink: /2008/11/12/product-review-sun-xvm-server/
ratings_users:
  - 1
ratings_score:
  - 1
ratings_average:
  - 1
views:
  - 2813
dsq_thread_id:
  - 5156596876
categories:
  - Good Reading
tags:
  - esxi
  - solaris
  - sun
  - xvm server
  - zfs
---
Just like everyone else, Sun has joined the Virtualization marketplace. A couple weeks back I reviewed Sun VirtualBox which takes a stab at VMware Server with somewhat of a success (simply because its fast and runs on virtually any operating system (Mac included)). This round I will discuss their bare-metal stage 1 hypervisor, xVM Server.

<!--more-->

At first I was a little excited about this product, the fact that it is based on the Sun Solaris operating system was definietly an eye opener.  But, once I dug deeper I was almost immediately disappointed in the short comings of this product.  Keep in mind, this product is still in Beta, but from what I hear even at its 1.0 GA release it will not be able to touch any of its competitors.

Here is some cut and dry information on xVM server, I&#8217;m going to hold off on a full product review until it becomes GA, but frankly &#8211; I don&#8217;t even feel its worth downloading.

  * Type-1 Bare Metal hypervisor
  * Built on the Solaris kernel (this means excellent throughput and performance)
  * Web Based Administration (Java and Ajax built)
  * Supports ZFS filesystem (a definite plus, this is a phenomenal filesystem)
  * Access to Guest consoles is via Java applet (if anything like Sun&#8217;s iLO applets, this can be buggy)
  * **No VLAN or vSwitch support!**
  * **No Balooning driver or other Guest OS based CPU/MEM performance enhancements**
  * **NFS only support at GA &#8211; Local Disk only during Beta (no iSCSI or FCP)**

IMO its going to take a lot from Sun to get this product where it needs to be.  To me this is an attempt to compete with ESXi, but it is nowhere near equal.  If your looking for a free bare metal hypervisor, stick with VMware ESXi.

More information on Sun xVM Server can be found at <a href="www.xvmserver.org" target="_blank">www.xvmserver.org</a>