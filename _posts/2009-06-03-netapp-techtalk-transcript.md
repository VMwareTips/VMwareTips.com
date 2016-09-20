---
id: 854
title: 'NetApp, VMware and SQL TechTalk &#8211; Q&#038;A Transcript'
date: 2009-06-03T17:05:53+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=854
permalink: /2009/06/03/netapp-techtalk-transcript/
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
  - 6304
dsq_thread_id:
  - 5156591864
categories:
  - Conferences
  - NetApp
  - VMware
tags:
  - NetApp
  - sql
  - techtalk
  - VMware
---
Most of you know that I was the featured guest on a Live TechTalk last week, NetApp has furnished me with the transcripts from the Q&A of the event &#8211; for those of you that submitted questions but were unable to get a response &#8211; the transcript below should have your answer.   I&#8217;m extremely excited to say that this transcript will only be available on VMwareTips.com and NetApp will even be sending the link to their customers, hopefully this will increase the traffic on the site.

If you have any additional questions in regards to the TechTalk event, please feel free to submit a comment to this post &#8211; or email me at rick (at) vmwaretips (dot) com.

<!--more-->

**Q: Did San Diego Data Processing Corporation (SDDPC) go with 64-bit OS and SQL Server® or 32-bit, and why?
  
_A: We have a mix of 64- and 32-bit OS and SQL. It really depends on the ISV to tell us which combination to use. Our preference is 64-bit OS and SQL for the obvious performance benefits._**

**Q: What&#8217;s the storage footprint of your virtual infrastructure?**
  
_A: The VMware® cluster that makes up the environment where our SQL virtual machines are located is currently 2TB in size. This includes space-saving features put in place by utilizing FlexVol® and Deduplication._

**Q: Please explain how you were able to run 30+ SQL instances using two SQL Enterprise licenses.
  
<span style="font-weight: normal; "><em>A: The 30+ SQL instances are running on an ESX host that only has two physical CPUs installed. We were able to procure two per-processor-based licenses of SQL 2008 Enterprise, which allows us to run any version of SQL 2008 and 2005 with as many instances on the ESX host that it was purchased for.</em></span>**

**Q: Can you please repeat for what groups of guests you have turned off DRS?
  
<span style="font-weight: normal; "><em>A: We disabled DRS for the specific SQL instances in the cluster. This was done because we only purchased two per-processor-based licenses of SQL 2008 Enterprise. We are still able to use VMware HA in the event of a host failure because it does not go against the Microsoft licensing agreement.</em></span>**

**Q: How much memory is he using on his SQL VM host?
  
<span style="font-weight: normal; "><em>A: The ESX host that we have dedicated for SQL instances has two quad-core processors and 64GB of RAM. Our average SQL VM instance has 4GB of RAM reserved to it.</em></span>**

**Q: What kind of activity do you have to your SAN?
  
<span style="font-weight: normal; "><em>A: We are actually running our entire VM environment (SQL included) over NFS. Utilization is extremely low. Virtual machines do not require much bandwidth, only low latency.</em></span>**

**Q: Are you using SQL 32- or 64-bit?
  
<span style="font-weight: normal; "><em>A: A mixture of both. It depends on ISV support. We prefer SQL 2008 64-bit.</em></span>**

**Q: So your single SQL ESX host with 23 VMs also is running application servers for performance? How many total VMs are on this host?
  
<span style="font-weight: normal; "><em>A: It really depends on capacity. There are some app servers running on this host, but DRS can move those instances freely. Currently we have about 27 machines on this host, which has two quad-core processors and 64GB of RAM.</em></span>**

**Q: What changes are you making on SQL configurations to make this work, since it seems you have oversubscribed CPUs?
  
<span style="font-weight: normal; "><em>A: CPUs are oversubscribed, but by nature SQL instances are more MEM intense over CPU. VMware ESX also does a great job with coscheduling the vCPU hardware execution contexts to physical cores—our %RDY utilization is low and in the event we see contention we can always set priorities for specific instances or, worst case, add more processors to the host.</em></span>**

**Q: How are you separating the LDL, MDL, application, and systems files on the iSCSI links?
  
