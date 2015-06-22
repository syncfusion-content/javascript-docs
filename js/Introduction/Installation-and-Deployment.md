---
layout: post
title: Installation-and-Deployment
description: installation and deployment
platform: js
control: Introduction
documentation: ug
---

# Installation and Deployment

## For Windows Users

Download the setup file (.exe) of **Essential Studio for JavaScript** product from this [link](http://www.syncfusion.com/downloads/javascript) with your Syncfusion account and follow the steps mentioned in the [setup guide](http://help.syncfusion.com/ug/common/index.html) to install the specific/entire platform on your machine.

### Install Location

The below specified root location is the place from where all the Syncfusion assemblies, scripts, stylesheets and dashboard samples are available,


<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\
</td>
</tr>
<tr>
<td>
<b>For example,</b> If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\
</td>
</tr>
</table>

If you are looking for the **JavaScript Samples**, you can find it from the **Samples** folder present within the above specified location. 

#### JavaScript Folder Structure and Asset Details

The location mentioned below is the root **JavaScript** folder which contains two important sub-folders namely,

* assets
* Src

<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\ JavaScript\
</td>
</tr>
<tr>
<td>
<b>For example,</b> If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\
</td>
</tr>
</table>


##### assets 

The **assets** folder comprises of all the minified versions of the external and common Scripts, StyleSheets and TypeScript files under their corresponding folders. It mainly includes 4 sub-folders namely,

  * Css
  * External
  * Scripts
  * TypeScript



The Stylesheets required for supporting the theming and styling of the Syncfusion components (both mobile and web) are available in a minified format within the **css** folder. The **css** folder is again sub-categorized into mobile and web where all the mobile related css files are present within the **mobile** folder and all those related to web components are availed within the **web** folder. 



The **external** folder contains the external dependency files such as jquery, jquery.easing, jsrender, Culture files and other third-party script files.



The **scripts** folder includes all the Syncfusion components UI scripts in the minified format for both web and mobile components. 



The **TypeScript** folder includes the default type-definition file (**ej.widgets.all.d.ts**) for the purpose of supporting classes, modules, strong-type checking during compile time itself and also provides IntelliSense support within the JavaScript environment.

##### Src

This folder comprises of the sub-folder namely **assets-src**, which includes all the non-minified versions of the Scripts and Stylesheets separately for all the individual Syncfusion widgets.

The same folders whichever available within the **assets** folder (namely css, external, scripts, typescript) are made available within the **assets-src** folder too, but in the **non-minified** format, which can be used for performing any customization or debugging purpose. 



The location under where these non-minified files are available are as follows,



<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\ JavaScript\Src\assets-src
</td>
</tr>
<tr>
<td>
<b>For example,</b> If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\Src\assets-src
</td>
</tr>
</table>

## For MAC and Linux OS Users

For **MAC OS** and **Linux** users, we are providing a zip folder instead of .exe file, which includes the following main folders (no installation needed) – 

**Assets** – It contains all the Essential JavaScript scripts and CSS as mentioned previously.

**External** – It includes the external jQuery dependencies, culture files and other third-party scripts.

**Samples** – This folder contains samples of all the Syncfusion JavaScript controls. The user can directly open the html sample page in any of the browser to view the output.

It also includes other folders namely Release Notes, License Agreement and Read Me. The control creation will be same as described in the Getting Started section (Here, the scripts and StyleSheets are needed to be referred from the **Assets** folder into their respective HTML pages).


>  **Note**: The **MAC** and **Linux** users cannot be able to make use of the **Reporting and Business Intelligence** controls, as it needs assembly reference to be included in the application. Due to the installation of .exe is not supported in those two OS (the assembly libraries required for the Reporting & BI controls are not available in the system), we provide only the zip folder containing the JavaScript related Scripts, Stylesheets and Samples. 
>  Also, the exporting functionality available in some of the JavaScript widgets will not work here, due to the assembly dependency.


## Configuring Syncfusion Nuget Packages

The steps to download and configure the Syncfusion Nuget Packages in Visual Studio are as follows,

Download the Syncfusion Nuget Packages for **JavaScript** from [here](http://nuget.syncfusion.com/login) and save it in your system. The downloaded file is a zip formatted file, therefore unzip the folder and copy the **SyncfusionJavaScript.{{ site.releaseversion }}.nupkg** package in it. Create a new folder namely **Nuget Packages** in any of the particular location in your system and place the copied file into it.

In Visual Studio, navigate to **Tools** -> **Library Package Manager** -> **Package Manager Settings**, the **Options** pop-up will appear on the screen as below,
{% include image.html url="/js/Introduction/Installation-and-Deployment_images/Installation-and-Deployment_img1.png" %}

Select **Package Manager** -> **Package Sources** in the above pop-up and click on the **Browse** button(preceding the **Add** button) to navigate to the location where the above collection of nuget packages are located (namely, within the **Nuget Packages** folder) in your system.
{% include image.html url="/js/Introduction/Installation-and-Deployment_images/Installation-and-Deployment_img3.png" %}

>  **Note**: The **Source** textbox in the above image denotes the location of the nuget packages in your machine and the **Name** section, allows you to provide a unique name which we will refer in the package installation section later.

Now click the **Add** button and the package name will be listed in the **Available package sources** list as shown below and then Click **OK**.
{% include image.html url="/js/Introduction/Installation-and-Deployment_images/Installation-and-Deployment_img4.png" %}

The configuration part of Syncfusion JavaScript Nuget packages ends here and now you can proceed with its installation part while using it in your application (which will be described in the Getting Started section).

