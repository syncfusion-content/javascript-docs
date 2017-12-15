---
layout: post
title: Data-Binding
description: data binding
platform: js
control: Rotator
documentation: ug
api: /api/js/ejrotator
---

# Data Binding

**Rotator** provides a flexible approach for binding the data from various data sources. There are various properties in **Toolbar** for **Data Binding**. The value set to this property is **object** type.

## Data fields and Configuration

The following sub-properties provide a way to bind the data either locally/remotely to the **Rotator** control. The value set to this property is **object** type.

## DataSource

This property specifies the list of data that contains a set of data fields. Each data value is used to render an item for the **Rotator**. The value set to this property is **object** type.

## Fields

It defines mapping fields for the data items of the **Rotator**. The value set to this property is **object** type.

## Text

It specifies the text content of the tag. The value set to this property is **string** type.

## URL

This property specifies the **URL** for an image. The value set to this property is **string** type.

## Query

This property retrieves data from remote data. This property is applicable only when a remote data source is used. Each data value is used to render an item for the **Rotator**. The value set to this property is **object** type.

## Local data binding

**Rotator** provides the data binding support for the **Rotator** **item**. So you can bind the data from **JSON** **Data**. For this behavior, you need to map the corresponding filed with their column names. The data can be bound as a list and it is assigned to [dataSource](https://help.syncfusion.com/api/js/ejrotator#members:datasource) property. You can refer the following code example to bind local data.

  {% highlight html %}

<div class="cols-sample-area">
  <ul id="sliderContent"></ul>
</div>

  {% endhighlight %}


  {% highlight javascript %}

    $(function () {
        // declaration
        var website = [
      { text: "Beautiful Bird", url: "../images/rotator/bird.jpg" },
      { text: "Colorful Night", url: "../images/rotator/night.jpg" },
      { text: "Technology", url: "../images/rotator/tablet.jpg" },
      { text: "Nature", url: "../images/rotator/nature.jpg" },
      { text: "Snow Fall", url: "../images/rotator/snowfall.jpg" },
      { text: "Credit Card", url: "../images/rotator/card.jpg" },
      { text: "Amazing Sculptures", url: "../images/rotator/sculpture.jpg" }
        ];
        $("#sliderContent").ejRotator({
            slideWidth: "600px",
            frameSpace: "0px",
            displayItemsCount: "1",
            slideHeight: "350px",
            navigateSteps: "1",
            enableResize: true,
            pagerPosition: ej.Rotator.PagerPosition.Outside,
            dataSource: website,
            orientation: ej.Orientation.Horizontal,
            showPager: true,
            enabled: true,
            showCaption: true,
            allowKeyboardNavigation: true,
            enableRTL: true,
            showPlayButton: true,
            animationType: "slide"
        });
    });

  {% endhighlight %}


![](/js/Rotator/Data-Binding_images/Data-Binding_img1.png)

## KnockoutJS support

**Knockout** support allows you to bind the **HTML** elements against any of the available data models.

Two types of **Knockout** binding are supported,

* One-way binding
* Two-way binding

**One way binding** refers to the process of applying observable values to all the available properties of the **Rotator**. But the changes made in **Rotator** widget are not reflected and triggered in turn to the observable collection. This kind of binding is applied to all the properties of the **Rotator**.

**Two-way binding** supports both the processes – it applies the observable values to the **Rotator** properties as well as the changes made in the **Rotator** widget are also reflected back and triggered within the observable collections. 

For more information about the **Knockout** binding, you can refer the online documentation in the following link location,

<https://help.syncfusion.com/js/knockoutjs>

Add the following script files along with the given code to access KnockoutJS binding. They have JS library for KnockoutJS binding.

 
* knockout-min.js
* ej.widget.ko.min.js

The link for those script files are as follows:

[http://cdn.syncfusion.com/js/assets/external/knockout.min.js](http://cdn.syncfusion.com/js/assets/external/knockout.min.js)

[http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js)

The following code example depicts the way to bind data to the **Rotator** through the **Knockout** support.

  {% highlight html %}

  
<body data-autoinit="false">
  <div class="cols-sample-area">
      <ul id="sliderContent" data-bind="ejRotator :{dataSource:dataList,slideWidth:width,slideHeight:height}" />
  </div>
</body>

  {% endhighlight %}


  {% highlight javascript %}

    $(function () {
        var imageList = [
          { text: "bird", url: "../images/rotator/bird.jpg" },
          { text: "night", url: "../images/rotator/night.jpg" },
          { text: "tablet", url: "../images/rotator/tablet.jpg" },
          { text: "nature", url: "../images/rotator/nature.jpg" },
          { text: "snowfall", url: "../images/rotator/snowfall.jpg" },
          { text: "card", url: "../images/rotator/card.jpg" },
          { text: "sculpture", url: "../images/rotator/sculpture.jpg" }
        ];
    
        window.viewModel = {
            dataList: ko.observableArray(imageList),
            height: ko.observable("350px"),
            width: ko.observable("600px"),
        };
        ko.applyBindings(viewModel);
    });
	

  {% endhighlight %}

![](/js/Rotator/Data-Binding_images/Data-Binding_img2.png) 

## AngularJS support

Rotator is availed with two types of AngularJS support namely, 

* One way binding
* Two way binding 

**One way binding** refers to the process of applying scope values to all the available properties of the Rotator. But the changes made in **Rotator** widget are not reflected or triggered in turn to the scope collection. This kind of binding is applied to all the properties of the **Rotator**.

**Two-way binding** supports both the processes – it applies the scope values to the **Rotator** properties as well as the changes made in the **Rotator** widget are also reflected back and triggered within the AngularJS scope change function.

To know more details about the **AngularJS** **binding**, you can refer the following link location,

<https://help.syncfusion.com/js/angularjs>

Add the following script files as given in the following example to access AngularJS binding. They have JS library for AngularJS binding.



* angular-min.js
* ej.widget.angular.min.js

The following code example depicts the way to bind data to the **Rotator** widget through **AngularJS** support.

{% highlight html %}

<!DOCTYPE html>
<html lang="en" ng-app="rotatorApp">
   <head>
      <title>Essential Studio for JavaScript :AngularJS Support for Toolbar</title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <!--scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
      <script src="[http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js"></script>
   </head>
   <body ng-controller="RotatorCtrl">
      <div class="cols-sample-area">
         <ul id="sliderContent" ej-rotator e-datasource="dataList" e-slidewidth="600px" e-slideheight="350px" />
      </div>
   </body>
</html>


{% endhighlight %}



{% highlight javascript %}


    var list = [
      { text: "snowfall", url: "../images/rotator/snowfall.jpg" },
      { text: "tablet", url: "../images/rotator/tablet.jpg" },
      { text: "nature", url: "../images/rotator/nature.jpg" },
      { text: "card", url: "../images/rotator/card.jpg" },
      { text: "bird", url: "../images/rotator/bird.jpg" },
      { text: "wheat", url: "../images/rotator/wheat.jpg" },
      { text: "night", url: "../images/rotator/night.jpg" }];
    
    angular.module('rotatorApp', ['ejangular']).controller('RotatorCtrl', function ($scope) {
        $scope.dataList = list;
    });



{% endhighlight %}



![](/js/Rotator/Data-Binding_images/Data-Binding_img3.png)

