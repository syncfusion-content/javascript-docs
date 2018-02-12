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

<<<<<<< HEAD
The animation option makes the pointer to rotate from minimum value to actual value with animation effects. The animation can be enabled/disabled by using the [`enableAnimation`](/api/js/ejcirculargauge#members:enableanimation) property. The speed of the pointer can be controlled by using the [`animationSpeed`](/api/js/ejcirculargauge#members:animationspeed) property. Time is represented in milliseconds.
=======
The animation option makes the pointer to rotate from minimum value to actual value with animation effects. Animation can be enabled/disabled by using the [`enableAnimation`](/api/js/ejcirculargauge#members:enableanimation) property.  The speed of the pointer can be controlled by using the [`animationSpeed`](/api/js/ejcirculargauge#members:animationspeed) property. Time is represented in milliseconds.
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //...
        enableAnimation: true,
        animationSpeed: 1000
    });

{% endhighlight %}