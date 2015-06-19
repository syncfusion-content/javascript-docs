---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: TagCloud
documentation: ug
---

# RTL Support

This feature supports you to change the left-to-right alignment of the **TagCloud** widget to right-to-left (RTL). This displays the content from right-to-left in the widget. You can achieve this using **enableRTL** property that is set false by default.

## Enabling RTL Support

The following steps explains you the enabling of right-to-left property in **TagCloud**.

1. In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

<table>
<tr>
<td>
<b>[HTML]</b>         &lt;div id="techweblist"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable RTL property for TagCloud.    $("#techweblist").ejTagCloud({                enableRTL:true,                titleText: "Tech Sites",                dataSource: websiteCollection           });</td></tr>
</table>
The following screenshot illustrates the **TagCloud** control with RTL support.

{% include image.html url="/js/TagCloud/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption=""%}

_TagCloud with enabled RTL_



