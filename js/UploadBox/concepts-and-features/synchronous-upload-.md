---
layout: post
title: synchronous-upload-
description: synchronous upload 
platform: js
control: Uploadbox
documentation: ug
---

# Synchronous Upload 

This features allow you to upload and remove the files **synchronously**. To achieve this, set the **asyncUpload** property to ‘**false**’. The data type is **Boolean.**

![http://help.syncfusion.com/ug/windows%20forms/pdf/ImagesExt/image517_36.jpg](synchronous-upload-_images\synchronous-upload-_img1.jpeg)_**Note: By default, UploadBoxUploadbox widget works with asynchronous upload option only**__._

The following steps guide you in uploading the file **synchronously**.

* In the **HTML** page, create a form with action and post method and then add the **&lt;div&gt;** element into the form to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;form id="upload" method="post" action="saveFiles.ashx"&gt;            &lt;div id="Uploadbox"&gt;&lt;/div&gt;            &lt;input type="submit" value="submit" /&gt;        &lt;/form&gt;     &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>    &lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({<b>                asyncUpload: false</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, create a form with action and post method and then add the UploadBox element.**



@using (Html.BeginForm("Save", "Uploadbox"))

{    

    @Html.EJ().Uploadbox("uploadbox").**AsyncUpload**(false)

    &lt;input type="submit" value="Submit" /&gt;

}



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

&lt;form id="upload" method="post" runat="server" action="saveFiles.ashx"&gt;

        &lt;div&gt;

            &lt;ej:UploadBox ID="Uploadbox" runat="server" AsyncUpload="false"&gt;&lt;/ej:UploadBox&gt;

        &lt;/div&gt;

        &lt;input type="submit" value="submit" /&gt;

    &lt;/form&gt;



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

Once the form is submitted by using **submit** button, it triggers the **saveFiles.ashx** handler. In the handler, save the files as usual.

For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

Once the form is submitted by using **submit** button, it triggers the **Save****ActionResult**.  In **ActionResult**, save the files as usual.

The following screenshot displays the output.



{% include image.html url="\js\UploadBox\concepts-and-features\synchronous-upload-_images\synchronous-upload-_img2.png" Caption="  Figure 125: UploadBoxUploadbox with synchronous option"%}

