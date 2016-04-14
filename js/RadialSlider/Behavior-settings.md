---
layout: post
title: Behavior-settings
description: behavior settings
platform: js
control: RadialSlider
documentation: ug
---

# Behavior settings

The following are some  properties that enables you to change the behavior of **Radial Slider** control.

##  Show/hide RadialSlider on initial rendering 

The **RadialSlider** property **autoOpen** this allow to enable or disable autoOpen  to the **RadialSlider**. Set the value to this property as **Boolean** type.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

    $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "chevron-right.png",autoOpen:false });
    
{% endhighlight %}

## EnableRoundOff 

The **RadialSlider** property **enableRoundOff** allow  to show  the rounded off value to the **RadialSlider**. Set the value to this property as **Boolean** type.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

        $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "chevron-right.png",enableRoundOff:false });

{% endhighlight %}

## Display inline

The **RadialSlider** property **inline** is used to show  the inline behavior to the **RadialSlider**. Set the value to this property as **Boolean** type.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

        $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "chevron-right.png",inline:true });

{% endhighlight %}

## Modifying Label Space 

The **RadialSlider** property **labelSpace** allow to  give the  space of label to the **RadialSlider**.  By default, the **Radial Menu** labelSpace is set as 30. Refer to the following code example.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

        $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "chevron-right.png",labelSpace:40 });

{% endhighlight %}

The following screenshot shows the output for the above code example.

![](Behavior-settings_images\Behavior-settings_images_img1.png)


## Setting radius

The **RadialSlider** property **radius**  indicates the radius of the Radialslider's circle ant its allow to change radius value of the  **RadialSlider**.  By default, the **Radial Slider** radius is set as 200. Refer to the following code example.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

        $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "chevron-right.png",radius:250 });

{% endhighlight %}

## Show/Hide inner circle

The **RadialSlider** property **showInnerCircle** allow to show  or hide  the inner circle of  the **RadialSlider**. Set the value to this property as **Boolean** type.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

        $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "chevron-right.png",showInnerCircle:false });

{% endhighlight %}

The following screenshot shows the output for the above code example.

![](Behavior-settings_images\Behavior-settings_images_img2.png)

## Ticks customization

The **RadialSlider** property **ticks** allow to show  the array of numeric value to  the **RadialSlider**. By Default "RadialSlider " ticks value is a set to an array of length 11 as following,

ticks= { 0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100 }. You can refer the below code for reference.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

        $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "chevron-right.png",ticks:[100,200,300,400,500,600,700,800,900,1000],value:100 });

{% endhighlight %}

The following screenshot shows the output for the above code example.

![](Behavior-settings_images\Behavior-settings_images_img3.png)
