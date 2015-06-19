---
layout: post
title: Updating-slider-value
description: updating slider value
platform: js
control: Slider
documentation: ug
---

# Updating slider value

**Slider** widget includes an option to specify/update its value. And also you can specify the starting and ending value for the **Slider** using the **minValue** and **maxValue** properties.

## Value

This property is used to set the value in the “Default” and “Min-Range” Sliders. By default its value is null when no value is specified. Data type of this property is “number”.

## Values

This property is used to set the value in “Range Slider”. By default range values is from 0 to 100. This property is of “Array” data type.

The following steps explains you the configuration of “value” and “values” property.

* In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Range Slider” and “Default Slider”.



<table>
<tr>
<td>
<b>[HTML]</b>        <div class="txt">Default Slider</div>        &lt;div id="defaultSlider"&gt;&lt;/div&gt;        &lt;br /&gt;        &lt;br /&gt;        <div class="txt">Range Slider</div>        &lt;div id="rangeSlider"&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// When initializing Slider widget, configure the “value” and “values” property as follows.    &lt;script&gt;        $("#defaultSlider").ejSlider({            sliderType: ej.SliderType.Default,<b>            value: 50,</b>            width: "500"        });        $("#rangeSlider").ejSlider({            sliderType: ej.SliderType.Range,<b>            values: [20,80],</b>            width: "500"        });    &lt;/script&gt; </td></tr>
</table>


Execute the above code example to render the following output.


{% include image.html url="/js/Slider/Concepts-and-Features/Updating-slider-value_images/Updating-slider-value_img1.png" Caption="Exhibits “value” and “values” property in Default and Range Sliders."%}

## MinValue

To set the minimum/starting value of the Slider, you can use the minValue property. By default its value is 0. Data type of this property is “number”.

## MaxValue

To set the maximum/ending value of the Slider, you can use the maxValue property. By default its value is 100. Data type of this property is “number”.

The following steps explains you on how to configure minValue and maxValue property.

* In an **HTML** page, specify the **&lt;div&gt;** elements to render the **Default Slider** and **Range Slider**.



<table>
<tr>
<td>
[<b>HTML</b>]        <div class="txt">Default Slider</div>        &lt;div id="defaultSlider"&gt;&lt;/div&gt;        &lt;br /&gt;        &lt;br /&gt;        <div class="txt">Range Slider</div>        &lt;div id="rangeSlider"&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// When initializing Slider widget, configure the minValue and maxValue properties as follows.    &lt;script&gt;        $("#defaultSlider").ejSlider({            sliderType: ej.SliderType.Default,            value: 60,            width: "500",<b>            minValue: 40,</b><b>            maxValue:80</b>        });        $("#rangeSlider").ejSlider({            sliderType: ej.SliderType.Range,            values: [10,90],            width: "500",<b>            minValue: 10,</b><b>            maxValue:90</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.

{% include image.html url="/js/Slider/Concepts-and-Features/Updating-slider-value_images/Updating-slider-value_img2.png" Caption="Exhibits “minValue” and “maxValue” properties in Default and Range Sliders."%}

In the above example, for **Default Slider** the slider value starts from “40” (min value) and ends in “80” (max value), so the slider handle is placed at the center of the Slider while specifying the value as “60”.

For **Range Slider**, the value starts from “10” (min value) and ends in “90” (max value). The range shadow occupies the entire **Slider**, since the range (values) is specified as “[10, 90]”.

