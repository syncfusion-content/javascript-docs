---
layout: post
title: asynchronous-upload
description: asynchronous upload
platform: js
control: Uploadbox
documentation: ug
---

# Asynchronous Upload

This feature allows you to upload and remove files **asynchronously**. To achieve this, set the **asyncUpload** property to ‘**true**’. The default value of **asyncUpload** property is ‘**true**’. The data type is **Boolean.**

The following steps guide you in uploading the file **asynchronously**.

*  In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>$(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                asyncUpload: true</b>            });         });</td></tr>
</table>


**[CSHTML]**

**// In the ASPX page, add the UploadBox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**AsyncUpload**(true)



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

    &lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" AsyncUpload="true" &gt;&lt;/ej:UploadBox&gt;



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

