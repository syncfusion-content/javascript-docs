---
layout: post
title: rtl-support-
description: rtl support 
platform: js
control: Uploadbox
documentation: ug
---

# RTL Support 

This feature supports the change of left-to-right alignment of the **UploadBoxUploadbox** widget to right-to-left (**RTL**). That is, it sets the **UploadBoxUploadbox** to right-to-left actions.

The following steps explain the configuration of **enableRTL** property in **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="Uploadbox"&gt;&lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b> <b>// Initialize the control in JavaScript.</b>$(function () {//Declaration.            $("#uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",                <b>enableRTL:true</b>            });        });</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the UploadBox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**EnableRTL**(true)



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

      &lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" EnableRTL="true"&gt;&lt;/ej:UploadBox&gt;



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

The following screenshot displays the output.



{% include image.html url="\js\UploadBox\concepts-and-features\rtl-support-_images\rtl-support-_img1.png" Caption="Figure 3626: UploadBoxUploadbox with RTL"%}{% include image.html url="\js\UploadBox\concepts-and-features\rtl-support-_images\rtl-support-_img2.png" Caption="Figure 3626: UploadBoxUploadbox with RTL"%}

