---
layout: post
title: rtl-support
description: rtl support
platform: js
control: CurrencyTextBox Editors 
documentation: ug
---

# RTL Support

The **Textbox** provides **RTL** (**Right-To-Left**) support. The alignment of **CurrencyTextBox Textboxes** can be changed from **Left-To-Right** into **Right-To-Left**.

## Enable RTL

The following steps explain the implementation of **enableRTL** in **CurrencyTextBox Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox Textbox** controls.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enableRTL </b>property<b> </b>as<b> “True”</b> to the <b>CurrencyTextBox Textbox</b> controls. The default value for <b>enableRTL </b>is false    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 11,            <b>enableRTL: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 22,            <b>enableRTL: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 33,            <b>enableRTL: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("11").**EnableRTL(true)**

@Html.EJ().PercentageTextbox("percentage").Value("22").**EnableRTL(true)**

@Html.EJ().CurrencyTextbox("currency").Value("33").**EnableRTL(true)**



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="11" EnableRTL="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" Value="22" EnableRTL="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency" Value="33" EnableRTL="true"  runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **CurrencyTextBox Textboxes** when **enableRTL** is **“True”** is as follows. 

{% include image.html url="\js\Currency\concepts-and-features\rtl-support_images\rtl-support_img1.png" Caption="Figure 383046: CurrencyTextBox Textboxes with enableRTL"%}{% include image.html url="\js\Currency\concepts-and-features\rtl-support_images\rtl-support_img2.png" Caption="Figure 383046: CurrencyTextBox Textboxes with enableRTL"%}

