---
layout: post
title: multiple-files-upload
description: multiple files upload
platform: js
control: Uploadbox
documentation: ug
---

# Multiple files upload

The **UploadBoxUploadbox** widget provides support to upload multiple files spontaneously. The **multipleFilesSelection** property enables you to select multiple files while browsing.  To achieve this, set the **multipleFilesSelection** property to ‘**true**’. The data type is **Boolean**.

![http://help.syncfusion.com/ug/windows%20forms/pdf/ImagesExt/image517_36.jpg](multiple-files-upload_images\multiple-files-upload_img1.jpeg)_**Note: The Multiple file selection supports all the latest versions of browser except Internet Explorer 9 and its previous versions.**_

The following steps explain the configuration of **multipleFilesSelection** property in **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="Uploadbox"&gt;&lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                multipleFilesSelection: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the UploadBox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**MultipleFilesSelection**(true)



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

  &lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" MultipleFilesSelection="true" &gt;&lt;/ej:UploadBox&gt;



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

The following screenshot displays the output.



{% include image.html url="\js\UploadBox\concepts-and-features\multiple-files-upload_images\multiple-files-upload_img2.png" Caption="Figure 126: Enables multiple selections"%}



{% include image.html url="\js\UploadBox\concepts-and-features\multiple-files-upload_images\multiple-files-upload_img3.png" Caption=" Figure 127: UploadBoxUploadbox with multiple files       "%}

