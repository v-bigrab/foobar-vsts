---
title: Visual Studio Servicing
description: Visual Studio Servicing
keywords: visualstudio
author: denizd
ms.author: denizd
manager: sacalla
ms.date: 05/10/2017
ms.topic: release-article
ms.prod: vs-devops-alm
ms.technology: vs-devops-articles
ms.assetid: dde71a19-97af-4e3e-a5fb-90104abe5cbe
---

# Servicing for Visual Studio and Team Foundation Server Products

## For Visual Studio and Team Foundation Server 2012 - 2017 

These products follow the Microsoft Support Lifecycle Policy of 10 years (5 years of Mainstream Support and 5 years of Extended Support), starting with the date the major product version is released to the world (RTW). For example, Visual Studio 2017 was released in 2017; its support lifecycle will end in 2027.

Servicing for these products is performed via “Updates” which are packages of new features and cumulative fixes for existing features in the product.

For these product versions, we support the RTW version for a period of time as detailed below, and the latest Update until the lifecycle completes.

### Support for Updates 

Once you install an Update over the RTW product, you must then continue to upgrade to the latest Update to remain in a supported state until the lifecycle completes.  

**Example 1:** If you have Visual Studio 2017 version 15.1, when 15.2 is released, you must move to 15.2 to continue being supported.

**Example 2:** If you have Visual Studio 2015 Update 2, when Update 3 is released, you must move to Update 3 to continue being supported.

### How to get Updates 

