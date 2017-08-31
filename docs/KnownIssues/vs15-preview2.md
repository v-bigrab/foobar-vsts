---
title: Visual Studio "15" Preview 2 Known Issues
description: Visual Studio "15" Preview 2 Known Issues
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: visual-studio-dev15
ms.service: visualstudio
ms.assetid: 11f12167-30a9-4362-b314-981a335e83f3
---


# Visual Studio “15” Preview 2 Known Issues

## May 10, 2016

Today, Microsoft released Visual Studio "15" Preview 2. This article lists the known issues for this release. To see the full list of fetaures check out the [Visual Studio "15" Preview 2 Release Notes](https://www.visualstudio.com/en-us/news/releasenotes/vs15/vs15-relnotes).

You can install the new Visual Studio release from the following link:

#### Download: [Visual Studio Enterprise "15" Preview 2](https://www.visualstudio.com/en-us/downloads/visual-studio-next-downloads-vs "Visual Studio Enterprise 15 Preview 2")

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/en-us/downloads/visual-studio-next-downloads-vs "Downloads") page.

## Known Issues

#### JavaScript Options
* #### Issue: 
  When [Salsa](https://github.com/Microsoft/TypeScript/wiki/Using-the-Salsa-Preview-in-Visual-Studio-15-Preview) is enabled, the editing options in `Tools > Options > Text Editor > JavaScript` have no effect.
  
  ###### Workaround:
  Make desired options changes to `Tools > Options > Text Editor > TypeScript` instead. 
  TypeScript and JavaScript currently share these options.

#### Web Platform and Tools
* #### Issue:
  If you have a Visual Studio "15" Preview installation, and you create an empty ASP.NET 5 application and then try to add a scaffold to the project by using the **Add New Scaffolded Item** context menu item or **Add Controller** context menu item, the context menu item for scaffolding is ioncorrectly highlighted, and you receive an error message that says, The command Microsoft.Extensions.CodeGeneration could not be executed if you try to add a scaffold.
  Adding a scaffolded item works only when you use the ASP.NET 5 Web Application template. It does not work for the ASP.NET 5 Empty template because that template does not carry all the required dependencies to enable scaffolding.
* #### Issue:
  When you install Visual Studio "15" Preview and then you create a Web Job and publish it as a scheduled web job to Azure, the publishing succeeds. However, the job does not run on schedule.
  ###### Workaround:
  To work around this issue, install Azure SDK 2.9 from here: [http://go.microsoft.com/fwlink/?LinkId=746956](http://go.microsoft.com/fwlink/?LinkId=746956)
  
* #### Issue:
  When you install Visual Studio "15" Preview, browse to an Azure Web App, and then select View Settings from the context menu, the logs pane does not work, and tab for the pane is surrounded by the texts "#if !VS15" and "#endif."
  ###### Workaround:
  To work around this issue, install Azure SDK 2.9 from here: [http://go.microsoft.com/fwlink/?LinkId=746956](http://go.microsoft.com/fwlink/?LinkId=746956). In Azure SDK 2.9, the tab and extra text are removed.
  
* #### Issue:
  After you install Visual Studio "15" Preview, and you try to publish an ASP.NET 5 web application by using **npm / Bower** (for example, you publish an application that is created by using the default ASP.NET 5 Web Application template), you may experience one of the following errors:

  Executing script 'prepublish' in project.json
  C:\Program Files (x86)\MSBuild\Microsoft\VisualStudio\v15.0\Web\Microsoft.DNX.Publishing.targets(151,5): Error : 'npm' is not recognized as an internal or external command,
  C:\Program Files (x86)\MSBuild\Microsoft\VisualStudio\v15.0\Web\Microsoft.DNX.Publishing.targets(151,5): Error : operable program or batch file.
  C:\Program Files (x86)\MSBuild\Microsoft\VisualStudio\v15.0\Web\Microsoft.DNX.Publishing.targets(151,5): Error : The 'prepublish' script failed with status code 1.
  `1>Publish failed due to build errors. Check the error list for more details`.
  ###### Workaround:
  To work around this issue, use one of the following methods:
    * This error does not reproduce if the computer has Visual Studio 2015 installed side-by-side with Visual Studio "15" Preview.
    * Add the following two paths to the PATH environment variable in the Command Prompt window that is used to start Visual Studio:
        * %DevEnvDir%\Extensions\Microsoft\Web Tools\External
        * %DevEnvDir%\Extensions\Microsoft\Web Tools\External\Git
    * Add the following paths to the PATH environment variable in System Environment Variables:
        * C:\Program Files (x86)\Microsoft Visual Studio 15.0\Common7\IDE\Extensions\Microsoft\Web Tools\External
        * C:\Program Files (x86)\Microsoft Visual Studio 15.0\Common7\IDE\Extensions\Microsoft\Web Tools\External\Git
    * Install npm, Bower, and Git globally.

* #### Issue:
  If you are not signed in to an account by using Azure Subscriptions, and you create a web application of any kind by pressing OK in the ASP.NET Project dialog box that has the **Host In Cloud** option selected, the App Service provisioning dialog box opens. The first time in a session that you press the **Cancel** button in the dialog box, a message is displayed that indicates that the "Object reference is not set to an instance of an object." When you press **Cancel** the next time, the dialog box does not contain this message.
  ###### Workaround:
  To work around this issue, clear the Host In Cloud check box or sign in to Azure. Or, install Azure SDK 2.9 from here: [http://go.microsoft.com/fwlink/?LinkId=746956](http://go.microsoft.com/fwlink/?LinkId=746956)
  
* #### Issue:
  When you create an ASP.NET 5 web application by using Visual Studio "15" Preview, or you open an existing ASP.NET 5 Web Application by using Visual Studio "15" Preview, you notice that there is no colorization or Intellisense for Razor tag helpers.
  ###### Workaround:
  To work around this issue, edit the ** _ViewImports.cshtml** file so that there are no quotation marks around the **@addTagHelper** value. This helps to restore **Razor** tag helper support.
  For example, in the **_ViewImports.cshtml** file, change from:
  @addTagHelper "*, Microsoft.AspNet.Mvc.TagHelpers"
  to:
  @addTagHelper *, Microsoft.AspNet.Mvc.TagHelpers

#### C++
* #### Issue: 
  Compiling C++ UWP project will throw a warning:
  warning MSB3785: No SDKs were found. SDKReference items will not be resolved. If your application requires these references there may be compilation errors.
  ###### Workaround:
  This warning is showing up after we removed support for Windows Store 8.1. It can be safely ignored. The C++ UWP application will compile and deploy successfully.
  
#### NuGet
* #### Issue: 
  You experience the following symptoms with Nuget:
    * Opening a project with a package that contains an init.ps1 script either crash Visual Studio or the PowerShell Console fails to respond.
    * Installing a NuGet package together with an install.ps1 will either crash Visual Studio or the PowerShell Console fails to respond.
    * Web Publishing crashes Visual Studio or the PowerShell console fails to respond.
    * Package Manager Console does not work on a computer that does not have the latest updates to Windows 10 version 1511 installed.
    
 ###### Workaround: 
  To work around this issue, install Cumulative Update for Windows 10 Version 1511: January 2016 ([KB 3124263](http://support.microsoft.com/kb/3124263)) or a later cumulative update.
  For more information, see GitHub issue [#1638](https://github.com/NuGet/Home/issues/1638).
  
* #### Issue: NuGet v2 protocol redirects are broken.  
  Custom NuGet repositories that redirect requests to an alternative host do not honor the redirect request. 
  ###### Workaround: 
  To work around this issue, configure the package repository URI in settings to point to the redirected server location.
  For more information, see GitHub issue [#387](https://github.com/NuGet/NuGet.Client/pull/387).
  
#### Load Test
* #### Issue: 
 You can't create load tests if Visual Studio "15" Preview and Test Controller of previous versions, such as, Visual Studio 2013, are installed side-by-side on the same computer. When you create load tests on a computer that has such a side-by-side configuration, you may see multiple typeload exceptions and load tests will not be added to the project.
 ###### Workaround:
 There is no workaround to this issue. The recommendation is to not install Visual Studio "15" preview and older Test Controller side-by-side on the same computer.
 
* #### Issue:
 You can't create load tests if Visual Studio "15" Preview and previous versions of Visual Studio (2015 or older) are installed side-by-side on the same computer. When you create load tests on a computer that has such a side-by-side configuration, you may see multiple typeload exceptions and load tests will not be added to the project.
 ###### Workaround:
 There is no workaround to this issue. The recommendation is to not install Visual Studio "15" preview and previous versions of Visual Studio side-by-side on the same computer.

#### Diagnostic Tools
* #### Issue:
 Selecting an IntelliTrace event or an Application Insights event inside the Events track in the Diagnostic Tools window when no time range is selected will cause the window to stop functioning.
 ###### Workaround:
 To work around this issue, make sure that a range of time is selected in the tool window before selecting any IntelliTrace or Application Insights events. This will be the normal case if you select an event while in break mode.
 
#### Open Folder
* #### Issue: 
 Visual Studio may freeze when you close a folder that was opened the first time on a computer.
 ###### Workaround:
 To work around this issue, end Visual Studio process, restart Visual Studio, and open the folder again. Do not delete the .vs subfolder.

#### Xamarin
* #### Issue:
 When you debug Xamarin-based projects by using the Visual Studio Emulator for Android (May update), the deployment will freeze and you receive the message "Emulator launched successfully" incorrectly in the Output window.When debugging Xamarin-based projects using the Visual Studio Emulator for Android (May update), the deployment will hang with the message "Emulator launched successfully" in the Output window.
 ###### Workaround:
 To work around this issue, stop debugging by closing the emulator instance that was launched. Manually launch the emulator from the emulator manager and then restart debugging. To launch the emulator manager, from the Tools menu, click Visual Studio Emulator for Android. Then in the debug drop-down list, select the emulator device configuration you want to use. Finally, change the device in the debugging drop-down list. The emulator that is running will include "inch" in the name (for example, "5-inch" rather than "5"). 

#### Visual Studio "15" Preview 2 with new installer
Visual Studio "15" introduces a new, experimental installer that supports more configurable, faster installations of Visual Studio. A more detailed changelog and list of known issues associated with this experimental installer can be found at [http://aka.ms/vsnewinstallerreadme](http://aka.ms/vsnewinstallerreadme).

#### Applies to

- Visual Studio Enterprise "15" Preview 2
