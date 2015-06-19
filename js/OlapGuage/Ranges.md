---
layout: post
title: Ranges
description: ranges
platform: js
control: OLAP Gauge
documentation: ug
---

# Ranges

**Ranges** are objects that highlight a range of values and can display different ranges in different colors. You can customize **Ranges** using various attributes such as height, color of the range. 

## Distance from Scale

You can set the distance between the **ranges** and scales in **OlapGauge** using “**distanceFromScale”**.

{% highlight js %}

$(function () {
 $("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
                            backgroundColor: "transparent", 
                            scales: [{
                                showRanges: true, 
                                radius: 150, showScaleBar: true, size: 1,
                                border: {
                                    width: 0.5
                                },
                                showIndicators: true, showLabels: true,
                                pointers: [{
                                    type: "needle",
                                    showBackNeedle: true,
                                    backNeedleLength: 20,
                                    length: 120,
                                    width: 9
                                },
                        {
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
                                    distanceFromScale: 15,
                                    height: 16,
                                    width: 1, color: "#8c8c8c"
                                },
                                {
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
                                    **distanceFromScale: -10,**
                                    backgroundColor: "#fc0606",
                                    border: {color: "#fc0606"}
                                }, {
                                    **distanceFromScale: -10,**
                                }],
                                customLabels: [{
                                    position: { x: 180, y: 290 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, {
                                    position: { x: 180, y: 320 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, {
                                    position: { x: 180, y: 150 },
                                    font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }]
                            }]
                        });
                    });


{% endhighlight %}

## Style Customization 

You can set the background color for the **ranges** in **OlapGauge** using “**backgroundColor**”.

{% highlight js %}

$(function () {
$("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
                            backgroundColor: "transparent", 
                            scales: [{
                                showRanges: true, 
                                radius: 150, showScaleBar: true, size: 1,
                                border: {
                                    width: 0.5
                                },
                                showIndicators: true, showLabels: true,
                                pointers: [{
                                    type: "needle",
                                    showBackNeedle: true,
                                    backNeedleLength: 20,
                                    length: 120,
                                    width: 9
                                },
                        {
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
                                    distanceFromScale: 15,
                                    height: 16,
                                    width: 1, color: "#8c8c8c"
                                },
                                {
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
                                    **backgroundColor: "black",**
                                    **border: {color: "red"}**
                                }, {
                                    distanceFromScale: -5,
                                }],
                                customLabels: [{
                                    position: { x: 180, y: 290 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, {
                                    position: { x: 180, y: 320 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, {
                                    position: { x: 180, y: 150 },
                                    font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }]
                            }]
                        });
                    });


{% endhighlight %}

{% include image.html url="/js/OlapGauge/Concepts-and-Features/Ranges_images/Ranges_img1.png" Caption="Range style customization"%}

## Size Setting

You can customize the **Range size** using “**size**” property.

{% highlight js %}

$(function () {
     $("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
         backgroundColor: "transparent", 
         scales: [{
             showRanges: true, 
             radius: 150, showScaleBar: true, size: 1,
             border: {
                 width: 0.5
             },
             showIndicators: true, showLabels: true,
             pointers: [{
                 type: "needle",
                 showBackNeedle: true,
                 backNeedleLength: 20,
                 length: 120,
                 width: 9
             },
     {
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
                 distanceFromScale: 15,
                 height: 16,
                 width: 1, color: "#8c8c8c"
             },
             {
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
                 distanceFromScale: -5,size:7,
                 backgroundColor: "#fc0606",
                 border: {color: "#fc0606"}
             }, {
                 distanceFromScale: -5, size: 7
             }],
             customLabels: [{
                 position: { x: 180, y: 290 },
                 font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }, {
                 position: { x: 180, y: 320 },
                 font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }, {
                 position: { x: 180, y: 150 },
                 font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }]
         }]
     });
 });

{% endhighlight %}

{% include image.html url="/js/OlapGauge/Concepts-and-Features/Ranges_images/Ranges_img2.png" Caption="Range Size Setting"%}

