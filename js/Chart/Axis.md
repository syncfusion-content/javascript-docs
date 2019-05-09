---
layout: post
title: Syncfusion EJ1 Chart Axis
description: How to customize the grid lines, tick lines, labels and title of chart axis
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Axis

**Charts** typically have two axes that are used to measure and categorize data: a vertical (y) [`primaryYAxis`](../api/ejchart#members:primaryyaxis), and a horizontal (x) [`primaryXAxis`](../api/ejchart#members:primaryxaxis).

Vertical axis always uses numerical or logarithmic scale. Horizontal(x) axis supports the following types of scale:

* Category
* Numeric
* DateTime
* DateTime Category
* Logarithmic

## Category Axis

Category axis displays the text labels instead of numbers. To use the categorical axis, you can set the [`valueType`](../api/ejchart#members:primaryxaxis-valuetype) property of the axis to the **category**. Default value of [`valueType`](../api/ejchart#members:primaryxaxis-valuetype) is **double**.

{% highlight js %}

$("#container").ejChart({
    primaryXAxis: {

        //Use categorical scale in primary X axis
        valueType: 'category',         

        //  ...         
    },
    //  ...
});


{% endhighlight %}



![Category](Axis_images/Axis_img1.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/column) here to view our online demo sample that uses Category axis.


### Place labels on ticks

Labels in the category axis can be placed on the ticks by setting the [`labelPlacement`](../api/ejchart#members:primaryxaxis-labelplacement) property of axis to the **onticks**. The default value of the [`labelPlacement`](../api/ejchart#members:primaryxaxis-valuetype) property is **betweenticks** i.e. labels are placed between the ticks, by default.

{% highlight javascript %}

$("#container").ejChart({
    primaryXAxis: {

        //Placing X-axis labels on the ticks
        labelPlacement: 'onticks',         

        //  ...        
    },
    //  ...
});


{% endhighlight %}

![Onticks](Axis_images/Axis_img2.png)


### Display labels after a fixed interval

To display the labels after a fixed interval n, you can set the [`interval`](../api/ejchart#members:primaryxaxis-range-interval) property of the axis range as **n**. The default value of the interval is 1 i.e. all the labels are displayed.

{% highlight javascript %}

$("#container").ejChart({
    primaryXAxis: {

        //Displaying labels after 2 intervals
        range: { interval: 2 },                

        //  ...        
    },
    //  ...
});


{% endhighlight %}

![Interval](Axis_images/Axis_img3.png)


### Indexed Category Axis

Category axis can also plot points based on index value of data points. Index based plotting can be enabled by setting [`isIndexed`](../api/ejchart#members:primaryxaxis-isindexed) property to true in the axis.

{% highlight javascript %}

    $("#container").ejChart({
         // ...             
         primaryXAxis: {                                  
             isIndexed: true
         },       
         series:[{
             points:[{ x: "Monday", y: 50 }, { x: "Tuesday", y: 40 }, { x: "Wednesday", y: 70 },
                    { x: "Thursday", y: 60 }, { x: "Friday", y: 50 },
                    { x: "Monday", y: 40 }, { x: "Monday", y: 30 } 
                       ] 
          }],
        // ...             
     });

{% endhighlight %}


![Indexed](Axis_images/Axis_img50.png)

**While Category axis isIndexed value false**

![IndexedFalse](Axis_images/Axis_img51.png)


## Numeric Axis 

Numeric axis uses numerical scale and displays numbers as labels. To use numeric axis, you can set the [`valueType`](../api/ejchart#members:primaryxaxis-valuetype) property of the axis to **double**. 

{% highlight javascript %}

$("#container").ejChart({
    // ...             
    primaryYAxis: {
        //Use numerical scale in primary Y axis
        valueType: 'double',        
        //  ...         
    },
    // ...             
});


{% endhighlight %}

![Double](Axis_images/Axis_img4.png)


### Customize numeric range

To customize the range of an axis, you can use the [`range`](../api/ejchart#members:primaryxaxis-range) property of the axis to set the [`min`](../api/ejchart#members:primaryxaxis-range-min), [`max`](../api/ejchart#members:primaryxaxis-range-max) and [`interval`](../api/ejchart#members:primaryxaxis-range-interval) values. Nice range is calculated automatically based on the provided data, by default.


{% highlight javascript %}

$("#container").ejChart({
    // ...             
    primaryYAxis: {

        //Customizing Y-axis range
        range: { min: 0, max: 50 },         

        //  ...       
    },
    // ...             
});


{% endhighlight %}

![Doublerange](Axis_images/Axis_img5.png)


#### Customizing numeric interval

Axis interval can be customized by using the [`interval`](../api/ejchart#members:primaryyaxis-range-interval) property of the axis range. Nice interval is calculated based on the minimum and maximum value of the provided data, by default.

{% highlight javascript %}

$("#container").ejChart({
    // ...             
    primaryYAxis: {
              
        //Customizing Y-axis interval
        range: { interval: 5 },         

        //  ...         
    },

    // ...             
});


{% endhighlight %}

![DInterval](Axis_images/Axis_img6.png)

### Apply padding to the range

Padding can be applied to the minimum and maximum extremes of the axis range by using the [`rangePadding`](../api/ejchart#members:primaryxaxis-rangepadding) property. Numeric axis supports the following types of padding

* None
* Round
* Additional
* Normal

**None**

When the value of the [`rangePadding`](../api/ejchart#members:primaryxaxis-rangepadding) property is **none**, padding can not be applied to the axis. This is also the default value of the rangePadding. 

{% highlight javascript %}

        $("#container").ejChart({
              // ...             
               primaryYAxis: {
               
                //Applying none as range padding
                rangePadding: 'none',       

                //  ...         
            },

            // ...             
        });


{% endhighlight %}

![Doublepad](Axis_images/Axis_img7.png)


#### Round

When the value of [`rangePadding`](../api/ejchart#members:primaryxaxis-rangepadding) property is **round**, the axis range is rounded to the nearest possible value divided by the interval. The [`roundingPlaces`](../api/ejchart#members:primaryxaxis-roundingplaces) property rounds the number to the given number of decimals.

{% highlight javascript %}

        $("#container").ejChart({
              // ...             
               primaryYAxis: {
               
                //Applying round as range padding
                rangePadding: 'round'
                //  ...         
            },

            // ...             
        });


{% endhighlight %}

**Chart before rounding axis range**

![Rounddouble](Axis_images/Axis_img8.png)



**Chart after rounding axis range**

![AfterDouble](Axis_images/Axis_img9.png)

**Additional**

When the value of the [`rangePadding`](../api/ejchart#members:primaryxaxis-rangepadding) property is **additional**, the axis range is rounded and an interval of the axis is added as padding to the minimum and maximum values of the range.

{% highlight javascript %}

        $("#container").ejChart({
              // ...             
               primaryYAxis: {
               
                //Applying additional range padding
                rangePadding: 'additional',      

                //  ...         
            },

            // ...             
        });


{% endhighlight %}

![AdditionalDouble](Axis_images/Axis_img10.png)


**Normal**

When the value of the [`rangePadding`](../api/ejchart#members:primaryyaxis-rangepadding) property is **normal**, the padding is applied to the axis based on the range calculation.

{% highlight javascript %}

        $("#container").ejChart({
              // ...             
               primaryYAxis: {
               
                //Applying normal range padding
                rangePadding: 'normal',      

                //  ...         
            },

            // ...             
        });


{% endhighlight %}

![NormalDouble](Axis_images/Axis_img11.png)


#### Customizing the starting range of the axis

By default the Y axis will be always calculated from the value 0 for column, bar, stacking column and stacking bar series types. You can modify this behavior by setting false to the property [`startFromZero`](../api/ejchart#members:primaryyaxis-startfromzero) in the axis. On setting this the axis minimum value will be calculated based on the value for the data points.

{% highlight javascript %}

$("#container").ejChart(
        {
	     //Initializing Primary Y Axis	
            primaryYAxis:
            {
               rangePadding: "none",
		       startFromZero: false                
            },
			
	     // ..
        });

{% endhighlight %}

![Startfalse](Axis_images/Axis_img66.png)


## DateTime Axis

Date time axis uses date time scale and displays the date time values as axis labels in the specified format. To use date time axis, set the [`valueType`](../api/ejchart#members:primaryxaxis-valuetype) property of the axis to **datetime**.

{% highlight javascript %}

        $("#container").ejChart({
              // ...             
            primaryXAxis: {

                //Use date time scale in primary X axis
                valueType: 'datetime',         

                //  ...         
            },
            // ...             
        });


{% endhighlight %}

![Datetime](Axis_images/Axis_img12.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/datetimeaxis) here to view our online demo sample for date time axis.

 
### Customizing date time range
 
 Axis range can be customized by using the [`range`](../api/ejchart#members:primaryxaxis-range) property to set the [`minimum`](../api/ejchart#members:primaryxaxis-range-minimum), [`maximum`](../api/ejchart#members:primaryxaxis-range-maximum) and [`interval`](../api/ejchart#members:primaryxaxis-range-interval) values. Nice range is calculated automatically based on the provided data, by default.
 
 {% highlight javascript %}

        $("#container").ejChart({
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

![Datetimerange](Axis_images/Axis_img13.png)


### Date time intervals

Date time intervals can be customized by using the [`interval`](../api/ejchart#members:primaryxaxis-range-interval) and [`intervalType`](../api/ejchart#members:primaryxaxis-intervaltype) properties of the axis. For example, when you set [`interval`](../api/ejchart#members:primaryxaxis-range-interval) as **2** and [`intervalType`](../api/ejchart#members:primaryxaxis-intervaltype) as **years**, it considers the 2 years as interval.

Essential Chart supports the following types of interval for date time axis.

* Days
* Hours
* Milliseconds
* Minutes
* Months
* Seconds
* Years

{% highlight javascript %}

        $("#container").ejChart({
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


![Datetimeinterval](Axis_images/Axis_img14.png)


### Apply padding to the range

Padding can be applied to the minimum and maximum extremes of the range by using the [`rangePadding`](../api/ejchart#members:primaryxaxis-rangepadding) property. Date time axis supports the following types of padding

* None
* Round
* Additional

**None**

When the value of the [`rangePadding`](../api/ejchart#members:primaryxaxis-rangepadding) property is **none**, padding is applied to the axis. This is also the default value of the rangePadding. 

{% highlight javascript %}

     $("#container").ejChart({
            primaryXAxis: {

                //Applying none as range padding
                rangePadding: 'none',
                //  ...       
            },
            //  ...
     });

{% endhighlight %} 

![DatetimeRangepad](Axis_images/Axis_img15.png)

**Round**

When the value of the [`rangePadding`](../api/ejchart#members:primaryxaxis-rangepadding) property is **round**, the axis range is rounded to the nearest possible date time value.

{% highlight javascript %}

     $("#container").ejChart({
            primaryXAxis: {

                //Applying round as range padding
                rangePadding: 'round',
                //  ...       
            },
            //  ...
     });

{% endhighlight %} 

**Chart before rounding axis range**

![Datetimeround](Axis_images/Axis_img16.png)


**Chart after rounding axis range**

![Afterdatetime](Axis_images/Axis_img17.png)

**Additional** 

When the value of the [`rangePadding`](../api/ejchart#members:primaryxaxis-rangepadding) property is **additional**, the range is rounded and date time interval of the axis are added as padding to the minimum and maximum extremes of the range.

{% highlight javascript %}

     $("#container").ejChart({
            primaryXAxis: {

                //Applying additional as range padding
                rangePadding: 'additional',
                //  ...       
            },
            //  ...
     });

{% endhighlight %} 

![Additionaldatetime](Axis_images/Axis_img18.png)


## DateTime Category Axis

DateTime category axis takes date time value as input but behaves like category axis. This is used to display the date time values with nonlinear intervals (used to depict the business days by skipping holidays). To use date time axis, set the [`valueType`] (../api/ejchart#members:primaryxaxis-valuetype) property of the axis to **datetimeCategory**.

{% highlight javascript %}

$("#container").ejChart({ 
	primaryXAxis: { 
		valueType: 'datetimeCategory', 
		// ... 
	}, 
	// ... 
});

{% endhighlight %}

![Datetimecategory](Axis_images/Axis_img63.png)

 [Click](http://js.syncfusion.com/demos/web/#!/bootstrap/chart/ChartAxes/DateTimeCategoryAxis) here to view our online demo sample for date time axis.

### Customizing DateTime Category range

Axis range can be customized by using the [`range`](../api/ejchart#members:primaryxaxis-range) property to set the [`minimum`](../api/ejchart#members:primaryxaxis-range-minimum), [`maximum`](../api/ejchart#members:primaryxaxis-range-maximum) and [`interval`](../api/ejchart#members:primaryxaxis-range-interval) values. Datetime category axis takes numeric input for minimum and maximum property.

{% highlight javascript %}

$("#container").ejChart({
            primaryXAxis: {

                range: {  //Customizing X-axis date time category range
                    min: 0, 
                    max: 4
                },         

                //  ...         
            },
            // ...             
        });

{% endhighlight %}

![DateRange](Axis_images/Axis_img64.png)

### DateTime Category intervals

Date time category intervals can be customized by using the [`interval`](../api/ejchart#members:primaryxaxis-interval) and [`intervalType`](../api/ejchart#members:primaryxaxis-intervalType) properties of the axis. For example, when you set the intervalType as months, it displays only the first label of all the months from the data.

Essential Chart supports the following types of interval for date time category axis.
* Days
* Hours
* Milliseconds
* Minutes
* Months
* Seconds
* Years
* Auto

{% highlight javascript %}

$("#container").ejChart({
            primaryXAxis: {
			
                intervalType: "months"        
                //  ...         
            },
            // ...             
        });

{% endhighlight %}

![Datemonths](Axis_images/Axis_img65.png)


## Logarithmic Axis

Logarithmic axis uses logarithmic scale and it is very useful in visualizing when the data has values with both lower order of magnitude **(eg: 10<sup>-6</sup>)** and higher order of magnitude **(eg: 10<sup>6</sup>)**. To use logarithmic axis, set the [`valueType`](../api/ejchart#members:primaryxaxis-valuetype) property of the axis to **logarithmic**.  

{% highlight javascript %}

      $("#container").ejChart({
            primaryXAxis: {

                //Use logarithmic scale in primary X axis
                valueType: 'logarithmic',         

                //  ...         
            },
            //  ...
      });


{% endhighlight %}


![Log](Axis_images/Axis_img19.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/logaxis) here to view our online demo sample link for logarithmic axis.

### Customize Logarithmic range

Logarithmic range can be customized by using the [`range`](../api/ejchart#members:primaryxaxis-range) property of the axis to change the [`minimum`](../api/ejchart#members:primaryxaxis-range-minimum), [`maximum`](../api/ejchart#members:primaryxaxis-range-maximum) and [`interval`](../api/ejchart#members:primaryxaxis-range-interval) values. Nice range is calculated automatically based on the provided data, by default.

{% highlight javascript %}

     $("#container").ejChart({
            primaryYAxis: {

                //Customizing logarithmic range
                range: { min: 1, max: 5 },         

                //  ...         
            },
            //  ...
      });

{% endhighlight %}

![LogInterval](Axis_images/Axis_img20.png)

### Logarithmic base

Logarithmic base can be customized by using the [`logBase`](../api/ejchart#members:primaryxaxis-logbase) property of the axis. The default value of the [`logBase`](../api/ejchart#members:primaryxaxis-logbase) is **10**.

{% highlight javascript %}

     $("#container").ejChart({
           primaryYAxis: {

                //Customizing logarithmic base
                logBase: 2,         

                //  ...         
            },
            //  ...
      });

{% endhighlight %}

![Logbase](Axis_images/Axis_img21.png)


### Logarithmic interval

Logarithmic axis interval can be customized by using the [`interval`](../api/ejchart#members:primaryxaxis-range-interval) property of the axis. When the logarithmic base is 10 and logarithmic interval is 2, then the axis labels are placed at an interval of 10<sup>2</sup>. The default value of the interval is 1. 

{% highlight javascript %}

     $("#container").ejChart({
           primaryYAxis: {

                //Customizing logarithmic interval
                range: { interval: 2 },              

                //  ...         
            },
            //  ...
      });

{% endhighlight %}

![Logrange](Axis_images/Axis_img22.png)


## Label Format

### Format numeric labels

Numeric labels can be formatted by using the [`labelFormat`](../api/ejchart#members:primaryxaxis-labelformat) property. Numeric values can be formatted with n (number with decimal points), c (currency) and p (percentage) commands.

{% highlight javascript %}

     $("#container").ejChart({
     
           primaryXAxis: {

                //Applying currency format to axis labels
                labelFormat: 'c',
                //  ...         
            },
            
            //  ...
      });

{% endhighlight %}

![Loglabel](Axis_images/Axis_img23.png)

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


### Format date time values

Date time labels can be formatted by using the [`labelFormat`](../api/ejchart#members:primaryxaxis-labelformat) property of the axis.

{% highlight javascript %}

     $("#container").ejChart({
            primaryXAxis: {

                //Formatting date time labels in date/Month name/Year format
                labelFormat: 'dd/MMMM/yyyy',
                //  …         
            },
            //  ...
     });

{% endhighlight %}

![Labelformat](Axis_images/Axis_img24.png)


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

Prefix and suffix can be added to the category labels by using the [`labelFormat`](../api/ejchart#members:primaryxaxis-labelformat) property. You can use the *{value}* as placeholder text in your custom text, it is replaced with the corresponding axis label at the runtime.

{% highlight javascript %}

$("#container").ejChart({
    primaryXAxis: {
        //...
        //Adding prefix and suffix to axis labels
        labelFormat: '${value} K',                 
    },
    //...
});

{% endhighlight %}

![Customlabel](Axis_images/Axis_img25.png)


## Common axis features

Customization of features such as axis crossing, title, labels, grid lines and tick lines are common to all the axis. Each of these features are explained in this section.


### Axis Crossing

Axis can be positioned anywhere in chart area using the [`crossesAt`](../api/ejchart#members:primaryxaxis-crossesat) property of axis. This property specifies where the horizontal axis should intersect or cross the vertical axis and vice versa. Default value of [`crossesAt`](../api/ejchart#members:primaryxaxis-crossesat) property is null.

{% highlight javascript %}

     $("#container").ejChart({

		primaryXAxis:
		{
			//Crosses primary Y axis at 0
			crossesAt: 0,

			//...
		},	
	});

{% endhighlight %}

![Crosses](Axis_images/Axis_img52.png)


#### Crossing a specific Axis

The [`crossesInAxis`](../api/ejchart#members:primaryxaxis-crossesinaxis) property takes axis name as input and determines the axis used for crossing. By default all the horizontal axes crosses in primary Y axis and all the vertical axes crosses in primary X axis.

{% highlight javascript %}

    $("#container").ejChart({

		primaryXAxis:
		{
			//Crosses vertical axis at -0.2
			crossesAt: -0.2,

			//Crosses in secondary Y axis
			crossesInAxis: 'secondaryYAxis',


			//...
		},	

		//Vertical axis for crossing
		axes: [{
			orientation: 'vertical',
			name: 'secondaryYAxis',

			//...
		}],
	});

{% endhighlight %}

![Axes](Axis_images/Axis_img53.png)

Axis will be placed in the opposite side if value of [`crossesAt`](../api/ejchart#members:primaryxaxis-crossesat) property is greater than the maximum value of crossing axis (axis name provided through [`crossesInAxis`](../api/ejchart#members:primaryxaxis-crossesinaxis) property or primary Y axis for horizontal axis).

{% highlight javascript %}

    $("#container").ejChart({

		primaryXAxis:
		{
			//Crosses primary Y axis at 200
			crossesAt: 200,

			//...
		},	
	});

{% endhighlight %}

![Ycrosses](Axis_images/Axis_img54.png)


#### Crossing in DateTime Axis

For crossing in a date time horizontal axis, date object should be provided as value for [`crossesAt`](../api/ejchart#members:primaryxaxis-crossesat) property of vertical axes.

{% highlight javascript %}

    $("#container").ejChart({

		primaryYAxis:
		{
			//Crosses horizontal axis at 5/29/2010
			crossesAt: new Date(2010, 4, 29),

			//...
		}
		//...
	});

{% endhighlight %}

![Datecrosses](Axis_images/Axis_img55.png)


#### Crossing in Category Axis

For crossing in a category type horizontal axis, either a string object or a number corresponding to the index of category value can be used for [`crossesAt`](../api/ejchart#members:primaryxaxis-crossesat) property of vertical axes.

W> String value provided for [`crossesAt`](../api/ejchart#members:primaryxaxis-crossesat) property is case-sensitive. 


{% highlight javascript %}

    $("#container").ejChart({

		primaryYAxis:
		{
			//Crosses horizontal axis at category value ‘Third’
			crossesAt: 'Tuesday',

			//...
		}
		//...
	});

{% endhighlight %}

![Stringcrosses](Axis_images/Axis_img56.png)

#### Positioning the axis elements while crossing
The [`showNextToAxisLine`](../api/ejchart#members:primaryxaxis-shownexttoaxisline) property is used for controlling the axis elements movement along with the axis line while axis crossing is performed. When the showNextToAxisLine is set as false only the axis line and the tick lines are placed at the crossing Value and the axis elements will be placed outside the chart area. The default value of [`showNextToAxisLine`](../api/ejchart#members:primaryxaxis-shownexttoaxisline) is **true**.  

{% highlight javascript %}

    $("#container").ejChart({

		primaryXAxis:
		{
            //Crosses primary Y axis at 0
			crossesAt: 0,
            showNextToAxisLine:false,
			//...
		}
		//...
	});

{% endhighlight %}

The axis is placed at the crossing value without the axis elements 

![NextAxis](Axis_images/Axis_img67.png)

### Axis Visibility

Axis visibility can be controlled by using the [`visible`](../api/ejchart#members:primaryxaxis-visible) property of the axis. The default value of the [`visible`](../api/ejchart#members:primaryxaxis-visible) property is **true**. 

{% highlight javascript %}

     $("#container").ejChart({

           primaryYAxis: {
                   
                //Disabling visibility of Y-axis
                visible: false

                //  ...         
            },
            //  ...
     });

{% endhighlight %}

![AxisVisibility](Axis_images/Axis_img26.png)


### Axis title

The [`title`](../api/ejchart#members:primaryxaxis-title) property in the axis provides options to customize the [`text`](../api/ejchart#members:primaryxaxis-title-text) and [`font`](../api/ejchart#members:primaryxaxis-title-font) of the axis title. You can customize the [`fontFamily`](../api/ejchart#members:primaryxaxis-title-font-fontfamily), [`fontStyle`](../api/ejchart#members:primaryxaxis-title-font-fontstyle), [`fontWeight`](../api/ejchart#members:primaryxaxis-title-font-fontweight), [`opacity`](../api/ejchart#members:primaryxaxis-title-font-opacity) and [`size`](../api/ejchart#members:primaryxaxis-title-font-size). Axis does not display the title, by default. Title text can also be trimmed using [`enableTrim`](../api/ejchart#members:primaryxaxis-title-enabletrim) based on the [`maximumTitleWidth`](../api/ejchart#members:primaryxaxis-title-maximumtitlewidth) or specified length. Other properties used to customize axis title are [`offset`](../api/ejchart#members:primaryxaxis-title-offset), [`position`](../api/ejchart#members:primaryxaxis-title-position), [`alignment`](../api/ejchart#members:primaryxaxis-title-alignment) and[`visible`](../api/ejchart#members:primaryxaxis-title-visible).

{% highlight javascript %}

     $("#container").ejChart({

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

![Maximumtitle](Axis_images/Axis_img27.png)

You can modify the position of the axis title either inside or outside the chart area using the property [`position`]. By default, it will be placed outside the chart area. In addition, you can also change the alignment of the title to near, far and center by [`alignment`] property, using [`offset`] property you can change the position with respect to pixels.

{% highlight javascript %}

     $("#container").ejChart({

           primaryXAxis: {
                      
                //Customizing axis title
                title : {
                    text : 'Month',
                    position:'inside',
                    alignment:'near',
                    offset: 10
                }
                //  ...         
            },

            //  ...
     });

{% endhighlight %}

![Offset](Axis_images/Axis_img62.png)

### Label customization

The [`font`](../api/ejchart#members:primaryxaxis-font) property of the axis provides options to customize the [`font-style`](../api/ejchart#members:primaryxaxis-font-fontstyle), [`font-family`](../api/ejchart#members:primaryxaxis-font-fontfamily), [`color`](../api/ejchart#members:primaryxaxis-font-color), [`opacity`](../api/ejchart#members:primaryxaxis-font-opacity), [`size`](../api/ejchart#members:primaryxaxis-font-size) and [`font-weight`](../api/ejchart#members:primaryxaxis-font-fontweight) of the axis labels.  

{% highlight javascript %}

     $("#container").ejChart({

          primaryXAxis: {

                //Customizing label appearance
                font : {
                        fontFamily : 'Segoe UI',
                        size : '14px',
                        fontWeight : 'bold',
                        opacity : 0.5,
                        color : 'blue',
                },                
                //  ...         
            },

            //  ...
     });

{% endhighlight %}

![Labelcustom](Axis_images/Axis_img28.png)

#### Axis Labels Line Break

Axis Labels can be placed in multiple lines by specifying **<br>** for data points x value and in label format.

For category value type, **<br>** can be specified in x value of data points.

{% highlight javascript %}

     $("#container").ejChart({
        series: 
			[ 
				{
				    points: [
                             { x: "India", y: 61.3 },                       
                             { x: "United<br>States<br>of<br>America", y: 31 },
                             { x: "South<br>Korea", y: 39.4 },
							 { x: "United<br>Arab<br>Emirates", y: 65.1 },
							 { x: "United<br>Kingdom", y: 75.9 }
                     ]
				}
			],
     });

{% endhighlight %}

![Linebreak](Axis_images/Axis_img68.png)

[JS Playground Sample](http://jsplayground.syncfusion.com/zsaomrq5)

For numeric, datetime and datetimeCategory value type, **<br>** can be specified in labelFormat.

{% highlight javascript %}

     $("#container").ejChart({
        primaryXAxis:
        {
            labelFormat: 'MMM<br>dd<br>yyyy',
            valueType: 'datetime'
        }
     });

{% endhighlight %}

![Format](Axis_images/Axis_img69.png)

[JS Playground Sample](http://jsplayground.syncfusion.com/fllsqowe)

### Label and tick positioning
 
Axis labels and ticks can be positioned inside or outside the chart area by using the [`labelPosition`](../api/ejchart#members:primaryxaxis-labelposition) and [`tickLinesPosition`](../api/ejchart#members:primaryxaxis-ticklinesposition) properties. The labels and ticks are positioned outside the chart area, by default.
 
{% highlight javascript %}

     $("#container").ejChart({

             primaryXAxis: {

                //Customizing label and tick positions
                labelPosition : 'inside',
                tickLinesPosition : 'inside',

                //  ...         
            },
            //  ...
     });

{% endhighlight %}

![Textposition](Axis_images/Axis_img29.png)


### Edge labels placement

Labels with long text at the edges of an axis may appear partially outside the chart. The [`edgeLabelPlacement`](../api/ejchart#members:primaryxaxis-edgelabelplacement) property of primary X axis and [`edgeLabelPlacement`](../api/ejchart#members:primaryyaxis-edgelabelplacement) of primary Y axis can be used to avoid the partial appearance of the labels at the corners. The edge labels of secondary axes can be customized using [`edgeLabelPlacement`](../api/ejchart#members:axes-edgelabelplacement).

{% highlight javascript %}

     $("#container").ejChart({

             primaryXAxis: {

                //Customizing axis edge label placement
                edgeLabelPlacement : 'shift',
                //  ...         
            }
            //  ...
     });

{% endhighlight %}

**Chart before setting edge label placement to X-axis**

![Xaxisplacement](Axis_images/Axis_img30.png)


**Chart after setting edge label placement to X-axis**

![Edgelabel](Axis_images/Axis_img31.png)


### Grid lines customization

The [`majorGridLines`](../api/ejchart#members:primaryxaxis-majorgridlines) and [`minorGridLines`](../api/ejchart#members:primaryxaxis-minorgridlines) properties in the axis are used to customize the major grid lines and minor grid lines of an axis. The majorGridLines provide options to change the [`dashArray`](../api/ejchart#members:primaryxaxis-majorgridlines-dasharray), [`color`](../api/ejchart#members:primaryxaxis-majorgridlines-color), [`opacity`](../api/ejchart#members:primaryxaxis-majorgridlines-opacity), [`visible`](../api/ejchart#members:primaryxaxis-majorgridlines-visible) and [`width`](../api/ejchart#members:primaryxaxis-majorgridlines-width) of the grid lines. The minor grid lines are not [`visible`](../api/ejchart#members:primaryxaxis-minorgridlines-visible), by default. The minorGridLines provide options to change [`dashArray`](../api/ejchart#members:primaryxaxis-minorgridlines-dasharray) and [`width`](../api/ejchart#members:primaryxaxis-minorgridlines-width). 

{% highlight javascript %}

     $("#container").ejChart({

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

![Gridline](Axis_images/Axis_img32.png)


### Tick lines customization

The [`majorTickLines`](../api/ejchart#members:primaryxaxis-majorticklines) and [`minorTickLines`](../api/ejchart#members:primaryxaxis-minorticklines) properties in the axis are used to customize the major tick lines of an axis and minor tick lines of an axis. The majorTickLines provide options to change the [`size`](../api/ejchart#members:primaryxaxis-majorticklines-size), visibility using [`visible`](../api/ejchart#members:primaryxaxis-majorticklines-visible) property and [`width`](../api/ejchart#members:primaryxaxis-majorticklines-width) of the tick lines. The minor tick lines are not [`visible`](../api/ejchart#members:primaryxaxis-minorticklines-visible) , by default. The majorTickLines provide options to change [`size`](../api/ejchart#members:primaryxaxis-minorticklines-size) and [`width`](../api/ejchart#members:primaryxaxis-minorticklines-width) of the tick lines. The [`minorTicksPerInterval`](../api/ejchart#members:primaryxaxis-minorticksperinterval) specifies the number of minor ticks per interval

{% highlight javascript %}

     $("#container").ejChart({

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

![Tickline](Axis_images/Axis_img33.png)

  
### Inversing axis

Axis can be inversed by using the [`isInversed`](../api/ejchart#members:primaryxaxis-isinversed) property of the axis. The default value of the [`isInversed`](../api/ejchart#members:primaryxaxis-isinversed) property is **false**.

{% highlight javascript %}

     $("#container").ejChart({

           primaryXAxis: {

                //Inversing the X-axis
                isInversed: false

                //  ...         
            },
            //  ...
     });

{% endhighlight %}

**Chart before inversing the axes**

![BeforeInversed](Axis_images/Axis_img34.png)


**Chart after inversing the axes**

![Afterinversed](Axis_images/Axis_img35.png)

   

### Place axes at the opposite side

The [`opposedPosition`](../api/ejchart#members:primaryxaxis-opposedposition) property of axis can be used to place the axis at the opposite side of its default position. The default value of the [`opposedPosition`](../api/ejchart#members:primaryxaxis-opposedposition) property is **false**. 

{% highlight javascript %}

     $("#container").ejChart({

            primaryXAxis: {

                //Placing axis at the opposite side of its normal position
                opposedPosition: true

                //  ...         
            },
            //  ...
     });

{% endhighlight %}

**Chart with X and Y axes at normal position**

![Normalposition](Axis_images/Axis_img36.png)


**Chart with Y-axis at opposed position**

![Opposed](Axis_images/Axis_img37.png)


### Maximum number of labels per 100 pixels

A maximum of 3 labels are displayed for each 100 pixels in the axis, by default. The maximum number of labels that is present within the 100 pixels length can be customized by using the [`maximumLabels`](../api/ejchart#members:primaryxaxis-maximumlabels) property of the axis. This property is applicable only for an automatic range calculation and it does not work when you set the value for [`interval`](../api/ejchart#members:primaryxaxis-range-interval) property in the axis range.

{% highlight javascript %}

     $("#container").ejChart({

         primaryXAxis: {

                //Maximum number of labels per 100 pixels
                maximumLabels : 1

                //  ...        
            },
            //  ...
     });

{% endhighlight %}

**Chart before setting maximum labels per 100 pixels**

![Maxlabelbefore](Axis_images/Axis_img38.png)


**Chart after setting maximum labels one per 100 pixels**

![Maxlabelafter](Axis_images/Axis_img39.png)

### Alternate Grid Band

The [`alternateGridBand`](../api/ejchart#members:primaryxaxis-alternategridband) property is used to customize the axis grid band. Alternate grid bands contains two properties such as [`odd`](../api/ejchart#members:primaryxaxis-alternategridband-odd) and [`even`](../api/ejchart#members:primaryxaxis-alternategridband-even) grid bands. You can change the [`opacity`](../api/ejchart#members:primaryxaxis-alternategridband-odd-opacity) and [`fill`](../api/ejchart#members:primaryxaxis-alternategridband-odd-fill) color of odd, [`opacity`](../api/ejchart#members:primaryxaxis-alternategridband-even-opacity) and [`fill`](../api/ejchart#members:primaryxaxis-alternategridband-even-fill) color of even grid bands for axis. 

{% highlight javascript %}

$("#container").ejChart({

    primaryXAxis: { 
        alternateGridBand: { 
            even :{ fill : "green",  opacity : 0.4 } ,
            odd : { fill : "red" , opacity : 0.8}
        } 
    }
});

{% endhighlight %}

### Axis Line

You can customize the [`color`](../api/ejchart#members:primaryxaxis-axisline-color), [`dashArray`](../api/ejchart#members:primaryxaxis-axisline-dasharray), [`offset`](../api/ejchart#members:primaryxaxis-axisline-offset), [`visible`](../api/ejchart#members:primaryxaxis-axisline-visible) and [`width`](../api/ejchart#members:primaryxaxis-axisline-width) using [`axisLine`](../api/ejchart#members:primaryxaxis-axisline) property. 

{% highlight javascript %}

$("#container").ejChart({
   primaryXAxis: { 
       axisLine : {
            color : "red", 
            dashArray : "2,3", 
            offset : 5, 
            visible : false, 
            width : 2 
        } 
    }   
});

{% endhighlight %}

### Column Index and Span

[`columnIndex`](../api/ejchart#members:primaryxaxis-columnindex) property specifies the index of the column where the axis is associated, when the chart area is divided into multiple plot areas by using columnDefinitions. The [`columnSpan`](../api/ejchart#members:primaryxaxis-columnspan) specifies number of columns or plot areas an axis has to span horizontally.

{% highlight javascript %}

$("#container").ejChart({
   primaryXAxis: { 
       columnIndex: 2,
       columnSpan: 2
   }                       
});

{% endhighlight %}

### Crosshair Label

The primary X axis provides an option to customize the [`crosshairLabel`](../api/ejchart#members:primaryxaxis-crosshairlabel). The [`visible`](../api/ejchart#members:primaryxaxis-crosshairlabel-visible) property of horizontal axis shows or hides the crosshair label.

{% highlight javascript %}

$("#container").ejChart({
  primaryXAxis: { 
      crosshairLabel : { 
          visible : true
      } 
  }
});

{% endhighlight %}

### Desired Intervals, Auto Zooming and Trimming

By setting [`desiredIntervals`](../api/ejchart#members:primaryxaxis-desiredintervals), you can request axis to calculate intervals approximately equal to your desired interval. The [`enableTrim`](../api/ejchart#members:primaryxaxis-enabletrim) of axis specifies whether to trim the axis label when the width of the label exceeds the [`maximumLabelWidth`](../api/ejchart#members:primaryxaxis-maximumlabelwidth). The [`enableAutoIntervalOnZooming`](../api/ejchart#members:primaryxaxis-enableautointervalonzooming) specifies the interval of axis according to the zoomed data of the chart. 

{% highlight javascript %}

$("#container").ejChart({
  primaryXAxis: { 
      desiredIntervals: 5, 
      enableTrim : true, 
      enableAutoIntervalOnZooming: true, 
      maximumLabelWidth : 34.5 
      }  
});

{% endhighlight %}

### Axis Alignment and Label Rotation

The [`alignment`](../api/ejchart#members:primaryxaxis-alignment) property is used to position axis labels. Axis Labels can be rotated by specifying angles in degrees using [`labelRotation`](../api/ejchart#members:primaryxaxis-labelrotation) property.

{% highlight javascript %}

$("#container").ejChart({
    primaryXAxis: {
        alignment : "far" ,
        labelRotation : 90
    }  
});

{% endhighlight %}

### Axis Label Text Anchor

ejChart provides an option to align the rotated x axis labels. The rotateOn property is used to rotate the labels from different positions. It takes string value as input. This property only works when [`labelRotation`](../api/ejchart#members:primaryxaxis-labelrotation) is available. The following code snippet illustrates an example,

{% highlight javascript %}

$("#container").ejChart({
    primaryXAxis: {
        labelRotation : 45,
        rotateOn: 'end'
    }  
});

{% endhighlight %}

### Axis Name, Orientation and Plot Offset

Unique name of the axis. To associate an axis with the series, you have to set this [`name`](../api/ejchart#members:primaryxaxis-name) to the xAxisName/yAxisName property of the series. The [`orientation`](../api/ejchart#members:primaryxaxis-orientation) property is used to specify the orientation of the axis line. The [`plotOffset`](../api/ejchart#members:primaryxaxis-plotoffset) is used to specify padding for plot area.

{% highlight javascript %}

$("#container").ejChart({

    primaryXAxis: { 
        name: "xAxis" ,
        orientation : 'Vertical',
        plotOffset: 0
    }                          
});

{% endhighlight %}

### StripLine Customization

Axis [`stripLine`](../api/ejchart#members:primaryxaxis-stripline) can be customized using attributes such as [`borderColor`](../api/ejchart#members:primaryxaxis-stripline-bordercolor), [`color`](../api/ejchart#members:primaryxaxis-stripline-color), [`end`](../api/ejchart#members:primaryxaxis-stripline-end), [`font`](../api/ejchart#members:primaryxaxis-stripline-font) [`color`](../api/ejchart#members:primaryxaxis-stripline-font-color), [`fontFamily`](../api/ejchart#members:primaryxaxis-stripline-font-fontfamily), [`fontStyle`](../api/ejchart#members:primaryxaxis-stripline-font-fontstyle), [`fontWeight`](../api/ejchart#members:primaryxaxis-stripline-font-fontweight), [`opacity`](../api/ejchart#members:primaryxaxis-stripline-font-opacity), [`size`](../api/ejchart#members:primaryxaxis-stripline-font-size), [`start`](../api/ejchart#members:primaryxaxis-stripline-start), [`startFromAxis`](../api/ejchart#members:primaryxaxis-stripline-startfromaxis), [`text`](../api/ejchart#members:primaryxaxis-stripline-text), [`textAlignment`](../api/ejchart#members:primaryxaxis-stripline-textalignment), [`visible`](../api/ejchart#members:primaryxaxis-stripline-visible), [`width`](../api/ejchart#members:primaryxaxis-stripline-width) and [`zIndex`](../api/ejchart#members:primaryxaxis-stripline-zindex).

{% highlight javascript %}

$("#container").ejChart({

    primaryXAxis: { 
        stripLine:[{ 
            borderColor: "green" ,
            color: "green",
            end: 5,
            font: {
                color: "green",
                fontFamily : "Algerian",
                fontStyle: "Bold",
                fontWeight: "lighter",
                opacity: 0.5,
                size: "15px"
            },
            start: 2,
            startFromAxis : true,
            text : "Empty Point",
            textAlignment : "middletop",
            visible : true,
            width : 0,
            zIndex: "behind"
        }]
    }                          
});

{% endhighlight %}

### Axis Label border

The borders of axis label can be customized using [`labelBorder`](../api/ejchart#members:primaryxaxis-labelborder). You can change the color and width of the axis label border using [`color`](../api/ejchart#members:primaryxaxis-labelborder-color) and [`width`](../api/ejchart#members:primaryxaxis-labelborder-width) property.

{% highlight javascript %}

$("#container").ejChart({

    primaryXAxis: { 
       labelBorder:{
           color: "green",
           width: 2
       }
    }                          
});

{% endhighlight %}

### ZoomFactor and ZoomPosition

The axis is scaled by [`zoomFactor`](../api/ejchart#members:primaryxaxis-zoomfactor). When zoomFactor is 0.5, the chart is scaled by 200% along this axis. Value of zoom factor ranges from 0 to 1. Position of the zoomed axis is specified by [`zoomPosition`](../api/ejchart#members:primaryxaxis-zoomposition). Value of zoom position ranges from 0 to 1.

{% highlight javascript %}

$("#container").ejChart({
    primaryXAxis: { 
        zoomFactor : 0.5,
        zoomPosition :0.5
    }                
});

{% endhighlight %}

### Axis Scrollbar

The [`scrollbarSettings`](../api/ejchart#members:primaryxaxis-scrollbarsettings) provides options to customize the axis scrollbar. The [`visible`](../api/ejchart#members:primaryxaxis-scrollbarsettings-visible) property of scrollbar enables or disables the scrollbar. The [`canResize`](../api/ejchart#members:primaryxaxis-scrollbarsettings-canresize) controls whether axis scrollbar is responsive in chart. The scrollbar [`range`](../api/ejchart#members:primaryxaxis-scrollbarsettings-range) can customized using range [`min`](../api/ejchart#members:primaryxaxis-scrollbarsettings-range-min) and [`max`](../api/ejchart#members:primaryxaxis-scrollbarsettings-range-max). The [`pointsLength`](../api/ejchart#members:primaryxaxis-scrollbarsettings-pointslength) is used to display maximum number of points in scrollbar.

{% highlight javascript %}

$("#container").ejChart({
    primaryXAxis: { 
       scrollbarSettings:{
           visible:true,
           canResize:true,
           range : { 
               min: 10,
               max: 100
           },
           pointsLength : 50
        }
    }                
});

{% endhighlight %}


## Multiple Axis

Multiple axes can be used in the Chart and chart area can be split into multiple panes to draw multiple series with multiple axes.

![Multipleimage1](Axis_images/Axis_img40.png)

An additional horizontal or vertical axis can be added to the chart by adding an axis instance to the **axes** collection and then you can associate it to a series by specifying the name of the axis to the [`xAxisName`](../api/ejchart#members:series-xaxisname) or [`yAxisName`](../api/ejchart#members:series-yaxisname) property of the series.

{% highlight javascript %}

        $("#container").ejChart({
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



![Multipleimage2](Axis_images/Axis_img41.png)

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/multipleaxes) here to view the multiple axis online demo sample.


## Smart Axis Labels

When the Axis labels overlap with each other based on the chart dimensions and label size, you can use the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) property of the axis to avoid overlapping. The default value of the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) is **none**. The other available values of the Label Intersect Actions are **rotate45**, **rotate90**, **trim**, **multipleRows**, **wrap**, **wrapByWord** and **hide**.

{% highlight javascript %}

       $("#container").ejChart({

            // Avoid overlapping of x-axis labels
            primaryXAxis: {
                labelIntersectAction : 'multipleRows',
                 //  ...
            },
            
            // ...
        });


{% endhighlight %}



![Smartaxis](Axis_images/Axis_img42.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/smartaxislabels) here to view our online demo sample for smart axis labels.



The following screenshot displays the result, when the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) property is set as **rotate45**.

![Labelintersect45](Axis_images/Axis_img43.png)


The following screenshot displays the result, when the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) property is set as **rotate90**.

![Labelintersect90](Axis_images/Axis_img44.png)


The following screenshot displays the result, when the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) property is set as **wrap**.

![Labelintersectwrap](Axis_images/Axis_img45.png)


The following screenshot displays the result, when of setting the **trim** as value to the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) property.

![Labelintersecttrim](Axis_images/Axis_img46.png)


The following screenshot displays the result, when the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) property is set as **hide**.

![Labelintersecthide](Axis_images/Axis_img47.png)


The following screenshot displays the result, when the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) property is set as **multipleRows **.

![Labelintersectmultiple](Axis_images/Axis_img48.png)


The following screenshot displays the result, when the [`labelIntersectAction`](../api/ejchart#members:primaryxaxis-labelintersectaction) property is set as **wrapByWord**.

![Labelintersectword](Axis_images/Axis_img49.png)

## Multi-level Labels
Axis can be customized with multiple levels of labels using the [`multiLevelLabels`](../api/ejchart#members:primaryxaxis-multilevellabels) property. These labels are placed based on the [`start`](../api/ejchart#members:primaryxaxis-multilevellabels-start) and [`end`](../api/ejchart#members:primaryxaxis-multilevellabels-end) range values and we can add any number of labels to an axis. You can customize the [`text`](../api/ejchart#members:primaryxaxis-multilevellabels-text) for each level, visibility of multi level label by [`visible`](../api/ejchart#members:primaryxaxis-multilevellabels-visible) property, alignment of text using [`textAlignment`](../api/ejchart#members:primaryxaxis-multilevellabels-textalignment), [`level`](../api/ejchart#members:primaryxaxis-multilevellabels-level) of multi level labels, [`maximumTextWidth`](../api/ejchart#members:primaryxaxis-multilevellabels-maximumtextwidth) of multi level label text, overflow of text using [`textOverflow`](../api/ejchart#members:primaryxaxis-multilevellabels-textoverflow), [`font`](../api/ejchart#members:primaryxaxis-multilevellabels-font) [`color`](../api/ejchart#members:primaryxaxis-multilevellabels-font-color), [`fontFamily`](../api/ejchart#members:primaryxaxis-multilevellabels-font-fontfamily), [`fontStyle`](../api/ejchart#members:primaryxaxis-multilevellabels-font-fontstyle), [`fontWeight`](../api/ejchart#members:primaryxaxis-multilevellabels-font-fontweight), [`opacity`](../api/ejchart#members:primaryxaxis-multilevellabels-font-opacity), [`size`](../api/ejchart#members:primaryxaxis-multilevellabels-font-size), [`border`](../api/ejchart#members:primaryxaxis-multilevellabels-border) [`color`](../api/ejchart#members:primaryxaxis-multilevellabels-border-color), [`width`](../api/ejchart#members:primaryxaxis-multilevellabels-border-width) and [`type`](../api/ejchart#members:primaryxaxis-multilevellabels-border-type) of labels.

{% highlight javascript %}       

         $("#container").ejChart(
            {
                primaryXAxis:
                {
                    multiLevelLabels: [
                        { 
                            visible: true,
                            start: -0.5,
                            end: 2.5
                         }]
                    }    
             });  

{% endhighlight %}

![Multi-level](Axis_images/Axis_img57.png)

### Customizing the multi-Level labels
The color, width and type of the border can be customized. The default border type is [`Rectangle`]. And the other supported border types are namely brace, curly brace, without top/bottom border and none. 

{% highlight javascript %}

        $("#container").ejChart(
            {
                primaryXAxis:
                {
                    multiLevelLabels: [
                        { 
                           // customizing the border properties 
                            border:{
                                type: "brace",
                                width: 2,
                                color: "black"
                           }
                         }]
                    }    
             });  

{% endhighlight %}

![Multi-levelcustom](Axis_images/Axis_img58.png)

The text of the labels can be customized using the [`text`] and [`font`] properties 

{% highlight javascript %}

         $("#container").ejChart(
            {
                primaryXAxis:
                {
                    multiLevelLabels: [
                        { 
                           // customizing the text and font properties
                            text: "Year - 2015",
                            font:{
                               fontFamily: "Algerian", 
                               size: "12px",
                               color: "black"                            
                              }
                         }]
                    }    
             });        

{% endhighlight %}

![Multi-levelfont](Axis_images/Axis_img59.png)

You can change the alignment of the text to far, near and center position using the [`textAlignment`] property. By default, the text will be center aligned. 

{% highlight javascript %}

        $("#container").ejChart(
            {
                primaryXAxis:
                {
                    multiLevelLabels: [
                        { 
                          // customizing the text alignment
                            textAlignment: "far",
                         }]
                    }    
             });          

{% endhighlight %}

![Multi-levelalignment](Axis_images/Axis_img60.png)

You can trim, wrap or wrapAndTrim the text if it exceeds the maximum text width value using the property [`textOverflow`]

{% highlight javascript %}

        $("#container").ejChart(
            {
                primaryXAxis:
                {
                    multiLevelLabels: [
                        { 
                          // customizing the text overflow  
                            textOverflow: “trim", 
                            maximumTextWidth: 40                                                                   
                      }]
                     }  
              });            

{% endhighlight %}

The below screenshot shows the trimmed multi-level labels

![Multi-leveltrim](Axis_images/Axis_img61.png)

And these labels can be placed in various rows using the [`level`] property.
[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/chart/chartaxes/multi-levellabels) here to view the multi-level labels online demo sample.
