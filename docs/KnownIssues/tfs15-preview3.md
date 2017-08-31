---
title: Team Foundation Server "15" Preview 3 Known Issues
description: Team Foundation Server "15" Preview 3 Known Issues
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: visual-studio-tfs-dev15
ms.service: visualstudio
ms.assetid: f34237cb-5b82-498b-99d9-952c359ee1d3
---


# Team Foundation Server “15” Preview Known Issues

## July 7, 2016

Today, Microsoft released Team Foundation Server "15" Preview. This article lists the known issues for this release. To see the full list of features, check out the [TFS "15" Preview Release Notes](https://www.visualstudio.com/news/releasenotes/tfs15-relnotes).

You can install the new Visual Studio release from the following link:

#### Download: [Team Foundation Server "15" Preview](https://go.microsoft.com/fwlink/?LinkId=817331 "Team Foundation Server 15 Preview")

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/en-us/downloads/visual-studio-next-downloads-vs "Downloads") page.

## Known Issues

#### Unable to restore or publish packages from Build
* #### Issue: 
  You will not be able to restore or publish packages from Team Build if the build agent is not running as an AD/domain account on a domain-joined machine.
  
* #### Workaround:
  You can set your build agent to run as a domain account on a domain-joined machine.

#### NuGet packages restore to an unexpected path

* #### Issue: 
   Nuget.config's repositoryPath is causing packages to be placed relative to a temporary copy of nuget.config.  
      
* #### Workaround:
   If possible, remove the repositoryPath setting completely to fall back on defaults.  If not possible, a temporary copy task will be needed to place the packages in the expected location. 

#### NuGet Restore is not finding packages that exist in nuget.org
* #### Issue: 
   Ensure nuget.org's feed is in nuget.config.
   
* #### Workaround:
   NuGet made a change between 3.3 and 3.4.3, so nuget.org as a package source needs to be listed explicitly. 
   
#### Kanban board fails with column configuration error
* #### Issue: 
   If you have your board configured to show bugs as requirements and the Bug and User Story work item type have different states, you will get an error "The column configurations are not valid.  The board cannot be displayed.  Correct this now."
   
* #### Workaround:
   Click the "correct this now" link to select the appropriate state mapping. This will be fixed in the next version.
   
#### Query Result widget fails when work item type doesn't have color assigned
* #### Issue: 
   Configuring the Query Result widget will fail with an error of "Ajax request failed with status: SyntaxError: Unexpected end of JSON input" if you have work item types that aren't assigned colors.
   
* #### Workaround:
   Assign colors to all work item types.  This will be fixed in the next version.
   
#### @mentions in pull requests and discussions may mention the wrong identity
* #### Issue: 
   When typing an @mention where the identity string is a substring of multiple identities, the first identity is used instead of the intended one.
   
* #### Workaround:
   There is no workaround at this time.  This will be fixed in the next version.
   
#### Refreshing a query does not refresh the work item
* #### Issue: 
   Refreshing a query does not refresh the individual work items in the query.
   
* #### Workaround:
   Refresh the individual work item to get the latest data.

## Applies To

- Team Foundation Server "15" Preview
