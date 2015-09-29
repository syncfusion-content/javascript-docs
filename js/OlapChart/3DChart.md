---
layout: post
title: 3D
description: 3d
platform: js
control: OlapChart
documentation: ug
---

# 3D

The OlapChart control provides three dimensional view for Bar, Column, StackingBar, StackingColumn and Pie Charts. The representation of data in 3D Chart is very clear and easy to understand when compared to 2D Chart. You can see all the three dimensions of the series by rotating them. To enable this functionality, you need to set `enable3D` property to "true".

The following code example explains on how to enable 3D in the OlapChart control.

{% highlight js %}
  $("#OlapChart").ejOlapChart(
{
    url: "../wcf/OlapChartService.svc",
    enable3D: true,
    commonSeriesOptions:
    {
        type: ej.olap.OlapChart.ChartTypes.Column
    },
    rotation: 24,
    size:
    {
        height: "450px",
        width: "650px"
    }
});
{% endhighlight %}

{% include image.html url="/js/OlapChart/3DChart_images/3DChart_images1.png"%}




