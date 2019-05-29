---
layout: post
title: Series with PivotChart widget for Syncfusion Essential JS
description: This document illustrates that how to enable series and its customization in JavaScript PivotChart control
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Series

## Series point customization
By using the [`fill`](/api/js/ejchart#members:series-fill) and [`border`](/api/js/ejchart#members:series-border) properties of the chart series, you can customize the series color, border color, and border width of the pivot chart.

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

![Series customization in JavaScript pivot chart control](Series_images/Series_img1.png)