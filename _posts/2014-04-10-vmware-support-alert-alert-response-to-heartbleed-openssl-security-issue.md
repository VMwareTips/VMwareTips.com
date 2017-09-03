---
id: 2313
title: 'VMware Support Alert &#8211; ALERT: Response to Heartbleed OpenSSL security issue'
date: 2014-04-10T08:13:57+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2313
permalink: /2014/04/10/vmware-support-alert-alert-response-to-heartbleed-openssl-security-issue/
ratings_users:
  - "1"
ratings_score:
  - "5"
ratings_average:
  - "5"
views:
  - "1252"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
<img class="alignleft size-full wp-image-6136" src="http://bit.ly/1kvpdPN" alt="heartbleed" width="68" height="82" />

This week, a new vulnerability was discovered affecting SSL, a protocol most of the Internet uses to encrypt and secure communications. The VMware Security Engineering, Communications, and Response group (vSECR) is investigating the OpenSSL issue dubbed “Heartbleed”. For information on which VMware products may be affected and resolution/remediation steps, refer to the two KB articles at the bottom of this post.

For the curious, we would like to quickly explain why this particular vulnerability could be a risk across the Internet. The bug — dubbed “Heartbleed” — allows anybody to read the memory on a system that is supposed to be protected by SSL.

An anonymous attacker could potentially steal any information from an SSL-secured communication when the issue is not addressed. Best practices dictate that websites and web service providers should always use SSL-encrypted communication when dealing with sensitive information like usernames, passwords, and bank info. Heartbleed could breach that information to anybody who knows how to extract it without leaving a trace.

  * **For details and updates on VMware products affected, refer to KB article: <a href="http://bit.ly/1kvpdPP" target="_blank">Response to OpenSSL security issue CVE-2014-0160/CVE-2014-0346 a.k.a: “Heartbleed” (2076225)</a>**
  * **For details and updates on VMware Customer Portals and websites, refer to KB article: <a href="http://bit.ly/1gbKKpc" target="_blank">Impact of OpenSSL security issue CVE-2014-0160/CVE-2014-0346 a.k.a: “Heartbleed” on VMware Customer Portals and web sites (2076353)</a>**