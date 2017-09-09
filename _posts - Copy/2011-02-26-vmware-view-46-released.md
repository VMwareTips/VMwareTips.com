---
id: 1295
title: VMware View 4.6 Released
date: 2011-02-26T11:00:44+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1295
permalink: /2011/02/26/vmware-view-46-released/
redirect_from: /wp/2011/02/26/vmware-view-46-released/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "2061"
categories:
  - View
tags:
  - desktop
  - pcoip
  - rdp
  - vdi
  - view
  - virtualized desktops
  - vmware view
  - vmware view 4
---
**vm**ware just dropped another dot release to their flagship desktop virtualization product, View. **vm**ware View 4.6 is now officially available for download. Although this release is mostly a ton of bug fixes rolled up into a single package, there are a number of great new features including PCoIP support when going through a Security Server as well as Sync Support for iPhone and iPad users.

Like I mention above, the biggest feature for me is now the ability to do PCoIP through the Security Server. Before this functionality was available you were either required to use RDP or you must VPN into the network where the View Connection Broker server was located, but this typically wouldn&#8217;t work because of the added latency the VPN tunnel would create.

All of the updates in this release can be found in the official <a href="http://www.vmware.com/support/view46/doc/view-46-release-notes.html" target="_blank">release notes</a>, however here are the hot what&#8217;s new items:

  * **Security servers can now accommodate PCoIP connections** &#8211; Security servers now include a PCoIP Secure Gateway component. The PCoIP Secure Gateway connection offers the following advantages: 
      * The only remote desktop traffic that can enter the corporate data center is traffic on behalf of a strongly authenticated user.
      * Users can access only the desktop resources that they are authorized to access.
      * No VPN is required, as long as PCoIP is not blocked by any networking component.
      * Security servers with PCoIP support run on Windows Server 2008 R2 and take full advantage of the 64-bit architecture.****
  * **Enhanced USB device compatibility** &#8211; View 4.6 supports USB redirection for syncing and managing iPhones and iPads with View desktops. This release also includes improvements for using USB scanners, and adds to the list of USB printers that you can use with thin clients. For more information, see the list of <a href="http://www.vmware.com/support/view46/doc/view-46-release-notes.html#fixed_client" target="_blank">View Client</a> resolved issues.
  * **Keyboard mapping improvements** &#8211; Many keyboard-related issues have been fixed. For more information, see the list of <a href="http://www.vmware.com/support/view46/doc/view-46-release-notes.html#fixed_client" target="_blank">View Client</a> resolved issues.
  * **New timeout setting for SSO users** &#8211; With the single-sign-on (SSO) feature, after users authenticate to View Connection Server, they are automatically logged in to their View desktop operating systems. This new timeout setting allows administrators to limit the number of minutes that the SSO feature is valid for. 
      * For example, if an administrator sets the time limit to 10 minutes, then 10 minutes after the user authenticates to View Connection Server, the automatic login ability expires. If the user then walks away from the desktop and it becomes inactive, when the user returns, the user is prompted for login credentials. For more information, see the <a href="http://www.vmware.com/pdf/view-46-administration.pdf" target="_blank">VMware View Administration</a> documentation.****
  * **VMware View 4.6 includes more than 160 bug fixes** &#8211; For descriptions of selected resolved issues, see [Resolved Issues](http://www.vmware.com/support/view46/doc/view-46-release-notes.html#fixedissues).****
  * **Experimental support for Microsoft Windows 7 SP1 RC operating systems**