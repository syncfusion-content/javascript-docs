---
layout: post
title: AngleSupport
description: AngleSupport
platform: js
control: Radial Slider
documentation: ug
---

# Change display angle

## Start Angle

The **RadialSlider** property **startAngle** Indicates the starting point of the Radialslider and its  allow you to change the startangle level view of the  **RadialSlider**. By default, the **Radial Slider** startAngle is set as 0. Refer to the following code example.


{% highlight html %}

        <div id="radialSlider">
        </div>

{% endhighlight %}
    
{% highlight js %}

     $("#radialSlider").ejRadialSlider({ innerCircleImageUrl:"chevron-right.png",startAngle: 20 });

{% endhighlight %}


The following screenshot illustrates the output of the above code.

![](Angle-Support_images\Angle-Support_images_img1.png)


## End Angle

The **RadialSlider** property **endAngle** Indicates the end point of the Radialslider and its  allow you  to change the   endangle level view of the  **RadialSlider**. By default, the **Radial Slider** startAngle is set as 0. Refer to the following code example.

{% highlight html %}

        <div id="radialSlider"></div>

{% endhighlight %}

{% highlight js %}

        $("#radialSlider").ejRadialSlider({ innerCircleImageUrl:"chevron-right.png" ,endAngle: 300 });

{% endhighlight %}


The following screenshot illustrates the output of the above code.

![](Angle-Support_images\Angle-Support_images_img2.png)




