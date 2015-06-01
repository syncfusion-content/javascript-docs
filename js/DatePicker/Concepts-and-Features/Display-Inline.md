---
layout: post
title: Display-Inline
description: display inline
platform: js
control: DatePicker
documentation: ug
---

# Display Inline

**Display****Inline** allows you to make **DatePicker** widget similar to a **Calendar date**. Also associate **DatePicker** with **&lt;div&gt;** element instead of input. Default value for **displayInline** property is set as ‘**false**’ 

The following steps explain you how to get the **Calendar** control using **DatePicker**.

* In the **HTML** page, add a **&lt;div&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="datepicker" /&gt; &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to get the <b>Calendar</b> control using <b>DatePicker</b>&lt;script type="text/javascript"&gt;$(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                displayInline: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>




* The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Display-Inline_images/Display-Inline_img1.png" Caption="Figure 15: Calendar date in DatePicker"%}

