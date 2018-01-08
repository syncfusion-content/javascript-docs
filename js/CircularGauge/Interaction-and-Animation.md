---
layout: post
title: Interaction-and-Animation
description: interaction and animation
platform: js
control: Circular Gauge
documentation: ug
api: /api/js/ejcirculargauge
---

# Interaction and Animation

**Interaction**

**Circular Gauge** control contains **Interaction** feature. You can use this interaction feature to change the pointer values manually. You can achieve this by clicking and dragging the pointer over the **Gauge** and you can see the value of pointer changes dynamically while dragging. To Enable/Disable the user interaction you can use the Boolean property called [`readOnly`](../api/ejcirculargauge#members:readonly). The user interaction option is enabled when you set the value as false for the property **readOnly**.By default it holds the true value.That is by default it does not support interaction. 

{% highlight html %}


  <div id="CircularGauge1">  </div>  


{% endhighlight %}

{% highlight javascript %}

$(function () {
        // For Circular Gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            // For User interaction
            readOnly: false,
        })
    });
   
{% endhighlight %}

Execute the above code to render the following output.

![](/js/CircularGauge/Interaction-and-Animation_images/Interaction-and-Animation_img1.png)

**Animations**

**Circular Gauge** contains an attractive concept called **Animation**. The animation option enables the pointer to rotate from the minimum value to the current value with animation effects. By using this animation you can change the pointer value dynamically.You can apply the animation on  pointer either by clockwise or counterclockwise based on the scale direction. You can enable / disable it using the property [`enableAnimation`](../api/ejcirculargauge#members:enableanimation). Animation is enabled when you set **enableAnimation** as ‘true’. By default it holds the true value. You can control the speed of the pointer during animating by using the property [`animationSpeed`](../api/ejcirculargauge#members:animationspeed). It is a numerical value that holds the time in milliseconds. That is when the value is given as 1000, it is considered as 1 second.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

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

![](/js/CircularGauge/Interaction-and-Animation_images/Interaction-and-Animation_img2.png)

**Gradient**

You can change the interior gradient of circular gauge by using [`interiorGradient`](../api/ejcirculargauge#members:interiorgradient) property. The [`isRadialGradient`](../api/ejcirculargauge#members:isradialgradient) property is used to check whether the gradient is circular or not.  

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

$(function () {
        $("#CircularGauge1").ejCircularGauge({          
        interiorGradient: { colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] },
        isRadialGradient : true,
        })
    });

{% endhighlight %}

**Distance From Corner**

You can display the circular gauge from distance apart from the corner by specifying value for [`distanceFromCorner`](../api/ejcirculargauge#members:distancefromcorner) property. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
        $("#CircularGauge1").ejCircularGauge({          
        distanceFromCorner :25
        })
    });

{% endhighlight %}

**Resize**

Circular gauge can be responsive while resizing by specifying [`enableResize`](../api/ejcirculargauge#members:enableresize) property as true. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

$(function () {
        $("#CircularGauge1").ejCircularGauge({          
            enableResize: true
        })
    });

{% endhighlight %}

Circular Gauge is made responsive when resizing the browser by using [`isResponsive`](../api/ejcirculargauge#members:isresponsive) property.

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
                    isResponsive: true,                                     
                });

{% endhighlight %}

**Localization**

The circular gauge can be localized based on name of culture specified in [`locale`](../api/ejcirculargauge#members:locale) property.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

$(function () {
        $("#CircularGauge1").ejCircularGauge({          
           locale : "en-US"
        })
    });

{% endhighlight %}

**Enable Group Separator** is used to Convert the date object to string while using the locale settings, you can set [`enableGroupSeparator`](../api/ejcirculargauge#members:enablegroupseparator) property as **true**.

{% highlight javascript %}

<div id="CircularGauge1"></div> 
 
<script>
        $("#CircularGauge1").ejCircularGauge({ 
            locale : "en-US" ,
            enableGroupSeparator: true
            }); 
</script>

{% endhighlight %}

**Themes**

**CircularGauge** theme is a set of pre-defined options that are applied to the control before **CircularGauge** is instantiated. Following predefined themes are available in JavaScript **CircularGauge**.

1. flatlight
2. flatdark
3. gradientlight 
4. gradientdark 
5. azure                      
6. azuredark               
7. lime 
8. limedark
9. saffron
10. saffrondark
11. gradientazure
12. gradientazuredark
13. gradientlime
14. gradientlimedark
15. gradientsaffron
16. gradientsaffrondark

The theme for circular gauge can be specified using [`theme`](../api/ejcirculargauge#members:theme) property.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
        $("#CircularGauge1").ejCircularGauge({          
            theme : "flatlight"
        })
    });

{% endhighlight %}

**Circular Gauge Values**

The [`minimum`](../api/ejcirculargauge#members:minimum), [`maximum`](../api/ejcirculargauge#members:maximum), [`radius`](../api/ejcirculargauge#members:radius) and [`value`](../api/ejcirculargauge#members:value) attributes of circular gauge are used to render the circular gauge with specified location. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
        $("#CircularGauge1").ejCircularGauge({            
            maximum: 120,
            minimum: 10,
            value: 30,
            radius: 100
        })
    });

{% endhighlight %}
