---
id: 1297
title: VMware vCenter XVP Manager
date: 2011-02-26T11:17:39+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=1297
permalink: /2011/02/26/vmware-vcenter-xvp-manager/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 2505
dsq_thread_id:
  - 5156593806
categories:
  - Hyper-V
  - vCenter
tags:
  - client
  - fling
  - hyper-v
  - labs
  - Microsoft
  - vcenter
  - VMware
  - vsphere
  - xvp
  - xvp manager
---
**vm**ware Labs has released vCenter XVP Manager and Converter, their first stab into management of non-VMware virtualized environments. vCenter XVP Manager allows you to use the vSphere Client to manage Hyper-V Server 2008 hosts and their associated virtual machines, it also allows you to easily migrate those Hyper-V based virtual machines into VMware virtual machines.

The installation is pretty simple, you first install a server piece that could very well be installed on your vCenter Server, then you install a XVP Manager Plug-in into your vSphere Client which is done via the vSphere Client Plug-in Manager.__

This product is currently only listed as a **vm**ware Labs Fling, which means that it is not guaranteed that it will continue beyond it&#8217;s 1.0 Technical Preview status, but if people like it and push **vm**ware for this type of functionality we may very well see it embedded within the core vCenter Server product.

<p style="text-align: center;">
  <a href="http://labs.vmware.com/wp-content/uploads/2011/02/xvp.png"><img class="aligncenter" src="http://labs.vmware.com/wp-content/uploads/2011/02/xvp.png" alt="" width="480" /></a>
</p>

<p style="text-align: left;">
  For more information and to download <strong>vm</strong>ware vCenter XVP Manager check out the <strong>vm</strong>ware Labs <a href="http://labs.vmware.com/flings/xvp" target="_blank">website</a>.
</p>