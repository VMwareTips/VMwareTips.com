---
id: 2815
title: 'VMware Support Alert &#8211; ALERT: Linked Clone pool creation and recompose failure'
date: 2015-09-24T06:34:37+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2815
permalink: /2015/09/24/vmware-support-alert-alert-linked-clone-pool-creation-and-recompose-failure/
redirect_from: /wp/2015/09/24/vmware-support-alert-alert-linked-clone-pool-creation-and-recompose-failure/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "26267"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
Before upgrading to vSphere 6 update 1, VMware would like everyone to read the following KB article for important information.

Creating and recomposing linked clone desktops will fail on Horizon view 6.1.x and all older releases after upgrading to vSphere 6.0 Update 1.

The Linked Clone desktop appears to be created on vCenter, but it will be deleted  soon after vCenter complains about either “disposable” or “internal” vmdk files  this desktop.

All older versions of Horizon View Composer prior to Horizon 6.2 require SSL v3 to communicate with ESXi hosts, however the SSL v3 has been disabled in ESX6i Update 1 hosts.

Please read this KB article for further information: <a href="http://vmw.re/1FhDhaC" target="_blank">Upgrading to vSphere 6 update 1 will cause Linked Clone pool creation and recompose failure with Horizon View 6.1.x and older releases (2133018)</a>

Any updates to this information will be made in the KB article itself.