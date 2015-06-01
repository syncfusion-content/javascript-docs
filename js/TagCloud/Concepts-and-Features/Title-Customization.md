---
layout: post
title: Title-Customization
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


The following screenshot illustrates a **TagCloud** control when you disable title,

{% include image.html url="/js/TagCloud/Concepts-and-Features/Title-Customization_images/Title-Customization_img1.png" Caption=""%}

_Figure 7: TagCloud without Title_

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


The following screenshot illustrates the **TagCloud** control with customized title text.

{% include image.html url="/js/TagCloud/Concepts-and-Features/Title-Customization_images/Title-Customization_img2.png" Caption=""%}

_Figure_ _8__: TagCloud with custom Title text_

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

{% include image.html url="/js/TagCloud/Concepts-and-Features/Title-Customization_images/Title-Customization_img3.png" Caption=""%}

_Figure_ _9__: TagCloud with a Title image_

