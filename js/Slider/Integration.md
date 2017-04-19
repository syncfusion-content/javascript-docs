---
layout: post
title: Integration
description: integration
platform: js
control: Slider
documentation: ug
api: /api/js/ejslider
---

# Integration

## AngularJS binding 

AngularJS is structural Framework to create dynamic web apps. It is distributed as a **JavaScript** file. It extends **HTML** attributes with Directives, and binds data to **HTML** with Expressions. To learn more about AngularJS refer the following link

[http://www.w3schools.com/angular/default.asp](http://www.w3schools.com/angular/default.asp)

**Slider** widget is provided with AngularJS support. The support is achieved by including the “**ej.widget.angular.min.js**” file. Refer the following link to know more about the AngularJS support.

<https://help.syncfusion.com/js/angularjs>

**Slider** widget is defined using the directive **slider**. The properties of the **Slider** widget can be included as inline **HTML** attributes by prefixing the properties with “**e-**“. The properties are not case sensitive when defining it. AngularJS provides two types of data binding “one way binding” and “two way binding”. 

All properties in the slider supports one way data binding. Here one way binding specifies that the values for the slider properties are assigned automatically when specified through the data binding notation, but the property values is not changed in the model. That is, the values are displayed only in the **HTML** view not in the application data.

The **Slider** properties **value** and **values** are provided with two way binding support. The changes made to these properties are reflected both in the application data (model) and in **HTML** view.

The following example explains you the binding of **value** property using the AngularJS support.

{% highlight html %}



<head>
     <title>Slider</title>
     <link href="http://cdn.syncfusion.com/js/web/ej.widgets.core.min.css" rel="stylesheet" />
     <link href="http://cdn.syncfusion.com/js/web/flat-azure/ej.theme.min.css" rel="stylesheet" />
     <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
     <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>
     <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
     <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
</head>


{% endhighlight %}



{% highlight html %}


<!-- Add this code in your html page -->

<body ng-app="syncApp" ng-controller="SliderCtrl">
    <div class="frame">
        <div id="sliderContainer" class="control">
            <div id="rangeSlider" ej-slider e-width="width" e-value="sliderValue"></div>
            <h5><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 25px;"></span></h5>
        </div>
        <div id="binding">
            <input type="text" name="slider" class="input ejinputtext" value="" ng-model="sliderValue" />
        </div>
    </div>
</body>


{% endhighlight %}



{% highlight javascript %}



        //In JavaScript, bind the “value” and “width” property in Angular way as follows,
        // declaration                   
        angular.module('syncApp', ['ejangular'])
           .controller('SliderCtrl', function ($scope) {
               $scope.sliderValue = 60;
               $scope.width = "80%";
            });


{% endhighlight %}



Execute the above code example to render the following output.


![](/js/Slider/Integration_images/Integration_img1.png) 

## Knockout binding

KnockoutJS is a **JavaScript** library that follows the MVVM pattern to build sophisticated user interface with a clean underlying data model. It supports to update the UI dynamically. Refer the following link to know more about KnockoutJS.

[http://knockoutjs.com/documentation/introduction.html](http://knockoutjs.com/documentation/introduction.html)

**Slider** widget includes support to use it with KnockoutJS. The support is achieved by integration of the JS library **ej.widget.ko.min.js file.** Refer the following link to know more about the KnockoutJS support

<https://help.syncfusion.com/js/knockoutjs>

The binding handler name for **Slider** component is **Slider**. Both one way binding and two way binding support is included. All properties of the **Slider** component supports one way binding. In the **HTML** markup, specify the property using the binding handler. 

Two way binding support is included only for the applicable **Slider** properties, **value** and **values**. To activate two way binding support, you can specify these properties as observables in the **ViewModel**. Then use the **ko.applyBindings** to activate it. Now these properties binds the underlying data model and the changes is reflected automatically.

The following example explains you the binding of **value** property using the AngularJS support.


{% highlight html %}

<body>
    <div class="frame">
        <div id="sliderContainer" class="control">
            <div id="rangeSlider" data-bind="ejSlider: { value: sliderValue }"></div> 
        </div>
        <div id="binding">
            <input type="text" name="slider"  class="input ejinputtext" value="" data-bind="value: sliderValue" />
        </div>
    </div>
</body>


{% endhighlight %}

{% highlight javascript %}



        // In JavaScript, specify the “value” property as observable in the ViewModel to enable the two way binding.
        $(function () {
            // declaration            
            window.viewModel = {
                sliderValue: ko.observable(40),
            };
            ko.applyBindings(viewModel);
        });


{% endhighlight %}

Execute the above code example to render the following output.


![](/js/Slider/Integration_images/Integration_img2.png) 

