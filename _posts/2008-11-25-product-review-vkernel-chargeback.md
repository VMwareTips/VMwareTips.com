---
id: 294
title: 'Product Review : vKernel Chargeback'
date: 2008-11-25T17:54:03+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=294
permalink: /2008/11/25/product-review-vkernel-chargeback/
redirect_from: /wp/2008/11/25/product-review-vkernel-chargeback/
ratings_users:
  - "1"
ratings_score:
  - "5"
ratings_average:
  - "5"
views:
  - "6333"
dsq_thread_id:
  - "5156597450"
categories:
  - Good Reading
  - Monitoring
tags:
  - chargeback
  - Monitoring
  - utilization
  - VMware
---
Recently my employer found the need to assess virtual machine utilization, to be used for FY10 budget planning.  So, I started my search for the best product to do just that.

As you may have read, I&#8217;ve already reviewed Vizioncore&#8217;s vFoglight &#8211; which is a real nice product and extremely flexible&#8230;but, as some may have already seen or heard, it is extremely bloated and put a 2 vCPU/4GB Virtual Machine to its knees. (Also, it does not have a Chargeback feature..which is surprising since the older versions of vCharter did) &#8230;So, this is where vKernel&#8217;s product line comes in.



vKernel&#8217;s Chargeback is exactly that, its a product designed to help you assess what a Virtual Machine is costing you to run it&#8230;.nothing more, nothing less.   The installation is the most streamlined process I&#8217;ve seen, but it should be since it is a Virtual Appliance.  Simply import this Virtual Appliance from within your VI Infrastructure Client and your up and running in less than an hour (depending on your WAN connection speed).

After it is downloaded and imported to your environment you simply answer a couple questions about your network and locale, including timezone.  You are then presented with a URL that you open with a web-browser, this is where you finish the configuration.

The first thing you want to configure is the database connection.  You can either use a local MySQL database, or you can connect to an external Oracle or MS SQL database.  In our deployment we&#8217;re using Microsoft SQL 2005, all I had to do was create an empty database with a SQL account that had DBO rights. I then created the connection in Chargeback and it did all the work for creating tables, etc.

<p style="padding-left: 30px;">
  <a class="thickbox" href="https://www.vmwaretips.com/wp/wp-content/gallery/screenshots/vkcb-db.png"><img class="ngg-singlepic ngg-none alignnone" src="https://www.vmwaretips.com/wp/wp-content/gallery/screenshots/vkcb-db.png" alt="vkcb-db.png" width="400" /></a>
</p>

After your database is connected, you then have the option of connecting to a VirtualCenter server or individual ESX hosts (One thing to keep in mind is that Chargeback is billed by each physical CPU of each host your collecting data from.  So, if you chose to connect to a VirtualCenter server you will need to have a license for each host VirtualCenter manages). Also, one nice feature is the ability to have Chargeback retrieve historical data, I was able to retrieve 6 months of statistics to help my bill-back process. The default is to go back one-week, which shouldn&#8217;t take that long depending on your statistics level. (Recommended setting is 3/2/2/2 = 5 Min: 3 / 30 Min: 2 / 2 Hour: 2 / 1 Day: 2)  For me to collect 4,380 hours of data took roughly a day or so&#8230;.the default should only take minutes.

<p style="padding-left: 30px;">
  <a class="thickbox" href="https://www.vmwaretips.com/wp/wp-content/gallery/screenshots/vkcb-conn.png"><img class="ngg-singlepic ngg-none alignnone" src="https://www.vmwaretips.com/wp/wp-content/gallery/screenshots/vkcb-conn.png" alt="vkcb-conn.png" width="400" /></a>
</p>

Ok&#8230;so now we&#8217;re online and Chargeback has some data.  Now lets get some numbers!  First you need to create groups, here you specify which datacenters, clusters, hosts, resource groups or virtual machines are members of a group. You also assign a cost to CPU, Memory, Storage and Network usage. To help you come up with these numbers vKernel provides an easy to use Excel spreadsheet.  At first I was a little skeptical about this spreadsheet, seeing that other vendors allow you to input raw costs into their product.  But, after talking with Alex Bakman, Founder and CEO of vKernel, he made me realize that this was to create further flexibility. Most other vendors just allow you to input your costs and they come up with a price per GHz/GB, etc. based on their own proprietary calculations&#8230;.vKernel Chargeback&#8217;s approach allows you to assign a capacity reserve, amortization schedule and even the ability to divide the total cost (ie: Instead of a 50/50 CPU to Memory cost analysis, you can say you want to recover 30% of your costs from CPU and 70% of your costs from Memory&#8230;this is a more realistic approach seeing that Memory ultimately costs more than CPU power). Another nice feature is the ability to input additional pricing data, this makes your options endless, for example you can include rates for server support costs, licensing costs and much more.

We now have our groups created and we are ready to see some reports.  First we need to create customers, then we can assign our custom groups to those customers.  Whats nice about this is that you can assign your custom groups to multiple customers (ie: Shared services).  Now you run your Chargeback reports on a per-customer basis.  The different options for Chargeback reports are Today, Yesterday, This Week, Last Week, This Month, Last Month and This Year.  I would&#8217;ve liked to seen the ability to create custom date ranges, but maybe this will come in a later version.  Once created you have the ability to export that report as a PDF, CSV or XML document. These reports can even be scheduled to run and sent via e-mail or uploaded to a SFTP server, the scheduling is extremely flexible and you can even have it send alerts (via email) if the reports were unable to be generated.

<p style="padding-left: 30px;">
  <a class="thickbox" href="https://www.vmwaretips.com/wp/wp-content/gallery/screenshots/vkcb-report.png"><img class="ngg-singlepic ngg-none alignnone" src="https://www.vmwaretips.com/wp/wp-content/gallery/screenshots/vkcb-report.png" alt="vkcb-report.png" width="400" /></a>
</p>

Another nice feature of Chargeback is the ability to run performance statistics, these can be ran against your custom groups, datacenters, clusters, hosts, resource groups or individual Virtual Machines. These reports cannot be scheduled but they still a nice to have feature of Chargeback. Another plus is the ability to run &#8220;Change Reports&#8221; against the same groups above, this shows you a change in usage (shown in a percentage) against the selected item.  For example I can see a CPU utilization change for an individual virtual machine comparing this week to last week.

<p style="padding-left: 30px;">
  <a class="thickbox" href="https://www.vmwaretips.com/wp/wp-content/gallery/screenshots/vkcb-perf.png"><img class="ngg-singlepic ngg-none alignnone" src="https://www.vmwaretips.com/wp/wp-content/gallery/screenshots/vkcb-perf.png" alt="vkcb-perf.png" width="400" /></a>
</p>

In closing, vKernel Chargeback is a great product. It does exactly what its called, it creates Chargeback reports for your Virtual Environment.  It is not bloated out with features you don&#8217;t need or want, your paying for exactly what you asked for.  It is extremely easy to configure and use and it has a lot of useful features.  Although, it would be nice to see their cost calculator embeded within the application, and perhaps some RBAC (role-based access control) features (perhaps ActiveDirectory or LDAP integration). But other than that I think this is a great product and can&#8217;t wait to see more from this great company.