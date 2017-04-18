---
layout: post
title: Multiple-Items
description: multiple items 
platform: js
control: Digital Gauge
documentation: ug
api : /api/js/ejdigitalgauge
---

# Multiple Items 

The text in the **Digital Gauge** is positioned with position object. This object contains two attributes such as **x** and **y.** The **x** variable positions the text in the horizontal axis and **y** variable positions the text in the vertical axis.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function() {
    // For Digital Gauge rendering
    $("#DigitalGauge1").ejDigitalGauge({
        Width: 1350,
        height: 400,
        frame: {
            backgroundImageUrl: "Board1.png"
        },
        items: [
            // For Item 1
            {
                // For setting text
                value: "BLUE",
                segmentSettings: {
                    color: "blue"
                },
                position: {
                    x: 90,
                    y: 0
                }
            },
            // For Item 2
            {
                // For setting text
                value: "RED",
                segmentSettings: {
                    color: "red"
                },
                position: {
                    x: 90,
                    y: 15
                }
            },
            // For Item 3
            {
                // For setting text
                value: "PINK",
                segmentSettings: {
                    color: "pink"
                },
                position: {
                    x: 90,
                    y: 30
                }
            }
        ]
    });
});


{% endhighlight %}

Execute the above code example to render the **Digital****Gauge** as follows.

![](/js/DigitalGauge/Multiple-Items_images/Multiple-Items_img1.png)

