---
layout: post
title: Appearance
description: appearance
platform: js
control: MaskEdit
documentation: ug
---

# Appearance

## Theme

The **MaskEdit** control’s style and appearance can be controlled based on CSS classes. In order to apply styles to the **Textbox** control, you need to refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **MaskEdit** control namely:

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

## CSS Class

The **CSS** can be customized by using the **cssClass** in the **MaskEdit**. You can customize the **MaskEdit** with **cssClass** property to appear like your desired control.

The following steps explain the implementation of MaskEdit with **cssClass** property.

In the HTML page, add a &lt;div&gt; element to render the MaskEdit widget.  



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;<b> </b></td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>cssClass: "customCss"</b>        });    });&lt;/script&gt;</td></tr>
</table>


* Customize the CSS properties in custom CSS class.



{% highlight css %}

**[CSS]**

    <style>
        .customCss .e-box {
            border-color: #9d241b;
        }
        .customCss .e-input {
            background-color: #f6db8d;            
        }
        .customCss .e-select {
            background-color: #ecf6ac;
            border-color: #3c36e7;
        }
    </style>



{% endhighlight %}



The output for MaskEdit after applying **cssClass** is as follows.



{% include image.html url="/js/MaskEdit/Concepts-and-Features/Appearance_images/Appearance_img1.png" Caption="Figure 18: MaskEdit with cssClass"%}

## Rounded Corner Support

MaskEdit provides you with rounded corner support whose appearance is different from normal textbox controls.

The following steps explain the implementation of MaskEdit with **showRoundedCorner** property.

In the HTML page, add a &lt;div&gt; element to render the MaskEdit widget. 



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>showRoundedCorner: true,</b>            value: "123456"        });    });&lt;/script&gt;</td></tr>
</table>


Output of MaskEdit when **showRoundedCorner** is “**true**”.



{% include image.html url="/js/MaskEdit/Concepts-and-Features/Appearance_images/Appearance_img2.png" Caption="Figure 19: MaskEdit with showRoundedCorner"%}

## WatermarkText Support

The **MaskEdit** control provide water mark text support. You can display the initial value in the control by water mark.

The following steps explain the implementation of MaskEdit with **watermarkText** property.

In the HTML page, add a &lt;div&gt; element to render the MaskEdit widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>watermarkText: "Enter the Mask"</b>        });    });&lt;/script&gt;</td></tr>
</table>




Output of MaskEdit when **showRoundedCorner** is “**true**”.



{% include image.html url="/js/MaskEdit/Concepts-and-Features/Appearance_images/Appearance_img3.png" Caption="Figure 20: MaskEdit with watermark text"%}

## Text Alignment Support

The **MaskEdit** provides text alignment support that allows you to set the alignment of text in the control by using the **textAlign** property.

The following steps explain the implementation of MaskEdit with **textAlign** property.

* In the HTML page, add a &lt;div&gt; element to render the MaskEdit widget



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>textAlign: ej.TextAlign.Right</b>        });    });&lt;/script&gt;</td></tr>
</table>




The output for Textboxes when t**extAlign** is set to **“right”**.

{% include image.html url="/js/MaskEdit/Concepts-and-Features/Appearance_images/Appearance_img4.png" Caption="Figure 21: MaskEdit with textAlign"%}



