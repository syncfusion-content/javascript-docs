---
layout: post
title: Getting-Started
description: getting started
platform: js
control: BulletGraph	
documentation: ug
api: /api/js/ejbulletgraph
---

# Getting Started

This section explains briefly about how to create a **BulletGraph** in your application with **JavaScript**.

## Create your first BulletGraph in JavaScript

This section encompasses the details on how to configure the **BulletGraph** control in applications. It also helps you to learn how to pass the required data to it and to customize its various options according to their needs. 

In the following screenshot, a **BulletGraph** is used to compare the actual monsoon rainfall received in a state versus its forecasted values for the years ranging from 1988 to 2013. 

![](/js/BulletGraph/Getting-Started_images/Getting-Started_img1.png) 

**Create a BulletGraph**

1.Create an **HTML** file and add references to the required libraries.

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



2.Now add a &lt;div&gt; element that acts as a container for **ejBulletGraph** widget.

{% highlight html %}


<html>
<body>
<div id="Bullet"></div>
</body>
</html>


{% endhighlight %}



3.Once the container is added, create the **ejBulletGraph** widget as follows.

{% highlight html %}



<head>
<!-- … -->
<script type="text/javascript">
    $(function () {
       $("#Bullet").ejBulletGraph();
    });
</script>
</head>



{% endhighlight %}



4.Run the above code and the **BulletGraph** is displayed. In order to customize the measure bars within the **BulletGraph**, either local or remote data should be passed to it.

![](/js/BulletGraph/Getting-Started_images/Getting-Started_img2.png) 

**Provide Required Data**

