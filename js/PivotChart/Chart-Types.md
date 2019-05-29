---
layout: post
title: Chart-Types with PivotChart widget for Syncfusion Essential JS
description: This document illustrates that how to define chart types and its customization in JavaScript PivotChart control
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Chart types

Essential **PivotChart JS** supports 18 different types of charts as follows:

   * Column
   * Stacking column
   * Bar
   * Stacking bar
   * Line
   * Step line
   * Spline
   * Area
   * Step area
   * Spline area
   * Stacking area
   * Pie
   * Doughnut
   * Pyramid
   * Funnel
   * Scatter
   * Bubble
   * WaterFall

## Column chart

The **column chart** is the most commonly used chart type. It uses vertical bars (called columns) to display different values of one or more items. Points from adjacent series are drawn as bars next to each other. It is used to compare the frequency, count, total, or average of the data in different categories. It is ideal to show the variations in the value of an item over a period of time.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        }
    });
{% endhighlight %}

The following screenshot displays the **column chart**.

![JavaScript column chart control](Chart-Types_images/ColumnChart.png)

## Stacking column chart

The **stacking column** chart is similar to column chart except the Y-values. These Y-values stack on top of each other in a specified series order. This helps to visualize the relationship of parts to the whole chart across various categories.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StackingColumn
        }
    });
{% endhighlight %}

The following screenshot displays the **stacking column chart**.

![JavaScript stacking column chart control](Chart-Types_images/StackingColumnChart.png)

## Bar chart

The **bar chart** displays horizontal bars for each point in the series and points from adjacent series. Bar charts are used to compare values across various categories for displaying the variations in the value of an item over a period of time or comparing the values of several items in a single point of time.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Bar
        }
    });
{% endhighlight %}

The following screenshot displays a **bar chart**.

![JavaScript bar chart control](Chart-Types_images/BarChart.png)

## Stacking bar chart

The **stacking bar chart** is a regular **bar** chart with the X-values stacked on top of each other in the specified series order.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StackingBar
        }
    });
{% endhighlight %}

The following screenshot displays the **stacking bar chart.**

![JavaScript bar chart control](Chart-Types_images/StackingBarChart.png)

## Line chart

The **line chart** joins the data points on a plot by using straight lines that show trends in the data at equal intervals.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Line
        }
    });
{% endhighlight %}

The following screenshot displays the **line chart**.

![JavaScript line chart control](Chart-Types_images/LineChart.png)

## Step line chart

**Step line chart** uses horizontal and vertical lines to connect the data points resulting in a step like progression.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StepLine
        }
    });
{% endhighlight %}

The following screenshot displays the **step line chart.**

![JavaScript step line chart control](Chart-Types_images/StepLineChart.png)

## Spline chart

The **spline chart** is similar to line chart whereas it connects different data points with curved lines instead of straight lines.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Spline
        }
    });
{% endhighlight %}

The following screenshot displays the **spline chart**.

![JavaScript spline chart control](Chart-Types_images/SplineChart.png)

## Area chart

The **area chart** emphasizes the degree of change of values over a period of time. Instead of rendering the data as discrete bars or columns, the area chart renders continuous ebb-and-flow pattern as defined against the y-axis.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Area
        }
    });
{% endhighlight %}

The following screenshot displays the **area chart**.

![JavaScript area chart control](Chart-Types_images/AreaChart.png)

## Step area chart

The **step area** chart is similar to the regular area chart except a straight line tracing the shortest path between the data points. The values are connected by continuous vertical and horizontal lines to form a step like progression.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StepArea
        }
    });
{% endhighlight %}

The following screenshot displays the **step area chart.**

![JavaScript step area chart control](Chart-Types_images/StepAreaChart.png)

## Spline area chart

The **spline area** chart is similar to area chart which differs by connecting the data points of a series. It connects each series of points by a smooth **spline curve**.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.SplineArea
        }
    });
{% endhighlight %}

The following screenshot displays the **spline area chart.**

![JavaScript spline area chart control](Chart-Types_images/SplineAreaChart.png)

## Stacking area chart

The **stacking area** chart is similar to regular area chart except the “Y-values”. These “Y-values” stack on top of each other in the specified series order. It helps to visualize the relationship of parts to the whole chart across various categories.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StackingArea
        }
    });
{% endhighlight %}

The following screenshot displays the **Stacking Area Chart.**

![JavaScript stacking area chart control](Chart-Types_images/StackingAreaChart.png)

## Pie chart

The **pie chart** is used to summarize a set of categorical data or displaying different values of a given variable (e.g., percentage distribution). This type of chart is a circle form that is divided into several segments. Each segment represents a particular category.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Pie
        }
    });
{% endhighlight %}

The following screenshot displays the **pie chart**.

![JavaScript pie chart control](Chart-Types_images/PieChart.png)

## Doughnut chart

The **doughnut chart** is used to summarize a set of categorical data which possesses a doughnut like structure that is divided into several segments. Each segment represents a particular category.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Doughnut
        }
    });
{% endhighlight %}

The following screenshot displays the **doughnut chart**.

![JavaScript doughnut chart control](Chart-Types_images/DoughnutChart.png)

## Pyramid chart

The **pyramid chart** type displays the data in the form of a triangle. It helps you to visualize the data in a hierarchical structure without any axes.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Pyramid
        }
    });
{% endhighlight %}

The following screenshot displays the **pyramid chart.**

![JavaScript pyramid chart control](Chart-Types_images/PyramidChart.png)

## Funnel chart

The **funnel chart** type displays the data in the form of an inverted triangle. It helps you to visualize the data in a hierarchical structure without any axes.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Funnel
        }
    });
{% endhighlight %}

The following screenshot displays the **funnel chart:**

![JavaScript funnel chart control](Chart-Types_images/FunnelChart.png)

## Scatter chart

The **scatter chart** type displays the data as a collection of points corresponding to associated values.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Scatter
        }
    });
{% endhighlight %}

The following screenshot displays the **scatter chart:**

![JavaScript scatter chart control](Chart-Types_images/ScatterChart.png)

## Bubble chart

The **bubble chart** type displays the data as a collection of bubbles.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Bubble
        }
    });
{% endhighlight %}

The following screenshot displays the **bubble chart:**

![JavaScript bubble chart control](Chart-Types_images/BubbleChart.png)

## WaterFall chart

The **waterfall chart** type is used to show how an initial value is increased and decreased by a series of intermediate values, leading to a final value.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.WaterFall
        }
    });
{% endhighlight %}

The following screenshot displays the **waterfall chart:**

![JavaScript waterfall chart control](Chart-Types_images/WaterFall.png)

## Combination chart

A **combination chart** combines two or more series types in a single chart. But there are some limitations in the combination chart. They are:

   1. The combination chart cannot combine the column and bar series.
   2. Th pie chart cannot be used with other series types.


{% highlight javascript %}

    $(function() {
        $("#PivotChart1").ejPivotChart({
            //...
            commonSeriesOptions: {
                type: ej.PivotChart.ChartTypes.Line
            },
            seriesRendering: "onSeriesRenders"
        });
    });

    function onSeriesRenders(args) {
        this.model.series[5].type = ej.PivotChart.ChartTypes.Column;
        this.model.series[5].marker.visible = true;
    }
{% endhighlight %}


![JavaScript combinations of charts](Chart-Types_images/CombinationChart.png)
