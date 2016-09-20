---
id: 446
title: Defunct cimservera processes freeze VMware ESX 3.5
date: 2009-01-06T15:29:18+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=446
permalink: /2009/01/06/defunct-cimservera-processes-freez-vmware-esx-35/
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
  - 4982
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Monitoring
tags:
  - cimservera
  - esx
  - pegasus
  - service console
---
Earlier today <a href="http://www.ivobeerens.nl/?p=255" target="_blank">Virtual IEF</a> posted a blog about not being able to access an ESX host, not by ssh, not by VIC and not even through vCenter.  Evidently this is caused by the hardware monitoring agents (HP, Dell, etc) auto-detecting the management server and failing authentication.  This causes cimservera to be spawned hundreds if not thousands of times thus causing so much CPU and Network traffic locally that it cannot respond within the thresholds for SSH, or VPX agents.

<!--more-->

<div>
  Cimservera is an authentication daemon and a defect was discovered that leaves the defunct process on failed login. This issue is <strong>not</strong> specific to certain management agents. This was observed to happen on idling VMware ESX hosts with hardware management agents installed and discovered by their corresponding management application. High number of the defunct processes could result in various symptoms resulting from the VMware ESX Service Console failing to spawn new processes.
</div>

<div>
  Symptoms include:
</div>

  * <div>
      Unable to login through SSH to VMware ESX host
    </div>

  * <div>
      Unable to login on local Service console
    </div>

  * <div>
      HA errors.
    </div>

<div>
  If you are able to logon to the Service Console, you may verify this issue via the following command which might show from few up to few thousands of cimservera defunct processes:
</div>

<div>
  # ps -ef
</div>

<div>
  root 6232 0.0 0.0 0 0 ? Z Sep24 0:00 [cimservera <defunct>]<br /> root 6377 0.0 0.0 0 0 ? Z Sep24 0:00 [cimservera <defunct>]<br /> root 6496 0.0 0.0 0 0 ? Z Sep24 0:00 [cimservera <defunct>]
</div>

<div>
  In addition, /var/log/messages will show the failed logins
</div>

<div>
  Nov 17 18:29:32 blr-cpd-018 cimservera[505]: user &#8220;root&#8221; failed to authenticate<br /> Nov 17 18:29:34 blr-cpd-018 cimservera[506]: user &#8220;root&#8221; failed to authenticate<br /> Nov 17 18:29:36 blr-cpd-018 cimservera[507]: user &#8220;root&#8221; failed to authenticate<br /> Nov 17 18:29:39 blr-cpd-018 cimservera[508]: user &#8220;root&#8221; failed to authenticate
</div>

To resolve this issue you need to login to the console of the host and restart the pegasus service;

<div style="padding-left: 30px;">
  # <strong>service pegasus restart</strong>
</div>

<div>
  More information on this can be found in <a href="http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1007887" target="_blank">VMware KB 1007887</a>
</div>