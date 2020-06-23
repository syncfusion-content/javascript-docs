---
layout: post
title: Segment Setting in JavaScript DigitalGauge widget | Syncfusion
description: You can learn here about segment setting support in Syncfusion JavaScript DigitalGauge control and more details.
platform: js
control: Digital Gauge
documentation: ug
api : /api/js/ejdigitalgauge
---

# Segment Settings in JavaScript DigitalGauge

## Appearance

* **Digital Gauge** consists of several digital segments. [`Segment`](../api/ejdigitalgauge#members:items-segmentsettings) is customized with following properties. 

* [`Color`](../api/ejdigitalgauge#members:items-segmentsettings-color) of the segment is set by using **color** property. Color is either given as string or hexadecimal value. 

* You can add gradient effects to the segments with the help of [`gradient`](../api/ejdigitalgauge#members:items-segmentsettings-gradient) attribute. 

* The [`opacity`](../api/ejdigitalgauge#members:items-segmentsettings-opacity) of the segment is also adjustable. 

* The space between two segments are adjusted with [`spacing`](../api/ejdigitalgauge#members:items-segmentsettings-spacing) property.

* You can set the length of the text segments with [`length`](../api/ejdigitalgauge#members:items-segmentsettings-length) property.

* The width for the text segments are adjusted with [`width`](../api/ejdigitalgauge#members:items-segmentsettings-width) property.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

  $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            width: 800,
            items: [{
                // For setting text
                value: "GO AHEAD",
                segmentSettings: {
                    // For setting segment color
                    color: "Green",
                    // For setting segment opacity
                    opacity: 0.1,
                    // For setting segment spacing
                    spacing: 4,
                }
            }]
        })
    });


{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![Appearance using DigitalGauge in JavaScript](Segment-Settings_images/Segment-Settings_img1.png)

## Dimension Modification

* **Digital Gauge** consists of several digital segments. [`Segment`](../api/ejdigitalgauge#members:matrixsegmentdata) is customized with some properties. Color of the segment is set by using **color** property. Color is either given as string or hexadecimal value. 

* You can add gradient effects to the segments with the help of [`gradient`](../api/ejdigitalgauge#members:items-segmentsettings-gradient) attribute. The [`opacity`](../api/ejdigitalgauge#members:items-segmentsettings-opacity) of the segment is also adjustable. The space between two segments are adjusted with [`spacing`](../api/ejdigitalgauge#members:items-segmentsettings-spacing) property.


{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            width: 800,
            items: [{
                // For setting text
                value: "WELCOME",
                segmentSettings: {
                    // For setting segment length
                    length: 3,
                    // For setting segment width
                    width: 3
                }
            }]
        })
    });


{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.

![Dimension Modification using DigitalGauge in JavaScript](Segment-Settings_images/Segment-Settings_img2.png)

