---
layout: post
title: Custom-Label
description: custom label
platform: js
control: OlapGauge
documentation: ug
---

# Custom Label

**Custom label** provides information about the members associated behind each OlapGauge. You can define multiple labels for OlapGauge and it can be positioned along X and Y co-ordinates based on location settings.

* You can set the location of the custom label in circular gauge using [Position](/js/api/ejCircularGauge#setcustomlabelanglespan-classsignaturespan) property.
* You can customize the custom label font with [font style](/js/api/ejCircularGauge#setcustomlabelanglespan-classsignaturespan), [font family](/js/api/ejCircularGauge#setcustomlabelanglespan-classsignaturespan), and [size](/js/api/ejCircularGauge#setcustomlabelanglespan-classsignaturespan) properties.

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
                    x: 280,
                    y: 390
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
                    y: 205
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

{% include image.html url="/js/OlapGauge/Custom-Label_images/Custom-Label_img3.png" %}

