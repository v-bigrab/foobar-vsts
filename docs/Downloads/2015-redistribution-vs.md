---
redirect_url: /productinfo/2015-redistribution-vs
---

# Distributable Code for Microsoft Visual Studio 2015 and Microsoft Visual Studio 2015 SDK (Includes Utilities and BuildServer Files)
#### Last updated: August 2016

## On this Page
* [Distributable Code Files for Visual Studio 2015](#VisualStudio)
* [Distributable Code Files for the Concurrency Visualizer Software Development Kit](#concurrency)
* [Distributable Code Files for Visual Studio 2015 SDK](#SDK)
* [List of Utilities for Visual Studio 2015](#util)
* [List of BuildServer Files for Visual Studio 2015](#bldsrv)
* [List of Application Insights Files](#AI)

**Note:** In the lists below, [arch] represents the processor architecture identifier, for instance "x86", "x64", or "arm". 
[locale] represents a specific language, locale, or culture identifier, for instance "ENU", "en-us", or "1033".  

## <a id="VisualStudio"> </a>Distributable Code Files for Visual Studio 2015
The following section is the "REDIST list" that is referenced in the "Distributable Code" section of the Microsoft Software License Terms for 
Visual Studio Enterprise 2015, Visual Studio Professional 2015, Visual Studio Community 2015, Visual Studio Express For Windows, 
Visual Studio Express For Windows Desktop, and Visual Studio Express For Web Editions ("the software"). 
If you have a validly licensed copy of such software, you may copy and distribute with your program the unmodified form of the files listed below, subject to the License Terms for the software.

### ASP.NET Libraries
The following software components are licensed and supported separately under the Microsoft .NET Library terms located at http://www.microsoft.com/web/webpi/eula/aspnetcomponent_rtw_enu.htm. If you do not agree to the license terms for these software components, you may not use them.  

MVC  
Web API  
Web Pages with Razor  
Entity Framework  
SignalR  
Katana  
Microsoft XML Document Transformation  

### Microsoft Azure
#### Source
MobileServices.js  
MobileServices.min.js  

#### Object Code
Microsoft.WindowsAzure.Mobile.dll  
Microsoft.WindowsAzure.Mobile.resources.dll  
Microsoft.WindowsAzure.Mobile.UI.dll  
Microsoft.WindowsAzure.Ext.dll  

### Blend and XAML Designers for Visual Studio

#### Blend Project and Item Templates for Visual Studio
Contents under  
C:\Program Files (x86)\Microsoft Visual Studio 14.0\Common7\IDE\ProjectTemplates  
C:\Program Files (x86)\Microsoft Visual Studio 14.0\Common7\IDE\ItemTemplates  
C:\Program Files (x86)\Microsoft Visual Studio 14.0\DesignTools\AppThemes  
C:\Program Files (x86)\MSBuild\Microsoft\Expression\Blend\Silverlight\  
C:\Program Files (x86)\MSBuild\Microsoft\Expression\Blend\.NETFramework  

#### Behaviors Runtime for XAML
C:\Program Files (x86)\Microsoft SDKs\Windows\v8.1\ExtensionSDKs\BehaviorsXamlSDKManaged\12.0  
\SDKManifest.xml  
\Redist\CommonConfiguration\Neutral\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.pri  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.pri  
\References\CommonConfiguration\Neutral\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.dll  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.dll  
\References\CommonConfiguration\Neutral\\[locale]\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.dll  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.dll  

C:\Program Files (x86)\Microsoft SDKs\Windows\v8.1\ExtensionSDKs\BehaviorsXamlSDKNative\12.0  
\SDKManifest.xml  
\Redist\CommonConfiguration\\[arch]\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.dll  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.dll  
\Redist\CommonConfiguration\Neutral\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.pri  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.pri  
\References\CommonConfiguration\Neutral\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.winmd  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.winmd  
\References\CommonConfiguration\Neutral\\[locale]\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.xml  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.xml  

#### Behaviors Runtime for Phone XAML
C:\Program Files (x86)\Microsoft SDKs\WindowsPhoneApp\v8.1\ExtensionSDKs\BehaviorsXamlSDKManaged\12.0  
\SDKManifest.xml  
\Redist\CommonConfiguration\Neutral\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.pri  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.pri  
\References\CommonConfiguration\Neutral\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.dll  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.dll  
\References\CommonConfiguration\Neutral\\[locale]\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.xml  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.xml  
C:\Program Files (x86)\Microsoft SDKs\WindowsPhoneApp\v8.1\ExtensionSDKs\BehaviorsXamlSDKNative\12.0  
\SDKManifest.xml  
\Redist\CommonConfiguration\\[arch]\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.dll  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.dll  
\Redist\CommonConfiguration\Neutral\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.pri  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.pri  
\References\CommonConfiguration\Neutral\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.winmd  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.winmd  
\References\CommonConfiguration\Neutral\\[locale]\  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactions.xml  
&nbsp;&nbsp;&nbsp; Microsoft.Xaml.Interactivity.xml  

#### Blend for Visual Studio

Redistributable files from Blend for Visual Studio are installed in the following locations:  

C:\Program files (x86)\Microsoft SDKs\Expression\Blend\Windows Phone\v8.0  
C:\Program files (x86)\Microsoft SDKs\Expression\Blend\.NETFramework\v4.0   
C:\Program files (x86)\Microsoft SDKs\Expression\Blend\.NETFramework\v4.5  
C:\Program files (x86)\Microsoft SDKs\Expression\Blend\Silverlight\v5.0  

#### Sample Data Resources
C:\Program Files (x86)\Microsoft Visual Studio 14.0\DesignTools\SampleData

### Microsoft Visual Basic PowerPacks
vb\_vbpowerpacks.exe

### LightSwitch 
ajax-loader.gif  
dark-theme-2.0.0.css  
dark-theme-2.5.3.css  
datajs-1.1.3.js  
datajs-1.1.3.min.js  
icons-18-black.png  
icons-18-white.png  
icons-36-black.png  
icons-36-white.png  
jquery.mobile.structure-1.3.0.css  
jquery.mobile.structure-1.3.0.min.css  
jquery.mobile.theme-1.3.0.css  
jquery.mobile.theme-1.3.0.min.css  
jquery.mobile-1.3.0.css  
jquery.mobile-1.3.0.js  
jquery.mobile-1.3.0.min.css  
jquery.mobile-1.3.0.min.js  
jquery.mobile-1.3.0-vsdoc.js  
jquery-1.9.1.intellisense.js  
jquery-1.9.1.js  
jquery-1.9.1.min.js  
light-theme-2.0.0.css  
light-theme-2.5.3.css  
Microsoft.CSharp.dll  
Microsoft.Data.Edm.dll  
Microsoft.Data.Edm.SL.dll  
Microsoft.Data.OData.dll  
Microsoft.Data.OData.SL.dll  
Microsoft.Data.Services.Client.dll  
Microsoft.Data.Services.Client.SL.dll  
Microsoft.Data.Services.dll  
Microsoft.IdentityModel.dll  
Microsoft.IdentityModel.Extensions.dll  
Microsoft.LightSwitch.AppBridge.dll  
Microsoft.LightSwitch.Base.Client.dll  
Microsoft.LightSwitch.Client.dll  
Microsoft.LightSwitch.Client.Internal.dll  
Microsoft.LightSwitch.CodeMarker.dll  
Microsoft.LightSwitch.CodeMarker.dll  
Microsoft.LightSwitch.Cosmopolitan.Client.dll  
Microsoft.LightSwitch.dll  
Microsoft.LightSwitch.dll  
Microsoft.LightSwitch.ExportProvider.dll  
Microsoft.LightSwitch.ExportProvider.dll  
Microsoft.LightSwitch.Extensions.Client.dll  
Microsoft.LightSwitch.Extensions.Design.Client.dll  
Microsoft.LightSwitch.Extensions.Server.dll  
Microsoft.LightSwitch.ManifestService.Client.dll  
Microsoft.LightSwitch.ManifestService.dll  
Microsoft.LightSwitch.Model.Xaml.Client.dll  
Microsoft.LightSwitch.Model.Xaml.dll  
Microsoft.LightSwitch.RuntimeEditor.Internal.dll  
Microsoft.LightSwitch.SDKProxy.dll  
Microsoft.LightSwitch.Server.dll  
Microsoft.LightSwitch.Server.Host.dll  
Microsoft.LightSwitch.Server.Manifest.dll  
Microsoft.LightSwitch.Server.Sap.dll  
Microsoft.VisualStudio.Debugger.Runtime.Dll.dll  
msls.js  
msls-2.0.0.css  
msls-2.0.0.js  
msls-2.0.0.min.css  
msls-2.0.0.min.js  
msls-2.0.0-vsdoc.js  
msls-2.5.3.css  
msls-2.5.3.js  
msls-2.5.3.min.css  
msls-2.5.3.min.js  
msls-2.5.3-vsdoc.js  
msls-black-icons-18.png  
msls-black-icons-36.png  
msls-dark-2.0.0.css  
msls-dark-2.5.3.css  
msls-light-2.0.0.css  
msls-light-2.5.3.css  
msls-loader-dark.gif  
msls-loader-light.gif  
msls-white-icons-18.png  
msls-white-icons-36.png  
System.ComponentModel.Composition.dll  
System.ComponentModel.DataAnnotations.dll  
System.ServiceModel.DomainServices.Client.dll  
System.ServiceModel.DomainServices.Client.Web.dll  
System.ServiceModel.DomainServices.EntityFramework.dll  
System.ServiceModel.DomainServices.Hosting.dll  
System.ServiceModel.DomainServices.Hosting.OData.dll  
System.ServiceModel.DomainServices.Server.dll  
System.ServiceModel.Extensions.dll    
System.ServiceModel.PollingDuplex.dll    
System.ServiceModel.PollingDuplex.dll  
System.ServiceModel.Web.Extensions.dll  
System.Spatial.dll  
System.Spatial.SL.dll  
System.Windows.Controls.Data.dll  
System.Windows.Controls.Data.Input.dll  
System.Windows.Controls.dll  
System.Windows.Controls.DomainServices.dll  
System.Windows.Controls.Input.dll  
System.Windows.Controls.Navigation.dll  
System.Windows.Data.dll  
System.Xml.Linq.dll  
System.Xml.Serialization.dll  
user-customization.css  
user-logo.png  
user-splash-screen.png  
winjs-1.0.0.js  
winjs-1.0.0.min.js  

### .NET Framework 4.6
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:    

#### Web Installer  
dotNetFx-Web.exe  
NDP46-KB3006565-Web.exe  

#### Offline Installer  
dotNetFx-x86-x64-AllOS-ENU.exe  
NDP46-KB3006563-x86-x64-AllOS-ENU.exe  

**Note:** Both files are identical but may use different names for different distribution channels.  
 
#### Language Packs  
dotNetFx-x86-x64-AllOS-[locale].exe  
NDP46-KB3006563-x86-x64-AllOS-[locale].exe  

**Note:** Both files are identical but may use different names for different distribution channels.  

Language Packs are available for the following locales (listed here with their associated identifier code): 
Arabic (ARA), Chinese-Taiwan (CHT), Czech (CSY), Danish (DAN), German (DEU), Greek (ELL), Finnish (FIN), 
French (FRA), Hebrew (HEB), Hungarian (HUN), Italian (ITA), Japanese (JPN), Korean (KOR), Dutch-Netherlands (NLD), 
Norwegian (NOR), Polish (PLK), Portuguese-Brazil (PTB), Russian (RUS), Swedish (SVE), Turkish (TRK), Chinese (CHS), 
Portuguese-Portugal (PTG), and Spanish (ESN).

### F# Runtime
Fsharp.Core.dll  

### ADO.NET
Subject to the License Terms for the software, you may copy and distribute the following .dll files, unmodified, with your program:  

System.Data.dll  
System.Data.DatasetExtensions.dll  
System.Data.OracleClient.dll  
Adonetdiag.dll  

### Visual C++ Runtime
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:  

\VC\redist\\[locale]\vcredist\_arm.exe  
\VC\redist\\[locale]\vcredist\_x64.exe    
\VC\redist\\[locale]\vcredist\_x86.exe  

Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, as a part of the installation package of your program:  
C:\Program Files (x86)\Common Files\Merge Modules\  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_CRT\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_CRT\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_CRT\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_CXXAMP\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_CXXAMP\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_CXXAMP\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_OpenMP\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_OpenMP\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC110\_OpenMP\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_CRT\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_CRT\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_CRT\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_CXXAMP\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_CXXAMP\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_CXXAMP\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_OpenMP\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_OpenMP\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC120\_OpenMP\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_CRT\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_CRT\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_CRT\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_CXXAMP\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_CXXAMP\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_CXXAMP\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_MFCLOC\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_MFCLOC\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_MFC\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_MFC\_x86.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_OpenMP\_arm.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_OpenMP\_x64.msm  
&nbsp;&nbsp;&nbsp; Microsoft\_VC140\_OpenMP\_x86.msm  

These files can be run as prerequisites during installation.

#### Visual C++ Runtime Files
Subject to the License Terms for the software, you may copy and distribute with your program any of the files within the followng folder and its subfolders except as noted below. You may not modify these files.
* C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\redist

You may not distribute the contents of the following folders:  
* C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\redist\debug\_nonredist
* C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\redist\onecore\debug\_nonredist

Subject to the License Terms for the software, you may copy and distribute the following files with your program in your program’s application local folder or by deploying them into the Global Assembly Cache (GAC):

VC\atlmfc\lib\mfcmifc80.dll  
VC\atlmfc\lib\amd64\mfcmifc80.dll  

### Universal Windows Apps and Windows Store Apps
**Windows Phone 8.0 Apps**
C:\Program Files (x86)\Microsoft SDKs\Windows Phone\v8.0\ExtensionSDKs\CppUnitTestFramework\11.0\Redist\CommonConfiguration
C:\Program Files (x86)\Microsoft SDKs\Windows Phone\v8.0\ExtensionSDKs\TestPlatform\11.0\Redist\CommonConfiguration

**Side-loading of Windows 8.1 Store Apps**
The AppX and DLL files downloaded from the following location can be distributed unmodified with your Windows Store 8.1 apps that you intend to side-load:
http://download.microsoft.com/download/5/F/0/5F0F8404-9329-44A9-8176-ED6F7F746F25/VCLibs_Redist_Packages.zip
* C:\Program Files (x86)\Microsoft SDKs\Windows Phone\v8.1\ExtensionSDKs\Microsoft.VCLibs\12.0\AppX\Retail
* C:\Program Files (x86)\Microsoft SDKs\WindowsPhoneApp\v8.1\ExtensionSDKs\Microsoft.VCLibs\12.0\AppX\Retail
* C:\Program Files (x86)\Microsoft SDKs\WindowsPhoneApp\v8.1\ExtensionSDKs\CppUnitTestFramework\12.0\Redist\CommonConfiguration
* C:\Program Files (x86)\Microsoft SDKs\WindowsPhoneApp\v8.1\ExtensionSDKs\CppUnitTestFramework\14.0\Redist\CommonConfiguration
* C:\Program Files (x86)\Microsoft SDKs\WindowsPhoneApp\v8.1\ExtensionSDKs\TestPlatform\14.0\Redist\CommonConfiguration

**Side-loading of Universal Windows Apps**
The AppX files contained in the following locations can be distributed unmodified with your Universal Windows apps that you intend to side-load:
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.VCLibs\14.0\Appx\Retail
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.VCLibs.120\14.0\Appx\Retail
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\CppUnitTestFramework.Universal\14.0\Redist\CommonConfiguration
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\MSTestFramework.Universal\14.0\Redist\CommonConfiguration
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\TestPlatform.Universal\14.0\Redist\CommonConfiguration
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.NET.Native.Framework.1.2\1.2\\[arch]\ret\Native
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.NET.Native.Framework.1.3\1.3\\[arch]\ret\Native
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.NET.Native.Runtime.1.1\1.1\AppX\\[arch]
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.NET.Native.Runtime.1.3\1.3\AppX\\[arch]
* C:\Program Files (x86)\Microsoft SDKs\Windows Kits\10\ExtensionSDKs\Microsoft.NET.Native.Runtime.1.4\1.4\AppX\\[arch]



#### Microsoft Windows Phone SDK 8.0  and Microsoft Windows Phone SDK 8.1

This is the "REDIST list" that is referenced in the "Distributable Code" section of the Microsoft Software License Terms for Microsoft Windows Phone SDK 8.0 
and Microsoft Windows Phone SDK 8.1 ("the software"). If you have a validly licensed copy of the software, you may copy and distribute the files listed below, 
unmodified, subject to the License Terms for the software.

##### **Microsoft XNA Game Studio 4.0**
Andyb.ttf  
JingJing.ttf  
Kooten.ttf  
Linds.ttf  
Miramo.ttf  
Miramob.ttf  
Moire-Bold.ttf  
Moire-ExtraBold.ttf  
Moire-Light.ttf  
Moire-Regular.ttf  
MotorwerkOblique.ttf  
NGO\_\_\_\_\_.ttf  
NGOB\_\_\_\_.ttf  
OcraExt.ttf  
Peric.ttf  
Pericl.ttf  
Pesca.ttf  
Pescab.ttf  
QuartMS.ttf  
SegoeKeycaps.ttf  
Segoepr.ttf  
Segoeprb.ttf  
egoeUIMono-Bold.ttf  
SegoeUIMono-Regular.ttf  
Wscsnbd.ttf  
Wscsnbdit.ttf  
Wscsnit.ttf  
Wscsnrg.ttf  

##### **Windows Phone Assemblies**

DoneListeningEarcon.wav  
ListeningEarcon.wav  
Microsoft.Phone.Controls.dll  
Microsoft.Phone.Controls.Maps.dll

##### **Windows Phone icon files**

The files contained in the following locations may be distributed unmodified with your Windows Phone apps:  
%programfiles%\Microsoft SDKs\Windows Phone\v8.0\Icons\Dark
%programfiles%\Microsoft SDKs\Windows Phone\v8.0\Icons\Light  
%programfiles%\Microsoft SDKs\Windows Phone\v8.1\Icons\Dark
%programfiles%\Microsoft SDKs\Windows Phone\v8.1\Icons\Light  

The following files may be distributed unmodified with your Windows Phone apps:
appbar.add.rest.png  
appbar.back.rest.png  
appbar.basecircle.rest.png  
appbar.cancel.rest.png  
appbar.check.rest.png  
appbar.close.rest.png  
appbar.delete.rest.png  
appbar.download.rest.png  
appbar.edit.rest.png  
appbar.favs.addto.rest.png  
appbar.favs.rest.png  
appbar.feature.camera.rest.png  
appbar.feature.email.rest.png  
appbar.feature.search.rest.png  
appbar.feature.settings.rest.png  
appbar.feature.video.rest.png  
appbar.folder.rest.png  
appbar.minus.rest.png  
appbar.new.rest.png  
appbar.next.rest.png  
appbar.overflowdots.png  
appbar.questionmark.rest.png  
appbar.refresh.rest.png  
appbar.save.rest.png  
appbar.share.rest.png  
appbar.stop.rest.png  
appbar.sync.rest.png  
appbar.transport.ff.rest.png  
appbar.transport.pause.rest.png  
appbar.transport.play.rest.png  
appbar.transport.rew.rest.png  
appbar.upload.rest.png  

#### Microsoft Advertising SDK for Windows Phone

Microsoft.Advertising.Mobile.dll  
Microsoft.Advertising.Mobile.resources.dll  
Microsoft.Advertising.Mobile.UI.dll  
Microsofot.Advertising.Mobile.XNA.dll  


### SQL Server Database Tooling files
Subject to the License Terms for the software, you may copy and distribute the .dll files and .exe files, unmodified, in this folder with your program:  

Common7\IDE\Extensions\Microsoft\SQLDB\DAC\120
Common7\IDE\Extensions\Microsoft\SQLDB\DAC\130

### SQL Server Redistributable Components
Subject to the License Terms for the software, you may copy and distribute the .MSI and .EXE files, unmodified, with your program:  

SqlCmdLnUtils.msi  
sqlncli.msi  
SSCERuntime\_x64-enu.exe  
SSCERuntime\_x86-enu.exe  
sqllocaldb.msi  
SharedManagementObjects.msi  
SqlDom.msi  
SQLSysClrTypes.msi  
TSqlLanguageService.msi  

### Microsoft WCF Data Services files
Subject to the License Terms for the software, you may copy and distribute the following .dll files, unmodified, with your program:  

Microsoft.Data.Services.dll  
Microsoft.Data.Services.Client.dll  
Microsoft.Data.OData.dll  
Microsoft.Data.Edm.dll  
System.Spatial.dll  


## <a id="concurrency"> </a> Distributable Code Files for the Concurrency Visualizer Software Development Kit
Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program:

Microsoft.ConcurrencyVisualizer.Markers.dll (for .NET 3.5)  
Microsoft.ConcurrencyVisualizer.Markers.dll (for .NET 4.0)  
cvmarkers.h  
cvmarkersobj.h  


## <a id="SDK"> </a>Distributable Code Files for Visual Studio 2015 SDK

This is the "REDIST list" that is referenced in the "Distributable Code" section of the Microsoft Software License Terms for the Microsoft Visual Studio 2015 Software Development Kit ("the software"). If you have a validly licensed copy of the software, you may copy and distribute the unmodified object code form of the files listed below, subject to the License Terms for the software.

vs120\_piaredist.exe  
vs\_isoshell.exe  
vs\_isoshellLP.exe  
vs\_intshelladditional.exe  
vs\_intshelladditionalLP.exe


## <a id="util"> </a>List of Utilities for Visual Studio 2015

This is the “Utilities List” that is referenced in the “Utilities” section of Microsoft Software License Terms for certain editions of Visual Studio 2015 (the “software”). Depending on the specific edition of the software, the software you received may not include all of the files on this list. To determine your rights with respect to the following files, please refer to the Visual Studio License Terms that came with your edition of the software.

Visual Studio IntelliTrace Standalone Collector  
IntelliTraceCollection.cab  
Visual Studio Concurrency Visualizer  
concvi\_standalonecollection.exe  
Visual Studio Remote Tools  
rtools\_setup\_x86.exe  
rtools\_setup\_x64.exe  
rtools\_setup\_arm.exe  
Visual Studio Standalone Profiler  
vs\_profiler\_x64\_\*.exe  
vs\_profiler\_x86\_\*.exe  
\VC\redist\Debug\_NonRedist\arm\Microsoft.VC120.DebugCRT\msvcp120d.dll  
\VC\redist\Debug\_NonRedist\arm\Microsoft.VC120.DebugCRT\msvcr120d.dll  
\VC\redist\Debug\_NonRedist\arm\Microsoft.VC120.DebugCRT\vccorlib120d.dll  
\VC\redist\Debug\_NonRedist\arm\Microsoft.VC120.DebugCXXAMP\vcamp120d.dll  
\VC\redist\Debug\_NonRedist\arm\Microsoft.VC120.DebugOPENMP\vcomp120d.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugCRT\msvcp120d.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugCRT\msvcr120d.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugCRT\vccorlib120d.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugCXXAMP\vcamp120d.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugMFC\mfc120d.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugMFC\mfc120ud.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugMFC\mfcm120d.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugMFC\mfcm120ud.dll  
\VC\redist\Debug\_NonRedist\x64\Microsoft.VC120.DebugOpenMP\vcomp120d.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugCRT\msvcp120d.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugCRT\msvcr120d.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugCRT\vccorlib120d.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugCXXAMP\vcamp120d.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugMFC\mfc120d.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugMFC\mfc120ud.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugMFC\mfcm120d.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugMFC\mfcm120ud.dll  
\VC\redist\Debug\_NonRedist\x86\Microsoft.VC120.DebugOpenMP\vcomp120d.dll  
\VC\redist\GraphicsDbgRedist\ARM\VsGraphicsHelper.dll  
\VC\redist\GraphicsDbgRedist\ARM\\[locale]\VsGraphicsResources.dll    
\VC\redist\GraphicsDbgRedist\X64\VsGraphicsHelper.dll    
\VC\redist\GraphicsDbgRedist\X64\\[locale]\VsGraphicsResources.dll    
\VC\redist\GraphicsDbgRedist\X86\VsGraphicsHelper.dll    
\VC\redist\GraphicsDbgRedist\X86\\[locale]\VsGraphicsResources.dll   
\VC\bin\arm\\[locale]\pgort120ui.dll  
\VC\bin\arm\pgort120.dll  
\VC\bin\arm\pgosweep.exe  

## <a id="bldsrv"> </a>List of BuildServer Files for Visual Studio 2015
This is the "BUILDSERVER list" that is referenced in the "BUILDSERVER.TXT File" section of the Microsoft Software License Terms for certain editions of Visual Studio 2015 (the "software"). To determine your rights with respect to the following files, please refer to the License Terms that came with your edition of the software.

### SharePoint Tooling for Visual Studio 2012
Program Files(86)\MsBuild\Microsoft\Visual Studio\v11.0\SharePointTools\  
&nbsp;&nbsp;&nbsp; Microsoft.VisualStudio.SharePoint.targets  
&nbsp;&nbsp;&nbsp; Microsoft.VisualStudio.SharePoint.Tasks.dll  

Windows\Microsoft.NET\assembly\GAC\_MSIL\  
&nbsp;&nbsp;&nbsp; Microsoft.VisualStudio.SharePoint.Designers.Models.dll  
&nbsp;&nbsp;&nbsp; Microsoft.VisualStudio.SharePoint.Designers.Models.Features.dll  
&nbsp;&nbsp;&nbsp; Microsoft.VisualStudio.SharePoint.Designers.Models.Packages.dll  
&nbsp;&nbsp;&nbsp; Microsoft.VisualStudio.SharePoint.dll  

### Visual C++ BuildServer files

All files in the following folders (and all files and folders within these folders, recursively)

Program Files\Common Files\Merge Modules
Program Files\Microsoft Visual Studio 14.0\VC\  
Program Files\Microsoft Visual Studio 14.0\Common7\Tools\ProjectComponents  
Program Files\MSBuild\Microsoft.Cpp\v4.0\V140\  

**Individual Files**

Program Files\Microsoft Visual Studio 14.0\Common7\IDE\msobj140.dll  
Program Files\Microsoft Visual Studio 14.0\Common7\IDE\msvcdis140.dll  
Program Files\Microsoft Visual Studio 14.0\Common7\Tools\makehm.exe  
Program Files\Microsoft Visual Studio 14.0\Common7\Tools\VCVarsQueryRegistry.bat  
Program Files\Microsoft Visual Studio 14.0\Common7\Tools\vsvars32.bat  

### Light Switch BuildServer files
Microsoft.Data.Schema.dll  
Microsoft.Data.Schema.ScriptDom.dll  
Microsoft.Data.Schema.ScriptDom.Sql.dll  
Microsoft.Data.Schema.Sql.dll  
Microsoft.Data.Schema.Utilities.dll  
Microsoft.LightSwitch.AppBridge.dll  
Microsoft.LightSwitch.Base.Client.dll  
Microsoft.LightSwitch.Base.Server.dll  
Microsoft.LightSwitch.Build.Publish.targets  
Microsoft.LightSwitch.Build.Tasks.dll  
Microsoft.LightSwitch.Build.Tasks.targets  
Microsoft.LightSwitch.Client.dll  
Microsoft.LightSwitch.Client.Internal.dll  
Microsoft.LightSwitch.Client.Internal.Resources.dll  
Microsoft.LightSwitch.Client.Resources.dll  
Microsoft.LightSwitch.CodeMarker.dll  
Microsoft.LightSwitch.CommandLineBuild.Manifest.dll  
Microsoft.LightSwitch.CommandLineBuildLoader.dll  
Microsoft.LightSwitch.Common.targets  
Microsoft.LightSwitch.Deploy.Provider.dll  
Microsoft.LightSwitch.Design.CodeGen.dll  
Microsoft.LightSwitch.Design.CodeGen.Internal.dll  
Microsoft.LightSwitch.Design.Core.dll  
Microsoft.LightSwitch.Design.Core.Internal.dll  
Microsoft.LightSwitch.Design.DataAccess.dll  
Microsoft.LightSwitch.Design.DataAccess.Internal.dll  
Microsoft.LightSwitch.Design.Designer.dll  
Microsoft.LightSwitch.Design.Designer.Extensions.dll  
Microsoft.LightSwitch.Design.Designer.Framework.dll  
Microsoft.LightSwitch.Design.Designer.Internal.dll  
Microsoft.LightSwitch.Design.DesignerWpfUtilities.dll  
Microsoft.LightSwitch.Design.dll  
Microsoft.LightSwitch.Design.Extensions.Internal.dll  
Microsoft.LightSwitch.Design.Extensions.Reader.dll  
Microsoft.LightSwitch.Design.Extensions.Reader.Internal.dll  
Microsoft.LightSwitch.Design.Internal.dll  
Microsoft.LightSwitch.Design.Loader.dll  
Microsoft.LightSwitch.Design.Manifest.dll  
Microsoft.LightSwitch.Design.Package.dll  
Microsoft.LightSwitch.Design.PackageUI.Neutral.dll  
Microsoft.LightSwitch.Design.Project.dll  
Microsoft.LightSwitch.Design.Project.Upgrade.dll  
Microsoft.LightSwitch.Design.Project.Upgrade.Internal.dll  
Microsoft.LightSwitch.Design.Publish.dll  
Microsoft.LightSwitch.Design.Publish.Internal.dll  
Microsoft.LightSwitch.Design.Server.Internal.dll  
Microsoft.LightSwitch.Design.Utilities.dll  
Microsoft.LightSwitch.Design.VSTemplateWizard.dll  
Microsoft.LightSwitch.Design.WpfUtils.dll  
Microsoft.LightSwitch.dll  
Microsoft.LightSwitch.ExportProvider.dll  
Microsoft.LightSwitch.ExportProvider.Resources.dll  
Microsoft.LightSwitch.ManifestService.Client.dll  
Microsoft.LightSwitch.ManifestService.Client.Resources.dll  
Microsoft.LightSwitch.ManifestService.dll  
Microsoft.LightSwitch.Model.Xaml.Client.dll
Microsoft.LightSwitch.Model.Xaml.Client.Resources.dll  
Microsoft.LightSwitch.Model.Xaml.dll  
Microsoft.LightSwitch.Publish.targets  
Microsoft.LightSwitch.Publish.Tasks.dll  
Microsoft.LightSwitch.Resources.dll  
Microsoft.LightSwitch.RuntimeEditor.Internal.dll  
Microsoft.LightSwitch.RuntimeEditor.Internal.Resources.dll  
Microsoft.LightSwitch.SDK.BuildTasks.dll  
Microsoft.LightSwitch.SDK.targets  
Microsoft.LightSwitch.SDKProxy.dll  
Microsoft.LightSwitch.SecurityData.svc  
Microsoft.LightSwitch.Server.dll  
Microsoft.LightSwitch.Server.Host.dll  
Microsoft.LightSwitch.Server.Internal.dll  
Microsoft.VisualStudio.Debugger.Runtime.dll.dll  
Microsoft.VisualStudio.ExtensionManager.dll
Microsoft.VisualStudio.Settings.11.0.dll  
Microsoft.VisualStudio.Shell.11.0.dll  
Microsoft.VisualStudio.Shell.Interop.9.0.dll  
Microsoft.VisualStudio.TextTemplating.11.0.dll  
Microsoft.Web.Deployment.dll  
Microsoft.Web.Publishing.AllFilesInTheProject.targets  
Microsoft.Web.Publishing.AspNetCompileMerge.targets  
Microsoft.Web.Publishing.Deploy.FileSystem.targets  
Microsoft.Web.Publishing.Deploy.FPSE.targets  
Microsoft.Web.Publishing.Deploy.FTP.targets  
Microsoft.Web.Publishing.Deploy.MsDeploy.targets  
Microsoft.Web.Publishing.Deploy.Package.targets  
Microsoft.Web.Publishing.MsDeploy.Common.targets  
Microsoft.Web.Publishing.OnlyFilesToRunTheApp.targets  
Microsoft.Web.Publishing.targets  
Microsoft.Web.Publishing.Tasks.dll  
Microsoft.WebApplication.Build.Tasks.Dll  
Microsoft.WebApplication.targets  
Microsoft.WindowsAzure.ServiceRuntime.dll  
Microsoft.WindowsAzure.StorageClient.dll  
System.ServiceModel.PollingDuplex.dll  
vslsHost.exe  

## <a id="AI"> </a>Distributable Code Files for Application Insights for Visual Studio 2015

Subject to the License Terms for the software, you may copy and distribute the following files, unmodified, with your program built with Visual Studio 2015:

Microsoft.ApplicationInsights.2.0.0.nupkg  
Microsoft.ApplicationInsights.Agent.Intercept.1.2.1.nupkg  
Microsoft.ApplicationInsights.AspNet.1.0.0-rc1-update4.nupkg  
Microsoft.ApplicationInsights.AspNetCore.1.0.0-rc2-final.nupkg  
Microsoft.ApplicationInsights.DependencyCollector.2.0.0.nupkg  
Microsoft.ApplicationInsights.JavaScript.0.22.9-build00167.nupkg  
Microsoft.ApplicationInsights.PerfCounterCollector.2.0.0.nupkg  
Microsoft.ApplicationInsights.Web.2.0.0.nupkg  
Microsoft.ApplicationInsights.WindowsServer.2.0.0.nupkg  
Microsoft.ApplicationInsights.WindowsServer.TelemetryChannel.2.0.0.nupkg  
Microsoft.Bcl.Async.1.0.168.nupkg  
Microsoft.Diagnostics.Tracing.EventSource.Redist.1.1.24.nupkg  

