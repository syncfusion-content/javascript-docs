---
layout: post
title: Legend
description: legend
platform: js
control: Chart
documentation: ug
---

# Legend

**EjChart** allows you to customize its **legend** position, color, border, size, shape, padding, font styles, opacity etc. You can enable and disable **Chart legends** using **legend visible** property. Default value of **legend****visible** property is set to **“true”**. 

## Legend Title

**EJ Chart** provides **Legend Title** support to the information about the series. It also provides options to customize the **Legend Title** with fonts and alignment.

{% highlight js %}


                $("#container").ejChart({
            legend: {
                visible: true,
                title: {
                    text: "Countries",
                    textAlignment: 'center',
                    font: {
                        size: ' 18px',
                        color: 'black',
                        fontFamily: "Segoe UI",
                        fontStyle: "normal"
                    },
                },
            }
            // ...
        });


{% endhighlight %}



The following screenshot displays **Legend Title**:

{% include image.html url="/js/Chart/Legend_images/Legend_img1.png" %}

## Legend Position

You can position the **legend** at top, bottom, left or right position of the Chart. Default value of **legend****position** is **“bottom”**.  And you can align the legend position using “**alignment**” property of **legend**.  This allows you to align the legend at center, far and near position of Chart area.  Default value of **legend****alignment** is “center”.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: { visible: true, position: 'bottom', alignment: 'center' }
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Legend_images/Legend_img2.png" %}

## Customization

**Legend border and shape**

In **EjChart**, you can customize the legend shape with different symbols like rectangle, circle, cross, diamond, pentagon, hexagon, star, ellipse, triangle etc. Default value of legend **“shape”** is “Rectangle”. And you can draw and customize the outline of Chart legends using border property of legend. Default value of legend border color is **“Transparent”**.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                visible: true,
                border: { color: 'red', width: 2 }, shape: 'circle'
            }
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Legend_images/Legend_img3.png" %}

### Legend rowCount and columnCount

**EjChart** allows you to display the **legend** items for row and column wise using “**rowCount**” and “**columnCount**” property. This is used to avoid overlapping between **legends** and **Chart** area when using more legends in Chart area.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: { visible: true, rowCount: 2 }
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Legend_images/Legend_img4.png" %}

### Legend item style and border customization

EjChart allows you to customize the legend item size, and border color and width using “**itemStyle**” property. Default value of legend item size is (10, 10), and legend item border color is “**Transparent**”.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                visible: true, rowCount: 2,
                itemStyle:
                    {
                        height: 12, width: 12,
                        border: { color: 'magenta', width: 1.5 }
                    },
            }
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Legend_images/Legend_img5.png" %}

### Legend font

You can customize the legend font family, font style, font weight and size and font styles using “**font**” property of **legend**. This is illustrated in the following code example.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                visible: true,
                font: { fontFamily: 'Segoe UI', fontStyle: 'Normal', fontWeight: 'Bold', size: '15px' },
                rowCount: 2,
                border: { color: 'red', width: 2 },
                shape: 'circle'
            }
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Legend_images/Legend_img6.png" %}

### Legend opacity and item padding

**EjChart** allows you to set “**opacity”** for Chart legends. And you can define the spacing between the legend items using “**itemPadding**” property of legend. Default value of **itemPadding** size is 10.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                visible: true, opacity: 1.5, itemPadding: 20,
                itemStyle: {
                    height: 12, width: 12,
                    border: { color: 'magenta', width: 1.5 }
                }
            }
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Legend_images/Legend_img7.png" %}

### Scrollbar for legends

**EjChart** allows you to customize the legend height and width using **size** property. Default value of the height and width are null and it varies depending upon the legend position. If the legen is in top or bottom of the chart, default value of height is 20% of chart height and width is 100% of chart width. Similarly if it is in the left or right side of the chart, default value of height is 100% of chart height and width is 20% of chart width.

This property supports both pixels and percentage values. E.g. 100 or 10%.

Scrollbar is enabled for the legends, when the legend size is greater than the user specified value or than the default value of the legend size.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...     
            commonSeriesOptions:{type: 'pie'},       
            size: { width: '800', height: '600' },
            legend: { visible: true, shape: 'circle', columnCount:2,
                size:{height:'25%',width:'150'}
            }
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Legend_images/Legend_img8.jpeg" %}

### Custom Legend Icons

You can customize the shape of the legend icon. Normally the available shapes are circle, rectangle, star, wedge, uparrow, downarrow, pentagon, etc. By default, the shape of the legend icon is rectangle, you can modify this by setting **shape** property of **legend**. If you want series type as icon then set the **shape property** value as “seriesType”. You can customize the height and width of the icon by setting **itemStyle** property. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                visible: true, position: 'bottom', shape: 'seriesType',
                itemStyle: { height: 15, width: 15 }
            }
            // ...             
        });


{% endhighlight %}


{% include image.html url="/js/Chart/Legend_images/Legend_img9.png" %}

## Legend Selection

Series visibility can be toggled through legend click, now we can control the legend click through **toggleSeriesVisibility** property in legend and this will be used to select or highlight the series through the legend.



{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                visible: true, 
                toggleSeriesVisibility: false  
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img10.png" %}