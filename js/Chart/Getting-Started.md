---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Chart
documentation: ug
---

# Getting Started

This section explains briefly on how to create a Chart in your application with JavaScript.

## Create your first Chart in JavaScript

This section encompasses on how to configure the **Chart** for your business requirements. You can also pass the required data to default **Chart** and customize it according to your requirements. In this example, you can see how to display the average climate data for Washington, DC during the period 1961 -1990.

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img1.png" %}

### Create a Chart

Getting started with your **Essential JavaScript Chart** is very easy. You can start by creating a simple line **Chart**.

1.Create an `HTML` page and add the following code example.

{% highlight html %}


<!DOCTYPE html>
<html>
<head>
    <!--  jquery script  -->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <!--  jquery localization dependency  -->
    <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"></script>
    <!-- Essential JS UI widget -->
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>
<body>
</body>
</html>



{% endhighlight %}



2.Create a `&lt;div&gt;` tag with an id and set height and width of the **Chart**.

{% highlight html %}


<body>
    <div id="chartcontainer" style="width: 820px; height: 500px;"></div>
</body>


{% endhighlight %}



3.Add a script tag inside the `&lt;Body&gt;` tag and add the following code example.

{% highlight html %}


<body>
    <div id="chartcontainer" style="width: 820px; height: 500px;"></div>
    <script type="text/javascript" language="javascript ">
        $(function () {
            $("#chartcontainer").ejChart();
        });
    </script>
</body>


{% endhighlight %}



The above code example renders a **Chart** with the default `Column series` type and some random values assigned to the column series. 

The following screenshot displays the Chart.

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img2.png" %}

## Add a Chart series

By default, line series is used. To create a **series**, you need to add the following code example to the scripts. For example, the following steps illustrate how to add a column series to the **Chart**.

1. You need to add the name of the series displayed in Chart legend.

2. Then, you need to specify the type of series you want to render using `[type](/js/api/ejchart#seriestypespan-classtype-signature-type-enumenumspan "series.type")` property.

3. You can add x and y `[points](/js/api/ejchart#seriespointsspan-classtype-signature-type-arrayarrayspan "points")` to the series as shown in the following code example.



{% highlight js %}


            $("#chartcontainer").ejChart({
                // ...      
                series: [{
                    name: 'Precipitation',
                    type: 'column',
                    points:
                        [
                             { x: 'Jan', y: 3.03 },
                             { x: 'Feb', y: 2.48 },
                             { x: 'Mar', y: 3.23 },
                             { x: 'Apr', y: 3.15 },
                             { x: 'May', y: 4.13 },
                             { x: 'Jun', y: 3.23 },
                             { x: 'Jul', y: 4.13 },
                             { x: 'Aug', y: 4.88 },
                             { x: 'Sep', y: 3.82 },
                             { x: 'Oct', y: 3.07 },
                             { x: 'Nov', y: 2.83 },
                             { x: 'Dec', y: 2.8 },
                        ],
                }
                ],
                // ...             

            });


{% endhighlight %}



The following screenshot displays a Chart series:

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img3.png" %}

## Add JSON data to the Chart

You can add **JSON** data to the **Chart** using the `[dataSource](/js/api/ejchart#seriesdatasourcespan-classtype-signature-type-objectobjectspan "dataSource")` property in Chart series. Since you need to show the average High and Low temperature along with the Precipitation, you can create a **JSON** data as in the following code example. 

