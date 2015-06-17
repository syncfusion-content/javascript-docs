---
layout: post
title: Button-Type
description: button type
platform: js
control: Button
documentation: ug
---

# Button Type

**Button** is used as normal clickable button, submitting form data, resetting the form data to its initial value. According to the usage of button, you can render the button in three types. Using the **type** property, you can easily render the button in following types.

_List of Button types_

<table>
<tr>
<td>
<b>button</b></td><td>
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

1. In the **HTML** page, add the following button elements to configure **Button** widget.

{% highlight html %}


    <button id="buttonType_button">button</button>
    <br />
    <br />
    <button id="buttonType_submit">submit</button>
    <br />
    <br />
    <button id="buttonType_reset">reset</button>
	
{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
    // Initialize the control in JavaScript
    //type property is used to render different type of buttons
    $(function () {
        $("#buttonType_button").ejButton({
            size: "mini",
            //this type specifes the normal clickable button
            type: "button",
            showRoundedCorner: true
        });
        $("#buttonType_submit").ejButton({
            size: "mini",
            //this button is used to submit form data
            type: "submit",
            showRoundedCorner: true
        });
        $("#buttonType_reset").ejButton({
            size: "mini",
            //this button is used to reset the form data to its initial value
            type: "reset",
            showRoundedCorner: true
        });
    });
    </script>

{% endhighlight %}

Execute the above code to render the following output.

{% include image.html url="/js/Button/Concepts-and-Features/Button-Type_images/Button-Type_img1.png" Caption=""%}

_Different button types_