<span style="font-weight: normal; "><em>A: We are not using iSCSI, we are using VMDKs tied to NFS shares. We have separate VMDKs for O/S, MDL, LDL, and applications; in some instances these are tied to separate raid groups (aggregates). However, most of our aggregates have a lot of spindles assigned to them, so I/O performance is not an issue.</em></span>**

**Q: How are the VM servers configured—FC, iSCSI?
  
<span style="font-weight: normal; "><em>A: We are using VMDKs tied to NFS shares on our NetApp® FAS6030.</em></span>**

**Q: How large are the databases? Are you using raw storage or VMDKs?
  
<span style="font-weight: normal; "><em>A: We&#8217;re using VMDKs tied to NFS shares, with varying DB sizes based on application. Ours vary from 5GB to 400GB, all running VMDK over NFS.</em></span>**

**Q: Are all of your databases stored within the virtual machine or are you using mounted drives to store them?
  
<span style="font-weight: normal; "><em>A: All databases migrated to the virtual environment are running on VMDKs tied to an NFS share.</em></span>**

**Q: How is storage attached?
  
<span style="font-weight: normal; "><em>A: VMDKs are tied to NFS shares.</em></span>**

**Q: What are your database sizes?
  
<span style="font-weight: normal; "><em>A: DB sizes range based on application. Ours vary from 5GB to 400GB, all running VMDK over NFS.</em></span>**

**Q: You stated that there are 250 employees. Does this number reflect IT staff or the total number of users accessing these SQL databases? In other words, how many users, actual and peak, utilize your SQL virtual infrastructure?
  
<span style="font-weight: normal; "><em>A: It really depends on the application. SDDPC has 250 employees, but some of these applications are for the City of San Diego, which has over 10,000 employees. Our largest database typically has a peak of 1,500 to 2,000 concurrent users.</em></span>**

**Q: When you refer to separate instances, are there single databases running on each instance or multiple databases?
  
<span style="font-weight: normal; "><em>A: There is a single database on a single virtual machine. This gives us the greatest scalability and best performance metrics for chargeback.</em></span>**

**Q: Do you have 22 SQL servers on 1 ESX host?
  
<span style="font-weight: normal; "><em>A: Correct. We have 22 SQL instances, each on its own virtual machine, connected to a single ESX host.</em></span>**

**Q: Do you have the architecture diagram of the deployment? Can you bring it up?
  
<span style="font-weight: normal; "><em>A: Due to Department of Justice regulations, I cannot provide you with a diagram of the architecture, but if you have specific questions I can provide you with our design best practices.</em></span>**

**Q: Did you implement NetApp&#8217;s best practice of separating datastores for OS, for pagefile/temp, for data drives, all as separate storage areas on the NetApp? And do you worry about doing MBR alignment for all partitions inside the Windows® VMs?
  
<span style="font-weight: normal; "><em>A: We separate OS/DB/LOG/app, etc., on individual VMDK drives. Then we separate some of those drives at the aggregate level as well. We watch our IOPs utilization at the raid group level very closely—if we are nearing a peak we migrate data as needed. Our virtual machine templates&#8217; &#8220;golden image&#8221; already has the MBR alignment set to the best practice, which enables any new instance deployed to be in alignment.</em></span>**

**Q: On which ESX version are you running SQL on VMware? For dedupe, how many VMs do you have per volume? What is the load on the SQL Servers? What is the virtual hardware giving to the SQL Server? When using memory reservation, does transparent memory sharing work?
  
<span style="font-weight: normal; "><em>A: We are now running ESX 4.0; last week these were on ESX 3.5 U3. For dedupe we currently have on average 40 to 50 virtual machines per volume to give us around 60% savings with A-SIS. The load on the SQL Servers varies—our busiest application has a constant 60% memory load but a 15% CPU load. To follow best practices, all of our SQL VMs have hard reservations and limits, and VMware TPS [transparent page sharing] still does a great job providing us with some good consolidation ratios. Our average VM has 1 vCPU and 4GB of RAM.</em></span>**

**Q: If we have SQL running in a VM using an RDM LUN, how can we back up the VM and the RDM-based SQL LUN?
  
