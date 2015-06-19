---
layout: post
title: RTL-Support
description: rtl support 
platform: js
control: Uploadbox
documentation: ug
---

# RTL Support 

This feature supports the change of left-to-right alignment of the **Uploadbox** widget to right-to-left (**RTL**). That is, it sets the **Uploadbox** to right-to-left actions.

The following steps explain the configuration of **enableRTL** property in **Uploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="Uploadbox"&gt;&lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b> <b>// Initialize the control in JavaScript.</b>$(function () {//Declaration.            $("#uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",                <b>enableRTL:true</b>            });        });</td></tr>
</table>


* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

The following screenshot displays the output.



{% include image.html url="/js/UploadBox/Concepts-and-features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 26: Uploadbox with RTL"%}

