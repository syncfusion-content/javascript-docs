---
layout: post
title: Series
description: series
platform: js
control: OlapChart
documentation: ug
---

#Series

##Series Point customization
By using the [`fill`](/js/api/ejchart#members:series-fill) and [`border`](/js/api/ejchart#members:series-border) properties of Chart series, you can customize the OlapChart series color, border color and border width.
 
{% highlight javascript %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        size:
        {
            height: "460px",
            width: "950px"
        },
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    this.model.series[0].points[0].fill = "aqua";
    this.model.series[0].points[0].border = {
        color: "black",
        width: 2
    };
}

{% endhighlight %}

![](Series_images/Series_img1.png)