---
layout: post
title: AngleSupport
description: AngleSupport
platform: js
control: Radial Slider
documentation: ug
api: /api/js/ejradialslider
---

# Display Angle Support

## Start Angle

The **RadialSlider** property [startAngle](https://help.syncfusion.com/api/js/ejradialslider#members:startangle) allows you to change the startAngle level of the  **RadialSlider**. By default, the **Radial Slider** startAngle is set as 0. Refer to the following code example.


{% highlight html %}

        <div id="radialSlider">
        </div>

{% endhighlight %}
    
{% highlight js %}

     $("#radialSlider").ejRadialSlider({ innerCircleImageUrl:"chevron-right.png",startAngle: 20 });

{% endhighlight %}


The following screenshot illustrates the output of the above code.

![](display-angle-settings_images\display-angle-settings_images_img1.png)


## End Angle

The **RadialSlider** property [endAngle](https://help.syncfusion.com/api/js/ejradialslider#members:endangle) allows you  to change the endAngle level of the  **RadialSlider**. By default, the **Radial Slider** endAngle is set as 360. Refer to the following code example.

{% highlight html %}

        <div id="radialSlider"></div>

{% endhighlight %}

{% highlight js %}

        $("#radialSlider").ejRadialSlider({ innerCircleImageUrl:"chevron-right.png" ,endAngle: 300 });

{% endhighlight %}


The following screenshot illustrates the output of the above code.

![](display-angle-settings_images\display-angle-settings_images_img2.png)