---
layout: post
title: Performance tips 
description: How to improve the performance of Essential JavaScript Chart
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Performance 

* When there are large number of points to load, you can enable canvas rendering mode in chart. Canvas rendering is faster than SVG because it does not involve manipulating DOM elements as much as SVG rendering.   

{% highlight javascript %}

      $("#container").ejChart({
            
            //  ...
            //Enable Canvas rendering mode
            enableCanvasRendering: true,         

            // ...
      });

{% endhighlight %}

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/performance) here to view the online demo sample that shows Chart performance with 100,000 data points.


* Instead of enabling data markers and labels when there are large number of data points, you can use **trackball** and **tooltip** to view point information.

## Lazy Loading

Lazy loading feature provides an effective way for loading data on demand by scrolling and viewing a smaller range of data from a larger collection.

{% highlight javascript %}

      $("#container").ejChart({
   
            primaryXAxis:
            {
                
                  scrollbarSettings: {

                              // enable the scrollbar

                              visible: true,  
       
                              // enable the resize option 

                              canResize: true,
       
                              range: {

                                       min: “2009/1/1”,
 
                                       max: “2014/1/1”
  
                              }        
                  }    
            },    
            // . . .	
      });

{% endhighlight %}

![](/js/Chart/Performance_images/Perform_img1.png)