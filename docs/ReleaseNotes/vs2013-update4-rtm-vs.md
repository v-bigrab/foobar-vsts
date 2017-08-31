---
ms.TocTitle: November 12
Title: Visual Studio 2013 Update 4 (2013.4) RTM
Description: Get the release notes for Visual Studio 2013 Update 4 (2013.4) RTM to learn what's new in this release
ms.ContentId: 7f237f48-c91c-44f7-965c-f2466eb90537
ms.author: reshmim
---

# <a id="top"> </a>Visual Studio 2013 Update 4 (2013.4) RTM

### November 12, 2014

Today, we are happy to announce the availability of Visual Studio 2013 and Team Foundation Server 2013 Update 4 Release to Manufacturing (RTM).

**Download Visual Studio 2013 Update 4**

This update is the latest in a cumulative series of feature additions and bug fixes for Visual Studio 2013. You can download Visual Studio 2013 and Team Foundation Server 2013 from 
[My.VisualStudio.com](https://www.visualstudio.com/vs/older-downloads/). My.VisualStudio.com requires a free [Dev Essentials](https://www.visualstudio.com/dev-essentials/) subscription, or a [Visual Studio Subscription](https://www.visualstudio.com/subscriptions/).


### What's new in Visual Studio 2013 Update 4

Visual Studio updates:

- [CodeLens](#CodeLens)
- [C++ Diagnostics](#C++)
- [JavaScript IntelliSense](#JS)
- [Microsoft ASP.NET and Web Tools](#AzureWeb)
- [Application Insights](#ApplicationInsights)
- [Developer License Renewal](#DevLicense)

Team Foundation Server updates:

- [Release Management](#ReleaseManagement)
- [Test](#Testing)
- [Version control](#VersionControl)
- [Plan and track work](#WIT)
- [Access level name changes and feature access](#Licensing)

Microsoft SQL Server Database Tooling updates:

- [Updates](#SQL)

Other changes:

-[Bug Fixes & Known Issues](#Other)

In addition, several Visual Studio 2013 products are available for download with Update 4, including the following:

- [Azure SDK for .NET 2.5](#AzureSDK)
- [Team Explorer Everywhere 2013 Update 2](#TEE)
- [Visual Studio Tools for Unity (VSTU) 2.0 Preview](#VSTU)
- [Kinect for Windows 2.0 SDK RTW](#Kinect)
- [Visual Studio Tools for Apache Cordova CTP3](#Cordova)
- [Office Developer Tools for Visual Studio 2013](#Office)
- [TypeScript 1.3](#TypeScript)
- [Visual Studio Community 2013](#Community)

To get more details on these releases, go to the [Related Releases](#Related) section below.

Watch the [Visual Studio 2013 Update 4 episode of Visual Studio Toolbox](http://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-2013-Update-4) to learn about new features in this release:

![Visual Studio Toolbox: Visual Studio 2013 Update 4](media/11_12_01.png)

## <a id="CodeLens"> </a> CodeLens

With CodeLens indicators you can learn about your code while staying focused on your work. You can find code references, changes to your code, related TFS items, and unit tests – all without looking away from the code. [Learn more about CodeLens](https://msdn.microsoft.com/library/dn269218.aspx).

### Reduced data storage requirements for CodeLens with TFVC

The size of CodeLens data stored in the TFS database has been reduced. The data has been reformatted and duplicated information removed.

By default, CodeLens now only processes changes from the last 12 months to calculate team indicators. You can change this duration by using the [TFSConfig CodeIndex command](https://msdn.microsoft.com/library/dn280925.aspx).

## <a id="C++"> </a> C++ Diagnostics

### GPU Usage

A new **GPU Usage** tool in the **Performance and Diagnostics** hub helps you determine whether the CPU or the GPU is the performance bottleneck. This tool lets you collect and analyze GPU usage data for DirectX applications.

![Performance and Diagnostics hub; GPU Usage tool](media/11_12_02.png)  

You can use this tool for both Windows Desktop and Windows Store apps; support for Windows Phone and remote diagnostics will ship in a later release. You can also inspect the timing of each individual GPU event if a supported graphics card is present and latest drivers are installed. 

### Faster browsing

Visual Studio now scans or rescans large solutions and updates the symbol database more quickly. Browsing should be more responsive, and operations such as **Go To Definition** should not be blocked, even if the database has not been completely updated. A non-blocking message will warn you that your results may be inaccurate.

## <a id="JS"> </a> JavaScript IntelliSense

You can now get IntelliSense in JavaScript modules loaded with RequireJS. Learn more about [RequireJS](http://www.requirejs.org/).

## <a id="AzureWeb"> </a> Microsoft ASP.NET and Web Tools

We have made improvements in the JSON and HTML editors.

### JSON Editor Improvements

We made a few improvements in the JSON editor, including loading the JSON schema asynchronously, caching child schemas, and improving IntelliSense.  We also have the following new features:

- JSON Schema validation. We added a JSON schema validation feature, based on the schema selected in the drop-down list.
- Un-minify the context menu button. You can right-click the JSON editor and select **Un-minify context menu button** to un-minify any long arrays in the JSON file.
- The Reload Schemas context menu button. Visual Studio caches the schema downloaded from internet, and will use the cache even after you restart Visual Studio. If you know the schema has changed, you can use the context menu to download the changed schema in the active JSON document and use it immediately.

### HTML Editor Improvements

We improved the HTML editor with some bug fixes, updated IntelliSense for web standards, and introduced the following new features:

- Better client template formatting. The HTML editor no longer parses or formats double-curly syntax {{…}}, so we don’t flag the content as invalid HTML or try to format it as HTML. This is great for Angular, Handlebars, Mustache and other double-curly template syntaxes.
- Support for custom elements, polymer-elements and attributes.   
We no longer validate unknown attributes for custom elements, because there can be many custom-made tags in different frameworks. There will no longer be squiggles under the unknown elements.
- HTML element tooltips. We now supply tooltips for HTML elements in the editor.
- #region support. The HTML editor now supports region folding. You can use a surrounding snippet to surround the current selection as well.
- viewport fix for the LESS editor. In the LESS editor, @viewport no longer shows verification warnings.
- Many more snippets. We now provide more snippets to make your developing experience easier.
- CSS auto-sync. Saving the CSS file or changing it externally (for example, with a LESS/SASS compiler) causes the whole CSS file to reload in the browser. If the file couldn’t auto-sync, Ctrl+S causes an automatic reload without needing to refresh the linked browsers(Ctrl+Alt+Enter). This feature can be disabled in the toolbar.

### Azure WebJobs

In Visual Studio 2013 Update 4 we’re releasing some new features that will make it easier than ever to build, deploy, and debug Azure WebJobs, and to add background processing to Azure Websites. WebJobs are now represented as nodes in the Visual Studio Server Explorer, so you can link directly to the WebJobs dashboards to see how your WebJobs are running. You can also use the Server Explorer to start and stop continuous jobs and run on-demand or scheduled jobs. We’ve also enabled one-click remote debugging of continuous WebJobs, so if you need to see how your continuous WebJob is processing incoming queues or blob messages, you can step through your code as it’s running live in the cloud.

![Server Explorer WebJobs node](media/11_12_03.png)

### WebJobs SDK

The WebJobs SDK is pre-installed in the Azure WebJob project templates. As before, you can create a new WebJob project using the Azure WebJob project template.

### ASP.NET MVC 5.2.2

Template packages are updated to use ASP.NET MVC 5.2.2. This release doesn’t have any new features or bug fixes in MVC. We made a change in Web Pages for a significant performance improvement, and have updated all other dependent packages we own to depend on this new version of Web Pages.

### ASP.NET Web API 5.2.2

In this release we have made a dependency change for Json.Net 6.0.4. Get more details about [what's new in this release of Json.NET 6.0 Release 4](http://james.newtonking.com/archive/2014/08/04/json-net-6-0-release-4-json-merge-dependency-injection). This release doesn’t have any other new features or bug fixes in Web API. We have subsequently updated all other dependent packages we own to depend on this new version of Web API.

### ASP.NET Web API OData 5.3.1 beta

See [what's New in ASP.NET Web API OData 5.3](http://www.asp.net/web-api/overview/releases/whats-new-in-aspnet-web-api-odata-53#OD).

### SignalR 2.1.2

Template packages are updated to use SignalR 2.1.2. See [SignalR 2.1.2](https://github.com/SignalR/SignalR/releases/tag/2.1.2).

### Microsoft Owin 3.0 package

Template packages are updated to use Microsoft Owin 3.0 NuGet packages. See this [Katana 3.0 release note](https://katanaproject.codeplex.com/releases/view/113283).

## <a id="ApplicationInsights"> </a> Application Insights

With Update 4, Application Insights Tools for Visual Studio has more performance improvements and bug fixes. It is fully compatible with projects that had Application Insights added with Visual Studio 2013.3. This update includes:

- Seamless integration with the workflow to publish to an Azure website
- Improved solution integration and project detection. (For example, Application Insights is no longer included in unsupported projects like Python.)

To learn more about changes to Application Insights data in the Azure Preview Portal, go [here](http://azure.microsoft.com/documentation/articles/app-insights-start-monitoring-app-health-usage/#add).

## <a id="DevLicense"> </a> Developer License Renewal

When your developer license is within 15 days of expiring, you will start to see a new notification in the notification hub. Click the notification when you’re ready to renew your license, and then click **I Agree** on the renewal window. You must have an internet connection to renew your license. After your license expires, you won’t be able to debug or deploy your Windows Store apps, or open the XAML or HTML designers.

## <a id="ReleaseManagement"> </a> Release Management

Improve the process of managing the release of your app. Deploy your app to a specific environment for each separate stage. Manage the steps in the process with approvals for each step. 

You can create release templates that use deployment agents to deploy your app, or you can create release templates that use [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx), Windows PowerShell Desired State Configuration ([DSC](https://technet.microsoft.com/library/dn249912.aspx)), or [Chef](http://www.getchef.com/). To help you know which type of release you are setting up, terms have been added to the UI to make your choices clearer: agent-based or vNext (without agents). This simply helps you identify that you are using the correct environments and components for your release templates and release paths.

### Use the Release Management service for Visual Studio Team Services

Now you can setup a release pipeline from check-in through to deployment without having to install and maintain an on-premises Release Management server. Use the Release Management service for Visual Studio Team Services to set up your release. (This service is in preview.)

From your Release Management client, connect to your Visual Studio Team Services account. Create a release definition for your app from the RM client. When you release your app to each stage, the Release Management service is used.

![Administration tab; Settings tab](media/11_12_04.png)

### Release to Azure from Visual Studio

You can now create a release definition directly from within the Visual Studio IDE using Release Management as a service with a Visual Studio Team Services account. You must use an Azure subscription to deploy to your Azure VMs with this release definition. Learn more about this [here](https://www.visualstudio.com/get-started/deploy-to-azure-vs).

![From Visual Studio, create a release definition](media/11_12_05.png)

### Use tags when you deploy to an environment

Now you can use tags with the servers in your Azure or standard environments when you deploy without agents. For example, if you have multiple web servers in your environment then you can tag them all with WebServer. Set up your deployment actions for your tags. When a stage is deployed, these actions are performed on any server with this tag. So you only have to create the set of actions once for multiple servers.

With tags you can also switch the deployment order from parallel to sequence.

### Access to system variables for your deployment sequences or scripts

By popular user demand, you can now access system variables just like other configuration variables and use them in your release template if you deploy without agents. You don't have to hardcode these any more.

Supported variables:

- Build directory
- Build number (for component in the release)
- Build definition (for component)
- TFS URL (for component)
- Team project (for component)
- Tag (for server which is running the action)
- Application path (destination path where component is copied)
- Environment (for stage)
- Stage
- Release id
- Release name

### Reduce the need for configuration files to deploy your builds

If you deploy without using agents, you can now set up configuration variables for your release at the following levels: global, server, component, action. This extra flexibility means you might no longer need to maintain configuration files with your build. If variables have the same name, the value is determined based on this order of precedence: action, component, server, global. (Action has the highest precedence to override the other values).

### Manual intervention for a release path

Now you can add manual steps to a stage in any release path, even if you deploy without agents. Add a manual intervention activity into your deployment sequence. When the notification is triggered in that sequence, the deployment pauses and you can run some manual steps before continuing with the rest of the automation for the release path.

### Build drops stored on TFS servers 

If you have set up your build definition to copy the build output to the server and not a UNC path, you can now use these builds that are stored on the server if you deploy your app without agents.

### Deploy from a build drop using a shared UNC path

You can now use Release Management to deploy to servers using build drops located on a shared UNC path. You can deploy only if both the target server and the Release Management server have access to the shared UNC path, and you deploy your app without deployment agents.

### Usability improvements

You can now select servers and components from the drop-down list in the action for all types of release templates. You can also give actions friendly names to make it easier to identify them.

### Mix and match Azure and standard environments

Previously for a release path that deployed to servers without agents, each stage in the path could only use either all Azure environments or all standard environments. Now you can mix and match your environments. For example, your test stage might deploy to an Azure environment, but your production stage deploys to on-premises production servers using standard environments.

## <a id="Testing"> </a> Test

### Find out quickly if a test case belongs to other test suites

As test cases can belong to more than one test suite, it's good to check if there are any other associated test suites before you make changes to a test case. Now you can quickly view all the test suites associated with a test case.

![Select test case; view test details pane; select test suites](media/11_12_06.png) 

### View recent test results for a test case

Quickly see the test result history for a test case to see if it has passed or failed recently. Just select the test case, view the details pane, and choose test results. 

### Real-time lightweight charts to show testing status

Now you can create snapshot and trend charts for test cases from the Charts tab in the test hub. You can also create snapshot charts for test results. Pin these charts to your home page so that all the team can see the test status.

![Test hub; open a test suite; Charts tab](media/11_12_07.png)

[Learn more and see examples of these charts.](https://msdn.microsoft.com/library/dn282443.aspx)

### Filter by tags in the test hub

Tag test cases in a suite with any tag that is important to you. For example, tag all the tests related to login so that you can rerun these tests if a bug is fixed for the login page. Then you can filter on that tag from the test hub. You can add and edit tags when you edit a test case, or bulk edit tags in the grid view.

![Choose a test suite; add Tags to the column list; click the filter icon to show tags](media/11_12_08.png)

## <a id="VersionControl"> </a> Version control

### Review and merge code with Git pull requests

Pull requests are a critical component of the developer workflow in Git. Now developers can use pull requests to help review and merge their code. Pull requests enable developers working in branches to get feedback on their changes from other developers before adding their code into the mainline. Any developer participating in the review can see the code changes, leave comments in the code, and give a “thumbs up” approval.

## <a id="WIT"> </a> Plan and track work

The many small improvements to Team Foundation Server (TFS) with Update 4 help make it easier for you to use our tools to get your work done faster.

### Visualize trends and aggregate field values

Query-based chart authoring now includes trend charts: Stacked Area, Area, and Line. You can visualize trends across a one-week, two-week, or four-week time range. Also, in addition to field counts, you can now sum a field value across work items returned in a flat-list query. These new chart types can be pinned to your home pages too. Learn more about how to [view the status of your progress](https://www.visualstudio.com/get-started/visualize-progress-vs).

### Quickly reorder backlog items

If you had a large backlog, it was hard to drag and drop items to a different position. The context menu for backlog items now contains options to move an item directly to the top or to a specific position in the backlog. Be aware that with this change, we removed the field that tracks backlog priority from the work item forms in the default TFS process templates.

### Full screen mode support for backlog views, boards, queries

If you’re running a daily standup or viewing large backlogs, it's useful to be able to maximize the screen space and see as many items at once. Now you can hide all the chrome in the UI and have full-screen views of the backlog and boards. The toggle to enter full screen mode works for all the pages under the Backlogs and Queries tabs in the Work hub. Press ESC to return to the full work item view.

### Full screen mode support for all HTML/rich-text fields

You can now enter full screen mode for rich-text fields to help improve the readability and usability. For example, the **Steps to Reproduce** field can be maximized as shown below. The button toggles the text area between full screen mode and the work item view. Press ESC to return to the full work item view.

![Maximize button to expand the steps to reproduce text area](media/11_12_09.png)

### Better triage experience

To improve the triage experience when you review query results, you can go back to the query by pressing Alt+Q. This keeps your position in the query.

### Assign backlog items to iterations within hierarchical views

From hierarchical views, you can now assign product backlog items to iterations with drag and drop.

### In-line search for area and iteration fields from the work item form

Often when triaging or assigning work items it’s necessary to change the area and/or the iteration path. Finding the path you want in large, deeply nested trees can be difficult. With inline search, values that match what you type are instantly highlighted. For example, type Team to highlight all path entries that contain the work Team in their name.

![Area path search made easier](media/11_12_10.png)

### Open hyperlinks quickly

If you have a hyperlinks defined within an HTML field, press the CTRL key and click the link. Previously it was a two step process to click the link, and then click the “navigate to…” command at the top of the text area.

### Teams choose whether or not to track bugs on their backlog

Teams now have greater flexibility in how they track bugs. While team projects created with the Scrum process template include bug tracking on the backlog, other process templates don't. Each team can now choose to view the bugs with the product backlog or turn off including them.

![Uncheck to remove bugs from the backlog and Kanban board](media/11_12_11.png)

More details about adding bugs to the task board are [here](https://msdn.microsoft.com/library/jj920163.aspx).

### Work item form enhancements

Track work and share information more easily using some of the new features listed below and highlighted in the work item form pictured.

- Send a nicely formatted email directly from the work item form using the new email icon.
- Return directly to the query result you navigated from. If you like to use the keyboard, press ALT+Q. Or you can use the browser back button to do the same thing. This keeps your position in the query.
- Enter full screen mode from all queries and all work items. Just click the command in the toolbar to remove all the chrome and maximize your screen real estate.
- Open a work item in a new browser tab with the context menu command for query results.
- Copy and paste of query results now formats the results much better for pasting into email or a document.

### More items in your Kanban board

There is no longer a hard limit on the number of items in the first and last columns of the Kanban board. Now you can configure this limit to have up to 999 items.

### Easier way to link work items

In Visual Studio, there has always been a dialog box to find a work item that you want to link to, but with Team Web Access you could only type the work item ID to find it. With Update 4, you get a similar dialog box to find the work item you want to link to. You can run an existing query or find the work item based by searching for its title.

## <a id="Licensing"> </a> Access level name changes and feature access

With Update 4, all access levels have been renamed. The new names correspond to the same names used for Visual Studio Team Services licensing.

- Stakeholder (previously was Limited)
- Basic (previously was Standard)
- Advanced (previously was Full)

With this change, the feature set support for the Stakeholder access has been enhanced. Stakeholders have access to the project home page and most of the “work” related functionality. This includes the ability to view the backlog, add and edit items, run work item queries and more.

Any number of users can be assigned a stakeholder license at no charge. See more details [here](https://msdn.microsoft.com/library/jj159364.aspx).

## <a id="SQL"> </a> Microsoft SQL Server Database Tooling for Visual Studio

These are the added features for Update 4:

- SQL Server 2014 is now supported.
- Schema compare supports MSBuild with text and XML output.
- Token-based authentication for Azure SQL Database node in Server Explorer is supported -for Microsoft accounts and organizational accounts.
- From the Azure Preview Portal for Microsoft Azure SQL databases, you can now open the database schema directly in Visual Studio.
- Extensibility for Static Code Analysis.
- Filtering for the editable data grid.
- Save your data compare settings to a file (.dcmp).
- Additional actions are available when you connect to the TSQL editor.
- PDW tools are now part of Visual Studio Express 2013 for Windows Desktop

## <a id="Other"> </a> Other Changes: Bug Fixes & Known Issues

For a complete description of technology improvements, bug fixes and known issues in this release see the [KB article for Visual Studio 2013 Update 4](http://go.microsoft.com/fwlink/?LinkId=510328).

## <a id="Related"> </a> Related Releases

### <a id="AzureSDK"> </a> Azure SDK 2.5

This release provides new and enhanced tooling for Azure development with Visual Studio 2013 Update 4 and now Visual Studio 2015 Preview, including Azure Resource Manager Tools, HDInsight Tools, and the ability to manage Azure WebJobs from Server Explorer. Learn more about this release from the[Azure SDK 2.5 release notes](http://go.microsoft.com/fwlink/?LinkID=517988).

Download [Azure SDK 2.5](http://azure.microsoft.com/downloads/archive-net-downloads/) now.

### <a id="TEE"> </a> Team Explorer Everywhere 2013 Update 2

TEE 2013 Update 2 improves how TEE stores credentials which makes signing in to [Visual Studio Team Services](https://www.visualstudio.com/products/visual-studio-team-services-vs) much easier. This release also adds the capability to browse Git repositories within TEE. Read more about this [here](http://blogs.msdn.com/b/visualstudioalm/archive/2014/09/22/team-explorer-everywhere-2013-update-2-is-here.aspx).

Download [TEE 2013 Update 2](http://go.microsoft.com/fwlink/?LinkId=321339) now.

### <a id="VSTU"> </a> Visual Studio Tools for Unity (VSTU) 2.0 Preview

VSTU is Microsoft’s free Visual Studio add-on that enables a rich programming and debugging experience for working with the [Unity gaming tools and platform](http://unity3d.com/). VSTU 2.0 Preview adds support for Visual Studio 2015 Preview. Better visualization for objects in watch and local windows has been added too.

**Recent releases**

2.0 VSTU -find out more about this release [here](http://unityvs.com/news/).

1.9.1 VSTU - find out the details of the new features and bug fixes from [this blog post](http://blogs.msdn.com/b/visualstudio/archive/2014/07/29/visual-studio-tools-for-unity-1-9.aspx).

1.9.2 VSTU - the minor features and bug fixes are listed here in [this change log](http://unityvs.com/documentation/changelog/#1.9.2).

To get started with the latest version of VSTU, download the tools from the Visual Studio Gallery: [VSTU for Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/20b80b8c-659b-45ef-96c1-437828fe7cf2), [VSTU for Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/7ab11d2a-f413-4ed6-b3de-ff1d05157714), and [VSTU for Visual Studio 2010](http://visualstudiogallery.msdn.microsoft.com/6e536faa-ce73-494a-a746-6a14753015f1).

### <a id="Kinect"> </a> Kinect for Windows 2.0 SDK RTW

Here are the details for this release:

- Kinect for Windows software development kit 2.0 features over 200 improvements and updates to the preview version of the SDK. The SDK is a free download, and there are no fees for runtime licenses of commercial applications developed with the SDK.
- Ability to develop Kinect apps for the Windows Store. With commercial availability of SDK 2.0, you can develop and deploy Kinect v2 apps in the Windows Store for the first time. Access to the Windows Store enables you to reach millions of potential customers for your business and consumer solutions.
- Availability of the US$49.99 Kinect Adapter for Windows that enables you to connect a Kinect for Xbox One sensor to Windows 8.0 and 8.1 PCs and tablets. Now developers can use their existing Kinect for Xbox One sensor to create Kinect v2 solutions, and consumers can experience Kinect v2 apps on their computer by using the Kinect for Xbox One sensor they already own. The adapter is available in over two dozen markets—rolling out later today—and will be available in a total of 41 markets in the coming weeks.

For more details, go [here](http://blogs.msdn.com/b/kinectforwindows/archive/2014/10/22/big-day-for-kinect-developers.aspx).

Download the [Kinect for Windows software development kit](http://go.microsoft.com/fwlink/?LinkId=403899) now.

### <a id="Cordova"> </a> Visual Studio Tools for Apache Cordova CTP3

Formerly known as Multi-Device Hybrid Aps for Visual Studio, Visual Studio Tools for Apache Cordova makes it easy to build, debug, and test cross-platform apps that target Android, iOS, Windows, and Windows Phone from one simple Visual Studio project. Learn more [here](http://go.microsoft.com/fwlink/?LinkID=518457).

CTP3 includes the following improvements over CTP2:

- Update on save for Ripple – No need to rebuild!
- The ability to debug an iOS version of your app right from Visual Studio when deployed to the iOS Simulator or a connected device on a Mac
- Improved security and simplified configuration for the included remote iOS build agent
- An improved plugin management experience that includes support for adding in custom plugin to your project from Git or the filesystem
- Support for Apache Cordova 4.0.0

Download the latest update of [Visual Studio Tools for Apache Cordova](http://go.microsoft.com/fwlink/?LinkId=397606) now.

### <a id="Office"> </a> Office Developer Tools for Visual Studio 2013 – November 2014 Update

This release includes the new Office 365 API Tools, which make it easy to develop apps that connect to Office 365 APIs. Simply choose the Add-&gt;Connected Service item on the project context menu and the dialog will guide you through the process of creating the app entry in Azure Active Directory and adding the appropriate references and configuration in your solution. The tool supports most project types in Visual Studio 2013, including ASP.NET MVC, ASP.NET Web Forms, WPF, Windows Forms, Universal Apps, Apache Cordova and Xamarin.

Download the latest update of [Office Developer Tools for Visual Studio 2013](http://aka.ms/OfficeDevToolsForVS2013) now.

### <a id="TypeScript"> </a> TypeScript 1.3

TypeScript 1.3, available as a separate download for Visual Studio 2013 Update 4, adds protected member access and tuple types, allowing for more natural object-oriented patterns and more precise array types.

Learn more and download  [here](http://blogs.msdn.com/b/typescript/archive/2014/11/12/announcing-typescript-1-3.aspx).

### <a id="Community"> </a> Visual Studio Community 2013

Visual Studio Community 2013 is a new edition that enables you to unleash the full power of Visual Studio to develop cross-platform solutions. Create apps in one unified IDE. Get Visual Studio extensions that incorporate new languages, features, and development tools into this IDE. (These extensions are available from the Visual Studio Gallery.) Learn more about [Visual Studio Community 2013](https://www.visualstudio.com/products/visual-studio-community-vs).

Download [Visual Studio Community 2013](http://go.microsoft.com/fwlink/?LinkId=510314) now.

[Top of Page](#top)