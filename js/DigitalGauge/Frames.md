---
layout: post
title: Frames
description: frames
platform: js
control: Digital Gauge
documentation: ug
---

# Frames

## Inner and Outer Width Customization

**Frames** are space that enclose the **Digital Gauge**. The inner width of the **Frame** is the distance between the canvas element and the frame. The outer width is the distance from the frame. The code example to set frame’s **innerWidth** and **outerWidth** is as follow.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight js %}

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

{% include image.html url="/js/DigitalGauge/Frames_images/Frames_img1.png" Caption=""%}



## Setting Background Image

For a better appearance, you can set the **background****image** for the **Digital Gauge** using the property **backgroundImageUrl.** 

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            // For setting text
            value: "RADAR",
            frame: {
                // For setting backgroung image
                backgroundImageUrl: "board3.jpg",
            },
            items: [{
                position: {
                    x: 80,
                    y: 10
                }
            }]
        })
    });

{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.

{% include image.html url="/js/DigitalGauge/Frames_images/Frames_img2.png" Caption=""%}

