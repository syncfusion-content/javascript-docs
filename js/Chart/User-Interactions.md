---
layout: post
title: Interactions available in Essential JavaScript Chart
description: What are the interactions available in Chart like tooltip, crosshair, trackball, highlighting, zooming and panning, etc..,
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# User Interactions

## Tooltip

### Enable tooltip for data point

Tooltip for the data points can be enabled by using the [`visible`](../api/js/ejchart#members:series-tooltip-visible) option of the [`tooltip`](../api/js/ejchart#members:series-tooltip) in the series.

{% highlight javascript %}


        $("#container").ejChart({
           
            // ...           
            series: [{
                  
                  //...
                  //Enable tooltip for the series
                  tooltip: {visible: true}	
              }],
           // ...
           
        });


{% endhighlight %}



![](/js/Chart/User-Interactions_images/User-Interactions_img1.png)

### Format the tooltip 

Tooltip displays data specified by the [`format`](../api/js/ejchart#members:series-tooltip-format) option of the tooltip. The default value of the format option is * **#point.x# : #point.y#** *. Here, * **#point.x#** * is the placeholder for x value of the point and * **#point.y#** * is the placeholder for y value of the point.

You can also use * **#series.<optionname>#** * as placeholder to display the value of an option in corresponding series and use * **#point.<optionname>#** * as place holder to display the value of an option in the corresponding point.

{% highlight javascript %}


        $("#container").ejChart({
            // ...
            series: [{
                 tooltip: {
                       //Displaying tooltip in a format
                       format: "#series.name# <br/> #point.x# : #point.y#  (g/kWh)"	
                       // ...
                 } 
              }],
            // ...
        });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img2.png)

### Tooltip Template

HTML elements can be displayed in the tooltip by using the [`template`](../api/js/ejchart#members:series-tooltip-template) option of the tooltip. The template option takes the value of the id attribute of the HTML element. You can use the * **#point.x#** * and * **#point.y#** * as place holders in the HTML element to display the x and y values of the corresponding data point. 

You can also use * **#series.<optionname>#** * as place holder to display the value of an option in corresponding series of the tooltip and use * **#point.<optionname>#** * as place holder to display the value of an option in the corresponding point for which the tooltip is displayed.
  

{% highlight html %}

<body>
   <div id="container"></div>
    <!-- Create Tooltip template here -->
    <div id="Tooltip" style="display: none;">
              <div id="icon"> <div id="eficon"> </div>  </div>
        <div id="value">
            <div>
               <label id="efpercentage">&nbsp;#point.y#% </label>
               <label id="ef">Efficiency </label>
            </div>
        </div>
    </div>
<script>
   $("#container").ejChart({   
     	// ...             
	    series: [{
              tooltip: {
                 //Set template id to tooltip template
                 template: 'Tooltip',	
                 // ...
                }
          }],
	    // ...             
    });
    
   </script>
</body>

{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img3.png)

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/line) here to view the Tooltip template online demo sample.


#### Tooltip template animation

You can enable animation by setting the [`enableAnimation`](../api/js/ejchart#members:series-tooltip-enableanimation) to true. Tooltip animates when the mouse moves from one data point to another point. The [`duration`](../api/js/ejchart#members:series-tooltip-duration) property in tooltip specifies the time taken to animate the tooltip. the duration is set to **"500ms"**, by default.

N> Tooltip is animated only if the template is specified for tooltip.

{% highlight javascript %}


        $("#container").ejChart({
            
            // ...
            series: [{
                  tooltip: {
                    //Enable tooltip template animation and set duration time
                    enableAnimation: true, duration: "1000ms",                                      
                    // ...
                 }
             }],
             
            // ...
        });


{% endhighlight %}


### Customize the appearance of tooltip   

The [`fill`](../api/js/ejchart#members:series-tooltip-fill) and [`border`](../api/js/ejchart#members:series-tooltip-border) [`color`](../api/js/ejchart#members:series-tooltip-border-color) and [`width`](../api/js/ejchart#members:series-tooltip-border-width) options are used to customize the background color and border of the tooltip respectively. The [`font`](../api/js/ejchart#members:series-tooltip-font) and [`opacity`](../api/js/ejchart#members:series-tooltip-opacity) option in the tooltip is used to customize the font and opacity of the tooltip text. 

{% highlight javascript %}


        $("#container").ejChart({
            // ...
            series: [{
                 tooltip: {
                       //Change tooltip color and border
                       fill: '#FF9933',
                       border: { width: 1, color: "#993300" }	
                       // ...
                 } 
              }],
            // ...
        });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img4.png)

#### Tooltip with rounded corners

The options [`rx`](../api/js/ejchart#members:series-tooltip-rx) and [`ry`](../api/js/ejchart#members:series-tooltip-ry) are used to customize the corner radius of the tooltip rectangle.

{% highlight javascript %}


        $("#container").ejChart({
           
	        // ...             
	        series: [{
                 tooltip: {
                    //Customize the corner radius of the tooltip rectangle.
                    rx: "50", ry: "50"                            
                    // ...
                 }
              }],
	       // ... 
        });


{% endhighlight %}


![](/js/Chart/User-Interactions_images/User-Interactions_img5.png)


## Zooming and Panning

### Enable Zooming

The Zooming of the chart is done using the [`zooming`](../api/js/ejchart#members:zooming) property.There are two ways you can zoom the chart,

* When the [`zooming.enable`](../api/js/ejchart#members:zooming-enable) option is set to true, you can zoom the chart by using the rubber band selection.

* When the [`zooming.enableMouseWheel`](../api/js/ejchart#members:zooming-enablemousewheel) option is set to true, you can zoom the chart on mouse wheel scrolling. 

* When [`zooming.enablePinching`](../api/js/ejchart#members:zooming-enablePinching) option is set to *true*, you can zoom the chart through pinch gesture.

* When [`zooming.enableDeferredZoom`](../api/js/ejchart#members:zooming-enabledeferredzoom) option is set to *true*,the chart is updated only on mouse up action while zooming and panning

N> Pinch zooming is supported only in browsers that support multi-touch gestures. Currently IE10, IE11, Chrome and Opera browsers support multi-touch in desktop devices.

{% highlight javascript %}


        $("#container").ejChart({
             //  ...             
	         //Enable zooming in chart
             zooming: {enable: true}
             // ...
        });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img6.png)


After zooming the chart, a zooming toolbar will appear with options to *zoom*, *pan* and *reset*. Selecting the Pan option will allow to pan the chart and selecting the Reset option will reset the zoomed chart.

![](/js/Chart/User-Interactions_images/User-Interactions_img7.png)


[Click](https://ej2.syncfusion.com/home/#!/azure/chart/userinteraction/zoomingandpanning) here to view the Zooming and Panning online demo sample.


### Types of zooming

The [`type`](../api/js/ejchart#members:zooming-type) option in zooming specifies whether the chart is allowed to scale along the horizontal axis or vertical axis or along both axis. The default value of the [`type`](../api/js/ejchart#members:zooming-type) is **"xy"** (both axis).

{% highlight javascript %}


        $("#container").ejChart({
             //  ...             
	         zooming: {
                    enable: true,
                    //Enable horizontal zooming
                    type: 'x'
                } 
             // ...
        });


{% endhighlight %}


### Customizing zooming toolbar

You can choose the items displayed in the zooming toolbar by specifying the property [`toolBarItems`](../api/js/ejchart#members:zooming-toolbaritems).

{% highlight javascript %}


    $("#container").ejChart({
             //  ...             
	         //Customizing zooming toolbar
	         zooming:{	
			   enable: true,
               toolbarItems: ["reset", "zoomIn", "zoomOut"]
			},
             // ...
    });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img8.png)



### Enable ScrollBar

EjChart provides scrollbar support to view the other portions of chart area which is not shown in the view port when zoomed, by setting true to [`enableScrollbar`](../api/js/ejchart#members:zooming-enablescrollbar) option in [`zooming`](../api/js/ejchart#members:zooming).  

{% highlight javascript %}


    $("#container").ejChart({
             //  ...             
	         //Enable zooming scrollbar  in chart
             zooming: {enable:true, enableScrollbar: true}
             // ...
     });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img9.png)

## Crosshair

Crosshair is used to view the value of an axis at mouse position or touch contact point. 

### Enable crosshair and crosshair label

Crosshair can be enabled by using the [`visible`](../api/js/ejchart#members:series-tooltip-visible) option in the [`crosshair`](../api/js/ejchart#members:crosshair). Crosshair label for an axis can be enabled by using the [`visible`](../api/js/ejchart#members:primaryxaxis-crosshairlabel-visible) option of [`crosshairLabel`](../api/js/ejchart#members:primaryxaxis-crosshairlabel) in the corresponding axis.


{% highlight javascript %}


        $("#container").ejChart({
            // ...             
            primaryXAxis:{
                //Enable crosshairLabel to X-Axis
                crosshairLabel: { visible: true },
            },

            primaryYAxis:{
                //Enable crosshairLabel to Y-Axis
                crosshairLabel: { visible: true },
            },
           
           //Initializing Crosshair
            crosshair:{
                visible: true
            },
            // ...             

        });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img10.png)

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/userinteraction/crosshair) here to view the Crosshair online demo sample.


### Customize the crosshair line and crosshair label

The [`fill`](../api/js/ejchart#members:crosshair-fill) and [`border`](../api/js/ejchart#members:crosshair-border) options of the [`crosshairLabel`](../api/js/ejchart#members:crosshairlabel) is used to customize the background color and border of the crosshair label respectively. Color and width of the crosshair line can be customized by using the [`line`](../api/js/ejchart#members:crosshair-line) option in the [`crosshair`](../api/js/ejchart#members:crosshair).

{% highlight javascript %}


        $("#container").ejChart({
             // ...             
             primaryXAxis: {
                     //...
                     crosshairLabel: {
                          visible: true,
                          //Customizing the crosshair label background color and border
                          fill: "red", 
                          border: { color: "green", width: 2 }
                      }
              },
               
              crosshair: {
                   visible: true,
                   //Customizing the crosshair line
                   line: { color: 'gray', width: 2 },
              } 
            // ...
        });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img11.png)

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/userinteraction/crosshair) here to view the Crosshair online demo sample.

### Crosshair marker

Options for customizing the [`marker`] (../api/js/ejchart#members:crosshair-marker) in crosshair.

### Crosshair marker Border

Options for customizing the [`border`] (../api/js/ejchart#members:crosshair-marker-border)

### Crosshair marker Border width

Border [`width`] (../api/js/ejchart#members:crosshair-marker-border-width) of the marker.

{% highlight javascript %}


     $("#container").ejChart({

   crosshair : { marker : { border : { width :2 } } }              

});


{% endhighlight %}

### Crosshair marker Opacity

[`Opacity`] (../api/js/ejchart#members:crosshair-marker-opacity) of the marker.


{% highlight javascript %}


     $("#container").ejChart({

   crosshair :{marker :{opacity :2}}                

});

{% endhighlight %}

### Crosshair marker size

Options for customizing the [`size`] (../api/js/ejchart#members:crosshair-marker-size)of the marker.

### Crosshair marker size height

[`Height`] (../api/js/ejchart#members:crosshair-marker-size-height)of the marker.

{% highlight javascript %}


     $("#container").ejChart({

  crosshair :{marker :{size :{ height :15 }}}                  

});

{% endhighlight %}

### Crosshair marker size width

[`Width`] (../api/js/ejchart#members:crosshair-marker-size-width)of the marker.

{% highlight javascript %}


     $("#container").ejChart({

  crosshair :{marker :{size : {width :15}}}                       

});

{% endhighlight %}

### Crosshair line

Options for customizing the crosshair [`line`] (../api/js/ejchart#members:crosshair-line)

### Crosshair line Color

[`Color`] (../api/js/ejchart#members:crosshair-line-color) of the crosshair line.


{% highlight javascript %}


     $("#container").ejChart({

  crosshair : { line : { color "red" } }                           

});

{% endhighlight %}

### Crosshair line Width

[`Width`] (../api/js/ejchart#members:crosshair-line-width) of the crosshair line.

{% highlight javascript %}


     $("#container").ejChart({

 
   crosshair : { line : { width: 2 } }                            

});

{% endhighlight %}

## Trackball

Trackball is used to track a data point close to the mouse position or touch contact point. Trackball marker indicates the closest point and trackball tooltip displays the information about the point.

### Enable Trackball

Trackball can be enabled by setting the [`visible`](../api/js/ejchart#members:crosshair-visible) option of the crosshair to *true* and then set the [`type`](../api/js/ejchart#members:crosshair-type) as **"trackball"**. The default value of type is **"crosshair"**.

{% highlight javascript %}


       $("#container").ejChart({   
	
             crosshair: {
                   visible: true,
                   //Change crosshair type to trackball
                   type: 'trackball',
                  } 
           //......
           });


{% endhighlight %}


![](/js/Chart/User-Interactions_images/User-Interactions_img12.png)

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/userinteraction/trackball) here to view the Trackball online demo sample.


#### Customize trackball marker and trackball line

Visibility,shape, size ,border of the trackball marker can be customized by using the[`visible`](../api/js/ejchart#members:crosshair-marker-visible) [`shape`](../api/js/ejchart#members:crosshair-marker-shape) , [`size`](../api/js/ejchart#members:crosshair-marker-size) and [`border`](../api/js/ejchart#members:crosshair-marker-border)options of the [`crosshair marker`](../api/js/ejchart#members:crosshair-marker). Color and width of the trackball line can be customized by using the [`line`](../api/js/ejchart#members:crosshair-line) option in the crosshair.

{% highlight javascript %}


       $("#container").ejChart({   
	
             // ...
             crosshair: {
                  visible: true,

                  //Customize the trackball line color and width
                  line: { color: '#800000', width: 2 },

                  //Customize the trackball marker shape size and visibility
                  marker: {
                       shape: 'pentagon',
                       size: {
                            height: 9, width: 9
                         },
                       //Enable/disable trackball marker
                       visible: true
                    }     
                } 
              // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img13.png)


### Format Trackball tooltip

X and Y values displayed in the trackball tooltip are formatted based on its axis [`labelFormat`](../api/js/ejchart#members:primaryxaxis-labelformat).  

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              primaryXAxis: {
                   labelFormat: 'MMM, yyyy',
                   //...
               },
              
              primaryYAxis: {
                    labelFormat: '{value}K',
                    //...
               },
               
               crosshair: {
                    visible: true,
                    type: 'trackball',                           
                }
                  // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img14.png)

### Customizing the Trackball Tooltip 

The  [`trackballTooltipSettings`](../api/js/ejchart#members:crosshair-trackballtooltipsettings) property is used for displaying the trackball tooltip.

#### Mode
You can able to show the trackball tooltip in two modes, using [`mode`](../api/js/ejchart#members:crosshair-trackballtooltipsettings-mode) property.

                1.	Grouping.
                2.	Float. 

#### Border

The border of the trackball tooltip can be customized by using the [`border`](../api/js/ejchart#members:crosshair-trackballtooltipsettings-border) property.
The width and color of the border can be customized using the  [`width`](../api/js/ejchart#members:crosshair-trackballtooltipsettings-border-width) and [`color`](../api/js/ejchart#members:crosshair-trackballtooltipsettings-border-color) properties


#### Fill,Rx,Ry,Opacity

The color ,opacity and  corners of the trackball tooltip are customized by using the [`fill`](../api/js/ejchart#members:crosshair-trackballtooltipsettings-fill) ,[`opacity`](../api/js/ejchart#members:crosshair-trackballtooltipsettings-opacity),[`rx`](../api/js/ejchart#members:crosshair-trackballtooltipsettings-rx) and [`ry`](../api/js/ejchart#members:crosshair-trackballtooltipsettings-ry) properties.

{% highlight javascript %}


            $("#container").ejChart({
                // ... 
                    crosshair: {
                        visible: true,
                        type: 'trackball',
                        //Customize the trackball tooltip
                        trackballTooltipSettings: {
                            //Trackball mode
                            mode: 'grouping',
                            //Customize the trackball border, fill, rx and ry               
                                border:{ 
                                    width:1,
                                    color: 'grey'
                                },
                            rx: 3,
                            ry: 3,
                            fill: 'whitesmoke'
                        }
                     }
         // ... });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img30.png)

#### Trackball tooltip template:

Trackball tooltip template is used to display the tooltip in the customized template format. You can define the  desired template  in css style.You can enable the **toolTipTemplate** by using the following  code snippet.

{% highlight javascript %}


            $("#container").ejChart({
                 
                  
               crosshair:
                 {
                     visible: true,
                     type: 'trackball',
                     trackballTooltipSettings: {
                         mode: "float",
                         tooltipTemplate: 'Tooltip'
                         }
                 }

               });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img33.png)


## Highlight

EjChart provides highlighting support for the series and data points on mouse hover. To enable the highlighting option, set the [`enable`](../api/js/ejchart#members:series-highlightsettings-enable) property to *true* in the [`highlightsettings`](../api/js/ejchart#members:series-highlightsettings) of the series.

N> When hovering mouse on the data points, the corresponding series legend also will be highlighted.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                    highlightSettings: {
                        
                         // enable the highlight settings
                         enable: true,
                     },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/chartcustomization/selection) here to view the highlight and selections online demo sample.


### Highlight Mode

You can set three different highlight mode for the highlighting data point and series by using the [`mode`](../api/js/ejchart#members:series-highlightsettings-mode) property of the [`highlightsettings`](../api/js/ejchart#members:series-highlightsettings).

* Series
* Points
* Cluster

**Series mode**

To highlight all the data points of the specified series, you can set the **"series"** value to the [`mode`](../api/js/ejchart#members:series-highlightsettings-mode) option in the highlightSettings. 


{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                    highlightSettings: {
                        enable: true, 
                        
                        //Change highlight mode
                        mode: 'series'

                     },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img15.png)


**Point mode**

To highlight a single point, you can set the **"point"** value to the [`mode`](../api/js/ejchart#members:series-highlightsettings-mode) option.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                    highlightSettings: {
                        enable: true, 
                        
                        //Change highlight mode
                        mode: 'point'

                     },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img16.png)


**Cluster mode**

To highlight the points that corresponds to the same index in all the series, set the **"cluster"** value to the [`mode`](../api/js/ejchart#members:series-highlightsettings-mode) option.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                    highlightSettings: {
                        enable: true, 
                        
                        //Change highlight mode
                        mode: 'cluster'

                     },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img17.png)

### Customize the highlight styles

To customize the highlighted series, use the [`color`](../api/js/ejchart#members:series-highlightsettings-color), [`border`](../api/js/ejchart#members:series-highlightsettings-border) [`color`](../api/js/ejchart#members:series-highlightsettings-border-color), [`width`](../api/js/ejchart#members:series-highlightsettings-border-width) and [`opacity`](../api/js/ejchart#members:series-highlightsettings-opacity) options in the highlightSettings.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                    highlightSettings: {
                        enable: true, 
                        
                        //Customizing 
                        border: { width: '1.5', color: "red" },
                        opacity: 0.5, color: "green"
                     },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img18.png)


### Patterns to highlight

EjChart provides pattern support for highlighting the data by setting the value to the [`pattern`](../api/js/ejchart#members:series-highlightsettings-pattern) property of the highlightSettings. The different types of highlight patterns are as follows.

1.	chessboard
2.	crosshatch
3.	dots
4.	pacman
5.	grid
6.	turquoise
7.	star
8.	triangle
9.	circle
10.	tile
11.	horizontalDash
12.	verticalDash
13.	rectangle
14.	box
15.	verticalStripe
16.	horizontalStripe
17.	bubble
18.	diagonalBackward
19.	diagonalForward

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                    highlightSettings: {
                        enable: true, 
                        
                        //Change highlighting pattern
                         pattern: "chessboard",

                     },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img19.png)

#### Custom pattern

To create a custom pattern for the highlighting data points, set the pattern type as **"custom"** and add the custom pattern **id** in the [`customPattern`](../api/js/ejchart#members:series-highlightsettings-custompattern) option of the highlightSettings.

{% highlight html %}


<body>
    <div id="container"></div>
            <svg>
                <pattern id="dots_a" patternUnits="userSpaceOnUse" width="6" height="6">
                    <rect x="0" y="0" width="6" height="6" transform="translate(0,0)" fill="black" opacity="1"></rect>
                    <path d='M 3 -3 L -3 3 M 0 6 L 6 0 M 9 3 L 3 9'stroke-width="1" stroke="white"></path>
                </pattern>
            </svg>
<script type="text/javascript">

   $("#container").ejChart({
            // ...
            series:[{
                highlightSettings: [{
                    enable: true,
                    //Add custom pattern for highlighting data
                    pattern: "custom",
                    customPattern: 'dots_a',
                    // ...
                }],
                // ...       
     });

        </script>
</body>

{% endhighlight %}


## Selection

EjChart provides selection support for the series and data points on mouse click. To enable the selection option, set the [`enable`](../api/js/ejchart#members:series-selectionsettings-enable) property to *true* in the [`selectionSettings`](../api/js/ejchart#members:series-selectionsettings) of the series.

N> When mouse is clicked on the data points, the corresponding series legend also will be selected.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                   selectionSettings: {
                         // enable the selection settings
                         enable: true, 
                      },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/chartcustomization/selection) here to view the highlight and selections online demo sample.


### Selection Mode

You can set four different selection mode for highlighting the data point and series by using the [`mode`](../api/js/ejchart#members:series-selectionsettings-mode) property of the selectionSettings.

* Series
* Points
* Cluster
* Range

**Series mode**

To select all the data points of the specified series, you can set the **"series"** value to the [`mode`](../api/js/ejchart#members:series-selectionsettings-mode) option in the selectionSettings.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                   selectionSettings: {
                         enable: true, 
                         
                        //Change selection mode
                         mode: 'series',
                         pattern: 'chessboard'
                      },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img20.png)

**Point mode**

To highlight a single point, you can set the **"point"** value to the [`mode`](../api/js/ejchart#members:series-selectionsettings-mode) option. 

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                   selectionSettings: {
                         enable: true, 
                         
                        //Change selection mode
                         mode: 'point',
                         // ...
                      },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img21.png)


**Cluster mode**

To select the points that corresponds to the same index in all the series, set the **"cluster"** value to the [`mode`](../api/js/ejchart#members:series-selectionsettings-mode) option.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                   selectionSettings: {
                         enable: true, 
                         
                        //Change selection mode
                         mode: 'cluster',
                         // ...
                      },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img22.png)



**Range mode**

To fetch the selected area data points value, you can set the selectionSettings [`mode`](../api/js/ejchart#members:series-selectionsettings-mode) as **range** in the chart series. The selection rectangle can be drawn as horizontally, vertically or in both direction by using [`rangeType`](../api/js/ejchart#members:series-selectionsettings-rangetype) property and the selected data’s are returned as an array collection in the [`rangeSelected`](../api/js/ejchart#events:rangeselected) event.  

{% highlight javascript %}


        $("#container").ejChart({
                    // ...
                    series:[{
                  
                        selectionSettings: {
                            enable: true, 
                         
                            //Change selection mode
                            mode: 'range',

                            //Enable both axis selection
                            rangeType:'xy'

                            // ...
                        }, 

                        // ... 
                    }],
                 //Subscribe the rangeSelected event. 
                 rangeSelected: "rangeSelection"  
                 // ...
           });

         //event to fetch the selected data point values
         rangeSelection:function (sender){
            var selectedData = sender.data.selectedDataCollection;
            //...
         }

{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img23.png)

[Click](https://ej2.syncfusion.com/home/#!/azure/chart/selection/rangeselection) here to view the Multiple data selection online demo sample.



### Selection Type

You can set two different selection type for selecting the data point and series on mouse click by using the [`type`](../api/js/ejchart#members:series-selectionsettings-type) property of the selectionSettings. 

* Single 
* Multiple 

**Single Type**

To select a data point or a series on mouse click based on the [`selectionSettings.mode`](../api/js/ejchart#members:series-selectionsettings-mode), set [`selectionSettings.type`](../api/js/ejchart#members:series-selectionsettings-type) as **"single"** in the series.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              commonSeriesOptions:{
                  			    
			    selectionSettings: {
			        enable: true,
                    //Selection mode is series or point ,cluster
			        mode: 'series',
                    //Selection type is single
			        type: 'single'
			    },
			}
 
               // ...
       });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img24.png)

**Multiple Type**

For selecting multiple data points or series on mouse click, set [`selectionSettings.type`](../api/js/ejchart#members:series-selectionsettings-type) as **"multiple"** in the series.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              commonSeriesOptions:{
                  			    
			    selectionSettings: {
			        enable: true,
                    //Selection mode is series or point ,cluster
			        mode: 'series',
                    //Selection type is multiple
			        type: 'multiple'
			    },
			}
 
               // ...
       });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img25.png)


### Customizing selection styles

To customize the selection styles, use the [`color`](../api/js/ejchart#members:series-selectionsettings-color), [`border`](../api/js/ejchart#members:series-selectionsettings-border) and [`opacity`](../api/js/ejchart#members:series-selectionsettings-opacity) options in the selectionSettings.
The border color and width can be customized using [`color`](../api/js/ejchart#members:series-selectionsettings-border-color) and [`width`](../api/js/ejchart#members:series-selectionsettings-border-width) property.

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                   selectionSettings: {
                         enable: true, 
                         
                        //Customizing selection rectangle styles
                         border: { width: '1.5', color: "red" },
                         opacity: 0.5, color: "red"
                         // ...
                      },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img26.png)


### Patterns for selection

EjChart provides pattern support for the data selection by setting the value to the [`pattern`](../api/js/ejchart#members:series-selectionsettings-pattern) property of the selectionSettings. The different types of selection patterns are as follows.

1.	chessboard
2.	crosshatch
3.	dots
4.	pacman
5.	grid
6.	turquoise
7.	star
8.	triangle
9.	circle
10.	tile
11.	horizontalDash
12.	verticalDash
13.	rectangle
14.	box
15.	verticalStripe
16.	horizontalStripe
17.	bubble
18.	diagonalBackward
19.	diagonalForward

{% highlight javascript %}


       $("#container").ejChart({   
	
              // ...
              series:[{
                  
                   selectionSettings: {
                         enable: true, 
                         
                        //Change selection pattern
                         pattern: "diagonalForward",
                         // ...
                      },
                    // ... 
               }]       
                    
               // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img27.png)


#### Custom pattern

To create a custom pattern for selecting the data points, set the [`pattern`](../api/js/ejchart#members:series-selectionsettings-pattern) type as **"custom"** and add the custom pattern **id** in the [`customPattern`](../api/js/ejchart#members:series-selectionsettings-custompattern) option of the selectionSettings.

{% highlight html %}


<body>
    <div id="container"></div>
            <svg>
                <pattern id="dots_a" patternUnits="userSpaceOnUse" width="6" height="6">
                    <rect x="0" y="0" width="6" height="6" transform="translate(0,0)" fill="black" opacity="1"></rect>
                    <path d='M 3 -3 L -3 3 M 0 6 L 6 0 M 9 3 L 3 9'stroke-width="1" stroke="white"></path>
                </pattern>
            </svg>
<script type="text/javascript">

   $("#container").ejChart({
            // ...
            series:[{
                selectionSettings: [{
                    enable: true,
                    //Add custom pattern for selection data
                    pattern: "custom",
                    customPattern: 'dots_a',
                    // ...
                }],
                // ...       
     });

        </script>
</body>

{% endhighlight %}


![](/js/Chart/User-Interactions_images/User-Interactions_img28.png)


### Handling Series Selection

To get the series information when selecting the specific series, subscribe to the [`seriesRegionClick`](../api/js/ejchart.html#events:seriesregionclick) event and set the **selectionSettings.mode** as **"series"**.

{% highlight javascript %}


       $("#container").ejChart({   
	
             // ... 
              series:[{
                selectionSettings: [{
                    enable: true,
                    //Change selection mode
                    mode: "series",
                    // ...
                }],
           
           //Subscribe series selection event
           seriesRegionClick: "seriesSelection",
            // ... 
        });

        function seriesSelection(sender) {
            //Get Series information on series selection
            var seriesData = sender.series;
        }

{% endhighlight %}


### Selection on Load

We can able to select the point/series programmatically on chart load, by setting series and point index in the [`selectedDataPointIndexes`](../api/js/ejchart#members:selecteddatapointindexes) property.

{% highlight javascript %}


       $("#container").ejChart({   
	
             // ... 
           
           //Added selected data point indexes

           selectedDataPointIndexes: [
               { seriesIndex:0 , pointIndex:2 },
               { seriesIndex:1 , pointIndex:4 }
           ],
            
            // ...

        });

{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img29.png)


## Data Editing

EjChart provides support to change the location of the rendered points. This can be done by dragging the point and dropping it on another location in chart. To enable the data editing, set the [`enable`] (../api/js/ejchart#members:series-dragsettings-enable) property to true in the [`drag settings`](../api/js/ejchart#members:series-dragsettings) of the series.

{% highlight javascript %}

$("#container").ejChart(
  {	  
      //Initializing Series
      series:[{     
              dragSettings:{     
		        enable: true
		}
           }]   
     });

{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img31.png)

[Click](https://ej2.syncfusion.com/home/#!/bootstrap/chart/UserInteraction/DataEditing) here to view the data editing online demo sample.

### Customize Dragging direction

To drag the point along x and y axes, you can specify [`type`] (../api/js/ejchart#members:series-dragsettings-type) as xy in drag settings. And to drag along x axis alone, specify the type as x and to drag along y axis, specify type as y.

{% highlight javascript %}

$("#container").ejChart(
  {	  
      //Initializing Series
      series:[{     
              dragSettings:{     
		        type: 'y'
		}
           }]   
     });

{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img32.png)
