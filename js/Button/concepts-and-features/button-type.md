---
layout: post
title: button-type
description: button type
platform: js
control: Button
documentation: ug
---

# Button Type

**Button** is used as normal clickable button, submitting form data, resetting the form data to its initial value. According to the usage of button, you can render the button in three types. Using the **type** property, you can easily render the button in following types.

_Table_ _4__: List of Button types_

<table>
<tr>
<td>
<b>Button</b></td><td>
The button is a clickable button </td></tr>
<tr>
<td>
<b>submit</b></td><td>
The button is a submit button (submits form-data) </td></tr>
<tr>
<td>
<b>reset    </b></td><td>
The button is a reset button (resets the form-data to its initial values)</td></tr>
</table>


The following steps explains you the details about rendering the **Button** with above mentioned button types.

* In the **HTML** page, add the following button elements to configure **Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>    <button id="buttonType_button">button</button>    &lt;br /&gt;    &lt;br /&gt;    <button id="buttonType_submit">submit</button>    &lt;br /&gt;    &lt;br /&gt;    <button id="buttonType_reset">reset</button></td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    //type property is used to render different type of buttons    $(function () {        $("#buttonType_button").ejButton({            size: "mini",            //this type specifes the normal clickable button<b>            type: "button",</b>            showRoundedCorner: true        });        $("#buttonType_submit").ejButton({            size: "mini",            //this button is used to submit form data<b>            type: "submit",</b>            showRoundedCorner: true        });        $("#buttonType_reset").ejButton({            size: "mini",            //this button is used to reset the form data to its initial value<b>            type: "reset",</b>            showRoundedCorner: true        });    });    &lt;/script&gt;</td></tr>
</table>



Execute the above code to render the following output.

![](button-type_images\button-type_img1.png)

_Figure 9: Different button types_

