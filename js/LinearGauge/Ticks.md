---
layout: post
title: Ticks
description: ticks
platform: js
control: Linear Gauge
documentation: ug
api: /api/js/ejlineargauge
---

# Ticks

Ticks are used to mark some values on the scale. Based on the tick’s value you can set the labels on the required position.

## Adding tick collection 

Tick collection can be directly added to the scale object. Refer the following code example to add tick collection in a **Linear Gauge** control.

{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
        //For Linear gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            enableAnimation: false,
            //Adding frame object
            frame: {
                innerWidth: 8,
                outerWidth: 10,
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            }, 
            value: 78,
            //Adding scale collection
            scales: [{
                width: 5,
                backgroundColor: "transparent", type: "roundedrectangle",
                border: { color: "Grey", width: 1 }, showBarPointers: true,
                //Adding label collection
                labels: [{ distanceFromScale: { x: -25, y: 0 } }],
                //Adding marker pointer collection
                markerPointers: [{ width: 10, length: 10, value: 60 }],
                //Adding bar pointer collection
                barPointers: [{ width: 5, backgroundColor: "#95C7E0" },
                {
                    width: 6, backgroundColor: "#EDC1D7",
                    distanceFromScale: -15, value: 30, opacity: 0.7
                }],
                //Adding tick collection
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: -10, y: 0 }, position: "far"
                },
              {
                  type: "minorinterval", width: 1, height: 6,
                  color: "#8c8c8c", distanceFromScale: { x: -10, y: 0 }, position: "far"
              }]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/LinearGauge/Ticks_images/Ticks_img1.png)



## Tick Customization

**Appearance**

* Height and width of the ticks can be applied by using the properties [`height`](../api/ejlineargauge#members:scales-ticks-height) and [`width`](../api/ejlineargauge#members:scales-ticks-width). You can customize ticks with the properties like angle, color, etc. [`angle`](../api/ejlineargauge#members:scales-ticks-angle) attribute is used to display the labels in the specified angles and [`color`](../api/ejlineargauge#members:scales-ticks-color) attribute is used to display the labels in specified [`color`](../api/ejlineargauge#members:tickcolor). 

* Ticks are two types such as major and minor. The opacity of the labels can be adjusted with the property [`opacity`](../api/ejlineargauge#members:scales-ticks-opacity). The opacity values lies between 0 and 1.


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}


 $(function () {
        //For Linear gauge rendering
        $("#LinearGauge1").ejLinearGauge({enableAnimation:false,
            //Adding scale object
            frame: {
                innerWidth: 8,
                outerWidth: 10,
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            }, 
            value: 78,
            //Adding scale collection
            scales: [{
                width:5,
                backgroundColor: "transparent", type: "roundedrectangle",
                border: { color: "Grey", width: 1 },showBarPointers: true,
                //Adding label collection
                labels: [{ distanceFromScale: { x: -25, y: 0 } }],
                //Adding marker pointer collection
                markerPointers:[{width:10,length:10, value:60}],
                //Adding bar pointer collection
                barPointers: [{ width: 5, backgroundColor: "#95C7E0" }],
                //Adding ticks collection
                ticks: [{
                    type: "majorinterval",
                  width: 2,
                  height:14,
                  angle:10,
                  color: "Black",
                    distanceFromScale: { x: -10, y: 0 },position:"far"
                },
                {
                    type: "minorinterval",
                  width: 1,
                  height: 10,
                  opacity:0.5,
                  color: "Black",
                    distanceFromScale: { x: -10, y: 0 }, position: "far"
                }]
            }]
        });
    });



{% endhighlight %}


Execute the above code to render the following output.

![](/js/LinearGauge/Ticks_images/Ticks_img2.png)

## Types

Ticks are two [`types`](../api/ejlineargauge#members:scales-ticks-type) such as **majorInterval** and **minorInterval**. Major type ticks are for major interval values and minor type ticks are for minor interval values.


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        //For Linear gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            enableAnimation: false,
            //Adding frame object
            frame: {
                innerWidth: 8,
                outerWidth: 10,
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            }, 
            value: 78,
            //Adding scale collection
            scales: [{
                width: 5,
                backgroundColor: "transparent", type: "roundedrectangle",
                border: { color: "Grey", width: 1 }, showBarPointers: true,
                //Adding label collection
                labels: [{ distanceFromScale: { x: -25, y: 0 } }],
                //Adding marker pointer collection
                markerPointers: [{ width: 10, length: 10, value: 60 }],
                //Adding bar pointer collection
                barPointers: [{ width: 5, backgroundColor: "#95C7E0" }],
                //Adding tick collection
                ticks: [{
                    type: "majorinterval", width: 2, height: 14,
                    color: "Black", position: "far"
                },
                {
                    type: "minorinterval",
                }]
            }]
        });
    });



{% endhighlight %}



Execute the above code to render the following output.



![](/js/LinearGauge/Ticks_images/Ticks_img3.png)

## Positioning the ticks

* You can position ticks with the help of two properties such as **distanceFromScale** and **placement**. The property [`distanceFromScale`](../api/ejlineargauge#members:scales-ticks-distancefromscale) defines the distance between the scale and ticks. 

* [`placement`](../api/ejlineargauge#members:scales-ticks-placement) property is used to locate the ticks with respect to scale either inside the scale or outside the scale or along the scale. It can be specified along [`x`](../api/ejlineargauge#members:scales-ticks-distancefromscale-x) and [`y`](../api/ejlineargauge#members:scales-ticks-distancefromscale-y) position. It is an enumerable data type. 


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        // For Linear Gauge rendering
        $("#LinearGauge1").ejLinearGauge({enableAnimation:false,
            //Adding frame collection
            frame: {
                innerWidth: 8,
                outerWidth: 10,
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            }, 
            value: 78,
            //Adding scale collection
            scales: [{width:5,
                backgroundColor: "transparent", type: "roundedrectangle",
                border: { color: "Grey", width: 1 },showBarPointers: true,
                //Adding label collection
                labels: [{ distanceFromScale: { x: -25, y: 0 } }],
                //Adding marker pointer collection
                markerPointers:[{width:10,length:10, value:60}],
                //Adding bar pointer collection
                barPointers: [{ width: 5, backgroundColor: "#95C7E0" }],
                //Adding tick collection
                ticks: [{
                    type: "majorinterval", width: 2,height:14,
                    color: "Black", distanceFromScale: { x: -10, y: 0 },
                position: "far", color: "Red"
                },
                {
                    type: "minorinterval",distanceFromScale: { x: -10, y: 0 },
                    color:"grey"
                }]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.



![](/js/LinearGauge/Ticks_images/Ticks_img4.png)

