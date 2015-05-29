---
layout: post
title: scale-settings
description: scale settings
platform: js
control: Slider
documentation: ug
---

# Scale Settings

**Slider** widget includes option to display the scale on the **Slider**. Scale in **Slider** supports you to easily identify the current value/values of the **Slider**. Scale contains “small ticks” and “large ticks”. Values of the **Slider** is displayed above each large ticks.

## Show Scale

This property enables the scale in the **Slider**. By default, its value is “false”. Data type of this property is “Boolean”.

The following steps explains you the configuration of **showScale** property.

* In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider” and “Range Slider”.



<table>
<tr>
<td>
<b>[HTML]</b>        <div class="txt">Default Slider</div>        &lt;div id="defaultSlider"&gt;&lt;/div&gt;        &lt;br /&gt;        &lt;br /&gt;        <div class="txt">Range Slider</div>        &lt;div id="rangeSlider"&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// In JavaScript, configure the showScale property as follows.    &lt;script&gt;        $("#defaultSlider").ejSlider({            sliderType: ej.SliderType.Default,            value: 60,            width: "500",            minValue: 40,            maxValue: 80,<b>            showScale: true</b>        });        $("#rangeSlider").ejSlider({            sliderType: ej.SliderType.Range,            values: [10,90],            width: "500",            <b>showScale: true</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.

{% include image.html url="\js\Slider\concepts-and-features\scale-settings_images\scale-settings_img1.png" Caption="Exhibits Scale in Default and Range Sliders."%}

## Enable Small Ticks

**Slider** widget provides you an option to enable/disable the small ticks present in the scale. By default, when you enable “showScale” property, small ticks is displayed in the scale. Use the **showSmallTicks** property to disable the small ticks present in the scale. Data type of this property is “Boolean”.

The following steps explains you on how to disable the small ticks in **Slider**.

* In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider” and “Range Slider”.



<table>
<tr>
<td>
[<b>HTML</b>]        <div class="txt">Default Slider</div>        &lt;div id="defaultSlider"&gt;&lt;/div&gt;        &lt;br /&gt;        &lt;br /&gt;        <div class="txt">Range Slider</div>        &lt;div id="rangeSlider"&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
[<b>JavaScript</b>]// In JavaScript, set the value of showSmallTicks property as “false”.<br>    &lt;script&gt;        $("#defaultSlider").ejSlider({            sliderType: ej.SliderType.Default,            value: 60,            width: "500",            minValue: 40,            maxValue: 80,            showScale: true,<b>            showSmallTicks: false</b>        });        $("#rangeSlider").ejSlider({            sliderType: ej.SliderType.Range,            values: [10,90],            width: "500",            showScale: true,<b>            showSmallTicks:false</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.


{% include image.html url="\js\Slider\concepts-and-features\scale-settings_images\scale-settings_img2.png" Caption="Shows Scale with small ticks disabled"%}

## Small step

This property specifies the distance between the two small ticks present in the scale and the position of the small ticks in the Slider scale. Data type of this property is “number”.

## Large step

This property specifies the distance between the two small ticks present in the scale and the position of the large ticks in the Slider scale. Data type of this property is “number”.

The following steps explains you on how to configure the smallStep and largeStep property in Slider scale.

* In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider” and “Range Slider”



<table>
<tr>
<td>
<b>[HTML]</b>        <div class="txt">Default Slider</div>        &lt;div id="defaultSlider"&gt;&lt;/div&gt;        &lt;br /&gt;        &lt;br /&gt;        <div class="txt">Range Slider</div>        &lt;div id="rangeSlider"&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// In JavaScript, specify the value for smallStep and largeStep properties.    &lt;script&gt;        $("#defaultSlider").ejSlider({            sliderType: ej.SliderType.Default,            value: 60,            width: "500",            minValue: 40,            maxValue: 80,            showScale: true,<b>            smallStep: 5,</b><b>            largeStep: 20</b>        });        $("#rangeSlider").ejSlider({            sliderType: ej.SliderType.Range,            values: [25,75],            width: "500",            showScale: true,<b>            smallStep: 5,</b><b>            largeStep:25</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.


{% include image.html url="\js\Slider\concepts-and-features\scale-settings_images\scale-settings_img3.png" Caption="Shows “smallStep” and “largeStep” properties enabled in Slider scale"%}

In the above example, for “Default Slider” the “**smallStep**” value is specified as “5”, so for each 5 values from the starting value, small ticks is enabled. Also, “**largeStep**” value is specified as “20”, so for each 20 values from the starting value, large ticks is enabled.

Similarly for “Range Slider”, “**smallStep**” value is specifies as “5”, so for each 5 values from the starting value, small ticks is enabled. Also, “**largeStep**” value is specified as “25” so, for each 25 values large ticks is enabled.

