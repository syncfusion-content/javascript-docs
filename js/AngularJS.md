---
layout: post
title: AngularJS
description: angularjs
platform: js
control: Introduction
documentation: ug
---

# AngularJS

**Essential JavaScript** has a complete support for [AngularJS](https://docs.angularjs.org/tutorial/step_02) by integrating a required angular JS library file. It lets you use HTML as your template language and lets you extend the HTML's syntax to express the application's components clearly. This support mainly covers the following topics, 

* Module
* Directives
* Controller
* Data Binding

## Required JavaScript libraries

The following two JavaScript libraries are necessary to create AngularJS applications,

* angular.min.js
* ej.widget.angular.min.js

You can find the common **angular.min.js** from the following installed location of your machine,

<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external
</td>
</tr>
<tr>
<td> 
<b>For example</b>, If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external
</td>
</tr>
</table>


The **ej.widget.angular.min.js** file can be copied from the below specified location,

<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\common 
</td>
</tr>
<tr>
<td>
<b>For example</b>, If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\common
</td>
</tr>
</table>


## Directives

In general, AngularJS directives are extended HTML attributes with the prefix **ng-**. The **ng-app** directive is a common directive that normally initializes the AngularJS applications. To do so, we need to define it in the &lt;html&gt; tag as depicted below,

{% highlight html %}


<html xmlns="http://www.w3.org/1999/xhtml" ng-app="DateCtrl">
  <head>
    <title>Essential Studio for JavaScript - Angular</title>
  </head>
  …
  …
</html>

{% endhighlight %}

All the Syncfusion widget’s **control directives** are prefixed with **ej-** to avoid conflict with other library directives and its properties are defined using **e-** prefix followed by the property name. The code example for defining controls in **AngularJS** is as follows,

{% highlight html %}


<html xmlns="http://www.w3.org/1999/xhtml" ng-app="DateCtrl">
  <head>
    <title>Essential Studio for JavaScript : DatePicker - Angular</title>
  </head>
  <body ng-controller="DatePickerCtrl">
    <input id="datepick" ej-datepicker e-value="dateValue" e-enableStrictMode="true" />
  </body>
</html>

{% endhighlight %}

In the above code snippet, **ej-datepicker** denotes the control directive for the Syncfusion’s datepicker widget and all its properties are prefixed with the letter **e-** (For example, **e-value**).

## Controller

AngularJS applications are controlled by the Controllers, which maintains the entire data of the application. Usually, it is defined by the keyword **ng-controller** within the &lt;body&gt; tag as shown below,

{% highlight html %}

<html xmlns="http://www.w3.org/1999/xhtml" ng-app="DateCtrl">
  <head>
    <title>Essential Studio for JavaScript : DatePicker - Angular</title>
  </head>
  <body ng-controller="DatePickerCtrl">
    <input id="datepick" ej-datepicker  e-value="dateValue" e-enableStrictMode="true" />
  </body>
</html>

{% endhighlight %}

## Module

A **Module** is a container for the various parts of an application that we create and it mainly defines an application. All the controllers within an application should belong to this module.

To use our Syncfusion widgets in AngularJS applications, all the EJ directives are encapsulated into a single module called **ejangular**. Therefore, in order to make use of Syncfusion widget’s angular features, you need to set your application’s module name as **ejangular** as depicted in the below sample code, 

{% highlight js %}

angular.module('DateCtrl', ['ejangular'])
     .controller('DatePickerCtrl', function ($scope) {
         $scope.dateValue = "2/3/2013";
});

{% endhighlight %}

## Data binding

Data-binding can be defined as an automatic synchronization of data between model and View components. Our Syncfusion widgets supports both one-way and two-way (**ng-model**) binding.

### One way binding

It is said one-way binding because the model values are directly bound to the widget’s properties and the changes in the property’s value won’t reflect in the model in any way. **All the properties of Syncfusion widgets support one-way binding**. The below code defines the one-way binding depicted in the DatePicker widget,

{% highlight html %}

    <input id="datepick" ej-datepicker  e-value="01/01/2015" e-enableStrictMode="true" />

{% endhighlight %}

Here, in the above code, the value property of the DatePicker widget is assigned with the direct value **01/01/2015**. Therefore, whenever we change the value of the DatePicker dynamically, the changes won’t get reflected in the value property.

### Two way binding

A two-way data binding can be defined as, when a model variable is bound to the widget’s properties instead of direct values, it can both change and display the value of the variable. In general, we could have more than one property bound to the same variable. 

#### Two way binding properties

The below table depicts the properties of all the Syncfusion widgets that supports two-way data-binding - 

<table>
<tr>
<th>
Control</th><th>
Supported Two way binding properties</th></tr>
<tr>
<td>
ejAccordion</td><td>
-</td></tr>
<tr>
<td>
ejAutocomplete</td><td>
value</td></tr>
<tr>
<td>
ejBarcode</td><td>
-</td></tr>
<tr>
<td>
ejBulletgraph</td><td>
value<br/>comparativeMeasureValue</td></tr>
<tr>
<td>
ejButton</td><td>
-</td></tr>
<tr>
<td>
ejChart</td><td>
xZoomFactor<br/>yZoomFactor<br/>xZoomPosition<br/>yZoomPosition </td></tr>
<tr>
<td>
ejCheckBox</td><td>
-</td></tr>
<tr>
<td>
ejCircularGauge</td><td>
value<br/>minimum<br/>maximum</td></tr>
<tr>
<td>
ejDatePicker</td><td>
value</td></tr>
<tr>
<td>
ejDateTimePicker</td><td>
value</td></tr>
<tr>
<td>
ejDiagram</td><td>
-</td></tr>
<tr>
<td>
ejDialog</td><td>
-</td></tr>
<tr>
<td>
ejDigitalGauge</td><td>
value</td></tr>
<tr>
<td>
ejDropDownList</td><td>
value</td></tr>
<tr>
<td>
ejGantt</td><td>
selectedItem</td></tr>
<tr>
<td>
ejGrid</td><td>
dataSource<br/>selectedRow<br/>pageSettings.currentPage</td></tr>
<tr>
<td>
ejLinearGauge</td><td>
value<br/>minimum<br/>maximum</td></tr>
<tr>
<td>
ejMaps</td><td>
zoomLevel<br/>minZoom<br/>zoomFactor<br/>maxZoom<br/>baseMapIndex</td></tr>
<tr>
<td>
ejMaskEdit</td><td>
value</td></tr>
<tr>
<td>
ejMenu</td><td>
-</td></tr>
<tr>
<td>
ejOlapChart</td><td>
title.text<br/>commonSeriesOptions.type<br/>locale</td></tr>
<tr>
<td>
ejOlapClient</td><td>
Title<br/>gridLayout<br/>displaySettings.mode<br/>displaySettings.defaultView<br/>displaySettings.controlPlacement<br/>displaySettings.enableTogglePanel<br/>locale </td></tr>
<tr>
<td>
ejOlapGauge</td><td>
rowsCount<br/>columnsCount<br/>showHeaderLabel<br/>locale<br/>radius<br/>frameType </td></tr>
<tr>
<td>
ejPivotGrid</td><td>
Layout<br/>enableCellContext<br/>hyperlinkSettings.enableValueCellHyperlink<br/>hyperlinkSettings.enableRowHeaderHyperlink<br/>hyperlinkSettings.enableColumnHeaderHyperlink<br/>hyperlinkSettings.enableSummaryCellHyperlink </td></tr>
<tr>
<td>
ejRadioButton</td><td>
-</td></tr>
<tr>
<td>
ejRangeNavigator</td><td>
-</td></tr>
<tr>
<td>
ejRating</td><td>
currentValue</td></tr>
<tr>
<td>
ejRTE</td><td>
value</td></tr>
<tr>
<td>
ejRotator</td><td>
-</td></tr>
<tr>
<td>
ejSchedule</td><td>
fields.dataSource<br/>currentView<br/>currentDate</td></tr>
<tr>
<td>
ejScroller</td><td>
scrollTop<br/>  scrollLeft</td></tr>
<tr>
<td>
ejSlider</td><td>
value <br/> values</td></tr>
<tr>
<td>
ejSplitButton</td><td>
-</td></tr>
<tr>
<td>
ejSpliter</td><td>
-</td></tr>
<tr>
<td>
ejTab</td><td>
-</td></tr>
<tr>
<td>
ejTagCloud</td><td>
-</td></tr>
<tr>
<td>
ejNumericTextbox</td><td>
value</td></tr>
<tr>
<td>
ejPercentageTextbox</td><td>
value</td></tr>
<tr>
<td>
ejCurrencyTextbox</td><td>
value</td></tr>
<tr>
<td>
ejTimePicker</td><td>
value</td></tr>
<tr>
<td>
ejToggleButton</td><td>
-</td></tr>
<tr>
<td>
ejToolbar</td><td>
-</td></tr>
<tr>
<td>
ejTreemap</td><td>
dataSource<br/>colorValuePath<br/>weightValuePath</td></tr>
<tr>
<td>
ejTreeView</td><td>
-</td></tr>
<tr>
<td>
ejUploadbox</td><td>
-</td></tr>
<tr>
<td>
ejWaitingPopup</td><td>
-</td></tr>
</table>


The two-way data binding has been demonstrated in the below code,

{% highlight html %}


<html xmlns="http://www.w3.org/1999/xhtml" ng-app="DateCtrl">
  <head>
    <title>Essential Studio for JavaScript : DatePicker - Angular</title>
    <!-- SCRIPT & CSS REFERENCE SECTION -->
  </head>
  <body ng-controller="DatePickerCtrl">
    <input id="mydatepicker1" ej-datepicker  e-value="dateValue" e-enableStrictMode="true" />
    <input id="mydatepicker2" ej-datepicker  e-value="dateValue" e-enableStrictMode="true" />
    <script type="text/javascript">
        angular.module('DateCtrl', ['ejangular'])
           .controller('DatePickerCtrl', function ($scope) {
               $scope.dateValue = "01/01/2015";
        });
    </script>
  </body>
</html>

{% endhighlight %}

Here, just for the demonstration purpose, we are using two DatePicker controls (with id **mydatepicker1** and **mydatepicker2**), both of its value property is bound to the scope variable **dateValue**. Initially, both the DatePickers will be displayed with the value **01/01/2015** and whenever any of the DatePicker’s value is changed dynamically, it gets simultaneously reflected in another DatePicker too, as both of them shared the same scope variable.

Though AngularJS comes with lot of advantages, at the same time it has some serious issues too - that the application written in AngularJS are not safe due to the pure JavaScript framework. Therefore, to overcome such issue, some kind of server-side authentication and authorization is necessary to keep the application more secure. 

