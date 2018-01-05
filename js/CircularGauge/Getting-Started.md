---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Circular Gauge
documentation: ug
api: /api/js/ejcirculargauge
---

# Getting Started

This section encompasses how to configure **Circular Gauge**. You can provide data to a **Circular Gauge** and make them to display  in a required way. 

The following screen shot displays a **Circular Gauge**, which visually represents the functions of an Automobile speedometer with RPM (Rotation per Minute), kph (Kilometer per hour) and it denotes the speed level indicators (Safe, Caution and Danger). 

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img1.png)

## Create a Circular Gauge

First create an **HTML** file and add references to the required libraries.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta charset="utf-8" />
    <link href="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/ej.web.all.min.js">                                                               </script>
</head>



{% endhighlight %}


Add a div element that acts as a container for **ejCircularGauge** widget.

{% highlight html %}


<body>
    <div id="CircularGauge1"></div>
</body>
</html>


{% endhighlight %}



Create the **ejCircularGauge** widget as follows,

{% highlight javascript %}

 $(function () {
        $("#CircularGauge1").ejCircularGauge();
    });

{% endhighlight %}



On executing the above code, sample renders a default **Circular Gauge** with default values as follows.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img2.png)

## Set Height and Width values

Pointers have different height and range. You can set the [`height`](../api/ejcirculargauge#members:height) and [`width`](../api/ejcirculargauge#members:width) of the gauge.

{% highlight javascript %}

  $("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
    });


{% endhighlight %}



The following screenshot displays a **Gauge** in which height and width are set.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img3.png)

## Set Background Color

You can draw the speedometer with dark [`backgroundColor`](../api/ejcirculargauge#members:backgroundcolor) and to vary the speed of the pointer, set the [`readOnly`](../api/ejcirculargauge#members:readonly) option as **False** for user interaction. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
        backgroundColor: "#3D3F3D",
        readOnly: false,
    });


{% endhighlight %}


The above code example renders a **Gauge** as shown in the following screen shot.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img4.png)

## Provide scale values

