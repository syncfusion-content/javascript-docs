---
layout: post
title: orientation
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



<table>
<tr>
<td>
[<b>HTML</b>]&lt;div id="ejSlider"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[<b>JavaScript</b>]// When initializing the Slider widget, configure the orientation property as follows.    &lt;script&gt;        $("#ejSlider").ejSlider({            height: "150",            width: "20",<b>            orientation:ej.Orientation.Vertical</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.

![](orientation_images\orientation_img1.png)

_Slider in vertical orientation_

