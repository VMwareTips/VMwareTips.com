---
id: 691
title: Fast Network Throughput in ESX
date: 2009-04-07T16:36:26+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=691
permalink: /2009/04/07/fast-network-throughput-in-esx/
aktt_notify_twitter:
  - yes
ratings_users:
  - 1
ratings_score:
  - 5
ratings_average:
  - 5
aktt_tweeted:
  - 1
views:
  - 4196
categories:
  - Networking
  - Storage
tags:
  - nfs
  - speed
  - test
  - throughput
  - vmdk
---
Doing some speed tests of IP based storage gave me some good results. First I enabled Jumbo frames on my dedicated IP storage Ethernet card, then I set the MTU on the vSwitch and the VMKnic to 9000 (Scott Lowe has a great write-up on doing this on his <a href="http://blog.scottlowe.org/2008/04/22/esx-server-ip-storage-and-jumbo-frames/" target="_blank">website</a>). I then mounted a NFS volume as Datastore and did a copy of a VMDK file which currently resides on a 7200rpm SATA 3 drive to the mounted NFS volume.

[<img class="aligncenter size-full wp-image-692" title="vsphere_netspeed" src="http://vmwaretips.com/wp/wp-content/uploads/2009/04/vsphere_netspeed.png" alt="" width="470" height="208" srcset="http://www.vmwaretips.com/wp/wp-content/uploads/2009/04/vsphere_netspeed.png 470w, http://www.vmwaretips.com/wp/wp-content/uploads/2009/04/vsphere_netspeed-300x132.png 300w" sizes="(max-width: 470px) 100vw, 470px" />](http://vmwaretips.com/wp/wp-content/uploads/2009/04/vsphere_netspeed.png)

I copied the 8GB file in under 2 minutes and my average MbTX/s was around 525Mb (65MBps) &#8211; keep in mind, this was a copy from a local SATA disk (low IOPS) and I was able to get around 65MBps &#8212; not bad!

The biggest thing to remember, VMDK access needs low latency&#8230;not high throughput &#8212; this is why NFS has become so popular for VMDK storage.