---
id: 1039
title: VMware Workstation 7 Tech Preview
date: 2009-09-25T17:02:01+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=1039
permalink: /2009/09/25/vmware-workstation-7-tech-preview/
redirect_from: /wp/2009/09/25/vmware-workstation-7-tech-preview/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
aktt_tweeted:
  - "0"
views:
  - "4455"
dsq_thread_id:
  - "5156595080"
categories:
  - Workstation
tags:
  - tech preview
  - vmware workstation
  - workstation
---
**Update** &#8211; Since Workstation 7 has now hit RC and is publicly available I can repost this blog!  Download the RC for yourself and check out the forums at <a href="http://communities.vmware.com/community/beta/workstation" target="_blank">http://communities.vmware.com/community/beta/workstation</a>

A couple weeks ago I was sent an e-mail about a VMware Workstation Technology Preview.  I particularly love these tech previews, mainly because they are great previews of where ESX is going (remember Record/Replay -> FT).

Here is a short list of enhancements found in Workstation 7:

  * Aero support for Windows 7 and Vista Guests!
  * Windows 7 support (as a Host and Guest OS)
  * OpenGL and Shader Model 3.0 support for Windows guests
  * Create guests with Multi-core or 4-way CPUs and up to 32GB of Memory
  * Download VMware vSphere 4 and install ESX as a guest OS to try out the latest features.
  * Dynamically Download the latest VMware Tools package only when you need it.
  * Print from your VM without installing printer drivers. Virtual Printing courtesy of our friends at ThinPrint.
  * Automatically create snapshots on scheduled intervals with AutoProtect.
  * Secure your Virtual Machines with 256-bit encryption.
  * Remote Replay Debugging and other advanced development features
  * ALSA Sound support on Linux hosts enables multiple VMs to play &#8220;music&#8221; concurrently.
  * Instantly pause a VM to free up system resources or dedicate horsepower to other running VMs.
  * The highly acclaimed Linux Virtual Network Editor user interface has been implemented for Windows users.

<a rel="attachment wp-att-1040" href="https://www.vmwaretips.com/wp/wp-content/uploads/2009/09/vmws7.png"><img class="alignright size-medium wp-image-1040" style="border: 0pt none; margin: 3px;" title="vmws7" src="https://www.vmwaretips.com/wp/wp-content/uploads/2009/09/vmws7-300x251.png" alt="" width="300" height="251" srcset="https://www.vmwaretips.com/wp/wp-content/uploads/2009/09/vmws7-300x251.png 300w, https://www.vmwaretips.com/wp/wp-content/uploads/2009/09/vmws7.png 666w" sizes="(max-width: 300px) 100vw, 300px" /></a>Some of the biggest enhancements not listed here include Multi-core and Four-way SMP support.  You can now specify how many physical processors and how many cores per processor right from GUI (this would be nice in ESX, right now you must manually edit the VMX file!).

Another would be the support for up to 32GB of RAM in a Virtual Machine and the ability to Pause a Virtual Machine.

**Pause a Virtual Machine** — Should not be confused with suspending a guest operating system. Pausing a virtual machine frees up system resources that can be dedicated to other virtual machines or operations by the host operating system. Pausing a virtual machine (available from the menu only) immediately halts the operation of a virtual machine.

Another big improvement is with 3D Graphics, OpenGL 2.1 and Shader Model 3.0 support is now available for Windows XP virtual machines.

**3D Graphics Improvements** — OpenGL 2.1 and Shader Model 3.0 support is now available for Windows XP virtual machines. The XPDM graphics driver works with Windows XP, Windows Vista, and Windows 7. However, only Windows XP virtual machines install a graphics driver by default.

This also means you&#8217;ll get Aero Glass support in Windows Vista and Windows 7.

This is some exciting stuff coming to the Workstation product line,  wouldn&#8217;t mind seeing some of this incorporated into ESX.  One thing I did notice, Record/Replay still only supports 1 vCPU, sorry guys!