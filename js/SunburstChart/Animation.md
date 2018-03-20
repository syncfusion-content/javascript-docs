---
layout: post
title: Animation
description: Learn how to animate the SunburstChart .
platform: js
control: SunburstChart
documentation: ug
api: /api/js/ejsunburstchart
---

# Animation

Sunburst chart allows you to animate the chart segments. You can enable animation using [`enableAnimation`](../api/ejsunburstchart#members:enableanimation) property. 

{% highlight js %}

$("#chart"). ejSunburstChart ({
	enableAnimation: true
   });

{% endhighlight %}


## Animation Types 
Sunburst chart provide options to animate the chart segments in different ways using [`animationType`](../api/ejsunburstchart#members:animationtype) property.

FadeIn – It gradually changes opacity of the chart segment.
Rotation – During an animation, control rotate from 0 to 360 angle.

### Fade In

The Fade In animation is enabled as follows 

{% highlight js %}

$("#chart"). ejSunburstChart ({
	enableAnimation: true,
       animationType:"fadeIn"
   });

{% endhighlight %}

![](/js/SunburstChart/Animation_images/Animation_img2.gif)

### Rotation

The following example shows how to enable rotation animation in ejSunburstChart

{% highlight js %}

$("#chart"). ejSunburstChart ({
	enableAnimation: true,
       animationType:"rotation"
   });

{% endhighlight %}

![](/js/SunburstChart/Animation_images/Animation_img1.gif)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/sunburst/animation) here to view the online demo sample of  Animation in  the Sunburst Chart.
