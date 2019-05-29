---
layout: post
title: Legend with PivotChart widget for Syncfusion Essential JS
description: This document illustrates that how to define legend and its customization in JavaScript PivotChart control
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Legend

## Legend visibility

You can enable or disable the legend by using the [`visible`](/api/js/ejpivotchart#members:legend) property in the [`legend`](/api/js/ejpivotchart#members:legend) object. By default, the legend is enabled in the pivot chart.

N> By default, the legend is visible in the pivot chart.

{% highlight javascript %}

$(function()
{
    $("#PivotChart1").ejPivotChart(
    {
        ....
        legend:
        {
            //Legend Visibility
            visible: true
        },
        ....
    });
});

{% endhighlight %}

![Legend visibility in JavaScript pivot chart control](Legend_images/Legend_img1.png)

## Legend shape
You can customize the legend [`shape`](/api/js/ejchart#members:legend-shape) in the pivot chart widget. The default value of legend shape is “Rectangle”. The following are the supported legend shapes:

* Rectangle
* Circle
* Cross
* Diamond
* Pentagon
* Hexagon
* Star
* Ellipse
* Triangle.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        ....
        legend:
        {
            //Legend Visibility
            visible: true,
            //Applying Legend Shape
            shape: "Star"
        },
        ....
    });

{% endhighlight %}

![Legend shape in JavaScript pivot chart control](Legend_images/Legend_img2.png)

## Legend position
By using the [`position`](/api/js/ejchart#members:legend-position) property, you can place the legend at top, bottom, left, or right of the pivot chart.

N> The default value of the legend position is bottom in the pivot chart.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        ....
        legend:
        {
            //Legend Visibility
            visible: true,
            //To place the legend at top of the Chart
            position: "top"
        },
        ....
    });

{% endhighlight %}

![Legend position in JavaScript pivot chart control](Legend_images/Legend_img3.png)

## Legend title
To add a legend title, you should specify the title text in the [`title.text`](/api/js/ejchart#members:legend-title-text) property.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        ....
        legend:
        {
            //Legend Visibility
            visible: true,
            //Add title to the Chart legend
            title:
            {
                text: "Countries"
            }
        },
        ....
    });

{% endhighlight %}

![Legend title in JavaScript pivot chart control](Legend_images/Legend_img4.png)

## Legend alignment
You can align the legend to center, far, and near based on its position in the chart area by using the [`alignment`](/api/js/ejchart#members:legend-alignment) .

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        ....
        legend:
        {
            //Legend Visibility
            visible: true,
            //Aligning the legend near to the Chart
            alignment: "Near"
        },
        ....
    });

{% endhighlight %}

![Legend alignment in JavaScript pivot chart control](Legend_images/Legend_img5.png)

## Legend items - size and border
By using the [`itemStyle.width`](/api/js/ejchart#members:legend-itemstyle-width), [`itemStyle.height`](/api/js/ejchart#members:legend-itemstyle-height), and [`itemStyle.border`](/api/js/ejchart#members:legend-itemstyle-border) properties of the legend, you can change the size and border of legend items.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        ....
        legend:
        {
            //Legend Visibility
            visible: true,
            //Changing legend items border, height and width
            itemStyle:
            {
                height: 12,
                width: 12,
                border:
                {
                    color: 'magenta',
                    width: 1.5
                }
            }
        },
        ....
    });

{% endhighlight %}

![Size and border of legend in JavaScript pivot chart control](Legend_images/Legend_img6.png)

## Legend border
By using the [`border`](/api/js/ejchart#members:legend-border) in the legend, you can customize the color and width of the border.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        ....
        legend:
        {
            //Legend Visibility
            visible: true,
            //Setting border color and width to legend
            border:
            {
                color: "#FFC342",
                width: 2
            }
        },
        ....
    });

{% endhighlight %}

![Legend border in JavaScript pivot chart control](Legend_images/Legend_img7.png)

## Legend text
By using the [`font`](/api/js/ejchart#members:legend-font), you can customize the font family, font style, font weight, and size of the legend text.

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        ....
        legend:
        {
            //Legend Visibility
            visible: true,
            //Customizing the legend text
            font:
            {
                fontFamily: 'Segoe UI',
                fontStyle: 'italic',
                fontWeight: 'bold',
                size: '13px'
            },
        },
        ....
    });

{% endhighlight %}

![Legend text in JavaScript pivot chart control](Legend_images/Legend_img8.png)