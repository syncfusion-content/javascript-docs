---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: PercentageTextBox 
documentation: ug
---

# RTL Support

The **PercentageTextBox** provides **RTL** (**Right-To-Left**) support. The alignment of **PercentageTextBox** can be changed from **Left-To-Right** into **Right-To-Left**.

## Enable RTL

The following steps explain the implementation of **enableRTL** in **PercentageTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enableRTL </b>property<b> </b>as<b> “true”</b> to the <b>PercentageTextBox </b>controls. The default value for <b>enableRTL </b>is false    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 22,            <b>enableRTL: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** when **enableRTL** is **“true”** is as follows. 

{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 30: PercentageTextBox with enableRTL"%}

