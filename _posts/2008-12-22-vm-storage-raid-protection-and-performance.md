---
id: 408
title: 'VM Storage &#8211; RAID Protection and Performance'
date: 2008-12-22T22:15:37+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=408
permalink: /2008/12/22/vm-storage-raid-protection-and-performance/
redirect_from: /wp/2008/12/22/vm-storage-raid-protection-and-performance/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "6561"
dsq_thread_id:
  - "5156589413"
categories:
  - Good Reading
  - Storage
tags:
  - disks
  - fc
  - iops
  - performance
  - raid
  - sas
  - sata
  - Storage
---
In the VM blogging world today there was some discussion on which RAID level to use with your virtual environment (<a href="http://professionalvmware.com/2008/12/19/what-raid-level-do-you-use-for-your-vmfs/" target="_blank">Professional VMware Blog</a> & <a href="http://rogerlunditblog.blogspot.com/2008/12/what-raid-level-do-you-use-for-your.html" target="_blank">Roger Lund&#8217;s IT Blog</a>). This is not an exact science, it really depends on what your doing and what your budget is &#8211; and what your storage array supports. If your as fortunate as I am and have a NetApp, you get to use their patented RAID-DP which is their flavor of RAID 6 (ADG) offering double parity &#8211; meaning you can sustain a dual disk failure per RAID group and see no performance degradation when repairing the RAID group.



If you have the money and room in your array, you can always implement RAID 10. This works as a mixture of RAID 1 and RAID 0, with a minimum of (4) disks you stripe the data over 50% of them then mirror it to the remaining 50%. Although a RAID 10 can sustain a dual disk failure, there is a catch; If both of the failures happen to disks containing the matching block &#8211; your data is gone. And you really need quite a few disks to lower your risk, for example with (4) disks in a RAID 10 your risk is 50%, (6) disks is 33% and so on. You really need a ton of disks to make this a safe option.

Ok, so this wasn&#8217;t really the reason why I wanted to post this topic &#8212; I think the other two posts above and their comments really hit hard on this &#8212; what I want to discuss is disk performance; this is something that is typically overlooked and it can really cause some heartache.

I recently ran into an environment running (12) SATA disks in a RAID-DP with it connected to VMware via FCP, but they were complaining that everything was so slow &#8212; I did a health check and CPU/Memory/IO performance was low, everything looked good. The storage array even had low utilization, I really couldn&#8217;t understand it. So, I asked the final question (which is now my first); What type of disks does your array have? They answered, SATA.

In some situations this wouldn&#8217;t matter.  SATA is a great option, but if you are like most companies and share your SAN and potentially have other applications on the same RAID group, just remember to keep track of whats on there.  If something is writing data to that SATA RAID group, the overall performance will be hit real hard, making everything slow for your VMs.

So, long story short; SATA is a great deal slower than its SAS sister and FC brother. In a presentation I did at the San Diego VMware vForum I discussed that bandwidth doesn&#8217;t really matter when it comes to VM I/O performance, it really all comes down to response time and IOPS. For example, the average 3.5&#8243; 7200 rpm SATA disk supports 65 IOPS &#8211; the average 2.5&#8243; 15k rpm SAS disk supports 156 IOPS and the average 3.5&#8243; 15k rpm FC disk supports 150 IOPS. The FC and SAS disks are almost 3 times the performance of a SATA disk &#8212; when loading up your storage environment with a egg basket of VM guests this is a huge thing to consider.

Of course, you can always throw more SATA disks into your RAID group &#8212; the more spindles, the faster performance. But IMO, if you have the budget do it right from the start and go with SAS or FC. When you start building out what can become a large deployment you&#8217;ll be glad you did.