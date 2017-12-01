---
layout: post
title: Getting Started for Electron
description: How to use Essential JS with Electron.
platform: js
control: Introduction
documentation: ug
---


# Electron 


## Introduction
	


Electron (Previously known as Atom Shell) is used create a cross platform desktop application for different OS like Linux, Windows and OS X by using JavaScript and able to access platform specific native API's.



Electron uses Chromium browser and Node.js (Building block of Electron) and we can able to build the app with HTML, CSS, and JavaScript.



For more information, refer the official electron page in this [link](http://electron.atom.io/).



## Prerequisites and Compatibility


**Prerequisites**

While running the electron it requires[Node.js](https://nodejs.org/en/download/)(which includes[npm](https://npmjs.org/)) on your system.

**Compatibility**

OS X

Only 64bit binaries are provided for OS X, and the minimum OS X version supported is OS X 10.9.

Windows

Electron supports Windows 7 and later, older OS versions are not supported.

Both x86 and amd64 (x64) binaries are provided for Windows and it is not supported in the ARM version of Windows.

## Using Syncfusion Essential JS controls with Electron Framework:

This step by step guide is used to create a combination of Essential JS UI controls with Electron Framework. 




## Steps to add the sample and run the Application



### Follow the below steps and enter the below commands using command prompt window.


Step1:

To clone and run this repository need[Git](https://git-scm.com/) and [Node.js](https://nodejs.org/en/download/)(which comes with[npm](http://npmjs.com/)) installed on your system, then enter the below command using terminal (Mac OS) or Command Prompt (Windows).


N> For Mac OS run the command in administrator mode with $sudo as prefix

1. Clone the Quick Start repository

        {% highlight bash %}

        $ git clone <a href=https://github.com/electron/electron-quick-start>https://github.com/electron/electron-quick-start</a> 

        {% endhighlight %}

![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img1.png)



2. Go into the repository

        {% highlight bash %}

        $ cd electron-quick-start 

        {% endhighlight %}



![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img2.png)



3. Install the dependencies

        {% highlight bash %}

        $ npm install 

        {% endhighlight %}



![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img3.png)


N> Learn more about Electron and its API in the [documentation](http://electron.atom.io/docs).



Step2:

Add the Syncfusion JS and CSS file reference in index.html file as mentioned on this [link](https://help.syncfusion.com/js/control-initialization), Refer the index.html location in the below image. 



![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img4.png)

N> When refer jQuery reference add the below_ [code](http://electron.atom.io/docs/faq/) _in head tag._

{% highlight javascript %}     

window.nodeRequire = require;        
delete window.exports;        
delete window.module;

{% endhighlight %}


Step3:


Add the below sample code in index.html file to render Accordion control.



{% highlight html %}

   <div id="accordion" style="margin: auto;">
        <h3>ASP.NET</h3>
        <div>Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser. </div>
        <h3>ASP.NET MVC</h3>
        <div>The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC Framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications. </div>
        <h3>JavaScript</h3>
        <div>JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. </div>
    </div>   

{% endhighlight %}

Initialize Accordion in the script.

{% highlight javascript %}

   $(function () {            
       // document ready            
       // Initialize Accordion control creation.            
       $("#accordion").ejAccordion({ width: "500px" });        
       });     

{% endhighlight %}


Step4:


Run the Electron Application using the below command.



{% highlight bash %}

$ npm start 

{% endhighlight %}




![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img5.png)



Now see the created Electron Application as below.




![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img6.png)



## Steps to use Electron Packager

Bundle the Electron based application and make it as executable file by using[Electron Packager](https://github.com/electron-userland/electron-packager)After creating the application as mentioned above, use the below steps to package the application.



## Electron Packager for Windows



Use the below CLI to create Electron package for windows.

 1. Install Electron packager


    {% highlight bash %}

    $ npm install electron-packager –g

    {% endhighlight %}


2. Package the application


    {% highlight bash %}

    $ electron-packager ./ JS_Electron --platform=win32 --arch=ia32 ./JS_Electron

    {% endhighlight %}

Now JS_Electron-win32-ia32 folder is created. Open the mentioned folder and JS_Electron.exe is the runnable Application file for the created Electron project. 




## Electron Packager for Windows



Use the below CLI to create Electron package for windows.

1. Install Electron packager


    {% highlight bash %}

    $ npm install electron-packager –g

    {% endhighlight %}




2. Package the application


    {% highlight bash %}

    $ electron-packager ./ JS_Electron --platform=win32 --arch=ia32 ./JS_Electron

    {% endhighlight %}

Now JS_Electron-win32-ia32 folder is created. Open the mentioned folder and JS_Electron.exe is the runnable Application file for the created Electron project. 




## Electron Packager for OS X



Use the below CLI to create Electron package in Mac OS(OS X).



1. Install npm

    {% highlight bash %}

    sudo npm install

    {% endhighlight %}



2. Install electron packager

    {% highlight bash %}

    sudo npm install electron-packager -g

    {% endhighlight %}


3. Package the application

    {% highlight bash %}

    sudo electron-packager ./ JS_Electron --platform=darwin ./JS_Electron

    {% endhighlight %}




Now the Electron Application is created in the mentioned folder JS_Electron-darwin-x64.



