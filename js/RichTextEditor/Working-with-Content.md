---
layout: post
title: Content related in RichTextEditor widget for Syncfusion Essential JS
description: Working with Content related changes in RichTextEditor widget
platform: js
control: RTE
documentation: ug

---
# Working with Content

## Submit Content

The editor allows you to process its content before it is being submitted to the server on form submit event. You can use this option to validate content on the client side to prevent invalid data from being submitted to the server.

This example shows how to encode the HTML content before form submit event.

{% highlight html %}

<form>
<textarea id ="texteditor"></textarea>
<button type ="submit">Submit</button>
</form>

<script type ="text/javascript">

        $(function () {
        $("#texteditor").ejRTE({
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        });
    });

    $("form").on("submit", function () {

        var editor = $("#texteditor").data("ejRTE");
        var encoded = $('<div />').text(editor.model.value).html();
        $("#texteditor").val(encoded);

    });
        </script>

{% endhighlight %}

## Refresh

When you move the editor’s wrapper element into another DOM element, the editor needs to be reinitialized by the [refresh](http://help.syncfusion.com/js/api/ejrte#methods:refresh) method to retain its content. The method reload the content area and rebind the events of the editor. 

{% highlight html %}

 <textarea id="texteditor"></textarea>

<div id="target"></div>
<button onclick="appendTo()">Append To</button>
<button onclick="refresh()">Refresh</button>
<script type="text/javascript">
        var editor = null;
        $(function () {
            $("#texteditor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            });
            editor = $("#texteditor").ejRTE("instance");
        });
        function appendTo() {
            editor._rteWapper.appendTo($("#target"))
        }
        function refresh() {
            editor.refresh()
        }
    </script>

{% endhighlight %}

## Editing and Formatting 

The editor’s [toolbar](#_Toolbar) contains buttons and dropdowns that allow you to editing and formatting in your content.

* Font name, font size, and color
* Bold, italic, underline, and strikethrough
* Text Alignment – left, right, center, and justify
* Indent – left and right
* styles – quotation, normal,  headings, and sub-headings
* superscript and subscript
* casing – convert to lower case and upper case
* list – create ordered and unordered list

{% highlight html %}

<textarea id ="texteditor"></textarea>

<script type ="text/javascript">
           $(function () {
        $("#texteditor").ejRTE({
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            toolsList: ["formatStyle", "font", "style", "effects", "alignment", "lists", "indenting", "clipboard", "doAction", "casing"],
            tools: {
                font: ["fontName", "fontSize", "fontColor", "backgroundColor"],
                style: ["bold", "italic", "underline", "strikethrough"],
                alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"],
                indenting: ["outdent", "indent"],
                formatStyle: ["format"],
                effects: ["superscript", "subscript"],
                casing: ["upperCase", "lowerCase"],
                lists: ["unorderedList", "orderedList"],
                clipboard: ["cut", "copy", "paste"],
                doAction: ["undo", "redo"]
            }
        });
    });
    </script>

{% endhighlight %}

## Undo and Redo 

Undo and Redo buttons allow you to editing the text by disregard/cancel the recently made changes and restore it to previous state. It is a useful tool to restore the performed action which got changed by mistake. Up to 50 actions can be undo/redo in the editor by default. 

To undo and redo operations, do one of the following:

* Press the undo/redo button on the toolbar
* Press the **Ctrl** **+** **Z**/**Ctrl** **+** **Y** combination on the keyboard


{% highlight html %}

<textarea id ="texteditor"></textarea>

<script type ="text/javascript">
$(function () {
        $("#texteditor").ejRTE({
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            toolsList: ["doAction"],
            tools: {
                doAction: ["undo", "redo"]
            }
        });
    });
</script>

{% endhighlight %}

## Clipboard Operations

The editor provides support for the clipboard operations (cut, copy, and paste) in all text and images using the toolbar buttons and the keyboard shortcuts. Toolbar includes buttons through which the clipboard operations, such as Cut, Copy, and Paste can be accessed.

You can use the keyboard shortcuts to perform the clipboard operations.

* Cut - CTRL+X
* Copy - CTRL+C
* Paste - CTRL+V

N> Some browsers block the clipboard access from JavaScript. If you want to use the Cut, Copy, and Paste buttons on the toolbar, you need to allow JavaScript to use the clipboard. If you don’t want to do this configuration, use CTRL+C, CTRL+X, and CTRL+V keyboard commands.

{% highlight html %}

<textarea id="texteditor"></textarea>

<script type="text/javascript">

       $(function () {

            $("#texteditor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                toolsList: ["clipboard"],
                tools: {
                    clipboard: ["cut", "copy", "paste"]
                }
            });

        });
</script>

{% endhighlight %}

## Persistence

The editor is capable to persist its content with HTML format. By default, the persistence support is disabled in the editor. When you set the [enablePersistence](http://help.syncfusion.com/js/api/ejrte#members:enablepersistence) property to true, the persistence will be enabled in the editor.

N>  [localstorage](http://www.w3schools.com/html/html5_webstorage.asp#) is not supported below ie9 version, therefore persistence support is fallback to [cookie](http://www.w3schools.com/js/js_cookies.asp#).

{% highlight html %}

$(function () {
$("#texteditor").ejRTE({
enablePersistence: true
});

});
{% endhighlight %}

## Change the Font

By default, the editor’s &lt; iframe &gt; is initialized with “Segoe UI” font. To change it, select a different font from the drop-down in the editor’s toolbar. To apply different font for particular section of the content, select the text that you would like to change, and select a required font from the drop-down to apply the changes to the selected text.

### Set Default Font

* Set a default font to the font drop-down programmatically.

{% highlight html %}

 <textarea id ="texteditor"></textarea>

<script type ="text/javascript">
      $(function () {
        $("#texteditor").ejRTE({
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images, it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            tools: {
                font: ["fontName", "fontSize", "fontColor", "backgroundColor"]
            }
        });

        var editor = $("#texteditor").ejRTE("instance");
        var ddl = editor._fontStyleDDL.ejDropDownList("instance");
        ddl.selectItemByIndex(7);
    });
</script>
{% endhighlight %}

* You can set default font for &lt; iframe &gt;’s body tag using **[iframeAttributes](#_Iframe_Attributes)** property.

{% highlight html %}

   <textarea id="texteditor"></textarea>

   <script type="text/javascript">

        $(function () {

            $("#texteditor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                iframeAttributes:{ style:"font-family:Arial;"}
            });

        });
    </script>
{% endhighlight %}

* If you want to override the default font from CSS, create a style tag with CSS styles and append it to the &lt; iframe &gt;’s head tag of the editor.

{% highlight html %}

<textarea id="texteditor"></textarea>

<script type="text/javascript">

        $(function () {

            $("#texteditor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            });

            var css = "html,body{font-family:sans-serif;font-size:14px; }";
            var editorDoc = $("#texteditor").ejRTE("instance").getDocument();
            var styleTag = document.createElement("style");
            styleTag.type = "text/css";
            if (styleTag.styleSheet) {
                styleTag.styleSheet.cssText = css;
            } else {
                styleTag.appendChild(document.createTextNode(css));
            }
            editorDoc.head.appendChild(styleTag);

        });

</script>
{% endhighlight %}

### Adding Fonts

If you want to add additional fonts to font drop-down, pass the font information as JSON data and bind it with instance of drop-down. 

{% highlight html %}

<textarea id="texteditor"></textarea>

<script type="text/javascript">
        $(function () {
            $("#texteditor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images, it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                tools: {
                    font: ["fontName", "fontSize", "fontColor", "backgroundColor"]
                }
            });

            var editor = $("#texteditor").ejRTE("instance");
            editor.defaults.fontName.push({ text: "Calibri Light", value: "CalibriLight" }, { text: "Calibri", value: "Calibri" });
            var ddl = editor._fontStyleDDL.ejDropDownList("instance");
            ddl.option({ "dataSource": editor.defaults.fontName });
            ddl.selectItemByValue("CalibriLight");
        });

</script>
{% endhighlight %}



## Insert the content at cursor

If you want to insert/paste the content at the current cursor position (or) to replace the selected content with some formatting, you can use pasteContent method in the editor.

{% highlight js %}
$(function () {
        $("#texteditor").ejRTE({
            value:"The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        });
    });
    function pasteContent() {
        var editor = $("#texteditor").ejRTE("instance");
        var selectedHtml = editor.getSelectedHtml();
        editor.pasteContent("<p style ='background-color:yellow;color:skyblue'>" + selectedHtml + "</p>");
    }
{% endhighlight %}

