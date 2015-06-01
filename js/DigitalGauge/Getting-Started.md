---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Digital Gauge
documentation: ug
---

# Getting Started

* This section encompasses on how to configure **Digital****Gauge**. You can provide your own data for a **Digital****Gauge** and make them to display in a required way. 

* You can also customize the default **Digital Gauge** appearance. As a result, **Digital Gauge** looks like a Digital thermometer. 

* **Digital gauge** is used in advertisement, decorative purpose, displaying share details in share market, game score boards, token systems, etc.





{% include image.html url="/js/DigitalGauge/Getting-Started_images/Getting-Started_img1.png" Caption="Digital Thermometer"%}

**Create a Digital Gauge**

* First create an **HTML** file and then add references to the required libraries.

{% highlight js %}

**[HTML]**

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta charset="utf-8" />
<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<!--scripts-->
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.js"></script>
<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script></head>



{% endhighlight %}



* Now add a **&lt;div&gt;** element that acts as a container for **ejDigitalGauge** widget.



{% highlight js %}

**[HTML]**

<body>
<div id="DigitalGauge1"></div>
</body>



{% endhighlight %}



* Once the container is added, create the **ejDigitalGauge** widget as follows,



{% highlight js %}

**[HTML]**

<script type="text/javascript">
$(function () {
$("#DigitalGauge1").ejDigitalGauge();
});
</script>




{% endhighlight %}



On executing the above code, sample renders a default **Digital Gauge** with default values as follows.

{% include image.html url="/js/DigitalGauge/Getting-Started_images/Getting-Started_img2.png" Caption="Digital Gauge"%}

**Set Height and Width values**

Basic attributes of each canvas elements are height and width. You can set the height and width of the gauge.

{% highlight js %}

$("#DigitalGauge1").ejDigitalGauge({
height: 145,
width: 260,
});


{% endhighlight %}



On executing the above code, sample renders a default **Digital Gauge** with the specified height and width values.

{% include image.html url="/js/DigitalGauge/Getting-Started_images/Getting-Started_img3.png" Caption="Digital Gauge with height and width set"%}

**Set Items Property**

You can customize the **Digital Gauge** using different properties.

**Add Segment and Character Properties**

* In this example, the **Digital Gauge** uses a welcome board in which the text color must be distinctly visible in nature. In order to meet this requirement, you can give some segment properties such as segment spacing, segment width, segment color, segment length and segment opacity.

* **Character** type is used to define the Digital representation of the character. Thee five types of character representation are as follows:

* EightCrossEightDotMatrix

* SevenSegment

* FourteenSegment

* SixteenSegment 

* EightCrossEightSquareMatrix.



{% highlight js %}

$("#DigitalGauge1").ejDigitalGauge({
height: 145,
width: 260,

items: [{
segmentSettings:{width: 2, length: 20},
characterSettings:{type: "sevensegment",spacing: 12, },
value: "102",
}]
});


{% endhighlight %}

On executing the above code, sample renders a **Digital Gauge** with default values as follows.

{% include image.html url="/js/DigitalGauge/Getting-Started_images/Getting-Started_img4.png" Caption="Digital Gauge"%}

**Add Background Image**

You can add a **&lt;div&gt;** element to set the background for the **Digital Gauge** and attach the styles to the **HTML** page such as height , width, background image **URL** ,background repeat property, etc.In the following code example, image used is a road in California. You can pass the text as **“WELCOME TO CALIFORNIA”**

{% highlight js %}

**[HTML]**

<div id="frameDiv">
<div id="DigitalGauge1" style="width:100%">
</div>
</div>

<style>
#frameDiv {
align : center;
position : relative;
margin : 0px auto;
display :table;
background-image :url("script/frame.png");
background-repeat :no-repeat;
}
</style>



{% endhighlight %}


On executing the above code, sample renders a default **Digital Gauge** as follows.           

{% include image.html url="/js/DigitalGauge/Getting-Started_images/Getting-Started_img5.png" Caption="Digital Gauge with backgound"%}

**Add Location**

You can position the digital letters inside the canvas element using **location** property.

{% highlight js %}

**[Javascript]**
$("#DigitalGauge1").ejDigitalGauge({
height: 145,
width: 260,

items: [{
//For Diplaying Farenheit value
segmentSettings:{width: 2, length: 20},
characterSettings:{type: "sevensegment",spacing: 12, },
value: "102",                       position: { x: 15, y: 40 }

}]
});


{% endhighlight %}



On executing the above code, sample renders a default **Digital Gauge** as follows.



{% include image.html url="/js/DigitalGauge/Getting-Started_images/Getting-Started_img6.png" Caption="Digital Gauge with positioned value"%}

**Add Items collection** 

You can add **Items****collection** to display the temperature value as used in the Digital thermometer.

{% highlight js %}

**[J[Javascript]**

$("#DigitalGauge1").ejDigitalGauge({
height: 145, width: 260,
items: [{
//For Diplaying fahrenheit value
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
position: { x: 70, y: 28 }            },
{
//For displaying fahrenheit symbol
segmentSettings: { width: 2, length: 20, spacing: 0 },
characterSettings: { type: "sevensegment", spacing: 12, },
value: "F",
position: { x: 170, y: 40 }
},
{
//For displaying Celcius value
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
//For displaying celcius symbol
segmentSettings: { width: 1, length: 9, spacing: 0, color: "#F5b43f" },
characterSettings: { type: "sevensegment", spacing: 12, },
value: "c",
position: { x: 120, y: 90 }

}]
});


{% endhighlight %}



The following screenshot displays a **Digital Gauge** with all the customizations discussed earlier.

{% include image.html url="/js/DigitalGauge/Getting-Started_images/Getting-Started_img7.png" Caption="Customized Digital Gauge"%}

