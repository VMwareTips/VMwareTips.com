---
id: 373
title: Hyper-V vs. VMware = Monday Debate
date: 2008-12-15T17:23:29+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=373
permalink: /2008/12/15/hyper-v-vs-vmware-monday-debate/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "3789"
dsq_thread_id:
  - "5156597339"
categories:
  - Good Reading
  - Hyper-V
  - VMware
tags:
  - comparison
  - esx
  - esxi
  - hyper-v
  - VMware
---
This morning when I came into work my twitter box was flooded and there was a lot of heat distributed across the virtualization blogging world.  This all started when <a href="http://fawzi.wordpress.com/2008/12/14/hyper-v-vs-vmware/" target="_blank">this post</a> was published on the Zero&#8217;s & One&#8217;s blog site.  Almost immediately <a href="http://blog.scottlowe.org/2008/12/15/youve-got-to-be-kidding-me/" target="_blank">Scott Lowe</a> and <a href="http://www.boche.net/blog/?p=690" target="_blank">Jason Boche</a> posted their rebuttals, along with dozens of other comments on the initial posting and even more spread across Twitter&#8230; Now I would like to chime in.

<!--more-->

Ok, so if you haven&#8217;t read the posting by now, it basically is comparing Microsoft Hyper-V to VMware ESX &#8211; the huge problem with this is that it is a completely unbalanced review mainly because the author is comparing Microsoft Hyper-V with the Enterprise Edition of VMware ESX &#8212; which IMO are in two completely different product offerings.

Reading the above mentioned posting brings me a lot of grief, the biggest issue I have with it is the complete lack of research done on the topic.  It appears that the author grabbed data from sites, blogs and possibly even some just made up and posted it as factual data.   Below are my opinions on each one of the topics he discussed.  If you haven&#8217;t, I strongly suggest you read his posting so you can compare.

<p style="padding-left: 30px;">
  <strong>Cost: </strong>Comparing VI3 Enterprise to Hyper-V is not a solid comparison.  The features in VI3 Enterprise over-power those built into Hyper-V.  The better comparison would be to compare it against VMware ESXi which has a 100% free edition.  Also noted is that Hyper-V does have a free edition, this does not include any guest operating system &#8211; which means you would be required to purchase this just like you would for ESXi.  Also noted is that none of the system management tools are included in the free edition of Hyper-V.
</p>

<p style="padding-left: 30px;">
  <strong>Support:</strong> With a valid VMware SnS subscription, VMware will make a best effort attempt to resolve your problem (with your supported guest O/S issues).  If for some reason they cannot resolve your problem they have escalation procedures to directly connect you with the ISV through a predetermined channel.  Also noted is Microsoft Hyper-V only supports Windows 2003, 2008 and Novell SUSE Linux.
</p>

<p style="padding-left: 30px;">
  <strong>Hardware Requirements</strong>: VMware requires your hardware be on the VMware Hardware Compatibility List, this is a fairly thorough list with a wide support offering.  Also for the advanced features like VMware HA, matching hardware is not required.  For the use of vMotion you are required however to utilize matching CPU models between hosts (No Intel -> AMD), further noted with ESX(i) 3.5 U2 there is now Enhanced vMotion Compatibility (EVC) which means you can now vMotion between older versions of the CPU manufacturers chips and their newer ones (ie: AMD Single Core Opteron to AMD Quad Core Opteron).<br /> Even though Microsoft Hyper-V is supported on virtually ALL models of hardware, it must be noted that if you plan on doing any &#8220;live migration&#8221; or clustering, you are required to obtain exact matching hardware to ensure compatibility.
</p>

<p style="padding-left: 30px;">
  <strong>Advanced Memory Management</strong>: His comment actually boggles my mind. He states that with the money you save on not purchasing ESX you can simply buy more RAM for Hyper-V because you&#8217;ll need it.  This is a completely worthless statement.  ESX has built-in advanced memory improvements, the VMware Ballooning driver allows your virtual machines to share memory for basic and common tasks.  Hyper-V forces you to ensure you have the full memory required for each VM (no memory sharing).  How is this efficient? And the comment about critical applications, just create a resource pool in VMware&#8217;s Virtual Infrastructure to guarantee your memory commitment to your Virtual Machine.
</p>

<p style="padding-left: 30px;">
  <strong>Hypervisor</strong>: His comments keep getting better with this one.  Here he states that Hyper-V is only 872KB and is more secure against attacks.  Wow.  Did he forget that you still need the full Windows kernel for this to run&#8230;and also the fact that its Windows.   So your telling me that a Windows kernel running Hyper-V is more secure than a proprietary 32MB bare metal hypervisor?  I don&#8217;t even need to comment.
</p>

<p style="padding-left: 30px;">
  <strong>Driver Support</strong>: This is an easy one.  Your running a hypervisor, why would you want 45,000 drivers to load? Your hypervisor should be the thinnest and most efficient piece installed on your hardware, it should only interact with the necessary hardware on the machine (CPU, Memory, Network & HBA interfaces).  This just means you&#8217;ll have more drivers and other things to patch on Patch Tuesday.
</p>

<p style="padding-left: 30px;">
  <strong>Processor Support</strong>: This is another comment that makes no sense.  It&#8217;s pretty simple, if you require 64-bit guest operating systems then you need to have x64 architecture.  If you don&#8217;t, then you can suffice with x86 architecture.  ESX does not require you install on x86 or x64 hardware, it can run on either. Hyper-V however requires you to run on x64.  ESX is currently a 32-bit operating system, but because of its address translation it allows 64-bit guests to run.  This does create an overhead, but it is still minimal and a necessity of any hypervisor (Hyper-V included).
</p>

<p style="padding-left: 30px;">
  <strong>Application Support</strong>: VMware IMO is the best candidate for any form of virtualization, whether it be your test/dev environments or your Tier 1 mission critical applications.  In fact, Microsoft SQL 2008 is fully supported on VMware ESX 3.5, as well as ERP software from SAP.   Whats funny is how he comments on clustered guests are not supported for vMotion &#8212; Hyper-V does not even have a vMotion type offering.  Their live migration actually suspends the guest then migrates and starts it up.  VMware&#8217;s product offering makes virtualizing your mission critical applications more of a reality than any Microsoft virtualization offering.
</p>

<p style="padding-left: 30px;">
  <strong>Product Hypervisor Technology</strong>: This is another section that just confuses me.  He is stating that because VMware ESX only has a small set of drivers it loads and supports it means that Hyper-V is better.  This goes back to Driver Support above &#8212;  IMO I would much rather have a hypervisor that is extremely thin and secure &#8212; Not a Windows Kernel with 45,000 drivers and Patch Tuesday.  If you look at the VMware HCL, it is extremely thorough and includes a lot of systems &#8211; any company that uses hardware from the major vendors (Dell, HP, Sun, Fujitsu, IBM, etc) will most likely have no problem finding their system on the list.
</p>

Alright, well I just wanted to throw this out there with my comments.  My biggest concern is the lack of knowledge out there.  We have people blogging about things they truly have no clue about and the worse part is there could be people out there that are looking for answers &#8212; then they find views like this.  It makes the possibility of making extremely bad decisions a reality. I hope that if you are one of those people out there looking for answers to your questions that you truly do your homework and thoroughly investigate all your options.

I am not knocking Hyper-V or any of the Microsoft products in any way, I feel that they have their place in the market just like all the other hypervisors. I just truly feel that VMware has a solid product that a lot of companies can benefit from.  We will always have these independent consulting agencies and other &#8220;bloggers&#8221; that preach incorrect information and other FUD (fear, uncertainty & doubt) to push companies into making bad decisions.