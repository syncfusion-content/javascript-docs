---
layout: post
title: Animation
description: animation
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Animation

The animation option makes the pointer to rotate from minimum value to actual value with animation effects. The animation can be enabled/disabled by using the [`enableAnimation`](/api/js/ejpivotgauge#members:enableanimation) property. The speed of the pointer can be controlled by using the [`animationSpeed`](/api/js/ejcirculargauge#members:animationspeed) property. Time is represented in milliseconds.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        enableAnimation: true,
        animationSpeed: 1000
    });

{% endhighlight %}