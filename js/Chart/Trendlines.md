---
layout: post
title: Trendlines
description: Trendlines
platform: js
control: Chart
documentation: ug
---

# Trendlines

EjChart can generate Trendlines for Cartesian type series *(line, column, scatter, area, candle, hilo etc.)* except bar type series. You can add more than one trendline object to the **trendlines** option.

{% highlight js %}

        $("#chartcontainer").ejChart({
            series:[{
                  trendlines: [{
                       //Enable Trendline to chart series
                       visibility: “visible”, type: “linear”
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![]("/js/Chart/Trendlines_images/Trendlines_img1.png" Caption="Adding Trendline to the chart")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/trendlines) here to view the Trendlines online demo sample.


## Customizing the trendline styles

A trendline can be customized using properties such as **fill**, **width**, **dahsArray** and **opacity**. Default type of trendline is **"linear"**.

{% highlight js %}

        $("#chartcontainer").ejChart({
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

![]("/js/Chart/Trendlines_images/Trendlines_img2.png" Caption="Customizing the trendlines")


## Types of Trendline

EjChart supports the following type of Trendlines.

* Linear
* Exponential
* Logarithmic
* Power 
* Polynomial

### Linear

To render Linear Trendline, you have to set *type* as **"linear"**. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: “linear”
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![]("/js/Chart/Trendlines_images/Trendlines_img3.png" Caption="Adding Linear Trendline to the chart")

### Exponential

Exponential Trendline can be rendered by setting the *type* as **"exponential"**. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: “exponential”
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![]("/js/Chart/Trendlines_images/Trendlines_img4.png" Caption="Adding Exponential Trendline to the chart")

### Logarithmic

Logarithmic Trendline can be rendered by setting the *type* as **"Logarithmic"**.  

{% highlight js %}

        $("#chartcontainer").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: “logarithmic”
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![]("/js/Chart/Trendlines_images/Trendlines_img5.png" Caption="Adding Logarithmic Trendline to the chart")

### Power

Power Trendline can be rendered by setting the *type* of trendline as **"power"**. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: “power”
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![]("/js/Chart/Trendlines_images/Trendlines_img6.png" Caption="Adding Power Trendline to the chart")

### Polynomial

Polynomial Trendline can be rendered by setting trendline *type* as **"polynomial"**.  You can change the polynomial order by using **polynomialOrder** of trendlines. It ranges from 2 to 6.

{% highlight js %}

        $("#chartcontainer").ejChart({
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: “polynomial”
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![]("/js/Chart/Trendlines_images/Trendlines_img7.png" Caption="Adding Polynomial Trendline to the chart")

## Forecasting

**Trendline forecasting** is the prediction of future/past situations.  **Forecasting** can be classified into two types as follows.

  * Forward Forecasting
  * Backward Forecasting

### Forward Forecasting

The value set for **forwardForecast** is used to determine the distance moving towards the future trend.

{% highlight js %}

        $("#chartcontainer").ejChart({
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

![]("/js/Chart/Trendlines_images/Trendlines_img8.png" Caption="Adding ForwardForecast value to Chart Trendline")


### Backward Forecasting

The value set for **backwardForecast** is used to determine the past trends.

{% highlight js %}

        $("#chartcontainer").ejChart({
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

![]("/js/Chart/Trendlines_images/Trendlines_img9.png" Caption="Adding BackwardForecast  value to Chart Trendline")

## Trendlines Legend

To display legend item for trendline, use **name** property. You can interact with trendline legends similar to the series legends *(show/hide trendlines on legend click)*.  

{% highlight js %}

        $("#chartcontainer").ejChart({
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

![]("/js/Chart/Trendlines_images/Trendlines_img10.png" Caption="Hide the Trendline series on legend mouse click")