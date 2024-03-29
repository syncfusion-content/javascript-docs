---
layout: post
title: Using Essential JavaScript Chart in real-time scenario 
description: Learn how to update the chart dynamically with real-time data. 
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Real-Time Chart 

Chart can be updated dynamically with the real time data. Whenever you add a point or remove a point from the dataSource, you can call the [`redraw`](../api/ejchart#members:redraw) method to request the chart to redraw its content.    

N> You can get the chart **instance** using instance method.

{% highlight javascript %}

     //Rendering empty Chart without data
     $("#container").ejChart({
            
             series: [ 
                     {  points: [ ] }
              ], 
             // ...
       });

    //Using set interval to update chart dynamically
    window.setInterval(updateChart, 200);

    //Function that updates chart dynamically
    function updateChart(){

        //Creating chart instance
        var chart =  $("#container").ejChart("instance");      
        
        if (chart.model.series[0].points.length > 10)
               chart.model.series[0].points.splice(0, 1);
        
        var point = chart.model.series[0].points;
        var xValue = point.length > 0 ? point[point.length - 1].x + 1 : 1;
        point[point.length] = { x:  xValue, y: getRandomNumber( 1000 ) }
                
        //Update Chart dynamically using redraw option
        //chart.redraw() can also be used here instead of redraw option
        $("#container").ejChart("redraw");      
       }

{% endhighlight %}

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/live) here to view the online demo sample for real-time Chart.


