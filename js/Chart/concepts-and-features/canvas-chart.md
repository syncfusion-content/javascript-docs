---
layout: post
title: canvas-chart
description: canvas chart
platform: js
control: Chart
documentation: ug
---

# Canvas Chart

**EjChart** provides canvas rendering support in Html5. By default, ejChart render in SVG(Scalable Vector Graphics). When you enable the **enableCanvasRendering** option in model, then the chart renders in canvas. Canvas chart is used for fast rendering when using large amount of data points.  And also you can export the canvas chart as an image for further use. All user interaction provided by ejChart can be done in canvas rendering. Canvas chart does not support 3D and animation functionalities that can be done in SVG rendering.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
                   // ...             
         enableCanvasRendering : true,
                   // ...             
               });


{% endhighlight %}



The following screenshot illustrates the canvas chart

![C:\Users\ApoorvahR\Desktop\1.png](canvas-chart_images\canvas-chart_img1.png)

_Canvas Chart_

