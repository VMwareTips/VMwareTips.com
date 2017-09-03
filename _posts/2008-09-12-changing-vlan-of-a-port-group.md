---
id: 13
title: Changing VLAN of a Port Group
date: 2008-09-12T08:54:59+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=13
permalink: /2008/09/12/changing-vlan-of-a-port-group/
views:
  - "11826"
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
dsq_thread_id:
  - "5156705527"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Networking
  - VMware
tags:
  - portgroup
  - vlan
  - vswitch
---
In the event you need to change the VLAN of any of your Port Groups here is some good instruction on doing just that. Remember, VLANs are configured at the Port Group level and not the vSwitch level. This allows you to trunk as many VLANs you need to your vSwitch&#8217;s then create dedicated Port Groups for each of those Virtual LANs.

<!--more-->

First lets look at our existing configuration;

> [root@dpcrcvmesx1 root]# **esxcfg-vswitch -l**
> 
> Switch Name Num Ports Used Ports Configured Ports MTU Uplinks
  
> vSwitch0 128 51 128 1500 vmnic2,vmnic0,vmnic9,vmnic8,vmnic7,vmnic5
> 
> PortGroup Name VLAN ID Used Ports Uplinks
  
> Network1 902 22 vmnic9,vmnic8,vmnic7,vmnic5,vmnic2,vmnic0
  
> Network0 1 20 vmnic5,vmnic7,vmnic8,vmnic9,vmnic0,vmnic2
  
> **Service Console 6 1 vmnic0,vmnic2,vmnic5,vmnic7,vmnic8,vmnic9**
> 
> Switch Name Num Ports Used Ports Configured Ports MTU Uplinks
  
> vSwitch1 64 19 64 1500 vmnic6,vmnic4,vmnic3,vmnic1
> 
> PortGroup Name VLAN ID Used Ports Uplinks
  
> VMkernel1 930 1 vmnic6,vmnic4,vmnic3,vmnic1
  
> Storage0 900 11 vmnic1,vmnic3,vmnic4,vmnic6
  
> VMkernel 900 1 vmnic6,vmnic4,vmnic3,vmnic1

I&#8217;ve highlighted the Service Console PortGroup because I would like to change the VLAN it uses. This is extremely dangerous to do when remote consoled into the machine (SSH, etc), I&#8217;d highly suggest using a local connection or iLO. I wrote these instructions in addition to the instructions of changing the Service Console IP address because we recently had to do so.

Ok, so now we are going to change the VLAN;

> [root@dpcrcvmesx1 root]# **esxcfg-vswitch -p Service\ Console -v 902 vSwitch0**
> 
> ****
> 
> ****
> 
>   * <span style="font-weight: normal;"><strong>-p represents the PortGroup</strong></span>
>   * <span style="font-weight: normal;"><strong>-v represents the NEW VLAN ID</strong></span>
>   * <span style="font-weight: normal;"><strong>at the end of all esxcfg-vswitch commands you enter the vSwitch your changing</strong></span> ****
> 
> ****

Thats it. Now my Service Console PortGroup is now in VLAN 902, next I will use my instructions for changing the Service Console IP address.