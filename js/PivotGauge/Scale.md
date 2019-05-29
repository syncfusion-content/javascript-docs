---
layout: post
title: Scale | JavaScript | PivotGauge | Syncfusion
description: This document illustrates that how to enable scales and its customization in JavaScript PivotGauge control
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Scale

## Adding scale

The scale can be added within the pivot gauge widget as an array.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            showScaleBar: true,
            radius: 150
            //...
        }]
    });
{% endhighlight %}

![Scale in JavaScript pivot gauge control](Scale_images/AddingScale.png) 

## Scale customization

### Pointer cap

The pointer cap is a circular shape element that is located at the center of the pivot gauge. It can be customized with the `pointerCap` property in the [`scales`](/api/js/ejpivotgauge#members:scales) option. Following are the properties that are used to customize the appearance of the pointer cap:

* **radius** – sets the radius of the pointer cap.
* **borderColor** – sets the color of the pointer cap border.
* **borderWidth** – sets the width of the pointer cap border.
* **backgroundColor** – sets the background color of the pointer cap.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            showScaleBar: true,
            pointerCap: {
                radius: 5,
                borderWidth: 2,
                borderColor: "green",
                backgroundColor: "yellow"
            }
        }]
    });

{% endhighlight %}

![Pointer cap in JavaScript pivot gauge control](Scale_images/PointerCap.png) 

### Appearance

The appearance of the scale can be customized through the following properties:

* **radius** – sets the radius of the scale.
* **backgroundColor** – sets the background color of the scale.
* **border** – sets the border of the scale with color and width properties.
* **size** – sets the size of the scale.
* **minimum** – sets the least value of the scale.
* **maximum** – sets the highest value of the scale.
* **majorIntervalValue** – sets the interval between major ticks in the scale.
* **minorIntervalValue** – sets the interval between minor ticks in the scale.
* **direction** – sets the direction of the scale. By default, it takes clockwise direction.

The `showIndicators`, `showTicks`, `showRanges`, `showPointers`, and `showScaleBar` properties are used to enable/disable the indicators, ticks, ranges, pointers, and scale bar respectively. By default, `showTicks` and `showPointers` are set to true, and other properties are set to false.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            showScaleBar: true,
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
            direction: ej.datavisualization.CircularGauge.Directions.CounterClockwise
        }]
    });

{% endhighlight %} 

![Scale appearance in JavaScript pivot gauge control](Scale_images/Appearance.png) 
