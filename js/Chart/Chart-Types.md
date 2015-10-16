---
layout: post
title: Chart-Types
description: chart types
platform: js
control: Chart
documentation: ug
---

# ChartTypes

## Line Chart

To render a Line Chart, set the series [type](../api/ejchart.html#members:series-type) as **"line"** in the chart series. To change the line segment color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
              // ...
            series: [{
                //Change type and color of the series.
                 type: 'line',         
                 fill: "#E94649",
               // ...         
            }],
              // ...
       });

{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img1.png)

Line Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/line) here to view the Line Chart online demo sample.


### Change the line width

To change the width of the line segment, you can use the [width](../api/ejchart.html#members:series-width) property in the series.

{% highlight js %}


       $("#chartcontainer").ejChart({
            //...
            series: [{
                //Change the width of line series
                 width: 3,         
               // ...       
            }],
            //...
       });

{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img2.png)

Changing the line width
{:.caption}


### Dashed lines

To render the line series with dotted lines, you can use the [dashArray](../api/ejchart.html#members:series-dasharray) option of the series.

{% highlight js %}

      $("#chartcontainer").ejChart({
            // ...
            series: [{
                 //Change dash array to display dotted or dashed lines
                 dashArray: '5,5',         
                 // ...         
            }],
            // ...
     });

{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img3.png)

Line series with dashed lines
{:.caption}



### Changing the line cap

For customizing the start and end caps of the line segment, you can use the [lineCap](../api/ejchart.html#members:series-linecap) property.  

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...
            series: [{
                 //Change line cap
                 lineCap: 'square',         
                 // ...         
            }],
            // ...
       });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img4.png)

Changin line cap
{:.caption}


### Changing the line join

You can use the [lineJoin](../api/ejchart.html#members:series-linejoin) property to specify how two intersecting line segments should be joined.

{% highlight js %}


       $("#chartcontainer").ejChart({
            //...
            series: [{
                 //Change line join
                 lineJoin: 'round',         
                 //...         
            }],
            //...
       });


{% endhighlight %}


![](/js/Chart/Chart-Types_images/Chart-Types_img5.png)

Changing the line join
{:.caption}


## Step Line Chart

To render a Step Line Chart, set the series [type](../api/ejchart.html#members:series-type) as **"stepline"** in the chart series. To change the StepLine segment color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
              // ...
            series: [{
                //Change type and color of the series.
                 type: 'line',         
                 fill: "#E94649",
               // ...         
            }],
              // ...
       });

{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img6.png)

Step Line Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/stepline) here to view the Step Line Chart online demo sample.


### Changing the line width

To change the line width, you can use the **width** property.  

{% highlight js %}


       $("#chartcontainer").ejChart({
            //...
            series: [{
                //Change the width of step line series
                 width: 3,         
               // ...       
            }],
            //...
       });

{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img7.png)

Changing the step line width
{:.caption}


### Dashed lines

To render the step line series with dotted lines, you can use the [dashArray](../api/ejchart.html#members:series-dasharray) option of the series.

{% highlight js %}

      $("#chartcontainer").ejChart({
            // ...
            series: [{
                 //Change dash array to display dotted or dashed lines
                 dashArray: '5,5',         
                 // ...         
            }],
            // ...
     });

{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img8.png)

Step Line series with dashed lines
{:.caption}



### Changing the line cap

For customizing the start and end caps of the line segment, you can use the [lineCap](../api/ejchart.html#members:series-linecap) property.  

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...
            series: [{
                 //Change line cap
                 lineCap: 'square',         
                 // ...         
            }],
            // ...
       });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img9.png)

Changin line cap
{:.caption}


### Changing the line join

