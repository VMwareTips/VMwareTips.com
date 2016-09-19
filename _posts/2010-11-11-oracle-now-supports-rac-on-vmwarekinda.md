---
id: 1228
title: 'Oracle now supports RAC on VMware&#8230;kinda'
date: 2010-11-11T12:07:38+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1228
permalink: /2010/11/11/oracle-now-supports-rac-on-vmwarekinda/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 2248
dsq_thread_id:
  - 5156594332
categories:
  - Good Reading
  - vSphere
tags:
  - oracle
  - rac
  - support
  - VMware
  - vsphere
---
<div class="ciText">
  <p>
    Oracle is finally starting to get it, earlier this week they updated Metalink note 249212.1 to include support for Oracle RAC 11.2.0.2 and later. But as we all know this document also leaves a lot of open ends in terms of supportability.
  </p>
  
  <p>
    The document states;
  </p>
  
  <blockquote>
    <p>
      Oracle has not certified any of its products on VMware virtualized environments. Oracle Support will assist customers running Oracle products on VMware in the following manner: Oracle will only provide support for issues that either are known to occur on the native OS, or can be demonstrated not to be as a result of running on VMware.
    </p>
    
    <p>
      If a problem is a known Oracle issue, Oracle support will recommend the appropriate solution on the native OS.  If that solution does not work in the VMware virtualized environment, the customer will be referred to VMware for support.   When the customer can demonstrate that the Oracle solution does not work when running on the native OS, Oracle will resume support, including logging a bug with Oracle Development for investigation if required.
    </p>
    
    <p>
      If the problem is determined not to be a known Oracle issue, we will refer the customer to VMware for support.   When the customer can demonstrate that the issue occurs when running on the native OS, Oracle will resume support, including logging a bug with Oracle Development for investigation if required.
    </p>
    
    <p>
      NOTE:  Oracle has not certified any of its products on VMware.  For Oracle RAC, Oracle will only accept Service Requests as described in this note on Oracle RAC 11.2.0.2 and later releases.
    </p>
  </blockquote>
  
  <p>
    What does this mean? Well like I said it is a huge step forward (in the right direction) for Oracle. They will provide best effort support for the native (guest) OS and if the problem isn&#8217;t resolved they will deflect to VMware (or you need to recreate on physical). The thing is, I&#8217;m unaware of any circumstance where someone needed to recreate an issue on physical hardware. If you have heard otherwise, please let me know in the comments.
  </p>
  
  <p>
    As far as what I&#8217;m telling my customers&#8230;.the story hasn&#8217;t changed. Oracle runs GREAT on VMware and I highly suggest virtualizing it. Of course there will be exceptions to the rule, but all you gotta do is try it.
  </p>
</div>