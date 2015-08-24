---
layout: post
title: Angular-Binding
description: angular binding
platform: js
control: PivotGrid
documentation: ug
---

# Angular Binding


AngularJS is a JavaScript framework added to a HTML page with a script tag. It extends HTML attributes with directives and binds data to HTML with expressions. AngularJS directives allow you to specify custom and reusable HTML tags that moderate the behavior of certain elements. Angular binding uses directives to plug its action into the page. Directives, all prefaced with ng-, are placed in HTML attributes.

In order to achieve **Angular Binding,** refer the following script files.

* angular.min.js
* ej.widget.angular.min.js

To use our Syncfusion widgets in AngularJS applications, all the EJ directives are encapsulated into a single module called ejangular. Therefore, in order to make use of Syncfusion widget’s angular features, you need to set your application’s module name as ejangular as depicted in the below sample code,

{% highlight js %}

angular.module('gridCtrl', ['ejangular'])
            .controller('PivotGridCtrl', function ($scope) {
                $scope.isResponsive = true;
                $scope.url = "../wcf/OLAPService.svc";
                $scope.gridLayout =  ej.PivotGrid.Layout.NoSummaries;
                $scope.layout = ["normal", "noSummaries", "normalTopSummary", "excelLikeLayout"];
            });

{% endhighlight %}

{% highlight html %}

<html xmlns="http://www.w3.org/1999/xhtml" ng-app="gridCtrl">

<body ng-controller="PivotGridCtrl">
    <div id="PivotGrid" ej-pivotgrid e-url="url" e-layout="gridLayout" e-isResponsive="isResponsive" />
</body>    
  

{% endhighlight %}


N>  This feature is applicable only for OLAP datasource.

