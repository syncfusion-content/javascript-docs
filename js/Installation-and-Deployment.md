---
layout: post
title: Installation and Deployment of Syncfusion Essential JS 
description: Learn how to download and set up Essential JS for development on Windows, Mac & Linux machines. 
platform: js
control: Introduction
documentation: ug
---

# Installation and Deployment

## For Windows Users

Download and install the **Essential Studio for JavaScript** setup from this [link](http://www.syncfusion.com/downloads/javascript) after logging in with your Syncfusion account. Licensed customers can download the install from the [downloads](http://www.syncfusion.com/support/directtrac/downloads) section.

### Install Location

The installer copies the required scripts, stylesheets and samples into the following location

`(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\`

_For example, if you had chosen to install under `C:\Program Files (x86)`, then navigate to the below location, C:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\_

Within the root `javascript` folder, the `assets` folder contains all the minified versions of scripts along with the [Source Maps](/js/sourcemap) and stylesheets where as the `assets-src` folder contains the uncompressed version of the same files. The assets have been organized in the following folder structure

  * CSS - contains the style sheets for mobile and web components.
  * External - contains the external dependency files such as jQuery, jquery.easing etc.
  * Scripts - includes all the necessary widget scripts as well as culture scripts for Syncfusion Essential JS components.
  * TypeScript - includes the default type-definition file `ej.widgets.all.d.ts`.

## For Mac and Linux Users

**Mac** and **Linux** users can download all the necessary files in a zip archive from this [link](http://www.syncfusion.com/downloads/javascript) after logging in with your Syncfusion account. Licensed customers can download the archive from the [downloads](http://www.syncfusion.com/support/directtrac/downloads) section.

The assets have been organized in the following folder structure

* Assets – contains all the necessary scripts and stylesheets.
* External – contains the external dependency files such as jQuery, jquery.easing etc.
* Samples  – contains sample code that demonstrate usage of all the components.


N>   **Mac** and **Linux** users will not be able to use the **Reporting and Business Intelligence** components since the controls have a server-side .NET dependency.
N>  Also, the exporting functionality available in some of the widgets like the grid will also not be available due to the server-side .NET dependencies.


## Configuring Syncfusion NuGet Packages in Visual Studio 

Syncfusion JavaScript NuGet packages are available [here](http://nuget.syncfusion.com/package/javascript).

### NuGet Configuration  

The steps to install the Syncfusion JavaScript NuGet Packages in Visual Studio are as follows,

1. In Visual Studio, navigate to `Tools | NuGet Package Manager | Package Manager Settings`, the options dialog will appear on the screen as shows below,

   ![](Installation-and-Deployment_images/NuGetConfig1.jpeg)

2. Select `NuGet Package Manager | Package Sources` and click `Add` button to add the `Package Name` and `Package Source` of Syncfusion NuGet Packages.    

   **Name**: Name of the package that listed in Available package sources  
   **Source**: Syncfusion JavaScript NuGet Package feed URL 
   [http://nuget.syncfusion.com/javascript](http://nuget.syncfusion.com/javascript)
    
   ![](Installation-and-Deployment_images/NuGetConfig2.jpeg)

   N> The `Source` text box in the above image denotes the location of the NuGet packages and the `Name` section, allows you to provide a unique name for NuGet Packages Source.
    
I> Syncfusion other platforms NuGet packages feed links are available [here](http://nuget.syncfusion.com/)

### NuGet Installation

Syncfusion JavaScript NuGet can install once configured the package source. The NuGet installation steps as below,

1. Once configured the Package source with Syncfusion NuGet Packages, right click on project and choose `Manage NuGet Packages | Online | <Package Source Name>`.

   ![](Installation-and-Deployment_images/NuGetConfig3.jpeg)

2. The NuGet Packages are listed which are available in package source location. Install the required packages to your application by clicking `Install` button.

   N> NuGet packages can be install directly through the **command line** (Package Manager Console). Further details click [here](http://help.syncfusion.com/extension/syncfusion-nuget-packages/nuget-install-and-configuration#install-from-package-manager-console)
   
3. Now you can proceed with the installation. The steps involved in usage within your application is explained in the [Control Initialization](/js/control-initialization#configuring-and-installing-nuget-into-your-project) section.

### Updating a NuGet Package

Using the `Manage NuGet Packages` in Visual Studio, NuGet packages can be update.
 
1. Right click on Project and Navigate to the `Manage NuGet Packages` and click on the `Updates` tab to check for updates.

2. Select the `Updates -> <Syncfusion Package Source>`. Refer to the following screenshot for more information.

   ![](Installation-and-Deployment_images/NuGetConfig4.jpeg)

3. If there is a new version of NuGet you will see it in the list of available updates.

4. Select NuGet Package in the list and click `Update`. When the update is complete, close and re-open all open instances of Visual Studio.

   N> By clicking `Update All` button, all NuGet packages are getting update. When the update is complete, close and re-open all open instances of Visual Studio.


## Configuring Syncfusion Bower Packages

### Overview

[Bower](http://bower.io) is a package manager for the Web. Syncfusion Bower package allows you to use the Syncfusion JavaScript Widgets in an efficient way.

I>Syncfusion JavaScript Bower package is available as [public Git Repository](https://github.com/syncfusion/JavaScript-Widgets) and also registered as Syncfusion-JavaScript in the Bower registry.

### Bower Installation

To configure the Bower in your machine you need to install [node, npm](http://nodejs.org) and [git](http://git-scm.org). For more information to configure the Bower package please refer the official site for [bower](http://bower.io/#install-bower). 
Syncfusion JavaScript Bower package can be configured in the following ways.

1. Using command prompt.

2. Using bower.json file.

3. From local directory.

#### Using command prompt

Perform the below steps to install Syncfusion Bower Package via command prompt in your web application.

1. Open your web project’s location in a command prompt window.

2. Then run the command Bower install <package name>.

   ~~~
   bower install syncfusion-javascript
   ~~~
   
   ![](Installation-and-Deployment_images/Installation-and-Deployment_img5.jpeg)

3. The Bower will install the Syncfusion JavaScript files into the project location to develop with Syncfusion controls.

N>To install a particular version of a Bower package, you need to provide the version as suffix of the package name while installing. For instance, run the below command, Eg: To install the package of version 13.3.0.18. 
N>'bower install Syncfusion-javascript#13.3.0.18'

#### Using bower.json file

In another way, you can add the packages to the bower.json file by simply specify the package name. This will install/restore the packages to your project. Please refer the below image.
 
![](Installation-and-Deployment_images/Installation-and-Deployment_img6.jpeg)

N>ASP.NET 5 (preview) projects have bower.json file by default. If your project doesn’t have bower.json file then run the below command from your project directory by Command prompt. 
N>'bower init'

![](Installation-and-Deployment_images/Installation-and-Deployment_img7.jpeg)

#### From local directory

You can install the Syncfusion Bower package from a local directory. To perform this follow the below steps.

1. Navigate the [Syncfusion JavaScript Bower repository](https://github.com/syncfusion/JavaScript-Widgets/) location on GitHub and download the repository as zip by click the “Download ZIP” button and extract the contents in your computer’s any of the local directory.

   ![](Installation-and-Deployment_images/Installation-and-Deployment_img8.jpeg)

2. Then run the install command by providing the package content’s location. 

   ![](Installation-and-Deployment_images/Installation-and-Deployment_img9.jpeg)

### Bower Update

To update the installed Bower packages, run the command Bower update <package name>.
~~~
bower update syncfusion-javascript
~~~

![](Installation-and-Deployment_images/Installation-and-Deployment_img10.jpeg)

## Configuring Syncfusion npm Packages

### Overview

npm is the Package Manager for JavaScript. npm makes it easy for JavaScript developers to share and reuse the code and it makes it easy to update the code that you're sharing.

### Syncfusion npm package

Syncfusion JavaScript npm package is available as [public Git Repository](https://github.com/syncfusion/JavaScript-Widgets) and also registered as syncfusion-javaScript in the npm registry.

### Syncfusion npm Installation 

To configure the npm,  install the [nodejs](http://nodejs.org/) and update the npm. For more information to configure the npm packages refer the official site of [npm](https://docs.npmjs.com/getting-started/installing-node). 

syncfusion-javascript npm package can be configured in following ways.

1. Using Command prompt

2. Using package.json file.

3. From local directory

#### Using command prompt

Follow the below steps to install Syncfusion JavaScript npm package via command prompt in required web application location.

1. Open project’s location in command prompt window.

2. Run the installation command for npm.

   ~~~
   npm install syncfusion-javascript
   ~~~

   ![](Installation-and-Deployment_images/npminstallationsteps_img1.jpeg)

3. npm install the Syncfusion JavaScript assets into the project location to develop with Syncfusion controls.  

N> As per standard Syncfusion used the 3 digit version for npm packages. To install a particular version of npm package, provide the version as suffix of the package name while installing. For instance, run the below command, 
N> E.g. The below command installs Syncfusion Javascript package of version 14.1.0.46. 
N> 'npm install Syncfusion-javascript@14.1.46'

#### Using package.json file

Add the Syncfusion JavaScript packages to the package.json by simply specify the package name. This will install/restore the package to the Visual Studio project. Refer the below image.

![](Installation-and-Deployment_images/npminstallationsteps_img2.jpeg)

N> ASP.NET 5 (preview) projects have package.json file by default. Visual Studio project doesn’t have package.json file then, run the below command using the project command prompt.  
N> 'npm init'

![](Installation-and-Deployment_images/npminstallationsteps_img3.jpeg)

#### From Local Directory

Install the Syncfusion JavaScript npm package from a local directory.

1. Navigate the [Syncfusion JavaScript repository](https://github.com/syncfusion/JavaScript-Widgets) location on GitHub and download the repository as zip by click the “Download ZIP” button and extract the contents in your computer’s any of the local directory.

   ![](Installation-and-Deployment_images/npminstallationsteps_img4.jpeg)

2. Run the install command by providing the package content location.

   ![](Installation-and-Deployment_images/npminstallationsteps_img5.jpeg)

### npm Update

#### Updating global packages

To update the globally installed npm packages, run the below command to update the package by globally.

~~~
npm install g- syncfusion-javascript
~~~

![](Installation-and-Deployment_images/npminstallationsteps_img6.jpeg)

### Updating local packages

To update the locally installed npm packages, run the below command to update the package by local location.

~~~
npm update
~~~

![](Installation-and-Deployment_images/npminstallationsteps_img7.jpeg)

## Configuring Syncfusion JSPM Packages

### Overview

jspm is a package manager for [SystemJS universal module loader](https://github.com/systemjs/systemjs), built on top of the dynamic [ES6 module loader](https://github.com/ModuleLoader/es6-module-loader). This can load any module format (ES6, AMD, CommonJS and globals) directly from any registry such as npm and GitHub with flat versioned dependency management. Any custom registry endpoints can be created through the Registry API.

### Syncfusion JavaScript JSPM

Syncfusion JavaScript jspm package is available as [public Git Repository](https://github.com/syncfusion/JavaScript-Widgets) and also registered as Syncfusion-JavaScript in the npm registry too.

### Syncfusion jspm Installation 

#### Using Command prompt 

Follow the below steps to install Syncfusion JavaScript jspm package via command prompt in required web application location.

1. Open project’s location in command prompt window.

2. A) To install the Syncfusion JavaScript jspm package via github repository.

   ~~~
   jspm install syncfusion=github:syncfusion/Javascript-Widgets
   ~~~
   
   ![](Installation-and-Deployment_images/jspminstallationsteps_img1.jpeg)

   B) To install the Syncfusion JavaScript jspm package via npm repository.
   
   ~~~
   jspm install npm:syncfusion-javascript
   ~~~
   
N> As per standard Syncfusion used the 3 digit version for jspm packages. To install a particular version of jspm package, need to provide the version as suffix of the package name while installing. For instance, run the below command,  
N> E.g. The below command installs Syncfusion Javascript package of version 14.1.0.46.  
N> 'jspm install syncfusion=github:syncfusion/JavaScript-Widgets@14.1.46'

### jspm Update

To update all the installed packages by using below command.

~~~
jspm update
~~~

![](Installation-and-Deployment_images/jspminstallationsteps_img1.jpeg)

To update specific package by using below commands.

~~~
jspm update npm:syncfusion-javascript
~~~

  (Or)
  
~~~
jspm update syncfusion=github:syncfusion/JavaScript-Widgets
~~~