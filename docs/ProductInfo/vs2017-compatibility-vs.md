---
title: Visual Studio 2017 Compatibility
description: Visual Studio 2017 Compatibility
keywords: visualstudio
author: pchapman
ms.author: pchapman
manager: sacalla
ms.date: 08/07/2017
ms.topic: release-article
ms.prod: vs-devops-alm
ms.technology: vs-devops-articles
ms.assetid: 205a4a2b-cb2a-4a8b-afa0-d69a2f0edadb
---


# <a id="top"> </a> Visual Studio 2017 Platform Targeting and Compatibility

> To see the latest updates, please visit the English [Compatibility](https://www.visualstudio.com/en-us/productinfo/vs2017-compatibility-vs) page.

Visual Studio 2017 contains many new and exciting features and IDE productivity enhancements to 
support Windows app development, cross-platform mobile development, Azure development, web and cloud development, 
and more. To try out Visual Studio 2017, see [Visual Studio 2017 Downloads](https://www.visualstudio.com/downloads). 
For more information about everything that's new in this release, see the 
[Visual Studio 2017 release notes](https://www.visualstudio.com/news/releasenotes/vs2017-relnotes) and 
[What's New in Visual Studio 2017](https://docs.microsoft.com/visualstudio/ide/whats-new-in-visual-studio).

For Visual Studio Code, see [Visual Studio Code FAQ](https://code.visualstudio.com/docs/supporting/faq). 
For [Visual Studio 2017 for Mac](https://www.visualstudio.com/visual-studio-for-mac/), see 
[Visual Studio 2017 for Mac Platform Targeting and Compatibility](https://www.visualstudio.com/productinfo/vs2017-compatibility-mac) 
and [Visual Studio 2017 for Mac release notes](https://www.visualstudio.com/news/releasenotes/vs2017-mac-relnotes). 

## Installation

You can [install and use Visual Studio 2017](https://docs.microsoft.com/visualstudio/install/install-visual-studio) alongside 
previous versions of Visual Studio, including Visual Studio 2015, Visual Studio 2013, and Visual Studio 2012.

## System Requirements
For information on the system requirements for installing and running the Visual Studio 2017 family of products, 
including Team Foundation Server 2017, see the [Visual Studio 2017 System Requirement page](https://www.visualstudio.com/productinfo/vs2017-system-requirements-vs) and 
[Visual Studio 2017 for Mac Product Family System Requirements](https://www.visualstudio.com/productinfo/vs2017-system-requirements-mac). 

## Feedback and Support
For support, or to submit feedback on Visual Studio, see:
* [Visual Studio Support](https://www.visualstudio.com/support/)
* [Submit a product suggestion or idea](https://visualstudio.uservoice.com)
* [Report a problem or bug](https://developercommunity.visualstudio.com/)

## Project Upgrade

When following the supported upgrade paths, your Visual Studio source, solutions, and project files will continue 
to work; however, you should expect to make some changes to sources. While we cannot guarantee binary compatibility 
between releases, we will do our best to document significant changes to assist you with updates.

For details on how to migrate your projects to Visual Studio 2017, see 
[Porting, Migrating, and Upgrading Visual Studio Projects](https://docs.microsoft.com/visualstudio/porting/port-migrate-and-upgrade-visual-studio-projects).

## Platform Targeting
Visual Studio provides cutting-edge tools and technologies to create apps that take advantage of the 
latest platform capabilities, whether Windows, Android, iOS, or Linux. Visual Studio 2017 also targets 
earlier platforms so you can create new apps or modernize existing apps that execute on earlier versions 
of Windows while leveraging the enhanced development tools, quality enablement, and team collaboration 
capabilities in Visual Studio 2017. For more information, see [Managing references in a 
project](https://docs.microsoft.com/visualstudio/ide/managing-references-in-a-project) and [Visual Studio Multi-Targeting 
Overview](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview).
* [Developing apps for Windows](#developWindows)
* [Developing apps for Android](#developAndroid)
* [Developing apps for iOS](#developIOS)
* [Developing apps for Linux](#developLinux)
* [Developing apps for macOS](#developMacOS)
* [Developing apps for other technologies and platforms](#developOther)

### <a id="developWindows"> </a>Visual Studio 2017 Support for Windows Development
The following table explains the Microsoft Windows platforms for which you can build apps by using Visual Studio 2017.

<table>
<tr>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Build Apps that Run on Windows Clients**</FONT></td>
  <td bgcolor="000000" style="width:40%"><FONT COLOR="FFFFFF">**Using Tools for Native and Managed Classic Windows Desktop Development**</FONT></td>
  <td bgcolor="000000" style="width:40%"><FONT COLOR="FFFFFF">**Using Tools for UWP App Development**</FONT></td>
</tr>
<tr>
  <td>Windows 10</td>
  <td>Yes <br/> 
      (see notes below)</td>
  <td>Yes <br/> 
      (see notes below)</td>
</tr>
<tr>
  <td>HoloLens</td>
  <td>No</td>
  <td>Yes <br/> 
      See [the Windows Holographic Dev Center](https://go.microsoft.com/fwlink/?LinkId=808650).</td>
</tr>
<tr>
  <td>Xbox One</td>
  <td>Not applicable</td>
  <td>Yes <br/> 
      See [the Xbox Dev Center](https://go.microsoft.com/fwlink/?LinkId=808649).</td>
</tr>
<tr>
  <td>Windows 8.1 ([Windows 8](https://support.microsoft.com/help/18581/lifecycle-support-policy-faq-windows-products))</td>
  <td>Yes</td>
  <td>Windows Store app development is not available.</td>
</tr>
<tr>
  <td>Windows 7</td>
  <td>Yes</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td>Windows Vista</td>
  <td>Yes <br/> 
      Remote debugging and profiling tools are not available.</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td>Windows XP</td>
  <td>Yes <br/> 
      Managed development requires using [Visual Studio .NET multi-targeting](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview). 
      Remote debugging and profiling tools are not available.</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Build Apps that Run on Windows Phone**</FONT></td>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Using Tools for Native and Managed Classic Windows Desktop Development**</FONT></td>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Using Tools for UWP App Development**</FONT></td>
</tr>
<tr>
  <td>Windows 10 Mobile</td>
  <td>No</td>
  <td>Yes <br/> 
      (see notes below)</td>
</tr>
<tr>
  <td>Windows Phone 8.1 and earlier</td>
  <td>No</td>
  <td>Windows Store app development is not available.</td>
</tr>
<tr>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Build Apps that Run on Windows Server**</FONT></td>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Using Tools for Native and Managed Classic Windows Desktop Development**</FONT></td>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Using Tools for UWP App Development**</FONT></td>
</tr>
<tr>
  <td>Windows Server 2016</td>
  <td>Yes</td>
  <td>Yes <br/> 
      (see notes below)</td>
</tr>
<tr>
  <td>Windows Server 2016, Nano Server Installation Option</td>
  <td>Yes, for .NET Core and a subset of Win32 <br/>
      See [the Nano Server Dev Center](https://go.microsoft.com/fwlink/?LinkId=808678).</td>
  <td>No</td>
</tr>
<tr>
  <td>Windows Server 2012 R2</td>
  <td>Yes</td>
  <td>Windows Store app development is not available.</td>
</tr>
<tr>
  <td>Windows Server 2012</td>
  <td>Yes</td>
  <td>Windows Store app development is not available.</td>
</tr>
<tr>
  <td>Windows Server 2008 R2</td>
  <td>Yes</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td>Windows Server 2008</td>
  <td>Yes <br/> 
      Remote debugging and profiling tools are not available.</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td>Windows Server 2003</td>
  <td>Yes <br/> 
      Remote debugging and profiling tools are not available. Managed development requires using 
      [Visual Studio .NET multi-targeting](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview) and requires 
      side-by-side installation of Visual Studio 2010. For more information, see: 
      [A Look Ahead at the Visual Studio 2012 Product Lineup and Platform Support](https://go.microsoft.com/fwlink/?LinkId=808329).</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Build Apps that Run on Windows Embedded Devices**</FONT></td>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Using Tools for Native and Managed Classic Windows Desktop Development**</FONT></td>
  <td bgcolor="000000" style="width:20%"><FONT COLOR="FFFFFF">**Using Tools for UWP App Development**</FONT></td>
</tr>
<tr>
  <td>Windows 10 IoT Core</td>
  <td>Yes, for a subset of Win32 APIs <br/> 
      [See the IoT Core API Porting Tool](https://go.microsoft.com/fwlink/?LinkId=808332) for information.</td>
  <td>Yes <br/> 
      See the [Windows IoT Dev Center](https://go.microsoft.com/fwlink/p/?linkID=532967) for additional tools and resources.</td>
</tr>
<tr>
  <td>Windows 10 IoT Mobile Enterprise</td>
  <td>No</td>
  <td>Yes <br/> 
      See the [Windows IoT Dev Center](https://go.microsoft.com/fwlink/p/?linkID=532967) for additional tools and resources.</td>
</tr>
<tr>
  <td>Windows 10 IoT Enterprise</td>
  <td>Yes <br/> 
      See the [Windows IoT Dev Center](https://go.microsoft.com/fwlink/p/?linkID=532967) for additional tools and resources.</td>
  <td>Yes <br/> 
      See the [Windows IoT Dev Center](https://go.microsoft.com/fwlink/p/?linkID=532967) for additional tools and resources.</td>
</tr>
<tr>
  <td>Windows Embedded 8 Standard and 8.1 Industry</td>
  <td>Yes</td>
  <td>No</td>
</tr>
<tr>
  <td>Windows Embedded Compact 2013</td>
  <td>No</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td>Windows Embedded 7 (Compact, Standard, and POSReady)</td>
  <td>No</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td>Windows Embedded CE 6.0 and earlier</td>
  <td>No</td>
  <td>Not applicable</td>
</tr>
<tr>
  <td>Windows XP Embedded (Including POSReady 2009, WES 2009, WEPOS)</td>
  <td>No</td>
  <td>Not applicable</tr>
</table>


**Notes**

* For support information regarding Microsoft operating systems, see [Microsoft Support Lifecycle](https://support.microsoft.com/lifecycle/) and [Windows 10 Release Information](https://technet.microsoft.com/en-us/windows/release-info.aspx).
* For support information on Microsoft .NET Framework, see [.NET Framework Support Lifecycle FAQ](https://support.microsoft.com/help/17455/lifecycle-policy-faq-microsoft-net-framework) 
  and [.NET Framework System Requirements](https://go.microsoft.com/fwlink/?LinkId=816388).
* [Windows 10 Enterprise LTSB edition](https://technet.microsoft.com/itpro/windows/manage/waas-overview) and [Windows 10 S](https://www.microsoft.com/windows/windows-10-s) are not supported for development. 
  You may use Visual Studio 2017 to build apps that run on Windows 10 LTSB and Windows 10 S. [Remote debuging](https://docs.microsoft.com/visualstudio/debugger/remote-debugging) is supported on LTSB.
* Universal Windows app development for all target platforms is available when Visual Studio is installed on Windows 10.
* Universal Windows apps can be built from the command line when using Windows Server 2012 R2 or Windows Server 2016. UWP development&mdash;including 
  designing, editing, and local debugging&mdash;is not available on Windows Server. You may deploy these apps to Windows server and [debug them remotely](https://docs.microsoft.com/visualstudio/debugger/remote-debugging).
* Cordova, Unity, and Xamarin can also be used for cross-platform development of Universal Windows Apps on Windows 10.

### <a id="developDotNET"> </a>Visual Studio 2017 Support for .NET Development
Visual Studio 2017 supports development of apps that use any of the .NET implementations. Among the workloads and project types, you can find support for 
.NET Framework, .NET Core,  Mono, and .NET Native for Universal Windows Platform (UWP). Visual Studio 2017 supports the following implementations:
* [.NET Framework](https://www.visualstudio.com/vs/net-development/) versions 4.7, 4.6.2, 4.6.1, 4.6, 4.5.2, and 3.5
* [.NET Core](https://dot.net/core) 2.0, 1.1, and 1.0.
* [.NET Native](https://docs.microsoft.com/dotnet/framework/net-native/)
* [Mono](http://www.mono-project.com/)

For more information on each of these implementations, and on the common API specification .NET Standard, 
see [.NET architectural components](https://docs.microsoft.com/dotnet/standard/components).

### <a id="developAndroid"> </a>Visual Studio 2017 Support for Android Development

Visual Studio 2017 enables you to build native Android apps using Xamarin and C# or using Java/C++, and hybrid 
Android apps using Apache Cordova 6.3.1 and JavaScript and TypeScript. The Visual Studio Tools for Unity and 
the Unreal Engine enable Android game development. You can also use [Visual Studio for Mac](https://www.visualstudio.com/vs/visual-studio-mac/) 
to build Android apps using a Mac.

You can use Visual Studio setup to easily obtain the Android SDK and Android API levels 19, 21, 22, and 23. 
You can download additional API levels separately using the [Android SDK Manager](https://go.microsoft.com/fwlink/?LinkId=808333). 
You can also use Visual Studio Setup to obtain the Android Native Development Kit (R10E), Java SE Development Kit, and Apache Ant.

For more information, see [Android development with Visual Studio](https://www.visualstudio.com/features/android-vs) and 
[Mobile App Development](https://www.visualstudio.com/vs/mobile-app-development/). 
For information on .NET development for Android, see [.NET architectural components](https://docs.microsoft.com/dotnet/standard/components). 

### <a id="developIOS"> </a>Visual Studio 2017 Support for iOS Development

Visual Studio 2017 enables you to build and debug apps for iOS by using Apache Cordova, C++, Unity, or Xamarin 
and a Mac configured for iOS development when using remotebuild, vcremote, the Visual Studio Tools for Unity, 
or the Xamarin Mac Agent. Xamarin supports iOS 7 and higher, and requires OS X 10.10 "Yosemite" or higher. 
Apache Cordova supports iOS 8 and higher, and requires OS X 10.9 "Mavericks" and higher. You can also use 
[Visual Studio for Mac](https://www.visualstudio.com/vs/visual-studio-mac/) to build iOS apps using a Mac.

For more information, see [Cross-platform mobile development in Visual Studio](https://docs.microsoft.com/visualstudio/cross-platform/cross-platform-mobile-development-in-visual-studio). 
For information on .NET development for iOS, see [.NET architectural components](https://docs.microsoft.com/dotnet/standard/components). 

### <a id="developLinux"> </a>Visual Studio 2017 Support for Linux Development

Visual Studio 2017 enables you to build and debug apps for Linux using C++, Python, and Node.js. 
[Creating C++ apps for Linux](https://aka.ms/linux-development-with-c-in-visual-studio) requires the 
Visual C++ for Linux Development extension. Creating apps with Python or 
Node,js, requires that you enable remote debugging on the target Linux machine. You can also create, build 
and remote debug .NET Core and ASP.NET Core applications for Linux using modern languages such as C#, VB and F#. 

For information on .NET development for Linux, see [.NET architectural components](https://docs.microsoft.com/dotnet/standard/components). 

* CentOS 7.1 and Oracle Linux 7.1
* Debian 8
* Fedora 23
* Linux Mint 17
* openSUSE 13.2
* Red Hat Enterprise Linux 7.2
* Ubuntu 14.04 and 16.04

For more information see [https://dot.net/core](https://dot.net/core).

### <a id="#developMacOS"> </a>Visual Studio 2017 Support for macOS Development

Visual Studio 2017 enables you to build console applications and ASP.NET applications that target macOS. 
However, debugging is not supported. For additional macOS development tools choices, try Visual Studio 
Code or Visual Studio for Mac. [Visual Studio Code](https://code.visualstudio.com/) provides a streamlined, 
extensible developer tool experience for macOS. [Visual Studio for Mac](https://www.visualstudio.com/vs/visual-studio-mac/) 
provides a feature-rich IDE that enables you to build native macOS apps, including ASP.NET, using C#.

For information on .NET development forMacOS, see [.NET architectural components](https://docs.microsoft.com/dotnet/standard/components). 

## <a id="developOther"> </a>Other Platforms and Technologies

Visual Studio 2017 also supports the following platforms and technologies. For more information, see 
[https://www.visualstudio.com/vs/features/](https://www.visualstudio.com/vs/features/).

* [Anaconda](https://docs.microsoft.com/visualstudio/python/python-environments)
* Apache Ant
* [Azure](https://www.visualstudio.com/vs/azure-tools/) web apps and connected services, including Azure Data Lake
* [Clang with Microsoft CodeGen](https://blogs.msdn.microsoft.com/vcblog/2017/03/07/use-any-c-compiler-with-visual-studio/)
* [ClickOnce](https://docs.microsoft.com/visualstudio/deployment/clickonce-security-and-deployment)
* [Cocos](https://blogs.msdn.microsoft.com/vcblog/2017/03/07/c-game-development-workload-in-visual-studio-2017/)
* [Cordova 6.3.1](https://docs.microsoft.com/en-us/visualstudio/cross-platform/cross-platform-mobile-development-in-visual-studio#HTML)
* Docker
* [Entity Framework 6](https://docs.microsoft.com/visualstudio/data-tools/create-a-simple-data-application-with-wpf-and-entity-framework-6)
* [F#](https://docs.microsoft.com/dotnet/fsharp/)
* [Git for Windows, and GitHub](https://www.visualstudio.com/vs/collaborate/)
* [HockeyApp](https://www.visualstudio.com/hockey-app/)
* [Microsoft SQL Server 2012, SQL Server 2014, and SQL Server 2016](https://www.visualstudio.com/vs/ssdt/)
* [Microsoft Office 365, Office 2016, Office 2013, Office 2010](https://www.visualstudio.com/vs/office-tools/)
* [Mobile Center](https://www.visualstudio.com/vs/mobile-app-development/)
* [Node.js](https://www.visualstudio.com/vs/node-js/)
* PowerShell
* [Python](https://www.visualstudio.com/vs/python/) and [Python IoT tools](https://blogs.msdn.microsoft.com/visualstudio/2017/05/12/a-lap-around-python-in-visual-studio-2017/)
* [R](https://www.visualstudio.com/vs/rtvs/)
* [TypeScript 2.3, 2.2, 2.1, and 2.0, and JavaScript](https://www.visualstudio.com/vs/javascript/)
* [Unity](https://docs.microsoft.com/visualstudio/cross-platform/visual-studio-tools-for-unity)
* [Unreal Engine](https://www.visualstudio.com/vs/game-development/)
* [Web Development](https://www.visualstudio.com/vs/modern-web-tooling/) with ASP.NET, HTML5/CSS3, JavaScript, Node.js, Python, or TypeScript

## Compatibility with Previous Releases

### .NET Framework

.NET 4.7 is is a highly compatible in-place update of .NET 4, 4.5, 4.5.1, 4.5.2, 4.6, 4.6.1, and 4.6.2. 
For more information, see the [Migration Guide to the .NET Framework 4.7, 4.6, and 4.5](https://docs.microsoft.com/dotnet/framework/migration-guide/).

### Team Explorer and Team Foundation Server

Team Explorer for Visual Studio 2017 will connect to Team Foundation Server 2017, Team Foundation Server 2015, 
Team Foundation Server 2013, Team Foundation Server 2012, and Team Foundation Server 2010 SP1.

### Silverlight

Silverlight projects are not supported in this version of Visual Studio. To maintain Silverlight applications, 
continue to use Visual Studio 2015.

### Windows Store and Windows Phone apps

Projects for Windows Store 8.1 and 8.0, and Windows Phone 8.1 and 8.0 are not supported in this release. To 
maintain these apps, continue to use Visual Studio 2015. To maintain Windows Phone 7.x projects, use Visual Studio 2012.

<center>[Top of Page](#top)</center>