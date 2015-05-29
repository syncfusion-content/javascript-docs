---
layout: post
title: rtl
description: rtl
platform: js
control: TimePicker
documentation: ug
---

# RTL

This feature supports to change the left-to-right alignment of the **TimePicker** widget to right-to-left(**RTL**). The custom template **TimePicker** also supports **RTL**.

### Enabling Right-To-Left Support

The following steps explains you in enabling the right-to-left property for the **TimePicker**.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.   



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Enable RTL for TimePicker controls as follows.</b>$(function () {           $('#time').ejTimePicker({                       enableRTL: true                 }); });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render TimePicker.**



         @Html.EJ().TimePicker("time").**EnableRTL**(**true**)



**[_aspx]**

**//** Add the code in ASPX page to render TimePicker

&lt;ej:TimePicker ID="time" EnableRTL="true" runat="server"&gt;&lt;/ej:TimePicker&gt;



The following screenshot illustrates a **TimePicker** control when **enableRTL** is set to **“true”**



![](rtl_images\rtl_img1.png)

_Figure_ _21__34__:_ _TimePicker_ _template with RTL support_

