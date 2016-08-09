---
layout: post
title: Pointers
description: pointers
platform: js
control: PivotGauge
documentation: ug
---

# Pointers

## Pointer Types

PivotGauge pointers has two types namely,
	
* Needle
* Marker

Needle type pointers are the default pointers which is always located at the center of the Gauge. Following shapes that are supported for the needle pointers are:
* rectangle
* triangle
* trapezoid
* arrow
* image.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            pointers: [{
                type: "needle",
                needleType: "trapezoid",
            }]
        }]
    });

{% endhighlight %}

![](Pointers_images/NeedlePointer.png) 

For marker pointer, the available shapes are rectangle, triangle, ellipse, diamond, pentagon, circle, slider, pointer, wedge, trapezoid, rounded rectangle and image.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            pointers: [{
                type: "marker",
                markerType: "diamond",
            }]
        }]
    });

{% endhighlight %}

![](Pointers_images/MarkerPointer.png) 

## Adding Pointer Collection

Pointer collection can be directly added to the scales option within the PivotGauge widget as an array.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            pointers: [
                {
                    type: "needle",
                    needleType: "triangle",
                }, 
                {
                    type: "marker",
                    markerType: "diamond"
                }     
            ]
        }]
    });
{% endhighlight %}

![](Pointers_images/AddingPointerCollection.png)

## Appearance Customization

The appearance of the pointer can be customized through the following properties.

* **border** – sets the “color” and “width” of the pointer border.
* **backgroundColor** – sets the background color of the pointer.
* **length** – sets the length of the pointer.
* **width** – sets the width of the pointer.
* **opacity** – sets the opacity of the pointer.  By default, the value is 1.
* **type** – sets the type of the pointer.  By default, the type is “needle”.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            pointers: [
                {
                    border: {
                        color: "green",
                        width: 2
                    },
                    backgroundColor: "yellow",
                    length: 120,
                    width: 7,
                    opacity: 0.6,
                    type: "needle",
                    needleType: "triangle"
                }, 
                {
                    border: {
                        color: "green",
                        width: 2
                    },
                    backgroundColor: "yellow",
                    length: 25,
                    width: 15,
                    opacity: 0.8,
                    type: "marker",
                    markerType: "diamond"
                }
            ]
        }]
    });

{% endhighlight %}

![](Pointers_images/AppearanceCustomization.png)
 
## Pointer Position

Pointer can be positioned with the help of below two properties.

* **distanceFromScale** -  defines the distance between scale and pointer. By default, the value is 0.
* **placement** -  defines the location of the pointer. By default, the value is "center".

N> Both the properties can be applied only if the pointer type is set to "marker". Needle pointer type appears only at the center of the widget, which is its default position.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            pointers: [{
                //...
                type: "marker",
                placement: "far",
                distanceFromScale: 2
            }]
        }]
    });

{% endhighlight %}

![](Pointers_images/PointerPosition.png) 
 
## Pointer Image

It is possible to replace the pointers with image. To view the pointers as image, we need to set the appropriate location in the `imageUrl` property.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            pointers: [{
                //For replacing needle pointer with image
                type: "needle",
                needleType: "image",
                imageUrl: "image.png"
            }, 
            {
                //For replacing marker pointer with image
                type: "marker",
                markerType: "image",
                imageUrl: "image.png"
            }]
        }]
    });
{% endhighlight %}

![](Pointers_images/PointerImage.png) 

## Pointer Value Text

To display the current value of the pointers in PivotGauge widget, `pointerValueText` option inside pointers is used.  Following are the properties used to enable and customize the pointer value text.
 
* **showValue** – enables the pointer value text by setting the property to “true”. By default, its value is “true”.
* **distance** – sets the distance between pointer and text.
* **color** – sets the color of the text.
* **opacity** – sets the opacity of the text. By default, its value is 1.
* **angle** – sets the rotation angle of the text. By default, its value is 0.
* **font** – sets the font size, font style and font family of the text.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        scales: [{
            //...
            pointers: [{
                //For needle type
                pointerValueText: {
                    showValue: true,
                    distance: 10,
                    color: "red",
                    opacity: 0.7,
                    angle: 20,
                    font: {
                        size: "15px",
                        fontStyle: "Normal",
                        fontFamily: "Arial"
                    }
                }
            }, 
            {
                //For marker type
                pointerValueText: {
                    showValue: true,
                    distance: 40,
                    color: "red",
                    opacity: 0.7,
                    angle: -40,
                    font: {
                        size: "15px",
                        fontStyle: "Normal",
                        fontFamily: "Arial"
                    }
                },
            }]
        }]
    });

{% endhighlight %}

![](Pointers_images/PointerValueText.png)