---
layout: post
title: Getting-Started
description: getting started
platform: js
control: BulletGraph	
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **BulletGraph** in your application with **JavaScript**.

## Create your first BulletGraph in JavaScript

This section encompasses the details on how to configure the **BulletGraph** control in applications. It also helps you to learn how to pass the required data to it and to customize its various options according to their needs. 

In the following screenshot, a **BulletGraph** is used to compare the actual monsoon rainfall received in a state versus its forecasted values for the years ranging from 1988 to 2013. 

{% include image.html url="/js/BulletGraph/Getting-Started_images/Getting-Started_img1.png" Caption="BulletGraph"%}

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
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
</head>
<body>
</body>
</html>

{% endhighlight %}



2.Now add a &lt;div&gt; elementthat acts as a container for **ejBulletGraph** widget.

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
       “$("#Bullet").ejBulletGraph();
    });
</script>
</head>



{% endhighlight %}



4.Run the above code and the **BulletGraph** is displayed. In order to customize the measure bars within the **BulletGraph**, either local or remote data should be passed to it.

{% include image.html url="/js/BulletGraph/Getting-Started_images/Getting-Started_img2.png" Caption="BulletGraph"%}

**Provide Required Data**

You can customize the values of feature and comparative measure bars in a **BulletGraph**, either locally or remotely. The category data is optional, and is used to display label values in parallel to the measure bars. 

Assign the data in **localData** variable to the **dataSource** property of **BulletGraph** as shown in the following code example.

{% highlight js %}


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



Once the **dataSource** property is assigned with the required values, you canbind the variable names used in the **JSON** data to the corresponding fields of the **BulletGraph** as shown in the following code sample.

{% highlight js %}


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

You can plot more number of measure bars within the **BulletGraph**, the height and width of the control should be increased to locate all the measure bars within the graph.The **qualitativeRangesize** and **quantitativeScaleLength** property needs to be set accordingly as shown in the following code example.

By default, the **BulletGraph** is rendered in the Horizontal orientation with its flow direction set to **Forward.** In this example,to achieve the desired output, horizontal orientation should bechanged to **Vertical** orientation with the flow direction set to **Backward**.

**Minimum**, **maximum** and **interval** values for the **quantitativeScale** of the **bulletgraph** should be set, as shown in the following code example. The ticks and labels within the scale also need to be positioned.

{% highlight js %}


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



{% include image.html url="/js/BulletGraph/Getting-Started_images/Getting-Started_img3.png" Caption="BulletGraph"%}

As you can see in the image above, the bullet graph without any ranges is displayed in thebackground. The steps to add the **qualitativeRanges** are described in the next section.

**Add Qualitative Ranges**

By default, 3 ranges are displayed in the **BulletGraph** control duringthe initial rendering of the control with its default values. In order to customize it, youneed to set appropriate values for the **rangeEnd** and its **rangeStroke** properties.  Any number of **qualitativeRanges** can be added to the control. 

{% highlight js %}


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

{% include image.html url="/js/BulletGraph/Getting-Started_images/Getting-Started_img4.png" Caption="BulletGraph"%}

**Ticks and Measure Bars Customization**

You have to dothe following code changes in the quantitative scalein order to customize the tick size, the colors of the feature bar and comparative measure symbols. 

{% highlight js %}


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

{% include image.html url="/js/BulletGraph/Getting-Started_images/Getting-Started_img5.png" Caption="BulletGraph"%}

**Add Caption and Subtitle**

You can display an appropriate Caption and Subtitle in the **BulletGraph** by adding the following code example.

{% highlight js %}


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

{% include image.html url="/js/BulletGraph/Getting-Started_images/Getting-Started_img6.png" Caption="BulletGraph"%}

**Show Tooltip**

You can use a Tooltip in your application to display anyinformation. In this example, a tooltip is used to show the values (in millimetre) of forecasted rainfall, actual rainfall received in (mm) and also the appropriate year. The tooltip is enabled by setting the **visible** property in tooltip to **True.** Also, in order to set the template tooltip, you can pass the template id to it as shown in the following code example.

{% highlight js %}


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

{% include image.html url="/js/BulletGraph/Getting-Started_images/Getting-Started_img7.png" Caption="BulletGraph"%}

