---
id: 1016
title: NetApp SnapManager for VI 2.0 (SMVI)
date: 2009-09-16T09:58:15+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=1016
permalink: /2009/09/16/netapp-snapmanager-for-vi-20-smvi/
redirect_from: /wp/2009/09/16/netapp-snapmanager-for-vi-20-smvi/
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
  - "15522"
dsq_thread_id:
  - "5156595258"
categories:
  - 'Backup &amp; Recovery'
  - NetApp
  - Storage
tags:
  - NetApp
  - smvi
---
For those of you using NetApp for your back-end virtual machine storage, there is a new version of their SnapManager for Virtual Infrastructure (SMVI) tool that was recently released. SMVI 2.0 will include a number of enhancements that really push the bar when it comes to NetApp/VMware integration.

Some of the enhancements to the 2.0 product include;

<ul style="margin-top: 10px; margin-bottom: 10px;">
  <li>
    <span style="color: #2d2d2d;">Autosupport Integration</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Backup Enhancements & GUI Re-design</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Snapshot Naming Changes</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Scripting</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Restore Enhancements</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Single File Restore</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Self-Service Restore</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Limited Self-Service Restore</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Administrator-Assisted Restore</span>
  </li>
  <li>
    <span style="color: #2d2d2d;">Restore Agent</span>
  </li>
</ul>

What really excites me with this new version is the ability for an end-user to do a single file restoration, this will dramatically decrease the labor required at the server administration level for these types of requests.  Most of us already using the 1.0 product have seen the benefits of the VMware/NetApp snapshot integration, how NetApp utilizes VMware Tools to quiesce the virtual machine(s) within a datastore then do a NetApp level snapshot. Then there is also the ability to tie this all into SnapMirror, which works great.

Check out this video demonstrating some of the new features in SMVI 2.0

<p style="text-align: center;">
  <a title="NetApp SMVI 2.0" rel="shadowbox;height=505;width=640" href="http://www.youtube.com/v/fPg8FNaA_MY"><img class="aligncenter size-full wp-image-1017" title="smvi2" src="https://www.vmwaretips.com/wp-content/uploads/2009/09/smvi2.png" alt="" width="400" height="301" srcset="https://www.vmwaretips.com/wp-content/uploads/2009/09/smvi2.png 400w, https://www.vmwaretips.com/wp-content/uploads/2009/09/smvi2-300x225.png 300w" sizes="(max-width: 400px) 100vw, 400px" /></a>
</p>

For those of you using NetApp, I&#8217;d strongly recommend adding SMVI to your FY11 budget!