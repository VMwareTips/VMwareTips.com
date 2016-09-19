---
id: 2835
title: 'VMware Support Alert &#8211; ALERT: Products with public CA certificates expiring Nov.1 | Are you affected?'
date: 2015-10-20T08:59:24+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=2835
permalink: /2015/10/20/vmware-support-alert-alert-products-with-public-ca-certificates-expiring-nov-1-are-you-affected/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 33799
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
<a style="float: right;" href="/tp/.a/6a00d8341c328153ef01543330c84d970c-pi"><br /> </a>

Starting **November 1st 2015**, public Certificate Authorities (CA) will no longer issue certificates with a subjectAltName extension or Subject commonName field containing a Reserved IP Address or Internal Name.

Effective **<span class="highlight begin selected">Octo</span><span class="highlight end selected">ber 1st</span> 2016**, CAs shall revoke all unexpired Certificates whose subjectAlternativeName extension or Subject commonName field contains a Reserved IP Address or Internal Name.

While this change is not VMware specific, VMware Administrators still need to be aware of the this change and understand if they are impacted. For this reason, we have created the following KB article, and urge you to familiarize yourself with it-

<a href="http://vmw.re/1MBKvDF" target="_blank">Frequently asked questions about Public Certificate Authority certificates with Internal Server Names and VMware Products (2134735)</a>

Any updates to this information will be made in the KB article itself.