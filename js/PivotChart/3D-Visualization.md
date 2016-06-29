---
layout: post
title: 3D-Visualization
description: 3d visualization
platform: js
control: PivotChart
documentation: ug
---

# 3D Visualization

The PivotChart control allows you to view the data in a 3D view with 5 different chart types namely Bar, Column, Stacking Bar, Stocking Column and Pie.

## 3D Column Chart

3D Column Chart is rendered by specifying the chart type as **“Column”** in the **“type”** enumeration property of **“commonSeriesOptions”** along with [`enable3D`](/js/api/ejchart#members:enable3d) property set to **“true”.**

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

![](3D-Visualization_images/3DColumnChart.png)

## 3D Bar Chart

3D Bar Chart is rendered by specifying the chart type as **“Bar”** in the **“type”** enumeration property of **“commonSeriesOptions”** along with  [`enable3D`](/js/api/ejchart#members:enable3d) property set to **“true”.**

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

![](3D-Visualization_images/3DBarChart.png)

## 3D Stacking Bar Chart
3D Stacking Bar Chart is rendered by specifying the chart type as **“Stacking Bar”** in the **“type”** enumeration property of **“commonSeriesOptions”** along with [`enable3D`](/js/api/ejchart#members:enable3d) property set to **“true”.**

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

![](3D-Visualization_images/3DStackingBarChart.png)

## 3D Stacking Column Chart
3D Stacking Column Chart is rendered by specifying the chart type as **“Stacking Column”** in the **“type”** enumeration property of **“commonSeriesOptions”** along with [`enable3D`](/js/api/ejchart#members:enable3d) property set to **“true”.**

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

![](3D-Visualization_images/3DStackingColumnChart.png)

## 3D Pie Chart
3D Pie Chart is rendered by specifying the chart type as **"Pie"** in the **“type”** enumeration property of **“commonSeriesOptions”** along with [`enable3D`](/js/api/ejchart#members:enable3d) property set to **“true”.**

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

![](3D-Visualization_images/3DPieChart.png)

##Rotating 3D Chart
We can rotate the 3D Chart towards left or right by setting an appropriate angle value to the [`rotation`](/js/api/ejchart#members:rotation) property. The direction of the Chart display depends upon the positive or negative angle value.

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

![](3D-Visualization_images/Rotating3DChart.png)