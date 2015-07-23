---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Linear Gauge
documentation: ug
---

# Getting Started

This section briefly explains on how to create a **Linear Gauge** control for your application.

* You can provide data for a **Linear Gauge** and display them in a required way. You can also customize the default **Linear Gauge** appearance to meet your requirements. 

* In this example, you will learn how to create a **Linear Gauge** and how to design a thermometer, which can be used to check the body temperature of a person.



{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img1.png" Caption=""%}

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



{% highlight js %}

$(function () {
        $("#LinearGauge1").ejLinearGauge();
    });

{% endhighlight %}


On executing the above code sample renders a default **Linear Gauge** with default values as follows.


{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img2.png" Caption=""%}

**Set Height and Width values**

* Basic attributes of each canvas elements are height and width properties. 

* You can set the height and width of the gauge as shown in the following code example.



{% highlight js %}

 $(function () {
        $("#LinearGauge1").ejLinearGauge({
            height: 550,
            width: 500,
        });
    });

{% endhighlight %}


On executing the above code sample renders a default **Linear Gauge** with height and width.


{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img3.png" Caption=""%}

## Set animate option and Label Color

* You can draw the Thermometer with Label color and set animate property to _True_.  

* Intially set the animate property to _False_ to avoid unwanted script loads.



{% highlight js %}

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

{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img4.png" Caption=""%}

## Provide scale values

* You can change the Scale Style of Thermometer using **type** property.

* You can set the Minimum temperature up to -10 and maximum body temperature up to 110. 

* You can set the Minimum scale value as -10 and maximum value as 110.

* You can set the Location values such as vertical and horizontal position in the thermometer.

* You can set the thermometer height using **length** property.

* You can set the Minor Interval value as 5 to get the exact temperature of the patient.



{% highlight js %}

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

{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img5.png" Caption=""%}

## Add pointers data

In **Linear gauge** there are two types of pointers available such as marker pointer and bar pointer.

* **Marker pointer** displays as a pointer device which shows the actual values. In this example, there is no need to show a marker pointer in a thermometer, therefore, you can hide it by setting the **Opacity** property to ‘0’.

* **Bar pointer** displays as a mercury metal that shows the exact temperature of the person. You can set the basic properties of the bar pointer such as **width**, **distanceFromScale**, **Value** and **backgroundColor**.



{% highlight js %}

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

{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img6.png" Caption=""%}

## Add Label Customization

* You can display the label value on both sides to get temperature in different scales. For that you can add two label values in an array.

* You can use the scale labels to display the value in the gauge. You can customize the label placement, font (including its style and family) and  its distance from scale.



{% highlight js %}

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

{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img7.png" Caption=""%}

## Add Ticks Details

* You can set the width and height of the major ticks greater than the Minor ticks. You can set dark background for tick Color to have a better visibility.

* You can also use four ticks for both the sides, each having two minor ticks and major ticks.



{% highlight js %}

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

{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img8.png" Caption=""%}

## Add Custom Label Details

* You can specify the texts using **Custom labels** which displays in the gauge and customize them using various properties.

* You can change the **showIndicators** property as **True** to show the custom labels.



The following code example illustrates how to use custom texts.

{% highlight js %}

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
                    font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "bold" }, color: "#666666"
                }, {
                    value: "(° F)",
                    position: { x: 56, y: 78 },
                    font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "bold" }, color: "#666666"
                },
                {
                    position: { x: 51, y: 90 },
                    font: { size: "13px", fontFamily: "Segoe UI", fontStyle: "bold" },
                    color: "#666666"
                }]
            }]
        });
    });

{% endhighlight %}



On executing the above code sample renders a customized **Linear Gauge** as follows. 

{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img9.png" Caption=""%}

## Change scale Degree to Fahrenheit

You can add a function to convert the temperature from Degrees to Fahrenheit values in the label by having index value as 1.



{% highlight js %}

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



{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img10.png" Caption=""%}

## Add Custom label for Current Value

You can add the function that displays the current temperature value in the custom label.



{% highlight js %}


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
            var fahValue = (temp * (9 / 5)) + 32;
            if (temp == -10) {
                args.style.textValue = "Very Cold Weather" + "(" + fahValue.toFixed(1) + "° F)";
            }
            else if ((temp > -10 && temp < 0) || (temp > 0 && temp < 15)) {
                args.style.textValue = "Cool Weather" + " (" + fahValue.toFixed(1) + "° F)";
            }
            else if (temp == 0) {
                args.style.textValue = "Freezing point of Water" + " (" + fahValue.toFixed(1) + "° F)";
            }
            else if (temp >= 15 && temp < 30) {
                args.style.textValue = "Room Temperature" + " (" + fahValue.toFixed(1) + "° F)";
            }
            else if (temp == 30) {
                args.style.textValue = "Beach Weather" + " (" + fahValue.toFixed(1) + "° F)";
            }
            else if (temp == 37) {
                args.style.textValue = "Body Temperature" + " (" + fahValue.toFixed(1) + "° F)";
            }
            else if (temp == 40) {
                args.style.textValue = "Hot Bath Temperature" + " (" + fahValue.toFixed(1) + "° F)";
            }
            else if (temp > 40 && temp < 100) {
                args.style.textValue = "Very Hot Temperature" + " (" + fahValue.toFixed(1) + "° F)";
            }
            else if (temp == 100) {
                args.style.textValue = "Boiling point of Water" + " (" + fahValue.toFixed(1) + "° F)";
            }
        }
    }


{% endhighlight %}



The following screen shot displays a linear gauge with all the customizations discussed earlier.

{% include image.html url="/js/LinearGauge/Getting-Started_images/Getting-Started_img11.png" Caption=""%}

