---
layout: post
title: Custom-Label
description: custom label
platform: js
control: OLAP Gauge
documentation: ug
---

# Custom Label

**Custom label** provides information about the members associated behind each **OlapGauge**. You can define multiple labels for **OlapGauge** and it can be positioned along X and Y co-ordinates based on location settings.

{% include image.html url="/js/OlapGauge/Custom-Label_images/Custom-Label_img1.png" Caption="Custom Label"%}

## Positioning the Custom Label

You can set the location of the **custom label** in circular gauge using “**location**” property. Refer the following code example.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
        url: "../wcf/OlapGaugeService.svc",
        enableTooltip: true,
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
                size: 7,
                backgroundColor: "#fc0606",
                border: {
                    color: "#fc0606"
                }
            }, {
                distanceFromScale: -5,
                size: 7
            }],
            customLabels: [{ position: {
                    x: 280,
                    y: 390
                },
            }, { position: {
                        x: 180,
                        y: 280
                    },

            }, { position: {
                    x: 180,
                    y: 170
                },
            }]
        }]
    });
});    

{% endhighlight %}

{% include image.html url="/js/OlapGauge/Custom-Label_images/Custom-Label_img2.png" Caption="Positioning Custom Label"%}

## Font and Style Customization of Custom Label

You can customize the **custom label** font with font style, font family, and size properties.

{% highlight js %}

$(function() {
    $("#OlapGauge1").ejOlapGauge({
        url: "../wcf/OlapGaugeService.svc",
        enableTooltip: true,
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
                    x: 280,
                    y: 290
                },
                font: {
                    size: "10px",
                    fontFamily: "Segoe UI",
                    fontStyle: "Normal"
                },
                color: "red"
            }, {
                position: {
                    x: 180,
                    y: 280
                },
                font: {
                    size: "10px",
                    fontFamily: "Segoe UI",
                    fontStyle: "Normal"
                },
                color: "red"
            }, {
                position: {
                    x: 180,
                    y: 170
                },
                font: {
                    size: "12px",
                    fontFamily: "Segoe UI",
                    fontStyle: "Normal"
                },
                color: "red"
            }]
        }]
    });
});

{% endhighlight %}

{% include image.html url="/js/OlapGauge/Custom-Label_images/Custom-Label_img3.png" Caption="Style Customization"%}

