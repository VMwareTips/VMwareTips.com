---
id: 487
title: SSH from ESX host to ESX host with No Password
date: 2009-01-16T14:04:59+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=487
permalink: /2009/01/16/ssh-from-esx-host-to-esx-host-with-no-password/
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
  - 8974
dsq_thread_id:
  - 5156597143
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Security
tags:
  - dsa
  - esx
  - keygen
  - password
  - ssh
---
Sometimes you need to script a job that SSH&#8217;s into another ESX host, problem is you will be prompted for a password&#8212;pretty much taking out all the automation aspect of a script.

There is a way around this.  Simply generate a public SSH key and place it in an authorized_keys file on your 2nd, 3rd, 4th, etc. ESX host.

<!--more-->

First we generate the key on the host you wish to SSH from:

[root@dpcrcvmesx1 .ssh]# **ssh-keygen -t dsa**
  
Generating public/private dsa key pair.
  
Enter file in which to save the key (/root/.ssh/id_dsa):

Using the default location is just fine.  We then take the contents of the id\_dsa.pub file (located by default in /root/.ssh/) and place it into a file called authorized\_keys which would be in the /root/.ssh/ folder of your destination ESX host.

After this has been done, I can now SSH from my primary ESX host to my secondary without being prompted for a password:

[root@dpcrcvmesx1 root]# ssh dpcrcvmesx2
  
Last login: Fri Jan 16 14:04:19 2009 from vmvc.sannet.gov
  
[root@dpcrcvmesx2 root]#