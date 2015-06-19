---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: CurrencyTextBox  
documentation: ug
---

# RTL Support

The **Textbox** provides **RTL** (**Right-To-Left**) support. The alignment of **CurrencyTextBox** can be changed from **Left-To-Right** into **Right-To-Left**.

## Enable RTL

The following steps explain the implementation of **enableRTL** in **CurrencyTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** controls.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input id="currency" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enableRTL </b>property<b> </b>as<b> “True”</b> to the <b>CurrencyTextBox </b>controls. The default value for <b>enableRTL </b>is false    &lt;script type="text/javascript"&gt;        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 33,            <b>enableRTL: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **CurrencyTextBox** when **enableRTL** is **“True”** is as follows. 

{% include image.html url="/js/Currency/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 30: CurrencyTextBox with enableRTL"%}

