---
layout: post
title: interaction-and-animation
description: interaction and animation
platform: js
control: Circular Gauge
documentation: ug
---

# Interaction and Animation

**Interaction**

* **Circular Gauge** control contains **Interaction** feature. You can use this interaction feature to change the pointer values manually. You can achieve this by clicking and dragging the pointer over the **Gauge** and you can see it dynamically changes the value of pointer changes dynamically while dragging.

*  To Enable/Disable the user interaction you can use the Boolean property called **readOnly**. The user interaction option is enabled when you set the value as false for the property **readOnly**.. By default it holds the true value.That is by default it does not support interaction. That is by default it does not support interaction.


{% highlight js %}

**[JavaScript]**

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Circular Gauge JS Default Functionalities</title>
<script src="@Url.Content("http://code.jquery.com/jquery-1.10.2.min.js ")"></script>


<script src="@Url.Content("http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js")"></script>

<script src="@Url.Content("http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js")"></script>

<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js">
</script><script src="@Url.Content("http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js")"></script>

</head>

<body>
<div id="CircularGauge1">
</div>


<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
// For User interaction
**readOnly: false,**
})
});
</script>
</body>
</html>




{% endhighlight %}





**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

    // For User interaction

    .ReadOnly(false)

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ReadOnly="false" ID="CircularGauge1"&gt;

        &lt;/ej:CircularGauge&gt; 



Execute the above code to render the following output.



![](interaction-and-animation_images\interaction-and-animation_img1.png)

 _Figure_ _35__: Circular Gauge with basic interaction property_

**Animations**

* **Circular Gauge** contains an attractive concept called **Animation**. The animation option enables the pointer to rotate from the minimum value to the current value with animation effects. By using this animation you can change the pointer value dynamically.You can apply the The animation on the pointer is either by clockwise or counterclockwise based on the scale direction. 

* You can enable / disable it using the property **enableAnimation.** Animation is enabled when you set **enableAnimation** as ‘true’. By default it holds the true value. You can control the speed of the pointer during animating by using the property **animationSpeed**. It is a numerical value that holds the time in millei seconds. That is when the value is given setting valuea is 1000, it is considered as 1 second.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>

<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
// For enabling animation
**enableAnimation: true,**
// For setting animation speed
**animationSpeed:1000**
})
});
</script>



{% endhighlight %}



**[view]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

       // For enabling animation

       .EnableAnimation(true)

       // For setting animation speed

       .AnimationSpeed(1000)

)





**[ASP]**



  &lt;%--For Circular Gauge rendering--%&gt; 

  &lt;%--For enabling animation and setting animation speed--%&gt;

       &lt;ej:CircularGauge runat="server" ReadOnly="false" enableAnimation="true"  animationSpeed="1000" Id="CircularGauge1"&gt;

        &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\interaction-and-animation_images\interaction-and-animation_img2.png" Caption="Figure 36: Circular Gauge with basic Animation property"%}

