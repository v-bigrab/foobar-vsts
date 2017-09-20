---
title: Team Foundation Server 2015 Update 3 Release Notes
description: Team Foundation Server 2015 Update 3 Release Notes
keywords: visualstudio> [!IMPORTANT]
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: vs-devops-alm
ms.technology: vs-devops-articles
ms.assetid: 2f2e5375-4c56-4286-944c-7a28aa1ad3ec
---


# Team Foundation Server 2015 Update 3

### Release Date: June 27, 2016

Today, we are happy to announce the availability of the Visual Studio Team Foundation Server 2015 Update 3. This is the newest version of Team Foundation Server (TFS), the collaboration platform at the core of Microsoft's application lifecycle management (ALM) solution. If these were not the release notes you were expecting, you have reached the release notes for the most current version.

Send us your feedback using the [Feedback](https://msdn.microsoft.com/en-US/library/mt632287.aspx) option in Visual Studio. You may also submit suggestions on the [Visual Studio 2015 UserVoice site](https://visualstudio.uservoice.com/forums/121579-visual-studio).

#### Download: [Team Foundation Server Update 3](https://go.microsoft.com/fwlink/?LinkId=615439)

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/downloads/download-visual-studio-vs) page.

## What's New ?
* [SSH Support for Git repos](#ssh-support)
* [Dashboard Widget SDK](#dashboard-sdk)
* [Testing - New features & Bug Fixes](#testing)
* [Agile Bug Fixes](#agile)
* [Build Bug Fixes](#build)
* [Version Control Bug Fixes](#version-control)
* [Administration Bug Fixes](#admin)
* [Extensibility Bug Fixes](#extensibility)
* [Release Management](#release-management)

##Other Changes
* [Known Issues](#knownissues)

### <a id="ssh-support"> </a> SSH Support for Git Repos

With TFS 2015 Update 3, you can now connect to any Team Foundation Server Git repo using an SSH key. This is very helpful if you develop on Linux or Mac. Just upload your personal SSH key and you're ready to go.

### <a id="dashboard-sdk"> </a> Dashboard Widget SDK
In Update 3, not only can you use the out-of-the box dashboard widgets, you can also create your own widgets by using the SDK. For more information, see the [Add a dashboard widget](https://www.visualstudio.com/integrate/extensions/develop/add-dashboard-widget) page on VisualStudio.com.

### <a id="testing"> </a> Testing - New Features & Bug Fixes 

#### Testing - New Features - Support for Azure, SCVMM and VMWare

You can now dynamically set up test machines in the cloud with Azure, or on-premises using SCVMM or VMWare and use these machines to run tests in a distributed manner. 
You can use one of the machine provisioning tasks - [Azure](https://github.com/Microsoft/vso-agent-tasks/tree/master/Tasks/DeployAzureResourceGroup), [SCVMM](https://marketplace.visualstudio.com/items?itemName=ms-vscs-rm.scvmmapp) or [VMWare](https://marketplace.visualstudio.com/items?itemName=ms-vscs-rm.vmwareapp) followed by the [Run Functional Tests task](https://www.visualstudio.com/en-us/docs/build/steps/test/run-functional-tests) to run tests. For more information, please see the [Install and configure test agents](http://go.microsoft.com/fwlink/?LinkId=799813)  page.

#### Testing - Bug Fixes
Bugs reported through Connect:
-	Test settings file is ignored when "Run in Parallel" is selected.
-	TEMP folder is not cleaned after Test Agent Deployment is completed.
-	Source filter string is required even with Test Selection set to Test Plan. User gets error "Cannot bind argument to parameter 'SourceFilter' because it is an empty string" if string is empty.
-   Email/print test artifacts feature hangs and throws JavaScript TypeError.
-   Web test runner window no longer wraps text.

Other bug fixes:
-	"DistributedTests: Exception occurred while parsing buildId" is thrown in Release.
-	Remote Test Execution gets aborted abruptly with error - Access to the path is denied.
-	Test results cannot be uploaded from Ant, Maven or Gradle tasks in Release.
-	VsTest task fails if full path of 2 DLLs are given separated by semicolon.
-	No Test results are shown in Release when results are grouped by 'Test Suite' and Environment selected is 'All.'
-	Visual Studio Test task will not upload test results if results folder is configured in runsettings file.
-   Feedback request hyperlink is incorrect in email request.
-   Query based test suites do not properly reflect the tests when assigned all the test cases in this test suite to be run by multiple testers.
-   Exception Microsoft.TeamFoundation.TestManagement.Server.InvalidStructurePathException: The structure path CEBIS FWK is not valid.
-   Error in test hub after upgrading of TFS to 2015.1.
-   MTM 2015 | 2013 - TFS 2015.2 | Analyze test runs -results , Plan tabs comes up as empty for specific users.
-   MTM Screen capture file upload retries after the failure with file not found error. 

### <a id="agile"> </a> Agile Bug Fixes
Bugs reported through Connect:
-   Setting styles in the sprint board cards may cause an error if the locale is set to French.
-   Setting styles in the sprint board cards may cause an error if the locale is set to German.
-   Unable to create a query when there is a clause with an Area Path with non-standard characters, such as an underscore or single quote.
-   The links label control does not show hyperlinks in web access.
-   Creating new team projects causes a TF30177 "Cannot insert duplicate key row in object 'dbo.Constants" error.
-   The Add Widget dialog respects the browser language over the language selected in "My Profile."
-   In the Build Chart widget, the most recent bar in the chart shows green, even if the build fails.
-   The Stakeholder banner is missing so users are not aware they are logged in as a stakeholder and do not have access to all features.
-   Readme files are not always displayed on the Team Project welcome page.
-   When setting a part of a time in work item tracking, the month and day values may get switched.

Other bug fixes:
-   A Work Item Tracking Web Page control referencing an identity field as Param with through an error when the value is empty.
-   Error when changing the name of the Query Result widget.
-   The Remaining Hours input is not big enough on the card.
-   Backlog doesn't load when the user doesn't have permissions to a parent work item.
-   Navigating to the WORK hub after changing team projects results in a TF400483 error.
-   The Dashboard Manager icon has no visual cue on focus.
-   The Add Dashboard icon in Dashboard Manager has no clear visual cue on focus.
-   The add and delete Dashboard buttons in Dashboard Manager do not work on pressing ENTER.
-   In the Query Tile and Work Item Chart widgets, when tabbing through the configuration blade, the input will get stuck on the Query Selector with an error that no query is selected.
-   When upgrading from Team Foundation 2013 Update 1 or earlier, the contents of the project homepage will not be migrated.
-   When licensed as a Stakeholder, you can't navigate between dashboards.
-   In the markdown widget, if the markdown references an image in source control, it won't display.
-   If a third party widget is in an error state, the entire dashboard fails to load.
-   If a third party widget is in an error state, adding new widgets get added as blank.
-   If a third part widget is in an error state and then removed from the dashboard, the error banner is not cleared.
-   When dashboard widgets are added and conflict with one another, such as in different browser sessions at the same time, the error is not descriptive.
-   Avatars don't load in the Pull Request widget.
-   In the Build Chart widget, the last completed status icon is incorrect when compared to the build chart.
-   When in Edit Mode of a dashboard, the error banner is covered up with the dashboard background.
-   In the Visual Studio Links widget, the "Open in Visual Studio" image is plain purple.
-   When making changes in the configure widget blade, there is no prompt about discarding changes when cancelling out.
-   If a widget has an error, the user can still save configuration changes.
-   When previewing a widget in the dashboard, it is zoomed in and blurry.
-   Tabbing in the Dashboard edit mode tabs through the widget instead of the delete and configure icons.
-   When in the Dashboard edit mode, ESC should exit out of edit mode.
-   When creating a new Work Item Chart widget in Firefox, the chart types are of varying sizes.
-   In the Work Item Chart widget, the chart options aren't displayed until a query is selected.
-   In the Sprint Overview widget, setting the iteration dates does not refresh the widget.
-   In the Sprint Burndown widget, tabbing to the graph and hitting Enter does not open the lightbox.
-   In the Conditional Query Tile, the input field for a rule allows a five digit number but only displays four digits.

### <a id="build"> </a> Build Bug Fixes
Bugs reported through Connect:
-   Unable to filter builds by tags on Firefox.
-   When setting the permissions of a user on a build, there is an error when saving.
-   If a build is scheduled to run in the late evening, it runs on the previous day.
-   Build fails with "TF14044: Access Denied: User Project Collection Build Service needs the AdminWorkspaces global permission(s).".
-   The time formatting from My Profile is not used in the Build hub.
-   Build fails with "curl was not found in the path" error when running a curl task in Build.
-   Gated build gives an error of "Shelveset not found."
-   There are formatting problems when creating a new build definition in Chrome.
-   When a XAML Build has a large number of warnings, it shows an error of "An undefined error occurred while attempting to connect to the server. Status code 0.".
-   When resizing the Reason column in the Build page, the entire icon array is shown.
-   In the Repository tab of a build definition, changing the Depth or Ignore Externals settings gets set back to the default.
-   Build fails with "Invalid solution configuration and platform.".
-   When including an npm install task, builds fail with an error that it cannot find the npm install.  
-   Error of "Invalid source label format" when editing a build definition that labels a Git repository with a build number.
-   Continuous Integration does not always trigger when using an external Git repository.
-   On upgraded project collections, gated checkins fail due it using the build account instead of service account.

Other bug fixes:
-   getBuildBadge vso-node-api fails if using a PAT without the "All Scopes" permission.
-   If a build definition name contains square brackets, the revision number is not calculated correctly.
-   When splitting a Team Project Collection, there are duplicate build service identities.
-   When entering a shelveset name when queuing a new build, you get a misleading error of "There are issues with the request or definition that will prevent the build from running:  The value specified for SourceVersion is not a valid version spec.".
-   Extensions with cross platform build tasks do not work.
-   Build fails to connect to Subversion when using SSL port 8443.
-   When using an SVN repository for a build which doesn't have mappings, the Source Version is not set.
-   Cannot queue a Team Foundation Version Control build from a source label.
  
### <a id="version-control"> </a> Version Control Bug Fixes
Note: These are bug fixes for Version Control in Team Foundation Server.  For Version Control fixes in Visual Studio, see the [Visual Studio Release Notes](https://www.visualstudio.com/news/releasenotes/vs2015-update3-vs).

Bugs reported through Connect:
-   When using Git LFS, there may be problems with functions such as cloning the repo.
-   There are hourly Git pull request event log errors of "TF53010: The following error has occurred in a Team Foundation component or extension.".

Other bug fixes:
-   Adding a Latest Version link type to a work item does not work.
-   The Team Foundation Version Control warehouse adapter fails after upgrading from Team Foundation Server 2010.
-   There is a limit of 25 commits when linking to work items during pull request creation.
-   If a repository has multiple build definitions configured, the Build Explorer may show one definition's name but link to the last build on another.
-   In Pull Requests, the identity picker is cut off on the right side.
-   Team Foundation Version Control files show that there is an encoding change even if there was no change.
-   On a Git push over SSH, there is an error "TF401030: The Git pack header is invalid.".


### <a id="admin"> </a> Administration Bug Fixes
Bugs reported through Connect:
-   When splitting a team project collection, after cloning the collection and deleting a team project in the first collection, the other collection may not show the project that was deleted in the other collection.  The direct URL will work, but the user cannot browse to the team project.

Other bug fixes:
-   When upgrading, the readiness check may fail with errors that Port 8080 is unavailable and "TF401147: The previously configured ports for the Application Tier Web Service site are currently in use.".
-   In the Admin Console, the Proxy Server URL is blank.
-   When configuring TFS, the port and vdir may incorrectly fall back to the default mappings.
-   The Admin Console may crash when loading the Collections tab.
  
### <a id="extensibility"> </a> Extensibility Bug Fixes
Bugs reported through Connect:
-   "TF400367: The request could not be performed due to a host type mismatch" error when omitting the collection in the URL when using the TFS SDKs.
-   Deleting a branch triggers a build when using Jenkins service hooks.
-   When clicking Manage Events in a team room, there is an error "Invalid Navigation Level".
-   When working with Alerts, fields may have unexpected allowed values.
-   Emails are not always received for alerts.
-   Alerts for team projects with spaces in the name include invalid links.
-   There is no link to All Alerts in the Alerts administration page.
-   In the Chinese version of TFS, there is no Slack option in service hooks.

### <a id="release-management"> </a> Release Management

We've fixed some of the reported issues in the web-based version of Release Management. Here are some of the key issues that were fixed:
-	Undefined error is shown while browsing the Release hub, when network is flaky.
-	Downloading server drop artifact creates additional file under Build artifacts directory.
-	Duplicate service endpoints are created from endpoint creation dialog.
-	Nuget Installer task fails with Release Management.
-	Auto-refresh: Pending approvals yellow bar is not displayed after starting deployment on an environment.
-	Email option in approvals is not enabled if there are multiple approvers for an environment.

We've also fixed a few reported bugs in the WPF version of Release Management.
-	When there is an api-version mismatch, releasemanagementbuild.exe should show proper error message instead of 403 error.
-	Intermittent network failures when copying files to Deployer.

### <a id="knownissues"> </a>  Known Issues
For a complete description of known issues in this release, see the following MSDN article: [Known Issues in Team Foundation Server Update 3](https://go.microsoft.com/fwlink/?LinkId=798775)