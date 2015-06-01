---
layout: post
title: Behaviour-Settings
description: behaviour settings
platform: js
control: Slider
documentation: ug
---

# Behaviour Settings

## Height

By default, **Slider** renders with a height of 14px. You can change the **Slider** height using **height** property. Specify the value for this property in string format.

## Width

By default, **Slider** widget renders with 100% width. You can customize the width of the Slider using **width** property. Specify the value for this property in string format.

The following steps explains you on how to configure the **height** and **width** of the **Slider**.

* In an HTML page, add a &lt;div&gt; element to render it as a Slider widget.



<table>
<tr>
<td>
[<b>HTML</b>]&lt;div id="BasicSlider"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[<b>JavaScript</b>]    &lt;script&gt;        $("#BasicSlider").ejSlider({<b>            height: "20",</b><b>            width: "500"</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.

{% include image.html url="/js/Slider/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img1.png" Caption="Slider with customized height and width"%}

## IncrementStep

This property sets the incremental step value for the **Slider**. When the **Slider** handle slides through mouse or keyboard, it increments / decrements the value based on the step value. By default, when the slider handle is moved, single value increments / decrements. Using **incrementStep** property you can change the increment step value. Data type of this property is number.

The following steps explains you on how to configure the **incrementStep** property.

* In an **HTML** page, add a **&lt;div&gt;** element to render it as a **Slider** widget.



<table>
<tr>
<td>
[<b>HTML</b>]&lt;div id="ejSlider"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[<b>JavaScript</b>]// When initializing the Slider widget, configure the “incrementStep” property as follows.    &lt;script&gt;        $("#ejSlider").ejSlider({            height: "15",            width: "500",<b>            incrementStep:5</b>        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code example to render the following output.

{% include image.html url="/js/Slider/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img2.png" Caption="Slider with incrementStep property enabled"%}

In the above example, value for **incrementStep** property is specified as “5” therefore, when you move the **Slider** handle, value “5” increments/decrements from the current **Slider** value.

## ReadOnly

This feature prevents you from interacting with the **Slider**. That is you can only view the **Slider** value and cannot change it.

The following steps explain you on how to enable the **readOnly** property.

* In an **HTML** page, add a **&lt;div&gt;** element to render it as a **Slider** widget.



<table>
<tr>
<td>
[<b>HTML</b>]&lt;div id="ejSlider"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[<b>JavaScript</b>]// When initializing the Slider widget, enable the “readOnly” property as follows.<br>    &lt;script&gt;        $("#ejSlider").ejSlider({            height: "15",            width: "500",<b>            readOnly:true</b>        });    &lt;/script&gt;</td></tr>
</table>


After you execute the above code example, the **Slider** values cannot be changed in any ways.

