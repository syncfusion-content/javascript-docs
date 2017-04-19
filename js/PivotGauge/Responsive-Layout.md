---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Responsive Layout

PivotGauge widget supports responsive rendering based on the target device (desktop & tablet) resolution. It supports resolution upto 1024x600. You can enable responsiveness in PivotGauge by setting [`isResponsive`](/api/js/ejpivotgauge#members:isresponsive) property to true.

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





