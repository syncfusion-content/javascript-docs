---
layout: post
title: Series
description: series
platform: js
control: OlapChart
documentation: ug
---

# Series

**Series** is an organization of actual data points to be plotted in a chart area with specified chart type.

##Series Points Customization

**OlapChart** series is customized using fill and border settings. The stroke-width of the line, spline series is customized using [width](/js/api/ejChart#members:series-border-width) property of series.  The series color is customized using [fill](/js/api/ejChart#members:series-fill) property of series. The border color and width of the column/bar is customized using [border](/js/api/ejChart#s#members:series-border) property of series. And the column/bar chart are customized using the [fill](/js/api/ejChart#members:series-fill) and [border](/js/api/ejChart#members:series-border) property of each point.

{% highlight js %}
 
$(function() {
    $("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc",
        size: {
            height: "460px",
            width: "950px"
        },
        commonSeriesOptions: {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args) {
    this.model.series[0].points[0].fill = "aqua";
    this.model.series[0].points[0].border = {
        color: "black",
        width: 2
    };
}

{% endhighlight %}

![](/js/OlapChart/Series_images/Series_img2.png) 
