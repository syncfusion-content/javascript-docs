---
layout: post
title: Series
description: series
platform: js
control: OlapChart
documentation: ug
---

# Series

**Series** is a collection of series items that contain the actual data points to be displayed on the chart. Series type allows you to customize the chart type whose appearance/style is customized.

##Series Type Customization

A combination Chart combines two or more series types in a single Chart. But there are some limitations in the combination Chart. They are:

   1. Can’t combine Column and Bar series.
   2. Pie Chart can’t be used with other series types.


{% highlight js %}

$(function() {
    $("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc",
        size: {
            height: "460px",
            width: "950px"
        },
        animation: true,
        commonSeriesOptions: {
            type: ej.olap.OlapChart.ChartTypes.Column,
            tooltip: {
                visible: true
            }
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args) {
    this.model.series[5].type = ej.olap.OlapChart.ChartTypes.Line;
    this.model.series[5].marker.visible = true;
}

{% endhighlight %}


{% include image.html url="/js/OlapChart/Series_images/Series_img1.png" %}

##Series Points Customization

**OlapChart** series is customized using `fill, border width and border color`. The stroke-width of the line, spline series is customized using [width](/js/api/ejChart#seriesborderwidthspan-classtype-signature-type-numbernumberspan) property of series.  The series color is customized using [fill](/js/api/ejChart#fillseriesfillspan-classtype-signature-type-stringstringspan) property of series. The border color and width of the column/bar is customized using [border](/js/api/ejChart#seriesborderspan-classtype-signature-type-objectobjectspan) property of series. And the column/bar chart are customized using the [fill](/js/api/ejChart#fillseriesfillspan-classtype-signature-type-stringstringspan) and [border](/js/api/ejChart#seriesborderspan-classtype-signature-type-objectobjectspan) property of each point.

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



