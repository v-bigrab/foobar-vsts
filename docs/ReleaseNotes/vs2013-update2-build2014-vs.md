---
ms.TocTitle: April 2
Title: Visual Studio 2013 Update 2 (Build 2014)
Description: Release notes for the April release of Visual Studio 2013 Update 2, which was an RC release for all but TFS and TFS Express.
ms.ContentId: 40269188-c808-4e7e-b5fc-b3dda1850204
ms.author: reshmim
---

# <a id="top"> </a> Visual Studio 2013 Update 2 (Build 2014)

### April 2, 2014

Today we are announcing the availability of [Team Foundation Server 2013 Update 2 RTM](https://www.visualstudio.com/news/2014-apr-2-vs#TFS2013Update2), continuing to deliver on our commitment to bring on-going value to Application Lifecycle Management (ALM) developer tools through continuous releases of new features and by resolving known issues.

In addition, we are also making available the Release Candidates (with go-live license) of [Visual Studio 2013 Update 2 RC](https://www.visualstudio.com/news/2014-apr-2-vs#VS2013Update2RC). This release includes new features for creating apps targeting Windows Phone 8.1, the ability to build universal Windows Apps targeting the Windows Runtime, TypeScript 1.0 RTM, and many other new capabilities. In addition, Release Management Update 2 RC includes a new feature that enables tagging servers for easier deployments. For more information about using Visual Studio 2013 Update 2 RC in a production environment (go-live use), see the Statement of support in the [Visual Studio Update KB Article](http://go.microsoft.com/fwlink/?LinkId=390522).

You can download Visual Studio 2013 and Team Foundation Server 2013 from [My.VisualStudio.com](https://www.visualstudio.com/vs/older-downloads/). My.VisualStudio.com requires a free [Dev Essentials](https://www.visualstudio.com/dev-essentials/) subscription, or a [Visual Studio Subscription](https://www.visualstudio.com/subscriptions/).

## Team Foundation Server 2013 Update 2 RTM

With the release of Team Foundation Server 2013 Update 2, we continue to bring new ALM features, bug fixes, and other improvements to our on-premises customers.

  **Note**  Many of these features are already available to our [Visual Studio Online subscribers](https://www.visualstudio.com/products/visual-studio-online-overview-vs)

Below is a summary of the most popular features in this release, and relevant links where you can learn more.

### CodeLens: New ‘Incoming Changes’ Indicator

The [CodeLens](https://msdn.microsoft.com/en-us/library/dn269218.aspx) feature in Visual Studio Ultimate provides developers with a heads-up display for finding information quickly without having to leave their code and offers insights from various available Indicators without losing code context.

In this release, CodeLens gains a new [Incoming Changes Indicator](http://blogs.msdn.com/b/visualstudioalm/archive/2014/03/03/new-codelens-indicator-incoming-changes.aspx) that provides insight on changes occurring in other branches to the code another developer is currently working on. This enables teams working with multiple branches a new and easy way to stay informed without having to leave their code editor window.

![Incoming Changes indicator in CodeLens](media\04_02_01.png)

### Work Item Tags: Edit from Visual Studio & Excel, use in Queries

[Work Item Tagging](https://msdn.microsoft.com/en-us/library/dn132606.aspx) is defined by a user and adds meta-data to a work item which enables a quick way to filter data without having to create queries or additional custom filters.

With this release, tagging gets even better. View and edit tags right from Visual Studio, or use them as part of a work item query for both the Contains and Does Not Contains operators (in both Visual Studio and Web Access).

![Querying work items using tags](media\04_02_02.png)

In addition, when opening work item queries in Excel (for things such as [bulk editing of items](https://msdn.microsoft.com/en-us/library/dd286627.aspx)), you can now view and manage tags right from the connected spreadsheet.

![Querying work items using tags in Excel](media\04_02_03.png)

### Cumulative Flow Diagram: Configurable Start Date

When [working with Kanban boards](https://msdn.microsoft.com/en-us/library/jj838789.aspx), Team Foundation Server is a great tool to visualize the current project state because it automatically maintains a Cumulative Flow Diagram as items are moved on the board.

In this release, we’ve added the ability in response to customer requests to set a new start date for Cumulative Flow Diagrams, which restarts the diagram’s calculations based on the new start date.

### Burndown Charts: Configurable Working Days

In Team Foundation Server Web Access, [agile teams](https://msdn.microsoft.com/en-us/library/vstudio/ee191595.aspx) are able to use burndown charts as a graphical representation of remaining work versus the time available in a sprint.

In this release, we’ve added a new team setting for configuring working days for a project team – effectively providing the ability to remove weekend days from burndown charts ([a highly requested feature](https://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/2792800-burndown-chart-should-exclude-non-work-days) on the [Visual Studio UserVoice](http://visualstudio.uservoice.com/)).

![Setting working days in burndown charts](media\04_02_04.png)

### Work Item Charting: Home Page Pinning and Color Customization

The [work item charting](https://msdn.microsoft.com/en-us/library/dn407521.aspx) feature in web access give users the ability to quickly view the status of work-in-progress by charting the results of a flat-list query. You can create several types of charts such as pie, bar, column, or stacked column – for the same query.

In this release, we’ve made charts even more useful by enabling the pinning of charts to a team or project’s home page; making it simple to keep everyone informed on the data points the team finds most valuable.

![Pin work item charts to the home page](media\04_02_05.png)

In addition, we’ve also enabled customizable work item chart series colorization via a simple to use color picker, as shown below.

![Customize colors in work item charts](media\04_02_06.png)

### Web-based Test Case Management: Exporting Artifacts and Shared Parameters

Creating, managing, and [executing manual tests from the browser](https://msdn.microsoft.com/en-us/library/dd380763.aspx) is possible using the web-based Test Case Management feature of TFS web access.

In this release, we’ve added a new feature for exporting test plans, test suites, or test cases together with their respective properties to an HTML file for various offline uses (such as sharing with others over email or easier printing).

![Export test plans, test suites, or test cases to HTML](media\04_02_07.png)

In addition, we’ve added a new feature called “Shared Parameters”, which enables sharing of Test Case Parameters by consolidating similar parameter data in a single location and referencing it across multiple test cases.

![Shared Parameters in Web-based test case management](media\04_02_08.png)

### Git Source Control: Various Improvements

No matter the size or complexity of a project, [Source Control](https://msdn.microsoft.com/en-us/library/ms181368.aspx) plays an important role in helping maintain control of changes made to source code over a period of time. With Team Foundation Server 2013, you can select from two type of source control options for your new team project: [TFVC](https://msdn.microsoft.com/en-us/library/ms181237.aspx) or [Git](https://msdn.microsoft.com/en-us/library/hh850437.aspx).

In this release, we focused on improving our Git source control implementation:

- Use the Annotate feature (aka blame) with Git
- Amend recent local commits using Visual Studio (similar to the command line: “git amend”), as long as the commits have not yet been pushed to the TFS repository
- Push to or pull from a selected remote repository in Team Explorer without having to use the command line
- Revert a commit to undo a check-in more easily
- Monitor or cancel long-running Git operations
- Use Ant or Maven on the build controller to build Java code managed in a Git repository (requires [Team Explorer Everywhere (TEE) Update 1](https://www.microsoft.com/en-us/download/details.aspx?id=40785) and TFS Build Extensions)

### Web Access: Updated Team Home Page and Improved Backlog Navigation Performance

When running Team Foundation Server (TFS) on-premises, [Team Web Access](https://msdn.microsoft.com/en-us/library/ee523998.aspx) provides a browser-based UI for use by any member of the team without their needing to install any additional software. This web interface provides access to capabilities across TFS which includes Source Code, Backlog Management, Builds, Web-based Test Case Management, and more.

In this release, we’ve revamped the Team and Project home pages with a more visually appealing design that makes better use of screen real-estate on wider screen resolutions.

![Redesigned home page for TFS web access](media\04_02_09.png)

Thanks to customer feedback, we’ve also made improvements to performance when navigating the backlog in the web interface.

### Other Changes and Bug Fixes

For a full list of changes, see the [Visual Studio Update KB Article](http://go.microsoft.com/fwlink/?LinkId=390522).

## Visual Studio 2013 Update 2 RC

With the release of Visual Studio 2013 Update 2 Release Candidate, we make available the latest developer tooling with a go-live license for our early adopters, enabling tons of great new features (see below) and the ability to target the new Windows Phone 8.1 platform.

- [Visual Studio 2013 Update 2 RC](http://go.microsoft.com/fwlink/?LinkId=390521)- for those who already have Visual Studio 2013 installed and would like to install just the latest Visual Studio 2013 Updates.
The following downloads provide a streamlined installation experience for both the Visual Studio product indicated and Visual Studio 2013 Update 2:

	- [Visual Studio Ultimate 2013 with Update 2 RC](http://go.microsoft.com/fwlink/?LinkId=331030)
	- [Visual Studio Premium 2013 with Update 2 RC](http://go.microsoft.com/fwlink/?LinkId=331032)
	- [Visual Studio Professional 2013 with Update 2 RC](http://go.microsoft.com/fwlink/?LinkId=331032)
	- [Visual Studio Express 2013 for Windows with Update 2 RC](http://go.microsoft.com/fwlink/?LinkID=386598)

- In addition, the following Visual Studio 2013 software is available with Visual Studio 2013 Update 2 RC:
	- [Release Management for Visual Studio 2013 with Update 2 RC](http://go.microsoft.com/fwlink/?LinkId=393085)
	- [Agents for Visual Studio 2013 Update 2 RC](http://go.microsoft.com/fwlink/?LinkId=393087)
	- [Remote Tools for Visual Studio 2013 Update 2 RC](http://go.microsoft.com/fwlink/?LinkId=393086)

### Windows Phone 8.1 and Universal Windows Apps

Today, the Windows team announced major updates across Windows and Windows Phone, including new developer platform capabilities in Windows Phone 8.1 and the next major step toward platform unification with universal Windows apps for a common Windows runtime across phones, tablets, and PCs.

![Universal Windows apps for a common Windows runtime](media\04_02_10.png)

What’s new for Visual Studio Developers targeting Windows Phone 8.1:

- Upgrade existing Windows Phone 8.0 apps to Windows Phone 8.1 and take advantage of the new platform capabilities
- Create new universal Windows apps that target both Windows Phone 8.1 and Windows Store 8.1 platforms using Universal Projects, enabling them to share code and UI elements, and to build on a common platform powered by Windows Runtime
- Developers have options for building using C# & .NET, HTML & JavaScript or C++ & DirectX when creating universal Windows apps

For more details, visit the [Windows Development Center](https://dev.windows.com/) and learn all about this new release.

### TypeScript 1.0 (RTM)

[TypeScript is an open-source language](http://www.typescriptlang.org/) developed by Microsoft for application-scale JavaScript projects, powered by a typed superset of JavaScript that compiles to plain JavaScript. TypeScript, combined with Visual Studio, is a first-class experience with features such as static checking, symbol-based navigation, code refactoring, and much more.

![TypeScript 1.0 (RTM) in Visual Studio](media\04_02_11.png)

In this release, we’re announcing that TypeScript has reached version 1.0 (RTM), bringing the language to the first official release after 18 months of development and much excitement from the developer community.

### Debugging, Diagnostic, and Profiling

In this release, we have new profiling tools, improvements to the debugger, .NET Managed Memory Analyzer, IntelliTrace, Performance and Diagnostics hub, and more.

Highlights include:

- Debugger
	- The Visual Studio debugger now supports [a new string visualizer for JSON encoded strings](http://blogs.msdn.com/b/visualstudioalm/archive/2014/02/06/json-debugger-visualizer-in-visual-studio-2013.aspx) that displays them as a treeview control and allows the developer to do things such as search, highlight, or copy a key/value pair
	- The .NET Managed Memory Analyzer has a new feature to [inspect values of objects and instances](http://blogs.msdn.com/b/visualstudioalm/archive/2014/02/06/net-memory-analysis-object-inspection.aspx) of captured memory dumps
	- It is now possible to debug websites within the Windows Phone 8.1 emulator
-Performance Tools & Analyzers
	- A new [CPU Usage tool](http://blogs.msdn.com/b/visualstudioalm/archive/2014/02/28/new-cpu-usage-tool-in-the-performance-and-diagnostics-hub-in-visual-studio-2013.aspx) is now available in the Performance and Diagnostics hub that can be used with WPF, Console, Windows Store 8.1, or Windows Phone 8.1 apps. This tool provides data on what functions are using the CPU and to what degree. This empowers the developer to make decisions about where to focus their effort optimizing their app code to achieve the best possible performance
	- A new [Memory Usage tool](http://blogs.msdn.com/b/visualstudioalm/archive/2014/04/03/diagnosing-memory-issues-with-the-new-memory-usage-tool-in-visual-studio.aspx) is now available in the Performance and Diagnostics hub for analyzing new universal Windows apps or any app built using the Windows runtime using C#/VB/C++ and XAML
	- It is now [possible to run more than one tool at a time](http://blogs.msdn.com/b/visualstudioalm/archive/2014/02/11/combining-tools-in-the-performance-and-diagnostics-hub-in-visual-studio-2013.aspx) in the Performance and Diagnostics hub while maintaining a common timeline so that you can save time, correlate data across tools to get better insight into performance issues, and inform performance tradeoffs
- IntelliTrace
	- IntelliTrace performance events collected by the Microsoft Monitoring Agent (MMA) have new features:
		- [Group performance events and review hot paths](http://blogs.msdn.com/b/visualstudioalm/archive/2014/02/11/ui-enhancements-for-intellitrace-with-visual-studio-2013-update-2.aspx) within performance data
		- [Jump to SQL](http://blogs.msdn.com/b/visualstudioalm/archive/2014/02/10/jump-to-sql-with-intellitrace.aspx) when ADO.NET event data is available. This allows the use of Visual Studio SQL tooling to inspect the SQL query that was captured in the IntelliTrace data
		- [Easily navigate to Actions/Controllers](http://blogs.msdn.com/b/visualstudioalm/archive/2014/02/12/intellitrace-mvc-navigation.aspx) for data collected from ASP.NET MVC web sites
	- When reviewing an IntelliTrace file collected by the Microsoft Monitoring Agent (MMA) with Exceptions data it is now easier to view parameters and to see where exceptions were thrown by [visualizing the call stack on a Code Map](http://blogs.msdn.com/b/visualstudioalm/archive/2014/03/07/enhancements-to-debugging-exceptions-with-intellitrace-in-visual-studio-2013.aspx)
- Windows Store Apps
	- [Trigger a Prefetch](http://blogs.msdn.com/b/visualstudioalm/archive/2014/02/06/triggering-prefetch-for-windows-store-apps-in-visual-studio-2013-update-2.aspx) when debugging Windows 8.1 store apps; enabling developers to manually trigger the Prefetch caching to test their program’s behavior or to validate that ContentPrefetcher is properly registered
	- Use Windows Azure Notification Hubs to send test notification messages to Windows Store or Phone apps and check the results in real-time	
- Graphics Diagnostics
	- New Graphics Profiler
		- [Graphics Frame Analysis](https://msdn.microsoft.com/en-us/library/dn642453.aspx) collects performance measurements on captured frames; in addition, it also performs a set of pre-defined experiments which provide insights into how performance would be affected when various texture techniques are applied. frame analysis also collects performance counters from hardware and works the same way on windows 8.1 and windows phone 8.1 devices. note that graphic frame analysis relies on a timestamp query which was not provided with windows phone 8.
	- Graphics Debugger Enhancements
		- With our new consecutive capture capability, you can now capture up to 30 consecutive frames with one capture.
		- [Programmatic capture](https://msdn.microsoft.com/en-us/library/hh780905.aspx) enables automatic capture that is triggered programmatically. This is useful for debugging compute shaders in programs that never call **Present**, or when a rendering problem makes it difficult to anticipate a capture in manual testing but that can be predicted programmatically by using information about the state of the app at runtime.
		- A new **Draw Calls** view has been added which displays captured events and their state in a hierarchy organized by draw calls. You can expand draw calls to display the device state that was current at the time of the draw call; and you can further expand each kind of state to display the events that set their values.
		- Graphics Debugger now fully supports debugging Windows Phone 8.1 apps in a phone emulator or a tethered phone.	
	
### Microsoft Azure and Web Development

For web developers, this release includes [new features and improvements](http://aka.ms/aspnetupdatesvs2013update2) for tooling and platform, including updates for ASP.NET MVC, Web API, and Web Pages. There are also improvements for web developers getting starting with Microsoft Azure.

Highlights:

- Code Editor improvements and two new editors (for SASS & JSON files):
	- New SASS editor with features such as colorization, variable and Mixins IntelliSense, syntax validation, goto definition, color picker, and more
	- New JSON editor with features such as syntax validation, colorization, outlining, and support for IntelliSense (through JSON schema)
	- Improvements to LESS editor with features such as Knockout IntelliSense Upgrade, New URL Picker in HTML, Razor, CSS, LESS or SASS pages, and more

- Browser Link support for HTTPS connections, Single Page Applications (SPA), and static html files
- Updated ASP.NET default project templates for the latest platform releases including ASP.NET MVC, Web API, Web Pages, SignalR, and more
- New features for Microsoft Azure developers including:
	- Improved getting started experience with Azure via a new capability that can optionally link newly created websites directly from the “File > New Project” dialog to a Windows Azure website or Virtual Machine. This enables simple publishing when needed later
	- Two new features in Server Explorer for Windows Azure Websites: a remote view feature that allows viewing/editing of live website files and the ability to view log files remotely
	- Brand new tooling support for working with [Mobile Services that leverage .NET](http://aka.ms/azuremobileservicesnet), including a new template for getting started with the new project type, as well as support for Remote Debugging

### Other Changes & Bug Fixes

For a full list of changes, see the [Visual Studio Update KB Article](http://go.microsoft.com/fwlink/?LinkId=390522).

[Top of Page](#top)