---
id: 515
title: 'VMware Workstation &#038; Ubuntu 8.10 Ctrl-Alt-Ins not working'
date: 2009-01-29T13:03:45+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=515
permalink: /2009/01/29/vmware-workstation-ubuntu-810-ctrl-alt-ins-not-working/
redirect_from: /wp/2009/01/29/vmware-workstation-ubuntu-810-ctrl-alt-ins-not-working/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
aktt_tweeted:
  - "1"
views:
  - "6839"
dsq_thread_id:
  - "5156590012"
categories:
  - Linux
  - Workstation
tags:
  - key mapping
  - ubuntu
  - workstation
---
Well, if some of you haven&#8217;t heard (from twitter) &#8211; I recently lost my HDD. Which not only stinks, but it is a huge pain having to rebuild to exactly how you like your system.  So I figured this would be a good time to upgrade to Ubuntu 8.10 (previously I ran 8.04).  After getting my O/S exactly how I like it, I installed VMware Workstation 6.5 and thankfully was able to recover my VMDK from my failed disk (more details in another blog later) and it started up just fine.   But, for some reason some of my keys were not working, first thing I noticed was Ctrl-Alt-Ins didn&#8217;t work (the alternative to Ctrl-Alt-Del for Windows logons).  Luckily, Duncan over at <a href="http://www.yellow-bricks.com" target="_blank">Yellow-Bricks</a> already hit this hurdle and posted a <a href="http://www.yellow-bricks.com/2008/11/19/vmware-workstation-ubuntu-ctrl-alt-ins-not-working/" target="_blank">blog</a> on how to resolve.  Thanks Duncan!



From Yellow-Bricks.com&#8230;.

I just noticed that when running a VM on VMware Workstation 6.5 and Ubuntu 8.10(but this problem probably also occurs on other non-Windows OS’es), you can’t use the arrow keys. But also ctrl-alt-ins isn’t working, which is annoying cause you would have to do it with the mouse. And no arrow keys also means that you can’t browse through your command-line history in Windows or Linux for that matter. Luckily there are two work arounds:

  1. sudo gedit /etc/vmware/config
  2. add the following to end of the file and save the file when done:
  
    xkeymap.nokeycodeMap = true
  3. If that doesn’t work try adding the following:
  
    xkeymap.keycode.108 = 0×138 # Alt_R
  
    xkeymap.keycode.106 = 0×135 # KP_Divide
  
    xkeymap.keycode.104 = 0×11c # KP_Enter
  
    xkeymap.keycode.111 = 0×148 # Up
  
    xkeymap.keycode.116 = 0×150 # Down
  
    xkeymap.keycode.113 = 0×14b # Left
  
    xkeymap.keycode.114 = 0×14d # Right
  
    xkeymap.keycode.105 = 0×11d # Control_R
  
    xkeymap.keycode.118 = 0×152 # Insert
  
    xkeymap.keycode.119 = 0×153 # Delete
  
    xkeymap.keycode.110 = 0×147 # Home
  
    xkeymap.keycode.115 = 0×14f # End
  
    xkeymap.keycode.112 = 0×149 # Prior
  
    xkeymap.keycode.117 = 0×151 # Next
  
    xkeymap.keycode.78 = 0×46 # Scroll_Lock
  
    xkeymap.keycode.127 = 0×100 # Pause
  
    xkeymap.keycode.133 = 0×15b # Meta_L
  
    xkeymap.keycode.134 = 0×15c # Meta_R
  
    xkeymap.keycode.135 = 0×15d # Menu

Thanks goes out to AlexPX and Johannes for pointing us out to this <a onclick="javascript:pageTracker._trackPageview('/outbound/article/communities.vmware.com');" href="http://communities.vmware.com/thread/177321?tstart=0">solution</a>. There’s also a <a onclick="javascript:pageTracker._trackPageview('/outbound/article/kb.vmware.com');" href="http://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&docType=kc&externalId=1007439&sliceId=1&docTypeID=DT_KB_1_1&dialogID=4954271&stateId=0%200%202420769">KB article</a> on this one I just noticed.