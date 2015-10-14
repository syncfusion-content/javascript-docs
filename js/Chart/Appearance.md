---
layout: post
title: Appearance
description: appearance
platform: js
control: Chart
documentation: ug
---

# Appearance

## Custom Color Palette

The Chart displays different series in different colors by default. You can customize the color of each series by providing a custom color palette of your choice by using the [palette](../api/ejchart#members:palette) property. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            
            //Providing a custom palette
            palette: [ "grey", "skyblue", "orange", ],         

            // ...
         });


{% endhighlight %}

{% include image.html url="/js/Chart/Appearance_images/Appearance_img1.png" Caption="Chart custom color palette"%}

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


You can set your desired theme by using the [theme](../api/ejchart#members:theme) property. Flat light is the default theme used in the Chart.

{% highlight js %}

       $("#chartcontainer").ejChart({
            
            //Using gradient theme
            theme: "gradientlight",         

            // ...
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Appearance_images/Appearance_img2.png" Caption="Chart using gradient light theme"%}


## Point level customization

Marker, data label and fill color of each point in a series can be customized individually by using the [points](../api/ejchart#members:series-points) collection.

{% highlight js %}

       $("#chartcontainer").ejChart({
            
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

{% include image.html url="/js/Chart/Appearance_images/Appearance_img3.png" Caption="Customize a specific point marker and color"%}


## Chart area customization

### Customize chart background

The Chart background can be customized by using the [background](../api/ejchart#members:background) property of the Chart. To customize the chart border, use [border](../api/ejchart#members:border) option of the chart. 

{% highlight js %}

       $("#chartcontainer").ejChart({
       
            // ...
            
            //Customizing Chart background
            background: "skyblue",   
              
            //Customize the chart border and opacity
            border: {color: "#FF0000", width: 2, opacity: 0.35}, 
                      
            // ...

        });


{% endhighlight %} 

{% include image.html url="/js/Chart/Appearance_images/Appearance_img4.png" Caption="Customizing chart background and border"%}

**Chart Margin**

The Chart [margin](../api/ejchart#members:margin) property is used to add the margin to the chart area at the left, right, top and bottom position.

{% highlight js %}

       $("#chartcontainer").ejChart({
       
            // ...
            
            //Change chart margin to left, right, top and bottom
            margin: { left: 40, right: 40, top: 40, bottom: 40 }, 
                      
            // ...

        });


{% endhighlight %} 

{% include image.html url="/js/Chart/Appearance_images/Appearance_img5.png" Caption="Customizing chartarea margin"%}


**Setting background image**

Background image can be added to the chart by using the [backGroundImageUrl](../api/ejchart#members:backgroundimageurl) property.

{% highlight js %}

       $("#chartcontainer").ejChart({
       
            // ...
            
            //Setting an image as Chart background 
            backGroundImageUrl: "images/chart/wheat.png",                
                      
            // ...

        });


{% endhighlight %} 

{% include image.html url="/js/Chart/Appearance_images/Appearance_img6.png" Caption="Add background image to chart"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/tooltiptemplate) here to view our online demo sample for setting Chart background image.


**Chart area background**

The Chart area background can be customized by using the [background](../api/ejchart#members:chartarea-background) property in the chart area. 

{% highlight js %}

       $("#chartcontainer").ejChart({
       
            // ...
            
           chartArea: {            
                 //Setting background for Chart area
                 background: "skyblue"
            },               
                      
            // ...

        });


{% endhighlight %} 

{% include image.html url="/js/Chart/Appearance_images/Appearance_img7.png" Caption="Add background color to chart area"%}


### Customize chart area grid bands

You can provide different color for alternate grid rows and columns formed by the grid lines in the chart area by using the [alternateGridBand](../api/ejchart#members:primaryxaxis-alternategridband) property of the axis. The properties [odd](../api/ejchart#members:primaryxaxis-alternategridband-odd) and [even](../api/ejchart#members:primaryxaxis-alternategridband-even) are used to customize the grid bands at odd and even positions respectively. 

{% highlight js %}

       $("#chartcontainer").ejChart({
       
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

{% include image.html url="/js/Chart/Appearance_images/Appearance_img8.png" Caption="Customizing chart area grid bands"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/alternategridband) here to view the alternate grid band online demo sample.


### Animation

You can enable animation by using the [enableAnimation](../api/ejchart#members:series-enableanimation) property of the series. This animates the chart series on two occasions – when the chart is loaded for the first time or whenever you change the series type by using the type property.

{% highlight js %}

       $("#chartcontainer").ejChart({
       
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

{% highlight js %}

       $("#chartcontainer").ejChart({
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
           $("#chartcontainer").ejChart("animate");      
        
      }


{% endhighlight %}

