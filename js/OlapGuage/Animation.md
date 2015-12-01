---
layout: post
title: Animation
description: animation
platform: js
control: OlapGauge
documentation: ug
---

# Animation

The animation option makes the pointer to rotate from minimum value to actual value with animation effects.  Animation could be enabled/disabled by using the [`enableAnimation`](/js/api/ejcirculargauge#members:enableanimation) property.  Speed of the pointer could be controlled by using the [`animationSpeed`](/js/api/ejcirculargauge#members:animationspeed) property. Time is represented in milliseconds.

{% highlight js %}

$("#OlapGauge1").ejOlapGauge({
    url: "../OlapGauge",
    //...
    enableAnimation: true,
    animationSpeed: 1000,
    //...
});

{% endhighlight %}
