---
layout: post
title: Axis
description: axis
platform: js
control: Chart
documentation: ug
---

# Axis

**Charts** typically have two axes that are used to measure and categorize data: a vertical (y) axis, and a horizontal (x) axis.

Vertical axis always uses numerical or logarithmic scale. Horizontal(x) axis supports the following types of scale:

* Category
* Numeric
* DateTime
* Logarithmic

## Category Axis

Category axis displays text labels instead of numbers. To use categorical axis, you can set **valueType** property of the axis to **category**. Default value of **valueType** is **double**.

{% highlight js %}

$("#chartcontainer").ejChart({
    primaryXAxis: {

        //Use categorical scale in primary X axis
        valueType: 'category',         

        //  ...         
    },
    //  ...
});


{% endhighlight %}



{% include image.html url="/js/Chart/Axis_images/axis_img1.png" Caption="Chart with category axis"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/column) here to view our online demo sample that uses Category axis.


### Placing labels on ticks

Labels in category axis can be placed on the ticks by setting **labelPlacement** property of axis to **onticks**. Default value of **labelPlacement** property is **betweenticks** i.e. labels will be placed between the ticks by default.

{% highlight js %}

$("#chartcontainer").ejChart({
    primaryXAxis: {

        //Placing X-axis labels on the ticks
        labelPlacement: 'onticks',         

        //  ...        
    },
    //  ...
});


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img2.png" Caption="Category axis labels on ticks"%}


### Displaying labels after a fixed interval

To display labels after a fixed interval n, you can set **interval** property of axis range as **n**. Default value of interval is 1 i.e. all the labels will be displayed by default.

{% highlight js %}

$("#chartcontainer").ejChart({
    primaryXAxis: {

        //Displaying labels after 2 intervals
        range: { interval: 2 },                

        //  ...        
    },
    //  ...
});


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img3.png" Caption="Change category axis labels fixed interval"%}


## Numeric Axis 

Numeric axis uses numerical scale and displays numbers as labels. To use numeric axis, you can set the **valueType** property of axis to **double**. 

{% highlight js %}

$("#chartcontainer").ejChart({
    // ...             
    primaryYAxis: {
        //Use numerical scale in primary Y axis
        valueType: 'double',        
        //  ...         
    },
    // ...             
});


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img4.png" Caption="Numeric axis"%}


### Customizing numeric range

To customize the range of an axis, you can use the **range** property of axis which has options to set the *minimum*, *maximum* and *interval* values. By default, nice range will be calculated automatically based on the provided data.


{% highlight js %}

$("#chartcontainer").ejChart({
    // ...             
    primaryYAxis: {

        //Customizing Y-axis range
        range: { min: 0, max: 50 },         

        //  ...       
    },
    // ...             
});


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img5.png" Caption="Customizing numeric range"%}


#### Customizing numeric interval

Axis interval can be customized using the **interval** property of axis range. By default, nice interval will be calculated based on the minimum and maximum value of the provided data.

{% highlight js %}

$("#chartcontainer").ejChart({
    // ...             
    primaryYAxis: {
              
        //Customizing Y-axis interval
        range: { interval: 5 },         

        //  ...         
    },

    // ...             
});


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img6.png" Caption="Customizing numeric interval"%}

### Apply padding to the range

Padding can be applied to the minimum and maximum extremes of the axis range by using **rangePadding** property. Numeric axis supports the following types of padding

* None
* Round
* Additional
* Normal

**None**

When the value of **rangePadding** property is **none**, padding will not be applied to the axis. This is also the default value of rangePadding. 

