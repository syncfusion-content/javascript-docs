---
layout: post
title: Chart-Types
description: chart types
platform: js
control: OlapChart
documentation: ug
---

# Chart Types

Essential **OlapChart JS** supports 14 different types of chart as follows:

   * Column
   * Stacking Column
   * Bar
   * Stacking Bar
   * Pie
   * Pyramid
   * Funnel
   * Line
   * Step Line
   * Spline
   * Area
   * Step Area
   * Spline Area
   * Stacking Area

## Column Chart

**Column Chart** is the most commonly used chart type. It uses vertical bars (called columns) to display different values of one or more items. Points from adjacent series are drawn as bars next to each other. It is used to compare the frequency, count, total or average of data in different categories. It is ideal to show the variations in the value of an item over a period of time.

{% highlight js %}
$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    }
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.Column
    },
    size: {
        height: "460px",
        width: "950px"
    }
});

{% endhighlight %}

The following screenshot displays a **Column Chart**.

![](/js/OlapChart/Chart-Types_images/Chart-Types_img1.png) 

## Stacking Column Chart

**Stacking Column** Chart is similar to column charts except the Y-values. These Y-values stack on top of each other in a specified series order. This helps to visualize the relationship of parts to whole across categories.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.StackingColumn
    },
    size: {
        height: "460px",
        width: "950px"
    }
});

{% endhighlight %}

The following screenshot displays the **Stacking Column Chart**.

![](/js/OlapChart/Chart-Types_images/Chart-Types_img2.png) 

## Bar Chart

The **Bar Chart** displays horizontal bars for each point in the series and points from adjacent series. Bar charts are used to compare values across categories, for displaying the variations in the value of an item over time or for comparing the values of several items at a single point in time.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.Bar
    },
    size: {
        height: "460px",
        width: "950px"
    }
});


{% endhighlight %}

The following screenshot displays a **Bar Chart**.

![](/js/OlapChart/Chart-Types_images/Chart-Types_img3.png) 

## Stacking Bar Chart

**Stacking Bar Chart** is a regular **bar** chart with the X-values stacked on top of each other in the specified series order.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.StackingBar
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});

{% endhighlight %}

The following screenshot displays the **Stacking Bar Chart.**

![](/js/OlapChart/Chart-Types_images/Chart-Types_img4.png) 

## Pie Chart

A **Pie chart** is used to summarize a set of categorical data or displaying different values of a given variable (e.g., percentage distribution). This type of chart is a circle divided into a series of segments. Each segment represents a particular category.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.Pie
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});


{% endhighlight %}

The following screenshot displays a **Pie Chart**.

![](/js/OlapChart/Chart-Types_images/Chart-Types_img5.png) 

## Pyramid Chart

The **Pyramid Chart** type displays the data in the form of a triangle. It helps you to visualize data in a hierarchical structure without any axes.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.Pyramid
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});

{% endhighlight %}

The following screen shot displays the **Pyramid Chart.**

![](/js/OlapChart/Chart-Types_images/Chart-Types_img6.png) 

## Funnel Chart

The **Funnel Chart**  type displays the data in the form of an inverted triangle. It helps you to visualize data in a hierarchical structure without any axes.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.Funnel
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});

{% endhighlight %}

The following screen shot displays the **Funnel Chart.**

![](/js/OlapChart/Chart-Types_images/Chart-Types_img14.png) 

## Line Chart

The **Line Chart** joins the data points on a plot using straight lines that show trends in data at equal intervals.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.Line
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});

{% endhighlight %}

The following screenshot displays the **Line Chart**.

![](/js/OlapChart/Chart-Types_images/Chart-Types_img7.png) 

## Step Line Chart

**Step Line Chart** uses horizontal and vertical lines to connect the data points resulting in a step like progression. 

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.StepLine
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});


{% endhighlight %}

The following screenshot displays the **Step Line Chart.**

![](/js/OlapChart/Chart-Types_images/Chart-Types_img8.png) 

## Spline Chart

The **Spline Chart** is similar to line charts except it connects different data points using curve lines instead of straight lines.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.Spline
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});

{% endhighlight %}

The following screenshot displays the **Spline Chart**.

![](/js/OlapChart/Chart-Types_images/Chart-Types_img9.png) 

## Area Chart

**Area Chart** emphasizes the degree of change of values over a period of time. Instead of rendering data as discrete bars or columns, an area chart renders it in a continuous ebb-and-flow pattern as defined against the y-axis.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.Area
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});


{% endhighlight %}

The following screenshot displays the **Area Chart**.

![](/js/OlapChart/Chart-Types_images/Chart-Types_img10.png) 

## Step Area Chart

**Step Area** chart is similar to the regular area chart except for a straight line tracing the shortest path between the data points. The values are connected by continuous vertical and horizontal lines forming a step like progression.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.StepArea
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});

{% endhighlight %}

The following screenshot displays a **Step Area Chart.**

![](/js/OlapChart/Chart-Types_images/Chart-Types_img11.png) 

## Spline Area Chart

**Spline Area** chart is similar to Area Chart with the difference in which the data points of a series are connected. It connects each series of points by a smooth **spline curve**.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.SplineArea
    },
    size: {
        height: "460px",
        width: "950px"
    }    
});


{% endhighlight %}

The following Screenshot displays a **Spline Area Chart.**

![](/js/OlapChart/Chart-Types_images/Chart-Types_img12.png) 

## Stacking Area Chart

**Stacking Area** chart is similar to regular area chart except the “Y-values”. These “Y-values” stack on top of each other in the specified series order. This helps to visualize the relationship of parts to whole across categories.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    legend: {
        visible: true,
        rowCount: 3
    },
    commonSeriesOptions: {
        type: ej.olap.OlapChart.ChartTypes.StackingArea
    },
    size: {
        height: "460px",
        width: "950px"
    }   
});


{% endhighlight %}

The following screenshot displays a **Stacking Area Chart.**

![](/js/OlapChart/Chart-Types_images/Chart-Types_img13.png) 

##Combination Chart

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


![](/js/OlapChart/Series_images/combinationalchart.png) 
