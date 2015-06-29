---
layout: post
title: Trendlines
description: Trendlines
platform: js
control: Chart
documentation: ug
---

# Trendlines

## Overview

**Trendlines** are straight or curved line that indicate the general pattern or direction of series and used to analyse and display the trends in chart graphically. It is built on the assumptions based on current and past trends. This analysis is also called as regression analysis.

**EjChart** can automatically generate Trendlines for Cartesian axes type series (line, column, scatter, area, candle, hilo etc...) except bar type series.

The following code snippet illustrates how to enable Trendlines feature in Chart.

{% highlight js %}

        $("#container").ejChart({
            series:[{
            trendines: [{
            visibility: “visible”, type: “linear”
            }],
            //....
            //.... 
            }]            
        });



{% endhighlight %}

## Customize the Trendlines styles

The line of Trendlines can be customized using properties such as fill, width, dahsArray and opacity. **fill** is used to add the color to the line stroke, **width** is used to specify line thickness, **dashArray** used to draw dotted lines and **opacity** is used to change the opacity value of the line. Default type of Trendline is “linear”.

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img1.png" Caption="Adding Trendline to the chart"%}

## Type of Trendlines

EjChart supports the following type of Trendlines.

* Linear
* Exponential
* Logarithmic
* Power 
* Polynomial

### Linear

**Linear Trendline** is a best-fit straight line that is used with sets of simple linear data. A **Linear Trendline** shows when something is increasing or decreasing at a steady rate.

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img2.png" Caption="Adding Linear Trendline to the chart"%}

### Exponential

**Exponential Trendline** is a curved line that is used when data values rise or fall at constantly increasing rates.

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img3.png" Caption="Adding Exponential Trendline to the chart"%}

### Logarithmic

**Logarithmic Trendline** is a best-fit curved line that is used when the rate of change in the data increases or decreases and then levels out.

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img4.png" Caption="Adding Logarithmic Trendline to the chart"%}

### Power

**Power Trendline** is a curved line that is used with sets of data comparing measurements that increase at a specific rate, for example the acceleration of race car at one second intervals.

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img5.png" Caption="Adding Power Trendline to the chart"%}

### Polynomial

**Polynomial Trendline** is a curved line that is used when data fluctuates.

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img6.png" Caption="Adding Polynomial Trendline to the chart"%}

## Forecasting

**Forecasting** is the prediction of future/past situations. **Trendlines** are also used to display trends for the future and the past. **Forecasting** can be classified into two types as follows.

  * Forward Forecasting
  * Backward Forecasting

These can be enabled by setting the value for the **Forward Forecasting** and **Backward Forecasting** properties. The value set for **Forward Forecasting** is used to determine the distance of moving towards the future and the value set for **Backward Forecasting** is used to determine the distance of moving backwards.

The following code snippet illustrates how to enable **Forward Forecasting** in Trendlines.

{% highlight js %}

        $("#container").ejChart({
            series:[{
            trendines: [{
            visibility: “visible”, type: “linear”, forwardForecast: 5
            }],
            //....
            //.... 
            }] 
             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img7.png" Caption="Adding ForwardForecast value to Chart Trendline"%}

The following code snippet illustrates how to enable **Backward Forecasting** in Trendlines.

{% highlight js %}

        $("#container").ejChart({
            series:[{
            trendines: [{
            visibility: “visible”, type: “linear”, backwardForecast: 5
            }],
            //....
            //.... 
            }] 
             
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img8.png" Caption="Adding BackwardForecast  value to Chart Trendline"%}

## Trendlines Legend

While setting trendlines visibility as **“visible”** or **“hidden”**, Trendlines legend appears with series legend collection in chart. We can do interaction with Trendlines legend as like series legends (show/hide series on legend click) and we can change the legend name using **“name”** property of Trendlines.

The below screenshot illustrates hide the Trendline series on legend mouse click.

{% include image.html url="/js/Chart/Trendlines_images/Trendlines_img9.png" Caption="Hide the Trendline series on legend mouse click"%}