Customers can get the Updates by following in-product prompts to update their version or by downloading the latest from [VisualStudio.com](https://www.visualstudio.com/) or [My.VisualStudio.com](https://my.visualstudio.com/). 

### Service Packs 

During the support lifecycle, Microsoft will designate one of the Updates of that product as the “Service Pack”.

* For Visual Studio 2017, the service pack has not yet been designated. For Team Foundation Server 2017, the service pack has not yet been designated. 

* For Visual Studio 2015, the designated Service Pack is Update 3 with the latest release of  [KB3165756](https://msdn.microsoft.com/library/mt752379.aspx). For Team Foundation Server 2015, there were two designated Service Packs - Update 3 and Update 4. Please see the [Team Foundation Server product entry on the Lifecycle Policy site](https://support.microsoft.com/en-us/lifecycle/search?alpha=team%20foundation%20server%202015) for dates.

* For Visual Studio 2013 and Team Foundation Server 2013, the designated Service Pack is Update 5.

* For Visual Studio 2012 and Team Foundation Server 2012, the designated Service Pack is Update 4.

When Microsoft designates an Update as a Service Pack, the [Support Lifecycle Database](https://support.microsoft.com/lifecycle/search?sort=PN&alpha=Visual%20Studio&Filter=FilterNO) will reflect the appropriate dates for support.

### Support for RTW  

For customers who are still on the RTW version, the Service Pack date is an important milestone. Support for RTW will be discontinued 1 year after an Update is designated as the “Service Pack”, per the [Microsoft Support Service Pack Lifecycle Policy](https://support.microsoft.com/lifecycle). Customers still on the RTW version should upgrade to the latest available Update before the end of that 1 year to continue to be in a supported state.  

* For Visual Studio 2017, customers who remain on the RTW version 15.0.x will continue to be supported until a service pack is designated, at which time, they will have one (1) year to move to the latest version of the product available.

* For Visual Studio 2015 and Team Foundation Server 2015, RTW will cease to be supported on October 10, 2017.

* For Visual Studio 2013 and Team Foundation Server 2013, RTW is no longer supported.

* For Visual Studio 2012 and Team Foundation Server 2012, RTW is no longer supported.

## For Visual Studio and Team Foundation Server 2008 – 2010 

The lifecycle for these products follows the Microsoft Support Lifecycle Policy of 10 years (5 years Mainstream Support and 5 years Extended Support), starting with the date RTW is released. These products are now in Extended Support and are only eligible for security fixes. For more information, please see the [Microsoft support lifecycle policy](https://support.microsoft.com/help/14085/microsoft-lifecycle-policy) or search the [Support Lifecycle Database](https://support.microsoft.com/lifecycle/search) for relevant dates.

## Components not covered by Visual Studio servicing

Visual Studio includes a collection of compilers, languages, runtimes, environments, and other resources or tools that enable development for many platforms. As a convenience to Visual Studio customers, the components in the list below may be installed with Visual Studio are subject to their own license and support & lifecycles policies. Please note this list does not represent the entire list of Visual Studio components which are governed by their own policy but aims to highlight the most used.

For those components that are installed by Visual Studio and do not have an explicit lifecycle policy in the lifecycle database, the supported version is the latest version that is currently available for download:

<table>
<col width=33%>
<col width=33%>
<col width=34%>

<tr>
  <td><FONT SIZE="2">[.NET](https://support.microsoft.com/lifecycle/search?alpha=.NET)</td>
  <td><FONT SIZE="2">[ASP.NET Web Stack](https://support.microsoft.com/kb/2902020)</td>
  <td><FONT SIZE="2">[.NET Core](https://support.microsoft.com/lifecycle/search?alpha=asp.net)</td>
</tr>
<tr>
  <td><FONT SIZE="2">[Entity Framework](https://support.microsoft.com/lifecycle/search?alpha=entity%20frame)</td>
  <td><FONT SIZE="2">[Exchange](https://support.microsoft.com/lifecycle/search?alpha=exchange)</td>
  <td><FONT SIZE="2">[Office](https://support.microsoft.com/lifecycle/search?alpha=office)</td>
</tr>
<tr>
  <td><FONT SIZE="2">[Windows](https://support.microsoft.com/lifecycle/search?alpha=windows)</td>
  <td><FONT SIZE="2">[Windows Server](https://support.microsoft.com/lifecycle/search?alpha=windows%20server)</td>
  <td><FONT SIZE="2">[Online Services](https://support.microsoft.com/help/17139/microsoft-online-services-support-lifecycle-policy)</td>
</tr>
<tr>
  <td><FONT SIZE="2">[SharePoint](https://support.microsoft.com/lifecycle/search?alpha=sharepoint)</td>
  <td><FONT SIZE="2">[Silverlight](https://support.microsoft.com/lifecycle/search?alpha=silverlight)</td>
  <td><FONT SIZE="2">[SQL Server](https://support.microsoft.com/lifecycle/search?alpha=sql)</td>
</tr>
<tr>
  <td><FONT SIZE="2">[Microsoft Azure](https://support.microsoft.com/help/18486)</td>
  <td><FONT SIZE="2">[Application Insights](https://support.microsoft.com/help/17139)</td>
  <td><FONT SIZE="2">[Xamarin](https://developer.xamarin.com/releases/current/)</td>
</tr>
<tr>
  <td><FONT SIZE="2">Cordova Tools for Visual Studio</td>
  <td><FONT SIZE="2">Python Tools for Visual Studio</td>
  <td><FONT SIZE="2">R Tools for Visual Studio</td>
</tr>
<tr>
  <td><FONT SIZE="2">VCMDD</td>
  <td><FONT SIZE="2">TypeScript</td>
  <td><FONT SIZE="2">NuGet</td>
</tr>
<tr>
  <td><FONT SIZE="2">Unity Tools for Visual Studio</td>
  <td><FONT SIZE="2">Clang/C2 Toolset</td>
  <td><FONT SIZE="2">[Git for Windows](https://git-scm.com/download/win)</td>
</tr>
<tr>
  <td><FONT SIZE="2">SignalR</td>
  <td><FONT SIZE="2">Web Optimization Framework</td>
  <td><FONT SIZE="2">WebGrease</td>
</tr>
<tr>
  <td><FONT SIZE="2">Visual Studio Emulator for Android</td>
  <td><FONT SIZE="2">JSON Web Token Handler for the Microsoft .Net Framework</td>
  <td><FONT SIZE="2">Windows SDK</td>
</tr>
</table>


In addition to components, Visual Studio also uses several projects and project item templates. The support for these templates is governed by the component that provides those templates. For example, if you use a Python template, then support for the template will follow the Python Tools for Visual Studio support policy. 