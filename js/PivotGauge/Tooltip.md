---
layout: post
title: Tooltip | JavaScript | PivotGauge | Syncfusion
description: This document illustrates that how to enable tooltip and its customization in JavaScript PivotGauge control
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Tooltip

The tooltip can be enabled by using the [`enableTooltip`](/api/js/ejpivotgauge#members:enabletooltip) property. 

N> By default, this property is set to false.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        enableTooltip: true
    });

{% endhighlight %}

The tooltip appearance can be customized by overriding its CSS class.

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
    
![Tooltip in JavaScript pivot gauge control](Tooltip_images/Tooltip.png) 

