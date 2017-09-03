---
id: 504
title: Cloning a Physical Linux PC that uses LVM
date: 2009-01-21T22:53:17+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=504
permalink: /2009/01/21/cloning-physical-linux-pc-that-uses-lvm/
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
  - "24122"
dsq_thread_id:
  - "5156597039"
categories:
  - Good Reading
tags:
  - clone
  - clonezilla
  - drbl
  - p2v
  - partition
  - pxe
---
I know this isn&#8217;t virtualization related, but a colleague of mine was attempting to clone 20 HP x4600 desktops running RedHat Enterprise Linux 5 and was having a heck of a time.  Using Ghost or Altiris would image the disk but during boot it would get a kernel panic. Reason being, the LVM wasn&#8217;t being copied properly with these tools.  After doing some quick research I recommended using <a href="http://www.clonezilla.org" target="_blank">Clonezilla</a>, an open source tool that has support for a number of different partition types, including most Linux, Windows, Mac and LVM2.

There are two options for Clonezilla, a Live edition which boots via CD (or local install) and allows a disk to disk copy or even partition to partition copy.  The other edition is SE, which includes a <a href="http://drbl.sf.net/" target="_blank">DRBL</a> server and allows multicasting of the cloning &#8211; basically allowing you to image multiple desktops at the same time from a single source.

As I type this, I&#8217;m thinking of a cool use for this product. Because ESX guests support PXE, you can connect to a DRBL server and do a quick and easy P2V of your Linux based machines.  Perhaps I should test this on my own! (Maybe P2V a Mac to ESX?)