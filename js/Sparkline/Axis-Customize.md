---
layout: post
title: Axis Customize
description: Learn how to customize axis in Sparkline.
platform: ts
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

## Axis Customize 

The Sparkline axis can be collapsed using visible property in [`axisLineSetting`](../api/ejsparkline#members:axisLineSettings) and this not applicable for win-loss. You can customize [`color`](../api/ejsparkline#members:axisLineSettings-color), [`width`](../api/ejsparkline#members:axisLineSettings-width) and [`dash array`](../api/ejsparkline#members:axisLineSettings-dashArray) of axis line.

 {% highlight js %}
 
 $("#container").ejSparkline({
            // ...
            axisLineSettings: {
                visible: true,
                color:"#ff14ae",
            }

            // ...
        });

{% endhighlight %}

![](/js/Sparkline/Axis-Customize_images/Axis-Customize_img1.png)