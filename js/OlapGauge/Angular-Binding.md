---
layout: post
title: Angular-Binding
description: angular binding
platform: js
control: OlapGauge
documentation: ug
---

# Angular Binding

AngularJS is a JavaScript framework added to a HTML page with a script tag. It extends HTML attributes with directives and binds data to HTML with expressions. AngularJS directives allow you to specify custom and reusable HTML tags that moderate the behavior of certain elements. Angular binding uses directives to plug its action into the page. Directives, all prefaced with ng-, are placed in HTML attributes.

In order to achieve **Angular Binding,** refer the following script files.

* angular.min.js
* ej.widget.angular.min.js

Apply the plugin and property assigning the OlapGauge element through the directive that starts with the letter "e-". The following example depicts how to bind data to the OlapGauge control through Angular support.

{% highlight js %}

angular.module('gaugeCtrl', ['ejangular'])
    .controller('OlapGaugeCtrl', function($scope) {
        $scope.url = "../wcf/OlapGaugeService.svc";
        $scope.enableTooltip = true;
        $scope.rowsCount = 2;
        $scope.columnsCount = 3;
        $scope.scales = scale;
        $scope.backgroundColor = "transparent";
    });
    
{% endhighlight %}

{% highlight html %}

<div id="OlapGauge" ej-olapgauge e-url="url" e-enabletooltip="enableTooltip" e-rowscount="rowsCount" e-columnscount="columnsCount" e-scales="scales" e-load="loadGaugeTheme" e-backgroundcolor="backgroundColor" />

{% endhighlight %}



