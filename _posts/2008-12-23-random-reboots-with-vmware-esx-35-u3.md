---
id: 432
title: Random Reboots with VMware ESX 3.5 U3
date: 2008-12-23T19:53:36+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=432
permalink: /2008/12/23/random-reboots-with-vmware-esx-35-u3/
ratings_users:
  - 3
ratings_score:
  - 11
ratings_average:
  - 3.67
views:
  - 4600
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - VMware HA
tags:
  - ha
  - reboot
  - vmm
  - VMware
---
<span style="color: #000000;">This goes back to a posting on December 12th about VMware HA&#8217;s Virtual Machine Monitoring <a href="http://vmwaretips.com/wp/2008/12/12/vm-may-unexpectedly-reboot-when-using-ha-with-virtual-machine-monitoring/" target="_blank">rebooting guests after a VMotion</a>, which<a href="http://vmwaretips.com/wp/2008/12/12/vm-may-unexpectedly-reboot-when-using-ha-with-virtual-machine-monitoring/" target="_blank"> </a>was originally brought up by <a href="http://blog.scottlowe.org/2008/12/12/vmware-ha-problem-with-update-3/" target="_blank">Scott Lowe</a> and <a href="http://www.yellow-bricks.com/2008/12/12/vms-may-unexpectedly-reboot-when-using-vmware-ha-with-virtual-machine-monitoring/" target="_blank">Duncan Epping</a>. Well, a reader on Scott&#8217;s site has been talking with him about this problem and even after disabling Virtual Machine Monitoring it hasn&#8217;t gone away.</span>

<span style="color: #000000;"><!--more--></span>

<span style="color: #000000;">Here is the excerpt from Scott&#8217;s website;</span>

> <div class="content">
>   <p>
>     <span style="color: #3366ff;">I’ve been communicating with a reader who is experiencing random reboots of virtual machines on his HA/DRS-enabled cluster running VMware ESX 3.5 Update 3. At first, I thought his problem was related to the bug with VM failure monitoring that I <a href="http://blog.scottlowe.org/2008/12/12/vmware-ha-problem-with-update-3/">discussed here</a>, but upon further discussion the random reboots are continuing to occur even when VM failure monitoring is disabled. The only relief the reader has been able to find thus far has been to completely disable VMware HA on his cluster, which—to be honest—is a less than acceptable solution.</span>
>   </p>
>   
>   <p>
>     <span style="color: #3366ff;">After a little bit of digging around, I turned up <a href="http://communities.vmware.com/thread/178417">this VMware Communities thread</a>, in which several other users also indicate they are seeing the same kinds of problems. The thread closes out by referencing <a href="http://www.yellow-bricks.com/2008/12/12/vms-may-unexpectedly-reboot-when-using-vmware-ha-with-virtual-machine-monitoring/">this post by Duncan Epping</a> regarding the VM failure monitoring bug. Clearly, though, this bug should not be affecting users who do not have VM failure monitoring enabled. I also found <a href="http://www.ivobeerens.nl/?p=180">this blog post</a> about another user having the issue, although it sounds like his problem was solved by disabling VM failure monitoring.</span>
>   </p>
>   
>   <p>
>     <span style="color: #3366ff;">Further research turned up <a href="http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1007501">this KB article on a post-Update 3 patch</a> that may address some of the random reboot issues. Judging from the KB article, it looks like the random reboots may be caused due to an unexpected interaction between VMotion and an option to automatically upgrade VMware Tools. This is just speculation, of course, but the symptoms seem to fit.</span>
>   </p>
>   
>   <p>
>     <span style="color: #3366ff;">Have any other users out there experienced this problem? If so, what was the fix, if any? It sounds like there may be more to this issue than perhaps I first suspected.</span></div> </blockquote> 
>     
>     <p>
>       <span style="color: #000000;">Well, we&#8217;ll need to keep on top of it, but here is one theory that I left as a comment on Scott&#8217;s site;</span>
>     </p>
>     
>     <div class="primary content">
>       <blockquote>
>         <p>
>           <span style="color: #993300;">The VMotion/VMware Tools upgrade theory might be a possibility. Remember, when doing a VMotion the Virtual Machine is actually started on a new host, if VMware Tools is configured to automatically upgrade during boot it is quite possible a “hole” left open in U3 could turn this into an unwanted feature.</span>
>         </p>
>         
>         <p>
>           <span style="color: #993300;">VM Running -> Automatically Upgrade VMware Tools Enabled -> VMotion to New Host -> VMware Tools Upgrade Initiated -> Guest O/S Reboots</span>
>         </p>
>         
>         <p>
>           <span style="color: #993300;">This also makes me think about how in U3 of the Free Edition of ESXi the programmers left the Read/Write RCLI commands in there….. Whats going on over at the VMware QC department ?</span>
>         </p>
>         
>         <p>
>           <span style="color: #993300;">This is all speculation &#8211; I would be curious in knowing if it is the same VMs rebooting, or do they reboot once then never again. This would be more icing on the cake for the VMware Tools theory if it were the latter.</span>
>         </p>
>       </blockquote>
>       
>       <p>
>         <span style="color: #000000;">I will keep you all posted.</span></div>