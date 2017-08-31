---
title: Visual Studio 2017 Known Issues
description: Visual Studio 2017 Known Issues
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 04/12/2017
ms.topic: release-article
ms.prod: visual-studio-dev15
ms.service: visualstudio
ms.assetid: 38382e59-f450-432b-a30e-f99c59ce3141
---

#Known Issues for Visual Studio 2017

To learn more about Visual Studio, please visit the [current release notes](https://opsstaging.www.visualstudio.com/en-us/news/releasenotes/vs2017-relnotes?branch=users/v-bigrab/BillieTrain). You may also visit the [Downloads](https://www.visualstudio.com/downloads/) page to learn more about other Visual Studio products.

Here are the current known issues and available workarounds.

### <a id="KIinstall"> </a>Installation Issues

#### <a id="sdkFailed"> </a>Windows 10 SDK fails to install with Return Code -2147023293
* #### Issue:
In certain circumstances, the Windows SDK may fail to install with Return Code -2147023293. The Setup Log dd_setup_<timestamp>_errors.log will show an error similar to this:
Package 'Win10SDK_10.0.14393.795,version=10.0.14393.79501' failed to install.
(details)
Return code: -2147023293
Return code details: Fatal error during installation.
Note that the exact package name will depend upon the Windows 10 SDK you have selected to install.

* #### Workaround:
There may be several causes for this issue. To work around this issue, try these steps:

    * Install the Windows 10 SDK separately from Visual Studio. You may download the Windows 10 SDK from [the Windows Developer Center](https://developer.microsoft.com/windows/downloads/windows-10-sdk).
    * In some cases when installing on a version of Windows earlier than Windows 10, the install failure may be caused by a missing Universal C Runtime. You may install this by using
[KB2999226](https://support.microsoft.com/help/2999226) for the Windows 10 1507 runtime, or [KB3118401]( https://support.microsoft.com/help/3118401) for the Windows 10 1511 runtime.   
For more information see the [Visual Studio Developer Community portal](https://developercommunity.visualstudio.com/content/problem/19241/windows-10-sdk-fails-to-install-with-return-code-2.html).

#### Cloud Explorer cannot be launched
* #### Issue:
If Cloud Explorer is installed with the Web development workload, launching Cloud Explorer may fail with error messages saying 'Setup cannot proceed when Visual Studio is running. Please close Visual Studio and retry'. This is caused by missing dependencies.

* #### Workaround:
Install the Azure development workload then launch Cloud Explorer again.



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

#### Using an Offline Installation Folder when disconnected from the Internet doesn't install the Windows Emulator
* #### Issue:
When you use an offline installation folder that includes the Windows 10 Mobile Emulator (Creators Update) to install Visual Studio without an internet connection, 
Visual Studio Installer finishes with the message "Setup Completed with Warning", and the Windows Emulator fails to install. 

* #### Workaround:
Install the Windows 10 Mobile Emulator separately from Visual Studio. 
  1. Open your offline installation folder for Visual Studio and navigate to the folder "Win10_Emulator_10.0.15063,version=10.0.15063.12,chip=x64".
  2. Run EmulatorSetup.exe to install the Windows Emulator.


    If you have not already installed Visual Studio, you can install the Windows Emulator first.
    1. Install the Windows Emulator using the instructions above.
    2. Run the Visual Studio Installer to install Visual Studio, and the installer will not report the warning.

#### "Visual Studio Installer" shortcut is not found from Start Menu
* #### Issue:
After installing Visual Studio 2017, "Visual Studio Installer" shortcut is not found from Start Menu.

* #### Workaround:
Create a shortcut to "%ProgramFiles(x86)%\Microsoft Visual Studio\Installer\vs_installer.exe" on 64-bit machines or "%ProgramFiles%\Microsoft Visual Studio\Installer\vs_installer.exe" on 32-bit machines.

### <a id="KIeditoride"> </a>Editor and IDE Issues

#### Changed files display yield/warning signs in Solution Explorer when using Windows Insider builds

* #### Issue: 
In the some Windows Insiders builds, saving files in .NET Core, UWP, and Shared projects may result in yield/warning signs next to the changed files.

* #### Workaround:
The yield/warning signs are benign and may be safely ignored. Reloading the solution will remove the yield/warning signs.


#### EditorConfig is not supported in XML files

* #### Issue:
Coding style conventions defined in .editorconfig are not applied when editing XML files.

* #### Workaround:
There is no workaround at this time.

#### EditorConfig insert_final_newline and trim_trailing_whitespace properties are not supported

* #### Issue:
insert_final_newline and trim_trailing_whitespace properties defined in .editorconfig file have no effect.

* #### Workaround:
There is no workaround at this time.

#### Key bindings may stop working after executing a Quick Launch command

* #### Issue:
After searching for and executing a command from Quick Launch, key bindings may stop working.  This could include such 
operations as navigating in the editor with the arrow keys, Backspace, Delete, etc.

* #### Workaround:
Activate and deactivate the main menu by pressing Alt/Alt, or by clicking the File menu then pressing Esc.

#### JavaScript IntelliSense stops working

* #### Issue:
Opening a project with more than 25Mb of JavaScript code displays the error "The language service is disabled for project <project> because it included a large number of .js files. Consider excluding files using 'exclude' section of a 'tsconfig.json' file."

* #### Workaround:
Add a `tsconfig.json` to your project root with the following code:

    ```json
    {
        "compilerOptions": {
            "allowJs": true,            // These settings apply to .js files as well as .ts files
            "noEmit":  true             // Do not compile the JS (or TS) files in this project on build
        },
        "exclude": [
            "node_modules",             // Don't include any JavaScript found under "node_modules" or "bower_components"
            "bower_components"
        ]
    }
    ```
    Add additional folders with JavaScript code libraries. Another common one is `Scripts/Office/1` if you're using office-js.

#### TypeScript not recognized in ASP.NET Core projects

* #### Issue:
TypeScript files in ASP.NET Core projects don't have any IntelliSense and aren't being compiled on build.

* #### Workaround:
Add an empty `tsconfig.json` file to your project root.

### <a id="KINuget"> </a> NuGet Issues

#### NuGet restore may treat disabled package sources as enabled in some cases
* #### Issue:
The following restore command line techniques will treat disabled packages sources as enabled. [NuGet#5704](https://github.com/NuGet/Home/issues/5704)
1. msbuild /t:restore
2. dotnet restore (either with dotnet.exe that ships with VS, or the one that comes with NetCore SDK 2.0.0)

* #### Workaround:
1. Use Visual Studio (2017 15.3 or later) or NuGet.exe (v4.3.0 or later)
2. Delete your disabled source and continue to use msbuild or dotnet.exe.
3. For your solution, you could use "Clear" in NuGet.config and then define the sources necessary for that solution.

### <a id="KILUT"> </a>Live Unit Testing Issues

#### Live Unit Testing does not work with .NET Core projects
* #### Issue:
Live Unit Testing is not supported on .NET Core projects.

* #### Workaround:
There is no workaround at this time.

### <a id="KIWebTools"></a> Web Tools Known Issues

#### MVC4 projects do not connect to SQL Server LocalDB at runtime
* #### Issue:
When running an MVC4 project in Visual Studio, database access by the application may fail if it is using SQL Server Express LocalDB 2012. This is caused because MVC4 projects by default depend on SQL Server Express LocalDB 2012 which is not installed with Visual Studio 2017.

* #### Workaround:
Upgrade the project to use SQL Server Express LocalDB 2016, or manually download and install [SQL Server Express LocalDB 2012](https://go.microsoft.com/fwlink/?LinkID=627336) on the machine.

### <a id="KICore"> </a>.NET Core Tools Issues

For a current list of issues with .NET Core and ASP.NET Core Tools see our [GitHub page.](https://github.com/aspnet/Tooling/blob/master/known-issues-vs2017.md ".NET Core and ASP.NET Core known issues")

### <a id="KIOpenFolder"> </a>Open Folder Issues

#### IntelliSense not available while editing launch.vs.json or tasks.vs.json
* #### Issue:
When you edit a launch.vs.json or tasks.vs.json file, IntelliSense is not available.

* #### Workaround:
Install the "ASP.NET and Web Development" workload.

#### C# refactoring may have inconsistent results
* #### Issue:
Refactoring C# or VB code may have inconsistent results in folder mode.

* #### Workaround:
Load C# or VB projects in Solution mode.

#### F10 does not start the debugger in folder mode
* #### Issue:
The F10 hotkey does not start the debugger in folder mode.

* #### Workaround:
Use F5 or F11, and set a breakpoint in the application's entry point.

#### Unsaved edits to launch.vs.json may be lost
* #### Issue:
Unsaved edits to launch.vs.json will be lost when selecting "Debug & Launch Settings" from the context menu.

* #### Workaround:
Save any changes to this file before selecting "Debug & Launch Settings" from the context menu.

#### Reloading a project that has been edited in folder mode may fail with a dialog
* #### Issue:
If you have edited a project file from the folder mode, it may fail to reload later from the
Solution mode.

* #### Workaround:
Try reloading the project again. If it still fails to load, reload the Solution.

### <a id="KITT"> </a>Testing Tools Issues

#### Discovery fails for UWP projects with a UITestMethod created in Visual Studio VS2017
* #### Issue:
Discovery fails for UWP projects with test methods adorned with the UITestMethod attribute, created in Visual Studio VS2017.

* #### Workaround:
Upgrade MSTest.TestAdapter NuGet package to the latest version (1.1.12+).

#### Run tests fail from Visual Studio when a test is adorned by a DeploymentItem attribute
* #### Issue:
Test projects created in Visual Studio that have tests adorned by a DeploymentItem attribute fail to run, throwing a FileNotFound exception.

* #### Workaround:
Add the following DeploymentItem as well on the test method\containing test class: `[DeploymentItem("Microsoft.VisualStudio.TestPlatform.TestFramework.Extensions.dll")]`.
This will be fixed in an upcoming version of MSTest.TestFramework and MSTest.TestAdapter.

### <a id="KIDebugger"> </a>Debugging and Diagnostics

#### Remote Tools for Visual Studio 2017 Preview are not available
* #### Issue:
We have not made an update for the Remote Tools for Visual Studio 2017 Preview available.

* #### Workaround:
The [Remote Tools for Visual Studio 2017](https://www.visualstudio.com/downloads#remote-tools-for-visual-studio-2017) is compatible with Visual Studio 2017 Preview. 
However, if you are interested in using the latest preview version of the remote debugger, see [Run the remote debugger from a file share](https://docs.microsoft.com/visualstudio/debugger/remote-debugging#optional-to-run-the-remote-debugger-from-a-file-share).


### <a id="KILSL"> </a>Lightweight Solution Load Issues

#### Some extensions may not behave as expected when Lightweight Solution load is enabled
* #### Issue:
Some extensions might not behave as expected when Lightweight Solution load is enabled.

* #### Workaround:
Disable Lightweight Solution load and reload the Solution.

#### Edit and Continue does not work when Lightweight Solution load is enabled
* #### Issue:
Edit and Continue may not work as expected when Lightweight Solution load is enabled.

* #### Workaround:
Disable Lightweight Solution load and reload the Solution before using Edit and Continue.

#### F# projects won't build or support symbol navigation when Lightweight Solution load is enabled
* #### Issue:
When Lightweight Solution load is enabled, F# projects may not properly build and symbols may not be fully available in GoTo.

* #### Workaround:
Disable Lightweight Solution load for Solutions that contain F# projects.

#### Warnings are duplicated when Lightweight Solution load is enabled

* #### Issue:
When building a Solution with Lightweight Solution load enabled, warnings from project files emitted by the build may appear duplicated in the Error List.

* #### Workaround:
Disable Lightweight Solution load and reload the Solution.


### <a id="KIExtensibility"> </a>Extensibility Issues

#### Error occurs when adding a Custom Command or a Custom Tool Window
* #### Issue:
Attempting to add a Custom Command or a Custom Tool Window to a project that contains a XAML file may result in the custom command or tool window to not be added to the project.  An error may also appear with the text: "Sequence contains more than one matching element".

* #### Workaround:
    1. Close all opened XAML files.
    2. Close Visual Studio.
    3. Start Visual Studio and open your project.
    4. Add the custom command or custom tool window to the project (before loading a XAML file).

### <a id="KITeamExplorer"> </a>Team Explorer Issues

#### Git commands that alter the index might fail if there is an orphaned index.lock
* #### Issue:
First reported as [Git undo and unstage failing](https://developercommunity.visualstudio.com/content/problem/4608/git-unstage-and-git-undo-does-not-work.html),
performing a Git command that alters the index will fail if there is an orphaned Git index.lock.
Git uses this file to indicate to other Git processes that the repository is locked for editing.
If the editing process became unresponsive or was terminated, the index.lock file can get left behind and prevent other Git processes from editing the repository.

* #### Workaround:
When this issue happens, please look in the .git/ folder of your repository and check for an index.lock file. If one exists, and you're **not** actively running a Git command, delete the file.

#### Cloning via SSH fails
* #### Issue:
Cloning via SSH fails in Team Explorer. A fix to this issue will be available in a future update.

* #### Workaround:
If you want to use SSH, clone from the command line then add the repository to your list of local repositories in Team Explorer.
You can also clone via HTTP in Team Explorer then set your remotes to use SSH in Settings > Repository Settings > Remotes.

#### Cancellation for Git commands in Team Explorer does not work
* #### Issue:
Cancelling a Git command (e.g. a clone) in Team Explorer does not work and instead the operation completes. This issue does not affect other Team Explorer operations.

* #### Workaround:
There is no workaround at this time.

### <a id="KIManagedWorkload"></a> Managed Workload Development Issues

#### .NET 2.0/3.0/3.5 projects generate assemblies with incorrect target
* #### Issue:
After you install Visual Studio 2017 on a fresh machine without first selecting .NET Framework 3.5 development tools from Individual components tab and build a .NET 2.0 (or 3.0/3.5) project, some assemblies (like resources) after the build will be marked as .NET4.0 even when the project targets .NET 2.0.
This happens because Visual Studio 2017 no longer installs .NET Framework 3.5 SDK by default and as the SDK is missing the build process defaults to .NET 4.X SDK.

* #### Workaround:
.NET 3.5 SDK is now only an optional component, so if your development targets a .NET 3.5 product (2.0/3.0/3.5) then you will also need to select “.NET Framework 3.5 development tools” from the Individual components tab during installation. This will install the required .NET 3.5 SDK on the machine that is used during the build process.


### <a id="xamarin"></a> Xamarin Workload Known Issues

#### Build canceled with error: Project 'project_name' requires the following components installed on your machine.

* #### Issue:
Building Android applications can require installing additional components. This can be needed in several cases, like if you're using a new component, NuGet Package, or if it's the first Xamarin.Forms solution you're building on a given machine. Xamarin for Visual Studio detects the lack of those missing resources, and [shows an error](https://developer.xamarin.com/releases/vs/xamarin.vs_4/xamarin.vs_4.6/#Known_issues) informing these resources must be downloaded and installed.

* #### Workaround:
Double-click the error message displayed. This will automatically install missing components and allow you to build your project.

Please keep in mind that you need to have Intellisense errors visible in the list, otherwise you won't be able to see that error. If you try to build any project in the solution without installing the missing components, the build will be canceled. You cannot build without installing those components. Please ensure Intellisense errors are visible to be able to start installing them.


### <a id="KIUWPWorkload"></a> Universal Windows Platform Development Workload Issues

#### XAML designer is not available
* #### Issue:
When developing a UWP app, the XAML designer is not available.

* #### Workaround:
The XAML designer is not available unless the Target Platform Version for the app is the same or lower than the version of Windows 10 on which you are running Visual Studio. 
For example: if you are running Visual Studio on "Windows 10 Anniversary Update (build 14393)" and the target platform version for your UWP app is "Windows 10 Creators Update", 
the XAML designer will not be available for that app project. To ensure that you can use the XAML designer, upgrade to the latest version of Windows 10.

#### Visual Studio update required when opening a UWP project
* #### Issue: 
When opening a project in Visual Studio that was created in Visual Studio 2017 Preview, you may get a dialog titled “Visual Studio update required” that instructs you to install an updated platform SDK. The Windows SDK archive website linked to from the dialog does not list the specified version of the Windows SDK.

* #### Workaround:
  This is expected, as Visual Studio 2017 Preview included a pre-release Windows SDK. To fix this, in your project file, change the target platform version to the Windows SDK version you intend to target. For the Windows 10 Creators Update, this is "10.0.15063.0".
  1. Right click on the project, and select "Edit [AppName].[xx]proj", where [xx]proj is .csproj, .vcxproj, etc. 
  2. In the project file "TargetPlatformVersion" (for C#, VB, and JS projects) or "WindowsTargetPlatformVersion" (for C++) project properties, and change the value to "10.0.15063.0" or to the version of another SDK you have installed. 

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

#### Some XAML controls are not available in the toolbox 
* #### Issue:
When using XAML controls that are installed from Extension SDKs, you may not see some of the controls in the toolbox.

* #### Workaround:
If you want to use these controls, you can manually add them in the XAML Editor.

### <a id="KINativeDesktopWorkload"> </a>Visual C++ Desktop Known Issues

#### Unable to build a newly-created C++ Win32 desktop project after installing the Windows 10 Creators Update SDK (10.0.15063.0)
* #### Issue:
The Windows 10 Creators Update SDK has been refactored to reduce installation footprint by default. 
Installing this SDK via the UWP workload will not install the headers/libs required for Win32 C++ Desktop Projects.
However, Visual C++ Desktop projects will detect this SDK as installed and will, by default, attempt to target the 10.0.15063.0 in newly-created projects.

* #### Workaround:
In the Visual Studio Installer:
    * Select the "Windows 10 SDK (10.0.15063.0) for Desktop C++ x86 and x64" feature under the "Desktop development with C++" workload.
    * An alternative is to choose an earlier SDK version, which is fully installed on the system (e.g. 10.0.14393.0), from the Project Properties dialog.

### <a id="KIxamarin"> </a>Xamarin Issues

#### Build cancelled with error: "Project 'project_name' requires the following components installed on your machine"
* #### Issue: 
Building Android applications can require installing additional components. This may be needed in several cases, like if you're using a new component, NuGet Package, or if it's the first Xamarin.Forms solution you're building on a given machine.

* #### Workaround:
    * Ensure that Intellisense errors are visible in the list and Xamarin for Visual Studio will detect those missing resources. You will be shown an error informing you of the resources that are required to download and install. Double click on the error in the list to start downloading and installing the missing components. You need to have Intellisense errors visible in the list, otherwise you won't be able to see that error. The build will be cancelled if you try to build any project in the solution without installing the missing components.
    * An optional way to install missing components is to build from the command-line.


### <a id="KIother"> </a>Other Issues

#### Unable to connect to (LocalDB)\\MSSQLLocalDB in x86 machine
* #### Issue:
It is a known intermittent localDB 2014 issue where (LocalDB)\MSSQLLocalDB cannot be connected in x86 machine.

* #### Workaround:
Run the following commands in the command prompt:
 1. sqllocaldb stop mssqllocaldb.
 2. sqllocaldb delete mssqllocaldb.
 3. sqllocaldb start mssqllocaldb.

#### Unable to create function breakpoints in SharePoint workflows
* #### Issue:
The Breakpoints pane in Visual Studio previously allowed creation of breakpoints of type "Workflow". This functionality has been removed.

* #### Workaround:
Create breakpoints in the designer view using the right-click menu.

#### SharePoint Workflow Activities may not load correctly in the Workflow Designer
* #### Issue:
When you create a new SharePoint Add-in or Solution project with a workflow and SharePoint Activities, you may see the following error in the workflow designer after building the project, "Activity could not be loaded because of errors in the XAML". By default, a new SharePoint Add-in project targets .NET Framework 4.5.2. To use SharePoint Activities in a workflow the project must target .NET Framework 4.5.

* #### Workaround:
    * Access Project Properties, either from the Context Menu in Solution Explorer or via the Project Menu.
    * On the Application Tab, set the Target framework to .NET Framework 4.5.

#### SharePoint project with a workflow may fail to build when Dynamic Values are used
* #### Issue:
A SharePoint project with a workflow may fail to build with the following error, "The type or namespace name 'Activities' does not exist in the namespace 'Microsoft' (are you missing an assembly reference?)".  

* #### Workaround:
    1. Expand the Workflow node in the Solution Explorer and View the Code for the workflow.xaml file in our project by hitting F7 or via the context menu when the file is selected in Solution Explorer.
    2. Add the following reference to the <TextExpression.ReferencesForImplementation> section:
        <AssemblyReference>Microsoft.Activities</AssemblyReference>.

#### The SharePoint Add-In project wizard may not correctly detect the version of SharePoint the project is targeting
* #### Issue:
When you create a SharePoint Add-in project, the new project dialog tries to detect the correct version of SharePoint based on the site URL that you provide.  However, if you also have Visual Studio 2015 or an older version of the SharePoint Client Components installed, the new project dialog may incorrectly determine that the project is targeting SharePoint 2016 instead of SharePoint Online.

* #### Workaround:
For new projects, when creating a new SharePoint Add-in project, be sure and verify that the last page of the new project dialog has selected the correct version of SharePoint your project is targeting. For existing projects, you can change the version of SharePoint the project is targeting by doing the following:  
   1. 	Access Project Properties, either from the Context Menu in Solution Explorer or via the Project Menu.  
   2. 	On the SharePoint Tab, set the Target SharePoint Version to the correct version of SharePoint your project is targeting.  

#### Office Web Add-In project may contain warnings in the Error List
* #### Issue:
The _officeintellisense.js file contains a declaration for an “Office’ object that conflicts with one declared in the office.d.ts file.  

* #### Workaround:  
These warnings should not impact your project but, you can remove the warnings by commenting out the extra “var Office” declaration in Scripts\Office\ _officeintellisense.js file or by excluding this file from the project with the “Exclude From Project” context menu in Solution Explorer.  

#### .NET Targeting Packs Not Included in Web Development Tools Workload of the Visual Studio Build Tools SKU
* #### Issue:
The Web development tools workload in Visual Studio Build Tools SKU does not contain any .NET Targeting packs.  This means that .NET binaries can only be built to target 4.6.

* #### Workaround:
Manually download and install .NET targeting packs from Microsoft to the build machine.

#### Files included by globbing are not shown in Solution Explorer if they are outside of a project's root
* #### Issue:
For .NET Core and ASP.NET Core projects, any files included by globbing patterns will only be shown in
the Solution Explorer if the files are included under the project's root directory.  Any files outside
of the project's root directory will not be shown.  Turning on "Show All Files" will not correct
this issue.  You will also not be able to navigate to these files via search, find in files, goto, or
go to definition.

* #### Workaround:
There is no known workaround for showing the missing files in the Solution Explorer or navigating to them.
However, building and debugging these projects should work without issues. In most cases, you
should be able to edit these files normally by opening them manually. We recommend using individually
linked files in place of external globbing patterns for the time being.

#### VS Test Professional 2017 SKU does not have Team Explorer, limiting access to Excel-based/SSRS-based reports from TFS Warehouse/Cube
* #### Issue is now fixed in version 15.1 (26403.00):

    Installing the VS Test Professional SKU no longer installs VS Team Explorer, which is used to access to Excel-based/SSRS-based based reports from TFS Warehouse/Cube. There is no impact to the Microsoft Test Manager (MTM) client – it continues to work without any known issues.

#### R Tools are not fully localized
* #### Issue:
Users with language packs installed may see some labels in English when using R.

* #### Workaround:
None, but an update with fully translated strings will be released as soon as possible.
