---
layout: post
title: Interaction-and-Animation
description: interaction and animation
platform: js
control: Circular Gauge
documentation: ug
---

# Interaction and Animation

**Interaction**

**Circular Gauge** control contains **Interaction** feature. You can use this interaction feature to change the pointer values manually. You can achieve this by clicking and dragging the pointer over the **Gauge** and you can see the value of pointer changes dynamically while dragging. To Enable/Disable the user interaction you can use the Boolean property called **readOnly**. The user interaction option is enabled when you set the value as false for the property **readOnly**.By default it holds the true value.That is by default it does not support interaction. 

{% highlight html %}



<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>Circular Gauge JS Default Functionalities</title>
    <script src="http://code.jquery.com/jquery-1.10.2.min.js "></script>

    <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"></script>

    <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"></script>

    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js">
    </script>

</head>

<body>
    <div id="CircularGauge1">
    </div>


    <script type="text/javascript">
        $(function () {

            // For Circular Gauge rendering
            $("#CircularGauge1").ejCircularGauge({
                // For User interaction
            readOnly: false,
})
        });
    </script>
</body>
</html>





{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/CircularGauge/Concepts-and-Features/Interaction-and-Animation_images/Interaction-and-Animation_img1.png" Caption="Circular Gauge with basic interaction property"%}

**Animations**

**Circular Gauge** contains an attractive concept called **Animation**. The animation option enables the pointer to rotate from the minimum value to the current value with animation effects. By using this animation you can change the pointer value dynamically.You can apply the animation on  pointer either by clockwise or counterclockwise based on the scale direction. You can enable / disable it using the property **enableAnimation.** Animation is enabled when you set **enableAnimation** as ‘true’. By default it holds the true value. You can control the speed of the pointer during animating by using the property **animationSpeed**. It is a numerical value that holds the time in milli seconds. That is when the value is given as 1000, it is considered as 1 second.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight js %}

$(function () {
        // For Circular Gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            // For enabling animation
        enableAnimation: true,
            // For setting animation speed
        animationSpeed:1000
        })
    });

{% endhighlight %}






Execute the above code to render the following output.

{% include image.html url="/js/CircularGauge/Concepts-and-Features/Interaction-and-Animation_images/Interaction-and-Animation_img2.png" Caption="Circular Gauge with basic Animation property"%}

