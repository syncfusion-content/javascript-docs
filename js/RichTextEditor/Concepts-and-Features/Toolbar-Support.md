---
layout: post
title: Toolbar-Support
description: toolbar support
platform: js
control: RichTextEditor
documentation: ug
---

# Toolbar Support

The **RichTextEditor** control provides a number of tool items that provide a rich look to the text entered in the editing area. It brings to the Web popular editing features found in desktop word processors such as **Microsoft Word** and **OpenOffice.org Writer.**

## Text Formatting 

All the formatting tools allow you to change the appearance of text. Formatted text is visually interesting and easy for the visitor to read. Formatting tags provide emphasis or act as markers to help the visitor, find information. Some text styling options are also available as a drop-down list. Upon clicking them, the list opens and you can select a styling option.

### List of Toolbar Items

* Alignment Formatting Tools: Left, right, center, and justify.

* Color palette: 

* Fore-color: To change the color of text in editing area

* Back-color: To change the background color of editing area

* Bulleting: Ordered and un-ordered list

* Style: Bold, Italic, Underline, and Strikethrough

* Subscript and Superscript 

* Text with subscript and superscript placed after or before the baseline respectively.

* Font options

* [Font Name](http://docs.cksource.com/CKEditor_3.x/Users_Guide/Styling/Font) – Typeface that is applied to the document text.

* [Font Size](http://docs.cksource.com/CKEditor_3.x/Users_Guide/Styling/Size) – Determines how big or small the text will be.

* Format

* Predefined sets of formatting features that can be applied to block and to make elements of the document inline.

* Upper & lower case conversion

* Indent



### Undo and Redo

As the name explains, the **undo** function allows you to undo a number of recent actions in an editing area. To go along with **Undo** is **Redo**. Using this tool, you can avoid mistakes while editing.

### Clipboard action

Most used clipboard actions are cut, copy, and paste. These tools are used to rearrange the content within your editing area. You can copy and paste the images or text from locations other than the editing area.

* To render RichTextEditor with the above toolbar options, include the following code in your **HTML** page.



{% highlight html %}


    <div>
        <textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px">
        </textarea>
    </div>


{% endhighlight %}

* Add the following code in your script section.



{% highlight js %}

<script>
    $(function(){
            $("#rteSample").ejRTE({
                width: "850px",
                showFooter: true,
                **tools**: {
                    font: ["fontName", "fontSize", "fontColor", "backgrounColor"],
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





{% include image.html url="/js/RichTextEditor/Concepts-and-Features/Toolbar-Support_images/Toolbar-Support_img1.png" Caption="List of Toolbar items"%}

The following image consists of formatted content by using the available toolbar items in **RTE** control.



{% include image.html url="/js/RichTextEditor/Concepts-and-Features/Toolbar-Support_images/Toolbar-Support_img2.png" Caption="Formatted content"%}

