---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Digital Gauge
documentation: ug
api : /api/js/ejdigitalgauge
---

# Getting Started

* This section encompasses on how to configure **Digital Gauge**. You can provide your own data for a **Digital Gauge** and make them to display in a required way. 

* You can also customize the default **Digital Gauge** appearance. As a result, **Digital Gauge** looks like a Digital thermometer. 

* **Digital gauge** is used in advertisement, decorative purpose, displaying share details in share market, game score boards, token systems, etc.


![](/js/DigitalGauge/Getting-Started_images/Getting-Started_img1.png)

## Create a Digital Gauge

First create an **HTML** file and then add references to the required libraries.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta charset="utf-8" />
    <link href="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/ej.web.all.min.js"></script>
</head>



{% endhighlight %}



Now add a **&lt;div&gt;** element that acts as a container for **ejDigitalGauge** widget.



{% highlight html %}

<body>
    <div id="DigitalGauge1"></div>
</body>
</html>


{% endhighlight %}



Once the container is added, create the **ejDigitalGauge** widget as follows,



{% highlight javascript %}


 $(function () {
        $("#DigitalGauge1").ejDigitalGauge();
    });



{% endhighlight %}



On executing the above code, sample renders a default **Digital Gauge** with default values as follows.

![](/js/DigitalGauge/Getting-Started_images/Getting-Started_img2.png)

## Set Height and Width values

Basic attributes of each canvas elements are height and width. You can set the [`height`](../api/ejdigitalgauge#members:height) and [`width`](../api/ejdigitalgauge#members:width) of the gauge.

{% highlight javascript %}

 $(function () {
        $("#DigitalGauge1").ejDigitalGauge({
            height: 145,
            width: 260,
        });
    });


{% endhighlight %}



On executing the above code, sample renders a default **Digital Gauge** with the specified height and width values.

![](/js/DigitalGauge/Getting-Started_images/Getting-Started_img3.png)

## Set Items Property

You can customize the **Digital Gauge** using different properties.

**Add Segment and Character Properties**

* In this example, the **Digital Gauge** uses a welcome board in which the text color must be distinctly visible in nature. In order to meet this requirement, you can give some [`segment`](../api/ejdigitalgauge#members:matrixsegmentdata) properties such as [`segment`](../api/ejdigitalgauge#members:segmentdata) spacing, segment width, segment color, segment length and segment opacity.

* **Character** [`type`](../api/ejdigitalgauge#members:items-charactersettings-type) is used to define the Digital representation of the character. Thee five types of character representation are as follows:

  * EightCrossEightDotMatrix

  * SevenSegment

  * FourteenSegment

  * SixteenSegment 

  * EightCrossEightSquareMatrix.



{% highlight javascript %}

$(function () {
        $("#DigitalGauge1").ejDigitalGauge({
            height: 145,
            width: 260,
            items: [{
                segmentSettings: { width: 2, length: 20 },
                characterSettings: { type: "sevensegment", spacing: 12, },
                value: "102",
            }]
        });
    });


{% endhighlight %}

On executing the above code, sample renders a **Digital Gauge** with default values as follows.

![](/js/DigitalGauge/Getting-Started_images/Getting-Started_img4.png)

## Add Background Image

You can add a **&lt;div&gt;** element to set the background for the **Digital Gauge** and attach the styles to the **HTML** page such as height , width, background image **URL** ,background repeat property, etc.In the following code example, image used is a road in California. You can pass the text as **“WELCOME TO CALIFORNIA”**

{% highlight html %}

<div id="frameDiv">
    <div id="DigitalGauge1" style="width: 100%">
    </div>
</div>

{% endhighlight %}

{% highlight css %}


 #frameDiv {
        align: center;
        position: relative;
        margin: 0px auto;
        display: table;
        background-image: url("script/frame.png");
        background-repeat: no-repeat;
    }


{% endhighlight %}


On executing the above code, sample renders a default **Digital Gauge** as follows.           

![](/js/DigitalGauge/Getting-Started_images/Getting-Started_img5.png)

## Add Location

You can position the digital letters inside the canvas element using [`position`](../api/ejdigitalgauge#members:items-position) property.

{% highlight javascript %}

$(function () {
        $("#DigitalGauge1").ejDigitalGauge({
            height: 145,
            width: 260,
            items: [{
                //For Displaying Fahrenheit value
                segmentSettings: { width: 2, length: 20 },
                characterSettings: { type: "sevensegment", spacing: 12, },
                value: "102", position: { x: 15, y: 40 }
            }]
        });
    });


{% endhighlight %}

On executing the above code, sample renders a default **Digital Gauge** as follows.


![](/js/DigitalGauge/Getting-Started_images/Getting-Started_img6.png)

## Add Items collection

You can add [`Items collection`](../api/ejdigitalgauge#members:items) to display the temperature value as used in the Digital thermometer.

{% highlight javascript %}

 $(function () {
        $("#DigitalGauge1").ejDigitalGauge({
            height: 145, width: 260,
            items: [{
                //For Displaying Fahrenheit value
                segmentSettings: { width: 2, length: 20, spacing: 0 },
                characterSettings: { type: "sevensegment", spacing: 12, },
                value: "102",
                position: { x: 15, y: 40 }
            },
            {
                //For displaying degree symbol
                segmentSettings: { width: 2, length: 5, spacing: 0 },
                characterSettings: { type: "sevensegment", spacing: 5, },
                value: "0",
                position: { x: 70, y: 28 }
            },
            {
                //For Displaying Fahrenheit symbol
                segmentSettings: { width: 2, length: 20, spacing: 0 },
                characterSettings: { type: "sevensegment", spacing: 12, },
                value: "F",
                position: { x: 170, y: 40 }
            },
            {
                //For displaying Celsius value
                segmentSettings: { width: 1, length: 9, spacing: 0, color: "#F5b43f" },
                characterSettings: { type: "sevensegment", spacing: 12, },
                value: "38",
                position: { x: 70, y: 90 },
            },
            {
                //For displaying degree symbol
                segmentSettings: { width: 1, length: 3, spacing: 0, color: "#F5b43f" },
                characterSettings: { type: "sevensegment", spacing: 12, },
                value: "0",
                position: { x: 90, y: 80 }
            },
            {
                //For displaying Celsius symbol
                segmentSettings: { width: 1, length: 9, spacing: 0, color: "#F5b43f" },
                characterSettings: { type: "sevensegment", spacing: 12, },
                value: "c",
                position: { x: 120, y: 90 }
            }]
        });
    });


{% endhighlight %}



The following screenshot displays a **Digital Gauge** with all the customizations discussed earlier.

![](/js/DigitalGauge/Getting-Started_images/Getting-Started_img7.png)

