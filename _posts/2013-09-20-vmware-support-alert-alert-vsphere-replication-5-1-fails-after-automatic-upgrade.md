---
id: 2177
title: 'VMware Support Alert &#8211; ALERT: vSphere Replication 5.1 fails after automatic upgrade'
date: 2013-09-20T09:32:14+00:00
author: Rick Scherer
layout: single
guid: http://vmwaretips.com/wp/?p=2177
permalink: /2013/09/20/vmware-support-alert-alert-vsphere-replication-5-1-fails-after-automatic-upgrade/
ratings_users:
  - 0
ratings_score:
  - 0
ratings_average:
  - 0
views:
  - 852
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
<span style="font-size: 13px; line-height: 19px;">vSphere Replication in a vSphere 5.1 environment will fail after an automatic upgrade to vSphere Replication 5.5. A pre-release version of vSphere Replication 5.5 has been released and will be downloaded and installed if you have Automatic Check and Install Updates configured. For more information about the issue, see the article linked below.</span>

Symptoms include:

<div>
  <ul>
    <li>
      vSphere Replication fails
    </li>
    <li>
      The vSphere Replication version now says 5.5 instead of 5.1
    </li>
  </ul>
</div>

#### If you experience this issue, contact <a href="http://www.vmware.com/ca/en/support/contacts/" target="_blank">VMware Support</a>.

<div>
  <div>
    <span style="font-size: 13px; line-height: 19px;">To ensure you are not impacted by this issue:</span>
  </div>
  
  <ol>
    <li>
      Log into the vSphere Replication Appliance.
    </li>
    <li>
      Click the <strong>Update</strong> tab.
    </li>
    <li>
      Click <strong>Settings</strong>.
    </li>
    <li>
      Choose <strong>No Automatic Updates</strong>.
    </li>
  </ol>
  
  <div>
    <div>
      vCenter Update Manager may also have this version downloaded. <strong>VMware recommends not installing the vSphere 5.5 Replication version in your 5.1 environment.</strong>
    </div>
    
    <div>
    </div>
    
    <div>
      <span style="font-size: 13px; line-height: 19px;">For more information, see this KB article: </span><a style="font-size: 13px; line-height: 19px;" href="http://kb.vmware.com/kb/2060190" target="_blank">http://kb.vmware.com/kb/2060190</a>
    </div>
  </div>
</div>