---
title: Visual Studio 2017 Installing earlier release
description: Visual Studio 2017 Installing earlier release
keywords: visualstudio
author: denizd
ms.author: denizd
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: visual-studio-dev15
ms.service: visualstudio
ms.assetid: 17f5d00a-681f-4dc5-bdac-6f82b1ebb725
---

#Installing an earlier release of Visual Studio 2017

We update Visual Studio often so that you get the most current, optimized features. Sometimes this may include changes which alter your development environment. If you need to go back to the previous release, then you must uninstall your current installation and use the link below to revert your Visual Studio state. This article describes how to do so.

> [!NOTE]
> Before attempting to modify your current installation of Visual Studio 2017, refer to our [support policy](https://www.visualstudio.com/en-us/productinfo/vs-servicing-vs), which outlines supported versions. Microsoft does not guarantee support outside of this policy.


##Uninstalling the current release
*   On your Windows desktop machine, open the Visual Studio Installer.
*   Uninstall every instance of Visual Studio 2017 that you currently have installed and visible in the Visual Studio Installer.
*   From **Add or Remove Programs**, find "Microsoft Visual Studio 2017" and uninstall it.

If you are unable to follow any of the steps above due to a corrupted install, do the following instead:
*	On your Windows desktop machine, go to **Add or Remove Programs**.
*	Find “Microsoft Visual Studio 2017”.
*	Select Uninstall. Once uninstallation is complete, you will need to run the Visual Studio Bootstrapper once more so that you can access the InstallCleanup tool. This tool will remove all traces of your previous Visual Studio instance, which is necessary for installing the earlier release.
*	Go to [VisualStudio.com/downloads](https://www.visualstudio.com/downloads) and select a version to download.
*	When prompted to select a workload to install, close the window (do not install anything).
*	Then close the Visual Studio Installer window (do not install anything).
*	You should now have access to InstallCleanup.exe from `C:\Program Files (x86)\Microsoft Visual Studio\Installer\resources\app\layout\`.
*	Using Command Prompt in administrator mode, go to this directory and run `InstallCleanup.exe -f`.

Please note, uninstallation will not remove standalone program entries, such as .NET, SQL, IIS, VC++ Redistributables and other SDKs. If required, these may need to be removed manually from **Add or Remove Programs**.

##Installing the earlier release
You can either create and use an offline installation, or you can download and launch the installer below directly.

To create an offline installation, follow the instructions at [Create an offline installation of Visual Studio 2017](https://docs.microsoft.com/visualstudio/ide/create-an-offline-installation-of-visual-studio), replacing the bootstrapper files referenced in the document with the versions below.

Please note that 15.2.6 contains a known [Git vulnerability](https://blogs.msdn.microsoft.com/devops/2017/08/15/git-vulnerability-with-submodules/), which has been addressed in later versions of Visual Studio.
| Product | Version | Installation link |
|---------|---------|-------------------|
| Community | 15.2.6 | [Community.exe](https://aka.ms/vs/15/release/3f9b192f9/vs_Community.exe) |
| Professional | 15.2.6 | [Professional.exe](https://aka.ms/vs/15/release/3f9b192f9/vs_Professional.exe) |
| Enterprise | 15.2.6 | [Enterprise.exe](https://aka.ms/vs/15/release/3f9b192f9/vs_Enterprise.exe) |


