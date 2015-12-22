---
layout: post
title: Interactions available in Essential JavaScript Chart
description: What are the interactions available in Chart like tooltip, crosshair, trackball, highlighting, zooming and panning, etc..,
platform: js
control: Chart
documentation: ug
---

# User Interactions

## Tooltip

### Enable tooltip for data point

Tooltip for the data points can be enabled by using the [`visible`](../api/ejchart#members:series-tooltip-visible) option of the [`tooltip`](../api/ejchart#members:series-tooltip) in the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
           
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

Chart with tooltip
{:.caption}

### Format the tooltip 

Tooltip displays data specified by the [`format`](../api/ejchart#members:series-tooltip-format) option of the tooltip. The default value of the format option is * **#point.x# : #point.y#** *. Here, * **#point.x#** * is the placeholder for x value of the point and * **#point.y#** * is the placeholder for y value of the point.

You can also use * **#series.<optionname>#** * as placeholder to display the value of an option in corresponding series and use * **#point.<optionname>#** * as place holder to display the value of an option in the corresponding point.

{% highlight js %}


        $("#chartcontainer").ejChart({
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

Chart with formatted tooltip
{:.caption}


### Tooltip Template

HTML elements can be displayed in the tooltip by using the [`template`](../api/ejchart#members:series-tooltip-template) option of the tooltip. The template option takes the value of the id attribute of the HTML element. You can use the * **#point.x#** * and * **#point.y#** * as place holders in the HTML element to display the x and y values of the corresponding data point. 

You can also use * **#series.<optionname>#** * as place holder to display the value of an option in corresponding series of the tooltip and use * **#point.<optionname>#** * as place holder to display the value of an option in the corresponding point for which the tooltip is displayed.
  

{% highlight html %}

<body>
   <div id="chartcontainer"></div>
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
   $("#chartcontainer").ejChart({   
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

Chart with tooltip template
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/line) here to view the Tooltip template online demo sample.


#### Tooltip template animation

You can enable animation by setting the [`enableAnimation`](../api/ejchart#members:series-tooltip-enableanimation) to true. Tooltip animates when the mouse moves from one data point to another point. The [`duration`](../api/ejchart#members:series-tooltip-duration) property in tooltip specifies the time taken to animate the tooltip. the duration is set to **"500ms"**, by default.

N> Tooltip is animated only if the template is specified for tooltip.

{% highlight js %}


        $("#chartcontainer").ejChart({
            
            // ...
            series: [{
                  tooltip: {
                    //Enable tooltip template animation and set duration time
                    enableAnimation: true, duaration: "1000ms",                                      
                    // ...
                 }
             }],
             
            // ...
        });


{% endhighlight %}


### Customize the appearance of tooltip   

The [`fill`](../api/ejchart#members:series-tooltip-fill) and [`border`](../api/ejchart#members:series-tooltip-border) options are used to customize the background color and border of the tooltip respectively. The [`font`](../api/ejchart#members:series-tooltip-font) option in the tooltip is used to customize the font of the tooltip text.

{% highlight js %}


        $("#chartcontainer").ejChart({
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

Customizing the appearance of tooltip 
{:.caption}


#### Tooltip with rounded corners

The options [`rx`](../api/ejchart#members:series-tooltip-rx) and [`ry`](../api/ejchart#members:series-tooltip-ry) are used to customize the corner radius of the tooltip rectangle.

{% highlight js %}


        $("#chartcontainer").ejChart({
           
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

Tooltip with rounded corners
{:.caption}



## Zooming and Panning

### Enable Zooming

There are two ways you can zoom the chart,

* When the [`zooming.enable`](../api/ejchart#members:zooming-enable) option is set to true, you can zoom the chart by using the rubber band selection.

* When the [`zooming.enableMouseWheel`](../api/ejchart#members:zooming-enablemousewheel) option is set to true, you can zoom the chart on mouse wheel scrolling. 

{% highlight js %}


        $("#chartcontainer").ejChart({
             //  ...             
	         //Enable zooming in chart
             zooming: {enable: true}
             // ...
        });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img6.png)

Zoomed chart
{:.caption}


After zooming the chart, a zooming toolbar will appear with options to *zoom*, *pan* and *reset*. Selecting the Pan option will allow to pan the chart and selecting the Reset option will reset the zoomed chart.

![](/js/Chart/User-Interactions_images/User-Interactions_img7.png)

Select panning option from zoomkit
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/userinteraction/zoomingandpanning) here to view the Zooming and Panning online demo sample.


### Types of zooming

The [`type`](../api/ejchart#members:zooming-type) option in zooming specifies whether the chart is allowed to scale along the horizontal axis or vertical axis or along both axis. The default value of the [`type`](../api/ejchart#members:zooming-type) is **"xy"** (both axis).

{% highlight js %}


        $("#chartcontainer").ejChart({
             //  ...             
	         zooming: {
                    enable: true,
                    //Enable horizontal zooming
                    type: 'x'
                } 
             // ...
        });


{% endhighlight %}


## Crosshair

Crosshair is used to view the value of an axis at mouse position or touch contact point. 

### Enable crosshair and crosshair label

Crosshair can be enabled by using the [`visible`](../api/ejchart#members:series-tooltip-visible) option in the [`crosshair`](../api/ejchart#members:crosshair). Crosshair label for an axis can be enabled by using the [`visible`](../api/ejchart#members:primaryxaxis-crosshairlabel-visible) option of [`crosshairLabel`](../api/ejchart#members:primaryxaxis-crosshairlabel) in the corresponding axis.


{% highlight js %}


        $("#chartcontainer").ejChart({
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

![](/js/Chart/User-Interactions_images/User-Interactions_img8.png)

Chart with crosshair
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/userinteraction/crosshair) here to view the Crosshair online demo sample.


### Customize the crosshair line and crosshair label

The [`fill`](../api/ejchart#members:crosshair-fill) and [`border`](../api/ejchart#members:crosshair-border) options of the [`crosshairLabel`](../api/ejchart#members:crosshairlabel) is used to customize the background color and border of the crosshair label respectively. Color and width of the crosshair line can be customized by using the [`line`](../api/ejchart#members:crosshair-line) option in the [`crosshair`](../api/ejchart#members:crosshair).

{% highlight js %}


        $("#chartcontainer").ejChart({
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

![](/js/Chart/User-Interactions_images/User-Interactions_img9.png)

Customize crosshair labels and line
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/userinteraction/crosshair) here to view the Crosshair online demo sample.



## Trackball

Trackball is used to track a data point close to the mouse position or touch contact point. Trackball marker indicates the closest point and trackball tooltip displays the information about the point.

### Enable Trackball

Trackball can be enabled by setting the [`visible`](../api/ejchart#members:crosshair-visible) option of the crosshair to *true* and then set the [`type`](../api/ejchart#members:crosshair-type) as **"trackball"**. The default value of type is **"crosshair"**.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
             crosshair: {
                   visible: true,
                   //Change crosshair type to trackball
                   type: 'trackball',
                  } 
           //......
           });


{% endhighlight %}


![](/js/Chart/User-Interactions_images/User-Interactions_img10.png)

Chart with trackball
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/userinteraction/trackball) here to view the Trackball online demo sample.


#### Customize trackball marker and trackball line

Shape and size of the trackball marker can be customized by using the [`shape`](../api/ejchart#members:crosshair-marker-shape) and [`size`](../api/ejchart#members:crosshair-marker-size) options of the crosshair marker. Color and width of the trackball line can be customized by using the [`line`](../api/ejchart#members:crosshair-line) option in the crosshair.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img11.png)

Customize trackball line and marker
{:.caption}


### Format Trackball tooltip

X and Y values displayed in the trackball tooltip are formatted based on its axis [`labelFormat`](../api/ejchart#members:primaryxaxis-labelformat).  

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
              // ...
              primaryXAxis: {
                   labelFormat: 'MMM, yyyy',
                   //.............
               },
              
              primaryYAxis: {
                    labelFormat: '{value}K',
                    //.............
               },
               
               crosshair: {
                    visible: true,
                    type: 'trackball',                           
                }
                  // ...
           });


{% endhighlight %}

![](/js/Chart/User-Interactions_images/User-Interactions_img12.png)

Change trackball tooltip format
{:.caption}


## Highlight

EjChart provides highlighting support for the series and data points on mouse hover. To enable the highlighting option, set the [`enable`](../api/ejchart#members:series-highlightsettings-enable) property to *true* in the [`highlightsettings`](../api/ejchart#members:series-highlightsettings) of the series.

N> When hovering mouse on the data points, the corresponding series legend also will be highlighted.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/selection) here to view the highlight and selections online demo sample.


### Highlight Mode

You can set three different highlight mode for the highlighting data point and series by using the [`mode`](../api/ejchart#members:series-highlightsettings-mode) property of the [`highlightsettings`](../api/ejchart#members:series-highlightsettings).

* Series
* Points
* Cluster

**Series mode**

To highlight all the data points of the specified series, you can set the **“series”** value to the [`mode`](../api/ejchart#members:series-highlightsettings-mode) option in the highlighSettings. 


{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img13.png)

Highlighting chart series
{:.caption}


**Point mode**

To highlight a single point, you can set the **“point”** value to the [`mode`](../api/ejchart#members:series-highlightsettings-mode) option.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img14.png)

Highlighting chart point
{:.caption}


**Cluster mode**

To highlight the points that corresponds to the same index in all the series, set the **“cluster”** value to the [`mode`](../api/ejchart#members:series-highlightsettings-mode) option.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img15.png)

Highlighting chart in cluster mode
{:.caption}


### Customize the highlight styles

To customize the highlighted series, use the [`color`](../api/ejchart#members:series-highlightsettings-color), [`border`](../api/ejchart#members:series-tooltip-border) and [`opacity`](../api/ejchart#members:series-highlightsettings-opacity) options in the highlightSettings.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img16.png)

Customizing highlight styles
{:.caption}


### Patterns to highlight

EjChart provides pattern support for highlighting the data by setting the value to the [`pattern`](../api/ejchart#members:series-highlightsettings-pattern) property of the highlightSettings. The different types of highlight patterns are as follows.

1.	chessboard
2.	crosshatch
3.	dots
4.	packman
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

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img17.png)

Changing pattern to highlight
{:.caption}


#### Custom pattern

To create a custom pattern for the highlighting data points, set the pattern type as **"custom"** and add the custom pattern **id** in the [`customPattern`](../api/ejchart#members:series-highlightsettings-custompattern) option of the highlightSettings.

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

EjChart provides selection support for the series and data points on mouse click. To enable the selection option, set the [`enable`](../api/ejchart#members:series-selectionsettings-enable) property to *true* in the [`selectionSettings`](../api/ejchart#members:series-selectionSettings) of the series.

N> When mouse is clicked on the data points, the corresponding series legend also will be selected.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/selection) here to view the highlight and selections online demo sample.


### Selection Mode

You can set three different selection mode for highlighting the data point and series by using the [`mode`](../api/ejchart#members:series-selectionsettings-mode) property of the selectionSettings.

* Series
* Points
* Cluster

**Series mode**

To select all the data points of the specified series, you can set the **"series"** value to the [`mode`](../api/ejchart#members:series-selectionsettings-mode) option in the selectionSettings.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img18.png)

Series selection
{:.caption}


**Point mode**

To highlight a single point, you can set the **"point"** value to the [`mode`](../api/ejchart#members:series-selectionsettings-mode) option. 

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img19.png)

Point selection
{:.caption}


**Cluster mode**

To select the points that corresponds to the same index in all the series, set the **"cluster"** value to the [`mode`](../api/ejchart#members:series-selectionsettings-mode) option.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img20.png)

Cluster selection
{:.caption}


### Customizing selection styles

To customize the selection styles, use the [`color`](../api/ejchart#members:series-selectionsettings-color), [`border`](../api/ejchart#members:series-selectionsettings-border) and [`opacity`](../api/ejchart#members:series-selectionsettings-opacity) options in the selectionSettings.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img21.png)

Customizing selection styles
{:.caption}


### Patterns for selection

EjChart provides pattern support for the data selection by setting the value to the [`pattern`](../api/ejchart#members:series-selectionsettings-pattern) property of the selectionSettings. The different types of selection patterns are as follows.

1.	chessboard
2.	crosshatch
3.	dots
4.	packman
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

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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

![](/js/Chart/User-Interactions_images/User-Interactions_img22.png)

Selection pattern
{:.caption}


#### Custom pattern

To create a custom pattern for selecting the data points, set the [`pattern`](../api/ejchart#members:series-selectionsettings-pattern) type as **"custom"** and add the custom pattern **id** in the [`customPattern`](../api/ejchart#members:series-selectionsettings-custompattern) option of the selectionSettings.

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


![](/js/Chart/User-Interactions_images/User-Interactions_img23.png)

Add custom pattern for selection
{:.caption}


### Handling Series Selection

To get the series information when selecting the specific series, subscribe to the [`seriesRegionClick`](../api/ejchart.html#events:seriesregionclick) event and set the **selectionSettings.mode** as **"series"**.

{% highlight js %}


       $("#chartcontainer").ejChart({   
	
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




