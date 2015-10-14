---
layout: post
title: Empty Points 
description: empty points 
platform: js
control: Chart
documentation: ug
---

# Empty Points 

The Data points that uses the **null** or **undefined** as value are considered as empty points. Empty data points are ignored and not plotted in the Chart. When the data is provided by using the **points** property, you can set the **isEmpty** to true to specify that the particular point is an empty point.   

{% highlight js %}

      $("#chartcontainer").ejChart({
            series : [{

                 //Using empty points
                 points: [ 
                      { x: 1, y: 50 },
                      { x: 2, y: null },
                      { x: 3, y: 70 },
                      { x: 4, y: 60, isEmpty: true },
                      { x: 5, y: 50 }   
                 ],    
            }],
            // ...
       });

{% endhighlight %}

![]("/js/Chart/Empty-Points_images/Empty-Points_img1.png" Caption="Chart with empty points")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/emptypoints) here to view the online demo sample for empty points.
