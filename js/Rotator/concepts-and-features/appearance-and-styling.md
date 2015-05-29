---
layout: post
title: appearance-and-styling
description: appearance and styling
platform: js
control: Rotator
documentation: ug
---

# Appearance and Styling

## Adjusting rotator item size

### Slide width

This property sets the **width** of a **Rotator** Item. The value set to this property is **string** or **number**.

<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ <b>slideWidth: "500px"</b> });    });&lt;/script&gt;<b>(or)</b></td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ <b>slideWidth: 500</b> });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).**SlideWidth**("600px").SlideHeight("350px")



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



### Slide height

This property sets the **height** of a **Rotator** Item. The value set to this property is **string** or **number**.

<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ <b>slideHeight: "500px"</b> });    });&lt;/script&gt;<b>(or)</b></td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ <b>slideHeight: 500</b> });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").**SlideHeight**("350px")



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideHeight="350px" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



