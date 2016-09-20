---
id: 1427
title: 'vSphere 5 Video Series &#8211; Installing ESXi 5.0 in Under 5 Minutes'
date: 2011-10-10T06:00:55+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=1427
permalink: /2011/10/10/vsphere-5-video-series-installing-esxi-50-in-under-5-minutes/
ratings_users:
  - 2
ratings_score:
  - 10
ratings_average:
  - 5
views:
  - 2131
categories:
  - vSphere
tags:
  - esx
  - esxi
  - installation
  - installing
  - video
  - vsphere 4
  - vsphere 5
---
This is going to be the first of many in my vSphere 5 Video Series where I&#8217;ll cover the basics to getting vSphere 5.0 installed, configured and operating. In this video see just how easy it is to do a bare-metal installation of ESXi 5.0. Out of all of the install and upgrade options available for vSphere 5.0 this by far is the easiest and cleanest method in my opinion.

Upgrading can be extremely easy as well, by leveraging VMware Update Manager (VUM) it allows existing configurations to be migrated and will even allow you to migrate from ESX to ESXi. One thing to keep in mind when doing a migration with VUM from vSphere 4 to vSphere 5 is that if you are using the ESX edition of vSphere 4 and have custom scripts, agents or modules loaded into ESX those will **<span style="text-decoration: underline;">not</span>** be migrated into ESXi 5.0.

Whatever your situation might be, my recommendation has always been to do a fresh installation of ESXi then leverage Host Profiles to push the configuration to the host. Even if you&#8217;re not an Enterprise Plus customer you can still get all of the benefits, like Host Profiles, free for 60 days by simply not licensing the product. Remember, you must license before the 60 days are up to avoid any service disruption.

Another great feature of vSphere 5 is Image Builder and Auto Deploy, I&#8217;ll cover Auto Deploy into more detail later, but with Image Builder you can build custom ESXi builds that include third party drivers and other custom data. Don&#8217;t worry though, you can still do custom installations with kickstart if you&#8217;d like, but after you see Auto Deploy you&#8217;re not going to want to.

So have a view of this video to see just how easy it is. I have sped up some portions of the video, specifically the blade server booting, the hardware discovery process and actually installation portion. Also, I suggest watching the video in full-screen mode by clicking the icon on the bottom right of the video. If for whatever reason the video isn&#8217;t displaying, you can use the following link to view; <a title="Installing ESXi 5.0 in Under 5 Minutes" href="http://youtu.be/aN9mc9YNiC0" target="_blank">http://youtu.be/aN9mc9YNiC0</a>