{% highlight js %}

        $("#chartcontainer").ejChart({
              // ...             
               primaryYAxis: {
               
                //Applying none as range padding
                rangePadding: 'none',       

                //  ...         
            },

            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img7.png" Caption="Chart’s Y-axis with RangePadding set to None"%}

#### Round

When the value of **rangePadding** property is **round**, axis range will be rounded to the nearest possible value divided by the interval.

{% highlight js %}

        $("#chartcontainer").ejChart({
              // ...             
               primaryYAxis: {
               
                //Applying round as range padding
                rangePadding: 'round',       

                //  ...         
            },

            // ...             
        });


{% endhighlight %}

**Chart before rounding axis range**

{% include image.html url="/js/Chart/Axis_images/axis_img8.png" Caption="Chart before rounding axis range" %}


**Chart after rounding axis range**

{% include image.html url="/js/Chart/Axis_images/axis_img9.png" Caption="Chart after rounding axis range" %}


**Additional**

When the value of **rangePadding** property is **additional**, axis range will be rounded and an interval of the axis will be added as padding to the minimum and maximum values of the range.

{% highlight js %}

        $("#chartcontainer").ejChart({
              // ...             
               primaryYAxis: {
               
                //Applying additional range padding
                rangePadding: 'additional',      

                //  ...         
            },

            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img10.png" Caption="Chart’s Y-axis with RangePadding set to Additional"%}


**Normal**

When the value of **rangePadding** property is **normal**, padding will be applied to the axis based on range calculation.

{% highlight js %}

        $("#chartcontainer").ejChart({
              // ...             
               primaryYAxis: {
               
                //Applying normal range padding
                rangePadding: 'normal',      

                //  ...         
            },

            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img11.png" Caption="Chart’s Y-axis with RangePadding set to Normal"%}

## DateTime Axis

Date time axis uses date time scale and displays date time values as axis labels in specified format. To use date time axis, you can set the **valueType** property of axis to **datetime**.

{% highlight js %}

        $("#chartcontainer").ejChart({
              // ...             
            primaryXAxis: {

                //Use date time scale in primary X axis
                valueType: 'datetime',         

                //  ...         
            },
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img12.png" Caption="DateTime axis"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/datetimeaxis) here to view our online demo sample for date time axis.

 
### Customizing date time range
 
 Axis range can be customized using the **range** property which has options to set the *minimum*, *maximum* and *interval* values. By default, nice range will be calculated automatically based on the provided data.
 
 {% highlight js %}

        $("#chartcontainer").ejChart({
              // ...             
            primaryXAxis: {

                //Customizing X-axis date time range
                range: { 
                    min: new Date(2000, 6, 1), 
                    max: new Date(2010, 6, 1)
                },         

                //  ...         
            },
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img13.png" Caption="DateTime axis range"%}

### Date time intervals

Date time intervals can be customized using **interval** and **intervalType** properties of the axis. For example, setting **interval** as **2** and **intervalType** as **years** will consider 2 years as interval.

Essential Chart supports the following types of interval for date time axis.

* Days
* Hours
* Milliseconds
* Minutes
* Months
* Seconds
* Years

{% highlight js %}

        $("#chartcontainer").ejChart({
            primaryXAxis: {

                //Customizing X-axis date time range
                range: { 
                    interval: 2,
                },         

                 intervalType: 'years',

                //  ...         
            },
            //  ...
     });

{% endhighlight %}


{% include image.html url="/js/Chart/Axis_images/axis_img14.png" Caption="DateTime Axis Interval"%}


### Apply padding to the range

Padding can be applied to the minimum and maximum extremes of the range by using **rangePadding** property. Date time axis supports the following types of padding

* None
* Round
* Aditional

**None**

When the value of **rangePadding** property is **none**, padding will not be applied to the axis. This is also the default value of **rangePadding**. 

{% highlight js %}

     $("#chartcontainer").ejChart({
            primaryXAxis: {

                //Applying none as range padding
                rangePadding: 'none',
                //  ...       
            },
            //  ...
     });

{% endhighlight %} 

{% include image.html url="/js/Chart/Axis_images/axis_img15.png" Caption="Chart’s X-axis with RangePadding set to None"%}

**Round**

When the value of **rangePadding** property is **round**, axis range will be rounded to the nearest possible date time value.

{% highlight js %}

     $("#chartcontainer").ejChart({
            primaryXAxis: {

                //Applying round as range padding
                rangePadding: 'round',
                //  ...       
            },
            //  ...
     });

{% endhighlight %} 

**Chart before rounding axis range**

{% include image.html url="/js/Chart/Axis_images/axis_img16.png" Caption="Chart before rounding axis range"%}

**Chart after rounding axis range**

{% include image.html url="/js/Chart/Axis_images/axis_img17.png" Caption="Chart after rounding axis range"%}

**Additional** 

When the value of **rangePadding** property is **additional**, range will be rounded and date time interval of the axis will be added as padding to the minimum and maximum extremes of the range.

{% highlight js %}

     $("#chartcontainer").ejChart({
            primaryXAxis: {

                //Applying additional as range padding
                rangePadding: 'additional',
                //  ...       
            },
            //  ...
     });

{% endhighlight %} 

{% include image.html url="/js/Chart/Axis_images/axis_img18.png" Caption="Chart’s x-axis with RangePadding set to Additional"%}

## Logarithmic Axis

Logarithmic axis uses logarithmic scale and it is very useful in visualizing when data has values with both lower order of magnitude **(eg: 10<sup>-6</sup>)** and higher order of magnitude **(eg: 10<sup>6</sup>)**. To use logarithmic axis, you can set the **valueType** property of axis to **logarithmic**.  

{% highlight js %}

      $("#chartcontainer").ejChart({
            primaryXAxis: {

                //Use logarithmic scale in primary X axis
                valueType: 'logarithmic',         

                //  ...         
            },
            //  ...
      });


{% endhighlight %}


{% include image.html url="/js/Chart/Axis_images/axis_img19.png" Caption="Chart with Logarthimic Axis"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/logaxis) here to view our online demo sample link for logarithmic axis.

### Customizing Logarithmic range

Logarithmic range can be customized using the **range** property of axis which provide options to change the *minimum*, *maximum* and *interval* values. By default, nice range will be calculated automatically based on the provided data.

{% highlight js %}

     $("#chartcontainer").ejChart({
            primaryYAxis: {

                //Customizing logarithmic range
                range: { min: 1, max: 5 },         

                //  ...         
            },
            //  ...
      });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img20.png" Caption="Change logarthimic axis range"%}

### Logarithmic base

Logarithmic base can be customized using the **logBase** property of axis. Default value of **logBase** is **10**.

{% highlight js %}

     $("#chartcontainer").ejChart({
           primaryYAxis: {

                //Customizing logarithmic base
                logBase: 2,         

                //  ...         
            },
            //  ...
      });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img21.png" Caption="Logarthimic axis logbase"%}


### Logarithmic interval

Logarithmic axis interval can be customized using the **interval** property of axis. If logarithmic base is 10 and logarithmic interval is 2, then axis labels will be placed at an interval of 10<sup>2</sup>. Default value of interval is 1. 

{% highlight js %}

     $("#chartcontainer").ejChart({
           primaryYAxis: {

                //Customizing logarithmic interval
                range: { interval: 2 },              

                //  ...         
            },
            //  ...
      });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img22.png" Caption="Logarthimic axis interval"%}        

## Label Format

### Formatting numeric labels

Numeric labels can be formatted using the **labelFormat** property. Numeric values can be formatted with n (number with decimal points), c (currency) and p (percentage) commands.

{% highlight js %}

     $("#chartcontainer").ejChart({
     
           primaryXAxis: {

                //Applying currency format to axis labels
                labelFormat: 'c',
                //  ...         
            },
            
            //  ...
      });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img23.png" Caption="Formatting numeric labels"%}

The following table describes the result of applying some commonly used label formats on numeric values. 
 
<table>
<tr>
<td><b>Label Value</b></td>
<td><b>Label Format property value</b></td>
<td><b>Result </b></td>
<td><b>Description </b></td>
</tr>        
<tr>
<td>1000</td>
<td>n1</td>
<td>1000.0</td>
<td>Number will be rounded to 1 decimal place</td>
</tr> 
<tr>
<td>1000</td>
<td>n2</td>
<td>1000.00</td>
<td>Number will be rounded to 2 decimal place</td>
</tr> 
<tr>
<td>1000</td>
<td>n3</td>
<td>1000.000</td>
<td>Number will be rounded to 3 decimal place</td>
</tr>
<tr>
<td>0.01</td>
<td>p1</td>
<td>1.0%</td>
<td>Number will be converted to percentage with 1 decimal place</td>
</tr>
<tr>
<td>0.01</td>
<td>p2</td>
<td>1.00%</td>
<td>Number will be converted to percentage with 2 decimal place</td>
</tr>
<tr>
<td>0.01</td>
<td>p3</td>
<td>1.000%</td>
<td>Number will be converted to percentage with 3 decimal place</td>
</tr>
<tr>
<td>1000</td>
<td>c1</td>
<td>$1,000.0</td>
<td>Currency symbol will be appended to number and number will rounded to 1 decimal place</td>
</tr>
<tr>
<td>1000</td>
<td>c2</td>
<td>$1,000.00</td>
<td>Currency symbol will be appended to number and number will rounded to 2 decimal place</td>
</tr>
</table>


### Formatting date time values

Date time labels can be formatted using the **labelFormat** property of axis.

{% highlight js %}

     $("#chartcontainer").ejChart({
            primaryXAxis: {

                //Formatting date time labels in date/Month name/Year format
                labelFormat: 'dd/MMMM/yyyy',
                //  …         
            },
            //  ...
     });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img24.png" Caption="Formatting datetime labels"%}


The following table describes the result of applying some common date time formats to labelFormat property

<table>
<tr>
<td><b>Label Value</b></td>
<td><b>Label Format Property Value</b></td>
<td><b>Result </b></td>
<td><b>Description </b></td>
</tr>        
<tr>
<td>new Date(2000, 03, 10)</td>
<td>dddd</td>
<td>Monday</td>
<td>Date will be displayed in day format</td>
</tr> 
<tr>
<td>new Date(2000, 03, 10)</td>
<td>MM/dd/yyyy</td>
<td>04/10/2000</td>
<td>Date will be displayed in month/date/year format</td>
</tr> 
<tr>
<td>new Date(2000, 03, 10)</td>
<td>n3</td>
<td>1000.000</td>
<td>Number will be rounded to 3 decimal place</td>
</tr>
<tr>
<td>new Date(2000, 03, 10)</td>
<td>MMM</td>
<td>Apr</td>
<td>Shorthand month for the date will be displayed</td>
</tr>
<tr>
<td>new Date(2000, 03, 10)</td>
<td>t</td>
<td>12:00 AM</td>
<td>Time of the date value will be displayed as label</td>
</tr>
<tr>
<td>new Date(2000, 03, 10)</td>
<td>hh:mm:ss</td>
<td>12:00:00</td>
<td>Label will be displayed in hours:minutes:seconds format</td>
</tr>
</table>

### Custom label format

Prefix and suffix can be added to category labels using the **labelFormat** property. Use *{value}* as placeholder text in your custom text, it will be replaced with corresponding axis label at runtime.

{% highlight js %}

$("#chartcontainer").ejChart({
    primaryXAxis: {
        //...
        //Adding prefix and suffix to axis labels
        labelFormat: '${value} K',                 
    },
    //...
});

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img25.png" Caption="Custom label format"%}

## Common axis features

Customization of features such as axis title, labels, grid lines and tick lines are common to all the axes. Each of these features are explained in this section.

### Axis Visibility

Axis visibility can be controlled using the **visible** property of axis. Default value of **visible** property is **true**. 

{% highlight js %}

     $("#chartcontainer").ejChart({

           primaryYAxis: {
                   
                //Disabling visibility of Y-axis
                visible: false

                //  ...         
            },
            //  ...
     });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img26.png" Caption="Chart with hidden Y-axis"%}

### Axis title

The **title** property in axis provides options to customize the text and font of axis title. Axis does not display title by default. Title text can also be trimmed based on title text length or specified length.

{% highlight js %}

     $("#chartcontainer").ejChart({

           primaryXAxis: {
                      
                //Customizing axis title
                title : {
                    text : 'Month',
                    font : {
                        fontFamily : 'Segoe UI',
                        size : '16px',
                        fontWeight : 'bold' ,
                        color : 'grey',
                    },
                    enableTrim : true,  
                    maximumTitleWidth : 80 
                }
                //  ...         
            },

            //  ...
     });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img27.png" Caption="Axis Title"%}


### Label customization

The **font** property of axis provides options to customize the **font-family**, **color**, **opacity**, **size** and **font-weight** of axis labels.  

{% highlight js %}

     $("#chartcontainer").ejChart({

          primaryXAxis: {

                //Customizing label appearance
                font : {
                        fontFamily : 'Segoe UI',
                        size : '14px',
                        fontWeight : 'bold' ,
                        color : 'blue',
                },                
                //  ...         
            },

            //  ...
     });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img28.png" Caption="Axis label customization"%}


### Label and tick positioning
 
Axis labels and ticks can be positioned inside or outside the chart area by using **labelPosition** and **tickPosition** properties. By default labels and ticks will be positioned outside the chart area.
 
{% highlight js %}

     $("#chartcontainer").ejChart({

             primaryXAxis: {

                //Customizing label and tick positions
                labelPosition : 'inside',
                tickLinesPosition : 'inside',

                //  ...         
            },
            //  ...
     });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img29.png" Caption="Label and tick positioning"%}


### Edge labels placement

Labels with long text at the edges of an axis may appear partially outside the chart. The **edgeLabelPlacement** property can be used to avoid the partial appearance of labels at the corners. 

{% highlight js %}

     $("#chartcontainer").ejChart({

             primaryXAxis: {

                //Customizing edge label placement
                edgeLabelPlacement : 'shift',
                //  ...         
            },
            //  ...
     });

{% endhighlight %}

**Chart before setting edge label placement to X-axis**

{% include image.html url="/js/Chart/Axis_images/axis_img30.png" Caption="Chart before setting edge label placement to X-axis"%}

**Chart after setting edge label placement to X-axis**

{% include image.html url="/js/Chart/Axis_images/axis_img31.png" Caption="Chart after setting edge label placement to X-axis"%}

### Grid lines customization

The **majorGridLines** and **minorGridLines** properties in axis are used to customize the major grid lines and minor grid lines of an axis. They provide options to change the width, color, visibility and opacity of grid lines. By default minor grid lines will not be visible.

{% highlight js %}

     $("#chartcontainer").ejChart({

          primaryXAxis: {

                //Customizing grid lines
                majorGridLines : {
                    color : 'blue',                    
                    visible : true,  
                    width : 1 
                },
                minorTicksPerInterval: 0,
                minorGridLines : {
                    color : 'red',                    
                    visible : false,  
                    width : 1 
                }
            }
            //  ...
     });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img32.png" Caption="Major gridlines customization"%}


### Tick lines customization

The **majorTickLines** and **minorTickLines** properties in axis are used to customize the major tick lines of an axis and minor tick lines of an axis. They provide options to change the width, size, color and visibility of grid lines. By default minor tick lines will not be visible.

{% highlight js %}

     $("#chartcontainer").ejChart({

           primaryXAxis: {

                //Customizing tick lines
                majorTickLines : {
                    color : 'blue',                    
                    visible : true,  
                    width : 1 ,
                    size : 5,
                },
                minorTicksPerInterval: 0,
                minorTickLines : {
                    color : 'red',                    
                    visible : false,  
                    width : 1 ,
                    size : 5
                }
                //  ...
             }
            //  ...
     });

{% endhighlight %}

{% include image.html url="/js/Chart/Axis_images/axis_img33.png" Caption="Major gridlines customization"%}

  
### Inversing axis

Axis can be inversed using the **isInversed** property of axis. Default value of **isInversed** property is **false**.

{% highlight js %}

     $("#chartcontainer").ejChart({

           primaryXAxis: {

                //Inversing the X-axis
                isInversed: false

                //  ...         
            },
            //  ...
     });

{% endhighlight %}

**Chart before inversing the axes**

{% include image.html url="/js/Chart/Axis_images/axis_img34.png" Caption="Chart before inversing the axes"%}

**Chart after inversing the axes**

{% include image.html url="/js/Chart/Axis_images/axis_img35.png" Caption="Chart after inversing the axes"%}
   

### Placing axes at the opposite side

The **opposedPosition** property of axis can be used to place the axis at the opposite side of its default position. Default value of **opposedPosition** property is **false**. 

{% highlight js %}

     $("#chartcontainer").ejChart({

            primaryXAxis: {

                //Placing axis at the opposite side of its normal position
                opposedPosition: true

                //  ...         
            },
            //  ...
     });

{% endhighlight %}

**Chart with X and Y axes at normal position**

{% include image.html url="/js/Chart/Axis_images/axis_img36.png" Caption="Chart with X and Y axes at normal position"%}

**Chart with Y-axis at opposed position**

{% include image.html url="/js/Chart/Axis_images/axis_img37.png" Caption="Chart with Y-axis at opposed position"%}


### Maximum number of labels per 100 pixels

By default, a maximum of 3 labels are displayed for each 100 pixels in axis. The maximum number of labels that should be present within 100 pixels length can be customized using the **maximumLabels** property of axis. This property is applicable only for automatic range calculation and will not work if you set value for **interval** property in axis range.

{% highlight js %}

     $("#chartcontainer").ejChart({

         primaryXAxis: {

                //Maximum number of labels per 100 pixels
                maximumLabels : 1

                //  ...        
            },
            //  ...
     });

{% endhighlight %}

**Chart before setting maximum labels per 100 pixels**

{% include image.html url="/js/Chart/Axis_images/axis_img38.png" Caption="Chart before setting maximum labels per 100 pixels"%}

**Chart after setting maximum labels one per 100 pixels**

{% include image.html url="/js/Chart/Axis_images/axis_img39.png" Caption="Chart after setting maximum labels one per 100 pixels"%}


## Multiple Axis

Multiple axes can be used in Chart and chart area can be split into multiple panes to draw multiple series with multiple axes.

{% include image.html url="/js/Chart/Axis_images/axis_img40.png" Caption="Chart with multiple axes"%}

An additional horizontal or vertical axis can be added to chart by adding an axis instance to the **axes** collection, and then you can associate it to a series by specifying the name of the axis to the **xAxisName** or **yAxisName** property of the series.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
           //  Creating a secondary horizontal axis
            axes: [{
                name : 'SecondaryX',
                //  ...         
            },{
                name : 'SecondaryY',
                //  ...        
            }],
            //  ...
            series: [{
                //  Binding secondary X-axis with a series
                xAxisName : 'SecondaryX',

               //  Binding secondary Y-axis with a series
                yAxisName : 'SecondaryY',
                //  …
            },
            {
                //  ...         
            }],

            // ...             

        });


{% endhighlight %}



{% include image.html url="/js/Chart/Axis_images/axis_img41.png" Caption="Chart with Multiple Axis"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/multipleaxes) here to view the multiple axis online demo sample.


## Smart Axis Labels

Axis labels may overlap with each other based on chart dimensions and label size. The **labelIntersectAction** property of axis is very useful in avoiding the overlapping of axis labels with each other. Default value of **labelIntersectAction** is **none**. Other available values of Label Intersect Actions are **rotate45**, **rotate90**, **trim**, **multiplerows**, **wrap** and **hide**.

{% highlight js %}

       $("#chartcontainer").ejChart({

            // Avoid overlapping of x-axis labels
            primaryXAxis: {¬¬
                labelIntersectAction : 'multiplerows',
                 //  ...
            },
            
            // ...
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Axis_images/axis_img42.png" Caption="Chart with smart Axis Labelss"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/smartaxislabels) here to view our online demo sample for smart axis labels.



Following screenshot displays the result of setting **rotate45** as value to *labelIntersectAction* property.

{% include image.html url="/js/Chart/Axis_images/axis_img43.png" Caption="LabelIntersectAction rotate to 45 degree"%}


Following screenshot displays the result of setting **rotate90** as value to *labelIntersectAction* property.

{% include image.html url="/js/Chart/Axis_images/axis_img44.png" Caption="LabelIntersectAction rotate to 90 degree"%}


Following screenshot displays the result of setting **wrap** as value to *labelIntersectAction* property.

{% include image.html url="/js/Chart/Axis_images/axis_img45.png" Caption="LabelIntersectAction with wrapping the text"%}


Following screenshot displays the result of setting **trim** as value to *labelIntersectAction* property.

{% include image.html url="/js/Chart/Axis_images/axis_img46.png" Caption="LabelIntersectAction with trimming the text"%}


Following screenshot displays the result of setting **hide** as value to *labelIntersectAction* property.

{% include image.html url="/js/Chart/Axis_images/axis_img47.png" Caption="LabelIntersectAction with hide the text"%}


Following screenshot displays the result of setting **multiplerows ** as value to *labelIntersectAction* property.

{% include image.html url="/js/Chart/Axis_images/axis_img48.png" Caption="LabelIntersectAction with multiplerows of the text"%}