---
id: 3367
title: 'VMSA-2017-0001 &#8211; AirWatch updates address bypass of root detection and local data encryption'
date: 2017-01-30T15:19:25+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=3367
permalink: /2017/01/30/vmsa-2017-0001-airwatch-updates-address-bypass-of-root-detection-and-local-data-encryption/
redirect_from: /wp/2017/01/30/vmsa-2017-0001-airwatch-updates-address-bypass-of-root-detection-and-local-data-encryption/
ratings_users:
  - "1"
ratings_score:
  - "5"
ratings_average:
  - "5"
views:
  - "2953"
categories:
  - Alert
tags:
  - alert
  - Bug
  - patch
  - support
  - VMware
---
<div>
  Advisory ID: VMSA-2017-0001
</div>

<div>
  Severity:    Important
</div>

<div>
  Synopsis:    AirWatch updates address bypass of root detection and local
</div>

<div>
               data encryption
</div>

<div>
  Issue date:  <span class="aBn" tabindex="0" data-term="goog_451499067"><span class="aQJ">2017-01-30</span></span>
</div>

<div>
  Updated on:  <span class="aBn" tabindex="0" data-term="goog_451499068"><span class="aQJ">2017-01-30</span></span> (Initial Advisory)
</div>

<div>
  CVE number:  CVE-2017-4895, CVE-2017-4896
</div>

<div>
</div>

<div>
  1. Summary
</div>

<div>
</div>

<div>
     AirWatch updates address bypass of root detection and local data
</div>

<div>
     encryption
</div>

<div>
</div>

<!--more-->

<div>
</div>

<div>
  2. Relevant Products
</div>

<div>
</div>

<div>
     Airwatch Agent
</div>

<div>
     Airwatch Console
</div>

<div>
     AirWatch Inbox
</div>

<div>
</div>

<div>
  3. Problem Description
</div>

<div>
</div>

<div>
     a. Root detection bypass
</div>

<div>
</div>

<div>
     Airwatch Agent for Android contains a vulnerability that may allow
</div>

<div>
     a device to bypass root detection during enrollment. Successful
</div>

<div>
     exploitation of this issue may result in an enrolled device having
</div>

<div>
     unrestricted access over local Airwatch security controls and data.
</div>

<div>
</div>

<div>
     VMware would like to thank Finn Steglich from SySS GmbH for reporting
</div>

<div>
     this issue to us.
</div>

<div>
</div>

<div>
     The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org&source=gmail&ust=1485901094156000&usg=AFQjCNF1Bmjggy81AbeDv78KakbZaKEYcw">cve.mitre.org</a>) has
</div>

<div>
     assigned the identifier CVE-2017-4895 to this issue.
</div>

<div>
</div>

<div>
     Column 5 of the following table lists the action required to remediate
</div>

<div>
     the vulnerability in each release, if a solution is available.
</div>

<div>
</div>

<div>
     VMware      Product    Running             Replace with/  Mitigation/
</div>

<div>
     Product     Version    on       Severity   Apply Patch    Workaround
</div>

<div>
     ==========  =========  =======  =========  =============  ==========
</div>

<div>
     Airwatch    x.x        Android  Important  7.0            None
</div>

<div>
     Agent
</div>

<div>
</div>

<div>
     b. Local data encryption bypass
</div>

<div>
</div>

<div>
     Airwatch Inbox for Android contains a vulnerability that may allow
</div>

<div>
     a rooted device to decrypt the local data used by the application.
</div>

<div>
     Successful exploitation of this issue may result in an unauthorized
</div>

<div>
     disclosure of confidential data.
</div>

<div>
</div>

<div>
     VMware would like to thank Finn Steglich from SySS GmbH for reporting
</div>

<div>
     this issue to us.
</div>

<div>
</div>

