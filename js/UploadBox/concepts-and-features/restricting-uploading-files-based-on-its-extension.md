---
layout: post
title: restricting-uploading-files-based-on-its-extension
description: restricting uploading files based on its extension
platform: js
control: Uploadbox
documentation: ug
---

# Restricting uploading files based on its extension

## Allow Extension

Files are filtered before they are uploaded. You can select the files to be filtered by using **browse** button. The **extensionsAllow** property allows upload of the selected extensions only. You can give multiple extensions by using comma (,).  The data type is **string**.

![http://help.syncfusion.com/ug/windows%20forms/pdf/ImagesExt/image517_36.jpg](restricting-uploading-files-based-on-its-extension_images\restricting-uploading-files-based-on-its-extension_img1.jpeg)_**Note: Prepend dot (.) symbol with extension like “.pdf”.**_



The following steps explain the configuration of **extensionsAllow** property in **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>  <b>// Initialize the control in JavaScript.</b>  $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                extensionsAllow: ".docx, .pdf"</b>            });         });</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add UploadBox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**ExtensionsAllow**(".docx,.pdf")



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

    &lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx"  ExtensionsAllow=".docx,.pdf" &gt;&lt;/ej:UploadBox&gt;



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

## Deny Extension

Files are filtered before they are uploaded. You can select the files to be filtered by using **browse** button. The **extensionsDeny** property denies upload of the selected extensions. You can give multiple extensions by using comma (,).  The data type is **string**.

![http://help.syncfusion.com/ug/windows%20forms/pdf/ImagesExt/image517_36.jpg](restricting-uploading-files-based-on-its-extension_images\restricting-uploading-files-based-on-its-extension_img2.jpeg)_**Note: Prepend dot (.) symbol with extension like “.pdf”.**_



The following steps explain the configuration of **extensionsDeny** property in **UploadBoxUploadbox**

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b><b> // Initialize the control in JavaScript.</b>  $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                extensionsDeny: ".docx, .pdf"</b>            });         });</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add UploadBox ox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**ExtensionsDeny**(".docx,.pdf")



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

&lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" ExtensionsDeny=".docx,.pdf" &gt;&lt;/ej:UploadBox&gt;



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

