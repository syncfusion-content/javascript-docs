---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: OLAP Gauge
documentation: ug
---

### Responsive Layout

**Responsive layout** is aimed at crafting sites to provide an optimal viewing experience - easy reading. It also provides navigation with a minimum of resizing, panning, and scrolling across a wide range of devices from tablet to desktop. To get responsive layout for **OLAP Gauge,** enable **IsResponsive** API to **true**. By using this feature, you can achieve an effective view of the **OLAP Gauge** control in all devices including desktops, tablets, mobiles, etc.

{% highlight js %}

<script type="text/javascript">
$(function () {
       $("#OlapGauge").ejOlapGauge({
                            url: "../wcf/OlapGaugeService.svc", enableTooltip: true, **isResponsive: true,**
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
</script>


{% endhighlight %}



{% include image.html url="/js/OlapGauge/Concepts-and-Features/Responsive-Layout_images/Responsive-Layout_img1.png" Caption="Normal View"%}

<br/>

{% include image.html url="/js/OlapGauge/Concepts-and-Features/Responsive-Layout_images/Responsive-Layout_img2.png" Caption="Responsive View"%}





