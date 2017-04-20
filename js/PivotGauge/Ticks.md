---
layout: post
title: Ticks
description: ticks
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Ticks

## Adding Tick Collection

Tick collection can be directly added to the scales option within the PivotGauge widget as an array.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            ticks: [{
                type: "major"
            }]
        }]
    });

{% endhighlight %}

## Tick Customization

The appearance of the tick can be customized through the following properties.

* **type** – indicates whether ticks are for major or minor intervals. By default, the type is "major".
* **height** – sets the height of the ticks.
* **width** – sets the width of the ticks.
* **angle** – rotates the ticks to a specified angle. By default, the angle value is 0.
* **color** – displays the ticks in specified color.
* **distanceFromScale** – sets the distance between scale and ticks. By default, the values is 0.
* **placement** – positions the ticks with respect to the scale.  By default, the value is set to "far".

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            ticks: [{
                type: "major",
                height: 15,
                width: 4,
                angle: 0,
                color: "green",
                distanceFromScale: 2,
                placement: "near"
            }]
        }]
    });

{% endhighlight %}

![](Ticks_images/TickCustomization.png) 

