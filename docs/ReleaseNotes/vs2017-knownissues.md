---
title: Visual Studio 2017 Known Issues
description: Visual Studio 2017 Known Issues
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 08/14/2017
ms.topic: release-article, localize
ms.prod: vs-devops-alm
ms.technology: vs-devops-articles
ms.assetid: f74efd99-3245-4733-be4f-4ae87d1ec3ca
---

# <a id="top"> </a> Visual Studio 2017 version 15.3 Known Issues

Visit the [current release notes](vs2017-relnotes.md) page to learn more about Visual Studio 2017. You may also visit the [Downloads](https://www.visualstudio.com/downloads/) page to acquire other Visual Studio products.

> [!NOTE]
> We are fully committed to listening to your feedback. Please visit the [Developer Community](https://developercommunity.visualstudio.com/index.html) Site for searching the latest issues, logging new issues and upvoting existing issues.

  * [Installation](#KIinstall)
  * [Editor and IDE](#KIeditoride)
  * [NuGet](#KINuGet)
  * [Web Tools](#KIWebTools)
  * [.NET Core Tools](#KICore)
  * [Open Folder](#KIOpenFolder)
  * [Testing Tools](#KITT)
  * [Debugging and Diagnostics](#KIDebugger)
  * [Lightweight Solution Load](#KILSL)
  * [Application Insights](#KIAppInsights)
  * [Team Explorer](#KITeamExplorer)
  * [Managed Workload Development](#KIManagedWorkload)
  * [Universal Windows Platform Development Workload](#KIUWPWorkload)
  * [Visual C++ Desktop](#KINativeDesktopWorkload)
  * [Xamarin](#KIxamarin)
  * [F# Tools](#KIFSharp)
  * [Other](#KIother)

****

### <a id="KIinstall"> </a>Installation Issues

#### Cloud Explorer cannot be launched
* #### Issue:
If you install Cloud Explorer with the Web development workload, Cloud Explorer may fail on launch with error message 'Setup cannot proceed when Visual Studio is running. Please close Visual Studio and retry'. The error is caused by missing dependencies.

* #### Workaround:
Install the Azure development workload then launch Cloud Explorer again.

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

#### DISM fails or causes setup to hang
* #### Issue:
Visual Studio may report errors when enabling certain OS features using DISM, e.g. NetFx4Extended-ASPNET45. This could be the result of corrupted manifests.

* #### Workaround:
1. Open a command prompt as administrator and repair the DISM manifests by running *dism /online /cleanup-image /restorehealth*
2. Reboot
3. Repair Visual Studio

### <a id="KIeditoride"> </a>Editor and IDE Issues

#### Changed files display yield/warning signs in Solution Explorer when using Windows Insider builds.

* #### Issue: 
In the some Windows Insiders builds, saving files in .NET Core, UWP, and Shared projects may result in yield/warning signs next to the changed files.

* #### Workaround:
The yield/warning signs are benign and may be safely ignored. Reloading the solution will remove the yield/warning signs.

#### Opening a project while GoTo is active will cause Visual Studio to crash.

* #### Issue:
Opening a project while GoTo is active will cause Visual Studio to crash.

* #### Workaround:
Ensure GoTo is closed before attempting to open a new project.

#### JavaScript IntelliSense stops working

* #### Issue:
When you open a project with more than 25Mb of JavaScript code, it displays the error "The language service is disabled for project because it included a large number of .js files. Consider excluding files using 'exclude' section of a 'tsconfig.json' file".

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

### <a id="KINuGet"> </a> NuGet Issues


#### While using Package Manager Console, the 'Enter' key may not work
* #### Issue:
On occasion, the Enter key does not work in the Package Manager Console. If you see this, please check out the progress on the fix, and provide any additional helpful information about your repro steps ([NuGet#4204](https://github.com/NuGet/Home/issues/4204) and [NuGet#4570](https://github.com/NuGet/Home/issues/4570)).

* #### Workaround: 
Restart Visual Studio and open the PMC before you open the solution. Alternatively, you can delete the project.lock.json and restore it again.

#### A package in a .NET Core project that contains an assembly with an invalid signature, can trigger an infinite restore loop 
* #### Issue:
Occasionally, when you use a package that contains an assembly with an invalid signature or when the package version is set with 'DateTime' ticker, it causes the package auto-restore to run in an infinite loop ([dotnet/project-system#1457](https://github.com/dotnet/project-system/issues/1457)).

* #### Workaround:
There is no workaround at this time.

#### Unable to view, add, or update DotNetCLITools using NuGet Package Manager
* #### Issue:
NuGet Package Manager does not display or allow add/update of DotNetCLITools ([NuGet#4256](https://github.com/NuGet/Home/issues/4256)).

* #### Workaround:
DotNetCLIToolReferences must be manually edited in your project file.

#### Retargeting target framework version may lead to incomplete IntelliSense
* #### Issue:
If you retarget a target framework version, it may lead to incomplete IntelliSense in Visual Studio. This happens when you use PackageReferences as the package manager format ([NuGet#4216](https://github.com/NuGet/Home/issues/4216)).

* #### Workaround:
Do a manual restore.

### <a id="KIWebTools"></a> Web Tools Known Issues

#### MVC4 projects do not connect to SQL Server LocalDB at runtime
* #### Issue:
When you run an MVC4 project in Visual Studio, the database access by the application may fail if it uses SQL Server Express LocalDB 2012. This is caused because MVC4 projects by default depend on SQL Server Express LocalDB 2012 which is not installed with Visual Studio 2017.

* #### Workaround:
Upgrade the project to use SQL Server Express LocalDB 2016, or manually download and install [SQL Server Express LocalDB 2012](https://go.microsoft.com/fwlink/?LinkID=627336) on the machine.

### <a id="KICore"> </a>.NET Core Tools Issues

For a current list of issues and workarounds with Visual Studio 2017 15.3, .NET Core and ASP.NET Core 2.0 for see our [GitHub page.]( https://go.microsoft.com/fwlink/?linkid=853703)

### <a id="KIOpenFolder"> </a>Open Folder Issues

#### IntelliSense not available while editing launch.vs.json or tasks.vs.json
* #### Issue:
When you edit a launch.vs.json or tasks.vs.json file, IntelliSense is not available.

* #### Workaround:
Install the "ASP.NET and Web Development" workload.

#### C# refactoring may have inconsistent results
* #### Issue:
When you refactor C# or VB code, it may have inconsistent results in folder mode.

* #### Workaround:
Load C# or VB projects in Solution mode.

#### Unsaved edits to launch.vs.json may be lost
* #### Issue:
Unsaved edits to launch.vs.json will be lost when you select "Debug & Launch Settings" from the context menu.

* #### Workaround:
Save any changes to this file before you select "Debug & Launch Settings" from the context menu.

#### Reloading a project that has been edited in folder mode may fail with a dialog
* #### Issue:
If you have edited a project file from the folder mode, it may fail to reload later from the
Solution mode.

* #### Workaround:
Reload the project again. If it still fails to load, reload the Solution.

### <a id="KITT"> </a>Testing Tools Issues

#### Native C++ unit testing code coverage
* #### Issue:
Native C++ unit testing code coverage fails with an error stating that no modules were loaded.
 
* #### Workaround:
Rebuild your code with debugging information generated with the /DEBUG:FULL option. The setting can be found under "project properties | Configuration Properties | Linker | Debugging".

#### Native C++ unit testing profiling
* #### Issue:
Native C++ unit test profiling fails with an error stating that no modules were loaded.
 
* #### Workaround:
Rebuild your code with debugging information generated with the /DEBUG:FULL option. The setting can be found under "project properties | Configuration Properties | Linker | Debugging".

#### .NET Core unit testing code coverage
* #### Issue:
Launching Code Coverage analysis from the Test Explorer does not work in the case of .NET Core unit test projects.
 
* #### Workaround:
Please see the ["Working with Code Coverage"](https://github.com/Microsoft/vstest-docs/blob/master/docs/analyze.md#coverage) document.

#### Lightweight Solution Load interaction
* #### Issue:
When Lightweight Solution Load is in effect, the 'Test Project' dropdown in the Create IntelliTest dialog may not list all available test projects.
 
* #### Workaround:
Projects that are not already loaded will not be shown. Load the relevant projects from the Solution Explorer to ensure that are shown here.

* #### Issue:
For solutions with Lightweight Solution Load enabled, tests may not be discovered from Deferred projects (projects that are not loaded in the lightweight solution mode).

* #### Workaround:
Either disable Lightweight Solution load for the solution or load the test projects of interest (by expanding the project node in Solution Explorer) and rebuild to discover tests.

### <a id="KIDebugger"> </a>Debugging and Diagnostics

#### Update variable inside the local window doesn't immediately reflect in the UI correctly for node.js project
* #### Issue:
When trying to update a local variable value inside the local window for a node.js project, it appears in the UI that the change doesn't take effect. The change to the local variable vable actually works correctly despite the UI update issue. The UI will be updated correctly after the execution continues.

* #### Workaround:
The UI will be updated properly after stepping into the next line of code.

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

#### IntelliSense may not update after configuration change
* #### Issue:
IntelliSense may not get updated after configuration change (e.g. release to debug and vice versa). The impact will depend on code differences due to configuration change.

* #### Workaround:
Reload solution after configuration change.

#### Deferred projects do not show up in the list of projects for “Create IntelliTest” and “Create Unit Test” wizards
* #### Issue:
Deferred projects (projects that are not loaded in the lightweight solution mode) do not show up in the list of test projects for both the “Create IntelliTest” and “Create Unit Test” wizards. This may be relevant if you are creating unit tests for those projects that are not loaded.

* #### Workaround:
Expand additional projects as needed.

#### Some references are not shown in Object Browser when Lightweight Solution Load is enabled

* #### Issue:
When Lightweight Solution Load is on and a project isn't expanded in the Solution Explorer, Object Browser will not show the references from such projects.

* #### Workaround:
To show the references, expand the project in Solution Explorer.

Please visit the [Optimize Visual Studio Startup Time](https://go.microsoft.com/fwlink/?linkid=849131) page to learn more about lightweight solution load and troubleshooting tips.


### <a id="KIAppInsights"> </a>Application Insights Issues

#### Application Insights Extensible Providers fail to load when right-clicking a project
* #### Issue:
Application Insights Extensible Providers fail to load when right-clicking a project in Visual Studio. This occurs because Extensible Providers load binaries from NuGet in a background thread, after the solution is loaded. Some Extensible Providers, like the ones for PHP and Azure Service Fabric are already installed, so they don't have this issue. A fix to this issue will be available via an auto-update shortly after the initial version of Visual Studio 2017.

* #### Workaround:
Open a command prompt with administrative privileges, then run the following based on your version of Visual Studio:
    * Visual Studio Enterprise
        * "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\IDE\VsRegEdit.exe" set "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise" HKCU AppInsightsGettingStarted UseBackgroundThreadToFetchProjectInfo string Disabled.

    * Visual Studio Professional
        * "C:\Program Files (x86)\Microsoft Visual Studio\2017\Professional\Common7\IDE\VsRegEdit.exe" set "C:\Program Files (x86)\Microsoft Visual Studio\2017\Professional" HKCU AppInsightsGettingStarted UseBackgroundThreadToFetchProjectInfo string Disabled.

    * Visual Studio Community
        * "C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\VsRegEdit.exe" set "C:\Program Files (x86)\Microsoft Visual Studio\2017\Community" HKCU AppInsightsGettingStarted UseBackgroundThreadToFetchProjectInfo string Disabled.

#### Some ASP.NET Core projects fail to add the Application Insights JavaScript snippet for page view collection
* #### Issue:
ASP.NET Core projects configured with Application Insights that were not created with Visual Studio 2017 will fail to run. Trying to run such an app will produce the error, "InvalidOperationException: No service of type 'Microsoft.ApplicationInsights.AspNetCore.JavascriptSnippet' has been registered".

* #### Workaround:
After configuring with Application Insights, a JavaScript snippet is added to the file Views/Shared/_Layout.cshtml. There are two workarounds, depending on whether you want Application Insights to collect page views from your app:
 1. Collect page views - Add ".UseApplicationInsights()" to the WebHostBuilder in Program.cs.
 2. Don't collect page views - Delete the following lines from Views/Shared/_Layout.cshtml:
    * @inject Microsoft.ApplicationInsights.AspNetCore.JavaScriptSnippet JavaScriptSnippet.
    * @Html.Raw(JavaScriptSnippet.FullScript).

### <a id="KITeamExplorer"> </a>Team Explorer Issues

#### Git commands that alter the index might fail if there is an orphaned index.lock
* #### Issue:
When you perform a Git command that alters the index, it fails if there is an orphaned Git index.lock. Git uses this file to indicate to other Git processes that the repository is locked for editing. If the editing process became unresponsive or was terminated, the index.lock file can be left behind and prevent other Git processes from editing the repository.

* #### Workaround:
When this issue happens, please look in the .git/ folder of your repository and check for an index.lock file. If one exists, and you're **not** actively running a Git command, delete the file.

#### Cloning via SSH fails
* #### Issue:
Cloning via SSH fails in Team Explorer. A fix to this issue will be available in a future update.

* #### Workaround:
If you want to use SSH, clone from the command line then add the repository to your list of local repositories in Team Explorer. You can also clone via HTTP in Team Explorer then set your remotes to use SSH in Settings > Repository Settings > Remotes. This has been fixed in Visual Studio 2017 version 15.3, which is in preview. 

#### Cancellation for Git commands in Team Explorer does not work
* #### Issue:
Cancelling a Git command (e.g. a clone) in Team Explorer does not work and instead the operation completes. This issue does not affect other Team Explorer operations.

* #### Workaround:
There is no workaround at this time.

### <a id="KIManagedWorkload"></a> Managed Workload Development Issues

#### .NET 2.0/3.0/3.5 projects generate assemblies with incorrect target
* #### Issue:
After you install Visual Studio 2017 on a fresh machine without first selecting .NET Framework 3.5 development tools from Individual components tab, and build a .NET 2.0 (or 3.0/3.5) project, some assemblies (like resources) after the build will be marked as .NET4.0 even when the project targets .NET 2.0. This happens because Visual Studio 2017 no longer installs .NET Framework 3.5 SDK by default, and the SDK is missing the build process defaults to .NET 4.X SDK.

* #### Workaround:
.NET 3.5 SDK is now only an optional component. If you target a .NET 3.5 product (2.0/3.0/3.5), then you will also need to select .NET Framework 3.5 development tools from the Individual components tab during installation. This will install the required .NET 3.5 SDK on the machine used during the build process.

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
When you open a project in Visual Studio that was created in Visual Studio 2017 Preview, you may get a dialog titled “Visual Studio update required” that instructs you to install an updated platform SDK. The Windows SDK archive website linked to from the dialog does not list the specified version of the Windows SDK.

* #### Workaround:
  This is expected, as Visual Studio 2017 Preview included a pre-release Windows SDK. To fix this, in your project file, change the target platform version to the Windows SDK version you intend to target. For the Windows 10 Creators Update, this is "10.0.15063.0".
  1. Right click on the project, and select "Edit [AppName].[xx]proj", where [xx]proj is .csproj, .vcxproj, etc. 
  2. In the project file "TargetPlatformVersion" (for C#, VB, and JS projects) or "WindowsTargetPlatformVersion" (for C++) project properties, and change the value to "10.0.15063.0" or to the version of another SDK you have installed. 

#### Some XAML controls are not available in the toolbox 
* #### Issue:
When you use XAML controls that are installed from Extension SDKs, you may not see some of the controls in the toolbox.

* #### Workaround:
If you want to use these controls, you can manually add them in the XAML Editor.

### <a id="KINativeDesktopWorkload"> </a>Visual C++ Desktop Known Issues

#### MFC Application wizard does not work in some languages
* #### Issue:
For some VS languages: In the "File->New->Project..." dialog, selecting "Visual C++->MFC->MFC Application" will fail to create a new solution/project when selected.

* #### Workaround:
Use "Visual C++->MFC Application" (i.e. the wizard under the Visual C++ root node) within the "File->New->Project..." dialog.

#### MFCCtlWiz project template doesn't work
* #### Issue:
Selecting the "MFCCtlWiz" project template in File->New Project has no effect. This was an (incorrect) old entry for the MFC ActiveX control wizard that was missed.

* #### Workaround:
Ignore this entry. Use the "MFC ActiveX control" wizard instead.

#### Unable to build a newly-created C++ Win32 desktop project after installing the Windows 10 Creators Update SDK (10.0.15063.0)
* #### Issue:
The Windows 10 Creators Update SDK has been refactored to reduce installation footprint by default. 
When you Install this SDK via the UWP workload, it will not install the headers/libs required for Win32 C++ Desktop Projects.
However, Visual C++ Desktop projects will detect this SDK as installed and will, by default, attempt to target the 10.0.15063.0 in newly-created projects.

* #### Workaround:
In the Visual Studio Installer:
    * Select the "Windows 10 SDK (10.0.15063.0) for Desktop C++ x86 and x64" feature under the "Desktop development with C++" workload.
    * An alternative is to choose an earlier SDK version, which is fully installed on the system (e.g. 10.0.14393.0), from the Project Properties dialog.

#### Running ResEdit with only the Windows 10 Creators Update SDK (10.0.15063.0) installed, will fail due to missing rcdll.dll
* #### Issue:
When you run ResEdit with only the Windows 10 Creators Update SDK (10.0.15063.0) installed, it will fail due to missing rcdll.dll. 
This issue is due to the RS2 SDK’s refactoring of directory layout, which results in the rcdll.dll to be included in a versioned directory location.

* #### Workaround:
Install the Anniversary Update of the Windows 10 SDK (10.0.14393.0) or earlier.

### <a id="KIxamarin"> </a>Xamarin Issues

#### Build cancelled with error: "Project 'project_name' requires the following components installed on your machine"
* #### Issue: 
Building Android applications can require installation of additional components. This may be needed in several cases. For example, if you use a new component such as NuGet Package, or if it's the first Xamarin.Forms solution you have built on a given machine.

* #### Workaround:
    * Ensure that IntelliSense errors are visible in the list. Xamarin for Visual Studio will detect those missing resources. You will be shown an error that informs you of the resources that are required to download and install. Double click on the error in the list. This will start the download and install the missing components. You need to have IntelliSense errors visible in the list, otherwise you won't be able to see that error. The build will be cancelled if you try to build any project in the solution without installing the missing components.
    * An optional way to install missing components is to build from the command-line.

### <a id="KIPython"> </a>Python Issues

#### Python Extension Module template does not build
* #### Issue:
When the Python Native Development optional component is selected, a C++ project template is installed for building extension modules. This template defaults to Python 3.5, which may not be installed if Python 3.6 was selected.

* #### Workaround:
Unload the project and edit it. There is a `PythonVersion` property that contains "3.5" that should read "3.6" in order to build against Python 3.6.

#### Azure Cloud Service projects do not load
* #### Issue:
When you create an Azure Cloud Service project with Python roles, you could see a "The system cannot find the file specified" error. This is because the Python workload does not correctly install all required files by default.

* #### Workaround:
Open the Visual Studio installer and modify your installation. In the Python development workload, check "Azure Cloud Services core tools" and apply the modification. This will add the missing files.

#### Django management console fails to start
* #### Issue:
When you open the management console for a Django project via the project's context menu, you receive an error that contains `django.core.exceptions.ImproperlyConfigured`. This is because the `DJANGO_SETTINGS_MODULE` environment variable is not correctly set before the console is started.

* #### Workaround:
Add the following code to your `settings.py` file, substituting the actual name of your settings module for the placeholder.

```python
import os
os.environ.setdefault("DJANGO_SETTINGS_MODULE", "<module name placeholder>")
```

When you open the management console, the first command you run should be `django.setup()`. After this, the console should behave normally.

#### Editing HTML files in a Django project displays error
* #### Issue:
When you open an HTML file that is part of a Django project, a message box is displayed and there is no JavaScript support. This is because JavaScript support in the editor depends on having a version of the TypeScript SDK installed, and the default installation options do not include TypeScript.

* #### Workaround:
Open the Visual Studio installer and modify your installation. Under Individual Components, find and select any "TypeScript SDK" option and apply the modification.

#### Modules in search paths do not appear in import completion list
* #### Issue:
After you add a Search Path to a project, the packages and modules available within that path do not appear in the `import` and `from ... import` completion lists.

* #### Workaround:
No workaround is available. If you enter the name of the package or module, completions from those modules should appear correctly.

### <a id="KIdotnetcore"> </a>.NET Core Issues

For a current list of issues and workarounds with .NET Core and ASP.NET Core 2.0 see our [GitHub page](https://go.microsoft.com/fwlink/?linkid=853703).

### <a id="KITestingTools"> </a>Testing Tools Issues

#### Native C++ unit testing code coverage
* #### Issue:
Native C++ unit testing code coverage fails with an error stating that no modules were loaded.
 
* #### Workaround:
Rebuild your code with debugging information generated with the /DEBUG:FULL option. The setting can be found under "project properties | Configuration Properties | Linker | Debugging".

#### .NET Core unit testing code coverage
* #### Issue:
Launching Code Coverage analysis from the Test Explorer does not work in the case of .NET Core unit test projects.
 
* #### Workaround:
Please see under "Working with Code Coverage" here  https://github.com/Microsoft/vstest-docs/blob/master/docs/analyze.md#coverage

#### Create IntelliTest project options
* #### Issue:
When Lightweight Solution Load is in effect, the 'Test Project' dropdown in the Create IntelliTest dialog may not list all available test projects.
 
* #### Workaround:
Projects that are not already loaded will not be shown. Load the relevant projects from the Solution Explorer to ensure they are shown here.

### <a id="KIDebugger"> </a>Debugging and Diagnostics Issues
### <a id="KIFSharp"> </a> F\# Tools

* #### Issue:
Enter, Backspace, and Arrow keys will fail to work intermittently.  Additionally, opening a solution with open documents will result in them not working for those documents.

* #### Workaround:
   * We have a fix for this in the [Visual F# nightly release](https://blogs.msdn.microsoft.com/dotnet/2017/03/14/announcing-nightly-releases-for-the-visual-f-tools/), and the fix will also be available in a future update.  Closing and re-opening an affected file will also fix it for that file, though this is just temporary.  
   * There are multiple issues related to F# support for .NET Core and .NET Standard projects, which we do not consider fully supported.  We're currently working on full support.  We wish to call out those issues here, though, in case you do choose to load these types of projects.

* #### Issue:
No way to create a new .NET Core or .NET Standard project in Visual Studio.

* #### Workaround:
None at this time.  We have disabled creating new F# and .NET Core/.NET Standard projects in Visual Studio until it is fully supported.

* #### Issue:
Dependencies do not load and IntelliSense reports errors, even though the program compiles, runs, and debugs.

* #### Workaround:
None at this time.

* #### Issue:
Newly-added files are not recognized by IntelliSense, even though the program compiles, runs, and debugs.

* #### Workaround:
None at this time.

### <a id="KIPython"> </a>Python

#### Remote debugger fails to attach

* #### Issue:
When attaching to a remote machine that is using [ptvsd](https://pypi.org/project/ptvsd), an error message appears.

* #### Workaround:
Significant changes were made to `ptvsd` in this release. Please update the version of `ptvsd` on your remote machine.

#### Remote debugger breaks randomly

* #### Issue:
When debugging remote code, the debugger may stop running as if an exception has been raised but without displaying any information.

* #### Workaround:
No known workaround exists. Press F5 or Continue to resume the process.

#### Tests with decorators do not appear in the Test Window

* #### Issue:
When test methods also have a decorator, they may not be shown in the Test Window:

```python
    @patch.object(os.path, 'isfile')
    def test_A(self):
        ''' Doesn't appear in Test Window'''
        self.fail("Not implemented")

    def test_B(self):
        ''' This does appear in Test Window'''
        self.fail("Not implemented")
```

* #### Workaround: 
No workaround currently exists, other than removing the decorator. Use `unittest` or PyTest from the command line to run these tests.

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
When you create a new SharePoint Add-in, or Solution project with a workflow and SharePoint Activities, you may see an "Activity could not be loaded because of errors in the XAML" error in the workflow designer after building the project. By default, a new SharePoint Add-in project targets .NET Framework 4.5.2. To use SharePoint Activities in a workflow the project must target .NET Framework 4.5.

* #### Workaround:
    * Access Project Properties, either from the Context Menu in Solution Explorer or via the Project Menu.
    * On the Application Tab, set the Target framework to .NET Framework 4.5.

#### The SharePoint Add-In project wizard may not correctly detect the version of SharePoint the project is targeting
* #### Issue:
When you create a SharePoint Add-in project, the new project dialog tries to detect the correct version of SharePoint based on the site URL that you provide.  However, if you also have Visual Studio 2015 or an older version of the SharePoint Client Components installed, the new project dialog may incorrectly determine that the project is targeting SharePoint 2016 instead of SharePoint Online.

* #### Workaround:
For new SharePoint Add-in projects, be sure to verify that the last page of the new project dialog has selected the correct version of SharePoint your project is targeting. For existing projects, you can change the version of SharePoint the project is targeting, by doing the following:
   * Access Project Properties, either from the Context Menu in Solution Explorer or via the Project Menu.  
   * On the SharePoint Tab, set the Target SharePoint Version to the correct version of SharePoint your project is targeting. 

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
should be able to edit these files normally by opening them manually. For now, we recommend that you use
individually linked files in place of external globbing patterns.

#### VS Test Professional 2017 SKU does not have Team Explorer, limiting access to Excel-based/SSRS-based reports from TFS Warehouse/Cube
* #### Issue is now fixed in version 15.1 (26403.00):

    Installing the VS Test Professional SKU no longer installs VS Team Explorer, which is used to access to Excel-based/SSRS-based based reports from TFS Warehouse/Cube. There is no impact to the Microsoft Test Manager (MTM) client – it continues to work without any known issues.

#### NavigateTo search in folder mode does not return external items for Visual C++ projects.
* #### Issue: 
When you open a folder with a VC project, NavigateTo search does not return external files.

* #### Workaround: 
Open the folder with Lightweight Solution Load on, close the solution, and reopen the folder. 

#### Globs with forward slashes (ie: "**/*.cs") are not supported in CPS based projects (.NET Core and Cordova).
* #### Issue: 
Globs with forward slashes are not supported in CPS projects and will cause a non-fatal error. 

* #### Workaround: 
No workaround at this time. 

#### Cannot create team projects or update process templates
* #### Issue:
Customers cannot create new team projects or upload or edit process templates from Visual Studio 2017 version 15.3. Project creation from web access continues to work.

* #### Workaround:
At this time, please use the released Visual Studio 2017 version 15.2 or earlier, if you need to create team projects or upload process templates from Visual Studio.

#### Error when opening folder if C\# and Visual Basic Component is not installed
* #### Issue:
Error message "Exception thrown by the target of an invocation” when opening folder if C# and Visual Basic Component is not installed.

* #### Workaround:
Install the C# and Visual Basic Component.

#### Microsoft Test Manager (MTM) client cannot connect to Team Foundation Server or Visual Studio Team Services
* #### Issue:
MTM client cannot connect to Team Foundation Server or Visual Studio Team Services, blocking users from creating and running tests cases. 

* #### Workaround
At this time, please use the following workaround:

Find the folder in which mtm.exe is installed by searching for mtm.exe in the start menu and choosing 'Open file location' in the right click menu. Edit the 'mtm.exe.config' file present in the same folder to add the following section in configuration -> runtime section:

      <dependentAssembly>
        <assemblyIdentity name="Microsoft.VisualStudio.Threading" publicKeyToken="b03f5f7f11d50a3a" culture="neutral"/>
        <bindingRedirect oldVersion="10.0.0.0-15.0.0.0" newVersion="15.3.0.0"/>
      </dependentAssembly>

#### Building a DSL project fails with FileNotFoundException

* #### Issue:
Building a newly created DSL project fails with FileNotFoundException.

* #### Workaround:
Add the following snippet to assemblyBinding element in MSBuild.exe.config (in <VSInstallPath>\MSBuild\15.0\Bin):

```xml
    <dependentAssembly>
      <assemblyIdentity name="Microsoft.VisualStudio.Zip.9.0" culture="neutral" publicKeyToken="b03f5f7f11d50a3a" />
      <codeBase version="9.0.0.0" href="..\..\..\Common7\IDE\PrivateAssemblies\Microsoft.VisualStudio.Zip.9.0.dll" />
    </dependentAssembly>

```



<center>[Top of Page](#top)</center>