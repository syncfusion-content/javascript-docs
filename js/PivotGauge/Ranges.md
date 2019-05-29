---
layout: post
title: Ranges | JavaScript | PivotGauge | Syncfusion
description: This document illustrates that how to enable ranges and its customization in JavaScript PivotGauge control
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Ranges

## Adding range collection

The range collection can be directly added to the scales option within the pivot gauge widget as an array.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            showRanges: true,
            ranges: [{
                distanceFromScale: 10
            }]
        }]
    });
{% endhighlight %}

## Appearance customization

The appearance of the range can be customized through the following properties:

* **startValue** – defines the start position of the range.
* **endValue** – defines the end position of the range.
* **startWidth** – sets the width at starting position of the range.
* **endWidth** – sets the width at ending position of the range.
* **backgroundColor** – sets the background color of the range.
* **border** – sets the height and width of the border of the range.
* **placement** – sets the position of the range.
* **distanceFromScale** – sets the distance between the range and the scale.

The position of the range can be set through the `placement` or `distanceFromScale` property.

N> By default, the placement takes the value "near", whereas other enumeration values available are "far" and "center".

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            showRanges: true,
            ranges: [{
                startValue: 20,
                endValue: 50,
                startWidth: 2,
                endWidth: 6,
                backgroundColor: "yellow",
                border: {
                    color: "red",
                    width: 2
                },
                distanceFromScale: 20
            }, 
            {
                startValue: 50,
                endValue: 100,
                startWidth: 2,
                endWidth: 7,
                backgroundColor: "blue",
                border: {
                    color: "green",
                    width: 2
                },
                placement: "near",
            }]
        }]
    });

{% endhighlight %}

![Custom appearance of ranges in JavaScript pivot gauge control](Ranges_images/AppearanceCustomization.png) 

N> When you set both the position properties - "distanceFromScale" and "placement" for a range, the preference is given to the value that is set in the "distanceFromScale" property.

## Multiple ranges
Multiple ranges can be added by placing an array of objects in the `ranges` option.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            showRanges: true,
            ranges: [
                {
                    startValue: 0,
                    endValue: 10,
                    backgroundColor: "Green",
                    distanceFromScale: -5
                }, 
                {
                    startValue: 10,
                    endValue: 30,
                    backgroundColor: "yellow",
                    distanceFromScale: -5
                }, 
                {
                    startValue: 30,
                    endValue: 50,
                    backgroundColor: "red",
                    distanceFromScale: -5
                }
            ]
        }]
    });

{% endhighlight %}

![Multiple ranges in JavaScript pivot gauge control](Ranges_images/MultipleRanges.png) 
