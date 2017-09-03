---
id: 510
title: USB On Your Virtual Machine
date: 2009-01-24T13:01:08+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=510
permalink: /2009/01/24/usb-on-your-virtual-machine/
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
  - "9846"
dsq_thread_id:
  - "5156590043"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Hyper-V
tags:
  - anywhereusb
  - digi
  - fabulatech
  - network
  - usb
  - virtual machine
---
<a href="http://www.ntpro.nl/blog/archives/897-Passing-USB-devices-to-the-Virtual-Machines.html" target="_blank">Eric Sloof</a> recently wrote about FabulaTech, which has a product called USB Over Network. This is a very nice software based client/server application that turns a PC with a USB device connected into a USB host &#8211; you can then install the client piece on your Virtual Machine to connect to the hosted USB connection.<img class="alignright" title="anywhereusb" src="http://www.digi.com/images/products/prd_usb_anywhereusb.jpg" alt="" width="170" height="170" />

Digi also has a product called <a href="http://www.digi.com/products/usb/anywhereusb.jsp" target="_blank">AnywhereUSB</a>, it pretty much does the same thing but without the need of a host machine, you plug your USB device into the AnywhereUSB appliance (very small 5 port USB hub) and install the client piece on your Virtual Machine, the connection is made over a 10/100 ethernet line.  I&#8217;ve used a couple dozen of these for software that requires a USB License Key, never having a problem with any of them.