---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Linear Gauge
documentation: ug
api: /api/js/ejlineargauge
---

# Getting Started

This section briefly explains on how to create a **Linear Gauge** control for your application.

* You can provide data for a **Linear Gauge** and display them in a required way. You can also customize the default **Linear Gauge** appearance to meet your requirements. 

* In this example, you will learn how to create a **Linear Gauge** and how to design a thermometer, which can be used to check the body temperature of a person.



![](/js/LinearGauge/Getting-Started_images/Getting-Started_img1.png)

## Create a Linear Gauge

First create an HTML file, and then add references to the required libraries.



{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
   <meta name="viewport" content="width=device-width, initial-scale=1.0" />
   <meta charset="utf-8" />
      <link href="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/ej.web.all.min.js"></script>
</head>

{% endhighlight %}

Now add a &lt;div&gt; element that acts as a container for **ejLinearGauge** widget.


{% highlight html %}

<body>
    <div id="LinearGauge1"></div>   
</body>
</html>

{% endhighlight %}



Create the **ejLinearGauge** widget as follows,



{% highlight javascript %}

$(function () {
        $("#LinearGauge1").ejLinearGauge();
    });

{% endhighlight %}


On executing the above code sample renders a default **Linear Gauge** with default values as follows.


![](/js/LinearGauge/Getting-Started_images/Getting-Started_img2.png)

**Set Height and Width values**

* Basic attributes of each canvas elements are height and width properties. 

* You can set the [`height`](../api/ejlineargauge#members:height) and [`width`](../api/ejlineargauge#members:width) of the gauge as shown in the following code example.



{% highlight javascript %}

 $(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
        });
    });

{% endhighlight %}


On executing the above code sample renders a default **Linear Gauge** with height and width.


![](/js/LinearGauge/Getting-Started_images/Getting-Started_img3.png)

## Set animate option and Label Color

* You can draw the Thermometer by using [`labelColor`](../api/ejlineargauge#members:labelcolor) option and set animate property [`enableAnimation`](../api/ejlineargauge#members:enableanimation) as _true_.  

* Initially set the animate property to _False_ to avoid unwanted script loads.



{% highlight javascript %}

 $(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
            labelColor: "#8c8c8c",
            enableAnimation: false,
        });

    });

{% endhighlight %}



On executing the above code sample renders a customized **Linear Gauge** as follows.

![](/js/LinearGauge/Getting-Started_images/Getting-Started_img4.png)

## Provide scale values

