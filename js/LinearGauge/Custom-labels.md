---
layout: post
title: Custom-labels
description: custom labels
platform: js
control: Linear Gauge
documentation: ug
api: /api/js/ejlineargauge
---

# Custom labels

Custom labels are the text that can paste in any location of the **Linear Gauge**. It is used to define the purpose of the gauge.

## Adding Custom label collection

[`Custom labels`](../api/ejlineargauge#members:members:scales-customlabels) collection can be directly added to the scale object. Refer the following code to add custom labels collection in a **Linear Gauge** control.


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        // For Linear Gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            enableAnimation: false, height: 500, width: 200, labelColor: "Grey",
            //Adding frame object
            frame: {
                innerWidth: 8,
                outerWidth: 10,
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            },
            //Adding scale collection
            scales: [{
                backgroundColor: "transparent",
                border: { color: "transparent", width: 0 },
                showMarkerPointers: false, showBarPointers: true,
                showCustomLabels: true,
                //Adding bar pointer collection
                barPointers: [{
                    width: 10, backgroundColor: "#8BABFF",
                    value: 91, placement: "near", distanceFromScale: 30
                }],
                //Adding tick collection
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                },
                {
                    type: "minorinterval", width: 1, height: 6,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                }],
                //Adding custom label collection
                customLabels: [{
                    value: "Mathematics Mark", position: { x: 55, y: 97 }
                }]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/LinearGauge/Custom-labels_images/Custom-labels_img1.png)

## Basic Customization

**Appearance**

* You can customize [`custom labels`](../api/ejlineargauge#members:scales-customlabels) using the properties like [`textAngle`](../api/ejlineargauge#members:scales-customlabels-textangle), [`color`](../api/ejlineargauge#members:scales-customlabels-color) and [`font`](../api/ejlineargauge#members:scales-customlabels-font). The API **textAngle** is used to display the custom labels in the specified angles and **color** attribute is used to display the custom labels in specified color. You can use [`value`](../api/ejlineargauge#members:scales-customlabels-value)attribute to set the text value in the custom labels. 

* To display the custom labels, set [`showCustomLabels`](../api/ejlineargauge#members:scales-showcustomlabels) as ‘true’. Font option is also available on the custom labels. The basic three properties of fonts such as [`size`](../api/ejlineargauge#members:scales-customlabels-font-size), [`family`](../api/ejlineargauge#members:scales-customlabels-font-fontfamily) and [`style`](../api/ejlineargauge#members:scales-customlabels-font-fontstyle) can be achieved by **size**, **fontStyle** and **fontFamily**. You can adjust the opacity of the label with the property [`opacity`](../api/ejlineargauge#members:scales-customlabels-opacity) and the value of opacity lies between 0 and 1.


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

   $(function () {
        // For Linear Gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            enableAnimation: false, height: 500, width: 200, labelColor: "Grey",
            //Adding frame collection
            frame: {
                innerWidth: 8,
                outerWidth: 10,
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            },
            //Adding scale collection
            scales: [{
                backgroundColor: "transparent",
                border: { color: "transparent", width: 0 },
                showMarkerPointers: false, showBarPointers: true,
                showCustomLabels: true,
                //Adding bar pointer collection
                barPointers: [
                {
                    width: 10, backgroundColor: "#8BABFF",
                    value: 91, placement: "near", distanceFromScale: 30
                }
                ],
                //Adding tick collection
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                },
                {
                    type: "minorinterval", width: 1, height: 6,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                }],
                //Adding custom labels
                customLabels: [{
                    position: { x: 55, y: 87 },
                    value: "Mathematics Mark",
                    color: "Red",
                    textAngle: 30,
                    opacity: 0.5
                }]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/LinearGauge/Custom-labels_images/Custom-labels_img2.png)

## Locating the CustomLabels

To set the location of the custom label in **Linear Gauge**, [`position`](../api/ejlineargauge#members:scales-customlabels-position) property is used. You can position the custom labels in horizontal and vertical axis using [`x`](../api/ejlineargauge#members:scales-customlabels-position-x) and [`y`](../api/ejlineargauge#members:scales-customlabels-position-y) axis respectively.

To specify the label [`position type`](../api/ejlineargauge#members:scales-customlabels-positiontype) as inner or outer in the custom labels.


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        //For rendering Liner gauge
        $("#LinearGauge1").ejLinearGauge({
            enableAnimation: false, height: 500, width: 200, labelColor: "Grey",
            //Adding frame object
            frame: {
                innerWidth: 8,
                outerWidth: 10,
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            },
            //Adding scale collection
            scales: [{
                backgroundColor: "transparent",
                border: { color: "transparent", width: 0 },
                showMarkerPointers: false, showBarPointers: true,
                showCustomLabels: true,
                //Adding bar pointer collection
                barPointers: [
                {
                    width: 10, backgroundColor: "#8BABFF",
                    value: 91, placement: "near", distanceFromScale: 30
                }
                ],
                //Adding ticks collection
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                },
                {
                    type: "minorinterval", width: 1, height: 6,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                }],
                //Adding custom label collection
                customLabels: [
                { value: "Mathematics Mark", position: { x: 55, y: 87 } }]
            }]
        });
    });

{% endhighlight %}


Execute the above code to render the following output.

![](/js/LinearGauge/Custom-labels_images/Custom-labels_img3.png)

## Multiple Custom Labels

You can set multiple custom labels in a single **Linear Gauge** by adding an array of custom label objects. Refer the following code example for multiple custom label functionality.

{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
        // For Linear Gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            enableAnimation: false, height: 500, width: 200, labelColor: "Grey",
            //Adding frame object
            frame: {
                innerWidth: 8,
                outerWidth: 10,
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            },
            //Adding scale collection
            scales: [{
                backgroundColor: "transparent",
                border: { color: "transparent", width: 0 },
                showMarkerPointers: false, showBarPointers: true,
                showCustomLabels: true,
                //Adding bar pointer collection
                barPointers: [
                {
                    width: 10, backgroundColor: "#8BABFF",
                    value: 91, placement: "near", distanceFromScale: 30
                }
                ],
                //Adding ticks collection
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                },
                {
                    type: "minorinterval", width: 1, height: 6,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                }],
                //Adding custom label collection
                customLabels: [
                {
                    value: "Mathematics Mark", position: { x: 55, y: 87 },
                    color: "Red"
                },
                {
                    value: "Marks in %", position: { x: 15, y: 57 },
                    color: "Red", textAngle: 90
                }]
            }]
        });
    });



{% endhighlight %}


Execute the above code to render the following output.

![](/js/LinearGauge/Custom-labels_images/Custom-labels_img4.png)


## Outer Custom Label

**Outer Custom Label** is used to show custom labels outside the **gauge** control. The **Outer Custom Label** can be positioned with API called [`outerCustomLabelPosition`](../api/ejlineargauge#members:outercustomlabelposition). The value for this API is enumerable type and its possible values are,

* Right

* Left

* Top

* Bottom

