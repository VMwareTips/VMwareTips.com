---
id: 1087
title: VMware View 4 Available for Download
date: 2009-11-25T11:37:25+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=1087
permalink: /2009/11/25/vmware-view-4-available-for-download/
aktt_notify_twitter:
  - yes
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
aktt_tweeted:
  - 1
views:
  - 6050
dsq_thread_id:
  - 5156592418
categories:
  - View
tags:
  - pcoip
  - thin client
  - vmware view 4
---
For my last post before leaving for the holiday I&#8217;d like to announce that VMware View 4 is available for download.

One prerequisite is that you&#8217;re running on <a href="http://vmwaretips.com/wp/2009/11/25/vmware-vsphere-40-update-1-released/" target="_blank">VMware vSphere 4.0 Update 1</a> or at least Update 3 of the VI 3.5 Suite.

The most anticipated feature (IMO) with View 4 is full PCoIP support, which brings a full rich desktop experience regardless of the connection type (LAN or WAN). This truly means that virtualized desktops are a viable option for almost any environment now.  Another amazing feature of PCoIP is the ability to support up to four monitors so now even my desktop could be a virtual one.

Here are a few of the other new features found in the <a href="http://www.vmware.com/support/view40/doc/releasenotes_viewmanager40.html" target="_blank">VMware View 4 Release Notes</a>:

> **VMware View 4  Release Notes
  
> What&#8217;s New**
> 
> **Enhanced single sign-on** – The **Log in as current user** feature is integrated with Active Directory and smart cards to help simplify the process of logging in to a VMware View desktop.
> 
> **Restricted entitlements** – Administrators can control user access to virtual desktops based on the View Connection Server being used for authentication.****
> 
> **Smart card policies** – Administrators can set group policies to force desktop disconnection and require reconnection when users remove smart cards.****
> 
> **Domain filtering** – You can use <tt>vdmadmin.exe</tt> to control the accessibility of domains and traverse trust relationships more quickly.
> 
> You can cleanly delete View desktops using scripts.
> 
> You can log in to View desktops using user principal names (UPN).
> 
> You can explicitly configure IP addresses to override those supplied by the View Agent when accessing a desktop.
> 
> Mixed Active Directory and Kerberos authentication is supported.

From viewing the <a href="http://www.vmware.com/resources/compatibility/search.php?action=search&deviceCategory=vdm&productId=2&advancedORbasic=advanced&maxDisplayRows=50&key=&release[]=82&datePosted=-1&partnerId[]=-1&filterByPCoIP=1&rorre=0" target="_blank">VMware HCL</a> it appears that there are a number of Thin Clients that already have full support for PCoIP and View 4.

Another topic of discussion on Twitter was the Guest O/S support matrix, there were concerns that Windows 7 wouldn&#8217;t be supported as a Guest.  From what I&#8217;ve read in <a href="http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1015591" target="_blank">KB 1015591</a> it appears that there is full support for Windows 95/98, Windows 2000 Professional, Windows XP Professional, Windows Vista Ultimate, Business or Enterprise, and Windows 7.

So, go <a href="http://downloads.vmware.com/d/info/desktop_downloads/vmware_view/4_0" target="_blank">download</a> your trial today and experience a true rich experience that PCoIP can provide.