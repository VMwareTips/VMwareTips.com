---
id: 1810
title: 'VMware Support Alert &#8211; Implementing CA signed SSL certificates with vSphere 5.1'
date: 2012-10-31T14:05:42+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=1810
permalink: /2012/10/31/vmware-support-alert-implementing-ca-signed-ssl-certificates-with-vsphere-5-1/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 4005
dsq_thread_id:
  - 5156597921
categories:
  - Alert
  - Security
  - vCenter
  - vSphere
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
In our effort to provide our viewers with up to the minute information on VMware related news and topics, we&#8217;re posting the following Special Alert direct from VMware Support Insider.

<img class="size-full wp-image-3782 alignright" style="margin: 10px 5px; border: 0px currentColor;" title="SSL" src="http://blogs.vmware.com/kb/files/2012/10/SSL-Logo1.gif" alt="SSL" width="194" height="121" />One of the most common things we see in VMware Global Support Services (GSS), regardless of product, version, or customer, is the need to implement **custom certificates**. This could be for a number of reasons:

  * Security
  * To get rid of the warning when you first login
  * You like a challenge

Whatever the case may be, in vSphere 5.1, the process has changed due to the addition of vCenter **Single Sign On** (SSO), which adds complexity to the procedure. This is because the majority of services register themselves to SSO. As a result of changing the certificates, the services also need to be re-registered.

As a result of repeated question from customers coming in on this, we gathered our Professional Services, Engineering, and Technical Writers to develop the following **Resolution Path** to guide you through the various steps through to completion (you can read more about <a href="http://blogs.vmware.com/kb/2010/08/resolution-paths-what-are-they-and-why-do-i-care.html" target="_blank">resolution path articles here</a>).

### Resolution Path Article:

  * <a href="http://kb.vmware.com/kb/2034833" target="_blank">Implementing CA signed SSL certificates with vSphere 5.1 (2034833)</a> <– Start Here!

### Child articles in the resolution path are:

  * <a href="http://kb.vmware.com/kb/2037432" target="_blank">Creating certificate requests and certificates for the vCenter 5.1 components (2037432)</a>
  * <a href="http://kb.vmware.com/kb/2035011" target="_blank">Configuring CA signed SSL certificates for vCenter SSO in vCenter 5.1 (2035011)</a>
  * <a href="http://kb.vmware.com/kb/2035009" target="_blank">Configuring CA signed SSL certificates for the Inventory service in vCenter 5.1 (2035009)</a>
  * <a href="http://kb.vmware.com/kb/2035005" target="_blank">Configuring CA signed certificates for vCenter 5.1 (2035005)</a>
  * <a href="http://kb.vmware.com/kb/2035010" target="_blank">Configuring CA signed SSL certificates for the Web Client and Log Browser in vCenter 5.1 (2035010)</a>
  * <a href="http://kb.vmware.com/kb/2037581" target="_blank">Configuring CA signed SSL certificates for vSphere Update Manager in vCenter 5.1 (2037581)</a>
  * <a href="http://kb.vmware.com/kb/2015499" target="_blank">Configuring CA signed SSL certificates with ESXi 5.x hosts (2015499)</a>

> **Note**: It is recommended that you follow the articles in the sequence provided as many steps are dependent on each other.

We have also created an article with the steps for vCenter Server Appliance 5.1:

  * <a href="http://kb.vmware.com/kb/2036744" target="_blank">Configuring certificates signed by a Certificate Authority(CA) for vCenter Server Appliance 5.1 (2036744)</a>

Finally, we have updated these vSphere 5.0 articles thanks to feedback received on them:

  * <a href="http://kb.vmware.com/kb/2015383" target="_blank">Implementing CA signed SSL certificates with vSphere 5.0 (2015383)</a>
  * <a href="http://kb.vmware.com/kb/2015387" target="_blank">Configuring OpenSSL for installation and configuration of CA signed certificates in the vSphere environment (2015387)</a>
  * <a href="http://kb.vmware.com/kb/2015421" target="_blank">Configuring CA signed certificates for VMware vCenter Server 5.0.x (2015421)</a>
  * <a href="http://kb.vmware.com/kb/2015499" target="_blank">Configuring CA signed certificates for ESXi 5.x hosts (2015499)</a>

> **Note**: The vCenter Service fails to start up issue is now resolved in vCenter Server 5.1.0a. For more details, refer to KB article:
  
> <a href="http://kb.vmware.com/kb/2035623" target="_blank">vCenter Server Services hang on startup after upgrading to vCenter Server 5.1 (2035623)</a>.

We hope that this helps everyone through their SSL implementation. If you find any errors or anomalies, there’s a feedback form at the bottom of every article. We will be keeping an active eye on your feedback!