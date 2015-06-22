---
layout: post
title: Multiple-Items
description: multiple items 
platform: js
control: Digital Gauge
documentation: ug
---

# Multiple Items 

The text in the **Digital Gauge** is positioned with position object. This object contains two attributes such as **x** and **y.** The **x** variable positions the text in the horizontal axis and **y** variable positions the text in the vertical axis.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            Width: 1300,
            height: 300,
            frame: {
                backgroundImageUrl: "Board1.jpg"
            },
            items: [
            // For Item 1
            {
                // For setting text
                value: "YELLOW",
                segmentSettings: { color: "Yellow" },
                position: {
                    x: 80, y: 0
                }
            },
            // For Item 2
            {
                // For setting text
                value: "RED",
                segmentSettings: { color: "red" },
                position: {
                    x: 80, y: 20
                }
            },
            // For Item 3
            {
                // For setting text
                value: "GREEN",
                segmentSettings: { color: "Green" },
                position: {
                    x: 80, y: 40
                }
            }]
        });
    });   


{% endhighlight %}

Execute the above code example to render the **Digital****Gauge** as follows.

{% include image.html url="/js/DigitalGauge/Multiple-Items_images/Multiple-Items_img1.png" Caption="Digital Gauge control with multiple items"%}