* The [`scales`](../api/ejcirculargauge#members:scales) values specifies the pointers, ticks, labels, indicators and ranges of **Circular Gauge**.

* You can customize the [`pointerCap`](../api/ejcirculargauge#members:scales-pointercap) using the following options- Cap [`radius`](../api/ejcirculargauge#members:scales-pointercap-radius), Cap [`borderColor`](../api/ejcirculargauge#members:scales-pointercap-bordercolor), cap [`backgroundColor`](../api/ejcirculargauge#members:scales-pointercap-backgroundcolor), pointer cap [`borderWidth`](../api/ejcirculargauge#members:scales-pointercap-borderwidth). 

* Set the [`maximum`](../api/ejcirculargauge#members:scales-maximum) speed limit in the **Gauge** as 200KmpH.

* Major Ticks and Minor Ticks have the [`majorIntervalValue`](../api/ejcirculargauge#members:scales-majorintervalvalue) 20 and [`minorIntervalValue`](../api/ejcirculargauge#members:scales-minorintervalvalue) 5 respectively. The [`showRanges`](../api/ejcirculargauge#members:scales-showranges) and [`showIndicators`](../api/ejcirculargauge#members:scales-showindicators) are used to display the ranges and indicators in their respective positions.

{% highlight javascript %}

 $("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
        backgroundColor: "#3D3F3D",
        readOnly: false,
        scales: [{
            showRanges: true,
            showIndicators: true,
            pointerCap: {
                radius: 15,
                borderWidth: 0,
                backgroundColor: "#797C79",
                borderColor: "#797C79"
            },
            maximum: 200,
            majorIntervalValue: 20,
            minorIntervalValue: 5,
            //Add the labels customization code here
            //Add the pointers customization code here
            //Add the ticks customization code here
            //Add the ranges customization code here
            //Add the indicators customization code here
            //Add the Custom labels customization code here
        }]
    });


{% endhighlight %}



On executing the above code, sample renders a **Circular Gauge** with customized labels as follows.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img5.png)

## Add Label Customization

To display the values in the **Gauge,** scale [`labels`](../api/ejcirculargauge#members:scales-labels) are used. You can customize the label [`color`](../api/ejcirculargauge#members:scales-labels-color).  

{% highlight javascript %}

 $("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
        backgroundColor: "#3D3F3D",
        readOnly: false,
        scales: [{
            //Add the labels customization code here
            labels: [{
                color: "#ffffff"
            }],
            //Add the pointers customization code here
            //Add the ticks customization code here
            //Add the ranges customization code here
            //Add the indicators customization code here
            //Add the Custom labels customization code here
        }]
    });



{% endhighlight %}



On executing the above code, sample renders a default **Circular Gauge** with customized labels as follows.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img6.png)

## Add pointer data

You can use three [`pointers`](../api/ejcirculargauge#members:scales-pointers) that denote kilometer value, rotation per minute value and torque value.The torque value pointer should not be similar to other two pointers. Set the torque pointer as marker pointer. You can set other attributes for pointer such as [`value`](../api/ejcirculargauge#members:scales-pointers-value), [`showBackNeedle`](../api/ejcirculargauge#members:scales-pointers-showbackneedle), [`type`](../api/ejcirculargauge#members:scales-pointers-type), [`markerType`](../api/ejcirculargauge#members:scales-pointers-markertype), [`needleType`](../api/ejcirculargauge#members:scales-pointers-needletype), [`backgroundColor`](../api/ejcirculargauge#members:scales-pointers-backgroundcolor), [`border`](../api/ejcirculargauge#members:scales-pointers-border) [`color`](../api/ejcirculargauge#members:scales-pointers-border-color), [`length`](../api/ejcirculargauge#members:scales-pointers-length), [`width`](../api/ejcirculargauge#members:scales-pointers-width), [`radius`](../api/ejcirculargauge#members:scales-pointers-radius) and [`distanceFromScale`](../api/ejcirculargauge#members:scales-pointers-distancefromscale).

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
        backgroundColor: "#3D3F3D",
        readOnly: false,
        scales: [{
            //Add the labels customization code here
            //Add the pointers customization code here
            pointers: [{
                value: 140,
                distanceFromScale: 60,
                showBackNeedle: false,
                length: 20,
                type: "marker",
                markerType: "triangle",
                width: 10,
                radius: 10,
                backgroundColor: "#FF940A",
                border: {
                    color: "#FF940A"
                },
            },
            {
                value: 110,
                showBackNeedle: false,
                length: 150,
                width: 2,
                radius: 10,
                needleType: "rectangle",
                backgroundColor: "#05AFFF",
                border: {
                    color: "#05AFFF"
                },
            }, {
                value: 67,
                showBackNeedle: false,
                length: 100,
                width: 15,
                radius: 10,
                backgroundColor: "#FC5D07",
                border: {
                    color: "#FC5D07"
                },
            }],
            //Add the ticks customization code here
            //Add the ranges customization code here
            //Add the indicators customization code here
            //Add the Custom labels customization code here
        }]
    });


{% endhighlight %}



On executing the above code, sample renders a customized **Circular Gauge** as follows.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img7.png)

## Add Tick Details

You can display the tick value with customization as given in the following code example. You can set [`width`](../api/ejcirculargauge#members:scales-ticks-width) and [`height`](../api/ejcirculargauge#members:scales-ticks-height) of the Major ticks greater than the Minor [`ticks`](../api/ejcirculargauge#members:scales-ticks). You can set dark background for tick [`color`](../api/ejcirculargauge#members:scales-ticks-color) to have a better visibility. You can specify the tick [`type`](../api/ejcirculargauge#members:scales-ticks-type) either major or minor type tick and [`distanceFromScale`](../api/ejcirculargauge#members:scales-ticks-distancefromscale) values.

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
        backgroundColor: "#3D3F3D",
        readOnly: false,
        scales: [{
            //Add the labels customization code here
            //Add the pointers customization code here
            //Add the ticks customization code here
            ticks: [{
                type: "major",
                distanceFromScale: 70,
                height: 20,
                width: 3,
                color: "#ffffff"
            }, {
                type: "minor",
                height: 12,
                width: 1,
                distanceFromScale: 70,
                color: "#ffffff"
            }],
            //Add the ranges customization code here
            //Add the indicators customization code here
            //Add the Custom labels customization code here
        }]
    });



