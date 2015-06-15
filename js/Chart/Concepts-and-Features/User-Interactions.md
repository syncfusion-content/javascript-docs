---
layout: post
title: User-Interactions
description: user interactions
platform: js
control: Chart
documentation: ug
---

# User Interactions

When you deal with a large amount of data, you require interactions like **tooltip**, **crosshair** etc that allows you to track data changes and provide interaction capabilities.

## ToolTip

**EjChart** provides you an option **tooltip** to display a pop up with the point values, on mouse move over the appropriate point. **EjChart** also allows you to customize its border color, border width, opacity, fill color, animation, duration, rx, ry, font size, font family, font style, font color, font weight, etc. You can change the **tooltip** properties for each series in Chart to change its appearance. When you require the same **tooltip** for all the series in Chart, you can specify the **tooltip** in **commonSeriesOptions**. You can also modify the default template for the **tooltip**using template property.

### Tooltip visibility

By default the visibility of **tooltip** is set to **false**, but you can change the visibility. When format or template is not specified for **tooltip**, then it displays the x and y values of the point.

{% highlight js %}


        $("#chartcontainer").ejChart({
            //  . . . 
            commonSeriesOptions: {
                tooltip: { visible: true }
                // . . .
            }
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img1.png" Caption="Chart with Tooltip"%}

### Tooltip format

**EjChart** provides you support to change the format of the text displayed in the tooltip that allows you to use the data point information in desired format.

For single y value, Chart like line series, you can form a format as follows.

format: " **#point.x#****#series.name#  #point.y#**%"

For multiple y values, in financial series, you can form a format as follows.

format: " **#point.x# #series.name# #point.high# #point.low# #point.open# #point.close#** %"

{% highlight js %}


        $("#chartcontainer").ejChart({
            // . . .
            commonSeriesOptions: {
                tooltip: {
                    visible: true, format: "In #point.x# #series.name# produced #point.y#%"
                },
                // . . .
            }
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img2.png" Caption="Chart with formatted ToolTip"%}

### Customize the tooltip border 

EjChart provides you options to customize the border of the tooltip. You can change the width and color of the border. By default the border width is set to 1.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // . . .
            commonSeriesOptions: {
                tooltip: {
                    visible: true, border: { width: 1, color: "#000000" }
                },
                // . . .
            }
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img3.png" Caption="Chart with Customized ToolTip border"%}

### Changing the tooltip fill color

You can modify the fill color of **tooltip**. By default the **tooltip** renders with the appropriate series color as background color.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // . . 
            commonSeriesOptions: {
                tooltip: { visible: true, fill: "#000000" },
                // . . 
            }
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img4.png" Caption="Chart with Customized ToolTip Fill color"%}

### Customize the tooltip font

**EjChart** provides you support to customize the text display in the **tooltip**. You can change font family, font color, font style, font weight. By default **“Segoe UI”** font family is set to **tooltip** text.

{% highlight js %}


       $("#chartcontainer").ejChart({
            // . . .
            commonSeriesOptions: {
                tooltip: {
                    visible: true,
                    font: {
                        fontFamily: "Algerian", fontWeight: "lighter", fontStyle: "Italic", size: "14px", color: "#000000"
                    }
                },
                // . . .
            }
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img5.png" Caption="Chart with Customized ToolTip Font"%}

### Tooltip Animation

**EjChart** provides you animation support for **tooltip** template. You can enable this by setting **“enableAnimation”** to **true**. The **“duration”** property in tooltip specificies the time taken to animate the **tooltip**, by default the duration is set to “500ms”.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // . . 
            commonSeriesOptions: {
                tooltip: {
                    visible: true, template: 'Tooltip', enableAnimation: true, duaration: "600ms"
                }
                // . . .
            }
        });


{% endhighlight %}



### Understanding the rx and ry in tooltip

**EjChart** has **rx** and **ry** property in **tooltip** to customize the corners radius of the **tooltip**.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // . . .
            commonSeriesOptions: {
                tooltip: { visible: true, rx: "50", ry: "50" }
                // . . .                                
            }
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img6.png" Caption="Chart with Animated ToolTip"%}

## Zooming and Panning

**EjChart** provides you an option to zoom the Chart. Using this option you can clearly view the points and data in Chart. Zooming is done by dragging the mouse on the Chart or by scrolling the mouse wheel. During runtime, you can simply select the range you want to zoom with the mouse and the Chart zooms-in accordingly.

### Enable zooming

By default zooming is not enabled. You can enable it using the “enable” option in “zooming” property.

{% highlight js %}


        $("#chartcontainer").ejChart({
            //  . . . 
            zooming: { enable: true }
            // . . .
        });


{% endhighlight %}



**Before zooming**

{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img7.png" Caption="Chart before zooming"%}

**Selection for zooming**

{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img8.png" Caption="Chart with selected area for zooming"%}

**After zooming**

{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img9.png" Caption="Chart after zooming"%}

### Programmatic Zooming

Programmatically the Chart can be zoomed using **zoomPosition** and **zoomFactor** properties.****Both the properties are usually between 0 and 1. When you set the **zoomFactor** to 1, the Chart isn't zoomed. When you set it to 0.5, the Chart is double its usual size. The **zoomPosition** is used to set the starting position of the zoomed axis. For example, when both the properties are set to 0.5 for horizontal axis then the Chart is zoomed to double its size and the view port of the horizontal axis start from half of the axis. 

### Enable zoom via mouse wheel

**EjChart** provides you support to zoom the Chart by scrolling the mouse wheel. By default it is not enabled, you can enable it with the **enableMouseWheel** property in zooming.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // . . .
            zooming: { enable: true, enableMouseWheel : true } 
            // . . .
        });


{% endhighlight %}



### Types of zooming 

**EjChart** supports three types of zooming. You can zoom only the x axis or can zoom only the y axis or can zoom both x and y axis respectively. This is achieved using **type** property in zooming.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // . . .
            zooming: { enable: true, enableMouseWheel: true, type: 'y' }
            //. . .
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img10.png" Caption="Chart with Programmatic zooming"%}

## Crosshair and Trackball

To enable tracking of data points in a Chart, you can use **Crosshair** and **Trackball**.

### Crosshair

In order to view the value at mouse position or touch contact point, you can use the **crosshair** property. You can customize the appearance further using the **crosshair.line** properties. 

To display the label containing the relevant data point value information, enable the **crosshairLabel.visible** property in the corresponding axis of the Chart. For example, to display the x-axis label you can set the **visible** property in **crosshairLabel** of the PrimaryAxis to **true**. You can customize **labels** and **tooltip** rect using font, fill and border properties in **crosshairLabel.**

The following code example illustrates you on how to enable the **crosshair**.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            primaryXAxis:
            {
                crosshairLabel: { visible: true },
            },

            primaryYAxis:
            {
                crosshairLabel: { visible: true },
            },

            crosshair:
            {
                visible: true,
                type: 'crosshair',
                line: { width: 2, color: 'black' }
            },
            // ...             

        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img11.png" Caption="Chart with Crosshairs enabled"%}

### Trackball

In order to track a data point closer to the mouse position or touch contact point, you can use trackball. You can customize the track ball appearance using the marker and line property in the crosshair. To display a label containing the relevant data point value information, you can enable the crosshairLabel.visible property in the corresponding axis of the Chart. For example, to display the x-axis label, set the visible property of crosshairLabel in the PrimaryAxis to true.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            primaryXAxis:
            {
                crosshairLabel: { visible: true, fill: '#E94649' },
            },
            crosshair:
            {
                visible: true,
                type: 'trackball',
                line: { width: 2, color: 'blue' },

            },
            // ...             

        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img12.png" Caption="Chart with Trackball"%}

## Drill Down

**Drill Down** allows you to view the data’s in depth, for example yearly data to quarterly, quarterly to monthly or from categorical data to individual item. The **drill down** support is achieved using the **pointRegionClick** event. On clicking points in Chart series, **pointRegionClick** event gets triggered, using this event you can refresh your Chart by assigning new data to the Chart series through set model. In the following example a pie Chart with two points are used, when you click on the pie slice, **pointRegionClick** event gets triggered. Using this event and set model option, the Chart is refreshed with new data based on the point index.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            series: [{
                points: [{ x: "SUV", y: 25, text: '25%' }, 
                         { x: "Car", y: 37, text: '37%' }],
                name: 'Market'                            
            }
            ],
            pointRegionClick: 'onclick',
            // ...           
        });

       function onclick(sender) {
            var pointIndex = sender.Data.Region.Region.PointIndex
            if (sender.model.series[0].name == "Market")
                $("#container").ejChart("option", { "drilldown": pieSeries(pointIndex) });
        }

        function pieSeries(index) {
            if (index == 0) {
                return {
                    title: { text: 'Automobile Sales in the SUV segment' },
                    series: [{
                        points: [{ x: "Toyota", y: 8, text: 'Toyota 8%' },
                                 { x: "Ford", y: 12, text: 'Ford 12%' },
                                 { x: "GM", y: 17, text: 'GM 17%' }
                        ],
                        name: 'SUV-Sale', labelPosition: 'outside',
                        marker: {
                            dataLabel: { visible: true }
                        }
                    }],

                    legend: { visible: false }
                };
            }
            else if (index == 1) {
                return {
                    title: { text: 'Automobile Sales in the Car segment' },
                    series: [{
                        points: [{ x: "Toyota", y: 7, text: 'Toyota 7%' },
                                 { x: "Chrysler", y: 12, text: 'Chrysler 12%' },
                                 { x: "Nissan", y: 9, text: 'Nissan 9%' }
                        ],

                        name: 'Car-Sale', labelPosition: 'outside',
                        marker: {
                            dataLabel: { visible: true }
                        }
                    }],
                    legend: { visible: false }

                };
            }
        }


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img13.png" Caption="Pie Chart with 2 parts"%}

Details about the first segment/slice in pie Chart:

{% include image.html url="/js/Chart/Concepts-and-Features/User-Interactions_images/User-Interactions_img14.png" Caption="Details about the first segment or slice in Pie Chart"%}

