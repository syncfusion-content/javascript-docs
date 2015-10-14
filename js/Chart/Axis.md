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

Category axis displays the text labels instead of numbers. To use the categorical axis, you can set the [valueType](../api/ejchart#members:primaryxaxis-valuetype) property of the axis to **category**. Default value of [valueType](../api/ejchart#members:primaryxaxis-valuetype) is **double**.

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

Labels in the category axis can be placed on the ticks by setting the [labelPlacement](../api/ejchart#members:primaryxaxis-labelplacement) property of axis to **onticks**. Default value of [labelPlacement](../api/ejchart#members:primaryxaxis-valuetype) property is **betweenticks** i.e. labels are placed between the ticks by default.

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

To display the labels after a fixed interval n, you can set the [interval](../api/ejchart#members:primaryxaxis-range-interval) property of the axis range as **n**. Default value of interval is 1 i.e. all the labels are displayed by default.

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

Numeric axis uses numerical scale and displays numbers as labels. To use numeric axis, you can set the [valueType](../api/ejchart#members:primaryxaxis-valuetype) property of axis to **double**. 

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

To customize the range of an axis, you can use the [range](../api/ejchart#members:primaryxaxis-range) property of axis to set the [minimum](../api/ejchart#members:primaryxaxis-range-minimum), [maximum](../api/ejchart#members:primaryxaxis-range-maximum) and [interval](../api/ejchart#members:primaryxaxis-range-interval) values. By default, nice range is calculated automatically based on the provided data.


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

Axis interval can be customized by using the [interval](../api/ejchart#members:primaryyaxis-range-interval) property of the axis range. By default, nice interval is calculated based on the minimum and maximum value of the provided data.

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

Padding can be applied to the minimum and maximum extremes of the axis range by using the [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding) property. Numeric axis supports the following types of padding

* None
* Round
* Additional
* Normal

**None**

When the value of the [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding) property is **none**, padding can not be applied to the axis. This is also the default value of the rangePadding. 

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

When the value of [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding) property is **round**, axis range is rounded to the nearest possible value divided by the interval.

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

When the value of the [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding) property is **additional**, axis range is rounded and an interval of the axis is added as padding to the minimum and maximum values of the range.

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

When the value of the [rangePadding](../api/ejchart#members:primaryyaxis-rangepadding) property is **normal**, padding is applied to the axis based on the range calculation.

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

Date time axis uses date time scale and displays date time values as axis labels in the specified format. To use date time axis, you can set the [valueType](../api/ejchart#members:primaryxaxis-valuetype) property of axis to **datetime**.

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
 
 Axis range can be customized by using the [range](../api/ejchart#members:primaryxaxis-range) property to set the [minimum](../api/ejchart#members:primaryxaxis-range-minimum), [maximum](../api/ejchart#members:primaryxaxis-range-maximum) and [interval](../api/ejchart#members:primaryxaxis-range-interval) values. By default, nice range is calculated automatically based on the provided data.
 
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

Date time intervals can be customized by using the [interval](../api/ejchart#members:primaryxaxis-range-interval) and [intervalType](../api/ejchart#members:primaryxaxis-intervaltype) properties of the axis. For example, setting [interval](../api/ejchart#members:primaryxaxis-range-interval) as **2** and [intervalType](../api/ejchart#members:primaryxaxis-intervaltype) as **years** considers 2 years as interval.

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

Padding can be applied to the minimum and maximum extremes of the range by using the [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding) property. Date time axis supports the following types of padding

* None
* Round
* Aditional

**None**

When the value of the [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding) property is **none**, padding is applied to the axis. This is also the default value of the [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding). 

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

When the value of the [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding) property is **round**, axis range is rounded to the nearest possible date time value.

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

When the value of the [rangePadding](../api/ejchart#members:primaryxaxis-rangepadding) property is **additional**, range is rounded and date time interval of the axis are added as padding to the minimum and maximum extremes of the range.

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

Logarithmic axis uses logarithmic scale and it is very useful in visualizing when the data has values with both lower order of magnitude **(eg: 10<sup>-6</sup>)** and higher order of magnitude **(eg: 10<sup>6</sup>)**. To use logarithmic axis, you can set the [valueType](../api/ejchart#members:primaryxaxis-valuetype) property of axis to **logarithmic**.  

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

Logarithmic range can be customized by using the [range](../api/ejchart#members:primaryxaxis-range) property of axis to change the [minimum](../api/ejchart#members:primaryxaxis-range-minimum), [maximum](../api/ejchart#members:primaryxaxis-range-maximum) and [interval](../api/ejchart#members:primaryxaxis-range-interval) values. By default, nice range is calculated automatically based on the provided data.

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

Logarithmic base can be customized by using the [logBase](../api/ejchart#members:primaryxaxis-logbase) property of the axis. Default value of [logBase](../api/ejchart#members:primaryxaxis-logbase) is **10**.

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

Logarithmic axis interval can be customized by using the [interval](../api/ejchart#members:primaryxaxis-range-interval) property of the axis. When the logarithmic base is 10 and logarithmic interval is 2, then the axis labels are placed at an interval of 10<sup>2</sup>. Default value of interval is 1. 

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

Numeric labels can be formatted by using the [labelFormat](../api/ejchart#members:primaryxaxis-labelformat) property. Numeric values can be formatted with n (number with decimal points), c (currency) and p (percentage) commands.

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
<td>The Number is rounded to 1 decimal place</td>
</tr> 
<tr>
<td>1000</td>
<td>n2</td>
<td>1000.00</td>
<td>The Number is rounded to 2 decimal place</td>
</tr> 
<tr>
<td>1000</td>
<td>n3</td>
<td>1000.000</td>
<td>The Number is rounded to 3 decimal place</td>
</tr>
<tr>
<td>0.01</td>
<td>p1</td>
<td>1.0%</td>
<td>The Number is converted to percentage with 1 decimal place</td>
</tr>
<tr>
<td>0.01</td>
<td>p2</td>
<td>1.00%</td>
<td>The Number is converted to percentage with 2 decimal place</td>
</tr>
<tr>
<td>0.01</td>
<td>p3</td>
<td>1.000%</td>
<td>The Number is converted to percentage with 3 decimal place</td>
</tr>
<tr>
<td>1000</td>
<td>c1</td>
<td>$1,000.0</td>
<td>The Currency symbol is appended to number and number is rounded to 1 decimal place</td>
</tr>
<tr>
<td>1000</td>
<td>c2</td>
<td>$1,000.00</td>
<td>The Currency symbol is appended to number and number is rounded to 2 decimal place</td>
</tr>
</table>


### Formatting date time values

Date time labels can be formatted by using the [labelFormat](../api/ejchart#members:primaryxaxis-labelformat) property of the axis.

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


The following table describes the result of applying some common date time formats to the labelFormat property

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
<td>The Date is displayed in day format</td>
</tr> 
<tr>
<td>new Date(2000, 03, 10)</td>
<td>MM/dd/yyyy</td>
<td>04/10/2000</td>
<td>The Date is displayed in month/date/year format</td>
</tr> 
<tr>
<td>new Date(2000, 03, 10)</td>
<td>n3</td>
<td>1000.000</td>
<td>The Number is rounded to 3 decimal place</td>
</tr>
<tr>
<td>new Date(2000, 03, 10)</td>
<td>MMM</td>
<td>Apr</td>
<td>The Shorthand month for the date is displayed</td>
</tr>
<tr>
<td>new Date(2000, 03, 10)</td>
<td>t</td>
<td>12:00 AM</td>
<td>Time of the date value is displayed as label</td>
</tr>
<tr>
<td>new Date(2000, 03, 10)</td>
<td>hh:mm:ss</td>
<td>12:00:00</td>
<td>The Label is displayed in hours:minutes:seconds format</td>
</tr>
</table>

### Custom label format

Prefix and suffix can be added to the category labels by using the [labelFormat](../api/ejchart#members:primaryxaxis-labelformat) property. You can use the *{value}* as placeholder text in your custom text, it is replaced with the corresponding axis label at runtime.

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

Customization of features such as axis title, labels, grid lines and tick lines are common to all the axis. Each of these features are explained in this section.

### Axis Visibility

Axis visibility can be controlled by using the [visible](../api/ejchart#members:primaryxaxis-visible) property of the axis. Default value of the [visible](../api/ejchart#members:primaryxaxis-visible) property is **true**. 

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

The [title](../api/ejchart#members:primaryxaxis-title) property in the axis provides options to customize the text and font of axis title. Axis does not display title by default. Title text can also be trimmed based on the title text length or specified length.

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

The [font](../api/ejchart#members:primaryxaxis-font) property of axis provides options to customize the [font-family](../api/ejchart#members:primaryxaxis-font-fontfamily), [color](../api/ejchart#members:primaryxaxis-font-color), [opacity](../api/ejchart#members:primaryxaxis-font-opacity), [size](../api/ejchart#members:primaryxaxis-font-size) and [font-weight](../api/ejchart#members:primaryxaxis-font-fontweight) of the axis labels.  

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
 
Axis labels and ticks can be positioned inside or outside the chart area by using the [labelPosition](../api/ejchart#members:primaryxaxis-labelposition) and [tickPosition](../api/ejchart#members:primaryxaxis-tickposition) properties. By default, the labels and ticks are positioned outside the chart area.
 
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

Labels with long text at the edges of an axis may appear partially outside the chart. The [edgeLabelPlacement](../api/ejchart#members:primaryxaxis-edgelabelplacement) property can be used to avoid the partial appearance of labels at the corners. 

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

The [majorGridLines](../api/ejchart#members:primaryxaxis-majorgridlines) and [minorGridLines](../api/ejchart#members:primaryxaxis-minorgridlines) properties in the axis are used to customize the major grid lines and minor grid lines of an axis. They provide options to change the width, color, visibility and opacity of grid lines. By default, the minor grid lines are not visible.

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

The [majorTickLines](../api/ejchart#members:primaryxaxis-majorticklines) and [minorTickLines](../api/ejchart#members:primaryxaxis-minorticklines) properties in the axis are used to customize the major tick lines of an axis and minor tick lines of an axis. They provide options to change the width, size, color and visibility of grid lines. By default, the minor tick lines are not visible.

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

Axis can be inversed by using the [isInversed](../api/ejchart#members:primaryxaxis-isinversed) property of the axis. Default value of [isInversed](../api/ejchart#members:primaryxaxis-isinversed) property is **false**.

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

The [opposedPosition](../api/ejchart#members:primaryxaxis-opposedposition) property of axis can be used to place the axis at the opposite side of its default position. Default value of [opposedPosition](../api/ejchart#members:primaryxaxis-opposedposition) property is **false**. 

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

By default, a maximum of 3 labels are displayed for each 100 pixels in the axis. The maximum number of labels that should be present within the 100 pixels length can be customized by using the [maximumLabels](../api/ejchart#members:primaryxaxis-maximumlabels) property of the axis. This property is applicable only for an automatic range calculation and will not work if you set value for [interval](../api/ejchart#members:primaryxaxis-range-interval) property in the axis range.

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

Multiple axes can be used in the Chart and chart area can be split into multiple panes to draw multiple series with multiple axes.

{% include image.html url="/js/Chart/Axis_images/axis_img40.png" Caption="Chart with multiple axes"%}

An additional horizontal or vertical axis can be added to the chart by adding an axis instance to the **axes** collection, and then you can associate it to a series by specifying the name of the axis to the [xAxisName](../api/ejchart#members:series-xaxisname) or [yAxisName](../api/ejchart#members:series-yaxisname) property of the series.

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

Axis labels may overlap with each other based on the chart dimensions and label size. The [labelIntersectAction](../api/ejchart#members:primaryxaxis-labelintersectaction) property of the axis is very useful in avoiding the overlapping of the axis labels with each other. Default value of [labelIntersectAction](../api/ejchart#members:primaryxaxis-labelintersectaction) is **none**. Other available values of Label Intersect Actions are **rotate45**, **rotate90**, **trim**, **multiplerows**, **wrap** and **hide**.

{% highlight js %}

       $("#chartcontainer").ejChart({

            // Avoid overlapping of x-axis labels
            primaryXAxis: {
                labelIntersectAction : 'multiplerows',
                 //  ...
            },
            
            // ...
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Axis_images/axis_img42.png" Caption="Chart with smart Axis Labelss"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/smartaxislabels) here to view our online demo sample for smart axis labels.



The following screenshot displays the result of setting the **rotate45** as value to the [labelIntersectAction](../api/ejchart#members:primaryxaxis-labelintersectaction) property.

{% include image.html url="/js/Chart/Axis_images/axis_img43.png" Caption="LabelIntersectAction rotate to 45 degree"%}


The following screenshot displays the result of setting the **rotate90** as value to the [labelIntersectAction](../api/ejchart#members:primaryxaxis-labelintersectaction) property.

{% include image.html url="/js/Chart/Axis_images/axis_img44.png" Caption="LabelIntersectAction rotate to 90 degree"%}


The following screenshot displays the result of setting the **wrap** as value to the [labelIntersectAction](../api/ejchart#members:primaryxaxis-labelintersectaction) property.

{% include image.html url="/js/Chart/Axis_images/axis_img45.png" Caption="LabelIntersectAction with wrapping the text"%}


The following screenshot displays the result of setting the **trim** as value to the [labelIntersectAction](../api/ejchart#members:primaryxaxis-labelintersectaction) property.

{% include image.html url="/js/Chart/Axis_images/axis_img46.png" Caption="LabelIntersectAction with trimming the text"%}


The following screenshot displays the result of setting the **hide** as value to the [labelIntersectAction](../api/ejchart#members:primaryxaxis-labelintersectaction) property.

{% include image.html url="/js/Chart/Axis_images/axis_img47.png" Caption="LabelIntersectAction with hide the text"%}


The following screenshot displays the result of setting the **multiplerows ** as value to the [labelIntersectAction](../api/ejchart#members:primaryxaxis-labelintersectaction) property.

{% include image.html url="/js/Chart/Axis_images/axis_img48.png" Caption="LabelIntersectAction with multiplerows of the text"%}