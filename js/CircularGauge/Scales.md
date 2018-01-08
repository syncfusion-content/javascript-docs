---
layout: post
title: Scales
description: scales
platform: js
control: Circular Gauge
documentation: ug
api: /api/js/ejcirculargauge
---

# Scales

**Scales** are the basic functional block of the **Circular Gauge**. By customizing the [`scales`](../api/ejcirculargauge#members:scales), the appearance of the **Gauge** can be improved. The functional blocks of Circular Gauge are 

* Pointers

* Labels

* CustomLabels

* Indicators

* Ticks

* Ranges

* Sub gauges.

## Adding Scale Collection

**Scale collection** is directly added to the **Gauge** object. Refer the following code example to add scale collection in **Gauge** control. You customize the scale radius using [`radius`](../api/ejcirculargauge#members:scales-radius) property. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
  //For circular gauge rendering
    $("#CircularGauge1").ejCircularGauge({
        scales: [{
            radius:150
        }]
    })
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Scales_images/Scales_img1.png)

## Scale Customization

**Colors and Border**

The Scale border is modified with the object called [`border`](../api/ejcirculargauge#members:scales-border). It has two border property namely [`color`](../api/ejcirculargauge#members:scales-border-color) and [`width`](../api/ejcirculargauge#members:scales-border-width) which are used to customize the border color of the scale and border width of the scale. Setting the background color improves the look and feel of the **Circular Gauge**. You can customize the background color of the scale using [`backgroundColor`](../api/ejcirculargauge#members:scales-backgroundcolor). The scale bar of circular gauge can be enabled by setting [`showScaleBar`](../api/ejcirculargauge#members:scales-showscalebar) property as true.


{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

$(function () {
        //For circular gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            scales: [{
                showScaleBar: true,
                radius: 150,
                backgroundColor: "Red",
                border: {
                    //For scale border color
                    color: "Blue",
                    //For scale border width
                    width: 3
                },
                pointers: [{ length: 100 }]
            }]
        })
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Scales_images/Scales_img2.png)

**Pointer Cap**

**Pointer cap** is a circular shape element that is located at the center of the **Circular Gauge**. The pointer cap is one of the cynosure of the **Circular Gauge**. By customizing the pointer cap, Gauge style is improved. The pointer cap is modified with the object [`pointerCap`](../api/ejcirculargauge#members:scales-pointercap). It contains radius, [`borderColor`](../api/ejcirculargauge#members:scales-pointercap-bordercolor), [`borderWidth`](../api/ejcirculargauge#members:scales-pointercap-borderwidth), [`interiorGradient`](../api/ejcirculargauge#members:scales-pointercap-interiorgradient) and [`backgroundColor`](../api/ejcirculargauge#members:scales-pointercap-backgroundcolor) properties. The property [`radius`](../api/ejcirculargauge#members:scales-pointercap-radius) is used to set the radius for the pointer cap. 


{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

  $(function () {
        // For Circular Gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            scales: [{ pointerCap: {
                // For setting pointer cap radius
            radius:10,
                // For setting pointer cap border width
            borderWidth: 4,
                // For setting pointer cap border color
            borderColor: "Blue",
                // For setting pointer cap background color
            backgroundColor: "Red"
            }}]
        })
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Scales_images/Scales_img3.png)

**Appearance**

**Circular Gauge** contains two types of scale direction such as clockwise and counter clockwise. You can set them by enumerable property called [`direction`](../api/ejcirculargauge#members:scales-direction). And you can set the minimum and maximum values for the scale with the properties [`minimum`](../api/ejcirculargauge#members:scales-minimum) and [`maximum`](../api/ejcirculargauge#members:scales-maximum)*. The two properties [`minorIntervalValue`](../api/ejcirculargauge#members:scales-minorintervalvalue) and [`majorIntervalValue`](../api/ejcirculargauge#members:scales-majorintervalvalue) are the values used to set interval value for the ticks and labels. The [`radius`](../api/ejcirculargauge#members:scales-radius) property is used to set the radius value for the circular scale and the [`size`](../api/ejcirculargauge#members:scales-size) property is used to set the scale bar width. You can also adjust the Opacity of the scale with the property [`opacity`](../api/ejcirculargauge#members:scales-opacity). The value for opacity lies between 0 and 1. You can also give some shadow effects for the scale by using the property [`shadowOffset`](../api/ejcirculargauge#members:scales-shadowoffset). 



{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

  $(function () {
        // For Circular Gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            scales: [{
                // For setting scale bar size
                size: 30,
                // For setting scale radius
                scaleRadius: 130,
                // For setting scale minimum value
                minimum: 20,
                // For setting scale maximum value
                maximum: 120,
                // For setting scale major interval value
                majorIntervalValue: 20,
                // For setting scale minor interval
                minorIntervalValue: 5,
                // For setting scale direction
                direction:ej.datavisualization.CircularGauge.Directions.CounterClockwise,
                // For setting scale background color
                backgroundColor:"red",
                // For setting scale bar opacity
                opacity:0.5,
                // For setting scale bar shadow offset
                shadowOffset: 20
            }]
        });
    });

{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Scales_images/Scales_img4.png)

**Circular Gauge Scale Angles**

The property [`startAngle`](../api/ejcirculargauge#members:scales-startangle) is used to set starting position of the scale at certain angle and [`sweepAngle`](../api/ejcirculargauge#members:scales-sweepangle) is used to shrink or expand the scale to certain angle. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

  $(function () {
        // For Circular Gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            scales: [{
                    startAngle: 90,
                    sweepAngle: 200
                 }]
        });
    });

{% endhighlight %}

**Enable/Disable properties**

You can enable / disable properties in Circular Gauge using some properties in scale collection. The [`showIndicators`](../api/ejcirculargauge#members:scales-showindicators) property is used to enable/disable the indicators. [`showLabels`](../api/ejcirculargauge#members:scales-showlabels), [`showTicks`](../api/ejcirculargauge#members:scales-showticks), [`showRanges`](../api/ejcirculargauge#members:scales-showranges), [`showPointers`](../api/ejcirculargauge#members:scales-showpointers) and [`showScaleBar`](../api/ejcirculargauge#members:scales-showscalebar) are used to enable/ disable labels, ticks, ranges, pointers and scale bar respectively. 

## Multiple Scales

You can set **Multiple scales** for a single **Circular Gauge** control by using an array of scale objects. Each scale object is independent of each other. The following code example refers to two scale objects in a **Gauge**.



{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}
$(function () {
        // For Circular Gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            scales: [
            // For setting scale1
            {
                size: 10,
                showScaleBar:true,
                scaleRadius: 150,
                minimum: 20,
                maximum: 120,
                majorIntervalValue: 20,
                minorIntervalValue: 5,
                direction:ej.datavisualization.CircularGauge.Directions.Clockwise,
                shadowOffset: 20,
                pointers:[{value:50,length:120}]
            },
            // For setting second scale
            {
                size: 10,
                showScaleBar:false,
                scaleRadius: 80,
                majorIntervalValue: 10,
                direction:ej.datavisualization.CircularGauge.Directions.CounterClockwise,
                opacity:0.5,
                shadowOffset: 5,
                pointers:[{value:40,length:50}],
                ticks:[{color:"red",distanceFromScale:80}],
                labels:[{ distanceFromScale:40,color:"red"}]

            }]
        });
    });

{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Scales_images/Scales_img5.png)

