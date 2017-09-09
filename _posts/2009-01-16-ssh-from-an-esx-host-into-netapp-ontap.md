---
id: 480
title: SSH from an ESX host into NetApp OnTAP
date: 2009-01-16T13:43:06+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=480
permalink: /2009/01/16/ssh-from-an-esx-host-into-netapp-ontap/
redirect_from: /wp/2009/01/16/ssh-from-an-esx-host-into-netapp-ontap/
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
  - "6571"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - NetApp
tags:
  - 3des
  - aes
  - cipher
  - esx
  - firewall
  - NetApp
  - ontap
  - ssh
---
<a href="http://blog.scottlowe.org/2006/12/27/ssh-from-esx-server-to-data-ontap/" target="_blank">Scott Lowe</a> covered this over two years ago but I thought I&#8217;d revisit just in case there is someone out there looking to SSH from their ESX hosts directly into the NetApp OnTAP operating system.

By default, ESX only supports AES encryption, OnTAP requires 3DES encryption. This means we&#8217;ll need to make a modification to the SSH configuration on ESX to have it support 3DES.  If your asking why would I want this, sometimes it comes in real handy to run OnTAP commands direct from your ESX command-line.  For example, if you want to see how much space an aggregate has left you can simply type; _ssh fas1 df -Ag aggr0_ &#8212; or if you want to grow the size of your LUN; _ssh fas1 lun resize /vol/vol#/qtree/lun# 500g &#8212;_ Anyways, the possibilities are endless.



To modify the ciphers supported by ESX Server, edit the /etc/ssh/ssh_config file and change this line;

`Ciphers aes256-cbc,aes128-cbc`

Instead, it should look like this;

`Ciphers aes256-cbc,aes128-cbc,3des-cbc`

This will enable SSH connections from the ESX Server to the SSH daemon running in Data OnTAP. Also make sure you have enabled SSH traffic through the ESX firewall;

`esxcfg-firewall -e sshClient`

And, of course, you’ll need to configure and enable SSH access on the NetApp storage system itself using the secureadmin command in Data OnTAP;

`secureadmin setup ssh<br />
secureadmin enable ssh2`

Once SSH is reconfigured on ESX Server and configured/enabled in Data OnTAP, then using SSH to run commands remotely from ESX Server to the NetApp storage system should work without any problems.

One final step would be to enable SSH from your ESX host to OnTAP without being asked for a password.  This is pretty simple,  on your ESX host you would do a keygen of a DSA key, you would then put the public key in the authorized keys file of the root user:

On your ESX host generate your key:

ssh-keygen -t dsa

It will ask you were to save the file(s), the default location is fine.

Then take the contents of the id\_dsa.pub file and put that into the authorized\_keys file on your NetApp filer.