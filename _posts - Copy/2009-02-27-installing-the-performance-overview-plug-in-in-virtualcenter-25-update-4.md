---
id: 630
title: Installing the Performance Overview Plug-In in VirtualCenter 2.5 Update 4
date: 2009-02-27T07:10:05+00:00
author: Rick Scherer
layout: post
guid: http://vmwaretips.com/wp/?p=630
permalink: /2009/02/27/installing-the-performance-overview-plug-in-in-virtualcenter-25-update-4/
redirect_from: /wp/2009/02/27/installing-the-performance-overview-plug-in-in-virtualcenter-25-update-4/
aktt_notify_twitter:
  - 'yes'
ratings_users:
  - "0"
ratings_score:
  - "0"
ratings_average:
  - "0"
aktt_tweeted:
  - "1"
views:
  - "8804"
dsq_thread_id:
  - "5156591346"
categories:
  - ESX 3.5 Tips
  - ESXi 3.5 Tips
  - Monitoring
tags:
  - overview
  - performance
  - plug-in
  - vcenter
---
For those of you upgrading to vCenter 2.5 U4 and and are planning to use the new Performance Overview Plugin, there are some additional steps required to making this work.  Pretty much the biggest thing is that you need the Java Development Kit installed on the vCenter server. All of this is covered in <a href="http://kb.vmware.com/kb/1008296" target="_blank">VMware KB 1008296</a>, but for your convenience I&#8217;ve included the steps here.

<!--more-->

<div>
  <strong>Prior to installing the Performance Overview plug-in:</strong>
</div>

  1. Copy the VirtualCenter 2.5 Update 4 build to the VirtualCenter Server system.
** 
    
    Note</strong>: If the contents of the folders <tt>vpx\perfCharts</tt> (iso) or <tt>bin\perfCharts</tt> (ZIP) are not copied to the local drive of the VirtualCenter Server, an <tt>Access Denied</tt> error appears when the <tt>install.bat</tt> command is run later in the installation process.</li> 
    
      * If you are upgrading to VirtualCenter 2.5 Update 4, stop the VMware Infrastructure Web Access service before upgrading the VirtualCenter.
      * Install or upgrade to VirtualCenter 2.5 Update 4 and start the VMware Infrastructure Web Access service.
      * Download <a href="https://cds.sun.com/is-bin/INTERSHOP.enfinity/WFS/CDS-CDS_Developer-Site/en_US/-/USD/ViewProductDetail-Start?ProductRef=jdk-6u11-oth-JPR@CDS-CDS_Developer" target="_blank"><span style="color: #003399;">Java SE Development Kit 6u11</span></a>, and install JDK 1.6.
      * Configure the environment variables: <ol type="a">
          <li>
            Right-click <strong>My Computer</strong> and click <strong>Properties</strong>.
          </li>
          <li>
            In the <strong>Advanced</strong> tab, click <strong>Environment Variables</strong>.
          </li>
          <li>
            In the System variable list, select <strong>Path</strong> and click <strong>Edit</strong>.
          </li>
          <li>
            In <strong>Variable value</strong>, append <p>
              <tt>C:\Program Files\Java\jdk1.6.0_11\bin\</p> 
              
              <p>
                </tt>If an older version of JRE is present, run the following command in the command window:<tt></p> 
                
                <p>
                  set path=C:\Program Files\Java\jdk1.6.0_11\bin\;%path%<br /> </tt></li> 
                  
                  <li>
                    <div>
                      In the System variable list, select <strong>JAVA_HOME</strong> and click <strong>Edit.</p> 
                      
                      <p>
                        </strong>If JAVA_HOME does not exist, click <strong>New</strong> and in the <strong>Variable name</strong>, enter JAVA_HOME.</div> </li> 
                        
                        <li>
                          <div>
                            In <strong>Variable value</strong>, enter <tt>C:\Program Files\Java\jdk1.6.0_11<br /> </tt>
                          </div>
                        </li>
                        
                        <li>
                          <div>
                            Log out and log back in to the VirtualCenter Server.
                          </div>
                        </li></ol> </li> </ol> 
                        
                        <div>
                          <strong>To install the Performance Overview plug-in:</strong>
                        </div>
                        
                        <ol>
                          <li>
                            In the command window of VirtualCenter Server system, go to the <tt>vpx/perfCharts</tt> folder, the location where the Performance Overview plug-in is available.<br /> If you are using the ZIP file, go to the <tt>bin\perfCharts</tt> folder.
                          </li>
                          <li>
                            Run <tt>install.bat <VirtualCenter_Username> <VirtualCenter_Password></tt>
                          </li>
                        </ol>
                        
                        <div>
                          <strong>Note</strong>:
                        </div>
                        
                        <ul>
                          <li>
                            If the VirtualCenter Server is using the Oracle database, see <a href="http://kb.vmware.com/kb/1008328" target="_blank"><span style="color: #003399;">Performance Overview Plug-In Requirements When VirtualCenter Is Using the Oracle Database (1008328)</span></a>.
                          </li>
                          <li>
                            If the VirtualCenter Server is using the SQL Express Bundled database, see <a href="http://kb.vmware.com/kb/1008329" target="_blank"><span style="color: #003399;">Performance Overview Plug-In Requirements When VirtualCenter Is Using the SQL Express Bundled Database (1008329)</span></a>.
                          </li>
                          <li>
                            If you did not stop the VMware Web Access service before upgrading to VirtualCenter 2.5 Update 4, see <a href="http://kb.vmware.com/kb/1008330" target="_blank"><span style="color: #003399;">Performance Overview Charts Might Fail to Display if VirtualCenter Is Upgraded Without Stopping the VMware Infrastructure Web Access Service (1008330)</span></a>.
                          </li>
                        </ul>