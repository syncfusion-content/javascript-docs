---
layout: post
title: Custom-Labels | JavaScript | PivotGauge | Syncfusion
description: This document illustrates that how to enable custom labels and its functionalities in JavaScript PivotGauge control
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Custom labels

## Adding custom label collection

The `customLabels` collection can be directly added to the scales option within the pivot gauge widget as an array.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            customLabels: [{
                position: {
                    x: 180,
                    y: 290
                }
            }]
        }]
    });

{% endhighlight %}

## Appearance customization

The appearance of the custom labels can be changed through the following properties:

* **position** – sets the position of the labels.
* **font** – sets the font size, font style, and font family of the label text.
* **color** – sets the color of the label text.
* **textAngle** – rotates the label to a specified angle. By default, the value is 0.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            customLabels: [{
                position: {
                    x: 180,
                    y: 320
                },
                font: {
                    size: "12px",
                    fontFamily: "Segoe UI",
                    fontStyle: "Normal"
                },
                color: "blue",
                textAngle: 20
            }]
        }]
    });

{% endhighlight %}

![Custom label customization in JavaScript PivotGauge control](Custom-Labels_images/AppearanceCustomization.png) 

## Multiple custom labels

Multiple custom labels can be set to a pivot gauge widget by adding an array of objects within the `customLabels` option.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            customLabels: [
                {
                    color: "Red",
                    font: {
                    size: "12px",
                    fontFamily: "Segoe UI",
                    fontStyle: "Normal"
                    },
                    position: {
                        x: 180,
                        y: 150
                    }
                }, 
                {
                    color: "Green",
                    font: {
                    size: "10px",
                    fontFamily: "Segoe UI",
                    fontStyle: "Normal"
                    },
                    position: {
                        x: 180,
                        y: 320
                    }
                }, 
                {
                    color: "Blue",
                    font: {
                    size: "10px",
                    fontFamily: "Segoe UI",
                    fontStyle: "Normal"
                    },
                    position: {
                        x: 180,
                        y: 290
                    }
                }
            ]
        }]
    });

{% endhighlight %}

![Multiple custom labels in JavaScript PivotGauge control](Custom-Labels_images/MultipleCustomLabels.png) 
