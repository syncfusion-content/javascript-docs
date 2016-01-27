---
layout: post
title: User-Interactions
description: user interactions
platform: js
control: OlapChart
documentation: ug
---

#User Interactions

##Tooltip

###Enable Tooltip for Data Points
Tooltip for the data points can be enabled using the **"visible"** option of the [`tooltip`](/js/api/ejchart#members:commonseriesoptions-tooltip-visible) property under **"commonSeriesOptions"** of the OlapChart.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            //....
            //Enabling tooltip for data points
            tooltip:
            {
                visible: true
            }
        },
        //....
    });
});

{% endhighlight %}

![](User-Interactions_images/tooltip.png) 

###Tooltip Template
HTML elements can be displayed inside the tooltip by using the [`template`](/js/api/ejchart#members:commonseriesoptions-tooltip-template) option. The template option takes the value of the “id” attribute from the HTML element. You can use the **#point.x#** and **#point.y#** as place holders in the HTML element to display the X and Y values of the corresponding data points.

{% highlight js %}

<body>
    <div id="OlapChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <div id="Tooltip" style="display: none;">
        <label id="cc1">In </label>
        <label id="fyvalue">&nbsp;#point.x# </label>
        <label id="cc2">, customer count is</label>
        <label id="ccvalue">&nbsp;#point.y# </label>
    </div>
    <script type="text/javascript">
        $(function()
        {
            $("#OlapChart1").ejOlapChart(
            {
                url: "../wcf/OlapChartService.svc",
                commonSeriesOptions:
                {
                    //....
                    //Enabling tooltip of data points
                    tooltip:
                    {
                        visible: true,
                        template: 'Tooltip'
                    }
                },
                //....
            });
        });
    </script>
</body>

{% endhighlight %}

![](User-Interactions_images/tooltiptemplate.png) 

###Tooltip Customization
By using [`fill`](/js/api/ejchart#members:commonseriesoptions-tooltip-fill) and [`border`](/js/api/ejchart#members:commonseriesoptions-tooltip-border) properties of tooltip, you can customize its background color, border color and border width.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            //....
            tooltip:
            {
                visible: true,
                //Customize tooltip background color and border
                fill: '#FF9933',
                border:
                {
                    width: 1,
                    color: "#993300"
                }
            }
        },
        //....
    });
});

{% endhighlight %}   

![](User-Interactions_images/tooltipcustomization.png) 

###Tooltip with Rounded Corners
The tooltip properties, `rx` and `ry` are used to customize its corner radius.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            //....
            tooltip:
            {
                visible: true,
                //Customize the corner radius of the tooltip rectangle
                rx: "50",
                ry: "50"
            }
        },
        //....
    });
});

{% endhighlight %} 

![](User-Interactions_images/tooltiprouded.png) 

##Zooming and Panning

###Enable Zooming

There are two ways to zoom the Chart:

* When [`zooming.enable`](/js/api/ejchart#members:zooming-enable) option is set to true, you can zoom the Chart by using rubber band selection.
* When [`zooming.enableMouseWheel`](/js/api/ejchart#members:zooming-enablemousewheel) option is set to true, you can zoom the Chart on mouse wheel scrolling.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        //Enable zooming in Chart
        zooming:
        {
            enable: true
        }
        //....
    });
});

{% endhighlight %} 

![](User-Interactions_images/zooming.png) 

After zooming the Chart, a zooming toolbar will appear with options to *zoom, pan and reset*. Selecting the **“Pan”** option will allow to view the Chart and selecting the **“Reset”** option will reset the zoomed Chart.

![](User-Interactions_images/pan.png) 

###Types of Zooming
You can zoom the particular axis like horizontal axis or vertical axis or both axis using [`type`](/js/api/ejchart#members:zooming-type) option in zooming. The default value is “x,y” (indicating both axis).

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        //Enable zooming in Chart
        zooming:
        {
            enable: true,
            //Enable horizontal zooming
            type: 'x'
        }
        //....
    });
});
{% endhighlight %}

##Marker and Crosshair

###Marker Shape Customization
In OlapChart, you can customize the marker [`shape`](/js/api/ejchart#members:series-marker-shape) with different symbols like rectangle, circle, cross, diamond, pentagon, hexagon, star, ellipse, triangle etc.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Line
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++) 
    this.model.series[seriescount].marker.shape = "Triangle";
}

