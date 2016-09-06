---
layout: post
title: Animation
description: Animation
platform: js
control: Radial slider
documentation: ug
---

## Animation Effect

The animation effect for the **RadialSlider** can be enabled or disabled using the **enableAnimation** property.By default, it is set as **true**, so that the handle movement will be animated.

{% highlight html %}

    <div id="radialSlider"></div>
    
{% endhighlight %}

Add the following script in your code and this will stop the handle movement's animation.
    
{% highlight js %}

     $("#radialSlider").ejRadialSlider({ innerCircleImageUrl:"chevron-right.png",enableAnimation:false });

{% endhighlight %}




