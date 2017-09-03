---
id: 517
title: 'My HDD Failed &#8211; But ddrescue Saved the Day'
date: 2009-01-29T13:56:58+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=517
permalink: /2009/01/29/my-hdd-failed-but-ddrescue-saved-the-day/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "2"
ratings_score:
  - "10"
ratings_average:
  - "5"
aktt_tweeted:
  - "1"
views:
  - "30138"
dsq_thread_id:
  - "5156590190"
categories:
  - Good Reading
  - Linux
tags:
  - ddrescue
  - disk
  - e2fsck
  - fsck
  - partition
  - recovery
---
On Tuesday morning my HDD failed on my PC at the office.  Most of my important data is in a NFS volume on a FAS6030, but my PC still had some important stuff on it.  Including a Windows XP virtual machine that has all my necessary programs (Outlook, SAP, TweetDeck) and some files that I forgot to copy over to my NFS share.  Using a tool called ddrescue I was able to save most of my data, I&#8217;ll go into how it works and what I did.

<!--more-->

Well, on Tuesday morning my PC wouldn&#8217;t start after a reboot, it would pretty much freeze right after GRUB did its thing.   I booted from the Ubuntu Live CD and saw some lovely errors in the messages file:

<p style="padding-left: 30px;">
  Jan 27 13:29:55 shrek kernel: [74211.342500] sd 1:0:0:0: [sdb] Result: hostbyte=DID_OK driverbyte=DRIVER_SENSE,SUGGEST_OK<br /> Jan 27 13:29:55 shrek kernel: [74211.342504] sd 1:0:0:0: [sdb] Sense Key : Medium Error [current] [descriptor]<br /> Jan 27 13:29:55 shrek kernel: [74211.342509] Descriptor sense data with sense descriptors (in hex):<br /> Jan 27 13:29:55 shrek kernel: [74211.342513]         72 03 11 04 00 00 00 0c 00 0a 80 00 00 00 00 00<br /> Jan 27 13:29:55 shrek kernel: [74211.342523]         02 80 07 64<br /> Jan 27 13:29:55 shrek kernel: [74211.342528] sd 1:0:0:0: [sdb] Add. Sense: Unrecovered read error &#8211; auto reallocate failed<br /> Jan 27 13:29:55 shrek kernel: [74211.342562] ata2: EH complete<br /> Jan 27 13:29:55 shrek kernel: [74211.342599] sd 1:0:0:0: [sdb] 312581808 512-byte hardware sectors (160042 MB)<br /> Jan 27 13:29:55 shrek kernel: [74211.342615] sd 1:0:0:0: [sdb] Write Protect is off<br /> Jan 27 13:29:55 shrek kernel: [74211.342642] sd 1:0:0:0: [sdb] Write cache: enabled, read cache: enabled, doesn&#8217;t support DPO or FUA<br /> Jan 27 13:29:58 shrek kernel: [74214.288344] ata2.00: configured for UDMA/33<br /> Jan 27 13:29:58 shrek kernel: [74214.288352] ata2: EH complete<br /> Jan 27 13:30:01 shrek kernel: [74217.226167] ata2.00: configured for UDMA/33<br /> Jan 27 13:30:01 shrek kernel: [74217.226177] ata2: EH complete<br /> Jan 27 13:30:01 shrek kernel: [74217.226220] sd 1:0:0:0: [sdb] 312581808 512-byte hardware sectors (160042 MB)
</p>

I then asked my companies desktop support group for two new hard drives, 160GB SATA3 Western Digital disks were delivered within a few hours.  I then configured the Intel Storage BIOS on my HP xw4600 to put both disks into a RAID-1 (I should have done this when I first build it &#8211; thing originally only came with 1 HDD).

I then installed Ubuntu 8.10 using the alternative disk because I need the dmraid support for my RAID-1 (if you didn&#8217;t know, most PCs do not actually have hardware RAIDs, they are software assisted which means you need a O/S driver for it to fully work).

After my O/S was installed and to my liking, I installed VMware Workstation 6.5 &#8211; now I am ready to recover my VMDK files!

I then shutdown the machine and connected my bad HDD to an open SATA port.  Booted up Ubuntu, which took forever because it was complaining about the above errors.  I also connected an external USB drive with plenty of open space (I&#8217;ll get into this more later). After the system was up and I was able to see the disk via _fdisk -l_ I proceeded to install ddrescue by typing  _sudo apt-get install gddrescue_

After install I then ran the following command:

<p style="padding-left: 30px;">
  <em>ddrescue -r3 /dev/sdb3 /media/USB/Backup/sdb3.image /media/USB/Backup/sdb3.logfile</em>
</p>

Lets break this down,  obvious ddrescue is the program, -r3 is the amount of retries it will attempt on a bad block (obviously if you think your HDD is going out fast, you would want to lower this number, or use -n to not retry at all).  You then specify the entire disk you wish to recover, or the partition. Here I&#8217;m attempting to recover partition 3 on disk sdb (found from _fdisk -l_). Next is where you want the image to be placed, ddrescue can write to a new partition on another disk or to a image file (on a USB drive or other type of media). Finally you tell it where to write the log file, one nice feature of ddrescue is the ability to stop and start the rescue process &#8211; it keeps a log of exactly what it did last so it can pick up right where it left off.

One thing you must know, if you rescue a partition (or disk) to another partition, disk or image-  you MUST have enough space on the destination to cover the entire partition (or disk).  For example, sdb3 on my bad disk was 60GB total size, although I was only using 30GB of it I needed to ensure my USB drive had 60GB free to write the image.

This is an example of ddrescue running, right here it has ran and it is splitting the bad blocks and writing over the bad ones with clean 0-data.  One thing thats cool about ddrescue is that it will attempt for example 512B blocks, if it hits a bad block it will attempt at 256B and then all the way down to 1B until it gets some successful data.  This can take a LONG time if you have a ton of bad blocks,  the below example has been running for over 20 hours and still isn&#8217;t complete.

<p style="padding-left: 30px;">
  Initial status (read from logfile)<br /> rescued:    80527 MB,  errsize:  14602 kB,  errors:    1550<br /> Current status<br /> rescued:    80527 MB,  errsize:  14286 kB,  current rate:        0 B/s<br /> ipos:    26172 MB,   errors:    2223,    average rate:       19 B/s<br /> opos:    26172 MB<br /> Splitting error areas&#8230;
</p>

So, after the ddrescue is complete, you will need to fsck the image (or partition(s)) before you can mount them.  If for some reason you cannot remember the filesystem type you can use a tool like _mmls_ to find out what type of filesystem the partition is.  Lets say it is a ext3 filesystem, we will use e2fsck to fsck it: _e2fsck -y /media/USB/Backup/sdb3.image_ &#8212; the -y will blast through the fsck answering yes to all of the block changes it will want to make.

After fsck, I then mounted the image:  _mount -o loop /media/USB/Backup/sdb3.image /mnt_ &#8212;  to my surprise, all my lovely VMDK and VMX files were in there!  Oh glory!

<p style="padding-left: 120px;">