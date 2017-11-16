---
layout: post
title: Ticks
description: ticks
platform: js
control: Circular Gauge
documentation: ug
api: /api/js/ejcirculargauge
---

# Ticks

The [`ticks`](../api/ejcirculargauge#members:scales-ticks) are used to mark some values on the scale. Based on the tick’s [`value`](../api/ejcirculargauge#members:scales-ticks-value) you can set the labels on the required position.

## Adding Tick Collection 

Tick collection is directly added to the scale object. Refer the following code example to add tick collection in a **Gauge** control.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}


    $(function () {
        //For circular gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            scales: [{
                ticks: [{
                    value: 30
                }]
            }]
        })
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Ticks_images/Ticks_img1.png)

## Tick Customization

Height and width of the ticks can be applied by using the properties [`height`](../api/ejcirculargauge#members:scales-ticks-height) and [`width`](../api/ejcirculargauge#members:scales-ticks-width). You can customize ticks with the properties such as angle, color, etc. [`angle`](../api/ejcirculargauge#members:scales-ticks-angle) attribute is used to display the labels in the specified angles and [`color`](../api/ejcirculargauge#members:scales-ticks-color) attribute is used to display the labels in specified color. Ticks are two types such as major and minor.

Major [`type`](../api/ejcirculargauge#members:scales-ticks-type) ticks are for major interval values and minor type ticks are for minor interval values.You can position ticks with the help of two properties such as [`distanceFromScale`](../api/ejcirculargauge#members:scales-ticks-distancefromscale) and [`placement`](../api/ejcirculargauge#members:scales-ticks-placement). **distanceFromScale** property defines the distance between the scale and ticks.  **Placement** property is used to locate the ticks with respect to scale either inside the scale or outside the scale or along the scale. It is an enumerable data type.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 
    $(function () {
        // For Circular Gauge rendering
        $("#CircularGauge1"). ejCircularGauge ({
            scales: [{
                ticks: [
                // For setting tick1
                { type: "major",color:"Red" },
                // For setting tick2
                {
                    // For setting tick type
                    type:"minor",
                    // For setting tick color
                    color:"yellow",
                    // For setting tick height
                    height:8,
                    // For setting tick placement
                    placement: "near",
                    // For setting tick distance from scale
                    distanceFromScale:5}]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Ticks_images/Ticks_img2.png)

