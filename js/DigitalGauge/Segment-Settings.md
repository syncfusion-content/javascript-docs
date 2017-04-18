---
layout: post
title: Segment-Settings
description: segment settings
platform: js
control: Digital Gauge
documentation: ug
api : /api/js/ejdigitalgauge
---

# Segment Settings

## Appearance

* **Digital Gauge** consists of several digital segments. Segment is customized with some properties. Color of the segment is set by using **color** property. Color is either given as string or hexadecimal value. 

* You can add gradient effects to the segments with the help of **gradient** attribute. The **opacity** of the segment is also adjustable. The space between two segments are adjusted with **spacing** property.

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

![](/js/DigitalGauge/Segment-Settings_images/Segment-Settings_img1.png)

## Dimension Modification

* **Digital Gauge** consists of several digital segments. Segment is customized with some properties. Color of the segment is set by using **color** property. Color is either given as string or hexadecimal value. 

* You can add gradient effects to the segments with the help of **gradient** attribute. The **opacity** of the segment is also adjustable. The space between two segments are adjusted with **spacing** property.


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

![](/js/DigitalGauge/Segment-Settings_images/Segment-Settings_img2.png)

