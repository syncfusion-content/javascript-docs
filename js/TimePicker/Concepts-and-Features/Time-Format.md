---
layout: post
title: Time-Format
description: time format
platform: js
control: TimePicker
documentation: ug
---

# Time Format

**TimePicker** widget provides you an option to change the time format.

### Steps to change Time Format of TimePicker widget

The following steps explains you to change the time format for the **TimePicker**.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Change time format for TimePicker controls as follows.</b>$(function () {                $('#time').ejTimePicker({                 timeFormat: "h:mm:ss tt"         }); });</td></tr>
</table>


Execute the above code to render the following output.



{% include image.html url="/js/TimePicker/Concepts-and-Features/Time-Format_images/Time-Format_img1.png" Caption=""%}

_Figure_ _20__: TimePicker with time format._

