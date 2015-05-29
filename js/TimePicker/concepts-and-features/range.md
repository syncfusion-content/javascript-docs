---
layout: post
title: range
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
<b>[JavaScript]</b><b>// Use minTime and maxTime property to change the Range of the TimePicker.</b>$(function () {                $('#time').ejTimePicker({                 minTime: "10:00 AM"”10:00 AM”,                maxTime: "9:00 PM"”9:00 PM”        }); });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render TimePicker.**



      @Html.EJ().TimePicker("time").**MinTime**("10:00 AM").**MaxTime**("10:00 PM")





**[_aspx]**

**//** Add the code in ASPX page to render TimePicker

&lt;ej:TimePicker ID="time" MinTime="10:00 AM" MaxTime="10:00 PM" runat="server"&gt;&lt;/ej:TimePicker&gt;



Execute the above code to render the following output.



![](range_images\range_img1.png)

_Figure_ _3__19__2__: Range for_ _TimePicker_ _widget_

