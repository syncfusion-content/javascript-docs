---
layout: post
title: time-format
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
<b>[JavaScript]</b><b>// Change time format for TimePicker controls as follows.</b>$(function () {                $('#time').ejTimePicker({                 timeFormat: "h:mm:ss tt"”h:mm:ss tt”         }); });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to Render TimePicker.**



    @Html.EJ().TimePicker("time").**TimeFormat**("**hh:mm:ss tt**")





**[_aspx]**

**//** Add the code in ASPX page to render TimePicker

&lt;ej:TimePicker ID="time" TimeFormat="hh:mm:ss tt" runat="server"&gt;&lt;/ej:TimePicker&gt;



Execute the above code to render the following output.



![](time-format_images\time-format_img1.png)

_Figure_ _20__33__:_ _TimePicker_ _with time format._

