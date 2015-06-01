---
layout: post
title: Tooltip
description: tooltip
platform: js
control: OLAP Gauge
documentation: ug
---

# Tooltip

**Tooltip** provides the information about the **OlapGauge** when you move the mouse pointer over the control. You can enable it using “**showtooltip**”****property**.**



{% highlight js %}

**[JS]**
<script type="text/javascript">
$(function () {
$("#OlapGauge1").ejOlapGauge({
  url: "../wcf/OlapGaugeService.svc", **enableTooltip**: true, backgroundColor: "transparent",
  scales: [{
          showRanges: true,
          scaleRadius: 150, showScaleBar: true, scaleBarSize: 1, scaleBorderWidth: 0.5,h
                               showLabels: true,
                                pointers: [{
                                    showBackNeedle: true,
                                    pointerType: "Needle",
                                    backNeedleLength: 20,
                                    pointerLength: 120,
                                    pointerWidth: 9,
                                    capBorderColor: "#f5b43f",
                                    capBackgroundColor: "#f5b43f"
                                },
                        {
                            pointerType: "Marker",
                            backgroundColor: "#29A4D9",
                            pointerLength: 25,
                            pointerWidth: 15
                        }],
                                ticks: [{ tickStyle: "Major", tickHeight: 16, 
                                          tickWidth: 1, tickColor: "red" },
                                        { tickStyle: "Minor", tickHeight: 6,
                                          tickWidth: 1, tickColor: "blue" }],
                                labels: [{
                                    labelColor: "#8c8c8c"
                                }],
                                ranges: [{
                                    distanceFromScale: -10
                                 },{
                                     distanceFromScale: -10,
                                     backgroundColor: "red"
                                }],
                                customLabel: [{
                                    location: { x: 280, y: 290 },                                   
                                }, {
                                    location: { x: 180, y: 350 },
                                }, {
                                    location: { x: 180, y: 150 },
                                }]
                            }]
                        });
                    });
                </script>



{% endhighlight %}



## Customizing the tooltip using CSS

You can customize the **Tooltip** by overriding the existing style attributes and referring it in web page.



{% highlight css %}

**[CSS]**
<style>
.e-olapgauge-tooltip {
  background-color: aqua !important;
  border: 2px solid red !important;
  color: black !important;
  border-radius: 18px!important;
  margin-top: 20px;
  text-align: left;
  font: 12px Segoe UI;
  line-height: 20px;
}
</style>


{% endhighlight %}





{% include image.html url="/js/OlapGuage/Concepts-and-Features/Tooltip_images/Tooltip_img1.png" Caption="Figure:Tooltip Customization"%}

