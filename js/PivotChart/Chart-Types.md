---
layout: post
title: Chart-Types
description: chart types
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Chart types

<<<<<<< HEAD
Essential **PivotChart JS** supports 17 different types of charts as follows:
=======
Essential **PivotChart JS** supports seventeen different types of chart as follows:
>>>>>>> hotfix/hotfix-v15.4.0.20

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

## Column chart

<<<<<<< HEAD
The **column chart** is the most commonly used chart type. It uses vertical bars (called columns) to display different values of one or more items. Points from adjacent series are drawn as bars next to each other. It is used to compare the frequency, count, total, or average of data in different categories. It is ideal to show the variations in the value of an item over a period of time.
=======
The **column chart** is the most commonly used chart type. It uses vertical bars (called columns) to display different values of one or more items. Points from adjacent series are drawn as bars next to each other. It is used to compare the frequency, count, total, or average of the data in different categories. It is ideal to show the variations in the value of an item over a period of time.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}
    
    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        }
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **column chart**:
=======
The following screenshot displays the **column chart**.
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/ColumnChart.png)

## Stacking column chart

<<<<<<< HEAD
The **stacking column** chart is similar to column charts except the Y-values. These Y-values stack on top of each other in a specified series order. This helps to visualize the relationship of parts to the whole chart across various categories.
=======
The **stacking column** chart is similar to column chart except the Y-values. These Y-values stack on top of each other in a specified series order. This helps to visualize the relationship of parts to the whole chart across various categories.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StackingColumn
        }
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **stacking column chart**:
=======
The following screenshot displays the **stacking column chart**.
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/StackingColumnChart.png)

## Bar chart

<<<<<<< HEAD
The **bar chart** displays horizontal bars for each point in the series and points from adjacent series. Bar charts are used to compare values across various categories for displaying the variations in the value of an item over a period of time or comparing the values of several items at a single point in time.
=======
The **bar chart** displays horizontal bars for each point in the series and points from adjacent series. Bar charts are used to compare values across various categories for displaying the variations in the value of an item over a period of time or comparing the values of several items in a single point of time.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Bar
        }
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **bar chart**:
=======
The following screenshot displays a **bar chart**.
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/BarChart.png)

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

<<<<<<< HEAD
The following screenshot displays the **stacking bar chart**:
=======
The following screenshot displays the **stacking bar chart.**
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/StackingBarChart.png) 

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

<<<<<<< HEAD
The following screenshot displays the **line chart**:
=======
The following screenshot displays the **line chart**.
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/LineChart.png)

## Step line chart

<<<<<<< HEAD
The **step line chart** uses horizontal and vertical lines to connect the data points resulting in a step like progression.
=======
**Step line chart** uses horizontal and vertical lines to connect the data points resulting in a step like progression.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StepLine
        }
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **step line chart:**
=======
The following screenshot displays the **step line chart.**
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/StepLineChart.png)

## Spline chart

<<<<<<< HEAD
The **spline chart** is similar to line chart whereas it connects different data points by using curved lines instead of straight lines.
=======
The **spline chart** is similar to line chart whereas it connects different data points with curved lines instead of straight lines.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Spline
        }   
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **spline chart**:
=======
The following screenshot displays the **spline chart**.
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/SplineChart.png)

## Area chart

<<<<<<< HEAD
The **area chart** emphasizes the degree of change of values over a period of time. Instead of rendering data as discrete bars or columns, an area chart renders it in a continuous ebb-and-flow pattern as defined against the y-axis.
=======
The **area chart** emphasizes the degree of change of values over a period of time. Instead of rendering the data as discrete bars or columns, the area chart renders continuous ebb-and-flow pattern as defined against the y-axis.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Area
        }   
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **area chart**:
=======
The following screenshot displays the **area chart**.
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/AreaChart.png)

## Step area chart

<<<<<<< HEAD
The **step area** chart is similar to the regular area chart except for a straight line tracing the shortest path between the data points. The values are connected by continuous vertical and horizontal lines to form a step like progression.
=======
The **step area** chart is similar to the regular area chart except a straight line tracing the shortest path between the data points. The values are connected by continuous vertical and horizontal lines to form a step like progression.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StepArea
        }   
    });
{% endhighlight %}