The precipitation data is taken from [http://www.usclimatedata.com/](http://www.usclimatedata.com/)

{% highlight js %}


        //Json data for chart datasource
        window.chartData = [
            { date: 'Jan', high: 42, low: 27, precipitation: 3.03 },
            { date: 'Feb', high: 44, low: 28, precipitation: 2.48 },
            { date: 'Mar', high: 53, low: 35, precipitation: 3.23 },
            { date: 'Apr', high: 64, low: 44, precipitation: 3.15 },
            { date: 'May', high: 75, low: 54, precipitation: 4.13 },
            { date: 'Jun', high: 83, low: 63, precipitation: 3.23 },
       	    { date: 'Jul', high: 87, low: 68, precipitation: 4.13 },
            { date: 'Aug', high: 84, low: 66, precipitation: 4.88 },
            { date: 'Sep', high: 78, low: 59, precipitation: 3.82 },
            { date: 'Oct', high: 67, low: 48, precipitation: 3.07 },
            { date: 'Nov', high: 55, low: 38, precipitation: 2.83 },
            { date: 'Dec', high: 45, low: 29, precipitation: 2.8 }
        ];



{% endhighlight %}



Now, set the datasource and corresponding x and y values to the **Chart** series using `[dataSource](/js/api/ejchart#seriesdatasourcespan-classtype-signature-type-objectobjectspan "dataSource")`, `[xName](/js/api/ejchart#seriesxnamespan-classtype-signature-type-stringstringspan "xName")`, `[yName](/js/api/ejchart#seriesynamespan-classtype-signature-type-stringstringspan "yName")` properties of the `[dataSource](/js/api/ejchart#seriesdatasourcespan-classtype-signature-type-objectobjectspan "dataSource")` as shown in the following code example.

{% highlight js %}


    $(function () {
            $("#chartcontainer").ejChart(
            {
                // ...             
                series: [
                    {
                        name: 'Precipitation',
                        type: 'column',
                        dataSource: window.chartData,
                        xName: "date",
                        yName: "precipitation"
                    },
                    {
                        name: 'Low',
                        type: 'line',
                        dataSource: window.chartData,
                        xName: "date",
                        yName: "low"
                    },
                    {
                        name: 'High',
                        type: 'line',
                        dataSource: window.chartData,
                        xName: "date",
                        yName: "high"
                    },
                ]
                // ...             
            });
     });


{% endhighlight %}



The following screenshot displays the Chart when **JSON** data is added.

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img4.png" %}

## Add Chart Axis of your choice

In the **Chart** when **JSON** is added, the axes are provided explicitly and **ejChart** initializes the right-axis based on the data type. You can also specify the axis type of your choice using `valueType` option and customize the options available in the axes. The following axes types are supported:

* `Category` -   String data can be plotted using `category` axis. Category axis can be initialized only as x-axis.
* `Double` -   Numeric values can be plotted using `double` axis.
* `Datetime` -  DateTime can be plotted using `datetime` axis. This type of axis can be initialized only as x-axis.
* `Logarithmic` -  Numeric values can be plotted using `logarithm` axis.

You can use `[primaryXAxis](/js/api/ejchart#primaryxaxisspan-classtype-signature-type-objectobjectspan "primaryXAxis")` and `[primaryYAxis](/js/api/ejchart#primaryyaxisspan-classtype-signature-type-objectobjectspan "primaryYAxis")` options to initialize the axes. As the data contains string values along x-axis, you can set `[valueType](/js/api/ejchart#primaryxaxisvaluetypespan-classtype-signature-type-enumenumspan "primaryXAxis.valueType")` as `category` for `[primaryXAxis](/js/api/ejchart#primaryxaxisspan-classtype-signature-type-objectobjectspan "primaryXAxis")` and `double` for `[primaryYAxis](/js/api/ejchart#primaryyaxisspan-classtype-signature-type-objectobjectspan "primaryYAxis")`. 

Since the values are in Farenheit for Temperature and Inches for Precipetation, you need to initialize different axis instance for each unit. You can use `[labelFormat](/js/api/ejchart#primaryyaxislabelformatspan-classtype-signature-type-stringstringspan "primaryYAxis.labelFromat")` option to add suffix for axis labels.

In order to add additional axes to the Chart other than `[primaryXAxis](/js/api/ejchart#primaryxaxisspan-classtype-signature-type-objectobjectspan "primaryXAxis")` and `[primaryYAxis](/js/api/ejchart#primaryyaxisspan-classtype-signature-type-objectobjectspan "primaryYAxis")`, you need to initialize `axes` option with collection of axis and set `name` for axis in the axes collection.

The following code example illustrates how to add Chart axis.

{% highlight js %}


    $("#chartcontainer").ejChart(
    {
        // ...
            primaryXAxis: {
                valueType:"category",
            },
            primaryYAxis:{
                valueType: "double",
                labelFormat: "{value}°F",
                range:{min:0, max:120,interval:20}
            },
            axes:[
            {
                orientation:'Vertical',
                opposedPosition: true,
                name: 'Precipitation',
                range:{min:0,max:6,interval:1},
                labelFormat: '{value} inch',
            },
            ]
        // ...
    });


{% endhighlight %}

## Assign the axis to the respective series

To assign the axis to the respective series, you can set `[yAxisName](/js/api/ejchart#seriesyaxisnamespan-classtype-signature-type-stringstringspan "series.yAxisName")` property of the `[series](/js/api/ejchart#seriesspan-classtype-signature-type-arrayarrayspan "series")`. In the following code example, `[yAxisName](/js/api/ejchart#seriesyaxisnamespan-classtype-signature-type-stringstringspan "series.yAxisName")` of Column series is set to “Precipitation”. This is the name set to the axis in the above code example.

{% highlight js %}

    $(function () {
        $("#chartcontainer").ejChart(
        {
	       // ...             
            series: [
            {
                name: 'Precipitation',
                type: 'column',
                dataSource: window.chartData,
                xName: "date",
                yName: "precipitation",
                yAxisName:'Precipitation',

            },
            {
                name: 'Low',
                type: 'line',
                dataSource: window.chartData,
                xName: "date",
                yName: "low"
            },
            {
                name: 'High',
                type: 'line',
                dataSource: window.chartData,
                xName: "date",
                yName: "high"
            },
            ]
	       // ...             
        });
    });


{% endhighlight %}



The following screenshot displays a Chart with the desired output.

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img5.png" %}

## Add Data Labels

Data Labels display the series points in **Chart**. To display the data labels, you need to enable the `[visible](/js/api/ejchart#seriesmarkerdatalabelvisiblespan-classtype-signature-type-booleanbooleanspan "dataLabel.visible")` property of `[dataLabel](/js/api/ejchart#seriesmarkerdatalabelspan-classtype-signature-type-objectobjectspan "dataLabel")` in the `[marker](/js/api/ejchart#seriesmarkerspan-classtype-signature-type-objectobjectspan "series.marker")` of specific series. By default, it displays the Y-value with label format provided in axis (For example: 4.88 inch ). The following code example shows how to add Data Labels.

{% highlight js %}

 
        $("#chartcontainer").ejChart({
            // ...             
            series: [{
                name: 'Precipitation',
                type: 'column',
                dataSource: window.chartData,
                xName: "date",
                yName: "precipitation",
                yAxisName: 'Precipitation',
                marker: {
                    dataLabel: {
                        visible: true,
                        textPosition: "top",
                        fill: "#FF7777",
                        verticalTextAlignment: "top",
                        offset: 20,
                        shape: "rectangle",
                        font: { color: "white" }
                    }
                }
            }
            // ...  
            ]
        });


{% endhighlight %}



The following screenshot displays a Chart when data labels are enabled.

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img6.png" %}

## Enable Tooltip

To display the `[tooltip](/js/api/ejchart#seriestooltipspan-classtype-signature-type-objectobjectspan "tooltip")` of **Chart** series, you can enable the `[visible](/js/api/ejchart#seriestooltipvisiblespan-classtype-signature-type-booleanbooleanspan "tooltip.visible")` property of `[tooltip](/js/api/ejchart#seriestooltipspan-classtype-signature-type-objectobjectspan "tooltip")` in the specific series. By default, it displays `X` and `Y` value of points when the mouse is hovered over the points. The following code example shows how to enable a Tooltip.

{% highlight js %}


         $("#chartcontainer").ejChart({
            // ...             
            series: [
            {
                name: 'Precipitation',
                type: 'column',
                dataSource: window.chartData,
                xName: "date",
                yName: "precipitation",
                yAxisName: 'Precipitation',
                marker: {
                    dataLabel: {
                        visible: true,
                        textPosition: "top",
                        fill: "#FF7777",
                        verticalTextAlignment: "top",
                        offset: 20,
                        shape: "rectangle",
                        font: { color: "white" },

                    }
                },
                tooltip: { visible: true },
            }

            // ...  
            ]
        });


{% endhighlight %}



The following screenshot displays a Chart when tooltip is enabled.

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img7.png" %}

