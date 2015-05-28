---
layout: post
title: empty-points
description: empty points
platform: js
control: Chart
documentation: ug
---

# Empty Points

The data that is passed to the Chart can have null or undefined values that are considered as empty points. Series type like line, spline, area, splinearea, stepline, steparea, column, bar, bubble, scatter, hilo, hiloopenclose, candle, rangecolumn and stacking series having empty point support.

{% highlight js %}

**[JS]**

$("#chartcontainer").ejChart(
               {   
                   // ...             
                   series: [{
                               points: [

                               { x: 1, y: 210 }, { x: 2, y: 150},
                               { x: 3, y: 200 }, { x: 4, y: null },
                               { x: 5, y: 170 }, { x: 6, y: 230 },
                               { x: 7, y: 120 },  
                               ],
                               name: 'Course', type: 'column',
                           }
                      ],	
                   // ...             
               });


{% endhighlight %}



{% include image.html url="\js\Chart\concepts-and-features\empty-points_images\empty-points_img1.png" Caption="Chart with Empty Points"%}

