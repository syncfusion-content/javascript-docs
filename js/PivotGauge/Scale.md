---
layout: post
title: Scale
description: scale
platform: js
control: PivotGauge
documentation: ug
---

# Scale

## Adding Scale

Scale can be added within the PivotGauge widget as an array.

{% highlight javascript %}

$("#PivotGauge1").ejPivotGauge({
    url: "../PivotGauge",
    //...
    scales: [{
        radius: 150
    }],
    //...
});

{% endhighlight %}

![](Scales_images/scale.png) 

## Scale Customization

### Pointer Cap

Pointer Cap is a circular shape element that is located at the center of the PivotGauge. It can be customized with the `pointerCap` option inside scales. Following are the properties used to customize its appearance.

* **radius** – sets the radius of the pointer cap.
* **borderColor** – sets the color of the pointer cap border.
* **borderWidth** – sets the width of the pointer cap border.
* **backgroundColor** – sets the background color of the pointer cap.

{% highlight javascript %}

$("#PivotGauge1").ejPivotGauge({
    url: "../PivotGauge",
    //...
    scales: [{
        //...
        pointerCap: {
            radius: 5,
            borderWidth: 2,
            borderColor: "green",
            backgroundColor: "yellow"
        },
        //...
    }],
    //...
});

{% endhighlight %}

![](Scales_images/pointercap.png) 

### Appearance

The appearance of the scale can be customized through the following properties.

* **radius** – sets the radius of the scale.
* **backgroundColor** – sets the background color of the scale.
* **border** – sets the border of the scale with color and width properties.
* **size** – sets the size of the scale.
* **minimum** – sets the least value of the scale.
* **maximum** – sets the highest value of the scale.
* **majorIntervalValue** – sets the interval between minor ticks in the scale.
* **minorIntervalValue** – sets the interval between major ticks in the scale.
* **direction** – sets the direction of the scale.  By default it takes "Clockwise" direction.

The `showIndicators`, `showTicks`, `showRanges`, `showPointers` and `showScaleBar` properties are used to enable/disable the indicators, ticks, ranges, pointers and scale bar respectively.  By default, these properties are set to true.

{% highlight javascript %}

$("#PivotGauge1").ejPivotGauge({
    url: "../PivotGauge",
    //...
    scales: [{
        //...
        radius: 120,
        backgroundColor: "yellow",
        border: {
            color: "Blue",
            width: 3
        },
        size: 10,
        minimum: 20,
        maximum: 120,
        majorIntervalValue: 20,
        minorIntervalValue: 5,
        direction: ej.datavisualization.CircularGauge.Directions.CounterClockwise,
        //...
    }],
    //...
});

{% endhighlight %} 

![](Scales_images/Scale-Customization-Appearance.png) 
