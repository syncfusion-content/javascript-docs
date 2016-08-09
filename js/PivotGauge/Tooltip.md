---
layout: post
title: Tooltip
description: tooltip
platform: js
control: PivotGauge
documentation: ug
---

# Tooltip

Tooltip can be enabled by using the [`enableTooltip`](/js/api/ejpivotgauge#members:enabletooltip) property. 

N> By default, this property is set to "false".

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        enableTooltip: true
    });

{% endhighlight %}

Tooltip appearance can be customized by overriding its CSS class.

{% highlight css %}

    .e-pivotgauge-tooltip {
        background-color: aqua!important;
        border: 2 px solid red!important;
        color: black!important;
        border-radius: 18 px!important;
        margin-top: 20 px;
        text-align: left;
        font: 12 px Segoe UI;
        line-height: 20 px;
    }

{% endhighlight %}
    
![](Tooltip_images/Tooltip.png) 

