---
title: Team Foundation Server 2015 Update 3 RC Known Issues
description: Team Foundation Server 2015 Update 3 RC Known Issues
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: visual-studio-tfs-dev14
ms.service: visualstudio
ms.assetid: 068438ab-fe2d-4c24-ad76-e9bc92f0719b
---


# Team Foundation Server Update 3 RC Known Issues
## June 7, 2016

Microsoft released Team Foundation Server Update 3 Release candidate on June 7, 2016. This article lists the known issues for Team Foundation Server Update 3 RC. 

To see the full list of features check out the [Team Foundation Server Update 3 RC Release Notes](https://www.visualstudio.com/news/releasenotes/tfs2015-update3-vs).


####  Download: [Team Foundation Server Update 3 RC](http://go.microsoft.com/fwlink/?LinkId=626619)

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/downloads/visual-studio-prerelease-downloads) page.

## Known Issues

#### Build output is corrupted for double byte character languages 
* #### Issue:
 On the Copy Files build task, the string “Copying <source file> to <target file>” in the build output is corrupted for double byte character languages. The file paths are still legible, and only affects the surrounding verbiage that appears as corrupted text in the build log.

  ###### Workaround:
  No workaround is required as the build completes without any errors.
  

## More information   

  [How to download Microsoft support files](https://support.microsoft.com/en-us/kb/119591)

  Updates for other products in the Team Foundation Server family can be found on the  [VisualStudio.com](https://www.visualstudio.com/downloads/download-visual-studio-vs) website.


#### Restart requirement

 You may have to restart your computer after you install this package.

#### Software requirement

To apply this update, you must have Team Foundation Server 2015 installed on your computer.


####  Supported architectures

* 32-bit (x86)

* 64-bit (x64) (WOW)

#### Applies to

* Team Foundation Server 2015


* Team Explorer Everywhere 2015


* Team Foundation Server Express 2015


* Team Foundation Server for Project Server Extensions 2015
