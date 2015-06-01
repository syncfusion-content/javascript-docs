---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: DatePicker
documentation: ug
---

# RTL Support

Right-to-left starts from the right of the page and continues to the left. By default, this option is set to “**false**” in the **DatePicker** widget. 

The **enableRTL** option allows the **DatePicker** widget to display it in the right to left direction.

The following steps explain you how to enable the **RTL** property of the **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to enable the <b>RTL</b> property of the <b>DatePicker</b> widget     &lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                <b>enableRTL: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


*  The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 21: RTL Support in DatePicker"%}

