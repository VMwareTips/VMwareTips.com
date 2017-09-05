---
id: 5
title: Changing Service Console IP Address in ESX 3.5
date: 2008-09-12T08:11:46+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=5
permalink: /2008/09/12/changing-service-console-ip-address-in-esx-35/
redirect_from: /wp/2008/09/12/changing-service-console-ip-address-in-esx-35/
redirect_from: /wp/2008/09/12/changing-service-console-ip-address-in-esx-35/
views:
  - "106981"
ratings_users:
  - "2"
ratings_score:
  - "10"
ratings_average:
  - "5"
dsq_thread_id:
  - "6115519017"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Networking
  - VMware
tags:
  - change ip
  - gateway
  - ip
  - route
  - service console
  - vswif
---
Actually this is not that difficult, but remember you will require console access to the server. Be sure to put the machine in Maintenance Mode then Disconnect it from Virtual Center. Then connect to the console of the ESX host;

<!--more-->

  1. First we need to remove the old IP, the easiest way is to delete the vswif interface
      * esxcfg-vswif -d vswif0
          * replace vswif0 with the interface you&#8217;d like to remove
  2. Then we need to create a new vswif interface with our new IP address
      * esxcfg-vswif -a vswif0 -p Service\ Console -i 10.1.1.1 -n 255.255.255.0 -b 10.1.1.255
          * replace vswif0 with the interface you&#8217;d like to use
          * replace Service\ Console with the name of your Service Console portgroup (this is the default)
          * -i reflects your new IP
          * -n reflects your subnet
          * -b reflects your broadcast
  3. Now we need to update our default gateway
      * This is a simple change to the /etc/sysconfig/network file
  4. One last thing you&#8217;ll want to do after changing your gateway is reset the vswif interface, this will ensure it is connected as well as generate the new default gateway.
      * esxcfg-vswif -s vswif0 (this will disable the vswif0 interface)
      * esxcfg-vswif -e vswif0 (this will enable the vswif0 interface)

That&#8217;s it&#8230;. Now do NOT forget to update DNS and your HOSTS files, then I would suggest doing a ipconfig /flushdns on your VirtualCenter server before you attempt to re-connect the Host in VirtualCenter.

<span style="color: #ff0000;"><strong>Interesting news&#8230; If you change your Service Console IP and your a host managed by VirtualCenter, SVMotion could stop working. The resolution I found was to put your host(s) into maintenance mode, disconnect, remove and re-add them. This will re-install the VC Agent and reconnect verifying the new IP, and SVMotion will work again.  Duncan Epping over at yellow-bricks.com has also seen this and has a similar resolution listed on his website (<a href="http://www.yellow-bricks.com/2008/09/29/storage-vmotion-fails-after-service-console-ip-change/">http://www.yellow-bricks.com/2008/09/29/storage-vmotion-fails-after-service-console-ip-change/</a>), it also includes a change to the VC database, but we both did not need this step for it to work.</strong></span>