* You can change the Scale Style of Thermometer using [`type`](../api/ejlineargauge#members:scales-type) property.

* You can set the Minimum temperature up to -10 and maximum body temperature up to 110. 

* You can set the Minimum scale value as -10 by using [`minimum`](../api/ejlineargauge#members:scales-minimum) property and maximum value as 110 by using [`maximum`](../api/ejlineargauge#members:scales-maximum) property.

* You can set the Location values such as vertical and horizontal position by using [`position`](../api/ejlineargauge#members:scales-position) property in the thermometer.

* You can set the thermometer height by using [`length`](../api/ejlineargauge#members:scales-length) property.

* You can set the Minor Interval value as 5 to get the exact temperature of the patient by using [`minorIntervalValue`](../api/ejlineargauge#members:scales-majorintervalvalue) property.



{% highlight javascript %}

$(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
            labelColor: "#8c8c8c",
            enableAnimation: false,
            scales: [{
                type: "thermometer",
                backgroundColor: "transparent",
                minimum: -10,
                maximum: 110,
                minorIntervalValue: 5,
                width: 20,
                position: { x: 50, y: 18 },
                length: 355,
                border: { width: 0.5 }
                //Add the pointers customization code here
                //Add the labels customization code here
                //Add the ticks customization code here
                //Add the Custom labels customization code here
            }]
        });
    });
    
{% endhighlight %}



On executing the above code sample renders a customized gauge with ranges as follows.

![](/js/LinearGauge/Getting-Started_images/Getting-Started_img5.png)

## Add pointers data

In **Linear gauge** there are two types of pointers available such as marker pointer and bar pointer.

* **Marker pointer** displays as a pointer device which shows the actual values. In this example, there is no need to show a marker pointer in a thermometer, therefore, you can hide it by setting the [`opacity`](../api/ejlineargauge#members:scales-markerpointers-opacity) property to ‘0’.

* **Bar pointer** displays as a mercury metal that shows the exact temperature of the person. You can set the basic properties of the bar pointer such as [`width`](../api/ejlineargauge#members:scales-barpointers-width), [`distanceFromScale`](../api/ejlineargauge#members:scales-barpointers-distancefromscale), [`value`](../api/ejlineargauge#members:scales-barpointers-value) and [`backgroundColor`](../api/ejlineargauge#members:scales-barpointers-backgroundcolor).



{% highlight javascript %}

 $(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
            labelColor: "#8c8c8c",
            enableAnimation: false,
            scales: [{
                //Add the pointers customization code here
                markerPointers: [{ opacity: 0 }],
                barPointers: [{
                    width: 10,
                    distanceFromScale: -0.5,
                    value: 37,
                    backgroundColor: "#DB3738"
                }],
                //Add the labels customization code here
                //Add the ticks customization code here
                //Add the Custom labels customization code here
            }]
        });
    });


{% endhighlight %}



On executing the above code sample renders a **Linear Gauge** with bar marker as follows.

![](/js/LinearGauge/Getting-Started_images/Getting-Started_img6.png)

## Add Label Customization

* You can display the label value on both sides to get temperature in different scales. For that you can add two label values in an array.

* You can use the scale labels to display the value by using [`labels`](../api/ejlineargauge#members:scales-labels) property in the gauge. You can customize the label [`placement`](../api/ejlineargauge#members:scales-labels-placement),[`font`](../api/ejlineargauge#members:scales-labels-font) (including its style and family) and its [`distanceFromScale`](../api/ejlineargauge#members:scales-labels-distancefromscale).



{% highlight javascript %}

 $(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
            labelColor: "#8c8c8c",
            enableAnimation: false,
            scales: [{
                //Add the pointers customization code here
                //Add the labels customization code here
                labels: [{
                    placement: "near",
                    font: {
                        size: "10px", fontFamily: "Segoe UI",
                        fontStyle: "Normal"
                    }
                },
                {
                    placement: "far",
                    distanceFromScale: { x: 10 }
                }],
                //Add the ticks customization code here
                //Add the Custom labels customization code here
            }]
        });
    });

{% endhighlight %}



On executing the above code sample renders a customized **Linear Gauge** as follows.

![](/js/LinearGauge/Getting-Started_images/Getting-Started_img7.png)

## Add Ticks Details

* You can set the [`width`](../api/ejlineargauge#members:scales-ticks-width) and [`height`](../api/ejlineargauge#members:scales-ticks-height) of the major ticks greater than the Minor ticks. You can set dark background for tick Color to have a better visibility.

* You can also use four [`ticks`](../api/ejlineargauge#members:scales-ticks) for both the sides, each having two minor ticks and major ticks.



{% highlight javascript %}

 $(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
            labelColor: "#8c8c8c",
            enableAnimation: false,
            scales: [{
                //Add the pointers customization code here
                //Add the labels customization code here
                //Add the ticks customization code here
                ticks: [{
                    type: "majorinterval",
                    height: 8,
                    width: 1,
                    color: "#8c8c8c",
                    distanceFromScale: { y: -4 }
                }, {
                    type: "minorinterval",
                    height: 4,
                    width: 1,
                    color: "#8c8c8c",
                    distanceFromScale: { y: -4 }
                }, {
                    type: "majorinterval",
                    placement: "far",
                    height: 8,
                    width: 1,
                    color: "#8c8c8c",
                    distanceFromScale: { y: -4 }
                }, {
                    type: "minorinterval",
                    placement: "far",
                    height: 4,
                    width: 1,
                    color: "#8c8c8c",
                    distanceFromScale: { y: -4 }
                }],
                //Add the Custom labels customization code here   
            }]
        });
    });

{% endhighlight %}



On executing the above code sample renders a **Linear Gauge** with custom labels as follows.

