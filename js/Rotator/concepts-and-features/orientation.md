---
layout: post
title: orientation
description: orientation
platform: js
control: Rotator
documentation: ug
---

# Orientation

The **Rotator** control supports both vertical and horizontal orientations allowing it to fit into any scenario. The **Rotator** property **orientation** defines the **orientation** where the control is rendered. The value set to this property is **enum or string** type. It accepts the following values.

* ej.Orientation.Horizontal or “Horizontal”

* ej.Orientation.Vertical  or “Vertical”

The following steps explain you how to set **orientation** for the **Rotator**.

## Horizontal

This property sets the **Rotator** in **horizontal****orientation**. You can refer the following steps to set **horizontal****orientation** for **Rotator** control.

* In **View**, create ul-li list of **Rotator** items and invoke the **Rotator** helper.

* Add the following script in your **HTML** page.

<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ slideWidth: 500, <b>orientation: ej.Orientation.Horizontal</b> });    });&lt;/script&gt; <b>(or)</b></td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ slideWidth: 500, <b>orientation: "Horizontal"</b> });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**Orientation**(Syncfusion.JavaScript.Orientation.Horizontal)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" Orientation="Horizontal" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;

## Vertical

This property sets the **Rotator** in **vertical****orientation**. You can refer the following steps to set **vertical****orientation** for **Rotator** control.

* Create ul-li list of **Rotator** items and invoke the **Rotator** helper.

* Add the following script in your **HTML** page.

<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ slideWidth: 500, <b>orientation: ej.Orientation.Vertical</b> });    });&lt;/script&gt;<b>(or)</b></td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ slideWidth: 500, <b>orientation: "Vertical"</b> });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**Orientation**(Syncfusion.JavaScript.Orientation.Vertical)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" Orientation="Vertical" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



