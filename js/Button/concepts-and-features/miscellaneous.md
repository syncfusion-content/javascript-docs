---
layout: post
title: miscellaneous
description: miscellaneous
platform: js
control: Button
documentation: ug
---

# Miscellaneous

## Text

You can display the user defined text for **Button**. Using **text** property, you can easily set text content for button. This text property overwrites the text that is provided on input button element.

The following steps explains you the details about rendering the button with specified text.

* In the **HTML** page, add the following button elements to configure **Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b><button id="button_text">button</button></td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            $("#button_text").ejButton({                size: "mini",                //used to set the text content for button<b>                text: "Enter"</b>            });        });    &lt;/script&gt;</td></tr>
</table>


In the above code, the content of button “button” is replaced by the text value “Enter” that is given using text property.

Execute the above code to render the following output.

![](miscellaneous_images\miscellaneous_img1.png)

_Figure 13: Button with new text_

## Show Rounded Corner

Specifies the corner of button in round shape. By default button doesn’t have rounded corner. To set rounded corner, you can enable **showRoundedCorner** property**.**

The following steps explains you the details about rendering the button with rounded corner.

* In the **HTML** page, add the following button elements to configure **Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b><button id="button_roundedCorner">button</button></td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            $("#button_roundedCorner").ejButton({                size: "mini",                //Enable or disable the rounded corner for button          <b>                showRoundedCorner: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>

Execute the above code to render the following output.

![](miscellaneous_images\miscellaneous_img2.png)

_Figure 14: Button with rounded corner_



