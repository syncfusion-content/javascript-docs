---
layout: post
title: Series
description: series
platform: js
control: PivotChart
documentation: ug
---

# Series

## Series Point Customization
By using the [`fill`](/js/api/ejchart#members:series-fill) and [`border`](/js/api/ejchart#members:series-border) properties of Chart series, you can customize the PivotChart series color, border color and border width.
 
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