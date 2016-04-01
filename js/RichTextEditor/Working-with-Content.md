---
layout: post
title: Working with content related operation in RichTextEditor widget for Syncfusion Essential JS
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

The editor’s [toolbar](/js/richtexteditor/user-interface#toolbar) contains buttons and dropdowns that allow you to editing and formatting in your content.

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

By default, the editor’s &lt; iframe &gt; is initialized with “Segoe UI” font name and 3(12pt) font size. To change it, select a different font name and font size from the drop-down in the editor’s toolbar. To apply different font style for particular section of the content, select the text that you would like to change, and select a required font style from the drop-down to apply the changes to the selected text.

### Set Default Font and Font Size

* Set a default font name and font size to the font name and size drop-down programmatically.

{% highlight html %}

<textarea id="texteditor"></textarea>
 
<script>
    $("#texteditor").ejRTE({
        value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images, it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        tools: {
            font: ["fontName", "fontSize", "fontColor", "backgroundColor"]
        },
         minWidth:"100px",
        isResponsive:true
    });

    var editor = $("#texteditor").ejRTE("instance");
    var ddl = editor._fontStyleDDL.ejDropDownList("instance");
    ddl.selectItemByIndex(7);
    var ddlSize = editor._fontSizeDDL.ejDropDownList("instance");
    ddlSize.selectItemByIndex(5);
</script>

{% endhighlight %}

* You can set default font for &lt; iframe &gt;’s body tag using [iframeAttributes](user-interface#iframe-attributes) property.

{% highlight html %}

<textarea id="texteditor"></textarea>
  
<script type="text/javascript">

    $(function () {

        $("#texteditor").ejRTE({
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            iframeAttributes: { style: "font-family:Arial;font-size:14px" }
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

### Adding Font Names and Font Size

If you want to add additional font names and font sizes to font drop-down, pass the font information as JSON data and bind it with instance of drop-down. 

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
        editor.defaults.fontSize.push({ text: "8 (42pt)", value: "8" });
		var ddl = editor._fontStyleDDL.ejDropDownList("instance");
		var ddlSize = editor._fontSizeDDL.ejDropDownList("instance");
        ddl.option({ "dataSource": editor.defaults.fontName });
		ddlSize.option({ "dataSource": editor.defaults.fontSize });
        ddl.selectItemByValue("CalibriLight");
		ddlSize.selectItemByValue("8");
    });

</script>

{% endhighlight %}

## Insert the content at cursor

If you want to insert/paste the content at the current cursor position (or) to replace the selected content with some formatting, you can use pasteContent method in the editor.

{% highlight javascript %}

    $(function () {
            $("#texteditor").ejRTE({
                value:"The RichTextEditor (RTE) control enables you to edit the contents with insert table and images,"+
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            });
        });
        function pasteContent() {
            var editor = $("#texteditor").ejRTE("instance");
            var selectedHtml = editor.getSelectedHtml();
            editor.pasteContent("<p style ='background-color:yellow;color:skyblue'>" + selectedHtml + "</p>");
        }
    
{% endhighlight %}


## Validation 

You can validate the RichTextEditor’s value on form submission by applying [validationRules](http://help.syncfusion.com/js/api/ejrte#members:validationrules) and [validationMessage](http://help.syncfusion.com/js/api/ejrte#members:validationmessage) to the RichTextEditor.

N> [jquery.validate.min](http://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js) script file should be referred for validation, for more details, refer [here](http://jqueryvalidation.org/documentation).

### jQuery Validation Methods

The following are jquery validation methods.

_List of jquery validation methods_

<table>
<tr>
<th>
Rules</th><th>
Description</th></tr>
<tr>
<td>
required</td><td>
 Requires value for the RichTextEditor control.</td></tr>
<tr>
<td>
minWordCount</td><td>
 Requires the value to be of given minimum words count.</td></tr>
<tr>
<td>
minlength</td><td>
 Requires the value to be of given minimum characters count.</td></tr>
<tr>
<td>
maxlength</td><td>
 Requires the value to be of given maximum characters count.</td></tr>
</table>

### Validation Rules

The validation rules help you to verify the content by adding validation attributes to the text area. This can be set by using [validationRules](http://help.syncfusion.com/js/api/ejrte#members:validationrules) property.


### Validation Messages 

You can set your own custom error message by using [validationMessage](http://help.syncfusion.com/js/api/ejrte#members:validationmessage) property. To display the error message, specify the corresponding annotation attribute followed by the message to display.


N> jQuery predefined error messages to that annotation attribute will be shown when this property is not defined. The below given example explain this behavior of ‘maxLength’ attribute,


When you initialize the RichTextEditor widget, it creates a text area hidden element which is used to store the value. Hence, the validation is performed based on the value stored in this hidden element.

Required field, minlength, maxlength, minWordCount and maxWordCount values validation is demonstrated in the below given example.


{% highlight html %}

    <form id="form1">
                    
		   <textarea id ="texteditor"></textarea>
		   <br/>
		   <button id="save">Validate</button>
		   
    </form>

{% endhighlight %}

{% highlight javascript %}

    <script type="text/javascript">
        $(function () {
			 $("#save").ejButton({
				size: "large",
				showRoundedCorner: true,
				type : "submit"
			});
            $("#texteditor").ejRTE({
				value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
						" it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                 allowEditing: true,
				 showFooter : true,
				 validationRules: {
						required: true,                
						minlength:15,
						maxlength: 150,
						minWordCount: 10,
						maxWordCount:50,
						
				 },
				 validationMessage: {
                    required: "Required RTE value",
                    minWordCount: "Minimum word count not reached.",
                    maxWordCount: "Maximum word count reached."
                }});
        });
    </script>
  
{% endhighlight %}

![](Working-with-Content_images/Validation.png)
