---
layout: post
title: behavior-settings
description: behavior settings
platform: js
control: ColorPicker
documentation: ug
---

# Behavior Settings

## showPreview

The **ColorPicker** control provides live preview support for current cursor selection color and selected color. **showPreview** property allows you to preview the selected color in the picker or from the palette.

The **showPreview** property is Boolean type and its default value is true.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget



<table>
<tr>
<td>
<b>[HTML]</b>     &lt;input type="text" id="colorPicker" /&gt;    </td></tr>
<tr>
<td>
<b>[JAVASCRIPT]</b> &lt;script&gt;    jQuery(function ($) {        $("#colorPicker").ejColorPicker({ value: "#278787", showPreview: true });      });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**//** In the **CSHTML** page, add the Html helpers to render **ColorPicker** widget

@Html.EJ().ColorPicker("colorPicker").Value("#278787").ShowPreview(true)



**[ASPX]**

// In the **ASPX** page add the following code to render **ColorPicker** widget

&lt;ej:ColorPicker runat="server" ID="colorpicker" Value="#278787" ShowPreview="true"&gt; &lt;/ej:ColorPicker&gt;



The following screenshot displays the output of the above code example.

{% include image.html url="\js\ColorPicker\concepts-and-features\behavior-settings_images\behavior-settings_img1.png" Caption="Figure 135: ColorPicker with Show Preview option"%}

## showRecentColors

The **ColorPicker** control allows you to store the color values in custom list by using **showRecentColors** property. The **ColorPicker** keeps up to 11 colors in a custom list.  By clicking the add button, the selected color from picker or palette gets added in the recent color list.  

The **showRecentColors** property is Boolean type and its default value is false.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget



<table>
<tr>
<td>
<b>[HTML]</b>     &lt;input type="text" id="colorPicker" /&gt;    </td></tr>
<tr>
<td>
<b>[JAVASCRIPT]</b> &lt;script&gt;    jQuery(function ($) {        $("#colorPicker").ejColorPicker({ value: "#278787", showRecentColors: true });      });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**//** In the **CSHTML** page, add the Html helpers to render **ColorPicker** widget

@Html.EJ().ColorPicker("colorPicker").Value("#278787").ShowRecentColors(true)



**[ASPX]**

// In the **ASPX** page add the following code to render **ColorPicker** widget

&lt;ej:ColorPicker runat="server" ID="colorpicker" Value="#278787" ShowRecentColors="true"&gt; &lt;/ej:ColorPicker&gt;



The following screenshot displays the output of the above code example.

{% include image.html url="\js\ColorPicker\concepts-and-features\behavior-settings_images\behavior-settings_img2.png" Caption="Figure 146: ColorPicker with Recent Color Swatches"%}

## enableOpacity

The **ColorPicker** control allows you to enable or disable the opacity slider. You can achieve this by using the **enableOpacity** property. 

The **enableOpacity** property is Boolean type and its default value is true.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget



<table>
<tr>
<td>
<b>[HTML]</b> &lt;input type="text" id="colorPicker" /&gt;    </td></tr>
<tr>
<td>
<b>[JAVASCRIPT]</b> &lt;script&gt;    jQuery(function ($) {        $("#colorPicker").ejColorPicker({ value: "#278787", enableOpacity: false });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**//** In the **CSHTML** page, add the Html helpers to render **ColorPicker** widget

 @Html.EJ().ColorPicker("colorPicker").Value("#278787").EnableOpacity(false) 



**[ASPX]**

// In the **ASPX** page add the following code to render **ColorPicker** widget

 &lt;ej:ColorPicker runat="server" ID="colorpicker" Value="#278787" EnableOpacity="false"&gt; &lt;/ej:ColorPicker&gt;



The following screenshot displays the output of the above code example.

{% include image.html url="\js\ColorPicker\concepts-and-features\behavior-settings_images\behavior-settings_img3.png" Caption="Figure 157: ColorPicker with Opacity Slider as disabled state"%}

## columns

The palette model consists of color values in the rows and columns order. Palette only consists of predefined colors and allows you to select anyone color from it. The **columns** property allows you to modify the number of columns in palette model. 

The **columns** property is Number type and its default value is 10.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget



<table>
<tr>
<td>
<b>[HTML]</b> &lt;input type="text" id="colorPicker" /&gt;    </td></tr>
<tr>
<td>
<b>[JAVASCRIPT]</b> &lt;script&gt;    jQuery(function ($) {        $("#colorPicker").ejColorPicker({ value: "#278787", columns: 9 });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**//** In the **CSHTML** page, add the Html helpers to render **ColorPicker** widget

 @Html.EJ().ColorPicker("colorPicker").Value("#278787").Columns(9)



**[ASPX]**

// In the **ASPX** page add the following code to render **ColorPicker** widget

 &lt;ej:ColorPicker runat="server" ID="colorpicker" Value="#278787" Columns="9"&gt; &lt;/ej:ColorPicker&gt;



The following screenshot displays the output of the above code example.

{% include image.html url="\js\ColorPicker\concepts-and-features\behavior-settings_images\behavior-settings_img4.png" Caption="Figure 168: ColorPicker with Columns"%}

