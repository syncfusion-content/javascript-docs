---
layout: post
title: Indicators
description: indicators
platform: js
control: OLAP Gauge
documentation: ug
---

### Indicators

**KPIs** are displayed with **Trend and Status visualizations** that supports Traffic Light, Road Signs and Standard Arrow .Status and Trend values are highlighted through user friendly images within the **OlapGauge** that is known as **indicators**.

#### Hiding Indicators

You can hide the **Indicator** by changing the “**showIndicator**” property to “**false**”.

{% highlight js %}

$(function () {
$("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
        backgroundColor: "transparent", 
        scales: [{
            showRanges: true, **showIndicators: false,**
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



{% include image.html url="/js/OlapGauge/Concepts-and-Features/Indicators_images/Indicators_img1.png" Caption="Hiding Indicators"%}

