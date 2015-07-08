---
layout: post
title: Scales and Pointers
description: Scales and Pointers
platform: js
control: OlapGauge
documentation: ug
---

# Scales and Pointers

**Scale** is a basic unit of **radial gauge**. You can customize the gauge scales by using properties such as radius, minimum, scale direction, interval values etc. Radius of the **Scale** is changed with the help of [radius](/js/api/ejCircularGauge#scalesradiusspan-classtype-signature-type-numbernumberspan) property and in order to make Scale visible, set [showScaleBar](/js/api/ejCircularGauge#scalesshowscalebarspan-classtype-signature-type-booleanbooleanspan) property to ‘**true’**. You can set size of the Scale with the help of [size](/js/api/ejCircularGauge#scalessizespan-classtype-signature-type-numbernumberspan) and border width using [width](/js/api/ejCircularGauge#scalesborderwidthspan-classtype-signature-type-numbernumberspan) property**.** 

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
        url: "../wcf/OlapGaugeService.svc",
        enableTooltip: true,
        load: "loadGaugeTheme",
        backgroundColor: "transparent",
        scales: [{
            showRanges: true,
            radius: 180,
            showScaleBar: true,
            size: 2,
            border: { 
               width: 2.5 
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
                    y: 320
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

{% include image.html url="/js/OlapGauge/Scales_images/Scales_img1.png" %}

## Pointers

**Pointers** are used to indicate the range on scale area based on the values passed for the range values.

* You can customize the Pointer type using [type](/js/api/ejCircularGauge#scalespointerstypespan-classtype-signature-type-enumenumspan) property.
* You can customize the Pointer length and width using the [length](/js/api/ejCircularGauge#scalespointerslengthspan-classtype-signature-type-numbernumberspan) and [width](/js/api/ejCircularGauge#scalespointerswidthspan-classtype-signature-type-numbernumberspan) property.
* You can customize Pointer shapes using the [needleType](/js/api/ejCircularGauge#scalespointersneedletypespan-classtype-signature-type-enumenumspan) property.

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
                backgroundColor: "red",
                needleType: "rectangle",
                length: 60,
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

{% include image.html url="/js/OlapGauge/Scales_images/Pointers_img1.png" %}


## Ticks

**Ticks** indicate values that are present in the scale area. The different types of ticks available are:

* You can further customize Ticks by setting [color](/js/api/ejCircularGauge#scalestickscolorspan-classtype-signature-type-stringstringspan), [width](/js/api/ejCircularGauge#scalestickswidthspan-classtype-signature-type-numbernumberspan) and [height](/js/api/ejCircularGauge#scalesticksheightspan-classtype-signature-type-numbernumberspan).
* You can change the distance from the scale and the Ticks using [distanceFromScale](/js/api/ejCircularGauge#scalesticksdistancefromscalespan-classtype-signature-type-numbernumberspan) property.
* You can set the height and width of the Ticks using the [width](/js/api/ejCircularGauge#scalestickswidthspan-classtype-signature-type-numbernumberspan) and [height](/js/api/ejCircularGauge#scalesticksheightspan-classtype-signature-type-numbernumberspan) property.

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
                distanceFromScale: 7,
                height: 18,
                width: 2,
                color: "red"
            }, {
                type: "minor",
                height: 8,
                width: 2,
                distanceFromScale: 7,
                color: "blue"
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

{% include image.html url="/js/OlapGauge/Scales_images/Ticks_img1.png" %}


### Hiding Ticks

You can hide the **Ticks** that indicate the range values using [showTicks](/js/api/ejCircularGauge#scalesshowticksspan-classtype-signature-type-booleanbooleanspan) property.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
        url: "../wcf/OlapGaugeService.svc",
        enableTooltip: true,
        backgroundColor: "transparent",
        scales: [{ showTicks: false,
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
                    distanceFromScale: 15,
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

{% include image.html url="/js/OlapGauge/Scales_images/Ticks_img2.png" %}

## Indicators

The Key Performance Indicators (KPIs): Status and Trend can be visualized through user-friendly images in OlapGauge.

* You can hide the **Indicator** by changing the [showIndicator](/js/api/ejCircularGauge#scalesindicatorsspan-classtype-signature-type-arrayarrayspan) property to “**false**”.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
        url: "../wcf/OlapGaugeService.svc",
        enableTooltip: true,
        load: "loadGaugeTheme",
        backgroundColor: "transparent",
        scales: [{
            showRanges: true,
            showIndicators: false,
            radius: 150,
            showScaleBar: true,
            size: 1,
            border: {
                width: 0.5
            },
            showIndicators: false,
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

{% include image.html url="/js/OlapGauge/Scales_images/Indicators_img1.png" %}

