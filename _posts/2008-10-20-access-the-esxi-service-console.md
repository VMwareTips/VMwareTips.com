---
id: 128
title: Access the ESXi Service Console
date: 2008-10-20T16:37:27+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=128
permalink: /2008/10/20/access-the-esxi-service-console/
views:
  - 55597
ratings_users:
  - 8
ratings_score:
  - 39
ratings_average:
  - 4.88
dsq_thread_id:
  - 5156597460
categories:
  - ESXi 3.5 Tips
  - VMware
tags:
  - esxi
  - inetd
  - service console
  - ssh
---
<span style="color: #888888;">Here is a brief write-up on how to access the Service Console of VMware ESXi. As a disclaimer, this should only be done under the direct supervision of a VMware Support Engineer.</span>

<span style="color: #888888;"><!--more--></span>

  1. <span style="color: #888888;">From the ESXi console summary screen hit <strong>ALT-F1<span style="font-weight: normal;">.</span></strong></span>
  2. <span style="color: #888888;"><strong><span style="font-weight: normal;">Enter the word &#8220;</span>unsupported<span style="font-weight: normal;">&#8221; (without quotes).</span></strong></span>
  3. <span style="color: #888888;"><strong><span style="font-weight: normal;">Enter in the root password for your system.</span></strong></span>
  4. <span style="color: #888888;"><strong><span style="font-weight: normal;">Be careful<strong> </strong></span></strong></span>

<span style="color: #888888;">Now edit the inetd.conf file to enable remote SSH into this console;</span>

  1. <span style="color: #888888;">Edit /etc/inetd.conf (<strong>vi /etc/inetd.conf</strong>).</span><span style="color: #888888;"><br /> </span>
  2. <span style="color: #888888;">Remove the # sign in front of the SSH line.</span><span style="color: #888888;"><br /> </span>
  3. <span style="color: #888888;">Kill and restart the inetd process.<br /> 1.) ps -ef |grep inetd<br /> 2.) kill -HUP <pid><br /> # pid is the Process ID, the first number displayed from ps -ef</span>
  4. <span style="color: #888888;">SSH into the IP of your ESXi server, using your root login/password.</span>