<div>
     The Common Vulnerabilities and Exposures project (<a href="http://cve.mitre.org/" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org&source=gmail&ust=1485901094156000&usg=AFQjCNF1Bmjggy81AbeDv78KakbZaKEYcw">cve.mitre.org</a>) has
</div>

<div>
     assigned the identifier CVE-2017-4896 to this issue.
</div>

<div>
</div>

<div>
     Column 5 of the following table lists the action required to remediate
</div>

<div>
     the vulnerability in each release, if a solution is available.
</div>

<div>
</div>

<div>
     VMware      Product    Running             Replace with/  Mitigation/
</div>

<div>
     Product     Version    on       Severity   Apply Patch    Workaround
</div>

<div>
     ==========  =========  =======  =========  =============  ==============
</div>

<div>
     Airwatch    x.x        Android  Important  9.0 FP1*       KB115002293928
</div>

<div>
     Console
</div>

<div>
     Airwatch    x.x        Android  Important  2.12*          KB115002293928
</div>

<div>
     Inbox
</div>

<div>
</div>

<div>
     *To remediate this vulnerability, Pin-Based Encryption (PBE) must be
</div>

<div>
      enabled. This feature was introduced in the versions of the Airwatch
</div>

<div>
      Console and Inbox listed in the table above. PBE is also available in
</div>

<div>
      many other Airwatch applications. For more information on PBE please
</div>

<div>
      see: <a href="https://support.air-watch.com/articles/115002156907" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://support.air-watch.com/articles/115002156907&source=gmail&ust=1485901094156000&usg=AFQjCNHtmvU9_nRHOGVvKjknzvT1F-sfTw">https://support.air-watch.com/<wbr />articles/115002156907</a>
</div>

<div>
</div>

<div>
  4. Solution
</div>

<div>
</div>

<div>
     Please review the patch/release notes for your product and version and
</div>

<div>
     verify the checksum of your downloaded file.
</div>

<div>
</div>

<div>
     Airwatch Agent for Android
</div>

<div>
     Downloads and Documentation:
</div>

<div>
</div>

<div>
  <a href="https://play.google.com/store/apps/details?id=com.airwatch.androidagent&hl=" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://play.google.com/store/apps/details?id%3Dcom.airwatch.androidagent%26hl%3D&source=gmail&ust=1485901094156000&usg=AFQjCNFTp0_TA3ciHykSmCk_NSU8X0BldQ">https://play.google.com/store/<wbr />apps/details?id=com.airwatch.<wbr />androidagent&hl=</a>
</div>

<div>
  en
</div>

<div>
</div>

<div>
     Airwatch Inbox for Android
</div>

<div>
     Downloads and Documentation:
</div>

<div>
     <a href="https://play.google.com/store/apps/details?id=com.airwatch.email&hl=en" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://play.google.com/store/apps/details?id%3Dcom.airwatch.email%26hl%3Den&source=gmail&ust=1485901094156000&usg=AFQjCNE2tYkinZWnfZJQlAfPpZp3i1-KVA">https://play.google.com/<wbr />store/apps/details?id=com.<wbr />airwatch.email&hl=en</a>
</div>

<div>
</div>

<div>
  5. References
</div>

<div>
</div>

<div>
     <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4895" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org/cgi-bin/cvename.cgi?name%3DCVE-2017-4895&source=gmail&ust=1485901094156000&usg=AFQjCNFwHejmU36GyT76blJ46CYI54B2yA">http://cve.mitre.org/cgi-bin/<wbr />cvename.cgi?name=CVE-2017-4895</a>
</div>

<div>
     <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-4896" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=http://cve.mitre.org/cgi-bin/cvename.cgi?name%3DCVE-2017-4896&source=gmail&ust=1485901094156000&usg=AFQjCNGfmjmJe07tONMQbdanUOKgThYDvw">http://cve.mitre.org/cgi-bin/<wbr />cvename.cgi?name=CVE-2017-4896</a>
</div>

<div>
     <a href="https://support.air-watch.com/articles/115002293928" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://support.air-watch.com/articles/115002293928&source=gmail&ust=1485901094156000&usg=AFQjCNHTA0eHIhlOVj-fjRRt6Ni2Z5bFbg">https://support.air-watch.<wbr />com/articles/115002293928</a>
</div>

<div>
     <a href="https://support.air-watch.com/articles/115002156907" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&q=https://support.air-watch.com/articles/115002156907&source=gmail&ust=1485901094156000&usg=AFQjCNHtmvU9_nRHOGVvKjknzvT1F-sfTw">https://support.air-watch.<wbr />com/articles/115002156907</a>
</div>

<div>
</div>

<div>
  &#8211; &#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr />&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<wbr />&#8212;&#8212;&#8212;&#8212;&#8211;
</div>

<div>
</div>

<div>
  6. Change log
</div>

<div>
</div>

<div>
     <span class="aBn" tabindex="0" data-term="goog_451499069"><span class="aQJ">2017-01-30</span></span>: VMSA-2017-0001
</div>

<div>
     Initial security advisory.
</div>