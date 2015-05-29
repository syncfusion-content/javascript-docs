---
layout: post
title: timepicker-customization
description: timepicker customization
platform: js
control: TimePicker
documentation: ug
---

# TimePicker Customization

The **TimePicker** provides support to display a **TimePicker** in your webpage and allows you to pick a time from it.

## Creating TimePicker Widget

The following steps explains you to create a **TimePicker** widget.

* In an **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.


<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// You can render TimePicker control as follows.</b>$(function () {           $('#time').ejTimePicker(); });</td></tr>
</table>


**[_cshtml]**

**// Add the following code example in your view page to render TimePicker.**

       @Html.EJ().**TimePicker**("**time**")



**[_**aspx**]**

**//** Add the code in ASPX page to render TimePicker

      &lt;ej:TimePicker ID="time" runat="server"&gt;&lt;/ej:TimePicker&gt;



The following screenshot illustrates you a default **TimePicker**.



![](timepicker-customization_images\timepicker-customization_img1.png)

_Figure_ _7__:_ _TimePicker Control_

_Figure_ _20__: TimePicker Control_

