---
layout: post
title: Angular-Binding
description: angular binding
platform: js
control: OLAP Client
documentation: ug
---

## Angular Binding

AngularJS is a JavaScript framework added to a HTML page with a script tag. It extends HTML attributes with directives and binds data to HTML with expressions. AngularJS directives allow you to specify custom and reusable HTML tags that moderate the behavior of certain elements. Angular binding uses directives to plug its action into the page. Directives, all prefaced with ng-, are placed in HTML attributes.

In order to achieve **Angular Binding,** refer the following script files.

* angular.min.js

* ej.widget.angular.min.js

Apply the plugin and property assigning the OlapClient element through the directive that starts with the letter "e-". The following example depicts how to bind data to the OlapClient control through Angular support.

{% highlight js %}

angular.module('clientCtrl', ['ejangular'])
            .controller('OlapClientCtrl', function ($scope) {
                $scope.url = "../wcf/OlapClientService.svc";
                $scope.title = "OLAP Browser";
                $scope.gridLayout =  ej.PivotGrid.Layout.NoSummaries;
                $scope.displaySettings = { mode: ej.olap.OlapClient.DisplayMode.ChartAndGrid,
                    defaultView: ej.olap.OlapClient.DefaultView.Grid
                };
                $scope.layout = ["normal", "noSummaries", "normalTopSummary", "excelLikeLayout"];
            });

{% endhighlight %}

{% highlight html %}

<div id="OlapClient" ej-olapclient e-url="url" e-title="title" e-gridlayout="gridLayout" e-displayoptions="displaySettings" e-chartload='setChartProperties' />

{% endhighlight %}



