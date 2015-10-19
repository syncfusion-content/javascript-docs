---
layout: post
title: Frame-Type
description: frame type 
platform: js
control: OlapGauge
documentation: ug
---

# Frame Type 

**OlapGauge** supports built-in frame types to provide effective rim styles.

   1. Full Circle - displays full view of the OlapGauge.
   2. Half Circle - displays half view of the OlapGauge.

## Full Circle

By default, frame type is `fullcircle`. You can also set frame type with [frameType](/js/api/ejCircularGauge#frameframetypespan-classtype-signature-type-enumenumspan) property.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
        url: "../wcf/OlapGaugeService.svc",
        enableTooltip: true,
        load: "loadGaugeTheme",
        backgroundColor: "transparent",
        frameType: "fullcircle",
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
                showBackNeedle: true,
                backNeedleLength: 20,
                length: 120,
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

![](/js/OlapGauge/Frame-Type_images/Frame-Type_img1.png) 

## Half Circle

You can set frame type as `halfcircle` with the help of [frameType](/js/api/ejCircularGauge#frameframetypespan-classtype-signature-type-enumenumspan) property to visualize the gauge control in **half circle**.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
        url: "../wcf/OlapGaugeService.svc",
        enableTooltip: true,
        load: "loadGaugeTheme",
        backgroundColor: "transparent",
        frameType: "halfcircle",
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
                showBackNeedle: true,
                backNeedleLength: 20,
                length: 120,
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

![](/js/OlapGauge/Frame-Type_images/Frame-Type_img2.png) 