You can use the [lineJoin](../api/ejchart.html#members:series-linejoin) property to specify how two intersecting line segments should be joined.

{% highlight js %}


       $("#chartcontainer").ejChart({
            //...
            series: [{
                 //Change line join
                 lineJoin: 'round',         
                 //...         
            }],
            //...
       });


{% endhighlight %}


![](/js/Chart/Chart-Types_images/Chart-Types_img10.png)

Changing the line join
{:.caption}


## Area Chart

To render an Area chart, you can specify the series [type](../api/ejchart.html#members:series-type) as **“area”** in the chart series. To change the Area color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
              
            //   ...
            series: [{
                // Change the series type and fill color
                type: 'area',         
                fill: '#69D2E7'
                // ...        
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img11.png)

Area Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/area) here to view the Area Chart online demo.


## Range Area Chart

To render a Range Area Chart, set the [type](../api/ejchart.html#members:series-type) as **"rangeArea"** in the chart series. To change the RangeArea color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

Since the RangeArea series requires two y values for a point, you have to add the [high](../api/ejchart.html#members:series-high) and [low](../api/ejchart.html#members:series-low) value. High and Low value specifies the maximum and minimum range of the points.

* When you are using the [points](../api/ejchart.html#members:series-points) option, specify the high and low values by using the [high](../api/ejchart.html#members:series-points-high) and [low](../api/ejchart.html#members:series-points-low) option of the point.

* When you are using the [dataSource](../api/ejchart.html#members:series-datasource) option to assign the data, map the fields from the dataSource that contain high and low values by using the [series.high](../api/ejchart.html#members:series-high) and [series.low](../api/ejchart.html#members:series-low) options. 

{% highlight js %}


        $("#chartcontainer").ejChart({
        
             //  ...
             series: [{
                //Change the series type and fill color
                type: 'rangeArea', 
                fill: "Indigo",

                //Use high and low values instead of y
                points:[{ x: 1935, high:80, low:70 },
                    //  ...
                ],
                //  ...         
            }],

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img12.png)

RangeArea Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/rangearea) here to view our Range Area Chart online demo.


## Step Area Chart

To render a Step Area Chart, set the [type](../api/ejchart.html#members:series-type) as **"stepArea"** in the chart series. To change the StepArea color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...
             series: [{
               // Change the series type and fill color
               type: 'stepArea',      
               fill: " #69D2E7",   
               //  ...         
            }],
            // ...

        });  


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img13.png)

StepArea Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/steparea) here to view our Step Area Chart online demo.


## Spline Area Chart

To render a Spline Area Chart, set the [type](../api/ejchart.html#members:series-type) as **"splineArea"** in the chart series. To change the SplineArea color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}

 
        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                 // Change the series type and fill color
                 type: 'splineArea',         
                 fill: "#C4C24A",   
                 //  ...         
            }],
            
            //...
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img14.png)

SplineArea Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/splinearea) here to view our Spline Area Chart online demo.


## Stacked Area Chart

To render a Stacked Area Chart, set the [type](../api/ejchart.html#members:series-type) as **"stackingArea"** in the chart series. To change the StackingArea color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
             // ...
             series: [{
                 //Change series type and fill color
                 type: 'stackingArea',      
                 fill: "#69D2E7",      
                 //  ...         
            }],

            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img15.png)

Stacked Area Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/stackedarea) here to view our Stacked Area Chart online demo.


## 100% Stacked Area Chart  

