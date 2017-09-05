---
id: 249
title: 'Product Review : Vizioncore vFoglight'
date: 2008-10-30T14:46:35+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=249
permalink: /2008/10/30/product-review-vizioncore-vfoglight/
redirect_from: /wp/2008/10/30/product-review-vizioncore-vfoglight/
ratings_users:
  - "8"
ratings_score:
  - "28"
ratings_average:
  - "3.5"
views:
  - "15331"
dsq_thread_id:
  - "5156596805"
categories:
  - Good Reading
  - Monitoring
tags:
  - Monitoring
  - reports
  - vfoglight
---
<p style="text-align: left;">
  I&#8217;ve been using a demo version of vFoglight for about 2 weeks now and I am overwhelmed with how much this product can do.  The installation is extremely straight forward, this product is based on Quest Software&#8217;s Foglight Application and Service Management software.  Basically you have three components, the actual Foglight software and the VMware Collector and Connector.  Long story short, this piece of software is most likely all you would ever need for complete monitoring, reporting and alerting of your VMware Infrastructure, the downside is that you would most likely need a team of server administrators and trained professionals to get it all configured and running to meet your needs.
</p>

<p style="text-align: left;">
  <!--more-->
</p>

<p style="text-align: left;">
  In the two weeks I&#8217;ve been using it, I&#8217;ve found that there are a great deal of built-in features to help monitor and retrieve data on your environment.  You can view CPU, Memory, Network I/O and Disk I/O consumption from a VirtualCenter level (includes all datacenters, clusters, resource pools, etc.), datacenter level, cluster level, resource pool level and guest VM level. The data is so granular that you can even see disk usage at a VM level (VMDK allocation, usage). Another note to add is that event messages from VirtualCenter are automatically imported into vFoglight as well.
</p>

<p style="text-align: left; padding-left: 30px;">
  <em><a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vfoglight1.png"><img class="ngg-singlepic alignnone" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vfoglight1.png" alt="vfoglight1.png" width="400" />(click to enlarge)</a><br /> </em>
</p>

<p style="text-align: left;">
  Another nice feature is the alarm/alerting functionality, there are a ton of alarms pre-configured but it does seem that they may be a tad on the sensitive side. For instance, I&#8217;m running vFoglight within a Virtual Machine, by default the Foglight software will consume at minimum 70% of available RAM, this triggers an alarm within vFoglight. <em>&#8220;<span class="cellContent" style="cursor: pointer;" onclick="w557101093.onCellSelectionOnClick(event)" onmouseover="w557101093.onCellSelectionOnMouseOver(event); ">Virtual machine dpcrcvfoglight is reserving 90 % of the memory ESX has granted to it. The application workload of the system is requesting an excessive amount of the available memory resources. Either add more memory to the system or better balance your virtual machines within the cluster.&#8221; </span></em><span class="cellContent" style="cursor: pointer;" onclick="w557101093.onCellSelectionOnClick(event)" onmouseover="w557101093.onCellSelectionOnMouseOver(event); ">The funny thing is that no matter how much more memory I add, this alarm will always be on.</span>
</p>

<p style="text-align: left; padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vfoglight4.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vfoglight4.png" alt="vfoglight4.png" width="400" /><em>(click to enlarge)</em><br /> </a>
</p>

<p style="text-align: left; padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vfoglight3.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vfoglight3.png" alt="vfoglight3.png" width="400" /><em>(click to enlarge)</em><br /> </a>
</p>

<p style="text-align: left;">
  One of the most exciting features for me is vmModeler, this allows you to look at an individual VM instance and see how it would perform on any other ESX host. This gives you estimated usage statistics for your ESX server after you&#8217;ve migrated the selected Virtual Machine to it.
</p>

<p style="text-align: left; padding-left: 30px;">
  <a class="thickbox" href="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vfoglight2.png"><img class="ngg-singlepic ngg-none" src="http://vmwaretips.com/wp/wp-content/gallery/screenshots/vfoglight2.png" alt="vfoglight2.png" width="400" /><em>(click to enlarge)</em></a>
</p>

<p style="text-align: left;">
  I&#8217;m not even going to touch on the reporting features of this product.  Because this product is built on Quest&#8217;s Foglight the opportunities are endless, you can generate completely custom reports with any piece of data that the collector has grabbed. The nice thing is that reports can be generated on a schedule, or on demand. They can be viewed via the Foglight dashboard or exported to PDF format.  One thing I must comment on though is the fact that the Report Browser function of my install suddenly stopped working and does not display properly.
</p>

<p style="text-align: left;">
  In closing I must tell you that this software is a complete resource hog.  I gave it 2 vCPU with 4GB of RAM and even ran their 64-bit edition and it was very slow (5-10 seconds) between different screens.  It is very possible that this is because I installed it using the provided local database (MySQL).  Performance could possibly improve by using a separate database server. vFoglight runs on Tomcat making it completely accessible via a web browser. vFoglight also supports Role Based Access Control (RBAC) meaning you can assign different permissions/reports/views to different employees, you can use the built-in authentication module or your can configure it to use your local LDAP (ActiveDirectory) server. It must also be noted that as the writing of this document vFoglight does not have any Charge-Back capabilities (unlike its predecessor vCharter Pro), although there are plans to integrate this feature at a later date.
</p>

<p style="text-align: left;">
  The capabilities of Vizioncore&#8217;s vFoglight are so overwhelming, that before I deploy it I would want to take at least a week or two for training and configuration. This product is so robust that it may be too much for most customers, I strongly suggest that if you are looking for a monitoring/reporting system, take your time and see what all the vendors offer, I would even suggest doing a POC with them.
</p>

<p style="text-align: left;">
  I do plan on performing a demo of monitoring/reporting systems from other vendors, next on the list will be utilities from Veeam.
</p>