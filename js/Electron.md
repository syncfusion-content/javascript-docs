# Electron 


## Introduction



Electron (Previously known as Atom Shell) is used create a cross platform desktop application for different OS like Linux, Windows and OS X by using JavaScript and able to achieve native API supports.



Electron uses Chromium browser and Node.js (Building block of Electron) and we can able to build the app with HTML, CSS, and JavaScript.



For more information, refer the official electron page in this [link](http://electron.atom.io/).



## Prerequisites and Compatibility


Prerequisites

While runningthe electron it requires[Node.js](https://nodejs.org/en/download/)(which includes[npm](https://npmjs.org/)) on your system.

Compatibility

OS X

Only 64bit binaries are provided for OS X, and the minimum OS X version supported is OS X 10.9.

Windows

Electron supports Windows 7 and later, older OS versions are not supported.

Both x86 and amd64 (x64) binaries are provided for Windows and it is not supported in the ARM version of Windows.

## Using Syncfusion Essential JS controls with Electron Framework:

This step by step guide is used to create a combination of Essential JS UI controls with Electron framework. 




## Steps to add the sample and run the Application



### Follow the below steps and enter the below commands using command prompt window.


Step1:

To clone and run this repository need[Git](https://git-scm.com/)and[Node.js](https://nodejs.org/en/download/)(which comes with[npm](http://npmjs.com/)) installed on your system, then enter the below command line using terminal (Mac OS) with administrator mode($sudo prefix) or Command Prompt (Windows).



1. # Clone the Quick Start repository



<table>
<tr>
<td>
$ git clone <a href=https://github.com/electron/electron-quick-start>https://github.com/electron/electron-quick-start</a> </td></tr>
<tr>
<td>
</td></tr>
</table>




![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img1.png)



2. # Go into the repository





<table>
<tr>
<td>
$ cd electron-quick-start </td></tr>
<tr>
<td>
</td></tr>
</table>


![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img2.png)



3. # Install the dependencies



<table>
<tr>
<td>
$ npm install </td></tr>
<tr>
<td>
</td></tr>
</table>


![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img3.png)


N>

_Learn more about Electron and its API in the___[documentation](http://electron.atom.io/docs/latest)_._



Step2:

Add the Syncfusion JS and CSS file reference in index.html file as mentioned on this [link](http://help.syncfusion.com/js/control-initialization), Refer the index.html location in the below image. 



![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img4.png)

N>

_When refer jQuery reference add the below_ [code](http://electron.atom.io/docs/faq/) _in head tag._

<table>
<tr>
<td>
&lt;script&gt;        window.nodeRequire = require;        delete window.exports;        delete window.module;&lt;/script&gt;</td></tr>
<tr>
<td>
</td></tr>
</table>


Step3:


Add the below sample code in index.html file to render Accordion control.



<table>
<tr>
<td>
    <h1 style="text-align: center;">Essential JS-Electron Demo</h1>    &lt;div id="accordion" style="margin: auto;"&gt;        &lt;h3&gt;            <a href="#">ASP.NET</a>&lt;/h3&gt;        &lt;div&gt;            Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.        &lt;/div&gt;        &lt;h3&gt;            <a href="#">ASP.NET MVC</a>&lt;/h3&gt;        &lt;div&gt;            The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.        &lt;/div&gt;        &lt;h3&gt;            <a href="#">Javascript</a>&lt;/h3&gt;        &lt;div&gt;            JavaScript (JS) is an interpreted computer programming language.                        It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.        &lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
</td></tr>
</table>


Initialize Accordion in the script.

<table>
<tr>
<td>
   $(function () {            // document ready            // Initialize Accordion control creation.            $("#accordion").ejAccordion({ width: "500px" });        });</td></tr>
<tr>
<td>
</td></tr>
<tr>
<td>
</td></tr>
</table>

Step4:


Run the Electron Application using the below command line.



<table>
<tr>
<td>
$ npm start </td></tr>
<tr>
<td>
</td></tr>
</table>




![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img5.png)



Now see the created Electron Application as below.




![](Electron-Getting-started\steps-to-add-the-sample-and-runthe-application_img6.png)



## Steps to use Electron Packager

Bundle the Electron based application and make it as executable file by using[Electron Packager](https://github.com/electron-userland/electron-packager)After creating the application as mentioned above, use the below steps to package the application.



## Electron Packager for Windows



Use the below CLI to create Electron package for windows.

1. Install Electron packager





$ npm install electron-packager –g





2. Package the application



$ electron-packager ./ JS_Electron --platform=win32 --arch=ia32 ./JS_Electron

Now JS_Electron-win32-ia32 folder is created. Open the mentioned folder and JS_Electron.exe is the runnable Application file for the created Electron project. 




## Electron Packager for Windows



Use the below CLI to create Electron package for windows.

1. Install Electron packager





$ npm install electron-packager –g





2. Package the application



$ electron-packager ./ JS_Electron --platform=win32 --arch=ia32 ./JS_Electron

Now JS_Electron-win32-ia32 folder is created. Open the mentioned folder and JS_Electron.exe is the runnable Application file for the created Electron project. 






## Electron Packager for OS X



Use the below CLI to create Electron package in Mac OS(OS X).



1. Install npm





sudo npm install



2. Install electron packager



sudo npm install electron-packager -g



3. Package the application



sudo electron-packager ./ JS_Electron --platform=darwin ./JS_Electron





Now the Electron Application is created in the mentioned folder JS_Electron-darwin-x64.