The following screenshot displays the **step area chart.**

![](Chart-Types_images/StepAreaChart.png)

## Spline area chart

<<<<<<< HEAD
The **spline area** chart is similar to area chart with the difference in which the data points of a series are connected. It connects each series of points by a smooth **spline curve**.
=======
The **spline area** chart is similar to area chart which differs by connecting the data points of a series. It connects each series of points by a smooth **spline curve**.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.SplineArea
        }    
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **spline area chart:**
=======
The following screenshot displays the **spline area chart.**
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/SplineAreaChart.png)

## Stacking area chart

<<<<<<< HEAD
The **stacking area** chart is similar to regular area chart except the “Y-values”. These “Y-values” stack on top of each other in the specified series order. This helps to visualize the relationship of parts to the whole chart across various categories.
=======
The **stacking area** chart is similar to regular area chart except the “Y-values”. These “Y-values” stack on top of each other in the specified series order. It helps to visualize the relationship of parts to the whole chart across various categories.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StackingArea
        }  
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **stacking area chart:**
=======
The following screenshot displays the **Stacking Area Chart.**
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/StackingAreaChart.png)

## Pie chart

<<<<<<< HEAD
A **pie chart** is used to summarize a set of categorical data or display the different values of a given variable (e.g., percentage distribution). This type of chart is in a circle shape that is divided into a series of segments. Each segment represents a particular category.
=======
The **pie chart** is used to summarize a set of categorical data or displaying different values of a given variable (e.g., percentage distribution). This type of chart is a circle form that is divided into several segments. Each segment represents a particular category.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Pie
        }
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **pie chart**:
=======
The following screenshot displays the **pie chart**.
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/PieChart.png)

## Doughnut chart

<<<<<<< HEAD
A **doughnut chart** is used to summarize a set of categorical data which possesses a doughnut like structure that is divided into a series of segments. Each segment represents a particular category.
=======
The **Doughnut chart** is used to summarize a set of categorical data which possesses a doughnut like structure that is divided into several segments. Each segment represents a particular category.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Doughnut
        }
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **doughnut chart**:
=======
The following screenshot displays the **doughnut chart**.
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/DoughnutChart.png)

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

<<<<<<< HEAD
The following screenshot displays the **pyramid chart.**
=======
The following screen shot displays the **pyramid chart.**
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/PyramidChart.png)

## Funnel chart

<<<<<<< HEAD
The **funnel chart** type displays the data in the form of an inverted triangle. It helps you to visualize the data in a hierarchical structure without any axes.
=======
The **funnel chart** type displays the data in the form of an inverted triangle. It helps you to visualize data in a hierarchical structure without any axes.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Funnel
        }   
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **funnel chart:**
=======
The following screen shot displays the **funnel chart.**
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/FunnelChart.png)

## Scatter chart

<<<<<<< HEAD
The **scatter chart** type displays the data as a collection of points corresponding to the associated values.
=======
The **scatter chart** type displays the data as a collection of points corresponding to associated values.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({
        //...
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Scatter
        }   
    });
{% endhighlight %}

<<<<<<< HEAD
The following screenshot displays the **scatter chart:**
=======
The following screen shot displays the **scatter chart.**
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/ScatterChart.png) 

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

<<<<<<< HEAD
The following screenshot displays the **bubble chart:**
=======
The following screen shot displays the **bubble chart.**
>>>>>>> hotfix/hotfix-v15.4.0.20

![](Chart-Types_images/BubbleChart.png)

## Combination chart

A **combination chart** combines two or more series types in a single chart. But there are some limitations in the combination chart. They are:

   1. The combination chart cannot combine the column and bar series.
<<<<<<< HEAD
   2. Th pie chart cannot be used with other series types.
=======
   2. The pie chart cannot be used with other series types.
>>>>>>> hotfix/hotfix-v15.4.0.20


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


![](Chart-Types_images/CombinationChart.png)
