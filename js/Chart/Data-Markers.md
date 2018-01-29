---
layout: post
title: Markers and data labels in Essential JavaScript Chart
description: Learn how to add markers and data point labels to a Chart series.
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Data Markers

Data markers are used to provide information about the data point to the user. You can add a shape and label to adorn each data point.

## Add Shapes

You can add shapes to any chart types but they are often used with line, area and spline series to indicate each data point. It is highlighted when you hover the mouse on the shape.

Shapes can be added to the chart by enabling the [`visible`](../api/ejchart#members:series-marker-visible) option of the [`marker`](../api/ejchart#members:series-marker) property. There are different shapes you can add to the chart by using the [`shape`](../api/ejchart#members:series-marker-shape) option such as rectangle, circle, diamond etc.

The following code example explains on how to enable series marker and add shapes,

{% highlight javascript %}


     $("#container").ejChart({
            // ...
            //Adding shapes to series	
            series: [{
                // ....
                marker: {
                    shape: 'Diamond',
                    visible: true
                }
            },
             {
                 // ... 
                 marker: {
                     shape: 'Triangle',
                     visible: true
                 }
             },
              {
                  // ...
                  marker: {
                      shape: 'Hexagon',
                      visible: true
                  }
              }],

           // ....
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img1.png)

## Customizing marker 

You can give color and opacity for the marker using [`fill`](../api/ejchart#members:series-marker-fill) and [`opacity`](../api/ejchart#members:series-marker-opacity) property.

    $("#container").ejChart({
            series :[{marker : { 
                fill : "green",
                opacity : 0.5 
                } 
            }]                  
    });

## Add image as marker

Apart from the shapes, you can also add images to mark the data point by using the [`imageUrl`](../api/ejchart#members:series-marker-imageurl) option.

The following code example illustrates this,

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
                // ...
                marker: {
                 // Enable and customize the marker shape and size
                    visible: true,
                // In order to set imageUrl, set shape as ‘image’ .
                    shape: "image",
                    imageUrl: "sun_annotation.png",
                    size: {width: 20, height: 20}
                }
            }],
           // ...
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img2.png)


## Add labels

Data label can be added to a chart series by enabling the [`visible`](../api/ejchart#members:series-marker-datalabel-visible) property in the [`dataLabel`](../api/ejchart#members:series-marker-datalabel) option. The labels appear at the top of the data point, by default.

The following code example shows how to enable data label and set its [`horizontalTextAlignment`](../api/ejchart#members:series-marker-datalabel-horizontaltextalignment) and [`vertical text alignment`](../api/ejchart#members:series-marker-datalabel-verticaltextalignment). 

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
                // ...
                marker: {
                        dataLabel: {
                      //Set text alignment to datalabel text	
                            visible: true,
                            horizontalTextAlignment: "center",
                            verticalTextAlignment: "far"
                        }
                    }
            }],
           // ...
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img3.png)


Label content can be formatted by using the template option. Inside the template, you can add the placeholder text *"point.x"* and *"point.y"* to display corresponding data points x & y value.

You can adorn the labels with background shapes by setting *shape* option.

The color for the datalabel text is set by using the [`fill`](../api/ejchart#members:series-marker-datalabel-fill) property.

The following code example shows how to add background shapes and set template to data label.

The border [`color`](../api/ejchart#members:series-marker-border-color) and [`width`](../api/ejchart#members:series-marker-border-width) for the marker is added by using the [`border`](../api/ejchart#members:series-marker-border) property.

{% highlight html %}


<div id="template">
     <div id="left">
	<img src="../images/chart/icon_investments.png"/>
     </div>
     <div id="right">
          <div id="point">#point.y#%</div>
     </div>
</div>

{% endhighlight %}

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
               // ...
               marker: {
		            dataLabel: {
			           visible: true,
                     //Set template to data label
            			template: 'template'
		              }}		
               }, {
	           // ...
               marker: {
		             dataLabel: {
			                visible: true,
                          //Add background shape to the data label
                            shape: 'Rectangle',
                            border: { width: 1, color: "red" }			     
                         }}
                    },{
                // ...
               marker: {
		            dataLabel: {
			           visible: true
		             }}               
              }],

           // ...
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img4.png)


