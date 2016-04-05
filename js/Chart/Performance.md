---
layout: post
title: Performance tips 
description: How to improve the performance of Essential JavaScript Chart
platform: js
control: Chart
documentation: ug
---

# Performance 

* When there are large number of points to load, you can enable canvas rendering mode in chart. Canvas rendering is faster than SVG because it does not involve manipulating DOM elements as much as SVG rendering.   

{% highlight javascript %}

      $("#chartcontainer").ejChart({
            
            //  ...
            //Enable Canvas rendering mode
            enableCanvasRendering: true,         

            // ...
      });

{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/performance) here to view the online demo sample that shows Chart performance with 100,000 data points.


* Instead of enabling data markers and labels when there are large number of data points, you can use **trackball** and **tooltip** to view point information.

