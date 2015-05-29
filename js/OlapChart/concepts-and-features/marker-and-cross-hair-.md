---
layout: post
title: marker-and-cross-hair-
description: marker and cross hair 
platform: js
control: OLAP Chart
documentation: ug
---

# Marker and Cross Hair 

**Markers** are the symbols that represent on the series of the Chart Area. **Cross Hair** helps you to view the value at mouse position or touch contact point.

**Real-time use of Cross Hair**

You can view the information while moving the mouse pointer over the Chart Area with the help of **Cross****Hair**. For example, in a **line chart** you can get exact values of x and y axis while moving the mouse on Chart Area.



{% include image.html url="\js\OlapChart\concepts-and-features\marker-and-cross-hair-_images\marker-and-cross-hair-_img1.png" Caption="Figure: Real time use of Cross Hair"%}

**Marker Shape Customization** 

In **OlapChart**, you can customize the marker shape with different symbols like rectangle, circle, cross, diamond, pentagon, hexagon, star, ellipse, triangle etc.

{% highlight js %}

**[JS]** 
$(function () {
 $("#OlapChart1").ejOlapChart({
   url: "../wcf/OlapChartService.svc",
   commonSeriesOptions: { type: ej.olap.OlapChart.chartTypes.Line },
   seriesRendering: "onSeriesRenders"
   });
});

function onSeriesRenders(args) {
   for (var seriescount = 0; seriescount < this.model.series.length; seriescount++)
      this.model.series[seriescount].marker.shape = "Triangle";
}


{% endhighlight %}



{% include image.html url="\js\OlapChart\concepts-and-features\marker-and-cross-hair-_images\marker-and-cross-hair-_img2.png" Caption="Figure: Marker Shape Customization"%}

**Cross Hair Customization** 

In order to view the value at mouse position or touch contact point, you can use the **crosshair** property. You can customize the appearance using the following code example.

{% highlight js %}

**[JS]**
$("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc", 
        primaryXAxis: { crosshairLabel: { visible: true }, },
        primaryYAxis: { crosshairLabel: { visible: true }, },
        crosshair:
         {
             marker: { size: { height: 5, width: 5 } },
             visible: true,
             type: 'crosshair',
             line: { width: 2, color: 'red' }
         }
});


{% endhighlight %}





{% include image.html url="\js\OlapChart\concepts-and-features\marker-and-cross-hair-_images\marker-and-cross-hair-_img3.png" Caption="Figure: Cross Hair Customization"%}