You can customize the values of feature and comparative measure bars in a **BulletGraph**, either locally or remotely. The [`category`](../api/ejbulletgraph#members:quantitativescalesettings-fields-category) data is optional, and is used to display label values in parallel to the measure bars. 

Assign the data in **localData** variable to the [`dataSource`](../api/ejbulletgraph#members:quantitativescalesettings-fields-datasource) property of **BulletGraph** as shown in the following code example.

{% highlight javascript %}


    var localData = [
                {
                    value: 90, comparativeMeasureValue: 100,
                    category: 2013
                },
                {
                    value: 93, comparativeMeasureValue: 99,
                    category: 2012
                },
                {
                    value: 98, comparativeMeasureValue: 96,
                    category: 2011
                },
                {
                    value: 102, comparativeMeasureValue: 98,
                    category: 2010
                },
                {
                    value: 77, comparativeMeasureValue: 96,
                    category: 2009
                },
                {
                    value: 99, comparativeMeasureValue: 99,
                    category: 2008
                },
                {
                    value: 106, comparativeMeasureValue: 94,
                    category: 2007
                },
                {
                    value: 105, comparativeMeasureValue: 95,
                    category: 2006
                },
                {
                    value: 98, comparativeMeasureValue: 98,
                    category: 2005
                },
                {
                    value: 87, comparativeMeasureValue: 100,
                    category: 2004
                },
                {
                    value: 105, comparativeMeasureValue: 98,
                    category: 2003
                },
                {
                    value: 84, comparativeMeasureValue: 101,
                    category: 2002
                },
                {
                    value: 93, comparativeMeasureValue: 98,
                    category: 2001
                },
                {
                    value: 90, comparativeMeasureValue: 96,
                    category: 2000
                },
                {
                    value: 95, comparativeMeasureValue: 107,
                    category: 1999
                },
                {
                    value: 104, comparativeMeasureValue: 98,
                    category: 1998
                },
                {
                    value: 102, comparativeMeasureValue: 92,
                    category: 1997
                },
                {
                    value: 103, comparativeMeasureValue: 98,
                    category: 1996
                },
                {
                    value: 100, comparativeMeasureValue: 96,
                    category: 1995
                },
                {
                    value: 110, comparativeMeasureValue: 92,
                    category: 1994
                },
                {
                    value: 100, comparativeMeasureValue: 103,
                    category: 1993
                },
                {
                    value: 94, comparativeMeasureValue: 93,
                    category: 1992
                },
                {
                    value: 91, comparativeMeasureValue: 95,
                    category: 1991
                },
                {
                    value: 107, comparativeMeasureValue: 103,
                    category: 1990
                },
                {
                    value: 101, comparativeMeasureValue: 102,
                    category: 1989
                },
                {
                    value: 119, comparativeMeasureValue: 112,
                    category: 1988
                }];
                
    $(function () {
        $("#Bullet").ejBulletGraph({
        fields: {
            dataSource: localData
            }
        });
     });




{% endhighlight %}



Once the **dataSource** property is assigned with the required values, you can bind the variable names used in the **JSON** data to the corresponding fields of the **BulletGraph** such as [`category`](../api/ejbulletgraph#members:quantitativescalesettings-fields-category), [`feature measures`](../api/ejbulletgraph#members:quantitativescalesettings-fields-featuremeasures), [`comparative measure`](../api/ejbulletgraph#members:quantitativescalesettings-fields-comparativemeasure) shown in below code example.

{% highlight javascript %}


    $(function () {
    $("#Bullet").ejBulletGraph({
        fields: {
                dataSource: localData, category: "category",
                featureMeasures: "value",
                comparativeMeasure: "comparativeMeasureValue"
            }
        });
     });


{% endhighlight %}

**Set Default and Scale Values**

You can plot more number of measure bars within the **BulletGraph**, the [`height`](../api/ejbulletgraph#members:height) and [`width`](../api/ejbulletgraph#members:width) of the control should be increased to locate all the measure bars within the graph.The [`qualitative range size`](../api/ejbulletgraph#members:qualitativerangesize) and [`quantitative scale length`](../api/ejbulletgraph#members:quantitativescalelength) property needs to be set accordingly as shown in the following code example.

By default, the **BulletGraph** is rendered in the Horizontal [`orientation`](../api/ejbulletgraph#members:orientation) with its [`flow direction`](../api/ejbulletgraph#members:flowdirection) set to **Forward.** In this example,to achieve the desired output, horizontal orientation should be changed to **Vertical** orientation with the flow direction set to **Backward**.

[`Minimum`](../api/ejbulletgraph#members:   -minimum), [`maximum`](../api/ejbulletgraph#members:quantitativescalesettings-maximum) and [`interval`](../api/ejbulletgraph#members:quantitativescalesettings-interval) values for the [`quantitative scale`](../api/ejbulletgraph#members:quantitativescalesettings) of the **bullet graph** should be set, as shown in the following code example. The [`ticks`](../api/ejbulletgraph#members:quantitativescalesettings-tickposition) and [`labels`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-position) within the scale also need to be positioned.

{% highlight javascript %}


    $(function () {
    $("#Bullet").ejBulletGraph({
            width:850,
            height: 540,
            qualitativeRangeSize: 800,
            quantitativeScaleLength: 425, 
            orientation: ej.datavisualization.BulletGraph.orientation.Vertical,
            flowDirection: ej.datavisualization.BulletGraph.flowDirection.Backward,
            quantitativeScaleSettings: {
                minimum: 70,
                maximum: 130,
                interval: 10,
                tickPosition: ej.datavisualization.BulletGraph.tickPosition.Above,
                labelSettings: {
                    position: ej.datavisualization.BulletGraph.labelPosition.Above
                }
            },
            fields: {
                dataSource: localData, category: "category",
                featureMeasures: "value",
                comparativeMeasure: "comparativeMeasureValue"
            }
        });
     });


{% endhighlight %}



![](/js/BulletGraph/Getting-Started_images/Getting-Started_img3.png) 

As you can see in the image above, the bullet graph without any ranges is displayed in the background. The steps to add the [`qualitativeRanges`](../api/ejbulletgraph#members:qualitativeranges) are described in the next section.

**Add Qualitative Ranges**

By default, 3 ranges are displayed in the **BulletGraph** control during the initial rendering of the control with its default values. In order to customize it, you need to set appropriate values for the [`range end`](../api/ejbulletgraph#members:qualitativeranges-rangeend),[`range opacity`](../api/ejbulletgraph#members:qualitativeranges-rangeopacity) and its [`rangeStroke`](../api/ejbulletgraph#members:qualitativeranges:rangestroke) properties.  Any number of [`qualitative ranges`](../api/ejbulletgraph#members:qualitativeranges) can be added to the control. 

{% highlight javascript %}


    $(function () {
    $("#Bullet").ejBulletGraph({
            width:850,
            height: 540,
            qualitativeRangeSize: 800,
            quantitativeScaleLength: 425, 
            orientation: ej.datavisualization.BulletGraph.orientation.Vertical,
            flowDirection: ej.datavisualization.BulletGraph.flowDirection.Backward,
            quantitativeScaleSettings: {
                minimum: 70,
                maximum: 130,
                interval: 10,
                tickPosition: ej.datavisualization.BulletGraph.tickPosition.Above,
                labelSettings: {
                    position: ej.datavisualization.BulletGraph.labelPosition.Above
                }
            },
            fields: {
                dataSource: localData, category: "category",
                featureMeasures: "value",
                comparativeMeasure: "comparativeMeasureValue"
            },
            qualitativeRanges: [{
                rangeEnd: 90
            }, 
            {
                rangeEnd: 110
            },
            {
                rangeEnd: 130, rangeStroke: "#CDC9C9"
            }]

        });
     });



{% endhighlight %}



After adding **qualitativeRanges** to the **BulletGraph**, the control will be rendered as follows.

![](/js/BulletGraph/Getting-Started_images/Getting-Started_img4.png) 

**Ticks and Measure Bars Customization**

You have to do the following code changes in the quantitative scale in order to customize the tick size, the colors of the [`feature bar`](../api/ejbulletgraph#members:quantitativescalesettings-featuredmeasuresettings) and [`comparative measure symbols`](../api/ejbulletgraph#members:quantitativescalesettings-comparativemeasuresettings). 

{% highlight javascript %}


    $(function () {
    $("#Bullet").ejBulletGraph({
            width:850,
            height: 540,
            qualitativeRangeSize: 800,
            quantitativeScaleLength: 425, 
            orientation: ej.datavisualization.BulletGraph.orientation.Vertical,
            flowDirection: ej.datavisualization.BulletGraph.flowDirection.Backward,
            quantitativeScaleSettings: {
                minimum: 70,
                maximum: 130,
                interval: 10,
                tickPosition: ej.datavisualization.BulletGraph.tickPosition.Above,
                labelSettings: {
                    position: ej.datavisualization.BulletGraph.labelPosition.Above
                },

            majorTickSettings:{width:1, size:7},
            minorTickSettings:{width:1},
            comparativeMeasureSettings:{stroke:"#507786"},
            featuredMeasureSettings:{stroke: "#169DD8"},

            },
            fields: {
                dataSource: localData, category: "category",
                featureMeasures: "value",
                comparativeMeasure: "comparativeMeasureValue"
            },
            qualitativeRanges: [{
                rangeEnd: 90
            }, {
                rangeEnd: 110
            }, {
                rangeEnd: 130, rangeStroke: "#CDC9C9"
            }]
        });
     });




{% endhighlight %}



When customization of ticks and measure bars is done, **BulletGraph** looks as follows

![](/js/BulletGraph/Getting-Started_images/Getting-Started_img5.png) 

**Add Caption and Subtitle**

You can display an appropriate [`Caption`](../api/ejbulletgraph#members:captionsettings) and [`Subtitle`](../api/ejbulletgraph#members:captionsettings-subtitle) in the **BulletGraph** by adding the following code example.

{% highlight javascript %}


    $(function () {
    $("#Bullet").ejBulletGraph({
            width:850,
            height: 540,
            qualitativeRangeSize: 800,
            quantitativeScaleLength: 425, 
            orientation: ej.datavisualization.BulletGraph.orientation.Vertical,
            flowDirection: ej.datavisualization.BulletGraph.flowDirection.Backward,
            quantitativeScaleSettings: {
                minimum: 70,
                maximum: 130,
                interval: 10,
                tickPosition: ej.datavisualization.BulletGraph.tickPosition.Above,
                labelSettings: {
                    position: ej.datavisualization.BulletGraph.labelPosition.Above
                },

                majorTickSettings:{width:1, size:7},
                minorTickSettings:{width:1},
                comparativeMeasureSettings:{stroke:"#507786"},
                featuredMeasureSettings:{stroke: "#169DD8"},

            },
            fields: {
                dataSource: localData, category: "category",
                featureMeasures: "value",
                comparativeMeasure: "comparativeMeasureValue"
            },
            qualitativeRanges: [{
                rangeEnd: 90
            }, {
                rangeEnd: 110
            }, {
                rangeEnd: 130, rangeStroke: "#CDC9C9"
            }],
            captionSettings: {
                textAngle: 90,
                location: { x: 470, y: 270 }, 
                text: "Monsoon Rainfall - Actual vs Forecast", 
                font: { fontFamily: 'Segoe UI', size: '20px', 
                        fontWeight: 'regular', opacity: 1 }, 
                subTitle: {
                    textAngle: 0,
                    text: "Rainfall (mm)", location: { x: 180, y: 4 }, 
                    font: { fontFamily: 'Segoe UI', size: '14px',
                    fontWeight: 'regular', opacity: 1} 
                }
            }
        });
     });


{% endhighlight %}



The following screenshot displays a **BulletGraph** in the caption and title in the **BulletGraph**.

![](/js/BulletGraph/Getting-Started_images/Getting-Started_img6.png) 

**Show Tooltip**

You can use a [`Tooltip`](../api/ejbulletgraph#members:tooltipsettings) in your application to display any information. In this example, a tooltip is used to show the values (in millimeter) of forecasted rainfall, actual rainfall received in (mm) and also the appropriate year. The tooltip is enabled by setting the [`visible`](../api/ejbulletgraph#members:tooltipsettings-visible) property in tooltip to **true.** Also, in order to set the [`template tooltip`](../api/ejbulletgraph#members:tooltipsettings-template), you can pass the template id to it as shown in the following code example.

{% highlight javascript %}


    $(function () {
    $("#Bullet").ejBulletGraph({
            width:850,
            height: 540, 
            tooltipSettings:{visible:true, template: **: "Tooltip"**}
            qualitativeRangeSize: 800,
            quantitativeScaleLength: 425, 
            orientation: ej.datavisualization.BulletGraph.orientation.Vertical,
            flowDirection: ej.datavisualization.BulletGraph.flowDirection.Backward,                
            quantitativeScaleSettings: {
                minimum: 70,
                maximum: 130,
                interval: 10,
                tickPosition: ej.datavisualization.BulletGraph.tickPosition.Above,
                labelSettings: {
                    position: ej.datavisualization.BulletGraph.labelPosition.Above
                },


            majorTickSettings:{width:1, size:7},
            minorTickSettings:{width:1},
            comparativeMeasureSettings:{stroke:"#507786"},
            featuredMeasureSettings:{stroke: "#169DD8"},

            },
            fields: {
                dataSource: localData, category: "category",
                featureMeasures: "value",
                comparativeMeasure: "comparativeMeasureValue"
            },
            qualitativeRanges: [{
                rangeEnd: 90
            }, {
                rangeEnd: 110
            }, {
                rangeEnd: 130, rangeStroke: "#CDC9C9"
            }],
            captionSettings: {
                textAngle: 90,
                location: { x: 470, y: 270 }, 
                text: "Monsoon Rainfall - Actual vs Forecast", 
                font: { fontFamily: 'Segoe UI', size: '20px', 
                        fontWeight: 'regular', opacity: 1 }, 
                subTitle: {
                    textAngle: 0,
                    text: "Rainfall (mm)", location: { x: 180, y: 4 }, 
                    font: { fontFamily: 'Segoe UI', size: '14px', 
                    fontWeight: 'regular', opacity: 1} 
                }
            }
        });
     });
     
{% endhighlight %}  

**Template content**

{% highlight html %}


<div id="Tooltip" style="display:none; width:125px;padding-top: 10px;padding-bottom:10px">
<div align="center" style="font-weight:bold">
           Rainfall 
</div>
<table>
<tr><td>Actual</td>
<td>: {{:currentValue}}mm</td></tr>
<tr><td>Forecast</td>
<td>: {{:targetValue}}mm</td></tr>
<tr><td>Year</td>
<td>: {{:category}}</td></tr>
</table>
</div>


{% endhighlight %}



By using the customization options discussed in this section, the **BulletGraph** is rendered as displayed on the following screenshot.

![](/js/BulletGraph/Getting-Started_images/Getting-Started_img7.png) 

