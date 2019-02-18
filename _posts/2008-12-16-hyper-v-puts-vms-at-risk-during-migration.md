---
id: 379
title: Hyper-V Puts VMs At Risk During Migration
date: 2008-12-16T17:22:57+00:00
author: Rick Scherer
layout: post
guid: https://www.vmwaretips.com/wp/?p=379
permalink: /2008/12/16/hyper-v-puts-vms-at-risk-during-migration/
redirect_from: /wp/2008/12/16/hyper-v-puts-vms-at-risk-during-migration/
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
views:
  - "2248"
categories:
  - Good Reading
  - Hyper-V
  - VMware
tags:
  - cpu
  - crash
  - esx
  - hyper-v
  - video
  - vmotion
---
A very cool video was sent over to me by an employee of VMware, it shows in a demo of Hyper-V an application failure because Hyper-V did not check the CPU compatibility prior to migration.  The origin host had the SSE4.1 instruction set, the destination did not.  Once migrated the application failed and crashed.  Later in the demo it shows a vMotion attempt of the same style, the CPU compatibility checking done during the vMotion process denied it to complete.

See it for yourself: <a href="http://www.vmware.com/technology/whyvmware/resources/cpu-feature-migration-checks.html" target="_blank">Click here to Launch</a>