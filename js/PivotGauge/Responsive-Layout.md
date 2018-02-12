---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Responsive layout

The pivot gauge widget supports responsive rendering based on the target device (desktop and tablet) resolution. It supports resolution upto 1024x600. You can enable the responsiveness in the pivot gauge by setting the [`isResponsive`](/api/js/ejpivotgauge#members:isresponsive) property to true.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        isResponsive: true
    });

{% endhighlight %}

![](Responsive-Layout_images/Responsive1.png)

_Normal View_


![](Responsive-Layout_images/Responsive2.png)

_Responsive View_





