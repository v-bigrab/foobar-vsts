---
title: Team Foundation Server 2015 Update 3 Known Issues
description: Team Foundation Server 2015 Update 3 Known Issues
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: visual-studio-tfs-dev14
ms.service: visualstudio
ms.assetid: 4bf56fbf-d516-44af-b0a2-940b1dd97dd3
---


# Team Foundation Server Update 3 Known Issues
## June 27, 2016

Microsoft released Team Foundation Server Update 3 on June 27, 2016. This article lists the known issues for Team Foundation Server Update 3. If these were not the known issues you were expecting, you have reached the known issues for the most current version.

To see the full list of features check out the [Team Foundation Server Update 3 Release Notes](https://go.microsoft.com/fwlink/?LinkId=798856).


####  Download: [Team Foundation Server Update 3](https://go.microsoft.com/fwlink/?LinkId=615439)

To learn more about other related downloads, see the [Downloads](https://www.visualstudio.com/downloads/download-visual-studio-vs) page.

## Known Issues

#### Build output is corrupted for double byte character languages 
* #### Issue:
 On the Copy Files build task, the string “Copying <source file> to <target file>” in the build output is corrupted for double byte character languages. The file paths are still legible, and only affects the surrounding verbiage that appears as corrupted text in the build log.

* #### Workaround:
  No workaround is required as the build completes without any errors.

  
#### Cannot change SSH port in Admin Console 
* #### Issue:
  When changing the SSH port in the TFS Admin Console, the port is not actually changed.
 
* #### Workaround:
  Reset the TeamFoundationSshService service after changing the SSH port in the Admin Console.

  
#### Additional commits associated with releases in Release Management
* #### Issue:
    When you use TF VC as your version control system, and you create a Release from a Build that compiles your source code, you may see additional commits associated with that Release. Consider a situation where you have the following source mappings in your Build: $/project/myapp1 and $/project/common. If you also have $/project/myapp2 in your version control, commits from that application will also be included in the Release even though that mapping is not present in the Build. This is because Release Management currently takes the most common root ($/project, in this case) and computes all the commits at that level.

* #### Workaround:
  * The only way to avoid this is to organize your version control folders such that the most common root corresponds to the mapping in Build.
  * We will fix this in future releases.  


#### The "Setting File" option does not work in the 'SonarQube for MSBuild - Begin Analysis build task'
* #### Issue:
  * The "Settings File" advanced field of the 'SonarQube for MSBuild - Begin Analysis' build task normally points
to a SonarQube setting file under source control. 
  * A regression in TFS 2015 Update 2 and Update 3 prevents you from using it.

* #### Workaround:
  * You can specify the location of the settings file in the "Additional settings" field using the /s: syntax. 
For example:
     "/s:$(BUILD.SOURCESDIRECTORY)/path/to/AnalysisConfig.xml"
  * More information is available on this [forum entry](https://social.msdn.microsoft.com/Forums/vstudio/en-US/daf24be2-1af8-48b4-9ebd-cec4886c2cb6/unable-to-find-the-sonarqube-analysis-settings-file-please-fix-the-path-to-this-settings-file?forum=TFService)
  * We will fix this in future releases (fixed in Team Services already).

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
