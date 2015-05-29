---
layout: post
title: rtl-support
description: rtl support
platform: js
control: TagCloud
documentation: ug
---

# RTL Support

This feature supports you to change the left-to-right alignment of the **TagCloud** widget to right-to-left (RTL). This displays the content from right-to-left in the widget. You can achieve this using **enableRTL** property that is set false by default.

## Enabling RTL Support

The following steps explains you the enabling of right-to-left property in **TagCloud**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;div id="techweblist"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable RTL property for TagCloud.    $("#techweblist").ejTagCloud({<b>                enableRTL:true,</b>                titleText: "Tech Sites",<b>                </b>dataSource: websiteCollection           });</td></tr>
</table>


**[CSHTML]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



@Html.EJ().TagCloud("tagcloud").Datasource((IEnumerable<MvcApplication2.WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("Text").Url("Url").Frequency("Frequency")).Title("Tech sites").**EnableRTL(true)**



**[ASPX]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



&lt;ej:TagCloud ID="tagcloud" runat="server" DataTextField="text" DataUrlField="url" DataFrequencyField="frequency" EnableRTL="true"&gt;**&lt;/ej:TagCloud&gt;**



The following screenshot illustrates the **TagCloud** control with RTL support.



![](rtl-support_images\rtl-support_img1.png)

_Figure_ _1__8__3__: TagCloud with enabled RTL_

