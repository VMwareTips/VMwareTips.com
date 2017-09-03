---
id: 1344
title: 'vSphere Doesn&#8217;t Like OVF with SCSI ID of X:15'
date: 2011-06-14T17:06:39+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=1344
permalink: /2011/06/14/vsphere-doesnt-like-ovf-with-scsi-id-of-15/
ratings_users:
  - "1"
ratings_score:
  - "5"
ratings_average:
  - "5"
views:
  - "2680"
categories:
  - Cloud
  - vSphere
tags:
  - import
  - ovf
  - scsi
  - vcloud
  - vsphere
---
In a very random situation that most customers probably wouldn&#8217;t even encounter, we&#8217;ve came across a bug while importing an OVF that has a VMDK with a SCSI Address of X:15 (ie: SCSI 0:15, SCSI 1:15, etc). It appears that vSphere doesn&#8217;t take kindly to virtual machines being imported that have virtual disks addressed as X:15 and will issue the fatal error _&#8220;Unsupported value &#8217;15&#8217; for element &#8216;addressOnParent&#8217;._ I&#8217;ve tested this with different SCSI Adapters thinking it was perhaps tied to LSI Parallel, this was not the case as it failed with all other adapters.

<a rel="attachment wp-att-1347" href="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture2.png"><img class="aligncenter size-medium wp-image-1347" title="ovf-error-vsphere" src="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture2-300x155.png" alt="" width="300" height="155" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture2-300x155.png 300w, http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture2.png 456w" sizes="(max-width: 300px) 100vw, 300px" /></a>

This issue actually came up initially while attempting to import an OVF into a Catalog within vCloud Director. A similar error appears stating _&#8220;The following error was encountered while processing the OVF file you provided: Unsupported value &#8217;15&#8217; for element &#8216;addressOnParent&#8217;.&#8221;_ 

<a rel="attachment wp-att-1348" href="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture1.png"><img class="aligncenter size-medium wp-image-1348" title="ovf-scsi-vcd" src="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture1-300x276.png" alt="" width="300" height="276" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture1-300x276.png 300w, http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture1.png 572w" sizes="(max-width: 300px) 100vw, 300px" /></a>

You can see the offending line within the actual OVF file shown below, this is tied back to the actual VMDK and what SCSI Bus it resides on, as shown in the picture below the OVF file.

<p style="text-align: center;">
  <a rel="attachment wp-att-1345" href="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture.png"><img class="size-full wp-image-1345 aligncenter" style="margin-top: 5px; margin-bottom: 5px;" title="ovf-file-scsi15" src="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture.png" alt="" width="473" height="105" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture.png 473w, http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture-300x66.png 300w" sizes="(max-width: 473px) 100vw, 473px" /></a>
</p>

<p style="text-align: center;">
  <a rel="attachment wp-att-1346" href="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture3.png"><img class="size-full wp-image-1346 aligncenter" style="margin-top: 5px; margin-bottom: 5px;" title="ovf-fail-vmdk-scsi" src="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture3.png" alt="" width="323" height="58" srcset="http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture3.png 323w, http://vmwaretips.com/wp/wp-content/uploads/2011/06/capture3-300x53.png 300w" sizes="(max-width: 323px) 100vw, 323px" /></a>
</p>

<p style="text-align: left;">
  I&#8217;ve raised the question to VMware Engineering and will hopefully be able to post their response to this issue shortly.
</p>