{% endhighlight %}

![](User-Interactions_images/marker.png) 

###Enable Crosshair and Crosshair Label
Crosshair helps you to view the value at mouse position or touch contact point. Crosshair can be enabled by using the [`visible`](/js/api/ejchart#members:crosshair-visible) option in [`crosshair`](/js/api/ejchart#members:crosshair) property. Crosshair label can be enabled by using the **“visible”** option in [`crosshairLabel`](/js/api/ejchart#members:crosshair) property within its corresponding axis.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        //...
        //Initializing Crosshair
        crosshair:
        {
            visible: true
        },
        primaryXAxis:
        {
            //Enable Crosshair Label in X-Axis
            crosshairLabel:
            {
                visible: true
            }
        },
        primaryYAxis:
        {
            //Enable Crosshair Label to Y-Axis 
            crosshairLabel:
            {
                visible: true
            }
        },
    });
});

{% endhighlight %}

![](User-Interactions_images/crosshair.png) 

###Crosshair Line and Label Customization
By using `line` property of crosshair, you can customize its line color and width. Also by using `fill` and `border` properties of crosshair label, you can customize its background color, border color and border width.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        //...
        //Initializing Crosshair
        crosshair:
        {
            visible: true,
            //Customizing the crosshair line
            line:
            {
                color: 'gray',
                width: 2
            }
        },
        primaryXAxis:
        {
            //Enable Crosshair Label in X-Axis 
            crosshairLabel:
            {
                visible: true,
                //Customizing the crosshair label background color and border
                fill: "red",
                border:
                {
                    color: "green",
                    width: 2
                }
            }
        },
        primaryYAxis:
        {
            //Enable Crosshair Label in Y-Axis
            crosshairLabel:
            {
                visible: true
            }
        },
    });
});

{% endhighlight %}

![](User-Interactions_images/crosshairline.png) 

##Trackball

###Enable trackball
Trackball can be enabled by setting both - ['visible'](/js/api/ejchart#members:crosshair-visible) option of the crosshair to true and [`type`](/js/api/ejchart#members:crosshair-type) option of the crosshair to **“trackball”.** The default value of type is **“crosshair”.**

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        //...
        //Initializing Crosshair 
        crosshair:
        {
            visible: true,
            //Change crosshair type to trackball
            type: 'trackball'
        },
    });
});

{% endhighlight %}

![](User-Interactions_images/trackball.png) 

###Trackball Marker and Line Customization
Shape and size of the trackball marker can be customized using the [`shape`](/js/api/ejchart#members:commonseriesoptions-marker-shape) and [`size`](/js/api/ejchart#members:crosshair-marker-size) options of the crosshair marker. Color and width of the trackball line can be customized using the **“line”** option in the crosshair.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        //...
        //Initializing Crosshair
        crosshair:
        {
            visible: true,
            //Change crosshair type to trackball
            type: 'trackball',
            //Customize the trackball line color and width
            line:
            {
                color: '#800000',
                width: 2
            },
            //Customize the trackball marker shape, size and visibility
            marker:
            {
                shape: 'pentagon',
                size:
                {
                    height: 9,
                    width: 9
                },
                visible: true
            }
        },
    });
});

{% endhighlight %} 

![](User-Interactions_images/trackballmarker.png) 

##Highlight
OlapChart provides highlighting support for the series and data points on mouse hover. To enable highlighting, set the **“enable”** property to true in the [`highlightsettings`](/js/api/ejchart#members:series-highlightsettings-enable) option of the series.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++) 
    this.model.series[seriescount].highlightSettings.enable = true
}

{% endhighlight %} 

###Highlight Mode
You can set three different modes for highlighting data points and series by using the [`mode`](/js/api/ejchart#members:series-highlightsettings-mode) property of the [`highlightsettings`](/js/api/ejchart#members:series-highlightsettings).
 
* series
* points
* cluster

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++)
    {
        this.model.series[seriescount].highlightSettings.enable = true;
        this.model.series[seriescount].highlightSettings.mode = "series";
    }
}

{% endhighlight %} 

![](User-Interactions_images/highlightmode.png) 

