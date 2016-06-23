---
layout: post
title: Dimensions
description: dimensions
platform: js
control: OlapChart
documentation: ug
---

#Dimensions

##Set size in percentage

You can customize the OlapChart dimension by setting the width and height of the widget in percentage.

{% highlight javascript %}

$(function () {
   $("#OlapChart1").ejOlapChart({
       url: "../wcf/OlapChartService.svc", 
       //Setting size to Chart container
       size: {
         height: "80%",
         width: "80%"
       }
    });
});

{% endhighlight %}

##Set size in pixels

You can customize the OlapChart dimension by setting the width and height of the widget in pixels.

{% highlight javascript %}

$(function()
{
    $("#OlapChart1").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
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

OlapChart widget supports responsive rendering based on the target device (desktop & tablet) resolution. It supports resolution upto 1024x600. You can enable responsiveness in OlapChart by setting [`isResponsive`](/js/api/ejolapchart#members:isresponsive) property to true.

{% highlight javascript %}

$(function () {
   $("#OlapChart1").ejOlapChart({
       url: "../wcf/OlapChartService.svc", 
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