---
layout: post
title: rtl
description: rtl
platform: js
control: RichTextEditor
documentation: ug
---

# RTL

**RTL** control supports right-to-left functionality and features for languages that work in a right-to-left way for entering, editing, and displaying text. You can change your display to read right-to-left. Arabic and Hebrew are written from right to left. The customers with writing style from right-to left can use this feature in **RTE**. You can achieve this in the editing area by using the **enableRTL** property. Setting this property to “**tTrue**” allows you to write in the right-to-left format. Position of the toolbars also changes from right to left.

* Add the following code to the script section in your **HTML** page to initialize the **RTE.**



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div class="rte"&gt;        &lt;textarea id="RTL"&gt;&lt;/textarea&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\ Add the following code in your script section to render RTE with right-to-left format.    $("#RTL").ejRTE({        width: "850px",<b>        enableRTL: true,</b>        tools: {            font: ["fontSize", "fontColor", "backgroundColor"],            style: ["bold", "italic", "underline", "strikethrough"],            alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"],            lists: ["unorderedList", "orderedList"],            copyPaste: ["cut", "copy", "paste"],            doAction: ["undo", "redo"],            clear: ["clearFormat", "clearAll"],            links: ["createLink"],            images: ["image", "video"],            tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"],            scripts: ["superscript", "subscript"],            casing: ["upperCase", "lowerCase"],            paragraph: ["paragraph"]        }    });</td></tr>
</table>


**[_cshtml]**

\\ Add the following code in your view page to render the RTE.

@{Html.EJ().RTE("rteSample").Width("850px").ContentTemplate(@&lt;p&gt;&lt;/p&gt;).**EnableRTL(true)**.Render(); }





**[_aspx]**

\\ Add the following code in your aspx page to render the RTE.

&lt;ej:RTE ID="rteSample" Width="850" enableRTL="true" runat="server"&gt;&lt;/ej:RTE&gt;





![](rtl_images\rtl_img1.png)

_Figure_ _29__41__: Show case for RTE with right to left appearance_

