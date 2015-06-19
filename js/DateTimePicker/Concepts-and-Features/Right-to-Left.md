---
layout: post
title: Right-to-Left
description: right-to-left
platform: js
control: DateTimePicker
documentation: ug
---

# Right-to-Left

RTL control supportsright-to-leftfunctionality and features for languages that work right-to-left for selecting and editing date and time. You can change your popup and textbox display to read right-to-left. Arabic and Hebrew are written from right to left. The customer who has a right to left writing style can use this feature. You can achieve this in your **DateTimePicker**by using **enableRTL** property. Setting this property to “**True**”allows you to write in the right to left format. Position of the toolbars are also changed to right to left.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b> [HTML]    </b>   &lt;div class="control"&gt;        &lt;input type="text" id="dateTime" /&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code in your script section to render <b>DateTimePicker</b> with right to left appearance<b>//</b>            $('#dateTime').ejDateTimePicker({                width: 200,<b>                enableRTL:true,</b>            });</td></tr>
</table>
{% include image.html url="/js/DateTimePicker/Concepts-and-Features/Right-to-Left_images/Right-to-Left_img1.png" Caption="Figure 14: Showcase of DateTimePicker with Right to Left appearance"%}

