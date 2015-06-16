---
layout: post
title: Chart-Types
description: chart types
platform: js
control: OLAP Chart
documentation: ug
---

### Chart Types

Essential **OLAP Chart JS** supports 13 different types of chart as follows:

   * Column

   * Stacking Column

   * Bar

   * Stacking Bar

   * Area

   * Step Area

   * Spline Area

   * Stacking Area

   * Pie

   * Pyramid

   * Line

   * Step Line

   * Spline

#### Column Chart

**Column Chart** is the most commonly used chart types. It uses vertical bars (called columns) to display different values of one or more items. Points from adjacent series are drawn as bars next to each other. It is used to compare the frequency, count, total or average of data in different categories. It is ideal to show the variations in the value of an item over a period of time.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 }
    commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Column }
});


{% endhighlight %}


The following screenshot displays a **Column Chart**.

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img1.png" Caption="Column chart"%}

<br/>

#### Stacking Column Chart

**Stacking Column** Chart is similar to column charts except the “Y-values”. These “Y-values” stack on top of each other in a specified series order. This helps to visualize the relationship of parts to the whole chart.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
     url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
     commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.StackingColumn }
 });


{% endhighlight %}


The following screenshot displays the **stacking Column Chart**.

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img2.png" Caption="Stacking Column Chart"%}

<br/>

#### Bar Chart

The **Bar Chart** is the simplest and most versatile chart of statistical diagrams. It displays horizontal bars for each point in the series and points from adjacent series. **Bar Charts** are drawn as bars next to each other. **Bar charts** are used to compare values across categories, for displaying the variations in the value of an item over time or for comparing the values of several items at a single point in time.

{% highlight js %}


$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
    commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Bar }
});


{% endhighlight %}


The following screenshot displays a **Bar Chart**.

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img3.png" Caption="Bar Chart"%}

<br/>

#### Stacking Bar Chart

**Stacking Bar Chart** is a Regular **bar** chart with the X-values stacked on top of each other in the specified series order.

{% highlight js %}


$("#OlapChart1").ejOlapChart({
     url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.StackingBar }
 });



{% endhighlight %}


The following screenshot displays the **Stacking Bar Chart.**

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img4.png" Caption="Stacking Bar Chart"%}

<br/>

#### Pie Chart

A **Pie chart** is used to summarize a set of categorical data or displaying different values of a given variable (e.g., percentage distribution). This type of chart is a circle divided into a series of segments. Each segment represents a particular category.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
  url: "../wcf/OlapChartService.svc",legend:{visible:true,rowCount:3},
  commonSeriesOptions:{type: ej.olap.OlapChart.ChartTypes.Pie }                                
});


{% endhighlight %}


The following screenshot displays a **Pie Chart**.

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img5.png" Caption="Pie Chart"%}

<br/>

#### Pyramid Chart

The **Pyramid Chart** type displays the data in the form of a triangle. It helps you to visualize data in a hierarchical structure without any axes.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
     url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
     commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Pyramid }
});


{% endhighlight %}


The following screen shot displays the **Pyramid Chart.**

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img6.png" Caption="Pyramid Chart"%}

<br/>

#### Line Chart

The **Line Chart** joins the data points on a plot using straight lines that show trends in data at equal intervals.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
     url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
     commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Line }
 });



{% endhighlight %}


The following screenshot displays the **Line Chart**.

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img7.png" Caption="Line Chart"%}

<br/>

#### Step Line Chart

**Step Line Chart** uses horizontal and vertical lines to connect the data points resulting in a step like progression. 

{% highlight js %}

$("#OlapChart1").ejOlapChart({
     url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
     commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.StepLine }
 });



{% endhighlight %}


The following screenshot displays the **Step Line Chart.**

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img8.png" Caption="Step Line Chart"%}

<br/>

#### Spline Chart

The **spline chart** is similar to line charts except it connects different data points using curve lines instead of straight lines.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
    commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Spline }
});



{% endhighlight %}


The following screenshot displays the **Spline Chart**.

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img9.png" Caption="Spline Chart"%}

<br/>

#### Area Chart

**Area Chart** emphasizes the degree of change of values over a period of time. Instead of rendering data as discreet bars or columns, an area chart renders it in a continuous ebb-and-flow pattern as defined against the y-axis.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
    commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Area }
});



{% endhighlight %}


The following screenshot displays the **Area Chart**.

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img10.png" Caption="Area Chart"%}

<br/>

#### Step Area Chart

**Step Area** chart is similar to the regular area chart except for a straight line tracing the shortest path between the data points. The values are connected by continuous vertical and horizontal lines forming a step like progression.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
    commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.StepArea }
});


{% endhighlight %}


The following screenshot displays a **Step Area Chart.**

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img11.png" Caption="Step Area Chart"%}

<br/>

#### Spline Area Chart

**Spline Area** chart is similar to Area Chart with the difference in which the data points of a series are connected. It connects each series of points by a smooth **spline curve**.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
    commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.SplineArea }
});


{% endhighlight %}


The following Screenshot displays a **Spline Area Chart.**

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img12.png" Caption="Spline Area Chart"%}

<br/>

#### Stacking Area Chart

**Stacking Area** chart is similar to regular area chart except the “Y-values”. These “Y-values” stack on top of each other in the specified series order. This helps to visualize the relationship of parts to the whole data.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc", legend: { visible: true, rowCount: 3 },
    commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.StackingArea }
});


{% endhighlight %}


The following screenshot displays a **Stacking Area Chart.**

{% include image.html url="/js/OlapChart/Concepts-and-Features/Chart-Types_images/Chart-Types_img13.png" Caption="Stacking Area Chart"%}

