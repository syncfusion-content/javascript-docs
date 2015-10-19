---
layout: post
title: Ranges
description: ranges
platform: js
control: OlapGauge
documentation: ug
---

# Ranges

**Ranges** can be defined in OlapGauge using various attributes such as height and color, to measure the sensitivity of the actual value. 

* You can set the distance between the ranges and scales in OlapGauge using [distanceFromScale](/js/api/ejCircularGauge#scalesrangesdistancefromscalespan-classtype-signature-type-numbernumberspan) property.
* You can set the background color for the ranges in OlapGauge using [backgroundColor](/js/api/ejCircularGauge#scalesrangesbackgroundcolorspan-classtype-signature-type-stringstringspan) property.
* You can customize the Range size using  [size](/js/api/ejCircularGauge#scalesrangessizespan-classtype-signature-type-numbernumberspan) property.

{% highlight js %}

$(function() {
     $("#OlapGauge").ejOlapGauge({
         url: "../wcf/OlapGaugeService.svc",
         enableTooltip: true,
         load: "loadGaugeTheme",
         backgroundColor: "transparent",
         scales: [{
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
                 type: "needle",
                 showBackNeedle: true,
                 backNeedleLength: 20,
                 length: 120,
                 width: 9
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
                 distanceFromScale: 5,
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
                 distanceFromScale: -10,
                 size: 7,
                 backgroundColor: "black",
                 border: {
                     color: "#fc0606"
                 }
             }, {
                 distanceFromScale: -10,
                 size: 7
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
                     y: 330
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
                     y: 150
                 },
                 font: {
                     size: "12px",
                     fontFamily: "Segoe UI",
                     fontStyle: "Normal"
                 },
                 color: "#666666"
             }]
         }]
     });
 });

{% endhighlight %}

![](/js/OlapGauge/Ranges_images/Ranges_img1.png) 

