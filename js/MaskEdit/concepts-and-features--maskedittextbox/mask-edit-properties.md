---
layout: post
title: mask-edit-properties
description: mask edit properties
platform: js
control: MaskEdit
documentation: ug
---

# Mask Edit Properties

## Custom Character

The **Mask Edit** allows you to use the custom character option. The specified character is allowed to enter in the Mask Edit Textbox by using the **cCcustomCharacter** property.

## Hide Prompt On Leave

The **Mask Edit TextBbox** provides the option to hide the prompt when you focus out from the control. The mask prompt is visible when you focus again to the control. The default value of **hHhidePromptOnLeave** is false.

## Input Mode

The **Mask Edit** supports two type of inputs such as text and password that have been assigned by using the enum values **ej.InputMode.Text** and **ej.InputMode.Password**. The default value for **iIinputMode** is text in **Mask Edit**.

## Mask Format

The **Mask Edit** provides the option to define the **mMmaskFormat** to the value. The default value for **mMmaskFormat** property is empty string.

The following steps explain the implementation of **Mask Edit Properties**.

In the **View** page use the corresponding Textbox helper****for rendering **MaskEdit** control. In the **HTML** page set the **&lt;input&gt;** element for rendering **Mask Edit Textbox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>maskEdit</b> property in the <b>ejMaskEdit</b> function    &lt;script type="text/javascript"&gt;        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            <b>            customCharacter: "r",           </b><b>            hidePromptOnLeave: true,</b><b>            inputMode: ej.InputMode.Text,</b><b>            maskFormat: "99-999-CCCC"</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@{Html.EJ().MaskEdit("mask")

.**MaskFormat**("99-999-CCCC").**CustomCharacter**("r").

**HidePromptOnLeave**(true).**InputMode**(InputMode.Text).Render();}





* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-CCCC",            customCharacter: "r",            hidePromptOnLeave: true,        });    });&lt;/script&gt;</td></tr>
</table>


**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-CCCC" CustomCharacter="r" HidePromptOnLeave="true" InputMode="Text"  runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for **Mask Edit TextBbox** with its properties is as follows.

{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img1.png" Caption="Figure 2139: MaskEdit with MmaskFormat"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img2.png" Caption="Figure 2139: MaskEdit with MmaskFormat"%}



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img3.png" Caption="Figure 3014: MaskEdit with HhidePromtOnLeave"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img4.png" Caption="Figure 3014: MaskEdit with HhidePromtOnLeave"%}



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img5.png" Caption="Figure 3115: MaskEdit with prompt focus"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img6.png" Caption="Figure 3115: MaskEdit with prompt focus"%}



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img7.png" Caption="Figure 3216: MaskEdit with IinputMode text"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img8.png" Caption="Figure 3216: MaskEdit with IinputMode text"%}



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img9.png" Caption="Figure 3317: MaskEdit with CcustomCharacter"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\mask-edit-properties_images\mask-edit-properties_img10.png" Caption="Figure 3317: MaskEdit with CcustomCharacter"%}

