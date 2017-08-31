---
title: Visual Studio 2015 Update 3 Known Issues
description: Visual Studio 2015 Update 3 Known Issues
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: visual-studio-dev14
ms.service: visualstudio
ms.assetid: 572cc840-8868-4567-9fb1-ffe40de0140c
---


# Visual Studio 2015 Update 3 Known Issues

## June 27, 2016
Microsoft released Visual Studio 2015 Update 3 on June 27, 2016. This article lists the known issues for Visual Studio 2015 Update 3. If these were not the known issues you were expecting, you have reached the known issues for the most current version.

To see the full list of features check out the [Visual Studio Update 3 Release Notes](https://go.microsoft.com/fwlink/?LinkId=798770).

#### Download: [Visual Studio Update 3](https://go.microsoft.com/fwlink/?LinkId=691129)

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/downloads/download-visual-studio-vs) page.

## Known Issues

### Installation Issues

#### <a id="LayoutInstall"> </a>When Installing Update 3, Setup Does Not Show Update 3 As An Install Option

* #### Issue: 
    If you have Visual Studio 2015 with Update 1 or Update 2, when installing Visual Studio 2015 Update 3 by using VS2015.3.exe, 
    setup may indicate that you already have an earlier update installed, but does not show that Update 3 can be installed. 
    The feature selection dialog also does not show any updated features. 
    
    You will experience this issue if you installed Visual Studio 2015 Update 1 or Update 2 using the /layout command and then try 
    to install Visual Studio 2015 Update 3 by running VS2015.3.exe.
* #### Workaround: 
    Instead of installing Visual Studio 2015 Update 3 by using VS2015.3.exe, install the update by using a full product installer. 
    You can find installers for "Visual Studio 2015 with Update 3" on the [Visual Studio download page](https://www.visualstudio.com/downloads/download-visual-studio-vs).
    Select the "Visual Studio 2015 with Update 3" download that matches the edition you already have installed, whether  Community, Professional, or Enterprise.                                                 

    Alternatively, you can follow the steps in [Updating an installation](https://msdn.microsoft.com/library/ee225237.aspx#Anchor_4) to force an update to the layouts.
    
    


#### Team Explorer: Installer displays CTP1 

* #### Issue: 
    When installing Update 3, you may see Team Explorer in the status bar incorrectly labeled as CTP1.

* #### Workaround: 
    None needed, this is an incorrect string.    
    
#### <a id="UWPinstall"> </a>Install Errors When Creating or Opening a UWP Project

* #### Issue:
    If you have Visual Studio Update 2 or earlier installed, along with the Tools for UWP app development, you may incorrectly receive 
    errors when creating or opening UWP projects. When creating a UWP project you may receive an error that "the project requires 
    a platform SDK (UWP, Version=10.0.10586.0) that is not installed." Or, when opening an existing UWP project, you may receive an 
    error "Install Missing Features. You need the Universal Windows App Development Tools to develop Windows app projects." 
    The project will also be unloaded. If you click Install, Visual Studio 2015 Update 3 is installed. 

* #### Workaround:
    Install Visual Studio 2015 Update 3. Or, install the updated [Windows SDK (1511) version 10.0.10586.212](https://developer.microsoft.com/windows/downloads/sdk-archive).

* #### Update [29 June 2016]
    This issue has been fixed. To receive the fix, close and re-open Visual Studio while you have an internet connection. 
    Then, for projects that open as unloaded, right-click and select "Reload Project". This fix does not require that you install
    Visual Studio 2015 Update 3. However, due to important fixes in the Windows SDK (1511), if you continue to use Visual Studio 2015 Update 2,
    we do recommend you [update the Windows SDK to build 10.0.10586.212](https://developer.microsoft.com/windows/downloads/sdk-archive).    



#### <a id="TailoredSetup"> </a>Error Installing Optional Items

* #### Issue:
    When running the Visual Studio Update 3 installer from [www.VisualStudio.com](https://www.visualstudio.com), you may see a message box that provides information about Secondary Installer usage syntax.  After dismissing the dialog, the Update 3 will fail to install correctly.

* #### Update [29 June 2016]
    This issue has been fixed.  The problem was caused by the downloaded installer having a space in the filename.  This can happen if the file was downloaded twice, causing the browswer to rename the file to something like "vs_community_ENU&nbsp;(1).exe".  The updated installer available on [www.VisualStudio.com](https://www.visualstudio.com) now correctly handles spaces in filenames, and installations will successfully complete.

* #### Note:
    If you received this error, simply modify Visual Studio from Control Panel -> Programs -> Programs and Features, and make sure that you reselect the optional components that you intended to install.  The Visual Studio installer will correctly install the optional items that previously failed.


#### Visual C++ : Project creation failure after Update

* #### Issue:
    After Update 3 is installed, in some cases, Visual C++ projects cannot be created with HResult 0x80041FE2. In some cases, applying Update 3 can 
    cause the optional feature selections for Visual C++ (e.g. Common Tools for Visual C++ 2015) to become deselected and uninstalled.

* #### Workaround:
    This issue can be resolved by re-selecting the required Visual C++ features in the Visual Studio 2015 setup dialog:
    - In "Programs and Features" (Add/Remove Programs), select "Microsoft Visual Studio <SKU> 2015 [with Updates]", then click "Change".
    - In the Visual Studio setup dialog, click "Modify"
    - Select/check "Programming Languages->Visual C++->Common Tools for Visual C++ 2015" and other features under "Programming Languages->Visual C++", as appropriate.
    - Click "UPDATE".






### Other Issues


#### Visual Studio Does Not Support Windows Information Protection

* #### Issue: 
    Visual Studio 2015 is unable to use data protected by Windows Information Protection (WIP). 
    (WIP, formerly known as Enterprise Data Protection or EDP, is a new security feature in Windows 10 Anniversary Update. 
    For more information see the [Windows ITPro Blog](https://blogs.technet.microsoft.com/windowsitpro/2016/06/29/introducing-windows-information-protection/)
    or [TechNet](https://technet.microsoft.com/itpro/windows/keep-secure/create-wip-policy-using-intune).) 
    If any of your source code files are encrypted by Windows Information Protection, when trying to compile a project 
    using the Visual Studio or third-party compilers, you will see errors like: 
    * Error MSB4025: The project file could not be loaded. Access to the path <PathToProject> is denied.
    * Error MSB4014: System.UnauthorizedAccessException: Access to the path <path> is denied.

* #### Workaround:
    To work around this issue, turn off Windows Information Protection. To verify whether Windows Information Protection is enabled, 
    right-click on the file. If there is a context menu item "File Ownership", then WIP is enabled.



#### Visual C++:  Passing non-pointer-like types to uninitialized_copy, uninitialized_copy_n, or uninitialized_fill 

* #### Issue: 
    Passing non-pointer-like types to uninitialized_copy, uninitialized_copy_n, or uninitialized_fill fails to compile.

* #### Workaround: 
    Provide a pointer_traits specialization for the supplied type.



#### Error when Reloading Shared Projects

* #### Issue:
    When using shared projects or linked files included in multiple projects, such as Universal Windows 8.1 Store projects, 
    if you unload and then reload the project you may receive an error “The method or operation is not implemented”.

* #### Workaround:
    Close the solution and then re-open it. You can avoid the error by closing files from shared projects before unloading the project. 




#### Windows Universal App Development
Known issues for Windows Universal App Development can be found in the forum [Known Issues for Windows 10 SDK and Tools](https://social.msdn.microsoft.com/Forums/en-US/home?forum=Win10SDKToolsIssues). 

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
