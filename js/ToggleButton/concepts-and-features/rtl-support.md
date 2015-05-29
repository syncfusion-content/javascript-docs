---
layout: post
title: rtl-support
description: rtl support
platform: js
control: Toggle Button
documentation: ug
---

# RTL support

In some cases, it is necessary to use right to left alignment. You can render **RTL** support by using **enableRTL** property. In **RTL** mode, when there is more than one content (image/text, image/image) in button, then the content is aligned in right to left format. For example, when text is in left and image is in right position, after applying right to left alignment these positions are interchanged.

The following steps explains you the details about rendering the **Toggle Button** with Right to left alignment support.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="checkbox" id="toggle_rtl" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            $("#toggle_rtl").ejToggleButton({                size: "small",                imagePosition: "imageleft",                contentType: "textandimage",                showRoundedCorner: true,                defaultText: "Play",                activeText: "Next",                defaultPrefixIcon: "e-mediaplay e-uiLight",                activePrefixIcon: "e-mediapause e-uiLight",                //used to enable or disable RTL support for toggle button<b>                enableRTL: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure the widget and initialize the control



    &lt;div class="one"&gt;

    @*enable right to left alignment*@

                 @Html.EJ().ToggleButton("toggleButton_rtl").Size(ButtonSize.Small).ShowRoundedCorner(true).ContentType(ContentType.TextAndImage).DefaultText("Play").ActiveText("Next").DefaultPrefixIcon("e-mediaplay").ActivePrefixIcon("e-medianext").**EnableRTL(true)**       

    &lt;/div&gt;



**[aspx]**

// Add the code in ASPX page to configure Toggle Button widget

&lt;%--enable right to left alignment--%&gt;



    &lt;ej:ToggleButton ID="ToggleButton_RTL" runat="server" Size="Small" ShowRoundedCorner="true" DefaultText="Play" ActiveText="Pause" ContentType="TextAndImage" DefaultPrefixIcon="e-mediaplay" ActivePrefixIcon="e-mediapause" EnableRTL="true"&gt;&lt;/ej:ToggleButton&gt;



In above mentioned code example **prefixIcon** property is used and the icon that is to be on left side, (before text) is rendered on right side as **enableRTL** property is used with **prefixIcon.**  Consequently, the alignment is changed in right to left order.

Output of above steps



![](rtl-support_images\rtl-support_img1.png)

_Figure_ _18__12__: Toggle button with RTL support_

