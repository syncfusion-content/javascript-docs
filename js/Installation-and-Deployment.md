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

Within the root `javascript` folder, the `assets` folder contains all the minified versions of scripts and stylesheets where as the `assets-src` folder contains the uncompressed version of the same files. The assets have been organized in the following folder structure

  * Css - contains the style sheets for mobile and web components.
  * External - contains the external dependency files such as jquery, jquery.easing etc.
  * Scripts - includes all the necessary scripts for Syncfusion Essential JS components.
  * TypeScript - includes the default type-definition file `ej.widgets.all.d.ts`.

## For Mac and Linux Users

**Mac** and **Linux** users can download all the necessary files in a zip archive from this [link](http://www.syncfusion.com/downloads/javascript) after logging in with your Syncfusion account. Licensed customers can download the archive from the [downloads](http://www.syncfusion.com/support/directtrac/downloads) section.

The assets have been organized in the following folder structure

* Assets – contains all the necessary scripts and stylesheets.
* External – contains the external dependency files such as jquery, jquery.easing etc.
* Samples  – contains sample code that demonstrate usage of all the components.


N>   **Mac** and **Linux** users will not be able to use the **Reporting and Business Intelligence** components since the controls have a server-side .NET dependency.
N>  Also, the exporting functionality available in some of the widgets like the grid will also not be available due to the server-side .NET dependencies.


## Configuring Syncfusion NuGet Packages

The steps to download and configure the Syncfusion NuGet Packages in Visual Studio are as follows,

* Download the and unzip the Syncfusion NuGet Packages for JavaScript from [here](http://nuget.syncfusion.com/login) 

* In Visual Studio, navigate to `Tools|Library Package Manager|Package Manager Settings`, the Options pop-up will appear on the screen as shown below,
  
  ![](/Installation-and-Deployment_images/Installation-and-Deployment_img1.png) 

* Select `Package Manager|Package Sources` in the above pop-up and click on the `Browse` button(preceding the `Add` button) to navigate to the location where the above collection of NuGet packages are located on your machine.
  
  ![](/Installation-and-Deployment_images/Installation-and-Deployment_img3.png) 

N>  The **Source** textbox in the above image denotes the location of the NuGet packages on your machine and the **Name** section, allows you to provide a unique name which we will refer to in the package installation section later.

* Now click the `Add` button and the package name will be listed in the **Available package sources** list as shown below and then Click `OK`.

  ![](/Installation-and-Deployment_images/Installation-and-Deployment_img4.png) 

* Now you can proceed with the installation. The steps involved in usage within your application is explained in the [Control Initialization](/js/control-initialization#configuring-and-installing-nuget-into-your-project) section.

## Configuring Syncfusion Bower Package

### Overview

[Bower](bower.io# "") is a package manager for the Web. Syncfusion bower package allows you to use the Syncfusion Javascript libraries in an efficient way.

I>Syncfusion JavaScript Bower package is available as [public Git Repository](https://github.com/syncfusion/JavaScript-Widgets/# "") and also registered as syncfusion-javascript in the bower registry.

### Bower Install and Configuration

#### Bower Installation

To configure the bower in your machine you need to install [node, npm](http://nodejs.org/# "") and [git](http://git-scm.org/# ""). For more information to configure the Bower package please refer the official site for [bower](http://bower.io/#install-bower ""). 
Syncfusion Javascript Bower package can be configured in the following ways.
1. Using command prompt.

2. Using bower.json file.

3. From local directory.

##### Using command prompt


Perform the below steps to install Syncfusion bower Package via command prompt in your web application.
1. Open your web project’s location in a command prompt window.

2. Then run the command bower install <package name>.

   ~~~
   bower install syncfusion-javascript
   ~~~
   
   ![](Installation-and-Deployment_images/Installation-and-Deployment_img5.jpeg)

3. The bower will install the Syncfusion Javascript files into the project location to develop with Syncfusion controls.

N>To install a particular version of a bower package, you need to provide the version as suffix of the package name while installing. For instance, run the below command, Eg: To install the package of version 13.3.0.18. 
N>'bower install syncfusion-javascript#13.3.0.18'

##### Using bower.json file

In another way, you can add the packages to the bower.json file by simply specify the package name. This will install/restore the packages to your project. Please refer the below image.
 
![](Installation-and-Deployment_images/Installation-and-Deployment_img6.jpeg)

N>ASP.NET 5 (preview) projects have bower.json file by default. If your project doesn’t have bower.json file then run the below command from your project directory by Command prompt. 
N>'bower init'

![](Installation-and-Deployment_images/Installation-and-Deployment_img7.jpeg)

##### From local directory

You can install the Syncfusion bower package from a local directory. To perform this follow the below steps.

1. Navigate the [Syncfusion Javascript bower repository](https://github.com/syncfusion/JavaScript-JavaScript-Widgets/# "") location on github and download the repository as zip by click the “Download ZIP” button and extract the contents in your computer’s any of the local directory.

   ![](Installation-and-Deployment_images/Installation-and-Deployment_img8.jpeg)

2. Then run the install command by providing the package content’s location. 

   ![](Installation-and-Deployment_images/Installation-and-Deployment_img9.jpeg)

#### Bower Update

To update the installed bower packages, run the command bower update <package name>.
~~~
bower update syncfusion-javascript
~~~

![](Installation-and-Deployment_images/Installation-and-Deployment_img10.jpeg)
