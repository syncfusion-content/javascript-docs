---
layout: post
title: Point Customization
description: Learn how to customize points in Sparkline.
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

## Point Customization

You can customize points by initializing the point colors. The customization options allow you to differentiate the [`first`](../api/ejsparkline#members:startpointcolor), [`last`](../api/ejsparkline#members:endpointcolor), [`highest`](../api/ejsparkline#members:highpointcolor), [`lowest`](../api/ejsparkline#members:lowpointcolor), and [`negative`](../api/ejsparkline#members:negativepointcolor) points. This customization only applicable for line, column and area type Sparkline.

{% highlight js %}

$("#container").ejSparkline({
            // ...
            negativePointColor: "red",
            highPointColor: "blue",
            lowPointColor: "orange",
            startPointColor: "green",
            endPointColor: "green",
            // ...
        });

{% endhighlight %}

![](/js/Sparkline/Point-Customization_images/Point-Customization_img1.png)