---
layout: post
title: appearance-and-styling
description: appearance and styling
platform: js
control: TagCloud
documentation: ug
---

# Appearance and Styling

## Minimum and maximum Font size

The **TagCloud** content are set to different font sizes from minimum to maximum based on its frequency values. By default, **minFontSize** is “10px” and **maxFontSize** is “40px”, using these properties you can customize the minimum and maximum font sizes.

### Customizing font sizes of TagCloud

The following steps explains you on how to configure font sizes for a **TagCloud**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;div id="techweblist"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Assign the values for minFontSize  and maxFontSize properties as follows.</b>    $("#techweblist").ejTagCloud({<b>                minFontSize: "20px",</b><b>                maxFontSize: "50px",</b>                titleText: "Tech Sites",<b>                </b>dataSource: websiteCollection           });</td></tr>
</table>


**[CSHTML]**   

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;

****

@Html.EJ().TagCloud("tagcloud").Datasource((IEnumerable<MvcApplication2.WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("Text").Url("Url").Frequency("Frequency")).Title("Tech sites")**.MinFontSize("20px").MaxFontSize("50px")**



**[ASPX]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



&lt;ej:TagCloud ID="tagcloud" runat="server" DataTextField="text" DataUrlField="url" DataFrequencyField="frequency" MaxFontSize="20 " MinFontSize="40"&gt;**&lt;/ej:TagCloud&gt;**



The following screenshot illustrates the **TagCloud** control with customized font sizes.

![](appearance-and-styling_images\appearance-and-styling_img1.png)

_Figure_ _1__5__0__: TagCloud with customized font sizes_

## Tag format

You can set the **TagCloud** content display format using **format** property. By default format is set to cloud, that displays content in **TagCloud**. You can set the format as list to display the content in linear format.

### Defining Cloud and List format

The following steps explains you to configure format for a **TagCloud**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.



<table>
<tr>
<td>
<b>[HTML]</b> &lt;table&gt;    &lt;tr&gt;        &lt;td&gt;            <span>Tag format cloud</span>            &lt;div id="techwebcloud"&gt;&lt;/div&gt;        &lt;/td&gt;        &lt;td&gt;            <span>Tag format list</span>            &lt;div id="techweblist"&gt;&lt;/div&gt;        &lt;/td&gt;    &lt;/tr&gt;&lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Assign the values for format property in TagCloud.      $("#techweblist").ejTagCloud({                <b>format:"list",</b>                titleText: "Tech Sites List",                dataSource: websiteCollection            });            $("#techwebcloud").ejTagCloud({                <b>format: "cloud",</b>                titleText: "Tech Sites Cloud",                dataSource: websiteCollection            });</td></tr>
</table>


**[CSHTML]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



@Html.EJ().TagCloud("tagcloudformat").Datasource((IEnumerable<WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("Text").Url("Url").Frequency("Frequency")).Title("Tech sites").**Format(Formats.Cloud)**

 @Html.EJ().TagCloud("tagCloudlist").Datasource((IEnumerable<WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("Text").Url("Url").Frequency("Frequency")).Title("Tech sites").**Format(Formats.List)**



**[ASPX]**



&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



&lt;ej:TagCloud ID="tagcloud" runat="server" DataTextField="text" DataUrlField="url" DataFrequencyField="frequency" Format="Cloud"&gt;&lt;/ej:TagCloud&gt;



&lt;ej:TagCloud ID="tagcloud" runat="server" DataTextField="text" DataUrlField="url" DataFrequencyField="frequency" Format="List"&gt;&lt;/ej:TagCloud&gt;



The following screenshot illustrates the **TagCloud** control with customized formats.

![](appearance-and-styling_images\appearance-and-styling_img2.png)

_Figure_ _16__11__: TagCloud using cloud and list formats_

## Theme

You can control the style and appearance of **TagCloud** based on CSS classes. To apply styles to the **TagCloud** control, you can refer two files, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer **ej.widgets.all.min.css** file, it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **TagCloud** control namely,

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

## Css Class

You can use the CSS class to customize the **TagCloud** appearance. Any of the CSS properties can be used to modify look and feel of tag cloud based on the requirement. Define a **CSS** class as per requirement and assign the class name to **cssClass** property.

### Configure TagCloud using CSS class

The following steps allows you to configure **CSS** class for **TagCloud**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;div id="techweblist"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the cssClass property to TagCloud.          $("#techweblist").ejTagCloud({                titleText: "Tech Sites",                dataSource: websiteCollection,                <b>cssClass:"CustomCss"</b>            });</td></tr>
</table>


**[CSHTML]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



@Html.EJ().TagCloud("tagcloud").Datasource((IEnumerable<WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("Text").Url("Url").Frequency("Frequency")).Title("Tech sites").CssClass("CustomCss")



**[ASPX]**

&lt;%-- Configure datasource referring local data binding section and assign it to datasource property -- %&gt;



&lt;ej:TagCloud ID="tagcloud" runat="server" DataTextField="text" DataUrlField="url" DataFrequencyField="frequency" CssClass="custom"&gt;**&lt;/ej:TagCloud&gt;**



Define CSS class for customizing the **TagCloud** widget.



{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
        /* Customize the TagCloud div element */
        .CustomCss
        {
            background-color: #DDC;
            width: 400px;
        }
        /* Customize the TagCloud header element */        
        .CustomCss .e-header.e-title {
            text-align: center;
            font-weight: bold;
        }
    </style>


{% endhighlight %}



The following screenshot illustrates the **TagCloud** with customized CSS class,

![](appearance-and-styling_images\appearance-and-styling_img3.png)

_Figure_ _1__7__2__: TagCloud with Custom CSS_

