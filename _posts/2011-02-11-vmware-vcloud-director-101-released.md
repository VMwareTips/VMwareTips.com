---
id: 1277
title: VMware vCloud Director 1.0.1 Released
date: 2011-02-11T19:24:13+00:00
author: "Rick Scherer"
layout: single
guid: http://vmwaretips.com/wp/?p=1277
permalink: /2011/02/11/vmware-vcloud-director-101-released/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 1441
categories:
  - Cloud
tags:
  - hybrid cloud
  - private cloud
  - public cloud
  - vcloud
  - vcloud director
---
VMware has released their first update to their vCloud Director product, the main focus of this update was to include support for the newly released vSphere 4.1 U1 update. There are a few other enhancements as well as some bug fixes. The other enhancements include Internationalization (I18N) Level 1 Support as well as support for IP Translation for Organization Networks.

For those of you that do not know what vCloud Director is, it provides the interface, automation, and management required by enterprises and service providers to build private and public clouds. vCloud Director supports multi tenancy/organizational isolation, allows for the creation of central application catalogs and personalization of templates, enables creation and deployment of vApps from catalogs/templates, controls user resource usage through roles/rights, quotas and leases, enables programmatic control through the RESTful vCloud API and provides an additional level of abstraction from underlying hardware

#### Internationalization (I18N) Level 1 Support

vCloud Director 1.0.1 complies with I18N Level 1. Although vCloud Director is not localized, it can run on non-English operating systems and handle non-English text. See <a href="http://www.vmware.com/support/vcd/doc/rel_notes_vcloud_director_101.html#i18nissues" target="_blank">I18N Issues</a> in the product release notes for known issues.

#### IP Translation for Organization Networks

vCloud Director 1.0.1 allows you to add IP translation rules for organization networks. When you create an IP translation rule for a network, vCloud Director adds a DNAT and SNAT rule to the vShield Edge associated with the network&#8217;s port group. The DNAT rule translates an external IP address to an internal IP address for inbound traffic. The SNAT rule translates an internal IP address to an external IP address for outbound traffic. If the network is also using IP masquerade, the SNAT rule takes precedence.

All of the information available from this release, including known issues, resolved issues and upgrade instructions can be found within the <a href="http://www.vmware.com/support/vcd/doc/rel_notes_vcloud_director_101.html" target="_blank">release notes</a>.

For some further reading pleasure you can read my post on <a href="http://vmwaretips.com/wp/2011/02/08/the-cloudnow-closer-than-ever/" target="_blank">vCloud Connector</a> which enables customers of Public Cloud providers running vCloud Director to effectively manage their Hybrid Cloud environment from right inside of the vSphere Client.