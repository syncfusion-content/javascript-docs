---
layout: post
title: miscellaneous
description: miscellaneous
platform: js
control: Toggle Button
documentation: ug
---

# Miscellaneous

## Show Rounded Corner 

It sets the corner of **Toggle Button** in rounded shape. The **Toggle Button**, by default doesn’t have rounded corner. To set rounded corner, you can enable **showRoundedCorner** property**.**

The following steps explains you the details about rendering the **Toggle Button** with Rounded corner support. 

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="checkbox" id="toggle_roundedCorenr" /&gt;  </td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            $("#toggle_roundedCorenr").ejToggleButton({                size: "small",                contentType: "textandimage",                //used to specify the rounded corner for toggle button<b>                showRoundedCorner: true,</b>                defaultText: "Play",                activeText: "Next",                defaultPrefixIcon: "e-mediaplay e-uiLight",                activePrefixIcon: "e-mediapause e-uiLight"            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure the widget and initialize the control



    &lt;div class="one"&gt;

        @*set rounded corner for toggle button*@       

                 @Html.EJ().ToggleButton("toggleButton_roundedCorner").Size(ButtonSize.Small).**ShowRoundedCorner(true).**ContentType(ContentType.TextAndImage).DefaultText("Play").ActiveText("Next").DefaultPrefixIcon("e-mediaplay").ActivePrefixIcon("e-medianext")       

    &lt;/div&gt;



**[aspx]**

// Add the code in ASPX page to configure Toggle Button widget

&lt;%--set rounded corner for toggle button--%&gt;



    &lt;ej:ToggleButton ID="ToggleButton_RoundedCorner" runat="server" Size="Small" ShowRoundedCorner="true" DefaultText="Play" ActiveText="Pause" ContentType="TextAndImage" DefaultPrefixIcon="e-mediaplay" ActivePrefixIcon="e-mediapause"&gt;&lt;/ej:ToggleButton&gt;



Execute the above code to render the following output.

![](miscellaneous_images\miscellaneous_img1.png)

_Figure_ _19__13__: Toggle button with Rounder corner_

**Prevent Toggle**

This property is used to prevent the state change of **Toggle Button** when it is clicked. When you set **preventToggle** property****as true, then the state of the **Toggle Button** is not changed even though it is clicked.

The following steps explains you the details about rendering the **Toggle Button** with **preventToggle** property enabled.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="checkbox" id="toggle_prevent" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            $("#toggle_prevent").ejToggleButton({                size: "small",                contentType: "textandimage",                defaultText: "Play",                activeText: "Next",                defaultPrefixIcon: "e-mediaplay e-uiLight",                activePrefixIcon: "e-mediapause e-uiLight",                //prevent changing state of toggle button<b>                preventToggle: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure the widget and initialize the control



    &lt;div class="one"&gt;

        @* set prevent toggle property for preventing states*@       

                 @Html.EJ().ToggleButton("toggleButton_preventToggle").Size(ButtonSize.Small).ContentType(ContentType.TextAndImage).DefaultText("Play").ActiveText("Next").DefaultPrefixIcon("e-mediaplay").ActivePrefixIcon("e-medianext")**.PreventToggle(true)**       

    &lt;/div&gt;



**[aspx]**

// Add the code in ASPX page to configure Toggle Button widget

&lt;%--set prevent toggle property for preventing states--%&gt;



    &lt;ej:ToggleButton ID="ToggleButton_Prevent" runat="server" Size="Small" DefaultText="Play" ActiveText="Pause" ContentType="TextAndImage" DefaultPrefixIcon="e-mediaplay" ActivePrefixIcon="e-mediapause" PreventToggle="true"&gt;&lt;/ej:ToggleButton&gt;



Execute the above code to render the following output.



![](miscellaneous_images\miscellaneous_img2.png)

_Figure_ _20__14__: Toggle button with prevent Togg_le._le_





