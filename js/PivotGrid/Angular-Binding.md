---
layout: post
title: Angular-Binding
description: angular binding
platform: js
control: PivotGrid
documentation: ug
---

### Angular Binding

>_**Note:** This feature is applicable only for OLAP datasource._

AngularJS is a JavaScript framework added to a HTML page with a script tag. It extends HTML attributes with directives and binds data to HTML with expressions. AngularJS directives allow you to specify custom and reusable HTML tags that moderate the behavior of certain elements. Angular binding uses directives to plug its action into the page. Directives, all prefaced with ng-, are placed in HTML attributes.

In order to achieve **Angular Binding,** refer the following script files.

* angular.min.js
* ej.widget.angular.min.js

Apply the plugin and property assigning the PivotGrid element through the directive that starts with the letter "e-". The following example depicts how to bind data to the PivotGrid control through Angular support.

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

<div id="PivotGrid" ej-pivotgrid e-url="url" e-layout="gridLayout" e-isResponsive="isResponsive" />

{% endhighlight %}



