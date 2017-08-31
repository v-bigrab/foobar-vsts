---
title: Visual Studio 2015 Update 3 RC Known Issues
description: Visual Studio 2015 Update 3 RC Known Issues
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: visual-studio-dev14
ms.service: visualstudio
ms.assetid: 6028158d-9be8-4bb7-a157-937bfdf04bca
---


# Visual Studio 2015 Update 3 RC Known Issues

## June 7, 2016
Microsoft released Visual Studio 2015 Update 3 RC on June 7, 2016. This article lists the known issues for Visual Studio 2015 Update 3 RC.

To see the full list of features check out the [Visual Studio Update 3 RC Release Notes](https://www.visualstudio.com/news/releasenotes/vs2015-update3-vs).

#### Download:[Visual Studio Update 3 RC](http://go.microsoft.com/fwlink/?LinkId=626599)

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/downloads/visual-studio-prerelease-downloads) page.

## Known Issues

#### TypeScript broken when uninstalling side-by-side Visual Studio "15" Preview

* #### Issue: 

  If you have Visual Studio 2015 and Visual Studio "15" Preview installed side-by-side and you uninstall Visual Studio "15" Preview, some Visual Studio 2015 TypeScript files are lost resulting in TypeScript not working in Visual Studio 2015.  

  ###### Workaround: 

  Repair Visual Studio 2015.


#### Code Coverage data collection for .Net code has the following limitations:

* #### Issue: 

  * Navigating to code will not work when Code Coverage data collection in done in conjunction with tools that do IL rewriting (like Code Contracts, for instance).
  * Code Coverage data collection for .NET code cannot be used in conjunction with Fakes.

  ###### Workaround:
  There is no workaround for this issue.


#### Cannot use JavaScript Memory, HTML UI Responsiveness, or Network Tools when debugging a JavaScript UWP app 

* #### Issue: 

  * When attempting to use the JavaScript Memory, HTML UI Responsiveness, or Network tools to debug a Javascript UWP app on a windows phone device or emulator, you may get the following errors:
    ```
    Diagnostics session failed to start. Unable to upload diagnostics tools to remote device
    DEP6701 : Bootstrapping failed with unexpected error: 'The system cannot find the path specified 'C:\Program Files (x86)\Common Files\Microsoft Shared\Phone Tools\15.0\ScriptDiagnostics\target\x86\JavaScriptCollectionAgent.dll'.'.
    ```

  ###### Workaround:
  * Open C:\ProgramData\Microsoft\Phone Tools\CoreCon\12.0\addons\Microsoft.VisualStudio.WebClient.Diagnostics_14.0.xsl and replace all occurrences of
    
    ```%CSIDL_PROGRAM_FILES%\Common Files\Microsoft Shared\Phone Tools\15.0\```
 
    with
 
    ```%CSIDL_PROGRAM_FILES%\Common Files\Microsoft Shared\Phone Tools\14.0\```
 

#### .NET Core 1.0.0 RC2 - VS 2015 Tooling Preview1 may fail to install or repair after Visual Studio 2015 Update 3 RC is installed

* #### Issue: 
  
  After installing Visual Studio 2015 Update 3 RC, you may encounter issues installing .NET Core 1.0.0 RC2 - VS 2015 Tooling Preview1 with the following error:
  
   * 0x80070666 - Another version of this product is already installed. Installation of this version cannot continue. To configure or remove the existing version of the product, use Add/Remove Programs on the Control Panel.
  
  This is due to a setup issue resulting in VC++ 2015 Update 3 RC Redistributable registry keys being incorrectly removed during Update 3 RC setup.
  
  ###### Workaround:

  Repair the Visual C++ 2015 Redistributable (both x86 and x64) via the "Programs and Feature" Window (a.k.a. Add/Remove Programs)
  * On Windows 10, right click the start button and select "Programs and Features"
  * Select "Microsoft Visual C++ 2015 Redistributable (x64) - 14.0.24123" and then click "Change"
  * In the Visual C++ 2015 redistributable dialog, select "Repair"
  * Select "Microsoft Visual C++ 2015 Redistributable (x86) - 14.0.24123" and then click "Change"
  * In the Visual C++ 2015 redistributable dialog, select "Repair"
  * Install or repair .NET Core 1.0.0 RC2 - VS 2015 Tooling Preview1

#### After switching Visual Studio theme, editor tooltip text might be hard to read due to wrong tooltip background color

* #### Issue: 
 After switching Visual Studio theme, the editor tooltip background might not be updated correctly, making the tooltip text hard to read.
  
  ###### Workaround:
  * Go to Tools/Options/Fonts and Colors
  * Select "Environment" in the "Show settings for:" dropdown list 
  * Change background color of the "Tooltip" item. Here are the RGB values of the recommended colors: 66,66,69 for the Dark theme, 246,246,246 for the Light theme, 231,232,236 for the Blue theme.

#### Visual Studio ThirdPartyNotices.txt file is not updated correctly

* #### Issue: 
  After you install Visual Studio Update 3 RC, the ThirdPartyNotices.txt file under C:\Program File(x86)\Microsoft Visual Studio (14.0)\shell shows an incomplete list of OSS attributions.

 ###### Workaround:
  * There is no workaround for this issue. However, for the correct list of OSS attributions please reference to the ThirdPartyNotices.txt file that installs as part of the Visual Studio 2015 Update 2 Release 

#### Visual C++ project build fails when using the v140_xp PlatformToolset

* #### Issue:
  When using PlatformToolset v140_xp, UCRT is not added to the Include and Library path.

  ###### Workaround:
  * In Visual Studio, go to the Solution Explorer.
  * Right click on the project, click on “Properties” 
  * Find and Select “VC++ Directories”
  * Append Includes Directory with “$(MSBuildProgramFiles32)\Windows Kits\10\Include\10.0.10240.0\ucrt” 
  * Append Library Directory with “$(MSBuildProgramFiles32)\Windows Kits\10\lib\10.0.10240.0\ucrt\$(PlatformShortName)”
  * Click OK or Apply to Save.

## More information   

#### Restart requirement

 You may have to restart your computer after you install this package.

#### Software requirement
On Windows 8.1 and Windows Server 2012 R2, you have to install update 2919355 (also available through Windows Update) before you install Visual Studio 2015 RTM. This is because the .NET Framework 4.6 installer can't be installed without update 2919355.

####  Supported architectures

* 32-bit (x86)

* 64-bit (x64) (WOW)


#### Third-party applications

* Visual Studio 2015 installation lets you install third-party applications. For information about which third-party applications are required when you install Cross Platform Mobile Development tools from Visual Studio 2015 , see [Knowledge Base article 3060693](https://support.microsoft.com/en-us/kb/3060693).


* Visual Studio 2015 removal does not uninstall third-party applications. For information about how to uninstall third-party applications that were installed together with Visual Studio 2015, see [Knowledge Base article 3060695](https://support.microsoft.com/en-us/kb/3060695).


#### Applies to


 - Visual Studio Professional 2015


 - Visual Studio Enterprise 2015


 - Visual Studio Community 2015


 - Visual Studio Express 2015 for Web


 - Visual Studio Express 2015 for Desktop


 - Visual Studio Express 2015 for Windows 10
