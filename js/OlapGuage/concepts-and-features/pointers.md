---
layout: post
title: pointers
description: pointers
platform: js
control: OLAP Gauge
documentation: ug
---

# Pointers

**Pointers** are used to indicate the range on scale area based on the values passed for the range values.

## Types of Pointers

Two different types of pointer available in **OlapGuage** are:

1. Needle

2. Marker

## Changing Pointer Types

You can set the **pointer** to Needle type by setting “**pointerType**”****property to “**Needle**” and the pointer to Marker type by setting the “**pointerType”** properties to “**Marker**”.



{% highlight js %}

**[JS]**
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
                                    **type: "needle",**
                                    showBackNeedle: true,
                                    backNeedleLength: 20,
                                    length: 120,
                                    width: 7
                                },
                        {
**type: "marker",**
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
                                    backgroundColor: "#fc0606",
                                    border: { color: "#fc0606" }
                                }, {
                                    distanceFromScale: -5
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







{% include image.html url="\js\OlapGuage\concepts-and-features\pointers_images\pointers_img1.png" Caption="Figure: Pointer Type – Needle & Marker"%}

## Length and Width Customization

You can customize the **Pointer** length and width using the “**pointerLength**” and “**pointerWidth**” property.



{% highlight js %}

**[JS]**
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
**length: 60,**
                                    **width: 9**
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
                                    distanceFromScale: 2,
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
                                    backgroundColor: "#fc0606",
                                    border: { color: "#fc0606" }
                                }, {
                                    distanceFromScale: -5
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







{% include image.html url="\js\OlapGuage\concepts-and-features\pointers_images\pointers_img2.png" Caption="Figure: Length and Width Customization"%}

## Background Customization 

You can customize the **Pointer background** color using “**backgroundcolor**”****property.



{% highlight js %}

**[JS]**
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
**backgroundColor:"red",**
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
                 distanceFromScale: 2,
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
                 backgroundColor: "#fc0606",
                 border: { color: "#fc0606" }
             }, {
                 distanceFromScale: -5
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









{% include image.html url="\js\OlapGuage\concepts-and-features\pointers_images\pointers_img3.png" Caption="Figure: Background Color Customization"%}

## Shapes Customization

You can customize **Pointer****shapes** using the “**needlestyle**” property. 



{% highlight js %}

**[JS]**
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
**needleType: "rectangle",**
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
                                    distanceFromScale: 2,
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
                                    backgroundColor: "#fc0606",
                                    border: { color: "#fc0606" }
                                }, {
                                    distanceFromScale: -5
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







{% include image.html url="\js\OlapGuage\concepts-and-features\pointers_images\pointers_img4.png" Caption="Figure: Shape Customization"%}

