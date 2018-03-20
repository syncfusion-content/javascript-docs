---
layout: post
title: RangeBand
description: Learn how to add Rangeband to Sparkline .
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

## Range Band  

The [`range band`](../api/ejsparkline#members:rangebandsettings) feature is used to highlight a particular range along the y-axis using [`start`](../api/ejsparkline#members:rangebandsettings-startrange) and [`end`](../api/ejsparkline#members:rangebandsettings-endrange) range property. You can also customize the [`color`](../api/ejsparkline#members:rangebandsettings-color) and [`opacity`](../api/ejsparkline#members:rangebandsettings-opacity) of the range band. 

{% highlight js %}

$("#container").ejSparkline({
            // ...
            rangeBandSettings:{
                startRange:4,
                endRange:30,
                color:"#ff14ae",
                opacity:0.4
            },

            // ...
});

{% endhighlight %}

![](/js/Sparkline/Range-Band_images/Range-Band_img1.png)

