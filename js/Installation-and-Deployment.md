---
layout: post
title: Installation and Deployment of Syncfusion Essential JS platform
description: How to installation and deployment of Essential JS platform in Windows, Mac & Linux machines. Configuring and installing through NuGet of Syncfusion Essential JS widgets.
platform: js
control: Introduction
documentation: ug
---

# Installation and Deployment

## For Windows Users

Download the **Essential Studio for JavaScript** setup from this [link](http://www.syncfusion.com/downloads/javascript) with your Syncfusion account and follow the steps mentioned in the [setup guide](http://help.syncfusion.com/ug/common/index.html).

### Install Location

The below specified root location is the place from where all the Syncfusion assemblies, scripts, stylesheets and dashboard samples are available,

`(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\`

_If you have installed the Essential Studio package within `C:\Program Files (x86)`, then navigate to the below location, C:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\_

If you are looking for the JavaScript samples, you can find it from the `Samples` folder present within the above specified location. 

#### JavaScript Folder Structure and Asset Details

The location mentioned below is the root `JavaScript` folder which contains two important sub-folders namely,

* assets
* Src

`(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\ JavaScript\`

_If you have installed the Essential Studio package within `C:\Program Files (x86)`, then navigate to the below location, C:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\_

##### assets 

The `assets` folder contains all the minified versions of the external scripts, common scripts, style sheets and TypeScript files under their corresponding folders.

  * Css - contains the style sheets for mobile and web components.
  * External - contains the external dependency files such as jquery, jquery.easing and etc.
  * Scripts - includes all the necessary scripts for Syncfusion Essential JS components.
  * TypeScript - includes the default type-definition file `ej.widgets.all.d.ts`.

##### Src

This folder contains the sub-folder namely `assets-src`, which includes all the non-minified versions of the Scripts and style sheets separately for all the individual Syncfusion widgets.

The same folders whichever available within the assets folder (namely css, external, scripts, typescript) are made available within the assets-src folder too, but in the **uncompressed** format, which can be used for performing any customization or debugging purpose. 



The location under where these uncompressed files are available are as follows,


`(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\Src\assets-src`

_If you have installed the Essential Studio package within `C:\Program Files (x86)`, then navigate to the below location,C:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\Src\assets-src_


## For Mac and Linux OS Users

For **Mac** and **Linux** OS users, we are providing a zip folder instead of .exe file, which includes the following main folders (no installation needed) – 

**Assets** – It contains all the Essential JavaScript scripts and CSS as mentioned previously.

**External** – It includes the external jQuery dependencies, culture files and other third-party scripts.

**Samples** – This folder contains samples of all the Syncfusion Essential JS widgets. 

It also includes other folders namely Release Notes, License Agreement and Read Me. The control creation will be same as described in the [Control Initialization](/js/control-initialization) section (Here, the scripts and style sheets are needed to be referred from the **Assets** folder into their respective `HTML` pages).


>  **Note:** The **Mac** and **Linux** users cannot be make use of the **Reporting and Business Intelligence** controls, as it needs assembly reference to be included in the application. Due to the installation of .exe is not supported in those two OS (the assembly libraries required for the Reporting & BI controls are not available in the system), we provide only the zip folder containing the JavaScript related scripts, style sheets and samples. 
>  Also, the exporting functionality available in some of the JavaScript widgets will not work here, due to the .NET assembly dependency.


## Configuring Syncfusion NuGet Packages

The steps to download and configure the Syncfusion NuGet Packages in Visual Studio are as follows,

Download the Syncfusion NuGet Packages for JavaScript from [here](http://nuget.syncfusion.com/login) and save it in your system. The downloaded file is a zip formatted file, therefore unzip the folder and copy the `SyncfusionJavaScript.{{ site.releaseversion }}.nupkg` package in it. Create a new folder namely `NuGet Packages` in any of the particular location in your system and place the copied file into it.

In Visual Studio, navigate to `Tools|Library Package Manager|Package Manager Settings`, the Options pop-up will appear on the screen as below,
{% include image.html url="/js/Installation-and-Deployment_images/Installation-and-Deployment_img1.png" %}

Select `Package Manager|Package Sources` in the above pop-up and click on the `Browse` button(preceding the `Add` button) to navigate to the location where the above collection of NuGet packages are located (namely, within the NuGet Packages folder) in your system.
{% include image.html url="/js/Installation-and-Deployment_images/Installation-and-Deployment_img3.png" %}

>  **Note**: The **Source** textbox in the above image denotes the location of the NuGet packages in your machine and the **Name** section, allows you to provide a unique name which we will refer in the package installation section later.

Now click the `Add` button and the package name will be listed in the **Available package sources** list as shown below and then Click `OK`.
{% include image.html url="/js/Installation-and-Deployment_images/Installation-and-Deployment_img4.png" %}

Now you can proceed with its installation part while using it in your application which will be described in the [Control Initialization](/js/control-initialization#configuring-and-installing-nuget-into-your-project) section.

