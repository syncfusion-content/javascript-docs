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

Angular 2 wrappers for Syncfusion JavaScript controls is available in the file `ej.angular2.min.js` which can be copied from Syncfusion Build installed location.

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
    <script src="node_modules/core-js/client/shim.min.js"></script>   
    <script src="node_modules/zone.js/dist/zone.js"></script>
    <script src="node_modules/reflect-metadata/Reflect.js"></script>
    <script src="node_modules/systemjs/dist/system.src.js"></script>

    <!-- Essential Studio for JavaScript  script references -->
    <script src="https://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/14.1.0.41/js/web/ej.web.all.min.js"> </script> 
    <script src="http://cdn.syncfusion.com/14.1.0.41/js/common/ej.angular2.min.js"><script>
    
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
For SystemJS configuration, please refer [Angular 2.0 documentation](https://angular.io/docs/ts/latest/quickstart.html#!#config-files).

## 2. Adding Syncfusion Component to your Application

Each Syncfusion components are wrapped as individual SystemJS module. So for importing and using any Syncfusion component, use `ej/<controlName>.component` in require path and variable name holding references to component is `EJ_<CONTROLNAME>_COMPONENTS`. For getting started, you can import the dialog component, refer the following code snippet for the same.

{% highlight javascript %}

import {EJ_DIALOG_COMPONENTS} from 'ej/dialog.component';

{% endhighlight %}

### Property Binding

Properties and events names of Syncfusion controls can be initialized with the exact casing of original property names. Bind property to the controls within square bracket(`[]`).

For autocomplete component, create attribute with prefixing `ej-` and control name then setting `dataSource` and `value` property will be

{% highlight html %}

<input type="text" ej-autocomplete [value]= "Austin-Healey" [dataSource]="states" [(ngModel)]="value"/>

{% endhighlight %}

### Event Binding

Events can be bind to controls using event name within bracket [`()`]. For example, to bind open event on ejAutocomplete, we need to define attribute (open) as onOpen($event). Refer the following snippet for event binding.

{% highlight html %}

<input type="text" ej-autocomplete (open)="onOpen($event)" />

{% endhighlight %}

Define event definition at component side as like follow.

{% highlight javascript %}

export class AppComponent { 
    onOpen(e){
        console.log("Triggers after the suggestion list is opened.");        
    }
}

{% endhighlight %}

### Two-way Binding

Two-way binding for Angular2 is bind the value in both view and component using attiribute `[(ngModel)]` and use the same for Syncfusion widget also, it can reflect the changes both ways. In general, we could have more than one property bound to the same variable.

Two-way binding for Autocomplete has been demonstrated in the below code,

{% highlight javascript %}

@Component({
    selector: 'my-app',
    template: ' <h2>Two-Way Binding</h2>
    <input type="text" ej-autocomplete [dataSource]="states" (open)="onOpen($event)" [(ngModel)]="value"/>
    <input type="text" name="AutoComplete" class="input ej-inputtext" [(ngModel)]="value" />
    ',
    directives: [EJ_AUTOCOMPLETE_COMPONENTS],
})
export class DefaultComponent {
    states: Array<string>;
    value:string; 
    constructor(public northwindService: NorthwindService) {
        this.states = [
         "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
                    "BMW 7 ", "Bentley Mulsanne", "Bugatti Veyron",
                    "Chevrolet Camaro", "Cadillac ",
                    "Duesenberg J ", "Dodge Sprinter",
                    "Elantra", "Excavator",
                    "Ford Boss 302", "Ferrari 360", "Ford Thunderbird ",
                    "GAZ Siber",
                    "Honda S2000", "Hyundai Santro",
                    "Isuzu Swift", "Infiniti Skyline",
                    "Jaguar XJS",
                    "Kia Sedona EX", "Koenigsegg Agera",
                    "Lotus Esprit", "Lamborghini Diablo ",
                    "Mercedes-Benz ", "Mercury Coupe", "Maruti Alto 800",
                    "Nissan Qashqai",
                    "Oldsmobile S98", "Opel Superboss",
                    "Porsche 356 ", "Pontiac Sunbird",
                    "Scion SRS/SC/SD", "Saab Sportcombi", "Subaru Sambar", "Suzuki Swift",
                    "Triumph Spitfire ", "Toyota 2000GT",
                    "Volvo P1800", "Volkswagen Shirako"
        ];
        this.value="Jaguar XJS";
   }
}


{% endhighlight %}



N> For complete understanding of Angular 2 inputs and outputs binding syntaxes, refer [this](https://angular.io/docs/ts/latest/guide/template-syntax.html#!#binding-syntax-an-overview) angular help document.

E> Error : Cannot find module 'ej/dialog.component' - This error will throw if missing of `ej.angular2.min.js` file from sample.

## 3. Invoking EJ widget methods from component instance

You can invoke the ej widget’s public methods using Angular 2 component instance reference. Syntax for this is 

{% highlight javascript %}

<componentInstance>.widget.<methodName>(<params_if_any>)

{% endhighlight %}

For ex, to invoke `clearText` method of autocomplete widget, you can use like `myApp.widget.clearText()`. So the complete code structure of `app.component.ts` will be as follows

{% highlight javascript %}

import {Component} from '@angular/core';
import {EJ_DIALOG_COMPONENTS} from 'ej/dialog.component';

@Component({
    selector: 'my-app',
    template: ' <h2>Two-Way Binding</h2>
    <button id="clearTxt" (click)="myApp.widget.clearText()">clearText</button>
    <input #myApp type="text" ej-autocomplete [dataSource]="states" (open)="onOpen($event)" [(ngModel)]="value"/>
    <input type="text" name="AutoComplete" class="input ej-inputtext" [(ngModel)]="value" />
    ',
    directives: [EJ_AUTOCOMPLETE_COMPONENTS],
})
export class DefaultComponent {
    states: Array<string>;
    value:string; 
    constructor(public northwindService: NorthwindService) {
        this.states = [
         "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
                    "BMW 7 ", "Bentley Mulsanne", "Bugatti Veyron",
                    "Chevrolet Camaro", "Cadillac ",
                    "Duesenberg J ", "Dodge Sprinter",
                    "Elantra", "Excavator",
                    "Ford Boss 302", "Ferrari 360", "Ford Thunderbird ",
                    "GAZ Siber",
                    "Honda S2000", "Hyundai Santro",
                    "Isuzu Swift", "Infiniti Skyline",
                    "Jaguar XJS",
                    "Kia Sedona EX", "Koenigsegg Agera",
                    "Lotus Esprit", "Lamborghini Diablo ",
                    "Mercedes-Benz ", "Mercury Coupe", "Maruti Alto 800",
                    "Nissan Qashqai",
                    "Oldsmobile S98", "Opel Superboss",
                    "Porsche 356 ", "Pontiac Sunbird",
                    "Scion SRS/SC/SD", "Saab Sportcombi", "Subaru Sambar", "Suzuki Swift",
                    "Triumph Spitfire ", "Toyota 2000GT",
                    "Volvo P1800", "Volkswagen Shirako"
        ];
        this.value="Jaguar XJS";
   }
   onOpen(e){
        console.log("Triggers after the suggestion list is opened.");        
    }
}

{% endhighlight %}

Final browser output will be as follows

![](/js/Angular2_images/angular2_sample_img.png)
