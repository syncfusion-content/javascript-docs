---
layout: post
title: Orientation
description: orientation
platform: js
control: Slider
documentation: ug
---

# Orientation

This property is used to set the **Slider** in either horizontal or vertical direction. By default, **Slider** renders in horizontal direction. Data type of this property is “enum”.

Possible **Slider** orientations are as follows,

_Property Table for JavaScript_

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Allowed values</b></td><td>
<b>Description</b></td></tr>
<tr>
<td rowspan = "2">
orientation</td><td>
ej.Orientation.Vertical</td><td>
Displays the <b>Slider</b> in vertical direction</td></tr>
<tr>
<td>
ej.Orientation.Horizontal (default value)</td><td>
Displays the <b>Slider</b> in horizontal direction</td></tr>
</table>


The following steps explains you on how to configure the **orientation** property.

* In an **HTML** page, add a **&lt;div&gt;** element to render it as a **Slider** widget.



{% highlight html %}

**[HTML]**

    <div id="ejSlider"></div>

{% endhighlight %}

{% highlight js %}

**[JavaScript]**

// When initializing the Slider widget, configure the orientation property as follows.
    <script>
        $("#ejSlider").ejSlider({
            height: "150",
            width: "20",
            orientation:ej.Orientation.Vertical
        });
    </script>

{% endhighlight %}

Execute the above code example to render the following output.

{% include image.html url="/js/Slider/Concepts-and-Features/Orientation_images/Orientation_img1.png" Caption=""%}

_Slider in vertical orientation_

