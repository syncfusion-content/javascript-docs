---
layout: post
title: EnableDisable-the-Slider
description: enable/disable the slider
platform: js
control: Slider
documentation: ug
---

# Enable/Disable the Slider

**Slider** widget includes an option to enable/disable it. When you disable the Slider, it is displayed in a blur state and you cannot perform any operations in it.

## Enabled	

Using this **enabled** property you can enable/disable the **Slider**. Data type of this property is “Boolean”.

The following steps explains you on how to disable the **Slider**.

* In an **HTML** page, specify the **&lt;div&gt;** elements to render the **Default Slider**.



<table>
<tr>
<td>
<b>[HTML]</b>        <div class="txt">Default Slider</div>        &lt;div id="defaultSlider"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// During initialization disable the Slider by setting value for enabled property as false.    &lt;script&gt;        $("#defaultSlider").ejSlider({            value: 60,            width: "500",<b>            enabled:false</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.


{% include image.html url="/js/Slider/Concepts-and-Features/EnableDisable-the-Slider_images/EnableDisable-the-Slider_img1.png" Caption="Slider in disabled state"%}

