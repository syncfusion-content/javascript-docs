---
layout: post
title: Range
description: range
platform: js
control: TimePicker
documentation: ug
---

# Range

**TimePicker** widget provide options to set the Range (minTime & maxTime) for the time.

## Steps to change minTime & maxTime of the TimePicker

The following steps explains you to change the Range of the **TimePicker**.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Use minTime and maxTime property to change the Range of the TimePicker.</b>$(function () {                $('#time').ejTimePicker({                 minTime: "10:00 AM",                maxTime: "9:00 PM"        }); });</td></tr>
</table>


Execute the above code to render the following output.



{% include image.html url="/js/TimePicker/Concepts-and-Features/Range_images/Range_img1.png" Caption=""%}

_Figure_ _19__: Range for TimePicker widget_

