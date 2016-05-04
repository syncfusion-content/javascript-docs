---
layout: post
title: Customizing the appearance of Essential JavaScript Chart
description: Learn how to customize the appearance of Chart using palettes, themes, color, background and animation. 
platform: js
control: Chart
documentation: ug
---

# Appearance

## Custom Color Palette

The Chart displays different series in different colors by default. You can customize the color of each series by providing a custom color palette of your choice by using the [`palette`](../api/ejchart#members:palette) property. 

{% highlight javascript %}

        $("#chartcontainer").ejChart({
            
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

       $("#chartcontainer").ejChart({
            
            //Using gradient theme
            theme: "gradientlight",         

            // ...
        });


{% endhighlight %}

![](/js/Chart/Appearance_images/Appearance_img2.png)


## Point level customization

Marker, data label and fill color of each point in a series can be customized individually by using the [`points`](../api/ejchart#members:series-points) collection.

{% highlight javascript %}

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

![](/js/Chart/Appearance_images/Appearance_img3.png)

## Column Width customization

Width of the column type series can be customized by using the [`columnWidth`](../api/ejchart#members:series-columnwidth) property. Default value of [`columnWidth`](../api/ejchart#members:series-columnwidth) is 0.7. Value ranges from 0 to 1. Here 1 corresponds to 100% of available width and 0 corresponds to 0% of available width.

N> Width of a column also depends upon the [`columnSpacing`](../api/ejchart#members:series-columnspacing) property, because [`columnSpacing`](../api/ejchart#members:series-columnSpacing) will reduce the space available for drawing a column

{% highlight javascript %}

    $('#container').ejChart({

		//Common settings for all series
		commonSeriesOptions: {
    
			//Width of columns in column type series
			columnWidth: 0.7

			//...        
		},

		//Settings specific to individual series
		series: [{
		
			//Width of columns in column type series
			columnWidth: 0.8

			//... 
		}],

		//...

	});	

{% endhighlight %}

![](/js/Chart/Appearance_images/Appearance_img10.png)

## Spacing between Column Series

Spacing between column type series can be customized using the [`columnSpacing`](../api/ejchart#members:series-columnspacing) property. Default value of [`columnSpacing`](../api/ejchart#members:series-columnspacing) is 0. Value ranges from 0 to 1. Here 1 corresponds to 100% available space and 0 corresponds to 0% available space.

N> Column spacing will also affect the width of the column. For example, setting 20% spacing and 100% width will render columns with 80% of total width.

{% highlight javascript %}

    $('#container').ejChart({

		//Common settings for all series
		commonSeriesOptions: {
    
			//Spacing between column series
		columnSpacing: 0,

			//...
		},

		//Settings specific to individual series
		series: [{
    
			//Spacing between column series
			columnSpacing: 0.2,
	
			//...
		}],

		//...

	});

{% endhighlight %}

![](/js/Chart/Appearance_images/Appearance_img11.png)

## Series border customization

To customize the series border color, width and dashArray, you can use [`series.border`](../api/ejchart#members:series-border) option. 

N> Series border can be applied to all the series (except line, spline, hilo, hiloopenclose and stepline series).

{% highlight javascript %}

  $("#chartcontainer").ejChart({

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

## Chart area customization

### Customize chart background

The Chart background can be customized by using the [`background`](../api/ejchart#members:background) property of the Chart. To customize the chart border, use [`border`](../api/ejchart#members:border) option of the chart. 

{% highlight javascript %}

       $("#chartcontainer").ejChart({
       
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

{% highlight javascript %}

       $("#chartcontainer").ejChart({
       
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

       $("#chartcontainer").ejChart({
       
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

       $("#chartcontainer").ejChart({
       
            // ...
            
           chartArea: {            
                 //Setting background for Chart area
                 background: "skyblue"
            },               
                      
            // ...

        });


{% endhighlight %} 

![](/js/Chart/Appearance_images/Appearance_img8.png)


### Customize chart area grid bands

You can provide different color for alternate grid rows and columns formed by the grid lines in the chart area by using the [`alternateGridBand`](../api/ejchart#members:primaryxaxis-alternategridband) property of the axis. The properties [`odd`](../api/ejchart#members:primaryxaxis-alternategridband-odd) and [`even`](../api/ejchart#members:primaryxaxis-alternategridband-even) are used to customize the grid bands at odd and even positions respectively. 

{% highlight javascript %}

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

![](/js/Chart/Appearance_images/Appearance_img9.png)

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/alternategridband) here to view the alternate grid band online demo sample.


### Animation

You can enable animation by using the [`enableAnimation`](../api/ejchart#members:series-enableanimation) property of the series. This animates the chart series on two occasions – when the chart is loaded for the first time or whenever you change the series type by using the type property.

{% highlight javascript %}

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

{% highlight javascript %}

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

