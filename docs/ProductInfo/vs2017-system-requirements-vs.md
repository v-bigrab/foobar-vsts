---
title: Visual Studio 2017 System Requirements
description: Visual Studio 2017 System Requirements
keywords: visualstudio
author: pchapman
ms.author: pchapman
manager: sacalla
ms.date: 7/24/2017
ms.topic: release-article
ms.prod: visual-studio-dev15
ms.service: visualstudio
ms.assetid: 1883171b-6f5e-4a28-97de-882da08aa664
---

# <a id="top"> </a> Visual Studio 2017 Product Family System Requirements

The minimum system requirements for the Visual Studio 2017 family of products is below. For information on compatibility, see [Visual Studio 2017 Platform Targeting and Compatibility](/productinfo/vs2017-compatibility-vs).

### What's New 
For information about features included in this release, see the following:
* For Windows, [Visual Studio IDE](https://www.visualstudio.com/vs/), the [Visual Studio 2017 release notes](/news/releasenotes/vs2017-relnotes), or [What's New in Visual Studio 2017](https://docs.microsoft.com/visualstudio/ide/whats-new-in-visual-studio).
* For Mac, [What’s New in Visual Studio for Mac](https://www.visualstudio.com/vs/visual-studio-mac/) or the [Visual Studio 2017 for Mac release notes](https://www.visualstudio.com/news/releasenotes/vs2017-mac-relnotes). 
* [Visual Studio Team Services](https://www.visualstudio.com/team-services/).
* [Visual Studio Code](https://code.visualstudio.com/) or the [release notes](https://code.visualstudio.com/updates).  

### Download
To install Visual Studio 2017, see [Visual Studio 2017 Downloads](https://www.visualstudio.com/downloads). 

### Older versions
For older versions of Visual Studio, see the system requirements for [Visual Studio 2015](https://www.visualstudio.com/productinfo/vs2015-sysrequirements-vs), 
[Visual Studio 2013](https://www.visualstudio.com/productinfo/vs2013-sysrequirements-vs), or 
[Visual Studio 2012](https://www.visualstudio.com/productinfo/vs2013-sysrequirements-vs#a-idvs2012-a-visual-studio-2012).

### Feedback and Support
For support, or to submit feedback on Visual Studio, see:
* [Visual Studio Support](https://www.visualstudio.com/support/)
* [Submit a product suggestion or idea](https://visualstudio.uservoice.com)
* [Report a problem or bug](https://developercommunity.visualstudio.com/)

## Visual Studio 2017 System Requirements

The following products support the minimum system requirements below:

* Visual Studio Enterprise 2017
* Visual Studio Professional 2017
* Visual Studio Community 2017
* Visual Studio Test Professional 2017
* Visual Studio Test Agent 2017
* Visual Studio Test Controller 2017
* Visual Studio Team Foundation Server Office Integration 2017
* Visual Studio Feedback Client 2017

<table>
<tr>
  <td><p>**Supported Operating Systems**</p></td>
  <td><p>Visual Studio 2017 will install and run on the following operating systems:</p>
    <ul>
      <li>Windows 10 version 1507 or higher: Home, Professional, Education, and Enterprise (LTSB and S are not supported)</li>
      <li>Windows Server 2016: Standard and Datacenter</li>
      <li>Windows 8.1 (with [Update 2919355](https://support.microsoft.com/kb/2919355)): Core, Professional, and Enterprise</li>
      <li>Windows Server 2012 R2 (with [Update 2919355](https://support.microsoft.com/kb/2919355)): Essentials, Standard, Datacenter</li>
      <li>Windows 7 SP1 (with latest Windows Updates): Home Premium, Professional, Enterprise, Ultimate</li>
  </ul></td>
</tr>
<tr>
  <td><p>**Hardware**</p></td>
  <td>
    <ul>
      <li>1.8 GHz or faster processor. Dual-core or better recommended</li>
      <li>2 GB of RAM; 4 GB of RAM recommended (2.5 GB minimum if running on a virtual machine)</li>
      <li>Hard disk space: 1GB to 40GB, depending on features installed</li>
      <li>Video card that supports a minimum display resolution of 720p (1280 by 720); Visual Studio will work best at a resolution of WXGA (1366 by 768) or higher</li>
    </ul>
  </td>
</tr>
<tr>
  <td><p>**Supported Languages**</p></td>
  <td>
    <p>Visual Studio is available in the following languages:</p>
    <ul>
      <li>English, Chinese (Simplified), Chinese (Traditional), Czech, French, German, Italian, Japanese, Korean, Polish, Portuguese (Brazil), Russian, Spanish, Turkish</li>
    </ul>
    <p>You can select the language of Visual Studio during installation. The Visual Studio Installer is available in the same fourteen languages, and will match the language of Windows, if available.</p>
    <p>**Note:** Visual Studio Team Foundation Server Office Integration 2017 is available in the ten languages supported by Visual Studio Team Foundation Server 2017.</p>
  </td>
</tr>
<tr>
  <td><p>**Additional Requirements**</p></td>
  <td>
    <ul>
      <li>.NET Framework 4.5 is required to install Visual Studio. Visual Studio requires .NET Framework 4.6.1, 
          which will be installed during setup.</li>
      <li>[Windows 10 Enterprise LTSB edition](https://technet.microsoft.com/itpro/windows/manage/waas-overview) and [Windows 10 S](https://www.microsoft.com/windows/windows-10-s) are not supported for development. 
          You may use Visual Studio 2017 to build apps that run on Windows 10 LTSB and Windows 10 S.</li>
      <li>Internet Explorer 11 or Edge is required for internet-related scenarios. [Some features](https://go.microsoft.com/fwlink/?linkid=833023) 
          might not work unless these, or a later version, are installed.</li>
      <li>For emulator support, Windows 8.1 Pro or Enterprise (x64) editions are required. A processor that supports 
          Client Hyper-V and Second Level Address Translation (SLAT) is also required.</li>
      <li>Universal Windows app development, including designing, editing, and debugging, requires Windows 10. Windows Server 2016 and Windows Server 2012 R2 
          may be used to build Universal Windows apps from the command line.</li>
      <li>The Server Core and Minimal Server Interface options are not supported when running Windows Server.</li>
      <li>Team Foundation Server 2017 Office Integration requires Office 2016, Office 2013, or Office 2010.</li>
      <li>Xamarin.Android requires a 64-bit edition of Windows and the 64-bit Java Development Kit (JDK).</li> 
      <li>PowerShell 3.0 or higher is required on Windows 7 SP1 to install the Mobile Development with C++, JavaScript, or .NET workloads.</li>
    </ul>
  </td>
</tr>
</table>

## Visual Studio Team Foundation Server 2017

For detailed information on system requirements for various deployment scenarios, and for information on 
integration with Microsoft Office and Microsoft SharePoint, see 
[Visual Studio Team Foundation Server Requirements and Compatibility](https://go.microsoft.com/fwlink/?LinkId=808683). 
The following products support the minimum requirements below:

* Visual Studio Team Foundation Server 2017
* Visual Studio Team Foundation Server Express 2017

<table>
<tr>
  <td><p>**Supported Operating Systems**</td>
  <td><p>Visual Studio Team Foundation Server 2017 will install and run on the 64-bit versions of the following operating systems:</p>
    <ul>
      <li>Windows 10 version 1507 or higher: Home, Professional, and Enterprise</li>
      <li>Windows Server 2016: Standard and Datacenter</li>
      <li>Windows Server 2012 R2 (with [Update 2919355](https://support.microsoft.com/kb/2919355)): Essentials, Standard, Datacenter</li>
      <li>Windows 8.1 (with [Update 2919355](https://support.microsoft.com/kb/2919355)): Core, Professional, and Enterprise</li>
      <li>Windows Server 2012: Essentials, Standard, Datacenter</li>
      <li>Windows Server 2008 R2 SP1: Standard, Enterprise, Datacenter</li>
      <li>Windows 7 SP1 (with latest Windows Updates): Home Premium, Professional, Enterprise, Ultimate</li>
    </ul>
  </td>
</tr>
<tr>
  <td><p>**Hardware**</p></td>
  <td><p>For hardware recommendations on single-server and multi-server deployments, see 
    [Visual Studio Team Foundation Server Requirements and Compatibility](https://go.microsoft.com/fwlink/?LinkId=808683).</p></td>
</tr>
<tr>
  <td><p>**Supported Languages**</p></td>
  <td>
    <p>Visual Studio Team Foundation Server is available in the following languages:</p>
    <ul>
      <li>English, Chinese (Simplified), Chinese (Traditional), French, German, Italian, Japanese, Korean, Russian, Spanish</li>
    </ul>
  </td>
</tr>
<tr>
  <td><p>**Additional Requirements**</p></td>
  <td>
    <ul>
      <li>.NET Framework 4.6.1, which will be installed during setup</li>
      <li>Microsoft SQL Server 2014 or Microsoft SQL Server 2016</li>
      <li>Team Foundation Server Web Client requires Microsoft Microsoft Edge, Internet Explorer 11, Google Chrome, Mozilla Firefox, or Apple Safari</li>
      <li>Team Foundation Server Office Integration requires Office 2016, Office 2013, or Office 2010</li>
    </ul>
  </td>
</tr>
</table>

## Microsoft Visual Studio 2017 for Mac

[Download Visual Studio 2017 for Mac](https://www.visualstudio.com/vs/visual-studio-mac/). For more information, see 
[Visual Studio 2017 for Mac release notes](https://www.visualstudio.com/news/releasenotes/vs2017-mac-relnotes), 
[Visual Studio 2017 for Mac Product Family System Requirements](https://www.visualstudio.com/productinfo/vs2017-system-requirements-mac), 
and [Visual Studio 2017 for Mac Platform Targeting and Compatibility](https://www.visualstudio.com/productinfo/vs2017-compatibility-mac). 

## Microsoft Visual Studio Code

[Dowload Visual Studio Code](https://code.visualstudio.com/). For more information, see [Requirements for Visual Studio Code](https://code.visualstudio.com/docs/supporting/requirements), 
the [release notes](https://code.visualstudio.com/updates), and [Visual Studio Code FAQ](https://code.visualstudio.com/docs/supporting/faq).

## Remote Tools, Performance Tools, and IntelliTrace Standalone Collector for Visual Studio 2017

The Remote Tools, Performance Tools, and IntelliTrace Standalone Collector support the same system requirements as Visual Studio with the following changes:

* Also installs on Windows 10 Enterprise LTSB, Windows Server 2012, and Windows Server 2008 R2 SP1
* Requires a 1.6 GHz or faster processor
* Requires 1 GB of RAM (1.5 GB if running on a virtual machine)
* Requires 1 GB of available hard disk space
* Requires 1024 by 768 or higher display resolution
* For the best experience, use the most recent update of these diagnostic tools for your version of Visual Studio

## Microsoft Visual Studio Build Tools 2017

The Build Tools support the same system requirements as Visual Studio with the following changes:

* Also installs on Windows Server 2008 R2 SP1
* Requires 250 MB to 2.1 GB of available hard disk space

## Microsoft Visual C++ Redistributable for Visual Studio 2017

The Visual C++ Redistributable supports the same system requirements as Visual Studio with the following changes:

* Also installs on Windows 10 Enterprise LTSB, Windows Server 2012, Windows Server 2008 R2 SP1, Windows Vista SP2, Windows Server 2008 SP2, Windows Server 2003 SP2, and Windows XP SP3
* Requires 1 GB of RAM (1.5 GB if running on a virtual machine)
* Requires 50 MB of available hard disk space

<center>[Top of Page](#top)</center>