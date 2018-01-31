---
layout: post
title: Series
description: series
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Series

## Series Point Customization
By using the [`fill`](/api/js/ejchart#members:series-fill) and [`border`](/api/js/ejchart#members:series-border) properties of Chart series, you can customize the pivot chart series color, border color and border width.
 
{% highlight javascript %}
$(function()
{
    $("#PivotChart1").ejPivotChart(
    {
        ....
        commonSeriesOptions:
        {
            type: ej.PivotChart.ChartTypes.Column
        },
        seriesRendering: "onSeriesRender"
    });
});

function onSeriesRender(args)
{
    this.model.series[0].points[0].fill = "aqua";
    this.model.series[0].points[0].border = {
        color: "black",
        width: 2
    };
}

{% endhighlight %}

![](Series_images/Series_img1.png)