{% endhighlight %}



On executing the above code, sample renders a **Circular Gauge** with customized labels as follows.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img8.png)

## Add Range Values

Ranges denote the property of scale value in the speedometer. The color values of the [`ranges`](../api/ejcirculargauge#members:scales-ranges) specify the speed variation. Set [`showRanges`](../api/ejcirculargauge#members:scales-showranges) property to **“true”** to show the ranges in the **Circular Gauge**. Select safe zone for low speed, caution zone for moderate speed and high zone for high speed.You can customize the range with the properties such as [`startValue`](../api/ejcirculargauge#members:scales-ranges-startvalue), [`endValue`](../api/ejcirculargauge#members:scales-ranges-endvalue), [`startWidth`](../api/ejcirculargauge#members:scales-ranges-startwidth), [`endWidth`](../api/ejcirculargauge#members:scales-ranges-endwidth), [`backgroundColor`](../api/ejcirculargauge#members:scales-ranges-backgroundcolor), [`border`](../api/ejcirculargauge#members:scales-ranges-border) [`color`](../api/ejcirculargauge#members:scales-ranges-border-color), [`distanceFromScale`](../api/ejcirculargauge#members:scales-ranges-distancefromscale) etc.,

{% highlight javascript %}

 $("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
        backgroundColor: "#3D3F3D",
        readOnly: false,
        scales: [{
            //Add the labels customization code here
            //Add the pointers customization code here
            //Add the ticks customization code here
            //Add the ranges customization code here
            ranges: [{
                distanceFromScale: 30,
                startValue: 0,
                endValue: 70,
                backgroundColor: "#5DF243",
                border: {
                    color: "#FFFFFF"
                },
            }, {
                distanceFromScale: 30,
                startValue: 70,
                endValue: 140,
                backgroundColor: "#F6FF0A",
                border: {
                    color: "#FFFFFF"
                },
            },
            {
                distanceFromScale: 30,
                startValue: 140,
                endValue: 200,
                backgroundColor: "#FF1807",
                border: {
                    color: "#FFFFFF"
                },
            }],
            //Add the indicators customization code here
            //Add the Custom labels customization code here
        }]
    });


{% endhighlight %}



On executing the above code, sample renders a **Circular Gauge** with customized range as follows.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img9.png)

## Add Indicator Details

