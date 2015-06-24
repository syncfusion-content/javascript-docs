---
layout: post
title: Angular-Binding
description: angular binding
platform: js
control: OlapChart
documentation: ug
---

#Angular Binding

AngularJS is a JavaScript framework added to a HTML page with a script tag. It extends HTML attributes with directives and binds data to HTML with expressions. AngularJS directives allow you to specify custom and reusable HTML tags that moderate the behavior of certain elements. Angular binding uses directives to plug its action into the page. Directives, all prefaced with ng-, are placed in HTML attributes.

In order to achieve **Angular Binding,** refer the following script files.

* angular.min.js
* ej.widget.angular.min.js

Apply the plugin and property assigning the OlapChart element through the directive that starts with the letter "e-". The following example depicts how to bind data to the OlapChart control through Angular support.

{% highlight js %}

angular.module('chartCtrl', ['ejangular'])
    .controller('OlapChartCtrl', function($scope) {
        $scope.url = "../wcf/OlapChartService.svc";
        $scope.title = "OlapChart in Essential JS";
        $scope.isResponsive = true;
        $scope.ctype = ej.olap.OlapChart.ChartTypes.Column;
        $scope.showTooltip = true;
        $scope.size = {
            height: "460px",
            width: "650px"
        };
        $scope.primaryXAxis = {
            title: {
                text: "Fiscal Year"
            },
            labelRotation: 0
        };
        $scope.primaryYAxis = {
            title: {
                text: "Customer Count"
            }
        };
        $scope.legend = {
            visible: true,
            rowCount: 2
        };
        $scope.list = ["column", "line", "spline", "area", "bar", "pie", "pyramid", "stepline", "splinearea", "steparea",
            "stackingarea", "stackingcolumn", "stackingbar", "funnel"
        ];
    });
{% endhighlight %}

{% highlight html %}

<div id="OlapChart" ej-olapchart e-url="url" e-title-text="title" e-showtooltip="showTooltip" e-isResponsive="isResponsive" e-animation="animation" e-commonseriesoptions-type="ctype" e-commonseriesoptions-tooltip-visible="showTooltip" e-size="size" e-primaryxaxis="primaryXAxis" e-primaryyaxis="primaryYAxis" e-legend="legend" e-load='loadTheme' />

{% endhighlight %}


