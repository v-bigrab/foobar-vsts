---
title: Team Foundation Server 2015 Update 4 Release Notes
description: Team Foundation Server 2015 Update 4 Release Notes
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 04/11/2017
ms.topic: release-article
ms.prod: visual-studio-tfs-dev14
ms.service: visualstudio
ms.assetid: 2f2e5375-4c56-4286-944c-7a28aa1ad3ec
---


# Team Foundation Server 2015 Update 4

### Release Date: April 11, 2017

Today, we are happy to announce the availability of the Visual Studio Team Foundation Server 2015 Update 4. This is an update for Team Foundation Server 2015 and includes bug fixes since Team Foundation Server 2015 Update 3. This is a go-live release and can be installed in a production environment.

Send us your feedback using the [Feedback](https://msdn.microsoft.com/en-US/library/mt632287.aspx) option in Visual Studio. You may also submit suggestions on the [Visual Studio 2015 UserVoice site](https://visualstudio.uservoice.com/forums/121579-visual-studio).

#### Download: [Team Foundation Server Update 4](https://go.microsoft.com/fwlink/?LinkId=844068)

To learn more about related downloads, see the [Downloads](https://www.visualstudio.com/downloads/download-visual-studio-vs) page.

### What's New in RTW?
These are new items that have been added since RC:
* When link between a bug and a test result gets deleted, the deletion date does not get updated in warehouse.
* Customers who do not have permissions on the default area path will get an error “Sequence contains not elements” when viewing a build's test results.
* In the MTM tool, customers get an error “Failed to initiate clone operation” when trying to clone a test plan.
* Extensions are not able to access __Test__ hub REST APIs.
* There can be performance problems when receiving notifications.
* The warehouse connection string points to the configuration database, instead of the warehouse database, after an upgrade, if the databases are on different SQL instances.

### What's New in TFS 2015 Update 4?
This includes all the fixes in Update 4:
* [Agile Bug Fixes](#agile)
* [Version Control Bug Fixes](#vc)
* [Build Bug Fixes](#build)
* [Release Management Bug Fixes](#rm)
* [Testing Bug Fixes](#test)
* [Administration Bug Fixes](#admin)
* [Marketplace Changes](#marketplace)


****

### <a id="agile"> </a> Agile Bug Fixes 
* The @Today and @Me macros do not work correctly in non-English in the Kanban board card style rules.
* The inline __add card__ experience on the Kanban board does not work correctly. For example, the Title field cannot be edited.
* If a user switches between two work items of the same type on the queries page before the HTML fields finish loading, the HTML field may become empty and the work item will become dirty.
* The Batch API, such as WorkItemStore.GetWorkItemIdsForArtifactUris(), may return incorrect results when called with many strings.
* When a customer has rules in the global workflow and tries to move them to a work item type definition, there will be an error, "TF237090: Does not exist or access is denied".
* If a TFS instance has a collection with a space in the name and has a public URL that is different from the internal URL, inline images may be missing in work items when opened by another user.
* Work item tracking warehouse sync fails with a name conflict when field names only differ by a space replacing a "." or "_" (i.e. "My Field" and "My_Field").
* Work item tracking warehouse sync fails when a work item has a link comment that contains special characters, such as 0x0B.

### <a id="vc"> </a> Version Control Bug Fixes
* Destroying a very large team project or a very large TFVC source tree will time out and rollback.
* Renaming branch objects across projects may lose the parent relationships.

### <a id="build"> </a> Build Bug Fixes 
* The first check-in after configuring a Gated Check-in trigger for a build definition fails.
* The error, "An item with the same key has already been added", is shown while loading build tasks or queuing builds.
* The Windows build agent cannot build from Subversion repositories when running on 32-bit Windows.
* Build tasks are not getting updated when the extension is updated.

### <a id="rm"> </a> Release Management Bug Fixes
* In a release environment, if the __All users in sequential order__ option is chosen and the approver order is changed, the definition is not marked dirty and cannot be saved.

### <a id="test"> </a> Testing Bug Fixes
* Users are unable to deploy a standalone test agent.
* When selecting a test plan, the source filter is null.
* When you mark a test case as paused then save and close the test runner, you cannot continue the test case when you return to the test.
* **New for RTW**: When link between a bug and a test result gets deleted, the deletion date does not get updated in the warehouse.
* **New for RTW**: Customers who do not have permissions on the default area path will get an error “Sequence contains not elements” when viewing a build's test results.
* **New for RTW**: In the MTM tool, customers get an error “Failed to initiate clone operation” when trying to clone a test plan.
* **New for RTW**: Extensions are not able to access __Test__ hub REST APIs.

### <a id="admin"> </a> Administration Bug Fixes
* The admin console (TfsMgmt) may close unexpectedly during an upgrade.
* Code reviewers in non-English versions of TFS do not get an email when added to code reviews.
* The upgrade to TFS 2015 may fail with duplicate workspace names if an orphaned user has a workspace with same name as valid user.
* **New for RTW**: There can be performance problems when receiving notifications.
* **New for RTW**: The warehouse connection string points to the configuration database, instead of the warehouse database, after an upgrade, if the databases are on different SQL instances.
* In previous releases, customers using SSL offloading needed to add the X-Forwarded-Proto header on their load balancer. With this update, they can simply configure the public URL in TFSMgmt.exe to generate https:// URLs.
* The Jenkins Service Hook was incompatible with newer versions of Jenkins because of a new authentication pattern.  With this release, newer versions of Jenkins are compatible.

### <a id="marketplace"> </a> Marketplace Bug Fixes
* Installations of MS.TFS.Server are now supported.
* Paid Preview extensions are now supported on TFS 2015 through this update. Once installed they become free forever since out-of-box Commerce integration for extensions does not exist for TFS 2015. Additionally, any flag in the extension manifest not understood by the system will be ignored and install will not be blocked.


