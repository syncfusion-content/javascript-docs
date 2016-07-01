---
layout: post
title: Dimensions
description: dimensions
platform: js
control: PivotChart
documentation: ug
---

#Dimensions

##Set size in percentage

You can customize the PivotChart dimension by setting the width and height of the widget in percentage.

{% highlight javascript %}

$(function () {
    $("#PivotChart1").ejPivotChart(
       ....
       //Setting size to Chart container
       size: {
         height: "80%",
         width: "80%"
       }
    });
});

{% endhighlight %}

##Set size in pixels

You can customize the PivotChart dimension by setting the width and height of the widget in pixels.

{% highlight javascript %}

$(function()
{
    $("#PivotChart1").ejPivotChart(
    {
        ....
        //Setting size to Chart container
        size:
        {
            height: "460px",
            width: "950px"
        }
    });
});

{% endhighlight %}

![](Dimensions_images/Dimensions.png) 

##Responsive

PivotChart widget supports responsive rendering based on the target device (desktop & tablet) resolution. It supports resolution upto 1024x600. You can enable responsiveness in PivotChart by setting [`isResponsive`](/js/api/ejpivotchart#members:isresponsive) property to true.

{% highlight javascript %}

$(function () {
    $("#PivotChart1").ejPivotChart(
       .... 
       //Enable responsiveness to change the Chart size dynamically.
       isResponsive: true,
       size: {
         height: "460px",
         width: "950px"
       }
    });
});

{% endhighlight %}

![](Dimensions_images/NormalView.png)

_Normal View_

![](Dimensions_images/ResponsiveView.png)

_ResponsiveView_