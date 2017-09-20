---
title: Team Foundation Server 2017 Update 3 Release Notes
description: Team Foundation Server 2017 Update 3 Release Notes
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 08/24/2017
ms.topic: release-article
ms.prod: visual-studio-tfs-dev15
ms.service: visualstudio
ms.assetid: e6c93e9e-20d1-4175-b8d2-fa85392e8820
---

# Team Foundation Server 2017 Update 3 RC Release Notes

In this article, you will find information regarding the newest release for Team Foundation Server 2017 Update 3. Click the button to download.

<a href="https://go.microsoft.com/fwlink/?LinkId=857134"><img src="media/tfs_download_button.png"alt="Download the latest version of Team Foundation Server"></a>

For other formats or languages, please see the [download site](https://www.visualstudio.com/downloads/#tfs2017-u3).

To learn more about Team Foundation Server 2017, see the [Team Foundation Server Requirements and Compatibility](https://go.microsoft.com/fwlink/?LinkId=809018 "Team Foundation Server Requirements and Compatibility") page.

***

## Feedback

We’d love to hear from you! You can report a problem and track it through [Developer Community](https://developercommunity.visualstudio.com/spaces/22/index.html) and get advice on [Stack Overflow](https://stackoverflow.com/questions/tagged/tfs). As always, if you have ideas on things you’d like to see us prioritize, head over to [UserVoice](https://visualstudio.uservoice.com/forums/330519-team-services) to add your idea or vote for an existing one.

***

## Release Date: September 19, 2017

## What's New in this Release

This is an update for Team Foundation Server 2017 that includes bug fixes since Team Foundation Server 2017 Update 2.

* [Work Bug Fixes](#work-bug-fixes)
* [Code Bug Fixes](#code-bug-fixes)
* [Build Bug Fixes](#build-bug-fixes)
* [Release Bug Fixes](#release-bug-fixes)
* [Test Bug Fixes](#test-bug-fixes)
* [Reporting Bug Fixes](#reporting-bug-fixes)
* [Known Issues](#known-issues)

***

## Work Bug Fixes

* Exporting a template with ASCII character code >127 does not have WebLayout and includes incorrect file names.
* Board and Card Settings does not handle Work Item Type rename.
* Kanban board card reordering in Turkish should be by stack rank.
* REST API WorkItemSearchConditionalFaultIn should throw NotSupportedException for Search.

## Code Bug Fixes

* [Maven: Code coverage not generated](https://github.com/Microsoft/vsts-tasks/pull/4744).
* HTML files should not default to Preview mode in the new explorer.
* [No scrollbar when viewing changesets](https://developercommunity.visualstudio.com/content/problem/69379/no-scrollbar-when-viewing-changesets.html).
* [Scrolling vertically in web (both Code->Changesets as Files) isn't working anymore in IE 11/Chrome](https://developercommunity.visualstudio.com/content/problem/73502/scrolling-vertically-in-webacces-both-code-changes.html).
* [Scrolling no longer works in Source Explorer (IE/Edge)](https://developercommunity.visualstudio.com/content/problem/74736/scrolling-no-longer-works-in-source-explorer-ieedg.html).
* [Filtering Changesets by a user who has left the project does not work](https://developercommunity.visualstudio.com/content/problem/79367/filtering-changesets-by-a-user-who-has-left-the-pr.html).
* Select a file and then select back to root directory in left tree in full screen mode, it will automatically exit full screen mode.
* Search URL length exceeded the default supported limit and started an throwing exception if large number of repositories.
* Files/Folders should not be configured when there is no default branch in the Git repository.
* Extension install conflicts with the jobs of previous extension uninstall operation.
* Search not working due to job failures.
* ReindexingStatus remains in Inprogress state if Accountfaultin job is run more than once.
* TFVC Crawl failure due to VC permission issues.
* Search failing post upgrade to TFS 2017 Update 2 in ja-jp build.
* Search failing post upgrade to TFS 2017 Update 2 from Update1 though WIS works.
* Job Result Message needs to give more insights into the indexing.
* Patch Operation failure count is high.
* TimeBoxed Crawler should at least crawl one batch irrespective of job execution time limit.

## Build Bug Fixes

* Error while attempting to register build agent: Authentication - "Insufficient stack to continue executing the program safely."

## Release Bug Fixes

* Upgrade from TFS 2017 failing migration of Azure-based connected service to service endpoint.

## Test Bug Fixes

* Deploy Test Agent task has multiple issues on Win7-SP1 machine.
* If Test Agent path is wrong it is not logged as error but appears only in debug.
* Test run/task shouldn’t fail if we failed to upload attachment.

## Reporting Bug Fixes

* RDL Burndown Reports shows hours for deleted tasks.

## Known Issues

### TFS Database Import Service does not support RC releases

The TFS Database Import Service for Visual Studio Team Services doesn’t support imports from RC releases of TFS. If you’re planning on importing your collection database to Team Services using this service, it’s important that you don’t upgrade your production database to this RC release. If you do upgrade, then you will need to wait and upgrade to the RTW version of this release or restore a backup copy of your database from a previous TFS version to import.

***

<center>[Top of Page](#top)</center>