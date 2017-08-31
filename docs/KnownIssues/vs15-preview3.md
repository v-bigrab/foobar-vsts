---
title: Visual Studio "15" Preview 3 Known Issues Preview 3
description: Visual Studio "15" Preview 3 Known Issues Preview 3
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: visual-studio-dev15
ms.service: visualstudio
ms.assetid: c3581b00-320e-4b0f-b94c-a610840fdda2
---


# Visual Studio “15” Preview 3 Known Issues

## July 7, 2016

Today, Microsoft released Visual Studio "15" Preview 3. This article lists the known issues for this release. To see the full list of features, check out the [Visual Studio "15" Preview 3 Release Notes](https://www.visualstudio.com/news/releasenotes/vs15-relnotes).

You can install the new Visual Studio release from the following link:

#### Download: [Visual Studio Enterprise "15" Preview 3](https://go.microsoft.com/fwlink/?LinkId=746567 "Visual Studio Enterprise 15 Preview 3")

To learn more about related downloads, see the [Downloads](https://www.visualstudio.com/en-us/downloads/visual-studio-next-downloads-vs "Downloads") page.


## Known Issues

#### Visual C++ project build fails when using the v140_xp PlatformToolset

* #### Issue:
  When using PlatformToolset v140_xp, UCRT is not added to the Include and Library path.

* #### Workaround:
  * In Visual Studio, go to the Solution Explorer.
  * Right click on the project, click on “Properties”.
  * Find and Select “VC++ Directories”.
  * Append Includes Directory with “$(MSBuildProgramFiles32)\Windows Kits\10\Include\10.0.10240.0\ucrt”.
  * Append Library Directory with “$(MSBuildProgramFiles32)\Windows Kits\10\lib\10.0.10240.0\ucrt\$(PlatformShortName)”.
  * Click OK or Apply to Save.
 
#### Cannot select startup item in open folder
* #### Issue:
   After opening a folder, selecting “Set as Startup Item” or “Debug and Launch Settings” on a file’s context menu triggers 
   an error dialog with the message “The method or operation is not implemented.”
* #### Workaround:
   To set the startup item, dismiss the dialog and select the startup project from the debug dropdown menu in the toolbar.
   Debug and launch settings can be edited normally via the context menu.  The error dialog can safely be ignored.


##Related Releases
 
#### Visual Studio "15" Preview 3 with new installer
Visual Studio "15" introduces a new, experimental installer that supports more configurable, faster installations of Visual Studio. A more detailed changelog and list of known issues associated with this experimental installer can be found at [http://aka.ms/vsnewinstallerreadme](http://aka.ms/vsnewinstallerreadme).

## Applies To

- Visual Studio Enterprise "15" Preview 3
