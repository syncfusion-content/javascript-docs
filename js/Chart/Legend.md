---
layout: post
title: Legend
description: legend
platform: js
control: Chart
documentation: ug
---

# Legend

The legend contains the list of chart series and Trendlines that appear in a chart. 

## Legend Visibility

By default, legend is enabled in chart. You can enable or disable it using [visible](../api/ejchart#members:legend-visible) option of legend.

{% highlight js %}


    $("#chartcontainer").ejChart({
         // ...
         legend: {
            //Visible chart legend
            visible: true
        },
        //...
     });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img1.png" Caption="Legend visibility in chart"%}


## Legend title

For adding title to the legend, you have to specify [legend.title.text](../api/ejchart#members:legend-title-text) option.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
              legend: {
                //...
                title: {
                   //Add title to the chart legend
	               text: "Countries",
				
		         }  },

            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img2.png" Caption="Chart with legend title"%}


## Positioning and Aligning Legend

Using [position](../api/ejchart#members:legend-position) option, you can position the legend at *left*, *right*, *top* or *bottom* of the chart. By default, legend is positioned at the **bottom** of the chart.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                // ...  
                //Place the legend at top of the chart
                position: 'top',

            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img3.png" Caption="Change legend position"%}

**Legend Alignment**

You can align the legend to *center*, *far* or *near* based on its position using [alignment](../api/ejchart#members:legend-alignment) option.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                //...
                //The below two settings will place the legend at the top-right corner of the chart.
                alignment: 'far',
                position: 'top', 
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img4.png" Caption="Change legend position and alignment"%}


## Arranging legend items in rows and columns

You can arrange the legend items horizontally and vertically using [rowCount](../api/ejchart#members:legend-rowcount) and [columnCount](../api/ejchart#members:legend-columncount) options of legend.

* If only [rowCount](../api/ejchart#members:legend-rowcount) is specified, legend items will be arranged according to [rowCount](../api/ejchart#members:legend-rowcount), and number of columns may vary based on number of legend items.

* If only [columnCount](../api/ejchart#members:legend-columncount) is specified, legend items will be arranged according to [columnCount](../api/ejchart#members:legend-columncount) and number of rows may vary based on number of legend items.

* If both options are specified, then the one which has higher value will be given preference. For example, if [rowCount](../api/ejchart#members:legend-rowcount) is 4 and [columnCount](../api/ejchart#members:legend-columncount) is 3, legend items will be arranged in 4 rows.

* If both options are specified and have same value, preference will be given to [columnCount](../api/ejchart#members:legend-columncount) if it is positioned at top/bottom position and to [rowCount](../api/ejchart#members:legend-rowcount) if it is positioned at left/right position.
 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                //Arrange legend items in 4 rows and approximately 4 columns. Column couldn’t may vary based on number of items. 
                rowCount: 4,
                columnCount: 4 
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img5.png" Caption="Arrangeing legend items in rows and columns"%}


## Customization

### Legend shape

For changing the legend icon shape, you have to specify the shape in [shape](../api/ejchart#members:legend-shape) property of legend. If you want the legend icon to display the prototype of the series, you have to set **seriesType** as shape.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                //...
                //Change legend shape
                 shape: 'seriesType',
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img6.png" Caption="Changing legend shape"%}


### Legend items size and border

You can change the size of legend items using [itemStyle.width](../api/ejchart#members:legend-itemstyle-width) and [itemStyle.height](../api/ejchart#members:legend-itemstyle-height) options. To change the legend item border, use [border](../api/ejchart#members:legend-border) option of legend itemStyle.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                //...
                //Change legend items border, height and width
                itemStyle: {width: 13, height: 13, border: { color: "#FF0000", width: 1 } },
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img7.png" Caption="Changing legend items size and border"%}


### Legend size

By default, legend takes 20% of **height** horizontally when it was placed on the top or bottom position and 20% of **width** vertically while placing on the left or right position of chart. You can change this default legend size using [size](../api/ejchart#members:legend-size) option of legend.  

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...
            legend: { 
                 //...
                 //Change legend size
                 size:{width: '550', height: '100'}
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img8.png" Caption="Change legend size"%}


### Legend Item Padding

You can control the spacing between legend items using [itemPadding](../api/ejchart#members:legend-itempadding) option of legend.  The default value is 10. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                //...
                //Add space between each legend item
                itemPadding: 15,
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img9.png" Caption="Change padding between the legend items"%}


### Legend border

You can customize the legend border using [border](../api/ejchart#members:legend-border) option in legend. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                //...
                //Set border color and width to legend
                border: {color: "#FFC342", width: 2},
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img10.png" Caption="Customize the legend border"%} 


### Scrollbar for legend

You can enable or disable the legend scrollbar using [enableScrollbar](../api/ejchart#members:legend-enablescrollbar) option of legend. If you disable the scrollbar option, legend won’t consider the [default size](legend.html#legend-size) and chart will draw in the reaming space. The default value of [enableScrollbar](../api/ejchart#members:legend-enablescrollbar) option is **true**.  

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                //...
                //Enable scrollbar option in for legend
                enableScrollbar: true,
                size:{width: '430', height: '80'},
            }
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img11.png" Caption="Enable scrollbar for legend"%}

### Customizing legend text

For customizing legend item text and title you can use [legend.font](../api/ejchart#members:legend-font) and [legend.title](../api/ejchart#members:legend-title) options. And you can change the legend title alignment using [textAlignment](../api/ejchart#members:legend-title-textAlignment) option of legend title.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legend: {
                //...
                //Customize the legend item text
                font: { fontFamily: 'Segoe UI', fontStyle: 'Normal', fontWeight: 'Bold', size: '15px' },
                title: {
                    //...
		            textAlignment: "center",
                    //Customize the legend title text
	                font: { fontFamily: 'Segoe UI', fontStyle: 'Italic', 
                                        fontWeight: 'Bold', size: '12px' },
	             }            
             },
            // ...             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img12.png" Caption="Customizing legend item and title text"%}


## Handling legend item clicked

You can get legend item details such as *index*, *bounds*, *shape* and *series* by subscribing [legendItemClick](../api/ejchart#events:legenditemclick) event on chart. When the legend item is clicked, it will triggers the event and returns [legend information](../api/ejchart.html#events:legenditemclick). 

{% highlight js %}


        $("#chartcontainer").ejChart({

            legend: {
                   //...
              },
              
           //Subscribe the legenditem click event
            legendItemClick: "onlegendclicked",
            
            //...
        });
        
     function onlegendclicked(sender) {
        //Get legend item details on legend item click.
        var legendItem = sender.data;
      }

{% endhighlight %}


## Series selection on legend item click

You can select a specific series or point while clicking on the corresponding legend item through disabling the [toggleSeriesVisibility](../api/ejchart#members:legend-toggleseriesvisibility) option in legend. The default value of [toggleSeriesVisibility](../api/ejchart#members:legend-toggleseriesvisibility) option is **true**. To customize the series selection refer series [selection](../api/ejchart.html#members:series-selectionsettings).

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
                legend: {
                   //...
                   //Disable series collapsing on legend item clicked
                   toggleSeriesVisibility: false,
               },
           //...
      });
      

{% endhighlight %}

{% include image.html url="/js/Chart/Legend_images/Legend_img13.png" Caption="Avoid series collapsing on legend item clicked"%}