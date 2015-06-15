---
layout: post
title: Ticks
description: ticks
platform: js
control: OLAP Gauge
documentation: ug
---

### Ticks

**Ticks** indicate values that are present in the scale area. The different types of ticks available are:

    1. **Major Ticks** contains the range interval values.

    2. **Minor Ticks** contains only intervals between the major.

You can further customize **Ticks** by setting color, width and height.

{% highlight js %}

[JS]
$(function () {
$("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
                            load: "loadGaugeTheme", backgroundColor: "transparent",
                            scales: [{
                                showRanges: true,
                                radius: 150, showScaleBar: true, size: 1,
                                border: {
                                    width: 0.5
                                },
                                showIndicators: true, showLabels: true,
                                pointers: [{
                                    showBackNeedle: true,
                                    backNeedleLength: 20,
                                    length: 120,
                                    width: 7
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
**type: "major",distanceFromScale: 2,height: 16,width: 1, color: "red"**
                                },
                                { **type: "minor", height: 6, width: 1, distanceFromScale: 2, color: "blue"** }
                                ],
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



{% include image.html url="/js/OlapGauge/Concepts-and-Features/Ticks_images/Ticks_img1.png" Caption="Ticks Customization"%}

#### Customizing the distance from Scale

You can change the distance from the scale and the **Ticks** using “**distanceFromScale**” property.

{% highlight js %}

[JS]
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
**distanceFromScale: 15,**
                height: 16,
                width: 1, color: "#8c8c8c"
            },
            {
                type: "minor",
                height: 6,
                width: 1,
**distanceFromScale: 15,**
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



{% include image.html url="/js/OlapGauge/Concepts-and-Features/Ticks_images/Ticks_img2.png" Caption="Adjusting distance between Scale and Ticks"%}

#### Height and Width Customization

You can set the height and width of the **Ticks** using the “**tickWidth**” and “**tickHeight**” property.

{% highlight js %}

[JS]
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
**height: 18,**
                 **width: 2, color: "red"**
             },
             {
                 type: "minor",
                 **height: 8,**
                 **width: 2,**
                 distanceFromScale: 15,
                 color: "blue"
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



{% include image.html url="/js/OlapGauge/Concepts-and-Features/Ticks_images/Ticks_img3.png" Caption="Ticks height and width customization"%}

#### Hiding Ticks

You can hide the **Ticks** that indicate the range values using “**showTicks**” property.

{% highlight js %}

[JS]
$(function () {
$("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
        backgroundColor: "transparent", 
        scales: [{
            **showTicks: false,**
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



{% include image.html url="/js/OlapGauge/Concepts-and-Features/Ticks_images/Ticks_img4.png" Caption="Hiding Ticks"%}

