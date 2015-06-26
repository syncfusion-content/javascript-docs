---
layout: post
title: Scales
description: scales
platform: js
control: OlapGauge
documentation: ug
---

# Scales

**Scale** is a basic unit of **radial gauge**. You can customize the gauge scales by using properties such as radius, minimum, scale direction, interval values etc. 

## Resizing the Scale Bar

Radius of the **Scale Bar** is changed with the help of [scale Radius](/js/api/ejCircularGauge#scalesradiusspan-classtype-signature-type-numbernumberspan) property and in order to make **Scale Bar** visible, set [showScaleBar](/js/api/ejCircularGauge#scalesshowscalebarspan-classtype-signature-type-booleanbooleanspan) property to ‘**true’**. You can set size of the **Scale Bar** with the help of [size](/js/api/ejCircularGauge#scalessizespan-classtype-signature-type-numbernumberspan) and border width using [width](/js/api/ejCircularGauge#scalesborderwidthspan-classtype-signature-type-numbernumberspan) property**.** 

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

