---
id: 1353
title: VAAI Train Running Late Today
date: 2011-06-14T17:28:32+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1353
permalink: /2011/06/14/vaai-train-running-late-today/
ratings_users:
  - "2"
ratings_score:
  - "10"
ratings_average:
  - "5"
views:
  - "1722"
dsq_thread_id:
  - "5156593571"
categories:
  - Storage
  - vSphere
tags:
  - Bug
  - vaai
  - vmax
  - vsphere
  - xcopy
---
Another one of those posts today that most likely will not affect most, however there is a known issue with the vStorage APIs for Array Integration (VAAI) mixed together with EMC VMAX Storage Arrays. My best bud, Chad Sakac, wrote about this last week (<a href="http://virtualgeek.typepad.com/virtual_geek/2011/06/important-vmax-epack-and-vsphere-hotfix.html" target="_blank">over here</a>).

Long story short, if you&#8217;re running a VMAX with Enginuity 5875.135.91 or 5875.139.93 along with ESX(i) 4.1 hosts you may see some slowness when trying to do things like Storage vMotion, Deploy from Template, etc&#8230;basically things that leverage HardwareAcceleratedMove.

So how do you fix it?  First thing is you need to disable HardwareAcceleratedMove, instructions on how to do this can be found in <a href="http://kb.vmware.com/selfservice/search.do?cmd=displayKC&docType=kc&docTypeID=DT_KB_1_1&externalId=1033665" target="_blank">VMware KB1033665</a>. Next thing is to contact EMC Support and have the ePack that engineering released for this problem installed on your VMAX. Then finally, contact VMware support for their hotfix&#8230;rumor has it that a VMware support bundle should be released sometime soon. After you have the patch for VMAX as well as vSphere you should have no problem turning HardwareAcceleratedMove back on.

So to wrap this up&#8230;.VAAI issue when mixed with VMAX, but it doesn&#8217;t affect all VAAI functionality, just XCOPY (HardwareAcceleratedMove) and even then it doesn&#8217;t affect every single operation. Get the patches, get them installed and get back on schedule!