---
layout: post
title: Insert-Hyperlink
description: insert hyperlink
platform: js
control: RichTextEditor
documentation: ug
---

# Insert Hyperlink

**RTE** control provides the option to insert hyperlink in the editing area. Consider your blog needs to give a product’s download link, then you can include the download link using “**insert or edit hyperlink**” tool item. 

By clicking this tool item, you can add **Text**, with hyperlink, and **Tooltip**, where a message appears when a cursor is positioned over a hyperlink. 

Also, this tool item enables you to add or edit the hyperlink, text, tooltip for selected text in the editing area. The following screenshot illustrates the hyperlink of the “**Click here**” text.

* Add the following code in your **HTML** page to initialize the **RTE**.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div class="rte"&gt;<b>        &lt;textarea id="rteSample"&gt;&lt;/textarea&gt;</b>    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>\\</b> Add the following code in your script section to render <b>RTE</b> with default set of tools.    $("#rteSample").ejRTE();</td></tr>
</table>


{% include image.html url="/js/RichTextEditor/Concepts-and-Features/Insert-Hyperlink_images/Insert-Hyperlink_img1.png" Caption=""%}

_Figure_ _22__: Show case for inserting hyperlink in RTE content area_

