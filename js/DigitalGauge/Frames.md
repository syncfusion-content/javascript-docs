---
layout: post
title: Frames
description: frames
platform: js
control: Digital Gauge
documentation: ug
api : /api/js/ejdigitalgauge
---

# Frames

## Inner and Outer Width Customization

[`Frames`](../api/ejdigitalgauge#members:frame) are space that enclose the **Digital Gauge**. The inner width of the [`Frame`](../api/ejdigitalgauge#members:frame) is the distance between the canvas element and the frame. The outer width is the distance from the frame. The code example to set frame’s [`innerWidth`](../api/ejdigitalgauge#members:frame-innerwidth) and [`outerWidth`](../api/ejdigitalgauge#members:frame-outerwidth) is as follow.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            // For setting text
            value: "WELCOME",
            frame: {
                // For setting inner width
                innerWidth: 6,
                // For setting outer width
                outerWidth: 10,
            },
        })
    });


{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.

![](/js/DigitalGauge/Frames_images/Frames_img1.png)



## Setting Background Image

For a better appearance, you can set the [`background image`](../api/ejdigitalgauge#members:frame-backgroundimageurl) for the **Digital Gauge** using the property **backgroundImageUrl.** 

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function() {
     // For Digital Gauge rendering
     $("#DigitalGauge1").ejDigitalGauge({
         // For setting text
         value: "RADAR",
         height: 300,
         frame: {
             // For setting background image
             backgroundImageUrl: "board3.jpg",
         },
         items: [{
             position: {
                 x: 95,
                 y: 10
             }
         }]
     })
 });

{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.

![](/js/DigitalGauge/Frames_images/Frames_img2.png)