![](/js/LinearGauge/Getting-Started_images/Getting-Started_img8.png)

## Add Custom Label Details

* You can specify the texts using **Custom labels** which displays in the gauge and customize them using various properties.

* You can change the [`showCustomLabels`](../api/ejlineargauge#members:scales-showcustomlabels) property as **true** to show the custom labels.



The following code example illustrates how to use custom texts.

{% highlight javascript %}

   $(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
            labelColor: "#8c8c8c",
            enableAnimation: false,
            scales: [{
                showCustomLabels: true,
                //Add the pointers customization code here
                //Add the labels customization code here
                //Add the ticks customization code here
                //Add the Custom labels customization code here
                customLabels: [{
                    value: "(° C)",
                    position: { x: 44, y: 78 },
                    font: "Bold 12px Segoe UI", color: "#666666"
                }, {
                    value: "(° F)",
                    position: { x: 56, y: 78 },
                    font: "Bold 12px Segoe UI", color: "#666666"
                },
                {
                    position: { x: 51, y: 90 },
                    font: "Bold 13px Segoe UI",
                    color: "#666666"
                }]
            }]
        });
    });

{% endhighlight %}



On executing the above code sample renders a customized **Linear Gauge** as follows. 

![](/js/LinearGauge/Getting-Started_images/Getting-Started_img9.png)

## Change scale Degree to Fahrenheit

You can add a function to convert the temperature from Degrees to Fahrenheit values in the label by having index value as 1.



{% highlight javascript %}

$(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
            labelColor: "#8c8c8c",
            enableAnimation: false,
            drawLabels: "DrawLabel"
        });
    });
    function DrawLabel(args) {
        if (args.label.index == 1) {
            args.style.textValue = (args.label.value * (9 / 5)) + 32;
            args.style.font = "Normal 10px Segoe UI";
        }
    }



{% endhighlight %}



On executing the above code sample renders a **Linear Gauge** with values in Degrees and Fahrenheit as follows.



![](/js/LinearGauge/Getting-Started_images/Getting-Started_img10.png)

## Add Custom label for Current Value

You can add the function that displays the current temperature value in the custom label.



{% highlight javascript %}


 $(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
            labelColor: "#8c8c8c",
            enableAnimation: false,
            drawCustomLabel: "DrawCustomLabel",
            drawLabels: "DrawLabel"
        });
    });
    function DrawCustomLabel(args) {
        if (args.customLabelIndex == 2) {
            var temp = args.scaleElement.barPointers[0].value;
            var faValue = (temp * (9 / 5)) + 32;
            if (temp == -10) {
                args.style.textValue = "Very Cold Weather" + "(" + faValue.toFixed(1) + "° F)";
            }
            else if ((temp > -10 && temp < 0) || (temp > 0 && temp < 15)) {
                args.style.textValue = "Cool Weather" + " (" + faValue.toFixed(1) + "° F)";
            }
            else if (temp == 0) {
                args.style.textValue = "Freezing point of Water" + " (" + faValue.toFixed(1) + "° F)";
            }
            else if (temp >= 15 && temp < 30) {
                args.style.textValue = "Room Temperature" + " (" + faValue.toFixed(1) + "° F)";
            }
            else if (temp == 30) {
                args.style.textValue = "Beach Weather" + " (" + faValue.toFixed(1) + "° F)";
            }
            else if (temp == 37) {
                args.style.textValue = "Body Temperature" + " (" + faValue.toFixed(1) + "° F)";
            }
            else if (temp == 40) {
                args.style.textValue = "Hot Bath Temperature" + " (" + faValue.toFixed(1) + "° F)";
            }
            else if (temp > 40 && temp < 100) {
                args.style.textValue = "Very Hot Temperature" + " (" + faValue.toFixed(1) + "° F)";
            }
            else if (temp == 100) {
                args.style.textValue = "Boiling point of Water" + " (" + faValue.toFixed(1) + "° F)";
            }
        }
    }


{% endhighlight %}



The following screen shot displays a linear gauge with all the customizations discussed earlier.

![](/js/LinearGauge/Getting-Started_images/Getting-Started_img11.png)

