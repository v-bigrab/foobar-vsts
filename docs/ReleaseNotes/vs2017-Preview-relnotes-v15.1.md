---
title: Visual Studio Preview Release Notes
description: Visual Studio Preview Release Notes
keywords: visualstudio
author: reshmim
manager: sacalla
ms.author: reshmim
ms.date: 05/10/2017
ms.topic: release-article
ms.prod: vs-devops-alm
ms.technology: vs-devops-articles
ms.assetid: 07da4285-cf6f-4cab-a8b6-da945e874851
---

# Visual Studio 2017 version 15.1 - Preview Release Notes

> [!NOTE]
> This release is not "go-live" and not intended for use on production computers or for creating production code.  

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/downloads) page. Also, see the [Visual Studio Preview System Requirements](https://www.visualstudio.com/productinfo/vs2017-system-requirements-vs)
and [Visual Studio Platform Targeting and Compatibility](https://www.visualstudio.com/productinfo/vs2017-compatibility-vs) pages.

### Feedback
We’d love to hear from you! For problems, let us know via the [Report a Problem](https://docs.microsoft.com/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017) option in the upper right corner, 
either from the installer or the Visual Studio IDE itself. Track your feedback on the [Developer Community](https://developercommunity.visualstudio.com/index.html) portal. For suggestions, 
let us know through [UserVoice](https://visualstudio.uservoice.com/forums/121579-visual-studio).

### Known Issues
The known issues in this release are [listed below](#knownissues).

****

## <a id="15.1.26401.01"></a>Release Date: April 3, 2017 - version 15.1 (26401.1 - Preview)

#### Summary of Updates in this Release
* Includes fixes for reliability and performance issues and also fixes a build issue in UWP projects with GenXbf.dll.

#### Issues Resolved in this Release
* Uninstalling Visual Studio Windows 10 SDK causes UWP build errors in Visual Studio 2017 or Visual Studio 2015.

****

## <a id="15.1.26323.1"></a>Release Date: March 27, 2017 - version 15.1 (26323.1 - Preview)

#### Summary of Updates in this Release 

* [Tools for Universal Windows App Development](#UWP-1703) - The Preview support for UWP apps includes an updated Windows SDK (build 15063) for Windows 10 Creators Update. 

****

## <a id="15.1.26315.00"></a>Release Date: March 16, 2017 - version 15.1 (26315.00 - Preview)

#### Summary of Updates in this Release 

* [Team Explorer standalone install](#te).
* [Tools for Universal Windows App Development](#UWP-1703) - Preview support for UWP apps for the upcoming Windows 10 Creators Update version 1703.

### What's New in this Release

#### <a id="te"> </a> Team Explorer standalone install

Visual Studio Team Explorer 2017 is a rich, standalone client for accessing Team Foundation Server and Visual Studio Team Services. It is free for any user. This [install](https://aka.ms/vs/15/pre/vs_teamexplorer.exe) only includes Team Explorer (_Figure 1_) so you can access version control and work item tracking without other IDE components.

<img src="media/teamexplorersku.png" alt="Team Explorer" style="border:3px solid Silver; display: block; margin: auto;">
<center>*(Figure 1) Team Explorer*</center>

#### <a id="UWP-1703"> </a> Tools for Universal Windows App Development

The Universal Windows App workload now includes a pre-release Creators Update SDK, build 15063, allowing you to start building apps for the Windows 10 Creators Update. 
These apps cannot be published to the Windows Store until the Creators Update has been released and you have rebuilt the apps using the final SDK and Tools for UWP. 
In addition, this release includes the following enhancements:
* Starting with the Creators Update SDK, the Windows 10 SDK will install side-by-side. This allows you to use a single machine to build production-ready apps that target the 
released version of the SDK. You can begin testing new OS features delivered by a Preview Windows SDK. 
* NuGet package management has been improved by using [PackageReference](https://docs.microsoft.com/nuget/consume-packages/package-references-in-project-files) to replace 
package.config and package.json.
* An enhanced .NET Native Compiler delivered as a NuGet package.
* Improved tooling support for XAML controls delivered as NuGet packages.
* IntelliSense in the XAML editor now highlights XAML types and properties that are not supported in the version of the SDK that your app is targeting.  

For more information, see [Creators Update SDK support in Visual Studio 2017](https://blogs.msdn.microsoft.com/visualstudio/2017/03/16/visual-studio-2017-update-preview-and-windows-10-creators-update-sdk/).

****

## <a id="15.1.26304.00"></a>Release Date: March 7, 2017 - version 15.1 (26304.00 - Preview)

#### Summary of Updates in this Release 

* [Python](#python) - Python development workload has been added to this release.
* [Manage your Preview installation](#manage).

### What's New in this Release

#### <a id="python"> </a> Python development workload

The Python development workload in Visual Studio is designed to maximize your productivity in Python. Improved IntelliSense, web development projects, git, and VSTS integration save you time and effort on everyday tasks. Use world class debugging (local, remote, cross-platform, and Python/native), and profiling tools to improve the quality and performance of your Python code.

#### <a id="manage"> </a> Manage your Preview installation

Should you decide that you no longer want to use Preview, you should first uninstall any Preview products you have installed. Then, locate the 'X' under the Available products section (for Preview), to remove the Preview products.


****


## <a id="knownissues"> </a>Known Issues

Here are the known issues and available workarounds specific to this Preview release. For known issues in Visual Studio 2017, which will also affect this release, 
see [Visual Studio 2017 Release Notes](https://www.visualstudio.com/news/releasenotes/vs2017-relnotes).

  * [Installation Issues](#KIInstallation)
  * [Debugging and Diagnostics Issues](#KIDebugger)
  * [Other Issues](#KIOther)

### <a id="KIInstallation"> </a> Installation Issues

#### Uninstalling Visual Studio Windows 10 SDK causes UWP build errors in Visual Studio 2017 or Visual Studio 2015
* #### Issue:
If you uninstall the Windows 10 SDK, you will receive the following error when building a UWP app:  
`Cannot resolve 'GenXbf.dll' under path 'C:\Program Files\Windows Kits\10'. Please install the Windows Software Development Kit. The Windows 10 SDK is installed with Visual Studio.`  
This issue affects Visual Studio 2017, Visual Studio 2017 Preview, and Visual Studio 2015. Your machine can get into this error state when you've installed:
  * Visual Studio 2017 and Visual Studio 2017 Preview, and then uninstalled one of these.
  * Visual Studio 2015 and Visual Studio 2017 or Visual Studio 2017 Preview, and then uninstalled one of these. 
  * Visual Studio 2017, Visual Studio 2017 Preview, or Visual Studio 2015 and then uninstalled any Windows 10 SDK either directly from Programs and Features or by using setup for Visual Studio.

* #### Workaround:
Open the Control Panel, and go to Programs and Features. Select one of the following, and click Repair:
  * Windows Software Development Kit - Windows 10.0.15063.00 (Creators Update).
  * Windows Software Development Kit - Windows 10.0.14393.795 (Anniversary Update).

### <a id="KIDebugger"> </a>Debugging and Diagnostics Issues

#### Remote Tools for Visual Studio 2017 Preview are not available
* #### Issue:
We have not made an update for the Remote Tools for Visual Studio 2017 Preview available.

* #### Workaround:
The [Remote Tools for Visual Studio 2017](https://www.visualstudio.com/downloads#remote-tools-for-visual-studio-2017) is compatible with Visual Studio 2017 Preview. 
However, if you are interested in using the latest preview version of the remote debugger, see [Run the remote debugger from a file share](https://docs.microsoft.com/visualstudio/debugger/remote-debugging#optional-to-run-the-remote-debugger-from-a-file-share).

### <a id="KIOther"> </a>Other Issues

#### Creating packages for UWP applications may fail
* #### Issue: 
Trying to create packages for UWP applications with scaled resources fails with "Error: File 'C:\somepath\..._scale-100.appx' not found." 

* #### Workaround
You can find a workaround on the [Visual Studio Developer Community](https://developercommunity.visualstudio.com/content/problem/40376/error-file-csomepathbinarmreleaseapp-112180-scale.html?).

#### R 3.4.0 is not yet supported
* #### Issue:
R 3.4.0 downloaded from [cran.r-project.org](https://cran.r-project.org/) is not yet supported due to changes in some native APIs.

* #### Workaround
Previous versions of R continue to work correctly, including Microsoft R Client as included in the installer. Support for R 3.4.0 will be added in a future update.

****
### [Current Preview Release Notes](vs2017-preview-relnotes.md)
### [Visual Studio 2017 version 15.2 - Preview Release Notes](vs2017-preview-relnotes-v15.2.md)
****
### [Visual Studio 2017 version 15.2 Release Notes](vs2017-relnotes.md)
### [Visual Studio 2017 version 15.1 Release Notes](vs2017-relnotes-v15.1.md)
### [Visual Studio 2017 version 15.0 Release Notes](vs2017-relnotes-v15.0.md)