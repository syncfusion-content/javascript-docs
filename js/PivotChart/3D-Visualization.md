---
layout: post
title: 3D-Visualization | Essential JS PivotChart widget | Syncfusion
description: This document illustrates that how to define 3d visualization and its types in JavaScript PivotChart control
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# 3D visualization in PivotChart

The pivot chart control allows you to view the data in a 3D view. The following are the chart types that are supported:

* Bar
* Column
* Stacking bar
* Stacking column
* Pie

## 3D column chart

The 3D column chart is rendered by specifying the chart type as **“Column”** in the **“type”** enumeration property of [`commonSeriesOptions`](/api/js/ejpivotchart#members:commonseriesoptions) and setting the [`enable3D`](/api/js/ejpivotchart#members:enable3d) property to **“true”.**

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        .....
        .....
        //Enable 3D Chart
        enable3D: true,
        commonSeriesOptions:
        {
            //Setting chart type to column
            type: ej.PivotChart.ChartTypes.Column
        }
    });
{% endhighlight %}

![JavaScript column chart control rendered in 3D](3D-Visualization_images/ColumnChart3D.png)

## 3D bar chart

The 3D bar chart is rendered by specifying the chart type as **“Bar”** in the **“type”** enumeration property of [`commonSeriesOptions`](/api/js/ejpivotchart#members:commonseriesoptions) and setting the  [`enable3D`](/api/js/ejpivotchart#members:enable3d) property to **“true”.**

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        .....
        .....
        //Enable 3D Chart
        enable3D: true,
        commonSeriesOptions:
        {
            //Setting chart type to bar
            type: ej.PivotChart.ChartTypes.Bar
        }
    });
{% endhighlight %}

![JavaScript bar chart control rendered in 3D](3D-Visualization_images/BarChart3D.png)

## 3D stacking bar chart
The 3D stacking bar chart is rendered by specifying the chart type as **“Stacking Bar”** in the **“type”** enumeration property of [`commonSeriesOptions`](/api/js/ejpivotchart#members:commonseriesoptions) and setting the [`enable3D`](/api/js/ejpivotchart#members:enable3d) property to **“true”.**

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        .....
        .....
        //Enable 3D Chart
        enable3D: true,
        commonSeriesOptions:
        {
            //Setting chart type to stacking bar
            type: ej.PivotChart.ChartTypes.StackingBar
        }
    });
{% endhighlight %}

![JavaScript stacking bar chart control rendered in 3D](3D-Visualization_images/StackingBarChart3D.png)

## 3D stacking column chart
The 3D stacking column chart is rendered by specifying the chart type as **“Stacking Column”** in the **“type”** enumeration property of [`commonSeriesOptions`](/api/js/ejpivotchart#members:commonseriesoptions) and setting the [`enable3D`](/api/js/ejpivotchart#members:enable3d) property to **“true”.**

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        .....
        .....
        //Enable 3D Chart
        enable3D: true,
        commonSeriesOptions:
        {
            //Setting chart type to stacking column
            type: ej.PivotChart.ChartTypes.StackingColumn
        }
    });
{% endhighlight %}

![JavaScript stacking column chart control rendered in 3D](3D-Visualization_images/StackingColumnChart3D.png)

## 3D pie chart
Th 3D pie chart is rendered by specifying the chart type as **"Pie"** in the **“type”** enumeration property of [`commonSeriesOptions`](/api/js/ejpivotchart#members:commonseriesoptions) and setting the [`enable3D`](/api/js/ejpivotchart#members:enable3d) property to **“true”.**

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        .....
        .....
        //Enable 3D Chart
        enable3D: true,
        commonSeriesOptions:
        {
            //Setting chart type to pie
            type: ej.PivotChart.ChartTypes.Pie
        }
    });
{% endhighlight %}

![JavaScript pie chart control rendered in 3D](3D-Visualization_images/PieChart3D.png)

## Rotating 3D chart
You can rotate the 3D chart towards left or right by setting an appropriate angle value to the [`rotation`](/api/js/ejpivotchart#members:rotation) property. The direction of the chart display depends on the positive or negative angle value.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        .....
        .....
        //Enable 3D Chart
        enable3D: true,
        //Rotates the 3D Chart
        rotation: 40
    });

{% endhighlight %}

![JavaScript pivot chart control with 3D rotation](3D-Visualization_images/Rotating3DChart.png)