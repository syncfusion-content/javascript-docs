---
layout: post
title: Angular-Binding
description: angular binding
platform: js
control: OlapGauge
documentation: ug
---

# Angular Binding

In order to achieve **Angular Binding,** refer the following script files.

* angular.min.js
* ej.widget.angular.min.js

Apply the plugin and property assigning the OlapGauge element through the directive that starts with the letter "e-". The following example depicts how to bind data to the OlapGauge control through Angular support.

{% highlight js %}

 var scale = [{
     showRanges: true,
     radius: 150,
     showScaleBar: true,
     size: 1,
     border: {
         width: 0.5
     },
     showIndicators: true,
     showLabels: true,
     pointers: [{
         showBackNeedle: true,
         backNeedleLength: 20,
         length: 125,
         width: 7
     }, {
         type: "marker",
         markerType: "diamond",
         distanceFromScale: 5,
         placement: "center",
         backgroundColor: "#29A4D9",
         length: 25,
         width: 15
     }],
     ticks: [{
         type: "major",
         distanceFromScale: 2,
         height: 16,
         width: 1,
         color: "#8c8c8c"
     }, {
         type: "minor",
         height: 6,
         width: 1,
         distanceFromScale: 2,
         color: "#8c8c8c"
     }],
     labels: [{
         color: "#8c8c8c"
     }],
     ranges: [{
         distanceFromScale: -5,
         backgroundColor: "#fc0606",
         border: {
             color: "#fc0606"
         }
     }, {
         distanceFromScale: -5
     }],
     customLabels: [{
         position: {
             x: 180,
             y: 290
         },
         font: {
             size: "10px",
             fontFamily: "Segoe UI",
             fontStyle: "Normal"
         },
         color: "#666666"
     }, {
         position: {
             x: 180,
             y: 320
         },
         font: {
             size: "10px",
             fontFamily: "Segoe UI",
             fontStyle: "Normal"
         },
         lcolor: "#666666"
     }, {
         position: {
             x: 180,
             y: 150
         },
         font: {
             size: "12px",
             fontFamily: "Segoe UI",
             fontStyle: "Normal"
         },
         color: "#666666"
     }]
 }];
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

<html xmlns="http://www.w3.org/1999/xhtml" ng-app="gaugeCtrl">
    
<body ng-controller="OlapGaugeCtrl">
    <div id="Div1" ej-olapgauge e-url="url" e-enabletooltip="enableTooltip" e-rowscount="rowsCount" e-columnscount="columnsCount" e-scales="scales" e-load="loadGaugeTheme" e-backgroundcolor="backgroundColor" />
</body>

{% endhighlight %}



