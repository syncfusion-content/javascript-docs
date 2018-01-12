---
layout: post
title: Customizing the appearance of Essential JavaScript Chart
description: Learn how to customize the appearance of Chart using palettes, themes, color, background and animation. 
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Appearance

## Custom Color Palette

The Chart displays different series in different colors by default. You can customize the color of each series by providing a custom color palette of your choice by using the [`palette`](../api/ejchart#members:palette) property. 

{% highlight javascript %}

        $("#container").ejChart({
            
            //Providing a custom palette
            palette: [ "grey", "skyblue", "orange", ],         

            // ...
         });


{% endhighlight %}

![](/js/Chart/Appearance_images/Appearance_img1.png)


N> The Color palette is applied to the points in accumulation type series

## Built-in Themes

Following are the built-in themes available in the Chart

* flatlight
* flatdark
* gradientlight
* gradientdark
* azure
* azuredark
* lime
* limedark
* saffron
* saffrondark
* gradient-azure
* gradient-azuredark
* gradient-lime
* gradient-limedark
* gradient-saffron
* gradient-saffrondark


You can set your desired theme by using the [`theme`](../api/ejchart#members:theme) property. Flat light is the default theme used in the Chart.

{% highlight javascript %}

       $("#container").ejChart({
            
            //Using gradient theme
            theme: "gradientlight",         

            // ...
        });


{% endhighlight %}

![](/js/Chart/Appearance_images/Appearance_img2.png)


## Point level customization

[`Marker`](../api/ejchart#members:series-points-marker), [`data label`](../api/ejchart#members:series-points-marker-datalabel) and [`fill`](../api/ejchart#members:series-points-fill) color of each point in a series can be customized individually by using the [`points`](../api/ejchart#members:series-points) collection. The visibility of marker can be customized using [`visible`](../api/ejchart#members:series-points-marker-visible) property. The [`border`](../api/ejchart#members:series-points-marker-border) of marker shape can be customized using [`color`](../api/ejchart#members:series-points-marker-border-color) and [`width`](../api/ejchart#members:series-points-marker-border-width). 

The color of marker shape can be specified using [`fill`](../api/ejchart#members:series-points-marker-fill) property.To display the image as marker, need to specify [`imageURL`](../api/ejchart#members:series-points-marker-imageurl). The [`opacity`](../api/ejchart#members:series-points-marker-opacity), [`shape`](../api/ejchart#members:series-points-marker-shape), [`width`](../api/ejchart#members:series-points-marker-size-width), [`height`](../api/ejchart#members:series-points-marker-size-height) of marker [`size`](../api/ejchart#members:series-points-marker-size) also be used to customize the points.

{% highlight javascript %}

       $("#container").ejChart({
            
           series: [{
                //Customizing marker and fill color of a point
                     points: [
                         {  
                            x : 0,
                            y: 210, 
                            fill: "#E27F2D",
                            marker: { 
                                 visible: true,
                                 // ...
                               }
                         },
                       // ...
                      ],         
                 // ...
            }],
            // ...

        });


{% endhighlight %}

![](/js/Chart/Appearance_images/Appearance_img3.png)

The [`border`](../api/ejchart#members:series-points-border) [`color`](../api/ejchart#members:series-points-border-color) and [`width`](../api/ejchart#members:series-points-border-width) property is used to customize the point border. This is applicable only for column type series and accumulation type series. The visibility of legend items can be enabled or disabled using [`visibleOnLegend`](../api/ejchart#members:series-points-visibleonlegend). 

The [`showIntermediateSum`](../api/ejchart#members:series-points-showintermediatesum) property shows/hides the intermediate summary from the last intermediate point. To show/hide the total summary of the waterfall series, [`showTotalSum`](../api/ejchart#members:series-points-showtotalsum) property can be used.

The close and open value of a point can be specified using [`open`](../api/ejchart#members:series-points-open) and [`close`](../api/ejchart#members:series-points-close) property. It is applicable only for financial type series. The [`size`](../api/ejchart#members:series-points-size) property is used to customize the bubble size in the bubble series. The data label text for the point can be provided using [`text`](../api/ejchart#members:series-points-text) property.

{% highlight javascript %}

       $("#container").ejChart({
            
           series: [{
                //Customizing border of a point
                     points: [
                         {  
                           text: 'Others',
                           border:{color : "green", width : 2},
                           visibleOnLegend: "hidden",
                           showIntermediateSum : true,
                           showTotalSum : true,
                           close : 50,
						   open : 50,
                           size : 5
                         },
                       // ...
                      ],         
                 // ...
            }],
            // ...

        });


{% endhighlight %}

## Series border customization

To customize the series border [`color`](../api/ejchart#members:series-border-color), [`width`](../api/ejchart#members:series-border-width) and [`dashArray`](../api/ejchart#members:series-border-dasharray), you can use [`border`](../api/ejchart#members:series-border) option. 

N> Series border can be applied to all the series (except Line, Spline, HiLo, HiLoOpenClose and StepLine series).

{% highlight javascript %}

  $("#container").ejChart({

            //...
            series: [{
                  
                //Change the color, width and dashArray to customize the border of series
                border: { color: "blue", width: 2, dashArray: "5,3" }
                //...
           }]

                //...
     });


{% endhighlight %}

![](/js/Chart/Appearance_images/Appearance_img4.png)

## Series font customization

To customize the series font color[`color`](../api/ejchart#members:series-font-color), [`fontFamily`](../api/ejchart#members:series-font-fontfamily), [`fontStyle`](../api/ejchart#members:series-font-fontstyle), [`fontWeight`](../api/ejchart#members:series-font-fontweight), [`opacity`](../api/ejchart#members:series-font-opacity) and [`size`](../api/ejchart#members:series-font-size), you can use [`font`](../api/ejchart#members:series-font) option. 

{% highlight javascript %}

  $("#container").ejChart({

            //...
            series: [{
                  
                //Change the color, fontFamily, fontStyle, fontWeight, opacity and size to customize the font of series
                font: { 
                    color : "green", 
                    fontFamily : "Algerian", 
                    fontStyle : "italic", 
                    fontWeight : "lighter", 
                    opacity : 0.5,
                    size : "14px" 
                }
                //...
           }]

                //...
     });


{% endhighlight %}

## Customizing Name and Opacity of Chart Series

The series name to be displayed on the legend can be provided using [`name`](../api/ejchart#members:series-name) property. The [`opacity`](../api/ejchart#members:series-opacity) property is used to provide the series opacity.

{% highlight javascript %}

    $("#container").ejChart({
            series :[{ 
                name: 'India',
                opacity : 0.5
            }]                  
    });

{% endhighlight %}

## Customizing data points fill color

The [`palette`](../api/ejchart#members:series-palette) is the field name in data source where fill color for all the data points is generated.

{% highlight javascript %}

    $("#container").ejChart({
        series :[{palette : "ColorFieldName"}]                  
    });

{% endhighlight %}

## Chart area customization


The [`chartArea`](../api/ejchart#members:chartarea) is the plot area of the chart.

### Customize chart background

The Chart background can be customized by using the [`background`](../api/ejchart#members:background) property of the Chart. To customize the chart border, use [`border`](../api/ejchart#members:border) option of the chart. 

The Chart border can be customized by using the [`color`](../api/ejchart#members:border-color),[`width`](../api/ejchart#members:border-width) and [`opacity`](../api/ejchart#members:border-opacity) properties.

{% highlight javascript %}

       $("#container").ejChart({
       
            // ...
            
            //Customizing Chart background
            background: "skyblue",   
              
            //Customize the chart border and opacity
            border: {color: "#FF0000", width: 2, opacity: 0.35}, 
                      
            // ...

        });


{% endhighlight %} 

![](/js/Chart/Appearance_images/Appearance_img5.png)


**Chart Margin**

The Chart [`margin`](../api/ejchart#members:margin) property is used to add the margin to the chart area at the left, right, top and bottom position.
The [`left`](../api/ejchart#members:margin-left),[`right`](../api/ejchart#members:margin-right),[`top`](../api/ejchart#members:margin-top),
[`bottom`](../api/ejchart#members:margin-bottom) properties are used to add the margin space in respective positions.

{% highlight javascript %}

       $("#container").ejChart({
       
            // ...
            
            //Change chart margin to left, right, top and bottom
            margin: { left: 40, right: 40, top: 40, bottom: 40 }, 
                      
            // ...

        });


{% endhighlight %} 

![](/js/Chart/Appearance_images/Appearance_img6.png)

**Setting background image**

Background image can be added to the chart by using the [`backGroundImageUrl`](../api/ejchart#members:backgroundimageurl) property.

{% highlight javascript %}

       $("#container").ejChart({
       
            // ...
            
            //Setting an image as Chart background 
            backGroundImageUrl: "images/chart/wheat.png",                
                      
            // ...

        });


{% endhighlight %} 

![](/js/Chart/Appearance_images/Appearance_img7.png)

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/tooltiptemplate) here to view our online demo sample for setting Chart background image.


**Chart area background**

The Chart area background can be customized by using the [`background`](../api/ejchart#members:chartarea-background) property in the chart area. 

{% highlight javascript %}

       $("#container").ejChart({
       
            // ...
            
           chartArea: {            
                 //Setting background for Chart area
                 background: "skyblue"
            },               
                      
            // ...

        });


{% endhighlight %} 

![](/js/Chart/Appearance_images/Appearance_img8.png)


**Chart area border**

The Chart area border can be customized by using the [`border`](../api/ejchart#members:chartarea-border) property in the chart area.
The color,opacity and width of the borders can be customized using the [`color`](../api/ejchart#members:chartarea-border-color),[`width`](../api/ejchart#members:chartarea-border-width),[`opacity`](../api/ejchart#members:chartarea-border-opacity) properties present inside the border option of the chart area.

{% highlight javascript %}

       $("#container").ejChart({
       
            // ...
            
           chartArea: {            
                 //Setting border for Chart area
                 border:{ color: "red", width:5, opacity:0.4 }
            },               
                      
            // ...

        });


{% endhighlight %} 


### Customize chart area grid bands

You can provide different color for alternate grid rows and columns formed by the grid lines in the chart area by using the [`alternateGridBand`](../api/ejchart#members:primaryxaxis-alternategridband) property of the axis. The properties [`odd`](../api/ejchart#members:primaryxaxis-alternategridband-odd) and [`even`](../api/ejchart#members:primaryxaxis-alternategridband-even) are used to customize the grid bands at odd and even positions respectively. 

{% highlight javascript %}

       $("#container").ejChart({
       
            // ...
       
            //Creating horizontal grid bands in chart area
            primaryYAxis: {            
            
               //Customizing horizontal grid bands at even position
               alternateGridBand: {                 
                   even: {
                            fill: "#A7A9AB", 
                            opacity: 0.1,
                          }  }
                   // ...               
            },
            // ...

        });


{% endhighlight %} 

![](/js/Chart/Appearance_images/Appearance_img9.png)

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/alternategridband) here to view the alternate grid band online demo sample.


### Animation

You can enable animation by using the [`enableAnimation`](../api/ejchart#members:series-enableanimation) property of the series. This animates the chart series on two occasions – when the chart is loaded for the first time or whenever you change the series type by using the type property.

{% highlight javascript %}

       $("#container").ejChart({
       
            // ...
       
            series : [{

                 //Enabling animation of series
                 enableAnimation: true,    

                 // ...    
            }],
            // ...

        });


{% endhighlight %}

However, you can force the chart to animate series by calling the animate method as illustrated in the following code example,

{% highlight javascript %}

       $("#container").ejChart({
            series : [{

                 //Enabling animation of series
                 enableAnimation: true,    

                 // ...    
            }],
            // ...
       });

      //Dynamically animating Chart
      function animateChart(){

           //Calling the animate method for dynamic animation
           $("#container").ejChart("animate");      
        
      }


{% endhighlight %}

### Control the Speed of animation

To control the speed of animation, you can use the [`animationDuration`](../api/ejchart#members:series-animationduration) property in the series. 

{% highlight javascript %}

       $("#container").ejChart({
       
            // ...
       
            series : [{

                 //Enabling animation of series
                 enableAnimation: true,
                 animationDuration: "2000",    

                 // ...    
            }],
            // ...

        });


{% endhighlight %}


