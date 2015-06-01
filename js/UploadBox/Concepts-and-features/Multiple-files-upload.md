---
layout: post
title: Multiple-files-upload
description: multiple files upload
platform: js
control: Uploadbox
documentation: ug
---

# Multiple files upload

The **Uploadbox** widget provides support to upload multiple files spontaneously. The **multipleFilesSelection** property enables you to select multiple files while browsing.  To achieve this, set the **multipleFilesSelection** property to ‘**true**’. The data type is **Boolean**.

> _**Note: The Multiple file selection supports all the latest versions of browser except Internet Explorer 9 and its previous versions.**_



The following steps explain the configuration of **multipleFilesSelection** property in **Uploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="Uploadbox"&gt;&lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                multipleFilesSelection: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

The following screenshot displays the output.



{% include image.html url="/js/UploadBox/Concepts-and-features/Multiple-files-upload_images/Multiple-files-upload_img1.png" Caption="Enables multiple selections"%}



{% include image.html url="/js/UploadBox/Concepts-and-features/Multiple-files-upload_images/Multiple-files-upload_img2.png" Caption="Uploadbox with multiple files       "%}

