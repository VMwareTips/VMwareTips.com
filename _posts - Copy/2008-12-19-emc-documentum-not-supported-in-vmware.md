---
id: 403
title: EMC Documentum not supported in VMware
date: 2008-12-19T16:54:12+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=403
permalink: /2008/12/19/emc-documentum-not-supported-in-vmware/
redirect_from: /wp/2008/12/19/emc-documentum-not-supported-in-vmware/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "4831"
dsq_thread_id:
  - "5156589340"
categories:
  - Good Reading
  - VMware
tags:
  - documentum
  - EMC
  - support
  - VMware
---
How could this be?!  EMC, owner of VMware does not support its own product to run virtualized?  You got it daddy-o!

We are currently working on an upgrade of Documentum and we need a new home for the full-text index search module of Documentum, we asked EMC support if we can virtualize this piece, they told us no.  Reference support note 43361 and line #5 clearly states _If Index Server is running on VMware, this is not supported._

I really hope someone at VMware or EMC  can collaborate on this and get it resolved.  I know that EMC recently purchased Documentum, but a top priority would be to make sure all of their products work together in harmony.

Another sad day in the vSphere for me. (no pun intended)