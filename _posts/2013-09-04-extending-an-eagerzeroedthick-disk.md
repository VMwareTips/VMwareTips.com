---
id: 2161
title: Extending an EagerZeroedThick Disk
date: 2013-09-04T09:50:55+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2161
permalink: /2013/09/04/extending-an-eagerzeroedthick-disk/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "2135"
categories:
  - Storage
  - vSphere
tags:
  - eagerzeroedthick
  - extending
  - lazyzeroed
  - vmdk
  - vmkfstools
---
Today a coworker asked me about extending an EagerZeroedThick disk, as they had a customer inform them that extending an EagerZeroedThick disk actually turned it LazyZeroed. Although this is somewhat true, it is not 100% accurate. What actually happens is the extension becomes LazyZeroed but the original portion of the disk still remains EagerZeroedThick. This is actually by design, if you want to extend the VMDK and ensure that it is all EagerZeroedThick you must specify a flag in the vmkfstools command to do so.

> **Extending an EagerZeroedThick VMDK**
> 
> \# vmkfstools -X 10G <span style="text-decoration: underline;">-d eagerzeroedthick</span> /path/to/vmdkfile.vmdk

In the above syntax example it is critical that you specify eagerzeroedthick as the disk format.