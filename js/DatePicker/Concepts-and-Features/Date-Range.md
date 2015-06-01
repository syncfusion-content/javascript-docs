---
layout: post
title: Date-Range
description: date range
platform: js
control: DatePicker
documentation: ug
---

# Date Range

**Date Range** from minimum to maximum value is set for **DatePicker** widget using “**minDate”** and “**maxDate”** properties respectively. This allows you to restrict the date selection between the **minDate** and **maxDate**. This disables the dates below the **minDate** and dates above the **maxDate**.

The following steps explain you how to get the **Date Range** of **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to set the <b>Date Range</b> of <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                <b>minDate: new Date("2014/06/03"),</b><b>                maxDate: new Date("2014/06/19")</b>            });        });    &lt;/script&gt;</td></tr>
</table>


*  The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Date-Range_images/Date-Range_img1.png" Caption="Figure 16: Date Range in DatePicker"%}

