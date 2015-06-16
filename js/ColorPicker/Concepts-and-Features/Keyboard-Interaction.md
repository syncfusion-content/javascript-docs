---
layout: post
title: Keyboard-Interaction
description: keyboard interaction
platform: js
control: ColorPicker
documentation: ug
---

# Keyboard Interaction

You can use **keyboard** shortcut keys as an alternative to the mouse while using the **ColorPicker** widget. The **ColorPicker** widget allows you to perform all kinds of actions using **keyboard** shortcuts.

_Table_ _6__: Keyboard shortcut keys_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Alt + j               </td><td>
Focuses into the <b>ColorPicker</b> control</td></tr>
<tr>
<td>
Enter</td><td>
Open / Close the Popup</td></tr>
<tr>
<td>
Up</td><td>
Increase the brightness value</td></tr>
<tr>
<td>
Down</td><td>
Decrease the brightness value</td></tr>
<tr>
<td>
Right</td><td>
Increase the staturation value</td></tr>
<tr>
<td>
Left</td><td>
Decrease the staturation value</td></tr>
<tr>
<td>
Enter</td><td>
Choose the current color</td></tr>
<tr>
<td>
Esc</td><td>
Closes the popup</td></tr>
<tr>
<td>
Tab</td><td>
Choose the next element</td></tr>
<tr>
<td>
Home</td><td>
Downwards to value 0</td></tr>
<tr>
<td>
End</td><td>
Upwards to value 100</td></tr>
</table>

**Configure Keyboard Interaction**

The following steps explain how you can enable **keyboard** interaction for **ColorPicker** textbox.

*     In the **HTML** page, add an **&lt;input&gt;** element to configure the **ColorPicker** widget and enable keyboard interaction by the **accesskey** property.

{% highlight html %}


    <input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight js %}

 
<script>
    jQuery(function ($) {
          $('#colorPicker').ejColorPicker({ value: "#278787", displayInline: true });
          $(document).on("keydown", function (e) {
                if (e.altKey && e.keyCode === 74) { // j- key code.
                    $("#colorPickerWrapper").focus();
                }
            });
    });
</script>

{% endhighlight %}

The following screenshot displays the output of the above code example.



{% include image.html url="/js/ColorPicker/Concepts-and-Features/Keyboard-Interaction_images/Keyboard-Interaction_img1.png" Caption="Figure 19: ColorPicker with Keyboard Navigation"%}

