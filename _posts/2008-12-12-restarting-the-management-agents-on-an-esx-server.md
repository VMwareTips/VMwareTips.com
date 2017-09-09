---
id: 350
title: Restarting the Management Agents on an ESX Server
date: 2008-12-12T14:13:51+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=350
permalink: /2008/12/12/restarting-the-management-agents-on-an-esx-server/
redirect_from: /wp/2008/12/12/restarting-the-management-agents-on-an-esx-server/
ratings_users:
  - "2"
ratings_score:
  - "5"
ratings_average:
  - "2.5"
views:
  - "51975"
dsq_thread_id:
  - "5158133827"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - VMware
tags:
  - agents
  - drs
  - ha
  - mgmt-service
  - VMware
  - vpxa
---
It sometimes happens, you see errors about DRS not being able to apply resource settings, most likely do to an invalid fault.  Well, the quick and easy fix for this (and most other common ESX/VC related issues) is to simply restart the Management Agents on your ESX host.



### Restarting the Management agents on ESX Server 3.x

<div>
  To restart the management agents on ESX Server 3.x:
</div>

  1. <div>
      Login to your ESX Server as <span style="font-size: x-small; font-family: Courier New;">root</span> from either an SSH session or directly from the console of the server.
    </div>

  2. <div>
      Type <span style="font-size: x-small; font-family: Courier New;">service mgmt-vmware restart</span>.<br /> <strong>Caution</strong>: Ensure Automatic Startup/Shutdown of virtual machines is disabled before running this command or you risk rebooting the virtual machines.  For more information, see <a href="http://kb.vmware.com/kb/1003312" target="_blank">Restarting hostd (mgmt-vmware) on ESX Server Hosts Restarts Hosted Virtual Machines Where Virtual Machine Startup/Shutdown is Enabled (1003312)</a>.
    </div>

  3. <div>
      Press Enter.
    </div>

  4. <div>
      Type <span style="font-size: x-small; font-family: Courier New;">service vmware-vpxa restart</span>.
    </div>

  5. <div>
      Press Enter.
    </div>

  6. <div>
      Type <span style="font-size: x-small; font-family: Courier New;">logout</span> and press Enter to disconnect from the ESX Server.
    </div>

<div>
  If this process is successful, it appears as:
</div>

<div>
  <span style="font-size: x-small; font-family: Courier New;">[root@server]# service mgmt-vmware restart<br /> Stopping VMware ESX Server Management services:<br /> VMware ESX Server Host Agent Watchdog                   [  <span style="color: #000000;">OK</span> ]<br /> VMware ESX Server Host Agent                            [  <span style="color: #000000;">OK </span> ]<br /> Starting VMware ESX Server Management services:<br /> VMware ESX Server Host Agent (background)               [  <span style="color: #000000;">OK</span> ]<br /> Availability report startup (background)                [  <span style="color: #000000;">OK</span> ]<br /> [root@server]# service vmware-vpxa restart<br /> Stopping vmware-vpxa:                                      [  <span style="color: #000000;">OK</span> ]<br /> Starting vmware-vpxa:                                      [  <span style="color: #000000;">OK</span> ]<br /> [root@server]#<br /> </span>
</div>

<div>
  <strong>Note</strong>: If there are failures listed:
</div>

  * <div>
      The most common reason for a stopping task to fail is that the service is not started.
    </div>

  * <div>
      If a starting task fails for the mgmt-vmware service, see <a href="http://kb.vmware.com/kb/1003561" target="_blank">Troubleshooting the VMware ESX Server Management Service when it will not start (1003561)</a>.
    </div>

  * <div>
      If a starting task fails for the vmware-vpxa service, see <a title="Troubleshooting the VirtualCenter Agent Service when it will not start (1006128)" href="http://kb.vmware.com/kb/1006128" target="_blank">Troubleshooting the VirtualCenter Agent Service when it will not start (1006128)</a>.
    </div>

### Restarting the Management agents on ESX Server 3i

<div>
  To restart the management agents on ESX Server 3i:
</div>

  1. <div>
      Connect to the console of your ESX Server.
    </div>

  2. <div>
      Press F2 to customize the system.
    </div>

  3. <div>
      Login as <span style="font-size: x-small; font-family: Courier New;">root</span>.
    </div>

  4. <div>
      Using the Up/Down arrows navigate to <strong>Restart Management Agents</strong>.
    </div>

  5. <div>
      Press Enter.
    </div>

  6. <div>
      Press F11 to restart the services.
    </div>

  7. <div>
      When the service has been restarted, press Enter.
    </div>

  8. <div>
      Press Esc to logout of the system.
    </div>

<div>
  The following dialogue indicates the process is complete:
</div>

<p style="text-align: center;">
  <img class="aligncenter" title="esxi mgmt restart" src="http://kb.vmware.com/Platform/Publishing/images/1003490_3irestart.JPG" alt="" width="470" />
</p>