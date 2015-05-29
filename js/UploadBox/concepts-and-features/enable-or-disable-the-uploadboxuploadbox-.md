---
layout: post
title: enable-or-disable-the-uploadboxuploadbox-
description: enable or disable the uploadboxuploadbox 
platform: js
control: Uploadbox
documentation: ug
---

# Enable or Disable the UploadBoxUploadbox 

This features helps to set the **enable** or **disable** option for **UploadBoxUploadbox** by setting **Boolean** type value to **enabled** property. For **enable** or **disable** option, set **enabled** property to ‘**false**’. The data type is **Boolean**.

The following steps explain the configuration of **enabled** property in **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>  <b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",                enabled :false            });         });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the UploadBox element.**



@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**Enabled(false)**



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**



&lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" Enabled="false" &gt;&lt;/ej:UploadBox&gt;



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

* The following screenshot displays the output.

{% include image.html url="\js\UploadBox\concepts-and-features\enable-or-disable-the-uploadboxuploadbox-_images\enable-or-disable-the-uploadboxuploadbox-_img1.png" Caption="Figure 124: UploadBoxUploadbox with enabled property"%}

