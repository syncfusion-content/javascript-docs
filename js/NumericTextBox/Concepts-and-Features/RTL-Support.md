---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: NumericTextbox
documentation: ug
---

# RTL Support

The **NumericTextBox** provides **RTL** (**Right-To-Left**) support. The alignment of NumericTextBox can be changed from **Left-To-Right** into **Right-To-Left**.

## Enable RTL

The following steps explain the implementation of **enableRTL** in **NumericTextBox** .

1. In the HTML page set the corresponding &lt;input&gt; elements for rendering NumericTextBox control.

2. 

<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enableRTL </b>property<b> </b>as<b> “True”</b> to the <b>NumericTextBox </b>controls. The default value for <b>enableRTL </b>is false    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 11,            <b>enableRTL: true</b>        });            &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** when **enableRTL** is **“True”** is as follows. 

{% include image.html url="/js/NumericTextBox/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="NumericTextBox with enableRTL"%}

