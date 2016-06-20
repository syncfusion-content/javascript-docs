---
layout: post
title: Getting Started with Syncfusion JavaScript for Angular 2.0
description: How to use Essential js Angular2.
platform: js
control: Introduction
documentation: ug
---

# Angular 2

Essential JavaScript provides support for Angular 2 framework through wrappers. Each Syncfusion widgets are created as Angular 2 components with built in support for data binding and child directives to make complex property defintion easier. 

# Getting Started

Before getting started with Syncfusion JavaScript for Angular 2, prepare your application with the official [Getting Started documentation](https://angular.io/docs/ts/latest/quickstart.html).

## 1. Preparing the HTML document

Angular 2 wrappers for Syncfusion JavaScript controls is available in the file `ej.angular2.js` which can be copied from Syncfusion Build installed location.

{% highlight html %}

<Program Files (x86)>\Syncfusion\Essential Studio\14.1.0.41\JavaScript\assets\scripts\common

{% endhighlight %}



For quicker startup, we are going to use CDN links for all Syncfusion resources. So the final boiler plate code will be.

{% highlight html %}
    <html>
    <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Essential Studio for JavaScript">
    <meta name="author" content="Syncfusion">
    <title></title>

    <!-- Essential Studio for JavaScript  theme reference -->
    <link rel="stylesheet" href="http://cdn.syncfusion.com/14.1.0.41/js/web/flat-azure/ej.web.all.min.css" />

    <!-- Angular2 related script references -->
    <!-- 1. Load libraries -->
         <!-- Polyfill(s) for older browsers -->
    <script src="deps/js/core-js/client/shim.min.js"></script>   
    <script src="deps/js/zone.js/dist/zone.js"></script>
    <script src="deps/js/reflect-metadata/Reflect.js"></script>
    <script src="deps/js/systemjs/dist/system.src.js"></script>

    <!-- Essential Studio for JavaScript  script references -->
    <script src="https://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/14.1.0.41/js/web/ej.web.all.min.js"> </script> 
    <script src="http://cdn.syncfusion.com/14.1.0.41/js/common/ej.angular2.js"><script>
    
    <!-- 2. Configure SystemJS -->
    <script src="system.config.js"></script>
    <script>       
      System.import('app')
            .then(null, console.error.bind(console));
    </script>

    </head>
    <!-- 3. Display the application -->
    <body>
    <my-app>Loading...</my-app>
    </body>
    </html>


{% endhighlight %}


N> In production, we highly recommend you to use our custom script generator to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use GZip compression in your server.
For SystemJS configuration, please refer [Angular 2.0 documentation](https://angular.io/docs/ts/latest/quickstart.html#!#systemjs-configuration).

## 2. Adding Syncfusion Component to your Application

Each Syncfusion components are wrapped as individual SystemJS module. So for importing and using any Syncfusion component, use `ej/<controlName>.component` in require path and variable name holding references to component is `EJ_<CONTROLNAME>_COMPONENTS`. For getting started, you can import the dialog component, refer the following code snippet for the same.

{% highlight javascript %}

import {EJ_DIALOG_COMPONENTS} from 'ej/dialog.component';

{% endhighlight %}

Now you have imported the list of Angular2 components and child directives if any, to your application. Also in HTML, you can create control element with tag name prefixing `ej-` and control name, i.e., for dialog component it will be `ej-dialog`. All the properties and events of Syncfusion controls can be initialized with the exact casing of original property names. i.e., for dialog component, setting `title` and `showOnInit` property will be 

{% highlight html %}

<ej-dialog [title]="'Welcome'" [showOnInit]="false" #welcomeMsg>
My First Syncfusion JavaScript’s Angular2 component
</ej-dialog>

{% endhighlight %}

So the complete file content of `app.component.ts` will be as follows

{% highlight javascript %}

import {Component} from '@angular/core';
import {EJ_DIALOG_COMPONENTS} from 'ej/dialog.component';

@Component({
    selector: 'my-app',
    template: `<h1>My First Angular 2 App</h1>
<ej-dialog title="Welcome" [showOnInit]="false" #welcomeMsg >
My First Syncfusion JavaScript’s Angular2 component
</ej-dialog>
`,
    directives: [EJ_DIALOG_COMPONENTS]
})
export class AppComponent { 
}

{% endhighlight %}

N> For complete understanding of Angular 2 inputs and outputs binding syntaxes, refer [this](https://angular.io/docs/ts/latest/guide/template-syntax.html#!#binding-syntax-an-overview) angular help document.

E> Error: Cannot find module 'ej/dialog.component’ - This error will throw if missing of `ej.angular2.min.js` file from sample.

## 3. Invoking EJ widget methods from component instance

You can invoke the ej widget’s public methods using Angular 2 component instance reference. Syntax for this is 

{% highlight javascript %}

<componentInstance>.widget.<methodName>(<params_if_any>)

{% endhighlight %}

For ex, to invoke `open` method of dialog widget, you can use like `welcomeMsg.widget.open()`. So the complete file content of `app.component.ts` will be as follows

{% highlight javascript %}

import {Component} from '@angular/core';
import {EJ_DIALOG_COMPONENTS} from 'ej/dialog.component';

@Component({
    selector: 'my-app',
    template: `<h1>My First Angular 2 App</h1>

<button (click)="welcomeMsg.widget.open()">Show Dialog</button>

<ej-dialog title="Welcome" [showOnInit]="false"  #welcomeMsg >
My First Syncfusion JavaScript’s Angular2 component
</ej-dialog>
`,
    directives: [EJ_DIALOG_COMPONENTS]
})
export class AppComponent {}

{% endhighlight %}

Final browser output will be as follows

![](/js/Angular2_images/angular2_sample_img.png)