The appearance of the labels can be customized by using the [`font`](../api/ejchart#members:series-marker-datalabel-font) and [`offset`](../api/ejchart#members:series-marker-datalabel-offset) options. The [`color`](../api/ejchart#members:series-marker-datalabel-font-color), [`fontFamily`](../api/ejchart#members:series-marker-datalabel-font-fontfamily), [`fontStyle`](../api/ejchart#members:series-marker-datalabel-font-fontstyle), [`fontWeight`](../api/ejchart#members:series-marker-datalabel-font-fontweight), [`opacity`](../api/ejchart#members:series-marker-datalabel-font-opacity) and [`size`](../api/ejchart#members:series-marker-datalabel-font-size) of font can also be customized. The [`offset`](../api/ejchart#members:series-marker-datalabel-offset) option is used to move the labels vertically. Also, labels can be rotated by using the [`angle`](../api/ejchart#members:series-marker-datalabel-angle) option.

The following code example shows how to rotate datalabel text and customize the font.

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
             // ...
               marker: {
                        dataLabel: {
                            visible: true,
                           //Rotate data label and customize the font
                            angle: "300",    
                            offset: 15,
                            font: { color: "black", size:"13px" }
                         }
                    }		
              }], 
           // ...
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img5.png)


You can position the label to the top, center or bottom position of the segment by using the [`textPosition`](../api/ejchart#members:series-marker-datalabel-textposition) option for the chart types such as column, bar, stacked bar, stacked column, 100% stacked bar, 100% stacked column, candle and OHLC.

The following code example shows how to set textPosition to display data label in the middle of the column rectangle.

{% highlight javascript %}


     $("#container").ejChart({
            // ... 
	        series:[{
                  // ....
                   marker: {
                       dataLabel: {
                           visible: true,
                         // Place the datalabel text position in the center of the rectangle
                           textPosition: "middle"
                          // ...
                       } } 
               }],            

	    // .....
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img6.png)


The label can be positioned inside or outside the perimeter of the series by using the [`labelPosition`](../api/ejchart#members:series-labelposition) option for the chart types such as Pie and Doughnut, .

The following code example shows how to set the *labelPosition*,

{% highlight javascript %}


     $("#container").ejChart({
            // ... 
	        series:[{
                   points: [{ x: 'India', y: 24, text: 'India 24%' },
                            { x: 'Japan', y: 25, text: 'Japan 25%' },
                            { x: 'Australia', y: 20, text: 'Australia 20%' },
                            { x: 'USA', y: 35, text: 'USA 35%' },
                            { x: 'China', y: 23, text: 'China 23%' },
                            { x: 'Germany', y: 27, text: 'Germany 27%' },
                            { x: 'France', y: 22, text: 'France 22%' }],

                   marker: {
                       dataLabel: {
                           visible: true,
                           shape: 'rectangle',
                           font: {color: "white"}
                       }
                   },
                   type: 'doughnut',
                   //Display data label outside position 
                   labelPosition: 'outside'
               }],            
	    // ...
    });


{% endhighlight %} 

![](/js/Chart/Data-Markers_images/Data-Markers_img7.png)


The following screenshot displays the labels when the [`labelPosition`](../api/ejchart#members:series-labelposition) is set as *inside* position.

![](/js/Chart/Data-Markers_images/Data-Markers_img8.png)


The following screenshot displays the labels when the [`labelPosition`](../api/ejchart#members:series-labelposition) is set as *outsideExtended* position.

![](/js/Chart/Data-Markers_images/Data-Markers_img9.png)


The label can be wrapped for pie, doughnut, funnel, and pyramid series by setting the [`enableWrap`](../api/ejchart#members:series-marker-datalabel-enablewrap) property. The maximum label width for data label can be specified using [`maximumLabelWidth`](../api/ejchart#members:series-marker-datalabel-maximumlabelwidth) property.

{% highlight javascript %} 

$("#container").ejChart({

        // . . .   

    series:[
    {
                //. . .
            marker: {
                 
                       dataLabel: {
                                 
                             // enable the dataLabel
                          
                             visible: true,

                             // enable the wrapping option

                             enableWrap: true,
           
                             // set the maximumLabelWidth of the data label

                             maximumLabelWidth: 32
               
                                //. . .

                      }
               }
    
             // . . .

        ]}

     // . . .

});


{% endhighlight %} 

![](/js/Chart/Data-Markers_images/Data-Markers_img13.png)


## Binding label from the datasource

You can bind the text value to the datalabel from the datasource and then you need to map the text value field with the [`textMappingName`](../api/ejchart#members:series-marker-datalabel-textmappingname) properties respectively.

{% highlight javascript %}

//data source for chart with label 
var chartData = [ 
          { month: 'Jan', sales: 35, Text: "January" },  
          { month: 'Feb', sales: 28, Text: "February" }, 
          //... 
]; 

$("#container").ejChart({
    // ...      
        series: [{
            // ...
            marker: {
                dataLabel: {
                    //Mapping the text name 
                    visible : true,
                    textMappingName : "Text",                            
                }
            }
        }],
        // ...
});


{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/vkziijnc)



## Binding fill color to the points from the datasource

You can bind the color value to the points from the datasource and then you need to map the color value field to the [`pointColorMappingName`](../api/ejchart#members:series-pointcolormappingname) property respectively.

{% highlight javascript %}

//data source for chart with fill color
var chartData = [ 
          { month: 'Jan', sales: 35, color: "red" },  
          { month: 'Feb', sales: 28, color: "blue" }, 
          //... 
]; 

$("#container").ejChart({
    // ...      
        series: [{
            // ...
            //Mapping the color values to the points
            pointColorMappingName:"color",                
        }],
    // ...
});


{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ham4a1b2)


## Contrast Color for the data label

 
To change the contrast color for the data label, you can set the [`enableContrastColor`](../api/ejchart#members:series-marker-datalabel-enablecontrastcolor) as **true** in the dataLabel property of the chart series.

When we enable this property, the data label text will be rendered in contrast color based on the segment on which it is placed.
If the data label is placed inside the data points segment, then that particular point's color is taken. Else the chart area or chart background color is considered for deriving the contrast color.
 
{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
                // ...
                marker: {
                        dataLabel: {
                      //Set the saturation color to datalabel text	
                            visible : true,
                            enableContrastColor : true,                            
                        }
                    }
            }],
           // ...
    });


{% endhighlight %}


## Show Edge labels

The partially visible data labels can be displayed inside chart area using [`showEdgeLabels`](../api/ejchart#members:series-marker-datalabel-showedgelabels) property.

{% highlight javascript %}

    $("#container").ejChart({
            series :[{
                marker :{
                    dataLabel :{showEdgeLabels : true}
                }
            }]            
    });

{% endhighlight %}

## DataLabel border

The border [`color`](../api/ejchart#members:series-marker-datalabel-border-color) and [`width`](../api/ejchart#members:series-marker-datalabel-border-width) of the data label can be customized using [`border`](../api/ejchart#members:series-marker-datalabel-border) property.

{% highlight javascript %}

        $("#container").ejChart({
                series :[{
                    marker :{
                        dataLabel :{
                            border : {
                                color : "green",
                                width : 2
                            }
                        }
                    }
                }]                 
        });

{% endhighlight %}


## Customize specific points

By using the ejChart, you can also customize the individual/specific markers with different colors, [`shape`](../api/ejchart#members:series-marker-datalabel-shape) and also with different images.

There are two ways to achieve this based on how the data is fed to the series.

The [`margin`](../api/ejchart#members:series-marker-datalabel-margin) property is used for providing the space in the [`left`](../api/ejchart#members:series-marker-datalabel-margin-left),[`right`](../api/ejchart#members:series-marker-datalabel-margin-right),[`top`](../api/ejchart#members:series-marker-datalabel-margin-top) and [`bottom`](../api/ejchart#members:series-marker-datalabel-margin-bottom) directions.

The required space for the datalabel text can also be customized by using the [`offset`](../api/ejchart#members:series-marker-datalabel-offset) property. The horizontal and vertical offset of data label can be customized using [`x`](../api/ejchart#members:series-marker-datalabel-offset-x) and [`y`](../api/ejchart#members:series-marker-datalabel-offset-y) property.

The opacity of the data label can be customized using [`opacity`](../api/ejchart#members:series-marker-datalabel-opacity) property.

When the data is provided by using the [`points`](../api/ejchart#members:series-points) option, you can add marker for each data point or specific point by using the [`marker`](../api/ejchart#members:series-points-marker) option as illustrated in the following code example. There are several options like [`angle`](../api/ejchart#members:series-points-marker-datalabel-angle), [`opacity`](../api/ejchart#members:series-points-marker-datalabel-opacity), [`border`](../api/ejchart#members:series-points-marker-datalabel-border) [`color`](../api/ejchart#members:series-points-marker-datalabel-border-color), [`width`](../api/ejchart#members:series-points-marker-datalabel-border-width), [`connectorLine`](../api/ejchart#members:series-points-marker-datalabel-connectorline) [`type`](../api/ejchart#members:series-points-marker-datalabel-connectorline-type), [`width`](../api/ejchart#members:series-points-marker-datalabel-connectorline-width), [`fill`](../api/ejchart#members:series-points-marker-datalabel-fill), [`font`](../api/ejchart#members:series-points-marker-datalabel-font) [`size`](../api/ejchart#members:series-points-marker-datalabel-font-size), [`opacity`](../api/ejchart#members:series-points-marker-datalabel-font-opacity), [`fontWeight`](../api/ejchart#members:series-points-marker-datalabel-font-fontweight), [`fontStyle`](../api/ejchart#members:series-points-marker-datalabel-font-fontstyle), [`fontFamily`](../api/ejchart#members:series-points-marker-datalabel-font-fontfamily), [`horizontalTextAlignment`](../api/ejchart#members:series-points-marker-datalabel-horizontaltextalignment), [`margin`](../api/ejchart#members:series-points-marker-datalabel-margin) [`left`](../api/ejchart#members:series-points-marker-datalabel-margin-left), [`right`](../api/ejchart#members:series-points-marker-datalabel-margin-right), [`top`](../api/ejchart#members:series-points-marker-datalabel-margin-top), [`bottom`](../api/ejchart#members:series-points-marker-datalabel-margin-bottom), [`shape`](../api/ejchart#members:series-points-marker-datalabel-shape), [`textPosition`](../api/ejchart#members:series-points-marker-datalabel-textposition), [`verticalTextAlignment`](../api/ejchart#members:series-points-marker-datalabel-verticaltextalignment), [`visible`](../api/ejchart#members:series-points-marker-datalabel-visible), [`template`](../api/ejchart#members:series-points-marker-datalabel-template) and [`offset`](../api/ejchart#members:series-points-marker-datalabel-offset) to customize the point data label.

{% highlight javascript %}


     $("#container").ejChart({
            // ...     
            series: [{
                    // ...
                    points: [  { x: 'Jan', y: 35 }, { x: 'Feb', y: 28 },   { x: 'Mar', y: 34 },
                      { x: 'Apr', y: 32 },{ x: 'May', y: 40 },  { x: 'Jun', y: 32 },
                      { x: 'Jul', y: 35 },  { x: 'Aug', y: 55,
                       marker: {
                         //Enable and customize the data label for a point
                            dataLabel: {
                                visible: true,
                                offset: -10,
                                shape: "upArrow", font: { color: "white" , size: '11px' },
                                margin: { left: 15, right: 15, top: 10, bottom: 10 },
                                fill: "green"
                           } } },

                          { x: 'Sep', y: 38 },{ x: 'Oct', y: 30 },
                          { x: 'Nov', y: 25,
                                  marker: {
                                    //Enable and customize the data label for a point
                                     dataLabel: {
                                        visible: true,
                                        offset: -22,
                                        verticalTextAlignment: 'near',
                                        shape: "downArrow", font: { color: "white", size: '11px' },
                                        margin: { left: 15, right: 15, top: 10, bottom: 10 },                    
                                        fill: "red"
                           } } },  { x: 'Dec', y: 32 }],

                     }],
                 // ...
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img10.png)

When the data is bound to the series by using the [`dataSource`](../api/ejchart#members:series-datasource) option, you can customize the points in the [`seriesRendering`](../api/ejchart#members:events-seriesrendering) event as illustrated in the following code example,

{% highlight javascript %}


     $("#container").ejChart({
           // ...
            series: [{
                         //Add datasource and set xName and yName 
                         dataSource: chartData, 
                          xName: "month", 
                          yName: "sales"
            }],
            
           //Fires on rendering the series
            seriesRendering: "onSeriesRender",

             // ...

    });

    //Define the seriesRendering client side event
  
     function onSeriesRender(sender) {
 
        
        //Enable and customize the dataLabel for a point using event

            sender.data.series.points[7].marker = {
               dataLabel: {
                    visible: true,
                    offset: -10,
                    shape: "upArrow", font: { color: "white", size: '11px' },
                    margin: { left: 15, right: 15, top: 10, bottom: 10 },                    
                    fill: "green"
                }};

            sender.data.series.points[10].marker = {
                 //Enable and customize the dataLabel for a point using event
                dataLabel: {
                        visible: true,
                        offset: -22,
                        verticalTextAlignment: 'near',
                        shape: "downArrow", font: { color: "white", size: '11px' },
                        margin: { left: 15, right: 15, top: 10, bottom: 10 },                    
                        fill: "red"
                }};
        }

{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img10.png)


## Connect Line

This feature is used to connect label and data point by using a line. It can be enabled only for Pie, Doughnut, Pyramid and Funnel chart types. Connector line types can be set as *bezier* or *line* by using the [`type`](../api/ejchart#members:series-marker-datalabel-connectorline-type) option. The [`color`](../api/ejchart#members:series-marker-datalabel-connectorline-color) and [`width`](../api/ejchart#members:series-marker-datalabel-connectorline-width) of connector line can also be customized using [`connectorLine`](../api/ejchart#members:series-marker-datalabel-connectorline) property.

 The following code example illustrates this,

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
		      // ...
		       marker: {
                   dataLabel: {
                             visible: true,
                             // Set connector line type and customize the color,
                             connectorLine: { type: 'bezier', color: 'black', width: 1 }
                             // ...
                         }  },
                         // ...
                         labelPosition: 'outsideExtended',
                 }],

           // ...
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img11.png)


## Smart labels

Overlapping of the labels can be avoided by enabling the [`enableSmartLabels`](../api/ejchart#members:series-enablesmartlabels) property. The default value is *true* for *accumulation type series* and *false* for *other series types*.

The following code example shows how to enable smart labels,

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            //Initializing Series	
            series: [{
                points: [{ x: 'Other Personal', y: 94658, text: 'Other Personal, 88.47%' },
                             { x: 'Medical care', y: 9090, text: 'Medical care, 8.49%' },
		                     { x: 'Housing', y: 2577, text: 'Housing, 2.40%' },
                             { x: 'Transportation', y: 473, text: 'Transportation, 0.44%' },
                             { x: 'Education', y: 120, text: 'Education, 0.11%' },
                             { x: 'Electronics', y: 70, text: 'Electronics, 0.06%' }],
           	    marker:{
		              dataLabel:{
				          visible: true,
				          shape: 'none',
				          connectorLine: { type: 'bezier', color: 'black' },
				          font: { size: '14px' }
                       }},
               	       border: { width: 2, color: 'white' },
		               type: 'pie',
                       labelPosition: "outsideExtended",
                       //Display data label outside position and enable smartLabels
                       enableSmartLabels: true
                 }],
           // ...
    });


{% endhighlight %}

![](/js/Chart/Data-Markers_images/Data-Markers_img12.png)


