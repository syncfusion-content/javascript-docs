---
layout: post
title: MaskEdit-Properties
description: maskedit properties
platform: js
control: MaskEdit
documentation: ug
---

# MaskEdit Properties

## CustomCharacter

The **MaskEdit** allows you to use the custom character option. The specified character is allowed to enter in the Mask Edit Textbox by using the **customCharacter** property.

## HidePromptOnLeave

The **MaskEdit** provides the option to hide the prompt when you focus out from the control. The mask prompt is visible when you focus again to the control. The default value of **hidePromptOnLeave** is false.

## InputMode

The **MaskEdit** supports two type of inputs such as text and password that have been assigned by using the enum values **ej.InputMode.Text** and **ej.InputMode.Password**. The default value for **inputMode** is text in **MaskEdit**.

## MaskFormat

The **MaskEdit** provides the option to define the **maskFormat** to the value. The default value for **maskFormat** property is empty string.

The following steps explain the implementation of **MaskEdit Properties**.



* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-CCCC",            customCharacter: "r",            hidePromptOnLeave: true,        });    });&lt;/script&gt;</td></tr>
</table>


The output for **MaskEdit** with its properties is as follows.

{% include image.html url="/js/MaskEdit/Concepts-and-Features/MaskEdit-Properties_images/MaskEdit-Properties_img1.png" Caption="Figure 13: MaskEdit with MaskFormat"%}



{% include image.html url="/js/MaskEdit/Concepts-and-Features/MaskEdit-Properties_images/MaskEdit-Properties_img2.png" Caption="Figure 14: MaskEdit with HidePromtOnLeave"%}



{% include image.html url="/js/MaskEdit/Concepts-and-Features/MaskEdit-Properties_images/MaskEdit-Properties_img3.png" Caption="Figure 15: MaskEdit with prompt focus"%}



{% include image.html url="/js/MaskEdit/Concepts-and-Features/MaskEdit-Properties_images/MaskEdit-Properties_img4.png" Caption="Figure 16: MaskEdit with InputMode text"%}

{% include image.html url="/js/MaskEdit/Concepts-and-Features/MaskEdit-Properties_images/MaskEdit-Properties_img5.png" Caption="Figure 17: MaskEdit with CustomCharacter"%}

