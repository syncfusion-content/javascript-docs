---
layout: post
title: keyboard-interaction
description: keyboard interaction
platform: js
control: PercentageTextBoxEditors 
documentation: ug
---

# Keyboard Interaction

With the keyboard navigation enabled in the **PercentageTextBox Textbox** control, it is possible to control the actions of the **PercentageTextBox Textbox** with the provided shortcut keys. Almost all the **PercentageTextBox Textbox** actions that are done through mouse can be controlled with shortcut keys.

The various keyboard shortcuts available within the **PercentageTextBox Textbox** control are discussed in the following table. 

_Table_ _1__: Keyboard Shortcuts_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
<a href=http://en.wikipedia.org/wiki/Access_key>Access key</a><b> + j</b></td><td>
Focuses the PercentageTextBox<b> </b>control</td></tr>
<tr>
<td>
Up</td><td>
Increments the value</td></tr>
<tr>
<td>
Down</td><td>
Decrements the value</td></tr>
<tr>
<td>
Tab</td><td>
Focus the next element</td></tr>
</table>
## Configuring Keyboard Navigation

The following steps explain the implementation of keyboard interaction in **PercentageTextBox Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox Textbox** controls. Set the **accesskey** property to the **PercentageTextBox Textbox** control for focusing the control while key is pressed.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" accesskey="j"/&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" accesskey="j" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 11                    });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 22                    });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 33                    });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[_cshtml]</b>@*<b> Add the following code in your view page to render Textbox controls.</b>*@@Html.EJ().NumericTextbox("numeric").Value("11")@Html.EJ().PercentageTextbox("percentage").Value("22")@Html.EJ().CurrencyTextbox("currency").Value("33")</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code in your script section.$(document).on("keydown", function (e) {        if (e.altKey && e.keyCode === 74) { // j- key code.            $("#numeric").<b>focus();</b>           }    });</td></tr>
</table>


<table>
<tr>
<td>
<b>[_aspx]</b>&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;&lt;ej:NumericTextBox ID="numeric" Value="11"  runat="server" &gt;&lt;/ej:NumericTextBox&gt;&lt;ej:PercentageTextBox ID="percentage" Value="22" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;&lt;ej:CurrencyTextBox ID="currency" Value="33" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code in your script section.$(document).on("keydown", function (e) {        if (e.altKey && e.keyCode === 74) { // j- key code.            $("#numeric").<b>focus();</b>           }    });</td></tr>
</table>


Run the above example and press [Access key](http://en.wikipedia.org/wiki/Access_key) **+ j** key to focus the **PercentageTextB****ox********Textbox**widget. Perform provided functionality by using keyboard shortcuts.



{% include image.html url="\js\PercentageTextBox\concepts-and-features\keyboard-interaction_images\keyboard-interaction_img1.png" Caption="Figure 4731: PercentageTextBoxTextbox focused with keyboard shortcut"%}{% include image.html url="\js\PercentageTextBox\concepts-and-features\keyboard-interaction_images\keyboard-interaction_img2.png" Caption="Figure 4731: PercentageTextBoxTextbox focused with keyboard shortcut"%}





















