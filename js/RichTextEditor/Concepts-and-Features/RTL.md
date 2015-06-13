---
layout: post
title: RTL
description: rtl
platform: js
control: RichTextEditor
documentation: ug
---

# RTL

**RTL** control supports right-to-left functionality and features for languages that work in a right-to-left way for entering, editing, and displaying text. You can change your display to read right-to-left. Arabic and Hebrew are written from right to left. The customers with writing style from right-to left can use this feature in **RTE**. You can achieve this in the editing area by using the **enableRTL** property. Setting this property to “**true**” allows you to write in the right-to-left format. Position of the toolbars also changes from right to left.

Add the following code to the script section in your **HTML** page to initialize the **RTE.**

{% highlight html %}

**[HTML]**

    <div class="rte">
        <textarea id="RTL"></textarea>
    </div>

{% endhighlight %}

{% highlight js %}

**[JavaScript]**

// Add the following code in your script section to render RTE with right-to-left format.
<script>
	$(function(){
        $("#RTL").ejRTE({
        width: "850px",
        enableRTL: true,
        tools: {
            font: ["fontSize", "fontColor", "backgroundColor"],
            style: ["bold", "italic", "underline", "strikethrough"],
            alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"],
            lists: ["unorderedList", "orderedList"],
            copyPaste: ["cut", "copy", "paste"],
            doAction: ["undo", "redo"],
            clear: ["clearFormat", "clearAll"],
            links: ["createLink"],
            images: ["image", "video"],
            tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"],
            scripts: ["superscript", "subscript"],
            casing: ["upperCase", "lowerCase"],
            paragraph: ["paragraph"]
            }
        });
	});
</script>
{% endhighlight %}


{% include image.html url="/js/RichTextEditor/Concepts-and-Features/RTL_images/RTL_img1.png" Caption="Show case for RTE with right to left appearance"%}

