---
layout: post
title: RTL-support
description: rtl support
platform: js
control: Slider
documentation: ug
---

# RTL support

**Slider** includes the Right to Left alignment support. Operations in the **Slider** is performed from Right to Left.

## Enabling RTL

Use the **enableRTL** property to enable the **RTL** support. By default this property is disabled. Data type of this property is “Boolean”.

The following steps explains you on how to enable **RTL** support in **Slider**.

* In an **HTML** page, specify the **&lt;div&gt;** elements to render the **Range Slider.**



<table>
<tr>
<td>
<b>[HTML]</b>        <div class="txt">Range Slider</div>        &lt;div id="rangeSlider"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// In JavaScript, when initializing the Slider, specify the value for “enableRTL” property as “true”    &lt;script&gt;        $("#rangeSlider").ejSlider({            sliderType: ej.SliderType.Range,            values: [25,75],            width: "500",<b>            enableRTL:true</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.


{% include image.html url="/js/Slider/Concepts-and-Features/RTL-support_images/RTL-support_img1.png" Caption="Slider with RTL support enabled"%}

