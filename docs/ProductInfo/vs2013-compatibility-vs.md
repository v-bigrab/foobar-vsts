---
title: Visual Studio 2013 Compatibility
description: Visual Studio 2013 Compatibility
keywords: visualstudio
author: pchapman
ms.author: pchapman
manager: sacalla
ms.date: 09/07/2016
ms.topic: release-article
ms.prod: vs-devops-alm
ms.technology: vs-devops-articles
ms.assetid: 9f753412-fc04-497b-8513-0943c773a256
---

# <a id="top"> </a> Visual Studio 2013 Platform Targeting and Compatibility

## System Requirements

When upgrading from Microsoft Visual Studio 2012 to Visual Studio 2013 you will take advantage of a refreshed and simplified environment with enhanced performance without any additional hardware requirements. Some of these core enhancements make use of capabilities that are only present in the latest versions of Windows and might require you to upgrade to a supported operating system.

The system requirements for Visual Studio 2015 can be found on the [Visual Studio 2013 System Requirement page](https://www.visualstudio.com/productinfo/vs2013-sysrequirements-vs).

## Platform Targeting

Visual Studio provides cutting-edge tools and technologies to create apps that take advantage of the latest platforms capabilities. Visual Studio 2013 also targets earlier platforms such as Windows XP and Windows Server 2003 so you can create new apps or modernize existing apps that execute on earlier versions of Windows while leveraging the enhanced development tools, quality enablement, and team collaboration capabilities in Visual Studio 2013. For more information, see [Managing Project References](https://msdn.microsoft.com/library/vstudio/ez524kew(v=vs.120).aspx) and [Visual Studio Multi-Targeting Overview](https://msdn.microsoft.com/library/bb398197(v=vs.120).aspx).

## Visual Studio 2013 Support for Windows Desktop Development

<table>
<col width="20%">
<col width="40%">
<col width="40%">

<tr> 
  <td>**Targeted Platform** <sup>1</sup></td>
  <td align="center">**Native Code Development**</td> 
  <td align="center">**Managed Code Development**</td>
</tr>

<tr><td colspan="3" bgcolor=#565758><Font color=#FFFFF>Client OS</td></tr>

<tr>
  <td><FONT SIZE="2">Windows 8.1</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>2</sup></td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>2</sup></td>
</tr>
<tr>
  <td><FONT SIZE="2">Windows 8</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>2</sup></td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>2</sup></td>
</tr>
<tr>
  <td><FONT SIZE="2">Windows 7</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
</tr>
<tr>
  <td><FONT SIZE="2">Windows Vista</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>5</sup></td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>5</sup></td>
</tr>
<tr>
  <td><FONT SIZE="2">Windows XP</td>
<td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>4</sup></td>
<td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>4, 5</sup></td>
</tr>
<tr><td colspan="3" bgcolor=#696c6d><Font color=#FFFFF>Server OS</td></tr>
<tr>
  <td><FONT SIZE="2">Windows Server 2012 R2</td>
<td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>2</sup></td>
<td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>2</sup></td>
</tr>
<tr>
  <td><FONT SIZE="2">Windows Server 2012</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
</tr>
<tr>
  <td><FONT SIZE="2">Windows Server 2008 R2</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
</tr>
<tr>
  <td><FONT SIZE="2">Windows Server 2008</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
</tr>
<tr>
  <td><FONT SIZE="2">Windows Server 2003</td>
<td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>3, 5</sup></td>
<td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>4, 5</sup></td>
</tr>
<tr><td colspan="3">
**Footnotes:**  
<FONT SIZE="2">1. Visual Studio supports the listed platforms when used with the latest available service pack for that platform. For more information, see [Microsoft Support Lifecycle](http://support.microsoft.com/lifecycle/).    
<FONT SIZE="2">2. See table below for Visual Studio 2013 support for Windows Store app development, including WinJS development.  
<FONT SIZE="2">3. Requires side-by-side installation of Visual Studio 2010. For more information, see: [A Look Ahead at the Visual Studio 2012 Product Lineup and Platform Support](https://go.microsoft.com/?linkid=9809565).  
<FONT SIZE="2">4. Requires using [Visual Studio managed multi-targeting](https://msdn.microsoft.com/library/bb398197.aspx).  
<FONT SIZE="2">5. Remote debugging and profiling tools not available for targeted platform.
</table> 

## Visual Studio 2013 Support for Windows Store App and Windows Phone Development

You can create Windows Store and Windows Phone apps with the following editions of Visual Studio 2013.

<table>
<col width=22%>
<col width=12%>
<col width=12%>
<col width=12%>
<col width=15%>
<col width=12%>
<tr>
  <td bgcolor=#565758><FONT SIZE="2"><Font color=#FFFFF>**Visual Studio 2013 Edition**</td>
  <td  align="center" bgcolor=#565758><FONT SIZE="2"><Font color=#FFFFF>**Installed OS for Development**</td>
  <td  align="center" bgcolor=#565758><FONT SIZE="2"><Font color=#FFFFF>**Windows Store apps for Windows 8.1**</td>
  <td  align="center" bgcolor=#565758><FONT SIZE="2"><Font color=#FFFFF>**Windows Phone 8.1 apps**</td>   
  <td  align="center" bgcolor=#565758><FONT SIZE="2"><Font color=#FFFFF>**Windows Store apps for Windows 8**</td>
  <td  align="center" bgcolor=#565758><FONT SIZE="2"><Font color=#FFFFF>**Windows Phone 8 apps**</td>
</tr>
<tr>
  <td><FONT SIZE="2">Express for Windows</td>
  <td align="center"><FONT SIZE="2">Windows 8.1</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>1</sup></td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
  <td align="center"><FONT SIZE="2">Not Supported <sup>2</sup></td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>5, 6, 7</sup></td>
</tr>
<tr>
  <td><FONT SIZE="2">Ultimate, Premium, Professional</td>
  <td align="center"><FONT SIZE="2">Windows 8.1</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>1</sup></td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark:</td>
  <td align="center"><FONT SIZE="2">Service existing <sup>1, 2, 3</sup></td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>4, 7</sup></td>
</tr>
<tr>
  <td><FONT SIZE="2">Ultimate, Premium, Professional</td>
  <td align="center"><FONT SIZE="2">Windows Server 2012 R2</td>
  <td align="center"><FONT SIZE="2">Build only <sup>1</sup> </td>
  <td align="center"><FONT SIZE="2">Build only</td>
  <td align="center"><FONT SIZE="2">Build only</td>
  <td align="center"><FONT SIZE="2">Build only</td>
</tr>
<tr>
  <td><FONT SIZE="2">Ultimate, Premium, Professional</td>
  <td align="center"><FONT SIZE="2">Windows 8</td>
  <td align="center"><FONT SIZE="2">Not Supported</td>
  <td align="center"><FONT SIZE="2">Not Supported</td>
  <td align="center"><FONT SIZE="2">Not Supported</td>
  <td align="center"><FONT SIZE="2">:heavy_check_mark: <sup>4</sup></td>
</tr>
<tr>
  <td><FONT SIZE="2">Ultimate, Premium, Professional</td>
  <td align="center"><FONT SIZE="2">Windows Server 2012</td>
  <td align="center"><FONT SIZE="2">Not Supported</td>
  <td align="center"><FONT SIZE="2">Not Supported</td>
  <td align="center"><FONT SIZE="2">Not Supported</td>
  <td align="center"><FONT SIZE="2">Build only</td>
</tr>
<tr><td colspan=6>
**Footnotes:**    
<FONT SIZE="2">1.  Includes support for remote debugging to Windows 8.1.    
<FONT SIZE="2">2.  Visual Studio 2013 supports migration of Windows Store app projects from Windows 8 to Windows 8.1.   
<FONT SIZE="2">3.  Existing Windows 8 projects may be maintained with Visual Studio 2013, including remote debugging to Windows 8.1 and Windows 8. Use Visual Studio 2012 to create new Windows 8 projects.   
<FONT SIZE="2">4.  Visual Studio 2013 supports migration of Windows Phone 7 and 7.5 projects to Windows Phone 8.  
<FONT SIZE="2">5.  Requires Visual Studio 2013 Update 2 or later.
<FONT SIZE="2">6.  Windows Phone emulator installed on demand.
<FONT SIZE="2">7.  Supports migration of Windows Phone 8 projects to Windows Phone Silverlight 8.1.
</table>

## Compatibility with Previous Releases

Windows Store app projects for Windows 8.1 and Windows Phone 8.1 cannot be opened in earlier versions of Visual Studio.

You can install and use Visual Studio 2013 alongside Visual Studio 2012. When installed on Windows 8.1, Visual Studio 2012 continues to support creation of Windows Store apps for Windows 8 and Windows Phone 8. In addition, Visual Studio 2012 Update 3 contains improvements for project compatibility between Visual Studio 2012 and Visual Studio 2013, and resolves compatibility issues for Visual Studio 2012 on Windows 8.1.

.NET 4.5.1 is a highly compatible in-place update of .NET 4 and .NET 4.5.

For additional information, see [Visual Studio 2013 Compatibility](https://msdn.microsoft.com/library/hh266747(v=vs.120).aspx).

### Upgrade paths

When following the supported upgrade paths, your Visual Studio source, solution, and project files will continue to work; however, you should expect to make some changes to sources. While we cannot guarantee binary compatibility between releases, we will do our best to document significant changes to assist you with updates.

#### Supported:

* Upgrade from Visual Studio Team Foundation Server (and Express) 2012 (RTM or any Update) to Visual Studio Team Foundation Server (and Express) 2013
* Upgrade from Visual Studio Team Foundation Server (and Express) 2010 to Visual Studio Team Foundation Server (and Express) 2013

### Carrying assets forward

All data in Visual Studio Team Foundation Server (work items, source files, tests and test results, builds, and warehouse data) carries forward when following supported upgrade paths. However, even when following supported upgrade paths, you should take adequate measures to back up and protect your data prior to upgrading to a new release.

[Top of Page](#top)