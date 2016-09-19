---
id: 459
title: 'Issue: VMware ESX/ESXi SAN I/O Failure'
date: 2009-01-12T22:07:25+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=459
permalink: /2009/01/12/issue-vmware-esxesxi-san-io-failure/
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
  - 13276
dsq_thread_id:
  - 5156589800
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Storage
tags:
  - esx
  - esxi
  - failure
  - fcp
  - fibre channel
  - hung
  - i/o
  - iscsi
  - Storage
---
In the twitter queue today I heard a new VMware KB has been released in regards to a potential SAN failure (FibreChannel and iSCSI).  More information and the most recent updates can be found on the <a href="http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1008130" target="_blank">VMware KB.</a>  I&#8217;ve included a breakdown of the issue and resolution, which can be found below.

<!--more-->

<table border="0" cellspacing="0" cellpadding="0" width="100%">
  <tr>
    <td>
      <table border="0" cellspacing="0" cellpadding="0">
        <tr>
          <td class="tabbar" style="padding-right: 5px; padding-left: 10px; padding-bottom: 1px; padding-top: 2px;">
            <strong>Symptoms</strong><br /> <strong><img src="http://vmwaretips.com/contactcenter/img/sp.gif" border="0" alt="" width="100" height="3" /></strong>
          </td>
          
          <td width="20" height="100%">
             
          </td>
        </tr>
      </table>
    </td>
  </tr>
  
  <tr>
    <td class="tabbar" height="2">
      <img src="http://vmwaretips.com/contactcenter/img/sp.gif" border="0" alt="" width="1" height="2" />
    </td>
  </tr>
  
  <tr>
    <td class="body" style="padding: 10px;">
      <span style="font-family: Courier New;"><span style="font-size: 10pt; font-family: 'Arial','sans-serif';">One or more of the following may be present:</span></span></p> 
      
      <ul>
        <li>
          <div>
            <span style="font-family: Courier New;"><span style="font-size: 10pt; font-family: 'Arial','sans-serif';">VMware ESX or ESXi host might get disconnected form VirtualCenter.<br />  </span></span>
          </div>
        </li>
        
        <li>
          <div>
            <span style="font-family: Courier New;"><span style="font-size: 10pt; font-family: 'Arial','sans-serif';"><span style="font-size: 10pt; font-family: 'Arial','sans-serif';">All paths to the LUNs are in standby state.<br />  </span></span></span>
          </div>
        </li>
        
        <li>
          <div>
            <span style="font-size: 10pt; font-family: 'Arial','sans-serif';"><span style="font-size: 10pt; font-family: 'Arial','sans-serif';">esxcfg-rescan might take a long time to complete or never completes (hung).<br />  </span></span>
          </div>
        </li>
        
        <li>
          <div>
            <span style="font-size: x-small; font-family: Arial;">Error messages matching this pattern are repeated continually in vmkernel:<br /> </span><span style="font-family: Courier New;"><span style="font-size: 10pt; font-family: 'Arial','sans-serif';"><span style="font-family: Courier New;"><date and time> <hostname> vmkernel: <server uptime> cpu6:1177)SCSI: 675: Queue for device vml.<Vol. Dev. ID> has been blocked for 7 seconds.<br /> </span></span><span style="font-family: Courier New;"><span style="font-size: 10pt; font-family: 'Arial','sans-serif';"><span style="font-family: Courier New;"><span style="font-size: 10pt; font-family: 'Arial','sans-serif';"><date and time></span> <hostname> vmkernel: <server uptime> cpu7:1184)SCSI: 675: Queue for device vml.<Vol. Dev. ID> has been blocked for 6399 seconds.</span><br /> </span></span></span><span style="font-size: 10pt; font-family: 'Arial','sans-serif';"> <br /> If you look at log entries previous to the first blocked message, you will see storage events and a failover attempt.<br /> Example:<br /> <span style="font-family: Courier New;"><date and time> <hostname> vmkernel: 31:19:32:26.199 cpu3:3824)Fil3: 5004:  READ error 0xbad00e5<br /> <date and time> <hostname> vmkernel: 31:19:32:29.224 cpu1:3961)StorageMonitor: 196: vmhba0:0:0:0 status = 0/5 0x0 0x0 0x0<br /> <date and time> <hostname> vmkernel: 31:19:32:29.382 cpu2:1144)FS3: 5034: Waiting for timed-out heartbeat [HB state abcdef02 offset 3736576 gen 26 stamp 2748610023852 uuid 4939b0cf-c85aa695-158d-00144f021dd4 jrnl <FB 383397> drv 4.31]<br /> <date and time> <hostname> vmkernel: 31:19:32:29.638 cpu3:1053)<6>qla2xxx_eh_device_reset(1): device reset failed<br /> <date and time> <hostname> vmkernel: 31:19:32:29.638 cpu3:1053)WARNING: SCSI: 4279: Reset during HBA failover on vmhba1:2:1 returns Failure<br /> <date and time> <hostname> vmkernel: 31:19:32:29.638 cpu3:1053)WARNING: SCSI: 3746: Could not switchover to vmhba1:2:1. Check Unit Ready Command returned an error instead of NOT READY for standby controller .<br /> <date and time> <hostname> vmkernel: 31:19:32:29.638 cpu3:1053)WARNING: SCSI: 4622: Manual switchover to vmhba1:2:1 completed unsuccessfully.<br /> <date and time> <hostname> vmkernel: 31:19:32:29.638 cpu3:1053)StorageMonitor: 196: vmhba0:2:1:0 status = 0/1 0x0 0x0 0x0<br /> <date and time> <hostname> vmkernel: 31:19:32:29.640 cpu2:1067)scsi(1): Waiting for LIP to complete&#8230;<br /> <date and time> <hostname> vmkernel: 31:19:32:29.640 cpu2:1067)<6>qla2x00_fw_ready ha_dev_f=0xc<br /> <date and time> <hostname> vmkernel: 31:19:32:30.532 cpu2:1026)StorageMonitor: 196: vmhba0:0:0:0 status = 0/2 0x0 0x0 0x0<br /> <date and time> <hostname> last message repeated 31 times<br /> <date and time> <hostname> vmkernel: 31:19:32:31.535 cpu2:1067)<6>dpc1 port login OK: logged in ID 0x81<br /> <date and time> <hostname> vmkernel: 31:19:32:31.541 cpu2:1067)<6>dpc1 port login OK: logged in ID 0x82<br /> <date and time> <hostname> vmkernel: 31:19:32:31.547 cpu2:1067)<6>dpc1 port login OK: logged in ID 0x83<br /> <date and time> <hostname> vmkernel: 31:19:32:31.568 cpu2:1067)<6>dpc1 port login OK: logged in ID 0x84<br /> <date and time> <hostname> vmkernel: 31:19:32:31.573 cpu2:1067)<6>dpc1 port login OK: logged in ID 0x85<br /> <date and time> <hostname> vmkernel: 31:19:32:31.576 cpu2:1067)<6>dpc1 port login OK: logged in ID 0x86<br /> <date and time> <hostname> vmkernel: 31:19:32:32.531 cpu2:4267)StorageMonitor: 196: vmhba0:0:0:0 status = 0/2 0x0 0x0 0x0<br /> <date and time> <hostname> last message repeated 31 times<br /> <date and time> <hostname> vmkernel: 31:19:32:32.532 cpu1:3973)StorageMonitor: 196: vmhba0:0:0:0 status = 2/0 0x6 0x29 0x0</span></span>
          </div>
        </li>
      </ul>
    </td>
  </tr>
  
  <tr>
    <td>
      <table border="0" cellspacing="0" cellpadding="0">
        <tr>
          <td class="tabbar" style="padding-right: 5px; padding-left: 10px; padding-bottom: 1px; padding-top: 2px;">
            <strong>Resolution</strong><br /> <img src="http://vmwaretips.com/contactcenter/img/sp.gif" border="0" alt="" width="100" height="3" />
          </td>
          
          <td width="20" height="100%">
             
          </td>
        </tr>
      </table>
    </td>
  </tr>
  
  <tr>
    <td class="tabbar" height="2">
      <img src="http://vmwaretips.com/contactcenter/img/sp.gif" border="0" alt="" width="1" height="2" />
    </td>
  </tr>
  
  <tr>
    <td class="body" style="padding: 10px;">
      <div>
        <span style="font-size: x-small; font-family: Arial;">This issue can occur on VMware ESX servers under the following conditions:</span>
      </div>
      
      <ul>
        <li>
          <div>
            <span style="font-size: x-small; font-family: Arial;">Hypervisor version: VMware ESX 3.5 U3.</span>
          </div>
        </li>
        
        <li>
          <div>
            <span style="font-size: x-small; font-family: Arial;">SAN hardware: Active/Passive and Active/Active arrays (Fibre Channel and iSCSI).</span>
          </div>
        </li>
        
        <li>
          <div>
            <span style="font-size: x-small; font-family: Arial;">Trigger: This occurs when VMFS3 metadata updates are being done at the same time failover to an alternate path occurs for the LUN on which the VMFS3 volume resides .</span>
          </div>
        </li>
      </ul>
      
      <div>
        <span style="font-size: x-small; font-family: Arial;">A reboot is required to clear this condition.</span>
      </div>
      
      <div>
        <span style="font-size: x-small; font-family: Arial;"> </span>
      </div>
      
      <div>
        <span style="font-size: x-small; font-family: Arial;">VMware is working on a patch to address this issue. This knowledge base article will be updated after the patch is available.</span>
      </div>
    </td>
  </tr>
</table>