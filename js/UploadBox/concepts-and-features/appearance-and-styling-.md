---
layout: post
title: appearance-and-styling-
description: appearance and styling 
platform: js
control: Uploadbox
documentation: ug
---

# Appearance and styling 

The **UploadBoxUploadbox** widget provides support to customize the **dialog box** text and **button** text. 

## Customizing Button Text

The following table contains the **subproperties** available under **buttonText** property. To customize the text, pass the alternate text with corresponding **subproperties**. 

_Table_ _3__: Sub__-__properties under buttonText property_

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Description</b></td><td>
<b>Data Type</b></td></tr>
<tr>
<td>
browse</td><td>
Sets the alternative text for browse button. </td><td>
String</td></tr>
<tr>
<td>
upload</td><td>
Sets the alternative text for upload button. </td><td>
String</td></tr>
<tr>
<td>
cancel</td><td>
Sets the alternative text for cancel button. </td><td>
String</td></tr>
</table>


The following steps explain the configuration of **buttonText** property in **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="Uploadbox"&gt;&lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b> <b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                buttonText:{ browse:"Choose File", upload:"Upload File", cancel:"Cancel Upload"}</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the UploadBox element.**



@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**UploadBoxButtonText**(text=>text.Browse("Choose Files").Cancel("Cancel upload").Upload("Upload file"))



<table>
<tr>
<td>
<b>[ASPX]</b><b>\\ In the ASPX page, add the uploadbox element.</b>    &lt;ej:UploadBox ID="Uploadbox" runat="server"  SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx"&gt;&lt;/ej:UploadBox&gt;</td></tr>
<tr>
<td>
<b>[C#]  </b><b>\\ In CS, initialize the property.</b>protected void Page_Load(object sender, EventArgs e){<b>Uploadbox.UploadBoxButtonText</b> = new Syncfusion.JavaScript.Models.UploadboxButtonText() {Browse="Choose File", Upload="Upload File", Cancel="Cancel Upload" };}</td></tr>
</table>


* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

The following screenshot displays the output.



{% include image.html url="\js\UploadBox\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img1.png" Caption="Figure 233: UploadBoxUploadbox with customized button text"%}

## Customizing Upload Dialog

The following table contains the **subproperties** available under **UploadBoxUploadbox’s DialogText** property. To customize the text, pass the alternate text with corresponding **subproperties**. 

_Table_ _4__: Sub__properties under dialogText property_

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
title</td><td>
Sets the alternative text for Title of <b>UploadBoxUploadbox</b> dialog. </td></tr>
<tr>
<td>
name</td><td>
Sets the alternative text for Name column.  </td></tr>
<tr>
<td>
size</td><td>
Sets the alternative text for Size column. </td></tr>
<tr>
<td>
status</td><td>
Sets the alternative text for status column.</td></tr>
</table>


The following steps explain the configuration of **dialogText** property in **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="Uploadbox"&gt;&lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b> <b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                dialogText: { title: "Upload File List", name: "File Name", size: "File Size", status: "File Status" }</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the UploadBox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**UploadBoxDialogText**(text=>text.Title("Upload File List").Name("File Name").Size("File Size").Status("File Status"))



<table>
<tr>
<td>
<b>[ASPX]</b><b>\\ In the ASPX page, add the uploadbox element.</b>    &lt;ej:UploadBox ID="Uploadbox" runat="server"  SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx"&gt;&lt;/ej:UploadBox&gt;</td></tr>
<tr>
<td>
<b>[C#]  </b><b>\\ In CS, we need to initialize the property.</b>protected void Page_Load(object sender, EventArgs e){ <b>Uploadbox.UploadBoxDialogText</b> = new Syncfusion.JavaScript.Models.UploadboxDialogText() { Title="Upload File List", Name= "File Name", Size="File Size", Status= "File Status" };}</td></tr>
</table>


* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively. 

The following screenshot displays the output.



{% include image.html url="\js\UploadBox\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img2.png" Caption="Figure 234: UploadBoxUploadbox with customized dialog text"%}

## Show or Hide File details 

You have an option to **show** or **hide****file****details** in the **uploaded file list****dialog**. By using this property, the **uploaded file dialog** does not display the file details once selected. To enable this, set **showFileDetails** to ‘**false**’. By default, its value is set to ‘**true**’. The data type is **Boolean**.

The following steps explains the configuration of **showFileDetails** property in **UploadBoxUploadbox**.

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="Uploadbox"&gt;&lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>  // Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                showFileDetails:false</b>        });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the UploadBox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**ShowFileDetails**(false)



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

&lt;ej:UploadBox ID="Uploadbox" runat="server" ShowFileDetails="true"  SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" &gt;&lt;/ej:UploadBox&gt;



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

## Theme

**UploadBoxUploadbox** control’s style and appearance are controlled based on **CSS** classes. In order to apply styles to the **UploadBoxUploadbox** control, you can refer to two files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these both files. 

By default, there are 12-theme support available for **UploadBoxUploadbox** control namely,

* Default-theme

* Flat-azure-dark

* Fat-lime

* Flat-lime-dark

* Flat-saffron

* Flat-saffron-dark

* Gradient-azure

* Gradient-azure-dark

* Gradient-lime

* Gradient-lime-dark

* Gradient-saffron

* Gradient-saffron-dark

## Custom CSS

**CSS****class** customizes the **UploadBoxUploadbox** control’s appearance. Define a **CSS****class** as per the requirement and assign the class name to **cssClass** property. The data type is **string**. 

The following steps explain the configuration of **cssClass** property in **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="Uploadbox"&gt;&lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>$(function () {//Declaration.            $("#uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",                cssClass: "customcss"            });        });</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the UploadBox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").**CssClass**("customcss")



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

&lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" CssClass="customcss"&gt;&lt;/ej:UploadBox&gt;



* In **CSS**, configure Custom Styles for the **UploadBoxUploadbox**.

{% highlight css %}

**[CSS]**
  <style class="cssStyles">
      .customcss.e-uploadbox.e-widget .e-selectpart.e-select .e-select{
            background-color: #FFFFCC;
            font-weight: bold; 
            font-family: sans-serif;
        }
    </style>


{% endhighlight %}



* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

* For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

The following screenshot displays the output.



{% include image.html url="\js\UploadBox\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img3.png" Caption="Figure 235: UploadBoxUploadbox with customized CSS"%}

