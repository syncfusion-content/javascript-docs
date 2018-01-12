---
layout: post
title: Trendlines in Essential JavaScript Chart
description: What are the different types of trendlines available in chart.
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Trendlines

EjChart can generate Trendlines for Cartesian type series *(Line, Column, Scatter, Area, Candle, HiLo etc.)* except bar type series. You can add more than one trendline object to the [`trendlines`](../api/ejchart#members:series-trendlines) option.
The visibility of the trendline is controlled by using the [`visibility`](../api/ejchart#members:series-trendlines-visibility) property.

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //Enable Trendline to chart series
                       visibility: "visible", type: "linear"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img1.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/trendlines) here to view the Trendlines online demo sample.


## Customize the trendline styles

A trendline can be customized by using the properties such as [`fill`](../api/ejchart#members:series-trendlines-fill), [`width`](../api/ejchart#members:series-trendlines-width), [`dashArray`](../api/ejchart#members:series-trendlines-dasharray) and [`opacity`](../api/ejchart#members:series-trendlines-opacity). The default type of trendline is **"linear"**.

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                         //...
                         //Customize the Trendline styles
                         fill: '#99CCFF', width: 3, opacity: 1, dashArray: '2,3'
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img2.png)



## Types of Trendline

EjChart supports the following type of Trendlines.

* Linear
* Exponential
* Logarithmic
* Power 
* Polynomial
* MovingAverage

### Linear

To render Linear Trendline, you have to set the [`type`](../api/ejchart#members:series-trendlines-type) as **"linear"**. 

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "linear"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img3.png)


### Exponential

Exponential Trendline can be rendered by setting the [`type`](../api/ejchart#members:series-trendlines-type) as **"exponential"**. 

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "exponential"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img4.png)


### Logarithmic

Logarithmic Trendline can be rendered by setting the [`type`](../api/ejchart#members:series-trendlines-type) as **"Logarithmic"**.  

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "logarithmic"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img5.png)


### Power

Power Trendline can be rendered by setting the [`type`](../api/ejchart#members:series-trendlines-type) of the trendline as **"power"**. 

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "power"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img6.png)


### Polynomial

Polynomial Trendline can be rendered by setting the trendline [`type`](../api/ejchart#members:series-trendlines-type) as **"polynomial"**.  You can change the polynomial order by using the [`polynomialOrder`](../api/ejchart#members:series-trendlines-polynomialorder) of the trendlines. It ranges from 2 to 6.

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "polynomial"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img7.png)



### MovingAverage

MovingAverage Trendline can be rendered by setting the [`type`](../api/ejchart#members:series-trendlines-type) of the trendline as **"movingAverage"**. 

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type and set [`period`](../api/ejchart#members:series-trendlines-period) for moving average
                       type: "movingAverage", period: 3
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img8.png)

## Forecasting

**Trendline forecasting** is the prediction of future/past situations.  **Forecasting** can be classified into two types as follows.

  * Forward Forecasting
  * Backward Forecasting

### Forward Forecasting

The value set for [`forwardForecast`](../api/ejchart#members:series-trendlines-forwardforecast) is used to determine the distance moving towards the future trend.

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //...
                       //Set forward forecasting value
                       forwardForecast: 5
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img9.png)



### Backward Forecasting

The value set for the [`backwardForecast`](../api/ejchart#members:series-trendlines-backwardforecast) is used to determine the past trends.

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //...
                       //Set forward forecasting value
                       backwardForecast: 5
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img10.png)


## Trendlines Legend

To display the legend item for trendline, use the [`name`](../api/ejchart#members:series-trendlines-name) property. You can interact with the trendline legends similar to the series legends *(show/hide trendlines on legend click)*.  

{% highlight javascript %}

        $("#container").ejChart({
            series:[{
                  trendlines: [{
                       //...
                       //Set Trendline name to display in the legend
                       name: 'Linear'
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](/js/Chart/Trendlines_images/Trendlines_img11.png)

## Trendlines Intercept and visibleOnLegend

The trendline intercept value can be provided using [`intercept`](../api/ejchart#members:series-trendlines-intercept) property. The [`visibleOnLegend`](../api/ejchart#members:series-trendlines-visibleonlegend) shows/hides the trendline legend.

{% highlight javascript %}

    $("#container").ejChart({
        series :[{ 
          trendlines:[{ 
              intercept : 10,
              visibleOnLegend:'hidden'
          }]
        }]                 
    });

{% endhighlight %}

## Trendlines Tooltip

The trendline [`tooltip`](../api/ejchart#members:series-trendlines-tooltip) can be customized using options like [`color`](../api/ejchart#members:series-trendlines-tooltip-border-color) and [`width`](../api/ejchart#members:series-trendlines-tooltip-border-width) of [`border`](../api/ejchart#members:series-trendlines-tooltip-border), [`rx`](../api/ejchart#members:series-trendlines-tooltip-rx), [`ry`](../api/ejchart#members:series-trendlines-tooltip-ry), [`duration`](../api/ejchart#members:series-trendlines-tooltip-duration), [`enableAnimation`](../api/ejchart#members:series-trendlines-tooltip-enableanimation), [`fill`](../api/ejchart#members:series-trendlines-tooltip-fill), [`format`](../api/ejchart#members:series-trendlines-tooltip-format) and [`opacity`](../api/ejchart#members:series-trendlines-tooltip-opacity).

{% highlight javascript %}

    $("#container").ejChart({        
          series :[{ 
              trendlines:[{ 
                  tooltip :{
                      border:{ color : "green", width : 2 },
                      rx: 10,
                      ry: 10,
                      duration : "300ms",
                      enableAnimation : false,
                      fill : "green",
                      format : "#point.x# : #point.y#%",
                      opacity : 0.5
                  } 
              }]
          }]                  
    });

{% endhighlight %}
