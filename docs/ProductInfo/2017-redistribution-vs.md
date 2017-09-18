---
title: Visual Studio 2017 Redistribution
description: Visual Studio 2017 Redistribution
keywords: visualstudio
author: reshmim
ms.author: reshmim
manager: sacalla
ms.date: 9/15/2017
ms.topic: release-article
ms.prod: visual-studio-dev15
ms.service: visualstudio
ms.assetid: fe66e774-caa0-4441-b9cf-6b3701b8b5dc
---

# <a id="top"> </a> Distributable Code for Microsoft Visual Studio 2017 (Includes Utilities, Extensibility, and BuildServer Files)

## On this Page
* [Distributable Code Files for Visual Studio 2017](#VisualStudio)
* [Distributable Code Files for the Concurrency Visualizer Software Development Kit](#concurrency)
* [Distributable Code Files for Visual Studio Extension Development](#SDK)
* [List of Utilities for Visual Studio 2017](#util)
* [List of BuildServer Files for Visual Studio 2017](#bldsrv)
* [List of Application Insights Files](#AI)
* [Distributable Code Files for Mobile Development with Xamarin](#xamarin)

**Note:** In the lists below, 
* [arch] represents the processor architecture identifier, for instance "x86", "x64", or "arm". 
* [locale] represents a specific language, locale, or culture identifier, for instance "ENU", "en-us", or "1033".
* [version] represents a folder name that uses a version number.
* [VisualStudioFolder] represents the install location for Visual Studio 2017.  

## <a id="VisualStudio"> </a>Distributable Code Files for Visual Studio 2017
The following section is the "REDIST list" that is referenced in the "Distributable Code" section of the Microsoft Software License Terms for 
Visual Studio Enterprise 2017, Visual Studio Professional 2017, Visual Studio Community 2017 ("the software"). 
If you have a validly licensed copy of such software, you may copy and distribute with your program the unmodified form of the files listed below, subject to the License Terms for the software.

### ASP.NET Libraries
The following software components are licensed and supported separately under the Microsoft .NET Library terms located at http://www.microsoft.com/web/webpi/eula/aspnetcomponent_rtw_enu.htm. 
If you do not agree to the license terms for these software components, you may not use them.  
* MVC  
* Web API  
* Web Pages with Razor  
* Entity Framework  
* SignalR  
* Katana  
* Microsoft XML Document Transformation  

### Microsoft Azure
#### Source
* MobileServices.js  
* MobileServices.min.js  

#### Object Code
* Microsoft.WindowsAzure.Mobile.dll  
* Microsoft.WindowsAzure.Mobile.resources.dll  
* Microsoft.WindowsAzure.Mobile.UI.dll  
* Microsoft.WindowsAzure.Ext.dll  

### Blend and XAML Designers for Visual Studio

Redistributable files for Blend Project and Item Templates for Visual Studio are installed in the following locations:
* [VisualStudioFolder]\Common7\IDE\ProjectTemplates  
* [VisualStudioFolder]\Common7\IDE\ItemTemplates  
* [VisualStudioFolder]\DesignTools\AppThemes  
* [Program Files (x86)]\MSBuild\Microsoft\Expression\Blend\.NETFramework 

#### Blend for Visual Studio

Redistributable files for Blend for Visual Studio are installed in the following locations:  
* [Program Files (x86)]\Microsoft SDKs\Expression\Blend\.NETFramework\v4.0  
* [Program Files (x86)]\Microsoft SDKs\Expression\Blend\.NETFramework\v4.5  

#### Sample Data Resources

* [VisualStudioFolder]\DesignTools\SampleData

### .NET Framework 4.6.2
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:    

#### Offline Installer  
* dotNetFx-x86-x64-AllOS-ENU.exe (.NET Framework 4.6.2 as present in Visual Studio)
* NDP462-KB3151800-x86-x64-AllOS-ENU.exe (.NET Framework 4.6.2 as present on other channels, such as the Microsoft Download Center)

**Note:** Both files are identical but may use different names for different distribution channels.  
 
#### Language Packs  
* dotNetFx-x86-x64-AllOS-[locale].exe  
* NDP462-KB3151800-x86-x64-AllOS-[locale].exe  

**Notes:** 
* Both files are identical but may use different names for different distribution channels.  
* [locale] represents the specific three-letter language identifier. For instance, NDP462-KB3151800-x86-x64-AllOS-DEU.exe  
   * Language Packs are available for the following (listed here with their associated identifier code):
     Arabic (ARA), Chinese-Taiwan (CHT), Czech (CSY), Danish (DAN), German (DEU), Greek (ELL), Finnish (FIN), French (FRA), Hebrew (HEB), Hungarian (HUN), Italian (ITA), Japanese (JPN), Korean (KOR), Dutch-Netherlands (NLD), Norwegian (NOR), Polish (PLK), Portuguese-Brazil (PTB), Russian (RUS), Swedish (SVE), Turkish (TRK), Chinese (CHS), Portuguese-Portugal (PTG), Spanish (ESN)  

### F# Runtime
* Fsharp.Core.dll  

### ADO.NET
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:    
* System.Data.dll  
* System.Data.DatasetExtensions.dll  
* System.Data.OracleClient.dll  
* Adonetdiag.dll  

### DIA SDK
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:  
* [VisualStudioFolder]\DIA SDK\bin\msdia140.dll  
* [VisualStudioFolder]\DIA SDK\bin\amd64\msdia140.dll  
* [VisualStudioFolder]\DIA SDK\bin\arm\msdia140.dll

### Visual C++ Runtime Files

Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, as a part of the installation package of your program:  
* [Program Files (x86)]\Common Files\Merge Modules\  
  * Microsoft\_VC140\_CRT\_\[arch].msm  
  * Microsoft\_VC140\_CXXAMP\_\[arch].msm  
  * Microsoft\_VC140\_MFC\_\[arch].msm  
  * Microsoft\_VC140\_MFCLOC\_\[arch].msm  
  * Microsoft\_VC140\_OpenMP\_\[arch].msm  

Subject to the License Terms for the software, you may copy and distribute with your program any of the files within the following folder and its subfolders except as noted below. You may not modify these files.
* [VisualStudioFolder]\VC\redist
* You may not distribute the contents of the following folders:  
  * [VisualStudioFolder]VC\Redist\MSVC\\[version]\debug_nonredist
  * [VisualStudioFolder]VC\Redist\MSVC\\[version]\debug_nonredist
  * [VisualStudioFolder]\VC\Redist\MSVC\\[version]\onecore\debug_nonredist

Subject to the License Terms for the software, you may copy and distribute the following files with your program in your program’s application local folder or by deploying them into the Global Assembly Cache (GAC):
* [VisualStudioFolder]\VC\Tools\MSVC\\[version]\atlmfc\lib\\[arch]\mfcmifc80.dll  


### Universal Windows Apps and Windows Store Apps
**Side-loading of Universal Windows Apps**  

The AppX files contained in the following locations may be distributed unmodified with your Universal Windows apps that you intend to side-load:
* [Program Files (x86)]\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.VCLibs\14.0\Appx\Retail\\[arch]\Microsoft.VCLibs.[arch].14.00.appx
* [Program Files (x86)]\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.VCLibs.120\14.0\Appx\Retail\\[arch]\Microsoft.VCLibs.[arch].12.00.Universal.appx
* [Program Files (x86)]\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.NET.Native.Framework.1.3\1.3\\[arch]\ret\Native\Microsoft.NET.Native.Framework.1.3.appx
* [Program Files (x86)]\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.NET.Native.Runtime.1.4\1.4\AppX\\[arch]\Microsoft.NET.Native.Runtime.1.4.appx
* For additional versions of .NET Native, see https://www.nuget.org/packages/Microsoft.Net.Native.Compiler/. 

The files contained in the following locations may be distributed unmodified with your Universal Windows apps that you intend to side-load:
* [Program Files (x86)]\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\CppUnitTestFramework.Universal\15.0\Redist\CommonConfiguration
* [Program Files (x86)]\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\MSTestFramework.Universal\15.0\Redist\CommonConfiguration
* [Program Files (x86)]\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\TestPlatform.Universal\15.0\Redist\CommonConfiguration


### SQL Server Database Tooling files
Subject to the License Terms for the software, you may copy and distribute the .dll files and .exe files, unmodified, in this folder with your program:  
* [VisualStudioFolder]Common7\IDE\Extensions\Microsoft\SQLDB\DAC\120
* [VisualStudioFolder]Common7\IDE\Extensions\Microsoft\SQLDB\DAC\130

### SQL Server Redistributable Components
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:
* SqlCmdLnUtils.msi  
* sqlncli.msi  
* SSCERuntime\_x64-enu.exe  
* SSCERuntime\_x86-enu.exe  
* sqllocaldb.msi  
* SharedManagementObjects.msi  
* SqlDom.msi  
* SQLSysClrTypes.msi  
* TSqlLanguageService.msi  

### Microsoft WCF Data Services files
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:
* Microsoft.Data.Services.dll  
* Microsoft.Data.Services.Client.dll  
* Microsoft.Data.OData.dll  
* Microsoft.Data.Edm.dll  
* System.Spatial.dll  

### Microsoft Visual Studio Tools for Office 
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:
* Microsoft.Office.Tools.Common.v4.0.Utilities.dll
* Microsoft.Office.Tools.Excel.v4.0.Utilities.dll
* Microsoft.Office.Tools.Outlook.v4.0.Utilities.dll
* Microsoft.Office.Tools.Word.v4.0.Utilities.dll
  
Subject to the License Terms for the software, you may copy and distribute the following files with your program:
* setup.exe (bootstrapper used to install Office Add-ins)

## <a id="concurrency"> </a> Distributable Code Files for the Concurrency Visualizer Software Development Kit
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:
* Microsoft.ConcurrencyVisualizer.Markers.dll (for .NET 3.5)  
* Microsoft.ConcurrencyVisualizer.Markers.dll (for .NET 4.0)  
* cvmarkers.h  
* cvmarkersobj.h  


## <a id="SDK"> </a>Distributable Code Files for Visual Studio extension development

This is the "REDIST list" that is referenced in the "Distributable Code" section of the Microsoft Software License Terms for
Visual Studio 2017 ("the software"). If you have a validly licensed copy of the software, you may copy and distribute the 
unmodified object code form of the files listed below, subject to the License Terms for the software.
* [VisualStudioFolder]\VSSDK\VisualStudioIntegration\Redistributables\VS150_piaredist.exe  
* [VisualStudioFolder]\VSSDK\VisualStudioIntegration\Redistributables\VSSDKTestHost.exe  


## <a id="util"> </a>List of Utilities for Visual Studio 2017

This is the “Utilities List” that is referenced in the “Utilities” section of Microsoft Software License Terms for certain editions of Visual Studio 2017 (the “software”).
Depending on the specific edition of the software, the software you received may not include all of the files on this list. To determine your rights with respect to the 
following files, please refer to the Visual Studio License Terms that came with your edition of the software. You may not modify these files.  

[IntelliTrace Standalone Collector for Visual Studio 2017](https://www.visualstudio.com/downloads/#intellitrace-standalone-collector-for-visual-studio-2017) 
* [VisualStudioFolder]\Common7\IDE\CommonExtensions\Microsoft\IntelliTrace\IntelliTraceCollection.cab  
[Remote Tools for Visual Studio 2017)[https://www.visualstudio.com/downloads/#remote-tools-for-visual-studio-2017]  
* vs_remotetools.exe (both x86 and x64 versions) 
[Performance Tools for Visual Studio 2017](https://www.visualstudio.com/downloads/#performance-tools-for-visual-studio-2017)  
* [VisualStudioFolder]\Team Tools\Performance Tools\Setups\vs\_profiler\\[arch]\_x64\_[locale].exe  

**Visual C++ Utilities**  

The "Utilities List" includes the following files within in the subfolders of the directories specified:
* [VisualStudioFolder]\VC\Auxiliary\VS\redist\GraphicsDbgRedist\
  * VsGraphicsHelper.dll  
  * VsGraphicsResources.dll    
* [VisualStudioFolder]\VC\Redist\MSVC\\[version]\debug_nonredist\
  * concrt140d.dll 
  * mfc140ud.dll  
  * mfcm140ud.dll  
  * msvcp140d.dll  
  * vcamp140d.dll  
  * vccorlib140d.dll  
  * vcomp140d.dll  
  * vcruntime140d.dll  
* [VisualStudioFolder]\VC\Tools\MSVC\\[version]\bin\
  * pgort140.dll  
  * pgort140ui.dll  
  * pgosweep.exe  

## <a id="bldsrv"> </a>List of Build Server Files for Visual Studio 2017
This is the "Build Server List" that is referenced in the "Build Server" section of the Microsoft Software License Terms for certain editions of
Visual Studio 2017 (the "software"). To determine your rights with respect to the following files, please refer to the License Terms that came with your edition of the software.

### SharePoint Tooling for Visual Studio
[VisualStudioFolder]\MSBuild\Microsoft\VisualStudio\v15.0\SharePointTools\  
* Microsoft.VisualStudio.SharePoint.targets  
* Microsoft.VisualStudio.SharePoint.Tasks.dll  

[VisualStudioFolder]\Common7\IDE\  
* PrivateAssemblies\Microsoft.VisualStudio.SharePoint.Designers.Models.dll  
* PrivateAssemblies\Microsoft.VisualStudio.SharePoint.Designers.Models.Features.dll  
* PrivateAssemblies\Microsoft.VisualStudio.SharePoint.Designers.Models.Packages.dll  
* PublicAssemblies\Microsoft.VisualStudio.SharePoint.dll  

### Visual C++ Build Server files

Any of the files within the following folders and their subfolders.  
* Program Files\Common Files\Merge Modules  
* [VisualStudioFolder]\VC\  
* [VisualStudioFolder]\Common7\IDE\VC\VCTargets  
* [VisualStudioFolder]\Common7\Tools\vsdevcmd  
* [Program Files (x86)]\Microsoft Visual Studio\Shared\14.0\VC  
* [Program Files (x86)]\MSBuild\Microsoft.Cpp\v4.0\V140\  

**Individual Files**

* [VisualStudioFolder]\Common7\IDE\msobj120.dll  
* [VisualStudioFolder]\Common7\IDE\msobj140.dll  
* [VisualStudioFolder]\Common7\IDE\msvcdis120.dll  
* [VisualStudioFolder]\Common7\IDE\msvcdis140.dll  
* [VisualStudioFolder]\Common7\Tools\makehm.exe  
* [VisualStudioFolder]\Common7\Tools\VsDevCmd.bat  

## <a id="AI"> </a>Distributable Code Files for Application Insights for Visual Studio 2017

Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program built with Visual Studio 2017:

* Microsoft.ApplicationInsights.2.0.0.nupkg  
* Microsoft.ApplicationInsights.Agent.Intercept.1.2.1.nupkg  
* Microsoft.ApplicationInsights.AspNet.1.0.0-rc1-update4.nupkg  
* Microsoft.ApplicationInsights.AspNetCore.1.0.0-rc2-final.nupkg  
* Microsoft.ApplicationInsights.DependencyCollector.2.0.0.nupkg  
* Microsoft.ApplicationInsights.JavaScript.0.22.9-build00167.nupkg  
* Microsoft.ApplicationInsights.PerfCounterCollector.2.0.0.nupkg  
* Microsoft.ApplicationInsights.Web.2.0.0.nupkg  
* Microsoft.ApplicationInsights.WindowsServer.2.0.0.nupkg  
* Microsoft.ApplicationInsights.WindowsServer.TelemetryChannel.2.0.0.nupkg  
* Microsoft.Bcl.Async.1.0.168.nupkg  
* Microsoft.Diagnostics.Tracing.EventSource.Redist.1.1.24.nupkg  

## <a id="xamarin"> </a>Distributable Code Files for Mobile Development with Xamarin
Subject to the License Terms for the software, you may copy and distribute with your application built using Visual Studio or Visual Studio for Mac the object code form of the following files (and associated debug symbol files) as installed within subfolders of the following directories:

**On macOS® operating system:**
* /Library/Frameworks/Xamarin.iOS.framework
* /Library/Frameworks/Xamarin.Android.framework
* /Library/Frameworks/Xamarin.Mac.framework 

**On Windows operating system:**
* \[VisualStudioFolder]\MSBuild\Xamarin\,
* \[VisualStudioFolder]\Common7\IDE\ReferenceAssemblies\Microsoft\Framework\MonoAndroid,
* \[VisualStudioFolder]\Common7\IDE\ReferenceAssemblies\Microsoft\Framework\MonoTouch,
* \[VisualStudioFolder]\Common7\IDE\ReferenceAssemblies\Microsoft\Framework\Xamarin.iOS,
* \[VisualStudioFolder]\Common7\IDE\ReferenceAssemblies\Microsoft\Framework\Xamarin.Mac,
* \[VisualStudioFolder]\Common7\IDE\ReferenceAssemblies\Microsoft\Framework\Xamarin.TVOS, or
* \[VisualStudioFolder]\Common7\IDE\ReferenceAssemblies\Microsoft\Framework\Xamarin.WatchOS

#### Xamarin Distributable Code Files:

* FSharp.Compiler.CodeDom.dll
* FSharp.Core.dll
* FSharp.Core.optdata
* FSharp.Core.sigdata
* FSharp.Core.xml
* I18N.CJK.dll
* I18N.dll
* I18N.MidEast.dll
* I18N.Other.dll
* I18N.Rare.dll
* I18N.West.dll
* Info.plist
* Ionic.Zip.dll
* Irony.dll
* Java.Interop.dll
* Java.Interop.Tools.Cecil.dll
* Java.Interop.Tools.Diagnostics.dll
* Java.Interop.Tools.JavaCallableWrappers.dll
* libapp.a
* libextension.a
* libmono-2.0.a
* libmono-2.0.dylib
* libmono-android.debug.d.dylib
* libmono-android.debug.d.so
* libmono-android.debug.dylib
* libmono-android.debug.so
* libmono-android.release.d.dylib
* libmono-android.release.d.so
* libmono-android.release.dylib
* libmono-android.release.so
* libmono-btls-shared.d.so
* libmono-btls-shared.so
* libMonoPosixHelper.d.dylib
* libMonoPosixHelper.d.so
* libMonoPosixHelper.dylib
* libMonoPosixHelper.so
* libmono-profiler-log.a
* libmono-profiler-log.d.dylib
* libmono-profiler-log.d.so
* libmono-profiler-log.dylib
* libmono-profiler-log.so
* libmonosgen-2.0.a
* libmonosgen-2.0.d.dylib
* libmonosgen-2.0.d.so
* libmonosgen-2.0.dylib
* libmonosgen-2.0.so
* libtvextension.a
* libwatchextension.a
* libxamarin.a
* libxamarin.dylib
* libxamarin-debug.a
* libxamarin-debug.dylib
* libxammac.a
* libxammac.dylib
* libxammac-debug.a
* libxammac-debug.dylib
* libxammac-system.a
* libxammac-system-debug.a
* libzip.3.0.dylib
* libZipSharp.dll
* libZipSharp.dll.config
* machine.config
* Microsoft.CSharp.dll
* Microsoft.Win32.Primitives.dll
* Microsoft.Win32.Registry.AccessControl.dll
* Microsoft.Win32.Registry.dll
* Mono
* mono.android.dex
* Mono.Android.dll
* Mono.Android.Export.dll
* mono.android.jar
* Mono.Btls.Interface.dll
* Mono.CompilerServices.SymbolWriter.dll
* Mono.CSharp.dll
* Mono.Data.Sqlite.dll
* Mono.Data.Sqlite.dll.config
* Mono.Data.Tds.dll
* Mono.Messaging.dll
* Mono.Posix.dll
* Mono.Security.dll
* MonoTouch.Dialog-1.dll
* monotouch.dll
* MonoTouch.NUnitLite.dll
* monotouch-fixes.dylib
* mscorlib.dll
* netstandard.dll
* OpenTK.dll
* OpenTK.dll.config
* OpenTK-1.0.dll
* OpenTK-1.0.dll.config
* System.AppContext.dll
* System.Collections.Concurrent.dll
* System.Collections.dll
* System.Collections.NonGeneric.dll
* System.Collections.Specialized.dll
* System.ComponentModel.Annotations.dll
* System.ComponentModel.Composition.dll
* System.ComponentModel.DataAnnotations.dll
* System.ComponentModel.dll
* System.ComponentModel.EventBasedAsync.dll
* System.ComponentModel.Primitives.dll
* System.ComponentModel.TypeConverter.dll
* System.config
* System.Configuration.dll
* System.Configuration.Install.dll
* System.Console.dll
* System.Core.dll
* System.Data.Common.dll
* System.Data.dll
* System.Data.Linq.dll
* System.Data.Services.Client.dll
* System.Data.SqlClient.dll
* System.Diagnostics.Contracts.dll
* System.Diagnostics.Debug.dll
* System.Diagnostics.FileVersionInfo.dll
* System.Diagnostics.Process.dll
* System.Diagnostics.StackTrace.dll
* System.Diagnostics.TextWriterTraceListener.dll
* System.Diagnostics.Tools.dll
* System.Diagnostics.TraceEvent.dll
* System.Diagnostics.TraceSource.dll
* System.Diagnostics.Tracing.dll
* System.dll
* System.Drawing.Primitives.dll
* System.Dynamic.Runtime.dll
* System.EnterpriseServices.dll
* System.Globalization.Calendars.dll
* System.Globalization.dll
* System.Globalization.Extensions.dll
* System.IdentityModel.dll
* System.IdentityModel.Selectors.dll
* System.IO.Compression.dll
* System.IO.Compression.FileSystem.dll
* System.IO.Compression.ZipFile.dll
* System.IO.dll
* System.IO.FileSystem.AccessControl.dll
* System.IO.FileSystem.dll
* System.IO.FileSystem.DriveInfo.dll
* System.IO.FileSystem.Primitives.dll
* System.IO.FileSystem.Watcher.dll
* System.IO.IsolatedStorage.dll
* System.IO.MemoryMappedFiles.dll
* System.IO.Pipes.dll
* System.IO.UnmanagedMemoryStream.dll
* System.Json.dll
* System.Linq.dll
* System.Linq.Expressions.dll
* System.Linq.Parallel.dll
* System.Linq.Queryable.dll
* System.Messaging.dll
* System.Net.AuthenticationManager.dll
* System.Net.Cache.dll
* System.Net.dll
* System.Net.Http.dll
* System.Net.Http.WinHttpHandler.dll
* System.Net.HttpListener.dll
* System.Net.Mail.dll
* System.Net.NameResolution.dll
* System.Net.NetworkInformation.dll
* System.Net.Ping.dll
* System.Net.Primitives.dll
* System.Net.Requests.dll
* System.Net.Security.dll
* System.Net.ServicePoint.dll
* System.Net.Sockets.dll
* System.Net.Utilities.dll
* System.Net.WebHeaderCollection.dll
* System.Net.WebSockets.Client.dll
* System.Net.WebSockets.dll
* System.Numerics.dll
* System.Numerics.Vectors.dll
* System.ObjectModel.dll
* System.Reflection.Context.dll
* System.Reflection.DispatchProxy.dll
* System.Reflection.dll
* System.Reflection.Emit.dll
* System.Reflection.Emit.ILGeneration.dll
* System.Reflection.Emit.Lightweight.dll
* System.Reflection.Extensions.dll
* System.Reflection.Primitives.dll
* System.Reflection.TypeExtensions.dll
* System.Resources.ReaderWriter.dll
* System.Resources.ResourceManager.dll
* System.Runtime.CompilerServices.VisualC.dll
* System.Runtime.dll
* System.Runtime.Extensions.dll
* System.Runtime.Handles.dll
* System.Runtime.InteropServices.dll
* System.Runtime.InteropServices.RuntimeInformation.dll
* System.Runtime.InteropServices.WindowsRuntime.dll
* System.Runtime.Numerics.dll
* System.Runtime.Serialization.dll
* System.Runtime.Serialization.Formatters.dll
* System.Runtime.Serialization.Formatters.Soap.dll
* System.Runtime.Serialization.Json.dll
* System.Runtime.Serialization.Primitives.dll
* System.Runtime.Serialization.Xml.dll
* System.Security.AccessControl.dll
* System.Security.Claims.dll
* System.Security.Cryptography.Algorithms.dll
* System.Security.Cryptography.Cng.dll
* System.Security.Cryptography.Csp.dll
* System.Security.Cryptography.DeriveBytes.dll
* System.Security.Cryptography.Encoding.dll
* System.Security.Cryptography.Encryption.Aes.dll
* System.Security.Cryptography.Encryption.dll
* System.Security.Cryptography.Encryption.ECDiffieHellman.dll
* System.Security.Cryptography.Encryption.ECDsa.dll
* System.Security.Cryptography.Hashing.Algorithms.dll
* System.Security.Cryptography.Hashing.dll
* System.Security.Cryptography.OpenSsl.dll
* System.Security.Cryptography.Pkcs.dll
* System.Security.Cryptography.Primitives.dll
* System.Security.Cryptography.ProtectedData.dll
* System.Security.Cryptography.RandomNumberGenerator.dll
* System.Security.Cryptography.RSA.dll
* System.Security.Cryptography.X509Certificates.dll
* System.Security.dll
* System.Security.Principal.dll
* System.Security.Principal.Windows.dll
* System.Security.SecureString.dll
* System.ServiceModel.dll
* System.ServiceModel.Duplex.dll
* System.ServiceModel.Http.dll
* System.ServiceModel.Internals.dll
* System.ServiceModel.NetTcp.dll
* System.ServiceModel.Primitives.dll
* System.ServiceModel.Security.dll
* System.ServiceModel.Web.dll
* System.ServiceProcess.ServiceController.dll
* System.Text.Encoding.CodePages.dll
* System.Text.Encoding.dll
* System.Text.Encoding.Extensions.dll
* System.Text.RegularExpressions.dll
* System.Threading.AccessControl.dll
* System.Threading.dll
* System.Threading.Overlapped.dll
* System.Threading.Tasks.dll
* System.Threading.Tasks.Parallel.dll
* System.Threading.Thread.dll
* System.Threading.ThreadPool.dll
* System.Threading.Timer.dll
* System.Transactions.dll
* System.ValueTuple.dll
* System.Web.Services.dll
* System.Windows.dll
* System.Xml.dll
* System.Xml.Linq.dll
* System.Xml.ReaderWriter.dll
* System.Xml.Serialization.dll
* System.Xml.XDocument.dll
* System.Xml.XmlDocument.dll
* System.Xml.XmlSerializer.dll
* System.Xml.XPath.dll
* System.Xml.XPath.XDocument.dll
* System.Xml.XPath.XmlDocument.dll
* System.Xml.Xsl.Primitives.dll
* Xamarin
* Xamarin.Android.NUnitLite.dll
* Xamarin.iOS.dll
* Xamarin.Mac.dll
* Xamarin.Mac.registrar.full.a
* Xamarin.Mac.registrar.mobile.a
* Xamarin.TVOS.dll
* Xamarin.TVOS.registrar.a
* Xamarin.WatchOS.dll
* Xamarin.WatchOS.registrar.a
* Xamarin-debug
* XamMac.CFNetwork.dll
* XamMac.dll
* XamMacLauncher
****

[Top of Page](#top)
