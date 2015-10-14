---
layout: post
title: Multiple-Panes
description: multiple panes                    
platform: js
control: Chart
documentation: ug
---

# Multiple panes

Chart area can be divided into multiple panes using the [rowDefinitions](../api/ejchart.html#members:rowdefinitions) and [columnDefinitions](../api/ejchart.html#members:rowdefinitions) properties.

### Row Definitions

To split the chart area vertically into number of rows use [rowDefinitions](../api/ejchart.html#members:rowdefinitions) of chart. 

* You can allocate space for each row, using [unit](../api/ejchart.html#members:rowdefinitions-unit) option which determines whether the chart area should be split by *percentage* or *pixels* for the given [rowHeight](../api/ejchart.html#members:rowdefinitions-rowheight) value of rowDefinitions.
 
* To associate a vertical axis to a row, specify the rowDefintions **index** value to [rowIndex](../api/ejchart.html#members:primaryyaxis-rowindex) property of chart axis.

* For customizing each row’s horizontal line, use [lineColor](../api/ejchart.html#members:rowdefinitions-linecolor) and [lineWidth](../api/ejchart.html#members:rowdefinitions-linewidth) property.


{% highlight js %}


       $("#chartcontainer").ejChart({
                    
               //  Splitting chart area into multiple rows
                rowDefinitions: [{
                    //  Split first row of the chart area
                    unit : 'percentage',                 
                    lineColor : 'Gray',
                    rowHeight : 50,
                    linewidth : 0
                }, {
                    //  Split second row of the chart area
                    unit : 'percentage',                 
                    lineColor : 'green',
                    rowHeight : 50,
                    linewidth : 0
                }],

                axes: [{
                          //Create secondary axis and bind it to second row of chart area
                           name: "yAxis1",
                           rowIndex: 1
                    }],   
               series: [{

                         //Binding vertical axis name
                         yAxisName: "yAxis1",
                         // ...
                }],        
            //  ...

        });


{% endhighlight %}

{% include image.html url="/js/Chart/Multiple-Panes_images/Multiple-Panes_img1.png" Caption="Chart with multiple rows"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/multipleaxes) here to view the online demo sample for multiple panes.


**Row Span**

For spanning the vertical axis along multiple panes vertically, you can use [rowSpan](../api/ejchart.html#members:primaryyaxis-rowspan) property of axis. 

{% highlight js %}


       $("#chartcontainer").ejChart({
                    
            rowDefinitions: [{

                         // ...
                  },{

                         // ...
                  }],
                   axes: [{

                          // ...
                    }],

                primaryYAxis: {
                    //  Span the PrimaryYAxis                    
                    rowSpan : 2,
                }, 

               series: [{
                         // ...
                }],        
            //  ...

        });


{% endhighlight %}

{% include image.html url="/js/Chart/Multiple-Panes_images/Multiple-Panes_img2.png" Caption="Chart with row span"%}


## Column Definitions

To split the chart area horizontally into number of columns use [columnDefinitions](../api/ejchart.html#members:columndefinitions) of chart.

* You can allocate space for each column, using [unit](../api/ejchart.html#members:columndefinitions-unit) option which determines whether the chart area should be split by *percentage* or *pixels* for the given [columnWidth](../api/ejchart.html#members:columndefinitions-columnwidth) value of columnDefinitions.
 
* To associate a horizontal axis to a column, specify the columnDefintions **index** value to [columnIndex](../api/ejchart.html#members:primaryxaxis-columnindex) property of chart axis.
 
{% highlight js %}

 
       $("#chartcontainer").ejChart({
                    
               //  Splitting chart area into multiple columns
                columnDefinitions: [{
                    //  Split first column of the chart area
                    unit : 'percentage', 
                    columnWidth : 50,
                }, {
                    //  Split second column of the chart area
                    unit : 'percentage',                 
                    columnHeight : 50,
                }],

                axes: [{
                          //Create secondary axis and bind it to second column of chart area 
                           name: "xAxis1",
                           columnIndex: 1
                    }],   
               series: [{

                         //Binding horizontal axis name
                         xAxisName: "xAxis1",
                         // ...
                }],        
            //  ...

        });


{% endhighlight %}

{% include image.html url="/js/Chart/Multiple-Panes_images/Multiple-Panes_img3.png" Caption="Chart with multiple columns"%}


**Column Span**

For spanning the horizontal axis along multiple panes horizontally, you can use [columnSpan](../api/ejchart.html#members:primaryxaxis-columnspan) property of axis. 

{% highlight js %}

 
       $("#chartcontainer").ejChart({
                    
               columnDefinitions: [{

                          // ...
                  },{

                          // ...
                  }],
                   axes: [{

                          // ...
                    }],

                primaryXAxis: {
                    //  Span the PrimaryXAxis                    
                    columnSpan : 2,
                }, 

               series: [{
                         // ...
                }],        
            //  ...

        });


{% endhighlight %}

{% include image.html url="/js/Chart/Multiple-Panes_images/Multiple-Panes_img4.png" Caption="Chart with column span"%}

