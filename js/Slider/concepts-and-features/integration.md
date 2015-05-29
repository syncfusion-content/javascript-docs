---
layout: post
title: integration
description: integration
platform: js
control: Slider
documentation: ug
---

# Integration

## Angular binding 

Angular JS is structural Framework to create dynamic web apps. It is distributed as a **JavaScript** file. It extends **HTML** attributes with Directives, and binds data to **HTML** with Expressions. To learn more about Angular JS refer the following link

[http://www.w3schools.com/angular/default.asp](http://www.w3schools.com/angular/default.asp)

**Slider** widget is provided with Angular JS support. The support is achieved by including the “**ej.widget.angular.min.js**” file. Refer the following link to know more about the AngularJS support.

[http://help.syncfusion.com/ug/js/default.htm#!documents/angularjs.htm](http://help.syncfusion.com/ug/js/default.htm)

**Slider** widget is defined using the directive **slider**. The properties of the **Slider** widget can be included as inline **HTML** attributes by prefixing the properties with “**e-**“. The properties are not case sensitive when defining it. Angular JS provides two types of data binding “one way binding” and “two way binding”. 

All properties in the slider supports one way data binding. Here one way binding specifies that the values for the slider properties are assigned automatically when specified through the data binding notation, but the property values is not changed in the model. That is, the values are displayed only in the **HTML** view not in the application data.

The **Slider** properties **value** and **values** are provided with two way binding support. The changes made to these properties are reflected both in the application data (model) and in **HTML** view.

* The following example explains you the binding of **value** property using the Angular support.

{% highlight html %}

[**HTML**]

<head>
    <title>Slider</title>

     <link href="http://cdn.syncfusion.com/js/web/ej.widgets.core.min.css" rel="stylesheet" />

    <link href="http://cdn.syncfusion.com/js/web/flat-azure/ej.theme.min.css" rel="stylesheet" />

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

     <scriptsrc="[http://cdn.syncfusion.com/js/assets/external/angular.min.js](http://cdn.syncfusion.com/js/assets/external/angular.min.js)"></script>

<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js)"></script>

     <scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js](http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js)"></script>
</head>


{% endhighlight %}



{% highlight html %}

[H**TML**]
**/ /** Add this code in your html page
<body ng-app="syncApp" **ng-controller="SliderCtrl"**>
    <div class="frame">
        <div id="sliderContainer" class="control">
            <div id="rangeSlider" ej-slider e-width="width" e-value="sliderValue"></div>
            <h5><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 25px;">Note:Two Way Angular Support</span></h5>
        </div>
        <div id="binding">
            <input type="text" name="slider" class="input ejinputtext" value="" ng-model="sliderValue" />
        </div>
    </div>
</body>


{% endhighlight %}



{% highlight js %}

**[JavaScript]**
//In JavaScript, bind the “value” and “width” property in Angular way as follows,
    <script>
        // declaration                   
        angular.module('syncApp', ['ejangular'])
           .controller('SliderCtrl', function ($scope) {
               $scope.sliderValue = 60;
               $scope.width = "80%";
           });
       </script>


{% endhighlight %}



* Execute the above code example to render the following output.


{% include image.html url="\js\Slider\concepts-and-features\integration_images\integration_img1.png" Caption="Slider rendered in Angular way."%}

## Knockout binding

KnockOutJS is a **JavaScript** library that follows the MVVM pattern to build sophisticated user interface with a clean underlying data model. It supports to update the UI dynamically. Refer the following link to know more about KnockOutJS.

[http://knockoutjs.com/documentation/introduction.html](http://knockoutjs.com/documentation/introduction.html)

**Slider** widget includes support to use it with KnockOutJS. The support is achieved by integration of the JS library **ej.widget.ko.min.js file.** Refer the following link to know more about the KnockOutJS support

[http://help.syncfusion.com/ug/js/documents/knockoutjs.htm](http://help.syncfusion.com/ug/js/documents/knockoutjs.htm)

The binding handler name for **Slider** component is **Slider**. Both one way binding and two way binding support is included. All properties of the **Slider** component supports one way binding. In the **HTML** markup, specify the property using the binding handler. 

Two way binding support is included only for the applicable **Slider** properties, **value** and **values**. To activate two way binding support, you can specify these properties as observables in the **ViewModel**. Then use the **ko.applyBindings** to activate it. Now these properties binds the underlying data model and the changes is reflected automatically.

* The following example explains you the binding of **value** property using the Angular support.



<table>
<tr>
<td>
[<b>HTML</b>]&lt;body&gt;    &lt;div class="frame"&gt;        &lt;div id="sliderContainer" class="control"&gt;            &lt;div id="rangeSlider" data-bind="ejSlider: { value: sliderValue }"&gt;&lt;/div&gt;         &lt;/div&gt;        &lt;div id="binding"&gt;            &lt;input type="text" name="slider"  class="input ejinputtext" value="" data-bind="value: sliderValue" /&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/body&gt;</td></tr>
<tr>
<td>
[<b>JavaScript</b>]// In JavaScript, specify the “value” property as observable in the ViewModel to enable the two way binding.    &lt;script&gt;        $(function () {            // declaration                        window.viewModel = {                sliderValue: ko.observable(40),            };            ko.applyBindings(viewModel);        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.


{% include image.html url="\js\Slider\concepts-and-features\integration_images\integration_img2.png" Caption="Exhibits two way binding support using KnockOutJS"%}

