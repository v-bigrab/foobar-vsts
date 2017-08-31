---
redirect_url: /productinfo/vs2017-FAQ
---


# Frequently Asked Questions (FAQ) for Visual Studio 2017 RC

## General

####  What are the highlights of RC?

In Visual Studio 2017 RC we have made lots of performance and productivity improvements.
A more detailed explanation can be found in this [blog post](https://blogs.msdn.microsoft.com/visualstudio/2016/11/16/visual-studio-2017-rc/). 
Also, you can now select a different UI language for Visual Studio at the time of installation, using the Language Pack tab.



For full details of what is new, see the [Release notes](https://www.visualstudio.com/news/releasenotes/vs2017-relnotes#willow). 

#### What editions are supported in RC?

For RC we are shipping a variety of SKUs and a consolidate list can be found on the [download page](https://www.visualstudio.com/downloads).

#### Is .NET Core and ASP.NET Core development supported in Visual Studio 2017 RC?

Yes. Tooling support for .NET Core and ASP.NET Core projects is available in this release of Visual Studio.

#### Is the Azure workload supported in RC?

The Azure workload is available for RC.

#### What platforms can I target using Visual Studio 2017 RC?

The list of operating systems, platforms, and technologies for which you can develop applications can be found [here](https://www.visualstudio.com/productinfo/vs2017-compatibility-vs).

#### Is Visual Studio 2017 RC compatible with previous releases?

Information on compatibilility with previous releases can be found [here](https://www.visualstudio.com/productinfo/vs2017-compatibility-vs).


## Feedback and Reporting Problems

#### What is the best way to provide feedback?
We strongly encourage you to use the [Report a Problem](https://msdn.microsoft.com/en-us/library/mt786523.aspx) feature to provide us with feedback or to report a problem. You can access this functionality by clicking the button at the top right of the window in *either* the Visual Studio Installer window or in the IDE.

Reporting a New Problem using Report a Problem tool:-
1. At the bottom left of the Visual Studio Report a Problem tool, click the "+" button.
2. Create a descriptive title for the problem that will help us route it to the correct Visual Studio team.
3. Give us any additional details, and if possible, provide us with the steps to reproduce the problem.

Using the Report a Problem feature rather than email, Twitter, blog comments, or other methods will help us address your issue faster because it provides more contextual data to help us efficiently analyze, diagnose, and fix reported issues.

#### How can I keep track of my issues logged via Report a Problem?
You can now view, track, and follow all issues you reported using Report a Problem in Visual Studio on the [Visual Studio Developer Community portal](https://developercommunity.visualstudio.com).

#### What information should I provide when reporting install issues?
To report issues with installation, click the Report a Problem button in the title bar of the Visual Studio Installer, and describe the issue that you've encountered. This will include the installation data we need in most cases to diagnose the issue. 

#### What information should I provide when reporting memory issues?
For issues in the Visual Studio IDE, use the Report a Problem user feedback icon on the title bar or from the Help Menu. For memory related problems heap dump files are very useful in helping us diagnose problems. 
Using the record option in the Report a Problem tool to record your repro steps collects a heap dump for you. These instructions are also availalble [here](https://msdn.microsoft.com/en-us/library/mt786523.aspx).
 
#### What information should I provide when reporting a performance problem?
For issues in Visual Studio IDE, use Report a Problem user feedback icon on the title bar or from the Help Menu. For performance related problems etl stack traces are very useful in helping us diagnose problems. 
Using the record option in Report a Problem tool to record your repro steps collects etl traces for you. These instructions are also availalble [here](https://msdn.microsoft.com/en-us/library/mt786523.aspx).

## Installation

#### What are the system requirements for Visual Studio 2017 RC?

System requirements for Visual Studio 2017 RC are listed [here](https://www.visualstudio.com/productinfo/vs2017-system-requirements-vs).

#### Can I install Visual Studio 2017 RC if I have already installed one of the prior Visual Studio '15' Previews?

Absolutely!   However, the prior previews of Visual Studio "15" must be uninstalled first.  During installation of Visual Studio 2017 RC, a cleaning tool will automatically be run on your machine that will detect artifacts from a prior preview installation and then remove them.  This process will ensure a "clean machine" state before the RC is installed. 

#### Can I install Visual Studio 2017 RC with Visual Studio 2015?

Yes, you can install this side by side with Visual Studio 2015.  Note that Visual Studio 2015 must be closed in order for the Visual Studio 2017 RC install to proceed.  There are a few other [known issues](https://www.visualstudio.com/news/releasenotes/vs2017-relnotes#knownissues) that you should be aware of.

#### How do I install updates to Visual Studio 2017 RC?

We will be delivering product updates to Visual Studio 2017 RC as we continue to improve the product quality and complete the final touches before it's finished.  When the update is available, the notification flag on the right side of the application title bar will pop.   Click on the notification, and install the quick update.  Note that you'll have to shut down the IDE prior installing the update.       

#### Where can I find ISO files for Visual Studio 2017 RC?

We do not have ISO files in Visual Studio 2017 RC, rather there is the ability to create your own offline layout installer. For more information read: [How to do offline install](https://go.microsoft.com/fwlink/?linkid=834546).
