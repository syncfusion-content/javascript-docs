---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: PivotGauge
documentation: ug
---

# Responsive Layout

PivotGauge widget supports responsive rendering based on the target device (desktop & tablet) resolution. It supports resolution upto 1024x600. You can enable responsiveness in PivotGauge by setting [`isResponsive`](/js/api/ejpivotgauge#members:isresponsive) property to true.

{% highlight javascript %}

$("#PivotGauge1").ejPivotGauge({
    url: "../PivotGauge",
    isResponsive: true,
    //...
});

{% endhighlight %}

![](Responsive-Layout_images/responsive 1.png)

_Normal View_


![](Responsive-Layout_images/responsive 2.png)

_Responsive View_





