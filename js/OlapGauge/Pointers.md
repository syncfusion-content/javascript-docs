---
layout: post
title: Pointers
description: pointers
platform: js
control: OlapGauge
documentation: ug
---

# Pointers

**Pointers** are used to indicate the range on scale area based on the values passed for the range values.

## Types of Pointers

Two different types of pointer available in **OlapGauge** are:

   1. Needle
   2. Marker

## Changing Pointer Types

You can set the **pointer** to Needle type by setting [type](/js/api/ejCircularGauge#scalespointerstypespan-classtype-signature-type-enumenumspan)  property to “**Needle**” and the pointer to Marker type by setting the [type](/js/api/ejCircularGauge#scalespointerstypespan-classtype-signature-type-enumenumspan) properties to  “**Marker**”.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
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
            pointers: [{ ** type: "needle", **
                    showBackNeedle: true,
                    backNeedleLength: 20,
                    length: 120,
                    width: 7
            }, { ** type: "marker", **
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

{% include image.html url="/js/OlapGauge/Pointers_images/Pointers_img1.png" %}

## Length and Width Customization

You can customize the **Pointer** length and width using the [length](/js/api/ejCircularGauge#scalespointerslengthspan-classtype-signature-type-numbernumberspan) and [width](/js/api/ejCircularGauge#scalespointerswidthspan-classtype-signature-type-numbernumberspan) property.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
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
                ** length: 60,**
                ** width: 9 **
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

{% include image.html url="/js/OlapGauge/Pointers_images/Pointers_img2.png" %}

## Background Customization 

You can customize the **Pointer background** color using [backgroundcolor](/js/api/ejCircularGauge#scalespointersbackgroundcolorspan-classtype-signature-type-stringstringspan) property.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
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
                ** backgroundColor: "red",**
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

{% include image.html url="/js/OlapGauge/Pointers_images/Pointers_img3.png" %}

## Shapes Customization

You can customize **Pointer shapes** using the [needleType](/js/api/ejCircularGauge#scalespointersneedletypespan-classtype-signature-type-enumenumspan) property. 

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
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
                needleType: "rectangle",
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

{% include image.html url="/js/OlapGauge/Pointers_images/Pointers_img4.png" %}

