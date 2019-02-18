---
id: 2908
title: Changing ESXi Hostname on an EVO:RAIL Appliance
date: 2016-01-13T12:24:47+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=2908
permalink: /2016/01/13/changing-esxi-hostname-on-an-evorail/
redirect_from: /wp/2016/01/13/changing-esxi-hostname-on-an-evorail/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "32099"
categories:
  - EVO:RAIL
tags:
  - change hostname
  - EMC
  - esxi
  - EVO
  - evo:rail
  - hostname
  - hyper converged
  - rail
  - vspex
  - vspex blue
---
The other day I did a VSPEX Blue (EMC&#8217;s flavor of EVO:RAIL Appliance) install for a customer that couldn&#8217;t conform to the hostname standards set forth by the EVO:RAIL Installation Wizard. After a little bit of digging and work I was able to change the hostnames and get everything working like it came from the factory. You simply cannot just change the ESXi hostname, you also need to modify EVO:RAIL Manager so things like health reporting actually function.

So, how do we do this?

First a quick warning&#8230; no guarantees :)  this worked for me and my customer and has been reported in a couple KB articles but due to the nature of EVO:RAIL you may want to open a ticket with your OEM Vendor for help on doing this.

It&#8217;s important to note two things&#8230; 1) if you&#8217;re building out a new EVO:RAIL Appliance and know you need to use custom hostnames, avoid putting in a DNS Server entry during installation &#8211; this will force the unit to use a local dnsmasq service for name resolution and will make it easier for us to modify the hostnames.  and 2) you should only place a single ESXi host into maintenance mode/change hostname at a time, this is important in allowing workloads to stay online.

And now on to the steps&#8230;

1.) On the vCenter Server Appliance modify the dnsmasq add-on file, by using _vi /var/lib/vmware-marvin/dnsmasq/hosts_ &#8211; modify this file to reflect the new hostname(s)

2.) Place the first ESXi host into maintenance mode, then remove it from the vCenter inventory

3.) Add new hostname(s) to the local file on the vCenter Server Appliance, by using _vi /etc/hosts_ &#8211; This is a temporary change to avoid any inconsistencies, we will remove these later

4.) Perform ESXi hostname change, I found the easiest way to do this was via esxcli by SSH&#8217;ing directly to the host

<a href="https://www.vmwaretips.com/wp-content/uploads/2016/01/esxi-hostname-change.jpg" target="_blank"><img class="wp-image-2909 alignnone" style="margin-top: 0px; margin-bottom: 0px; border: 0px;" title="esxi-hostname-change" src="https://www.vmwaretips.com/wp-content/uploads/2016/01/esxi-hostname-change-300x123.jpg" alt="" width="450" srcset="https://www.vmwaretips.com/wp-content/uploads/2016/01/esxi-hostname-change-300x123.jpg 300w, https://www.vmwaretips.com/wp-content/uploads/2016/01/esxi-hostname-change.jpg 593w" sizes="(max-width: 300px) 100vw, 300px" /></a>

5.) Add new hostname to vCenter Server through vSphere (Web) Client, and exit Maintenance Mode

6.) Go to Step #2 for any additional ESXi hosts you&#8217;d like to change

7.) Restart the dnsmasq service on the vCenter Server Appliance; _/etc/init.d/vmware-dnsmasq restart_

8.) Clean up the /etc/hosts file by removing the changes you made in Step #3

That should be it for the changing of the ESXi hostname.  However, you may notice now that the Health tab in EVO:RAIL Manager isn&#8217;t looking too happy.
  
This is because of two things, obviously 1) the hostname change but also 2) the morefId changed which breaks the connection between EVO:RAIL Manager and vCenter.

<a href="https://www.vmwaretips.com/wp-content/uploads/2016/01/evorailmanager.jpg" target="_blank"><img class="wp-image-2913 alignnone" title="evorailmanager" src="https://www.vmwaretips.com/wp-content/uploads/2016/01/evorailmanager.jpg" alt="" width="450" srcset="https://www.vmwaretips.com/wp-content/uploads/2016/01/evorailmanager.jpg 498w, https://www.vmwaretips.com/wp-content/uploads/2016/01/evorailmanager-300x139.jpg 300w" sizes="(max-width: 498px) 100vw, 498px" /></a>

So, let&#8217;s go fix EVO:RAIL Manager.

1.) On the vCenter Server Appliance we&#8217;ll need to first determine the new morefId of the ESXi host(s).  SSH into the vCenter Server Appliance and run the following command; _sudo /opt/vmware/vpostgres/9.0/bin/psql -d VCDB vc -c&#8221;select id, dns\_name from VPX\_HOST;&#8221;_

<a href="https://www.vmwaretips.com/wp-content/uploads/2016/01/evo-psql.jpg" target="_blank"><img class="alignnone  wp-image-2917" style="margin: 0px; border: 0px;" title="evo-psql" src="https://www.vmwaretips.com/wp-content/uploads/2016/01/evo-psql.jpg" alt="" width="450" height="93" srcset="https://www.vmwaretips.com/wp-content/uploads/2016/01/evo-psql.jpg 853w, https://www.vmwaretips.com/wp-content/uploads/2016/01/evo-psql-300x61.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" /></a>

As you can see, our newname-esx01.vlab.local host has a new morefId of 26.

2.) Change the morefId and hostname by running _vi /var/lib/vmware-marvin/hosts.json_ &#8211; change the morefId and hostname for the host(s) you&#8217;d like to modify

<a href="https://www.vmwaretips.com/wp-content/uploads/2016/01/hosts_json.jpg" target="_blank"><img class="alignnone  wp-image-2919" style="border: 0px; margin: 0px;" title="hosts_json" src="https://www.vmwaretips.com/wp-content/uploads/2016/01/hosts_json.jpg" alt="" width="450" height="60" srcset="https://www.vmwaretips.com/wp-content/uploads/2016/01/hosts_json.jpg 1129w, https://www.vmwaretips.com/wp-content/uploads/2016/01/hosts_json-300x39.jpg 300w, https://www.vmwaretips.com/wp-content/uploads/2016/01/hosts_json-1024x136.jpg 1024w" sizes="(max-width: 450px) 100vw, 450px" /></a>

3.) Restart the EVO:RAIL Manager process with _/etc/init.d/vmware-marvin restart_

4.) Check EVO:RAIL Manager Health and all should be good!

<a href="https://www.vmwaretips.com/wp-content/uploads/2016/01/marvin-newhost.jpg" target="_blank"><img class="alignnone  wp-image-2920" style="border: 0px; margin: 0px;" title="marvin-newhost" src="https://www.vmwaretips.com/wp-content/uploads/2016/01/marvin-newhost.jpg" alt="" width="450" srcset="https://www.vmwaretips.com/wp-content/uploads/2016/01/marvin-newhost.jpg 1013w, https://www.vmwaretips.com/wp-content/uploads/2016/01/marvin-newhost-300x74.jpg 300w" sizes="(max-width: 1013px) 100vw, 1013px" /></a>

It&#8217;s as easy as that. So, if your organization has a specific hostname requirement that cannot be met by the EVO:Rail Installation Wizard, have no fear&#8230; you can always modify after the build if needed!

Say you did an install without specifying a corporate DNS server, and you&#8217;d like to go back and add one after the fact all you need to do is add an entry into the /etc/dnsmasq.conf file. You can even add multiples.

_server=IP.ADDRESS.OF.DNS.SERVER
  
server=IP.ADDRESS.OF.2ND.DNS.SERVER _

Then you need to restart the dnsmasq service,  _/etc/init.d/vmware-dnsmasq restart_

There you go, much better :)