To render a 100% Stacked Area Chart, set the [type](../api/ejchart.html#members:series-type) as **"stackingArea100"** in the chart series. To change the StackingArea100 color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.   

{% highlight js %}


        $("#chartcontainer").ejChart({
        
           //  ...        
            series: [{
                 //Change type and fill color of the series
                 type: 'stackingArea100',         
                 fill: "#C4C24A",      
                 //  ...       
            }],
           //  ...
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img16.png)

100% Stacked Area Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/stackedarea) here to view our 100% Stacked Area Chart online demo.


## Column Chart

To render a Column Chart, set the [type](../api/ejchart.html#members:series-type) as **"column"** in the chart series. To change the color of the column series, you can use the [fill](../api/ejchart.html#members:series-fill) property.  

{% highlight js %}


        $("#chartcontainer").ejChart({
            //   ...
            series: [{
                //Change type and fill color of the series
                 type: 'column',     
                 fill: "#E94649",
               //  ...         
            }],
            
            //    ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img17.png)

Column Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/column) here to view our Column Chart demo.


### Change a point color

You can change the color of a column by using the [fill](../api/ejchart.html#members:series-points-fill) property of the point.

{% highlight js %}


        $("#chartcontainer").ejChart({
            //   ...
            series: [{
               //  Change the color of a column
                points:[{ fill: 'skyblue' },
                       //  ...         
                ],
               //  ...         
            }],
            
            //    ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img18.png)

Change the color of a column
{:.caption}


## RangeColumn Chart

To render a Range Column Chart, set the [type](../api/ejchart.html#members:series-type) as **"rangeColumn"** in the chart series. To change the RangeColumn color, use the [fill](../api/ejchart.html#members:series-fill) property of the series.

Since, the RangeColumn series requires two y values for a point, add the [high](../api/ejchart.html#members:series-high) and [low](../api/ejchart.html#members:series-low) value. High and Low value specifies the maximum and minimum range of the points.

* When you are using the [points](../api/ejchart.html#members:series-points) option, specify the high and low values by using the [high](../api/ejchart.html#members:series-points-high) and [low](../api/ejchart.html#members:series-points-low) option of the point.

* When you are using the [dataSource](../api/ejchart.html#members:series-datasource) option to assign the data, you have to map the fields from the dataSource that contains high and low values by using the [series.high](../api/ejchart.html#members:series-high) and [series.low](../api/ejchart.html#members:series-low) options.  

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            
            series: [{
                //Set chart type to series
                 type: 'rangeColumn',        
                 fill: "#E94649",
                //Use high and low values instead of y
                points:[{ high: 6.1, low:0.7 },
                    //  ...         
                ],
               //  ...         
            }],
            //  ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img19.png)

Range Column Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/rangecolumn) here to view our Range Column Chart online demo.


### Change a point color 

To change the color of a range column, you can use the [fill](../api/ejchart.html#members:series-points-fill) property of point. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            //   ...
            series: [{
               //  Change the color of a range column
                points:[{ fill: 'skyblue' },
                       //  ...         
                ],
               //  ...         
            }],
            
            //    ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img20.png)

Change the color of a range column
{:.caption}


## Stacked Column Chart

To render a Stacked Column Chart, set the [type](../api/ejchart.html#members:series-type) as **"stackingColumn"** in the chart series. To change the StackingColumn color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
            
            // ...
            
            series: [{
                //Change type and color of the series
                type: 'stackingColumn',       
                 fill: "#E94649",  
                //  ...         
            }],
            //  ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img21.png)

Stacked Column Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/stackedcolumn) here to view our Stacked Column Chart online demo.


### Group stacked columns

You can use the [stackingGroup](../api/ejchart.html#members:series-stackinggroup) property to group the stacked columns. Columns with same group name are stacked on top of each other.

{% highlight js %}


        $("#chartcontainer").ejChart({
            
            // ...
            
            series: [{
                // For grouping stacked columns
                stackingGroup: 'GroupOne'
                //  ...        
            }, 
            {
                // For grouping stacked columns
                stackingGroup: 'GroupOne'
                //  ...         
            }],
            //  ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img22.png)

grouping stacked columns
{:.caption}


### Change a point color

To change the color of a stacking column, you can use the [fill](../api/ejchart.html#members:series-points-fill) property of the point. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            //   ...
            series: [{
               //  Change the color of a stacking column
                points:[{ fill: 'skyblue' },
                       //  ...         
                ],
               //  ...         
            }],            
            //    ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img23.png)

Change the color of a stacked column
{:.caption}

 

## 100% Stacked Column Chart    

To render a 100% Stacked Column Chart, set the [type](../api/ejchart.html#members:series-type) as **"stackingColumn100"** in the chart series. To change the StackingColumn100 color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}

        $("#chartcontainer").ejChart({             
            // ...
             
            series: [{
                //Change type and color of the series
                type: 'stackingColumn100',         
                 fill: "#E94649",  
                //  .......         
            }],
           // ...
           
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img24.png)

100% Stacking column chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/100%stackedcolumn) here to view our 100% Stacked Column Chart online demo.


### Group 100% stacked columns

By using the [stackingGroup](../api/ejchart.html#members:series-stackinggroup) property, you can group the 100% stacking columns. Columns with same group name are stacked on top of each other. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            
            // ...
            
            series: [{
                // For grouping 100% stacked columns
                stackingGroup: 'GroupOne'
                //  ...        
            }, 
            {
                // For grouping 100% stacked columns
                stackingGroup: 'GroupOne'
                //  ...         
            }],
            //  ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img25.png)

grouping 100% stacked columns
{:.caption}


### Change a point color

To change the color of a 100% stacking column, you can use the [fill](../api/ejchart.html#members:series-points-fill) property of the point. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            //   ...
            series: [{
               //  Change the color of a 100% stacking column
                points:[{ fill: 'skyblue' },
                       //  ...         
                ],
               //  ...         
            }],
            
            //    ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img26.png)

Change the color of a 100% stacked column
{:.caption}


## Bar Chart

To render a bar Chart, set the [type](../api/ejchart.html#members:series-type) as **"bar"** in the chart series. To change the bar color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
            //  ...
            series: [{
                //Change type and color of the series
                type: 'bar',         
                 fill: "#E94649",  
                //  ...         
            }],
            //  ...

        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img27.png)

Bar Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/bar) here to view our Bar Chart demo.


### Change the color of a bar

By using the [fill](../api/ejchart.html#members:series-points-fill) property of the point, you can change the specific point of the series. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            //   ...
            series: [{
               //  Change the color of a bar
                points:[{ fill: 'skyblue' },
                       //  ...         
                ],
               //  ...         
            }],
            
            //    ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img28.png)

Change the color of a bar
{:.caption}


## Stacked Bar Chart

To render a Stacked Bar Chart, set the [type](../api/ejchart.html#members:series-type) as **"stackingBar"** in the chart series. To change the StackingBar color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
            //   ...
            series: [{
                //Change type and color of the series.
                type: 'stackingBar',         
                 fill: "#E94649",  
                //  ...         
            }],
            // ...

        });          


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img29.png)

Stacked Bar Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/stackedbar) here to view our Stacked Bar Chart online demo.


### Group stacked bars

You can use the [stackingGroup](../api/ejchart.html#members:series-stackinggroup) property to group the stacking bars with the same group name. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            
            // ...
            
            series: [{
                // For grouping stacked bar
                stackingGroup: 'GroupOne'
                //  ...        
            }, 
            {
                // For grouping stacked bar
                stackingGroup: 'GroupOne'
                //  ...         
            }],
            //  ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img30.png)

grouping stacked bar
{:.caption}


### Change a point color

You can change the color of a stacking bar by using the [fill](../api/ejchart.html#members:series-points-fill) property of the point.

{% highlight js %}

        $("#chartcontainer").ejChart({
            //   ...
            series: [{
               //  Change the color of a stacking bar
                points:[{ fill: 'skyblue' },
                       //  ...         
                ],
               //  ...         
            }],            
            //    ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img31.png)

Change the color of a stacked bar
{:.caption}


## 100% Stacked Bar Chart

To render a 100% Stacked Bar Chart, set the [type](../api/ejchart.html#members:series-type) as **"stackingBar100"** in the chart series. To change the StackingBar100 color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
           // ...
           series: [{
                //Change type and color of the series.
                type: 'stackingBar100',     
                 fill: "#E94649",      
                //  ...         
            }],
           // ...
        });   


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img32.png)

100% Stacked Bar Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/100%stackedbar) here to view our 100% Stacked Bar Chart online demo.

By using the [stackingGroup](../api/ejchart.html#members:series-stackinggroup) property, you can group the 100% stacking bars with the same group name. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            
            // ...
            
            series: [{
                // For grouping 100% stacked bar
                stackingGroup: 'GroupOne'
                //  ...        
            }, 
            {
                // For grouping 100% stacked bar
                stackingGroup: 'GroupOne'
                //  ...         
            }],
            //  ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img33.png)

grouping 100% stacked bar
{:.caption}


### Change a point color

To change the color of a 100% stacking bar, you can use the [fill](../api/ejchart.html#members:series-points-fill) property of the point. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            //   ...
            series: [{
               //  Change the color of a 100% stacking bar
                points:[{ fill: 'skyblue' },
                       //  ...         
                ],
               //  ...         
            }],            
            //    ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img34.png)

Change the color of a 100% stacked bar
{:.caption}


## Spline Chart

To render a Spline Chart, set the [type](../api/ejchart.html#members:series-type) as **"spline"** in the chart series. To change the Spline segment color, you can use the [fill](../api/ejchart.html#members:series-fill) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
                //Change type and color of the series.
                type: 'spline',         
                 fill: "#6ADCB0",     
                //  ...         
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img35.png)

Spline Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/spline) here to view the Spline Chart online demo sample.


### Change the spline width

To change the spline segment width, you can use the [width](../api/ejchart.html#members:series-width) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
                //Change the width of spline series
                 width: 3,         
               // ...       
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img36.png)

Changing the spline width
{:.caption}


### Dashed lines

To render the spline series with dotted lines, you can use the [dashArray](../api/ejchart.html#members:series-dasharray) option of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
                 //Change dash array to display dotted or dashed splines
                 dashArray: '5,5',           
               // ...       
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img37.png)

Spline chart with dashed lines
{:.caption}


## Pie Chart

You can create a pie chart by setting the series [type](../api/ejchart.html#members:series-type) as **"pie"** in the chart series.


{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
                //Set chart type to series
                 type: 'pie',         
               //  ...         
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img38.png)

Pie Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/pie) here to view the Pie chart online demo sample.


### Change the pie size

You can use the [pieCoefficient](../api/ejchart.html#members:series-piecoefficient) property to change the diameter of the Pie chart with respect to the plot area. It ranges from 0 to 1 and the default value is **0.8**.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
                //Change pie chart coefficient value
                pieCoefficient: 0.4,                                
               //  ...         
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img39.png)

Changing the pie size
{:.caption}


### Explode a pie segment

You can explode a pie segment on the chart load by using the [explodeIndex](../api/ejchart.html#members:series-explodeIndex) of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
               //Set point index value to explode the pie segment. 
               explodeIndex: 1,                                  
               //  ...         
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img40.png)

Exploding a pie segment
{:.caption}


### Explode all the segments

To explode all the segments of the Pie chart, you can enable the [explodeAll](../api/ejchart.html#members:series-explodeall) property.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
                 //Enable explodeAll property for pie chart. 
                 explodeAll: true,                                  
                 //  ...         
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img41.png)

Exploding all the segments
{:.caption}


### Explode a pie segment on mouse over

To explode a pie segment on a mouse over, you can enable the [explode](../api/ejchart.html#members:series-explode) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
                  //Enable pie explode option on mouse over the chart 
                 explode: true,                                  
                 //  ...         
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img42.png)

Exploding a pie segment on mouse over
{:.caption}

### Sector of Pie

EjChart allows you to render all the data points/segments in the semi-pie, quarter-pie or in any sector by using the [startAngle](../api/ejchart.html#members:series-startangle) and [endAngle](../api/ejchart.html#members:series-endangle) options.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            //  ...
            series: [{
                 type: 'pie',     
                 //Set startAngle and endAngle to draw the semi pie chart
                 startAngle: -90, endAngle: 90                                                        
                 //  ...         
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img43.png)

SemiPie Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/semipieanddoughnut) here to view the Semi Pie Chart online demo sample.



## Doughnut Chart

To create a Doughnut chart, you can specify the series [type](../api/ejchart.html#members:series-type) as **"doughnut"** in the chart series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                 //Set chart type to series
                 type: 'doughnut', 
                 //  ...
            }],
            //   ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img44.png)

Doughnut Chart
{:.caption}


### Change Doughnut inner radius

You can change the doughnut chart inner radius by using the [doughnutCoefficient](../api/ejchart.html#members:series-doughnutcoefficient) with respect to the plot area. It ranges from 0 to 1 and the default value is **0.4**.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                 //Change doughnut chart coefficient value
                 doughnutCoefficient: 0.6
                 //  ...
            }],
            //   ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img45.png)

Changing Doughnut inner radius
{:.caption}


### Change the doughnut size

You can use the [doughnutSize](../api/ejchart.html#members:series-doughnutsize) property to change the diameter of the Doughnut chart with respect to the plot area. It ranges from 0 to 1 and the default value is **0.8**.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                 //Change doughnut chart coefficient value
                 doughnutSize: 0.4,                         
                 //  ...
            }],
            //   ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img46.png)

Changing the doughnut size
{:.caption}


### Explode a doughnut segment

To explode a specific doughnut segment, set the index to be exploded by using the [explodeIndex](../api/ejchart.html#members:series-explodeIndex) option of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                 //Set point index value to explode the doughnut segment. 
                 explodeIndex: 1,                                     
                 //  ...
            }],
            //   ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img47.png)

Exploding a doughnut segment
{:.caption}


### Explode all the segments

To explode all the segments, you can enable the [explodeAll](../api/ejchart.html#members:series-explodeall) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                 //Enable explodeAll property of doughnut chart
                 explodeAll: true,                                                
                 //  ...
            }],
            //   ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img48.png)

Exploding all the segments
{:.caption}


### Explode a doughnut segment on mouse over

To explode a doughnut segment on a mouse over, you can enable the [explode](../api/ejchart.html#members:series-explode) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                 //Enable doughnut explode option on mouse over the chart
                 explode: true,                                                           
                 //  ...
            }],
            //   ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img49.png)

Exploding a doughnut segment on mouse over
{:.caption}

### Sector of Doughnut

EjChart allows you to render all the data points/segments in the semi-doughnut, quarter- doughnut or in any sector by using the [startAngle](../api/ejchart.html#members:series-startangle) and [endAngle](../api/ejchart.html#members:series-endangle) options.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                  type: 'doughnut',     
                  //Set startAngle and endAngle to draw the semi pie chart
                  startAngle: -90, endAngle: 90                                                                                  
                 //  ...
            }],
            //   ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img50.png)

Arc of Doughnut
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/semipieanddoughnut) here to view the Semi Doughnut Chart online demo sample.


## Pyramid Chart

To create a Pyramid chart, you can specify the series [type](../api/ejchart.html#members:series-type) as **"pyramid"** in the chart series.  

{% highlight js %}


        $("#chartcontainer").ejChart( {
        
            //...
            series: [{
                    //Set chart type to series
                    type: 'pyramid', 
                     // ...     
            }],
            // ...

        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img51.png)

Pyramid Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/pyramid) here to view the Pyramid Chart online demo sample.


### Pyramid Mode

Pyramid mode has two types, *linear* and *surface* respectively. The default **"pyramidMode"** type is "linear".

{% highlight js %}


        $("#chartcontainer").ejChart( {
        
            //...
            series: [{
                    //Change pyramid mode 
                    pyramidMode: 'surface',                         
                    // ...     
            }],
            // ...

        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img52.png)

Pyramid Chart with surface mode
{:.caption}


### Gap between the segments

You can control the gap between the segments by using the [gapRatio](../api/ejchart.html#members:series-gapratio) option of the series. Its ranges from 0 to 1.

{% highlight js %}


        $("#chartcontainer").ejChart( {
        
            //...
            series: [{
                    //Set gapRatio value to pyramid chart
                    gapRatio: 0.1,                                     
                    // ...     
            }],
            // ...

        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img53.png)

Pyramid Chart with GapRatio
{:.caption}


### Explode a pyramid segment

You can explode a pyramid segment on the chart load by using the [explodeIndex](../api/ejchart.html#members:series-explodeIndex) of the series.

{% highlight js %}


        $("#chartcontainer").ejChart( {
        
            //...
            series: [{
                    //Set point index value to explode the pyramid segment. 
                    explodeIndex: 4,                                                 
                    // ...     
            }],
            // ...

        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img54.png)

Exploding a pyramid segment
{:.caption}


## Funnel Chart

You can create a funnel chart by setting the series [type](../api/ejchart.html#members:series-type) as **"funnel"** in the chart series.  

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                    //Set chart type to series
                    type: 'funnel', 
                    // ...
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img55.png)

Funnel Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/funnel) here to view the Funnel Chart online demo sample.


### Change the funnel width and height

Funnel segments height and width is calculated from the chart size, by default. You can change this height and width directly without changing the chart size by using the [funnelHeight](../api/ejchart.html#members:series-funnelheight) and [funnelWidth](../api/ejchart.html#members:series-funnelwidth) property of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                    //Change funnel height and width
                    funnelHeight:"22%",
                    funnelWidth:"25%",             
                    // ...
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img56.png)

Changing funnel width and height
{:.caption}


### Explode a funnel segment

You can explode a funnel segment on the chart load by using the [explodeIndex](../api/ejchart.html#members:series-explodeIndex) of the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                    //Set point index value to explode the funnel segment. 
                    explodeIndex: 3,                         
                    // ...
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img57.png)

Exploding a funnel segment
{:.caption}


## Bubble Chart

To create a Bubble chart, you can set the series [type](../api/ejchart.html#members:series-type) as **"bubble"** in the chart series. Bubble chart requires 3 fields (*x, y and size*) to plot a point. Here, **size** is used to specify the size of each bubble segment. 

{% highlight js %}

       var chartData = [
                { month: 'Jan', sales: 35, profit:1.34 },
                { month: 'Feb', sales: 28, profit:1.05 },
                { month: 'Mar', sales: 34, profit:0.45 },
                { month: 'Apr', sales: 32, profit:1.10 },
               // ...     
        ];

        $("#chartcontainer").ejChart({
            // ...      
            series: [{
                   //Set chart type to series
                    type: 'bubble', 
                    //Add datasource and set xName, yName and size to bubble chart
                    dataSource: chartData, 
                    xName: "month", 
                    yName: "sales",
                    size: "profit"	,   
               }],
            // ...
            
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img58.png)

Bubble Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/bubble) here to view the Bubble Chart online demo sample.

## Scatter

To create a Scatter chart, you can set the series [type](../api/ejchart.html#members:series-type) as **"scatter"**’ in the chart series. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            
            // ...
            series: [{
                   //Set chart type to series
                    type: 'scatter', 
                    // ...     
             }],
             // ...
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img59.png)

Scatter Series
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/scatter) here to view the Scatter Chart online demo sample.

### Customize the scatter chart

You can change the scatter size by using the [size](../api/ejchart.html#members:series-marker-size) property of the series marker. And you can change the scatter color by using the series [fill](../api/ejchart.html#members:series-fill) property. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...
            series: [{
            
                 // ...
                   marker: {
                       //Change the scatter size
                       size: { height: 13, width: 13 }
                },
                //Set fill color to scatter series
                fill: "#41F282",                    
                // ...     
             }],
           // ...
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img60.png)

Changing scatter size and color
{:.caption}
 

## HiloOpenClose Chart 

To create a HiloOpenClose chart, you can set the series [type](../api/ejchart.html#members:series-type) as **"hiloopenclose"** in the chart series. HiloOpenClose chart requires 5 fields ([x](../api/ejchart.html#members:series-points-x), [high](../api/ejchart.html#members:series-high), [low](../api/ejchart.html#members:series-low), [open](../api/ejchart.html#members:series-open) and [close](../api/ejchart.html#members:series-close)) to plot a segment.  


{% highlight js %}

        var chartData = [
            { month: 'Jan', high: 38, low: 10, open: 38, close: 29 },
            { month: 'Feb', high: 28, low: 15, open: 18, close: 27  },
            { month: 'Mar', high: 54, low: 35, open: 38, close: 49  },
            { month: 'Apr', high: 52, low: 21, open: 35, close: 29  },
            // ...    
         ];

        $("#chartcontainer").ejChart({
            // ...
            series: [{
                   //Set chart type to series
                    type: 'hiloopenclose', 
                    //Add datasource and set xName, high and low to hilo chart
                    dataSource: chartData, 
                    xName: "month", 
                    high: "high",
                    low: "low", 
                    open: 'open',
                    close: 'close',
             }],
           // ...
           
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img61.png)

HiLoOpenCloseSeries
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/hiloopenclose) here to view the HiloOpenClose Chart online demo sample.


### DrawMode

You can change the HiloOpenClose chart [drawMode](../api/ejchart.html#members:series-drawmode) to [open](../api/ejchart.html#members:series-open), [close](../api/ejchart.html#members:series-close) or *both*. The default value of [drawMode](../api/ejchart.html#members:series-drawmode) is **"both"**. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...
            series: [{
                  // ...
                  //Change the OHLC drawMode type
                  drawMode: 'open',                    
             }],
           // ...
           
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img62.png)

HiLoOpenCloseSeries Open DrawMode 
{:.caption}


### Bull and Bear Color	

Hiloopenclose chart [bullFillColor](../api/ejchart.html#members:series-bullfillcolor) is used to specify a fill color for the segments that indicates an increase in stock price in the measured time interval and [bearFillColor](../api/ejchart.html#members:series-bearfillcolor) is used to specify a fill color for the segments that indicates a decrease in the stock price in the measured time interval. 

{% highlight js %}


        $("#chartcontainer").ejChart({
        
            // ...
            series: [{
                     //Change bullFill and bearFill color of hiloopenclose chart
                     bullFillColor: '#FF6600',
                     bearFillColor: '#336600',                   
                     // ...     
              }],
           // ...
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img63.png)

Change OHLC Bull and Bear Color
{:.caption}


## Candle

You can create a Candle chart by specifying the series [type](../api/ejchart.html#members:series-type) as **"candle"** in the chart series. Candle chart requires 5 fields ([x](../api/ejchart.html#members:series-points-x), [high](../api/ejchart.html#members:series-high), [low](../api/ejchart.html#members:series-low), [open](../api/ejchart.html#members:series-open) and [close](../api/ejchart.html#members:series-close)) to plot a segment.

{% highlight js %}

        var chartData = [
            { month: 'Jan', high: 38, low: 10, open: 38, close: 29 },
            { month: 'Feb', high: 28, low: 15, open: 18, close: 27  },
            { month: 'Mar', high: 54, low: 35, open: 38, close: 49  },
            { month: 'Apr', high: 52, low: 21, open: 35, close: 29  },
            // .......     
       ];

        $("#chartcontainer").ejChart({

             // ...
             series: [{
                   //Set chart type to series
                    type: 'candle', 
                    //Add datasource and set xName, high and low to hilo chart
                    dataSource: chartData, 
                    xName: "month", 
                    high: "high",
                    low: "low", 
                    open: 'open',
                    close: 'close'  
             }],
             // ...
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img64.png)

Candle Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/candle) here to view the Candle Chart online demo sample.


### Bull and Bear Color

Candle chart [bullFillColor](../api/ejchart.html#members:series-bullfillcolor) is used to specify a fill color for the segments that indicates an increase in the stock price in the measured time interval and [bearFillColor](../api/ejchart.html#members:series-bearfillcolor) is used to specify a fill color for the segments that indicates a decrease in the stock price in the measured time interval.

{% highlight js %}

        $("#chartcontainer").ejChart({

             // ...
             series: [{
                   //Change bullFill and bearFill color of candle chart
                   bullFillColor: '#FF6600',
                   bearFillColor: '#336600',                   
                   // ...
             }],
             // ...
        });


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img65.png)

Change Candle bull and bear Color
{:.caption}


## Hilo

Hilo chart is created by setting the series [type](../api/ejchart.html#members:series-type) as **"hilo"** in the chart series. Hilo chart requires 3 fields ([x](../api/ejchart.html#members:series-points-x), [high](../api/ejchart.html#members:series-high) and [low](../api/ejchart.html#members:series-low)) to plot a segment.  

{% highlight js %}


      var chartData = [
              { month: 'Jan', high: 38, low: 34 },
              { month: 'Feb', high: 28, low: 15 },
              { month: 'Mar', high: 54, low: 45 },
              { month: 'Apr', high: 32, low: 21 },
              // ...     
        ];

       $("#chartcontainer").ejChart({
            // ...     
            series: [{
                   //Set chart type to series
                    type: 'hilo', 
                    //Add datasource and set xName, high and low to hilo chart
                    dataSource: chartData, 
                    xName: "month", 
                    high: "high",
                    low: "low",   
               }],               
            // ...
                        
        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img66.png)

Change Candle bull and bear Color
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/hilo) here to view the Hilo Chart online demo sample.

## Polar

Polar chart is created by setting the series [type](../api/ejchart.html#members:series-type) as **polar** in the chart series. 

{% highlight js %}


       $("#chartcontainer").ejChart({
            // ...     
            series: [{
                   //Set chart type to series
                    type: 'hilo', 
                    //Add datasource and set xName, high and low to hilo chart
                    dataSource: chartData, 
                    xName: "month", 
                    high: "high",
                    low: "low",   
               }],               
            // ...
                        
        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img67.png)

Polar Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/polar) here to view the Polar Chart online demo sample.


### DrawType

Polar [drawType](../api/ejchart.html#members:series-drawtype) property is used to change the series plotting type to *line*, *column* or *area*. The default value of [drawType](../api/ejchart.html#members:series-drawtype) is **"line"**.  

{% highlight js %}


       $("#chartcontainer").ejChart({
            // ...     
            series: [{
                   //Change polar series drawType
                   drawType: 'column',
                   // ...                       
               }],               
            // ...
                        
        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img68.png)

Polar Chart column type
{:.caption}


### Stack columns in Polar chart

By using the [isStacking](../api/ejchart.html#members:series-isstacking) property, you can specify whether the column has to be stacked when the [drawType](../api/ejchart.html#members:series-drawtype) is column. Its default value is **false**.

{% highlight js %}


       $("#chartcontainer").ejChart({
            // ...     
            series: [{
                   //Enable isStacking property for stacked column polar chart
                   isStacking: true
                   // ...                       
               }],               
            // ...
                        
        }); 


{% endhighlight %}

![](/js/Chart/Chart-Types_images/Chart-Types_img69.png)

Polar Chart IsStacking
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/windrose) here to view the Polar Wind Rose Chart online demo sample.


## Radar Chart  

To create a Radar chart, you can specify the series [type](../api/ejchart.html#members:series-type) as **"radar"** in the chart series.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
           // ...
           series: [{
                   //Set chart type to series
                    type: 'radar', 
                    // ...     
            }],          
              // ...
        }); 


{% endhighlight %}


![](/js/Chart/Chart-Types_images/Chart-Types_img70.png)

Radar Chart
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/radar) here to view the Radar Chart online demo sample.


### DrawType

Radar [drawType](../api/ejchart.html#members:series-drawtype) property is used to change the series plotting type to *line*, *column* or *area*. The default value of [drawType](../api/ejchart.html#members:series-drawtype) is **"line"**.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
           // ...
           series: [{
                   //Change radar series drawType
                   drawType: 'column',                     
                   // ...     
            }],          
              // ...
        }); 


{% endhighlight %}


![](/js/Chart/Chart-Types_images/Chart-Types_img71.png)

Radar Chart with column drawType
{:.caption}


### Stack columns in Radar chart

By using the [isStacking](../api/ejchart.html#members:series-isstacking) property, you can specify whether the column has to be stacked when the [drawType](../api/ejchart.html#members:series-drawtype) is set as *column*. Its default value is set to **false**.

{% highlight js %}


        $("#chartcontainer").ejChart({
        
           // ...
           series: [{
                   //Enable isStacking property for stacked column radar chart
                   isStacking: true                     
                   // ...     
            }],          
              // ...
        }); 


{% endhighlight %}


![](/js/Chart/Chart-Types_images/Chart-Types_img72.png)

Radar IsStacking
{:.caption}



