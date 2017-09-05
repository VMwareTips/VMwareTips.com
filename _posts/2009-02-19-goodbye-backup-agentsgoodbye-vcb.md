---
id: 582
title: 'Goodbye Backup Agents&#8230;.Goodbye VCB'
date: 2009-02-19T16:23:38+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=582
permalink: /2009/02/19/goodbye-backup-agentsgoodbye-vcb/
redirect_from: /wp/2009/02/19/goodbye-backup-agentsgoodbye-vcb/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "1"
ratings_score:
  - "5"
ratings_average:
  - "5"
aktt_tweeted:
  - "1"
views:
  - "9863"
dsq_thread_id:
  - "5156590861"
categories:
  - 'Backup &amp; Recovery'
  - NetApp
  - Storage
tags:
  - fas
  - NetApp
  - smvi
  - snapmirror
  - tsm
  - vcb
  - VMware
---
I&#8217;ve been quite busy the last couple weeks, so busy that I&#8217;ve neglected VMwareTips.com for far too long!  Today I&#8217;d like to tell you about an exciting upcoming release for IBM Tivoli Storage Manager (TSM) and NetApp SnapMirror users.

NetApp announced a couple weeks back the integration of NetApp SnapMirror to Tape and Snapshot technologies with IBM Tivoli Storage Manager (TSM) 6. As a result, NetApp and IBM customers using TSM 6 will experience enhanced backup capabilities for data stored on NetApp FAS storage devices.

<p class="fontNormal">
  TSM 6 leverages NetApp SnapMirror to Tape technology, enabling customers to use TSM Network Data Management Protocol (NDMP) support to back up FAS volumes directly to tape or across the network to any tape device managed by TSM. This can be done without having to scan each volume to find new and changed files, helping reduce the amount of time customers need to back up their FAS systems, which can make the backup process up to 12 times faster.
</p>

<p class="fontNormal">
  TSM 6 also leverages NetApp Snapshot technology to reduce progressive incremental file backup time by comparing the current backup Snapshot copy with the previous backup Snapshot copy to identify new, changed, and deleted files. Traditional backup scans of large file systems can take hours. However, TSM 6, together with NetApp Snapshot technology, completes the identification of new, changed, and deleted files in seconds, drastically reducing the amount of time customers need to complete NetApp file system backups with TSM.
</p>

<p class="fontNormal">
  <!--more-->
</p>

<p class="fontNormal">
  For those of you that may have noticed, the above paragraphs came from the direct NetApp <a href="http://www.netapp.com/us/company/news/press-releases/news-rel-20090205.html" target="_blank">press release</a>. This is exciting news for me, currently an NDMP copy from our NetApp filer to our TSM managed tape drives requires a &#8220;full backup&#8221;, with 4-6TB of storage this can be time consuming.  This will change to a simple incremental type backup, only pushing the snapshot deltas to the tape drives.  Restoration will be as simple as a &#8220;snap restore&#8221; command on the filer.
</p>

<p class="fontNormal">
  So, goodbye VMware VCB and goodbye TSM Agents on every VM guest.  Now I can simply rely on NetApp SnapManager for Virtual Inf<img class="alignright" src="http://blogs.netapp.com/storage_nuts_n_bolts/WindowsLiveWriter/srm2.png" alt="" width="313" height="299" />rastructure (SMVI) for my D2D daily backups, and now SnapMirror to Tape with the upcoming release of TSM 6 for my D2T archives.
</p>

<p class="fontNormal">
  Also, you should already know about VMware&#8217;s Site Recovery Manager direct integration with NetApp SnapMirror to handle your disaster recovery automation. For those of us with a second datacenter, you can put another NetApp FAS system out there and use SnapMirror to replicate your virtual machines to that site, then use SRM to automate the process.
</p>