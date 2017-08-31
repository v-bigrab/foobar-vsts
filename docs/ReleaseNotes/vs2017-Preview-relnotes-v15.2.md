---
title: Visual Studio Preview Release Notes
description: Visual Studio Preview Release Notes
keywords: visualstudio
author: reshmim
manager: sacalla
ms.author: reshmim
ms.date: 05/10/2017
ms.topic: release-article
ms.prod: visual-studio-dev15
ms.service: visualstudio
ms.assetid: ca215c37-607e-453e-b403-f87cb0ed4fa2
---

# Visual Studio 2017 version 15.2 - Preview Release Notes

> [!NOTE]
> This release is not "go-live" and not intended for use on production computers or for creating production code.  

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/downloads) page. Also, see [Visual Studio Preview System Requirements](https://www.visualstudio.com/productinfo/vs2017-system-requirements-vs)
and [Visual Studio Platform Targeting and Compatibility](https://www.visualstudio.com/productinfo/vs2017-compatibility-vs).

### Feedback
We’d love to hear from you! For problems, let us know via the [Report a Problem](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017) option in the upper right corner, 
either from the installer or the Visual Studio IDE itself. Track your feedback on the [Developer Community](https://developercommunity.visualstudio.com/index.html) portal. For suggestions, 
let us know through [UserVoice](https://visualstudio.uservoice.com/forums/121579-visual-studio).

****

## <a id="15.2.26424.02"></a>Release Date: April 26, 2017 - version 15.2 (26424.02 - Preview)

#### Summary of Updates in this Release
* [Added a Preview badge.](#previewBadge)
* [The Visual Studio Installer will display Visual Studio offerings based on your current configuration.](#vsofferings)
* For long-running debugging sessions, the Diagnostic Tools Window will stop collecting data if memory and disk consumption exceed user-configured thresholds.
* [ReSharper extension has announced support for Lightweight solution load feature in Visual Studio 2017 (starting ReSharper 2017.1 release).](https://blog.jetbrains.com/dotnet/2017/04/03/meet-resharper-ultimate-2017-1)

#### Top Issues Fixed in this Release
* [Scanning new and updated MEF components every time Visual Studio 2017 launches.](https://developercommunity.visualstudio.com/content/problem/31028/scanning-new-and-updated-mef-components-every-time.html) 
* GitHub extension updated in-box to fix acquisition flow from the Start Page.
* Fixed deadlock when using certain TFVC commands after an hour.
* [VSIXInstaller cannot find setup engine instance in silent mode.](https://developercommunity.visualstudio.com/content/problem/26008/vs-2017-rtm-vsixinstaller-cannot-find-setup-engine.html)

****
### What's New in this Release

#### <a id="previewBadge"> </a> Added Preview Badge
A Preview Badge *(Figure 1)* has been added to the top of Preview installs to make them easier to identify when installed along SxS with VS.

<img src="media/PreviewBadge-2.png" alt="Preview Badge" style="border:2px solid Silver; display: block; margin: auto;">
<center>*(Figure 1) Preview Badge*</center>

#### <a id="vsofferings"> </a> The Visual Studio Installer will display Visual Studio offerings based on your current configuration
For example:
* If you have Enterprise installed on your machine, you will only see Enterprise offerings.
* If you have Professional, you will see both Professional and Enterprise offerings. 
* If you have Community, you will see Community, Professional, and Enterprise offerings.

****

## <a id="15.2.26419.01"></a>Release Date: April 20, 2017 - version 15.2 (26419.01 - Preview)

#### Summary of Updates in this Release
* [Solutions shown in Team Explorer.](#tesolutions)
* [Xamarin 4.5 is included in Visual Studio 2017.](#xamarin)  

#### Top Issues Fixed in this Release
* R Tools is now localized in all supported Visual Studio language packs.
* Python debugger no longer crashes on Unicode characters.
* New Python files will be created with correct encoding.
* JavaScript support is re-enabled when editing Django templates.

****

### What's New in this Release

#### <a id="tesolutions"> </a> Solutions shown in Team Explorer

Solutions have been brought back to Team Explorer, due to your [feedback](https://developercommunity.visualstudio.com/content/problem/34779/bring-back-showing-solutions-file-in-team-explorer.html).

#### <a id="xamarin"> </a> Property Pages and Manifests Redesign

In Xamarin 4.5 we've started a redesign of our Property Pages and Manifest editors. Looking for consistency with Visual Studio itself and Visual Studio for Mac, our new property pages were reorganized and simplified, supporting high-DPI displays. We've also split editors in more natural way. Now you can keep editing csproj options from the Property Pages, and manifest options from the manifest editor.

Please visit the [Xamarin release notes](https://developer.xamarin.com/releases/vs/xamarin.vs_4/xamarin.vs_4.5/) for full details.

****

## <a id="15.2.26412.01"></a>Release Date: April 17, 2017 - version 15.2 (26412.01 - Preview)

#### Summary of Updates in this Release
* [Data science and analytical applications](#datascience) workload has been added.
* The Python development workload is now localized in all supported Visual Studio language packs.
* Side-by-side support for [TypeScript compiler versions](#typescript).
* You can now pass command line debug arguments in JavaScript UWP applications. This was previously available for C#, VB, and C++ UWP applications. Note: There is an issue with passing command line arguments to the Simulator in this release.
* Multiple [Team Explorer fixes](#tefixes).
* You can now [change the location of where packages are cached](#nocache) or even disable caching of packages during install, modify, or repair.
* Multiple [F# tools](#fsharp) improvements.
* **CMake integration** now supports [CMake 3.7.2](https://cmake.org/cmake/help/v3.7/release/3.7.html). This updated CMake menu is based on your feedback.
* **Linux C++** now enables improved type visualization during debugging.
* [Fixed issue where Visual Studio 2017 may not launch when installed alongside Visual Studio 2005 or earlier](https://developercommunity.visualstudio.com/content/problem/30312/problems-when-starting-vs-2017-enterprise-on-windo.html).
* The **Game Development with Unity** workload now offers to install [Unity 5.6](https://unity3d.com/unity).

#### Top Issues Fixed in this Release
* A debugger crash in C++ code that uses the typeid operator is now fixed.
* Customers using website projects would see crashes when right clicking in the solution explorer that are now fixed.
* A crash when using the HTML editor in .Net core web projects.

**** 

### What's New in this Release

#### <a id="datascience"> </a> Data Science and Analytical Applications Workload

The Data science and analytical applications workload provides a one-click install of all your data analysis needs. It includes support for Python, R, F#, and their respective packages/distros to enable acquisition, analysis, and visualization of data all the way through to building and deploying machine learning models.

#### <a id="typescript"> </a> TypeScript Side-by-Side Support

Multiple versions of the TypeScript compiler may now be used in Visual Studio 2017. During installation, TypeScript 2.2 will be automatically included with the Web, Node.js, Universal Windows, or Mobile JavaScript workloads. TypeScript 2.1 may also be selected from the 'Individual Components' installer page.

By default, the version of TypeScript used by IntelliSense *(Figure 2)* and by the build will be the latest installed. To change the version used by IntelliSense, use the "Tools / Options / Text Editor / JavaScript/TypeScript / IntelliSense" setting shown below. To change the TypeScript version used for building a project, set the MSBuild property `<TypeScriptToolsVersions>` in the project file (see [the TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/compiler-options-in-msbuild.html) for more info on MSBuild properties).

<img src="media/tsversion-2.png" width="700" height="237" style="border:2px solid Silver; display: block; margin: auto;">
<center>*(Figure 2) TypeScript used by IntelliSense*</center>

#### <a id="tefixes"> </a> Team Explorer Fixes
* [Customers see an error of "Team Foundation Error\n\nNon-space character detected within the skipped tab prefix.\nParameter name: tabSize" when viewing Git history](https://developercommunity.visualstudio.com/content/problem/5465/git-history-isn39t-working.html).
* [Error of "non-space character detected within the skipped tab prefix" when using Git Blame](https://developercommunity.visualstudio.com/content/problem/25899/error-when-using-blame-for-git-repository-non-spac.html).
* [Git Commands don't work when folder name has special characters](https://developercommunity.visualstudio.com/content/problem/28449/git-commands-dont-work-when-folder-name-has-specia.html).
* [Git __Compare with Unmodified__ not working](https://developercommunity.visualstudio.com/content/problem/17952/team-explorer-git-compare-with-unmodified-not-work.html).
* [Error message of "Substring must begin at a code-point boundry." when running __View History__ on a Git branch](https://developercommunity.visualstudio.com/content/problem/25137/git-get-error-message-when-click-view-history-on-a.html).
* [Customers need to enter passwords multiple times](https://developercommunity.visualstudio.com/content/problem/32255/when-integrating-with-team-services-you-have-to-en.html).

#### <a id="nocache"> </a> Moving or Disabling the Installer Package Cache

When [installing Visual Studio 2017 using the command line](https://docs.microsoft.com/visualstudio/install/use-command-line-parameters-to-install-visual-studio)
you can pass `--cache` to enable the caching policy (default) for the install and subsequent install, modify, and repair operations; or you can pass `--nocache` to disable the policy
which will prevent packages from being cached and remove any packages already cached for the current instance.

The policy can also be changed through the registry and group policy. See [our setup blog](https://aka.ms/setup/nocache) for more information.

#### <a id="fsharp"> </a> F\# Tools Improvements

* Basic autocomplete support.
* Ability to Go to Definition when clicking in the tooltip.
* Mutable values colorized, and other semantic colorization improvements.
* Project system performance improvements.
* Large performance improvements all-up.
* Move Up/Move Down on Solution folder nodes.
* Intelligent ordering in Completion lists.

****
### [Current Preview Release Notes](vs2017-preview-relnotes.md)
### [Visual Studio 2017 version 15.1 - Preview Release Notes](vs2017-preview-relnotes-v15.1.md)
****
### [Visual Studio 2017 version 15.2 Release Notes](vs2017-relnotes.md)
### [Visual Studio 2017 version 15.1 Release Notes](vs2017-relnotes-v15.1.md)
### [Visual Studio 2017 version 15.0 Release Notes](vs2017-relnotes-v15.0.md)
