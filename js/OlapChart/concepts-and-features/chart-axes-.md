---
layout: post
title: chart-axes-
description: chart axes 
platform: js
control: OLAP Chart
documentation: ug
---

# Chart Axes 

**OlapChart** typically have two axes that are used to measure and categorize data: a vertical (y) axis and a horizontal (x) axis. By default horizontal (x) axis and vertical (y) axis is added to the Chart with axis labels, gridlines, and tick lines. You can also customize this axis explicitly by adding axis title or removing gridlines, tick lines that are added to the axis by default.



{% highlight js %}

**[JS]**
$("#OlapChart1").ejOlapChart({
  url: "../wcf/OlapChartService.svc",
  primaryXAxis: { majorTickLines: { visible: false } },
  primaryYAxis: { majorTickLines: { visible: false } },
 });


{% endhighlight %}



**Axis Title Customization**

Primary axis title font appearance is further customized with the help of the following code example.

{% highlight js %}

**[JS]**
$(function () {
    $("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
        commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Column },
        primaryXAxis: { title: { text: "Primary X title customization", font: { color: 'red', fontFamily: 'Segoe UI', fontStyle: 'Italic', size: '18px', opacity: 1, fontWeight: 'lighter' } } },
        primaryYAxis: { title: { text: "Primary Y title customization", font: { color: 'red', fontFamily: 'Segoe UI', fontStyle: 'Italic', size: '18px', opacity: 1, fontWeight: 'lighter' } } }
    });
});



{% endhighlight %}



{% include image.html url="\js\OlapChart\concepts-and-features\chart-axes-_images\chart-axes-_img1.png" Caption="Figure: Primary Axis - Title Customization"%}

**Axis Line**

**Axis line** is drawn in Chart to represent the end of the axis in **ChartArea**. It is customized with the help of following code example.



{% highlight js %}

**[JS]**
$("#OlapChart1").ejOlapChart({
url: "../wcf/OlapChartService.svc", title: { text: "OLAP Chart in Essential Studio" },  
legend: { visible: true, rowCount: 3 },
                                primaryXAxis: {
                                    axisLine: { visible: true },
                                    axisLine: { offset: 1 },
                                    axisLine: { width: 3.5 },
                                },
                                primaryYAxis: {
                                    axisLine: { dashArray: "2,3" }
                                }
});


{% endhighlight %}



{% include image.html url="\js\OlapChart\concepts-and-features\chart-axes-_images\chart-axes-_img2.png" Caption="Figure: Axis Line Customization"%}

**Position Opposed**

**Position** of the primary X and Y axis is set to the top with the help **opposedPosition** property.



{% highlight js %}

**[JS]**
$("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc", title: { text: "OLAP Chart in Essential Studio" },
        primaryXAxis: {opposedPosition: true },primaryYAxis: {opposedPosition: true}
        }
});


{% endhighlight %}



{% include image.html url="\js\OlapChart\concepts-and-features\chart-axes-_images\chart-axes-_img3.png" Caption="Figure: Position Opposed"%}

**Appearance Customization** 

Background, border color and outer width of the Chart Area is customized with the help of following properties.

**Background –** sets the background color for Chart Area.

**Color –** sets the color for the border.

**Width** – sets the width for the border.



{% highlight js %}

**[JS]**
$("#OlapChart1").ejOlapChart({
url: "../wcf/OlapChartService.svc", title: { text: "OLAP Chart in Essential Studio" }, chartArea: { border: { color: "gray", width: 4 }, background: "aqua" }
});


{% endhighlight %}

{% include image.html url="\js\OlapChart\concepts-and-features\chart-axes-_images\chart-axes-_img4.png" Caption="Figure: Chart Area Customization"%}

