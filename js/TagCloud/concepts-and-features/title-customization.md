---
layout: post
title: title-customization
description: title customization
platform: js
control: TagCloud
documentation: ug
---

# Title Customization

## Show title

The **TagCloud** items are displayed with a Title element by default. To hide the title, you can use **showTitle** property that is true by default.

### How to disable title in TagCloud

The following steps explains you on how to configure **title** for a **TagCloud**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;div id="techweblist"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Disable the Title element of TagCloud control as follows.    $("#techweblist").ejTagCloud({                <b>showTitle:false, </b><b>                dataSource: websiteCollection</b>            });</td></tr>
</table>


**[CSHTML]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



@Html.EJ().TagCloud("tagcloud").Datasource((IEnumerable<WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("Text").Url("Url").Frequency("Frequency")).**ShowTitle(false)**



**[ASPX]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



&lt;ej:TagCloud ID="tagcloud" runat="server" DataTextField="text" DataUrlField="url" DataFrequencyField="frequency" ShowTitle="false"&gt;

    &lt;/ej:TagCloud&gt;



The following screenshot illustrates a **TagCloud** control when you disable title,

![](title-customization_images\title-customization_img1.png)

_Figure______7__12__: TagCloud without Title_

## Title text

**TagCloud** widget allows you to set a custom title text by using the **titleText** property. By default titleText property is set to string value “Title”.

### Defining title text for TagCloud

The following steps explains you on how to configure **titleText** for a **TagCloud**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;div id="techweblist"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Disable the Title element of TagCloud control as follows:    $("#techweblist").ejTagCloud({<b>                </b>showTitle:true, <b>                titleText: "Tech Sites",</b><b>                </b>dataSource: websiteCollection            });</td></tr>
</table>


**[CSHTML]** 

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



@Html.EJ().TagCloud("tagcloud").Datasource((IEnumerable<WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("Text").Url("Url").Frequency("Frequency")).**Title("Tech sites")**



**[ASPX]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



&lt;ej:TagCloud ID="tagcloud" runat="server" DataTextField="text" DataUrlField="url" DataFrequencyField="frequency" Title="Sites"&gt;

    &lt;/ej:TagCloud&gt;



The following screenshot illustrates the **TagCloud** control with customized title text.

![](title-customization_images\title-customization_img2.png)

_Figure_ _8__13__: TagCloud with custom Title text_

## Title image

**TagCloud** widget provides **titleImage** to set an image for the title. You can set the desired image **URL** to **titleImage** property.

### Defining title text for TagCloud

The following steps explains you to configure **titleImage** for a **TagCloud**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;div id="techweblist"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Assign the image URL from local location or remote location to titleImage property of TagCloud control as follows.$("#techweblist").ejTagCloud({<b>  titleImage: "http://js.syncfusion.com/demos/web/images/waitingpopup/js_logo.png",</b>  titleText: "Tech Sites",<b>  </b>dataSource: websiteCollection });</td></tr>
</table>


**[CSHTML]**    

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;

****

@Html.EJ().TagCloud("tagcloud").Datasource((IEnumerable<WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("Text").Url("Url").Frequency("Frequency")).Title("Tech sites").**TitleImage("http://js.syncfusion.com/demos/web/images/waitingpopup/js_logo.png")**



**[ASPX]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



&lt;ej:TagCloud ID="tagcloud" runat="server" DataTextField="text" DataUrlField="url" DataFrequencyField="frequency" TitleImage="http://js.syncfusion.com/demos/web/images/waitingpopup/js_logo.png"&gt;

    &lt;/ej:TagCloud&gt;



Using CSS class you can resize the image content as follows.



{% highlight css %}

**[Style]**
style type="text/css">
**.e-title-img** {
            height::35px;
            width:35px;
        }
    </style>


{% endhighlight %}



The following screenshot illustrates the **TagCloud** control with customized title image.

![](title-customization_images\title-customization_img3.png)

_Figure_ _9__14__: TagCloud with a Title image_

