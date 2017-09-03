---
id: 711
title: Committing snapshots generates a content ID mismatch error
date: 2009-04-14T05:52:12+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=711
permalink: /2009/04/14/committing-snapshots-generates-a-content-id-mismatch-error/
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
  - "12252"
dsq_thread_id:
  - "5156596208"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Storage
tags:
  - CID
  - commit
  - esx
  - esxi
  - snapshot
  - vcb
  - vmdk
---
I had a big problem Monday AM on one of my core SAP VM instances, that also happens to have a SQL DB server on it. Our VCB process finishes up on late Sunday night, if you&#8217;re not aware of how VCB works, it basically creates a snapshot of the Virtual Machine, then mounts the now readable VMDK parent to a proxy server where your backup agent resides. Once the backup is complete the snapshot is committed.  This wasn&#8217;t the case Monday AM &#8212; the VM crashed and I was paged. Snapshot didn&#8217;t commit, parent VMDK could not be found, had to manually set Parent CID in the delta VMDK file then finally when I got it back online the SQL DB was corrupt :( &#8212; luckily I had a full SQL backup from the night before.

This is where <a href="http://kb.vmware.com/kb/1007969" target="_blank">VMware KB 1007969</a> comes into the story&#8230;

<!--more-->

**Symptoms**

  * <span style="font-family: Arial; ">P</span><span style="font-family: Arial;">erforming a commit of a snapshot fails</span>
  * The virtual machine shuts down abruptly during snapshot commit
  * Performing a snapshot commit generates the error:
  
    <span style="font-family: 'Courier New'; ">Content ID mismatch </span>
  * <span style="font-family: 'Courier New'; "><span style="font-family: 'Lucida Grande'; ">Powering on the virtual machine generates the error:<br /> <span style="font-family: 'Courier New'; ">Content ID mismatch </span></span></span>
  * <span style="font-family: 'Courier New'; "><span style="font-family: 'Lucida Grande'; "><span style="font-family: 'Courier New'; "><span style="font-family: 'Lucida Grande'; ">The virtual machine log contains the following:<br /> <span style="font-family: 'Courier New'; ">Sep 11 03:01:45.328: vmx| DISKLIB-LINK : Attach: Content ID mismatch (d504c2f0 != 62e0e8bf).<br /> Sep 11 03:01:45.331: vmx| DISKLIB-CHAIN : &#8220;/vmfs/volumes/48a1b01c-67422c6d-f5aa-00188b50e0ff/test/w2k3-lsi-64.vmdk&#8221; : failed to open (The parent virtual disk has been modified since the child was created).<br /> Sep 11 03:01:45.336: vmx| DISKLIB-VMFS : &#8220;/vmfs/volumes/48a1b01c-67422c6d-f5aa-00188b50e0ff/186-testing/w2k3-lsi-64-000001-delta.vmdk&#8221; : closed.<br /> Sep 11 03:01:45.342: vmx| DISKLIB-VMFS : &#8220;/vmfs/volumes/48a1b01c-67422c6d-f5aa-00188b50e0ff/186-testing/w2k3-lsi-64-000013-delta.vmdk&#8221; : closed.<br /> Sep 11 03:01:45.348: vmx| DISKLIB-VMFS : &#8220;/vmfs/volumes/48a1b01c-67422c6d-f5aa-00188b50e0ff/test/w2k3-lsi-64-flat.vmdk&#8221; : closed.<br /> Sep 11 03:01:45.352: vmx| DISKLIB-LIB : Failed to open &#8216;/vmfs/volumes/48a1b01c-67422c6d-f5aa-00188b50e0ff/186-testing/w2k3-lsi-64-000001.vmdk&#8217; with flags 0xa (The parent virtual disk has been modified since the child was created).<br /> Sep 11 03:01:45.355: vmx| DISK: Cannot open disk &#8220;/vmfs/volumes/48a1b01c-67422c6d-f5aa-00188b50e0ff/186-testing/w2k3-lsi-64-000001.vmdk&#8221;: The parent virtual disk has been modified since the child was created (18).</span></span></span></span></span>

**Resolution**

<span style="font-family: Arial; ">V</span>Mware is aware of, and actively investigating the issue.

When a snapshot delete is requested:

  1. The CID of the disk being combined into is updated
  2. The virtual disk is updated with changes.
  3. The CIDs of the children (that are not being removed) are updated.

If a failure occurs during the combine process (I/O errors or running out of disk space), the combine process aborts. The CIDs of the supporting children files never get updated, resulting in mismatch.

**<span style="font-weight: normal;">Warning</span>**: Do not perform a **<span style="font-weight: normal;">Go To</span>** and do not **<span style="font-weight: normal;">Revert</span>** to the parent snapshot.

You must correct the snapshot parent/child relationship.

To correct the parent/child relationship:

  1. Log in to the ESX Server console and verify the CID of all the virtual disks. The current snapshot disks are identified in the virtual machine configuration file (.vmx).
  2. Examine the virtual disk header files to verify the CID and ParentCID of each member to ensure that they match all the way up the tree.
  3. When the one that does not match is found, update the ParentCID of the child to match the CID of the file next up the chain.

**<span style="font-weight: normal;">Note</span>**: For more information related to performing these steps, see <a href="http://kb.vmware.com/kb/1007849" target="_blank"><span style="color: #000000; text-decoration: none;">Consolidating Snapshots (1007849)</span></a>.

The virtual machine powers on normally at this point.

You can safely continue to use the snapshot or perform the commit operation again. VMware recommends to perform the commit operation so that all changes found in the delta are written down to the next level of snapshot or base disk (if there was only one level of snapshot).