###Customize the Highlight Styles
To customize the highlighted series, use [`border.color`](/js/api/ejchart#members:series-highlightsettings-border-color), [`border.width`](/js/api/ejchart#members:series-highlightsettings-border-width) and [`opacity`](/js/api/ejchart#members:series-highlightsettings-opacity)
 options in the [`highlightSettings`](/js/api/ejchart#members:series-highlightsettings) property.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++)
    {
        this.model.series[seriescount].highlightSettings.enable = true;
        this.model.series[seriescount].highlightSettings.opacity = "0.5";
        this.model.series[seriescount].highlightSettings.border.width = "1.5";
        this.model.series[seriescount].highlightSettings.border.color = "red";
    }
}

{% endhighlight %} 

![](User-Interactions_images/customizehighlight.png) 

###Patterns to Highlight
OlapChart provides pattern support for highlighting the data by setting an appropriate value to the [`pattern`](/js/api/ejchart#members:series-highlightsettings-pattern) property of the [`highlightSettings`](/js/api/ejchart#members:series-highlightsettings). The different types of highlight patterns are as follows.

* chessboard
* crosshatch
* dots
* packman
* grid
* turquoise
* star
* triangle
* circle
* tile
* horizontalDash
* verticalDash
* rectangle
* box
* verticalStripe
* horizontalStripe
* bubble
* diagonalBackward
* diagonalForward


{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++)
    {
        this.model.series[seriescount].highlightSettings.enable = true;
        this.model.series[seriescount].highlightSettings.pattern = "chessboard";
    }
}

{% endhighlight %} 

![](User-Interactions_images/patternhighlight.png) 

##Selection
OlapChart provides selection support for the series and data points on mouse click. To enable selection, set the **“enable”** property to true in the [`selectionSettings`](/js/api/ejchart#members:series-selectionsettings-enable) option of the series.

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++)
    {
        this.model.series[seriescount].selectionSettings.enable = true;
    }
}

{% endhighlight %}

###Selection Mode

You can set three different selection mode for highlighting the data points and series by using the [`mode`](/js/api/ejchart#members:series-selectionsettings-mode) property of the [`selectionSettings`](/js/api/ejchart#members:series-selectionsettings).

* series
* points
* cluster

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++)
    {
        this.model.series[seriescount].selectionSettings.enable = true;
        this.model.series[seriescount].selectionSettings.mode = "series";
    }
}

{% endhighlight %}

![](User-Interactions_images/selectionmode.png) 

###Customize the Selection Styles
To customize the selection styles, use the [`border.color`](/js/api/ejchart#series-selectionsettings-border-color), [`border.width`](/js/api/ejchart#members:series-selectionsettings-border-width) and [`opacity`](/js/api/ejchart#members:commonseriesoptions-selectionsettings-opacity) options in the [`selectionSettings`](/js/api/ejchart#members:series-selectionsettings).

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++)
    {
        this.model.series[seriescount].selectionSettings.enable = true;
        this.model.series[seriescount].selectionSettings.border.width = "1.5";
        this.model.series[seriescount].selectionSettings.border.color = "red";
    }
}

{% endhighlight %}

![](User-Interactions_images/customizeselection.png) 

###Patterns for Selection
OlapChart provides pattern support for the selecting the data by setting an appropriate value to the [`pattern`](/js/api/ejchart#members:series-selectionsettings-pattern) property of the [`selectionSettings`](/js/api/ejchart#members:series-selectionsettings) option. The different types of selection patterns are as follows.

* chessboard
* crosshatch
* dots
* packman
* grid
* turquoise
* star
* triangle
* circle
* tile
* horizontalDash
* verticalDash
* rectangle
* box
* verticalStripe
* horizontalStripe
* bubble
* diagonalBackward
* diagonalForward

{% highlight js %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        commonSeriesOptions:
        {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        size:
        {
            height: "460px",
            width: "950px"
        },
        seriesRendering: "onSeriesRenders"
    });
});

function onSeriesRenders(args)
{
    for (var seriescount = 0; seriescount < this.model.series.length; seriescount++)
    {
        this.model.series[seriescount].selectionSettings.enable = true;
        this.model.series[seriescount].selectionSettings.pattern = "chessboard";
    }
}

{% endhighlight %}

![](User-Interactions_images/patternselecion.png) 