Indicators denote whether the pointer values are placed in their respective zones. You can position the [`indicators`](../api/ejcirculargauge#members:scales-indicators) on the respective range value for the required changes. You can set the location of the indicator using [`position`](../api/ejcirculargauge#members:scales-indicators-position) property.You can also specify [`height`](../api/ejcirculargauge#members:scales-indicators-height), [`width`](../api/ejcirculargauge#members:scales-indicators-width) and [`type`](../api/ejcirculargauge#members:scales-indicators-type) for indicators. The [`stateRanges`](../api/ejcirculargauge#members:scales-indicators-stateranges) property defines how the indicator should behave when the pointer is in certain values. You can customize state ranges with properties like [`endValue`](../api/ejcirculargauge#members:scales-indicators-stateranges-endvalue), [`startValue`](../api/ejcirculargauge#members:scales-indicators-stateranges-startvalue), [`backgroundColor`](../api/ejcirculargauge#members:scales-indicators-stateranges-backgroundcolor), [`borderColor`](../api/ejcirculargauge#members:scales-indicators-stateranges-bordercolor), [`text`](../api/ejcirculargauge#members:scales-indicators-stateranges-text), [`textColor`](../api/ejcirculargauge#members:scales-indicators-stateranges-textcolor), etc. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
        backgroundColor: "#3D3F3D",
        readOnly: false,
        scales: [{
            //Add the labels customization code here
            //Add the pointers customization code here
            //Add the ticks customization code here
            //Add the ranges customization code here
            //Add the indicators customization code here
            indicators: [
            {
                height: 10,
                width: 10,
                type: "circle",
                position: { x: 210, y: 300 },
                stateRanges: [{
                    endValue: 70,
                    startValue: 0,
                    backgroundColor: "#5DF243",
                    borderColor: "#5DF243",
                    text: "",
                    textColor: "#870505"
                }, {
                    endValue: 200,
                    startValue: 70,
                    backgroundColor: "#145608",
                    borderColor: "#145608",
                    text: "",
                    textColor: "#870505"
                }]
            },
            {
                height: 10,
                width: 10,
                type: "circle",
                position: { x: 255, y: 200 },
                stateRanges: [{
                    endValue: 140,
                    startValue: 70,
                    backgroundColor: "#F6FF0A",
                    borderColor: "#F6FF0A",
                    text: "",
                }, {
                    endValue: 70,
                    startValue: 0,
                    backgroundColor: "#969B0C",
                    borderColor: "#969B0C",
                    text: "",
                }, {
                    endValue: 200,
                    startValue: 140,
                    backgroundColor: "#969B0C",
                    borderColor: "#969B0C",
                    text: "",
                }]
            }, {
                height: 10,
                width: 10,
                type: "circle",
                position: { x: 300, y: 300 },
                stateRanges: [{
                    endValue: 140,
                    startValue: 0,
                    backgroundColor: "#890F06",
                    borderColor: "#890F06",
                    text: "",
                },
                {
                    endValue: 200,
                    startValue: 140,
                    backgroundColor: "#FF1807",
                    borderColor: "#FF1807",
                    text: "",
                }]
            }],
            //Add the Custom labels customization code here
        }]
    });

{% endhighlight %}



On executing the above code, sample renders a **Circular Gauge** with customized indicators as follows.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img10.png)

## Add Custom Label Details

You can specify the text in the **Gauge** using [`customLabels`](../api/ejcirculargauge#members:scales-customlabels) and you can customize it through various properties such as [`value`](../api/ejcirculargauge#members:scales-customlabels-value), [`position`](../api/ejcirculargauge#members:scales-customlabels-position), [`color`](../api/ejcirculargauge#members:scales-customlabels-color), [`font`](../api/ejcirculargauge#members:scales-customlabels-font) [`size`](../api/ejcirculargauge#members:scales-customlabels-font-size), [`fontFamily`](../api/ejcirculargauge#members:scales-customlabels-font-fontfamily) and [`fontStyle`](../api/ejcirculargauge#members:scales-customlabels-font-fontstyle). You can use custom texts to display the three range description.

{% highlight javascript %}


 $("#CircularGauge1").ejCircularGauge({
        width: 500,
        height: 500,
        backgroundColor: "#3D3F3D",
        readOnly: false,
        scales: [{
            //Add the labels customization code here
            //Add the pointers customization code here
            //Add the ticks customization code here
            //Add the ranges customization code here
            //Add the indicators customization code here
            //Add the Custom labels customization code here
            customLabels: [{
                value: "Safe",
                position: { x: 200, y: 280 },
                color: "#5DF243",
                font:
                {
                    size: "12px",
                    fontFamily: "Arial",
                    fontStyle: "Bold"
                }
            }, {
                value: "Caution",
                position: { x: 253, y: 212 },
                color: "#F6FF0A",
                font:
                {
                    size: "12px",
                    fontFamily: "Arial",
                    fontStyle: "Bold"
                }
            }, {
                value: "Danger",
                position: { x: 290, y: 280 },
                color: "#FF1807",
                font:
                {
                    size: "12px",
                    fontFamily: "Arial",
                    fontStyle: "Bold"
                }
            }]
        }]
    });


{% endhighlight %}



The following screenshot displays a **Circular Gauge** control with all customization properties.

![](/js/CircularGauge/Getting-Started_images/Getting-Started_img11.png)

