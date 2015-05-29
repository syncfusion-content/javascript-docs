---
layout: post
title: orientation
description: orientation
platform: js
control: Toolbar
documentation: ug
---

# Orientation

The **Toolbar** control supports both vertical and horizontal orientations, allowing it to fit into any scenario. The **orientation** property **of Toolbar** defines the orientation in which the control is rendered. Set the value to this property as **enum or string** type. It accepts the following values.

* ej.Orientation.Horizontal or “Horizontal”

* ej.Orientation.Vertical  or “Vertical”

The following section explains you on how to set orientation for the toolbar.

## Horizontal

This property sets the **Toolbar** in **horizontal** orientation. You can refer the following steps to set horizontal orientation for **Toolbar** control.

1. In View, create ul-li list of toolbar items and invoke the toolbar helper.

Add the following script in your **HTML** page.


<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ width: "290px", orientation: ej.Orientation.Horizontal });    });&lt;/script&gt;</td></tr>
<tr>
<td>
<b>OR</b><b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration                    $("#toolbarcontent").ejToolbar({ width: "290px", orientation: "Horizontal" });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).**Orientation**(Syncfusion.JavaScript.Orientation.Horizontal)

&lt;/div&gt;



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;

&lt;div class="cols-sample-area"&gt;

    &lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px" Orientation="Horizontal" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;

&lt;/div&gt;



Build and run the application.

The following screenshot illustrates a **Toolbar** with horizontal orientation.

![](orientation_images\orientation_img1.png)

_Figure_ _25__10__: Toolbar with Horizontal Orientation_

## Vertical

This property sets the **Toolbar** in **vertical** orientation. You can refer the following steps to set vertical orientation for **Toolbar** control.

* Create ul-li list of toolbar items and invoke the toolbar helper.

Add the following script in your **HTML** page.


<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ orientation: ej.Orientation.Vertical });    });&lt;/script&gt;</td></tr>
<tr>
<td>
<b>OR</b><b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ orientation: "Vertical" });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).**Orientation**(Syncfusion.JavaScript.Orientation.Vertical)

&lt;/div&gt;



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;

&lt;div class="cols-sample-area"&gt;

    &lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px" Orientation="Vertical" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;

&lt;/div&gt;



Build and run the application.

The following screenshot illustrates a **Toolbar** with vertical orientation.

![](orientation_images\orientation_img2.png)

_Figure_ _26__11__: Toolbar with Vertical Orientation_

