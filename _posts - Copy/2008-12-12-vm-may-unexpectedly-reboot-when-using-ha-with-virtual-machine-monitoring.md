---
id: 348
title: VM may unexpectedly reboot when using HA with Virtual Machine Monitoring
date: 2008-12-12T14:08:32+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=348
permalink: /2008/12/12/vm-may-unexpectedly-reboot-when-using-ha-with-virtual-machine-monitoring/
redirect_from: /wp/2008/12/12/vm-may-unexpectedly-reboot-when-using-ha-with-virtual-machine-monitoring/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "8694"
dsq_thread_id:
  - "5157916424"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - VMware
tags:
  - ha
  - reboot
  - vmm
  - VMware
---
As mentioned on <a href="http://blog.scottlowe.org/2008/12/12/vmware-ha-problem-with-update-3/" target="_blank">Scott Lowe</a> and <a href="http://www.yellow-bricks.com/2008/12/12/vms-may-unexpectedly-reboot-when-using-vmware-ha-with-virtual-machine-monitoring/" target="_blank">Duncan Epping&#8217;s</a> sites, an issue has been uncovered with VMware ESX 3.5 Update 3 in regards to Virtual Machines rebooting when using VMware HA with Virtual Machine Monitoring enabled.

<!--more-->

**To stay up to date on this VMware KB, please visit their website; <a href="http://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&docType=kc&externalId=1007899&sliceId=1&docTypeID=DT_KB_1_1&dialogID=9798685&stateId=1%200%209806084" target="_blank">VMware KB 1007899</a>**

**Symptoms:
  
** Virtual Machines may unexpectedly reboot after a VMotion migration to an ESX 3.5 Update 3 Host OR after a Power On operation on an ESX 3.5 Update 3 Host, when VMware HA feature with Virtual Machine Monitoring is active.

**Purpose:
  
** <span lang="EN">A virtual machine may reboot itself when the following conditions exist:</span>

  * <span lang="EN"><span lang="EN"> 
    
    <div>
      Virtual Machine is running on ESX 3.5 Update 3 Host, either by virtue of VMotion or a Power On operation, and
    </div>
    
    <p>
      </span></span></li> 
      
      <li>
        <span lang="EN"><span lang="EN"> 
        
        <div>
          <span lang="EN"><span lang="EN">Host has VMware HA enabled with &#8220;Virtual Machine Monitoring&#8221; option active.</span></span>
        </div>
        
        <p>
          </span></span></li> </ul> 
          
          <p>
            Virtual Machine monitoring is dependent on VMware tools heartbeats to determine the state of the Virtual Machines.
          </p>
          
          <p>
            <span lang="EN">With ESX Server 3.5 Update 3 after a VMotion or Power On operation, host agent running on the ESX server may delay sending the heartbeat state of the Virtual Machine to the Host. </span>VMware HA detects this as a failure of the Virtual Machine and attempts to restart the Virtual Machine
          </p>
          
          <p>
            <strong>Resolution:<br /> </strong>To work around this problem:
          </p>
          
          <div>
            <strong>Option 1: Disable Virtual Machine Monitoring </strong>
          </div>
          
          <ol>
            <li>
              <div>
                <span lang="EN">Select the VMware HA cluster and choose Edit Settings from the right-click menu (note that this feature can also be enabled for a new cluster on the VMware HA page of the New Cluster wizard).</span>
              </div>
            </li>
            
            <li>
              <div>
                <span lang="EN">In the Cluster Settings dialog box, select VMware HA in the left column.</span>
              </div>
            </li>
            
            <li>
              <div>
                <span lang="EN">Un-Check the Enable virtual machine monitoring check box.</span>
              </div>
            </li>
            
            <li>
              <div>
                <span lang="EN">Click OK.</span>
              </div>
            </li>
          </ol>
          
          <div dir="ltr">
            <strong>Option 2: Set hostd hearbeat delay to 0</strong>
          </div>
          
          <ol>
            <li>
              <div>
                Disconnect the host from VC (<span lang="EN">Right click on host in VI Client and select &#8220;Disconnect&#8221; )</span>
              </div>
            </li>
            
            <li>
              <div>
                Login as root to the ESX Server with SSH.
              </div>
            </li>
            
            <li>
              <div>
                Using a text editor such as <span style="font-family: Courier New;">nano </span>or <span style="font-family: Courier New;">vi</span>, edit the file <span style="font-family: Courier New;">/etc/vmware/hostd/config.xml</span>
              </div>
            </li>
            
            <li>
              <div>
                Set the &#8220;heartbeatDelayInSecs&#8221; tag under &#8220;vmsvc&#8221; to 0 seconds as shown here:<br /> <span style="font-family: Courier New;"><vmsvc><br /> <heartbeatDelayInSecs>0</heartbeatDelayInSecs><br /> <enabled>true</enabled><br /> </vmsvc></span>
              </div>
            </li>
            
            <li>
              <div>
                Restart the management agents for this change to take effect.  See <a href="http://vmwaretips.com/wp/2008/12/12/restarting-the-management-agents-on-an-esx-server/" target="_blank">Restarting the Management agents on an ESX Server</a>
              </div>
            </li>
            
            <li>
              <div>
                <span lang="EN">Reconnect the host in VC ( Right click on host in VI Client and select &#8220;Connect&#8221; )</p> 
                
                <p>
                  </span></div> </li> </ol>