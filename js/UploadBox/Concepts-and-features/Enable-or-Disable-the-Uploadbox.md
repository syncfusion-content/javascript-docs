---
layout: post
title: Enable-or-Disable-the-Uploadbox
description: enable or disable the uploadbox 
platform: js
control: Uploadbox
documentation: ug
---

# Enable or Disable the Uploadbox 

This features helps to set the **enable** or **disable** option for **Uploadbox** by setting **Boolean** type value to **enabled** property. For **enable** or **disable** option, set **enabled** property to ‘**false**’. The data type is **Boolean**.

The following steps explain the configuration of **enabled** property in **Uploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>  <b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",                enabled :false            });         });    &lt;/script&gt;</td></tr>
</table>


* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

* The following screenshot displays the output.



{% include image.html url="/js/UploadBox/Concepts-and-features/Enable-or-Disable-the-Uploadbox_images/Enable-or-Disable-the-Uploadbox_img1.png" Caption="Uploadbox with enabled property"%}

