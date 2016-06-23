---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: OlapGauge
documentation: ug
---

# Responsive Layout

OlapGauge widget supports responsive rendering based on the target device (desktop & tablet) resolution. It supports resolution upto 1024x600. You can enable responsiveness in OlapGauge by setting [`isResponsive`](/js/api/ejolapgauge#members:isresponsive) property to true.

{% highlight javascript %}

$("#OlapGauge1").ejOlapGauge({
    url: "../OlapGauge",
    isResponsive: true,
    //...
});

{% endhighlight %}

![](Responsive-Layout_images/responsive 1.png)

_Normal View_


![](Responsive-Layout_images/responsive 2.png)

_Responsive View_





