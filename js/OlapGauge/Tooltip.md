---
layout: post
title: Tooltip
description: tooltip
platform: js
control: OlapGauge
documentation: ug
---

# Tooltip

**Tooltip** provides the information about the **OlapGauge** when you move the mouse pointer over the control. You can enable it using "**showtooltip**”  property.

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
             size: 7,
             backgroundColor: "#fc0606",
             border: {
                 color: "#fc0606"
             }
         }, {
             distanceFromScale: -5,
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
         }]
     }]
 });
});
{% endhighlight %}

## Customizing the tooltip using CSS

You can customize the **Tooltip** by overriding the existing style attributes and referring it in web page.

{% highlight css %}

.e - olapgauge - tooltip {
    background - color: aqua!important;
    border: 2 px solid red!important;
    color: black!important;
    border - radius: 18 px!important;
    margin - top: 20 px;
    text - align: left;
    font: 12 px Segoe UI;
    line - height: 20 px;
}
{% endhighlight %}

{% include image.html url="/js/OlapGauge/Tooltip_images/Tooltip_img1.png" %}

