---
redirect_url: /productinfo/vs2017-system-requirements-vs
---

# Visual Studio 2017 Product Family System Requirements

The minimum system requirements for the Visual Studio 2017 family of products is below. For information about everything 
that's new in this release, see the [Visual Studio 2017 release notes](https://www.visualstudio.com/news/releasenotes/vs2017-relnotes). 
See also [Visual Studio 2017 Platform Targeting and Compatibility](https://www.visualstudio.com/productinfo/vs2017-compatibility-vs).

## Visual Studio 2017

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
  <td>**Supported Operating Systems**</td>
  <td>Visual Studio 2017 will install and run on the following operating systems:
    <ul>
      <li>Windows 10 version 1507 or higher: Home, Professional, and Enterprise</li>
      <li>Windows Server 2016: Standard and Datacenter</li>
      <li>Windows 8.1 (with [Update 2919355](https://support.microsoft.com/kb/2919355)): Basic, Professional, and Enterprise</li>
      <li>Windows Server 2012 R2 (with [Update 2919355](https://support.microsoft.com/kb/2919355)): Essentials, Standard, Datacenter</li>
      <li>Windows 7 SP1 (with Update [3033929](https://support.microsoft.com/kb/3033929)): Home Premium, Professional, Enterprise, Ultimate</li>
  </ul></td>
</tr>
<tr>
  <td>**Hardware**</td>
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
  <td>**Supported Languages**</td>
  <td>
    Visual Studio is available in the following languages:
    <ul>
      <li>English, Chinese (Simplified), Chinese (Traditional), Czech, French, German, Italian, Japanese, Korean, Polish, Portuguese (Brazil), Russian, Spanish, Turkish</li>
    </ul>
    You can select the language of Visual Studio during installation.  
    The Visual Studio Installer is available in the same fourteen languages, and will match the language of Windows, if available.  
    **Note:** Visual Studio Team Foundation Server Office Integration 2017 is available in the ten languages supported by Visual Studio Team Foundation Server 2017.
  </td>
</tr>
<tr>
  <td>**Additional Requirements**</td>
  <td>
    <ul>
      <li>.NET Framework 4.5 is required to install Visual Studio. Visual Studio requires .NET Framework 4.6.1, 
          which will be installed during setup.</li>
      <li>Internet Explorer 11 or Edge is required for internet-related scenarios. [Some features](https://go.microsoft.com/fwlink/?linkid=833023) 
          might not work unless these, or a later version, are installed.</li>
      <li>For emulator support, Windows 8.1 Pro or Enterprise (x64) editions are required. A processor that supports 
          Client Hyper-V and Second Level Address Translation (SLAT) is also required.</li>
      <li>Universal Windows app development, including designing, editing, and debugging, requires Windows 10. Windows Server 2016 and Windows Server 2012 R2 
          may be used to build Universal Windows apps from the command line.</li>
      <li>Team Foundation Server 2017 Office Integration requires Office 2016, Office 2013, or Office 2010.</li>
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
  <td>**Supported Operating Systems**</td>
  <td>Visual Studio Team Foundation Server 2017 will install and run on the 64-bit versions of the following operating systems:
    <ul>
      <li>Windows 10 version 1507 or higher: Home, Professional, and Enterprise</li>
      <li>Windows Server 2016: Standard and Datacenter</li>
      <li>Windows Server 2012 R2 (with [Update 2919355](https://support.microsoft.com/kb/2919355)): Essentials, Standard, Datacenter</li>
      <li>Windows 8.1 (with [Update 2919355](https://support.microsoft.com/kb/2919355)): Basic, Professional, and Enterprise</li>
      <li>Windows Server 2012: Essentials, Standard, Datacenter</li>
      <li>Windows Server 2008 R2 SP1: Standard, Enterprise, Datacenter</li>
      <li>Windows 7 SP1 (with Update [3033929](https://support.microsoft.com/kb/3033929)): Home Premium, Professional, Enterprise, Ultimate</li>
    </ul>
  </td>
</tr>
<tr>
  <td>**Hardware**</td>
  <td>For hardware recommendations on single-server and multi-server deployments, see 
    [Visual Studio Team Foundation Server Requirements and Compatibility](https://go.microsoft.com/fwlink/?LinkId=808683).</td>
</tr>
<tr>
  <td>**Supported Languages**</td>
  <td>
    Visual Studio Team Foundation Server is available in the following languages:
    <ul>
      <li>English, Chinese (Simplified), Chinese (Traditional), French, German, Italian, Japanese, Korean, Russian, Spanish</li>
    </ul>
  </td>
</tr>
<tr>
  <td>**Additional Requirements**</td>
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

## Remote Tools, Performance Tools, and IntelliTrace Standalone Collector for Visual Studio 2017

The Remote Tools, Performance Tools, and IntelliTrace Standalone Collector support the same system requirements as Visual Studio with the following changes:

* Also installs on Windows Server 2012 and Windows Server 2008 R2 SP1
* Requires a 1.6 GHz or faster processor
* Requires 1 GB of RAM (1.5 GB if running on a virtual machine)
* Requires 1 GB of available hard disk space
* Requires 1024 by 768 or higher display resolution
* For the best experience, use the most recent update of these diagnostic tools for your version of Visual Studio

## Microsoft Visual Studio Build Tools 2017

The Build Tools support the same system requirements as Visual Studio with the following changes:

* Also installs on Windows Server 2012 and Windows Server 2008 R2 SP1
* Requires 250 MB to 2.1 GB of available hard disk space

## Microsoft Visual C++ Redistributable for Visual Studio 2017

The Visual C++ Redistributable supports the same system requirements as Visual Studio with the following changes:

* Also installs on Windows Server 2012, Windows Server 2008 R2 SP1, Windows Vista SP2, Windows Server 2008 SP2, Windows Server 2003 SP2, and Windows XP SP3
* Requires 1 GB of RAM (1.5 GB if running on a virtual machine)
* Requires 50 MB of available hard disk space