<span style="font-weight: normal; "><em>A: This really isn&#8217;t a cut-and-dried answer. If your RDMs are in virtual mode, then you can utilize a tool like SMVI to quiesce and take a snapshot at the VM level. If they are in physical mode, then you need to utilize SnapManager® for SQL to quiesce the SQL DB and then SMVI for the VM itself. I&#8217;d suggest getting someone in from Professional Services to help you plan this critical piece of your environment.</em></span>**

**Q: How does SDDPC back up SQL in the VMs?
  
<span style="font-weight: normal; "><em>A: Because we are running everything on VMDKs, we can utilize SnapManager for VI to quiesce the OS and DB using VMware snapshot technology, then integrate with NetApp Snapshot™ copies for D2D backup. SnapMirror® and NDMP are then used to migrate this data off site and to tape for archiving.</em></span>**

**Q: Can you go over the SQL licensing in a little more detail? Did I understand correctly that if two per-processor licenses are purchased for the VM host, multiple VMs with SQL can run on that host and use the same two licenses?
  
<span style="font-weight: normal; "><em>A: That is correct, but this is with the SQL Enterprise (per-processor) license. SQL Standard per processor would still be at the virtual CPU level. Enterprise allows you to purchase at the physical CPU level, allowing you to run as many copies of SQL as needed. You truly need to find your &#8220;sweet spot&#8221; for licensing. This is typically found by averaging the prices and determining how many instances you will be running.</em></span>**

**Q: Each instance of SQL, if it&#8217;s on its own VM, will be costly (the SQL license). Did I understand the statement about instances on their own VMs?
  
<span style="font-weight: normal; "><em>A: That is correct, but this is with the SQL Enterprise (per-processor) license. SQL Standard per processor would still be at the virtual CPU level. Enterprise allows you to purchase at the physical CPU level, allowing you to run as man</em><em>y copies of SQL as needed. You truly need to find your &#8220;sweet spot&#8221; for licensing. This is typically found by averaging the prices and determining how many instances you will be running.</em></span>**

**Q: What type of transaction load is on the SQL Servers? Is the business logic in an app tier or is it in stored procedures?
  
<span style="font-weight: normal; "><em>A: For most of our applications the logic is typically in the application layer—some DBs have storage procedures but they are not that I/O intense. Most DBs are for Web applications (.NET + Java™), payment-processing applications, and also SAP®.</em></span>**

**Q: Why did SDDPC decide to go with NFS over fiber or iSCSI?
  
<span style="font-weight: normal; "><em>A: Mainly because of its flexibility—using NFS for your VMDK datastores gives you extreme flexibility over block-level storage (iSCSI, FCP). There is also a major misconception about the throughput—VMDKs do not require high throughput, only low latency, which can be achieved with 1GbE and NFS. For DBs that require larger data loads and warrant the need of >1GbE I suggest looking at 10GbE. It truly comes down to what you already have installed—if you have an FC infrastructure that you can tie into, then utilize it. We already had an IP storage infrastructure for NFS, so that is why we chose that route.</em></span>**

**Q: Have you done any special tuning to the NFS options on your NetApp to optimize storage performance?
  
<span style="font-weight: normal; "><em>A: I recommend following the best practices found in NetApp TR-3428 for configuring IP storage on VMware ESX.</em></span>**

**Q: Would you elaborate on &#8220;separate storage&#8221; (that is, separate appliances, separate aggregates, separate volumes, and so on)? What are your thoughts on using NFS exclusively?
  
<span style="font-weight: normal; "><em>A: We&#8217;re using NFS here and love it—the flexibility it creates is the main seller over iSCSI or FCP. The only down side is the throughput, which is typically not an issue—average VMDK usage does not warrant needing more than 1GbE—but if you have a DB that is doing large data loads, then you may want to look at 10GbE for throughput. As far as separating storage, obviously at the VMDK level it is a must, but also separating at the RAID group level (aggregate) is needed—you need to put your high I/O data on faster disks with more spindles, low I/O on slower disks. But if you have an aggregate that can meet the I/O needs of all your data, then you can run all of it on the same aggregate.</em></span>**

###### *This transcript includes a select group of questions and answers from the NetApp and VMware Live TechTalk: Virtualizing SQL on VMware with confidence featuring customer guest Rick Scherer of San Diego Data Processing Corporation and does not represent the TechTalk Q&A in its entirety.