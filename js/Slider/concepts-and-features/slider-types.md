---
layout: post
title: slider-types
description: slider types
platform: js
control: Slider
documentation: ug
---

# Slider Types

This feature allows you to specify the type of **Slider**. There are three different types of **Slider**, **Default Slider**, **Min-Range Slider** and **Range Slider**. By default, **Default Slider** renders. You can use the **sliderType** property to choose the type of **Slider**. Data type of this property is “Enum”

Both **Default Slider** and **Min-Range Slider** have same behaviour that is used to select a single value. In **Min-Range Slider**, a shadow is considered from the start value to current handle position. But **Range Slider** contains two handles that is used to select a range of values and a shadow is considered in between the two handles.

Possible Slider types are as follows,

_Property Table for JavaScript_

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Allowed values</b></td><td>
<b>Description</b></td></tr>
<tr>
<td rowspan = "3">
sliderType</td><td>
ej.SliderType.Default (default value)</td><td>
It is the default Slider type. It helps to select a single value. </td></tr>
<tr>
<td>
ej.SliderType.MinRange</td><td>
Use this Slider to select a single value; Displays shadow from the start value to the current value.</td></tr>
<tr>
<td>
ej.SliderType.Range</td><td>
Use this Slider to select a range of values; Displays shadow in-between the selection range.</td></tr>
</table>


The following steps explains you on how to configure the **sliderType** property to display **Range Slider** and **MinRange Slider**.

* In an **HTML** page, specify the **&lt;div&gt;** elements to render the **RangeSlider** and **MinRange****Slider**.



<table>
<tr>
<td>
[<b>HTML</b>]        <div class="txt">Range</div>        &lt;div id="rangeSlider"&gt;&lt;/div&gt;        &lt;br /&gt;        &lt;br /&gt;        <div class="txt">Min-Range</div>        &lt;div id="minSlider"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[<b>JavaScript</b>]// When initializing the Slider components, configure the sliderType property as follows.    &lt;script&gt;        $("#minSlider").ejSlider({<b>            sliderType: ej.SliderType.MinRange,</b>            value: 60,            width:"500"        });        $("#rangeSlider").ejSlider({<b>            sliderType: ej.SliderType.Range,</b>            values: [30, 60],            width:"500"        });    &lt;/script&gt;</td></tr>
</table>




Execute the above code example to render the following output.



![](slider-types_images\slider-types_img1.png)

_Shows different Slider types (Range and Min-Range sliders)_

