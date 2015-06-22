---
layout: post
title: Canvas-Chart
description: canvas chart
platform: js
control: Chart
documentation: ug
---

# Canvas Chart

**EjChart** provides canvas rendering support in Html5. By default, ejChart render in SVG(Scalable Vector Graphics). When you enable the **enableCanvasRendering** option in model, then the chart renders in canvas. Canvas chart is used for fast rendering when using large amount of data points.  And also you can export the canvas chart as an image for further use. All user interaction provided by ejChart can be done in canvas rendering. Canvas chart does not support 3D and animation functionalities that can be done in SVG rendering.

{% highlight js %}


       $("#chartcontainer").ejChart({
            // ...             
            enableCanvasRendering: true,
            // ...             
        });


{% endhighlight %}

The following screenshot illustrates the canvas chart

{% include image.html url="/js/Chart/Canvas-Chart_images/Canvas-Chart_img1.png" Caption="Canvas Chart"%}


