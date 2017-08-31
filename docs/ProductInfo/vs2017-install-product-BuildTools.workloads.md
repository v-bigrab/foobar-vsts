---
redirect_url: https://aka.ms/vs2017componentids
---


# Visual Studio Build Tools 2017 component directory

The tables below provide the IDs you can use to install Visual Studio using the command line. 

**Understanding this page**  

The tables on this page include the workload and component IDs you’ll need to install Visual Studio 2017 by using 
the command line. Note that we may add additional components as we release updates to Visual Studio.

Each workload has its own section on this page, followed by the workload ID and a table of the components that are 
available for the workload. By default, the **Required** components will be installed when you install the workload. 
If you choose to, you can also install the **Recommended** and **Optional** components. 

At the end of this page, we’ve added a section that lists the additional components that are not affiliated with any 
workload. For more information, see [Use Command-Line Parameters to Install Visual Studio 2017](https://docs.microsoft.com/visualstudio/install/use-command-line-parameters-to-install-visual-studio).

For a list of workload and component IDs for other products, see [Visual Studio 2017 Workload and Component IDs](https://www.visualstudio.com/en-us/productinfo/vs2017-install-product--list).

## MSBuild Tools

**ID:** Microsoft.VisualStudio.Workload.MSBuildTools

**Description:** Provides the tools required to build MSBuild-based applications.

### Components included by this workload

Component ID | Name | Version | Dependency type
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 15.0.26004.1 | Required
Microsoft.VisualStudio.Component.CoreBuildTools | Visual Studio Build Tools Core | 15.0.26004.1 | Required
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# and Visual Basic Roslyn compilers | 15.0.26004.1 | Required


## Visual C++ build tools

**ID:** Microsoft.VisualStudio.Workload.VCTools

**Description:** Build classic Windows-based applications using the power of the Visual C++ toolset, ATL, and optional features like MFC and C++/CLI.

### Components included by this workload

Component ID | Name | Version | Dependency type
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.CoreBuildTools | Visual C++ Build Tools core features | 15.0.26004.1 | Required
Microsoft.VisualStudio.Component.Windows10SDK | Windows Universal C Runtime | 15.0.26004.1 | Required
Microsoft.VisualStudio.Component.VC.CMake.Project | Visual C++ tools for CMake | 15.0.26004.1 | Recommended
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26127.0 | Recommended
Microsoft.Component.VC.Runtime.UCRTSDK | Windows Universal CRT SDK | 15.0.26004.1 | Optional
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 15.0.26004.1 | Optional
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 targeting pack | 15.0.26004.1 | Optional
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Static analysis tools | 15.0.26004.1 | Optional
Microsoft.VisualStudio.Component.VC.ATL | Visual C++ ATL support | 15.0.26109.1 | Optional
Microsoft.VisualStudio.Component.VC.ATLMFC | MFC and ATL support (x86 and x64) | 15.0.26109.1 | Optional
Microsoft.VisualStudio.Component.VC.ClangC2 | Clang/C2 (experimental) | 15.0.26109.1 | Optional
Microsoft.VisualStudio.Component.VC.CLI.Support | C++/CLI support | 15.0.26206.0 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ core features | 15.0.26109.1 | Optional
Microsoft.VisualStudio.Component.VC.Modules.x86.x64 | Standard Library Modules | 15.0.26109.1 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | VC++ 2017 v141 toolset (x86,x64) | 15.0.26109.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10240 | Windows 10 SDK (10.0.10240.0) | 15.0.26004.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26004.1 | Optional
Microsoft.VisualStudio.Component.Windows81SDK | Windows 8.1 SDK | 15.0.26127.0 | Optional


## Web development build tools

**ID:** Microsoft.VisualStudio.Workload.WebBuildTools

**Description:** MSBuild tasks and targets for building web applications.

### Components included by this workload

Component ID | Name | Version | Dependency type
--- | --- | --- | ---
n/a | n/a | n/a | n/a

## Unaffiliated components

These are components that are not included with any workload, but may be selected as an individual component.

Component ID | Name | Version
--- | --- | ---
n/a | n/a | n/a
