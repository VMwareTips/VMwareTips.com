---
id: 1053
title: Before Host Profiles there was vicfg-cfgbackup.pl
date: 2009-10-12T12:36:35+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1053
permalink: /2009/10/12/before-host-profiles-there-was-vicfg-cfgbackuppl/
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
  - "21229"
dsq_thread_id:
  - "5156595036"
categories:
  - 'Backup &amp; Recovery'
  - ESXi 3.5 Tips
  - vSphere
tags:
  - enterprise plus
  - esxi
  - host profiles
  - rcli
  - vicfg-cfgbackup
  - vsphere
---
This last weekend I was reminded of a RCLI command that creates a backup of your ESXi Host configuration.  A client had an ESXi host where the USB drive failed.  The system didn&#8217;t entirely crash, it pinged so HA didn&#8217;t kick-in however hostd and vpxa weren&#8217;t responding so management from vCenter was impossible. Performing a reboot of the host proved it was a USB failure when it failed to boot.

So, HA kicked in finally when the host was powered off &#8211; however the remaining hosts in their cluster did not have adequate resources to power _everything_ back on.  We needed to get this failed ESX host back online and quick!

Brought in new USB stick with fresh ESXi 4.0 installed, plugged in and powered up.  In the TUI configured the Management Port IP address/gateway/DNS, etc.    But now what, all of the (NFS) Datastores, vSwitch configuration and advanced settings were toast&#8230;and they didn&#8217;t have Enterprise Plus.

Say Hello to vicfg-cfgbackup.pl &#8212; a RCLI command which could be found in the vMA.  This utility will allow you to create a backup and restore a full ESXi configuration.  Luckily we had this (backup) command running on a nightly basis so we knew the configuration was complete.  A simply command and the host was online.

Seeing that ESX is going to be phased out, this RCLI command is a valid alternative for those ESXi users that do not have Enterprise Plus licensing.

> <p class="style1">
>   The commands vicfg-cfgbackup.pl (esxcfg-cfgbackup.pl) allow you to backup and restore the configuration of your ESXi host.
> </p>
> 
> <p class="style1">
>   <span class="style4"><strong><span style="color: #ff0000;">To backup </span></strong></span>the host you would run the command.
> </p>
> 
> <p class="style2">
>   vicfg-cfgbackup.pl &#8211;server <server_name> -s <backup_file_name>
> </p>
> 
> <p class="style1">
>   <span class="style4"><strong><span style="color: #ff0000;">To restore</span></strong></span> your backup configuration to your host you would run. This will cause the host to reboot once the process is complete. <strong>NOTE:</strong> The host must be in Maintenance Mode for this to work. The backup configuration must also match the patch level of the ESXi install. You can add a -f to force if needed.
> </p>
> 
> <p class="style2">
>   vicfg-cfgbackup.pl &#8211;server <server_name> -l <backup_file_name>
> </p>