---
layout: post
title: Working with content related operation in RichTextEditor widget for Syncfusion Essential JS
description: Working with Content related changes in RichTextEditor widget
platform: js
control: RTE
documentation: ug
keywords: RichTextEditor, IFrame Attributes, Editing and Formatting 
api: /api/js/ejrte
---
# Working with Content

The editor creates the iframe element as the content area on control initialization, it is used to display and editing the content. In Content Area, the editor displays only the body tag of a &lt; iframe &gt; document. To set or modify details in the &lt; head &gt; tag, use [Source view](#footer#source-view) of the editor.

## Iframe Attributes

The editor allows you to passing an additional attributes to body tag of a &lt; iframe &gt; element using [iframeAttributes](https://help.syncfusion.com/api/js/ejrte#members:iframeattributes) property. The property contains name/value pairs in string format, it is used to override the default appearance of the content area. 

N> the content area’s font, color, margins, and background can be overridden using iframeAttributes property. You can specifies the editable behavior (content editable) of the content also in this property.

{% highlight html %}

<textarea id="editor"></textarea>
 
<script type="text/javascript">
    $(function () {
        $("#editor").ejRTE({
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            iframeAttributes:{style: "background-color:#e0ffff;color:#6495ed;"}
        });
    });
</script>

{% endhighlight %}

N> Background image for the RTE control : {{'[Link](http://jsplayground.syncfusion.com/Sync_cpaoqshs)'| markdownify }} <BR>
Set default font for the Iframe : {{'[Link](http://jsplayground.syncfusion.com/Sync_k2uwsibi)'| markdownify }}


## Adding External CSS File

The editor offers you to add external CSS file to style the &lt; iframe &gt; element.  Easily change the appearance of editor’s content using an external CSS file. For example, apply default styles for headings (h1, h2, etc.) and lists (bulleted or numbered) of the editor’s content. 

{% highlight javascript %}

 <textarea id="editor"></textarea>
 
 <script type="text/javascript">
    $(function () {
        $("#editor").ejRTE({
        value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
        " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea." 
        });
    });
    function addCssToIframe() {
        var editor = $("#editor").ejRTE("instance");
        var iframeDoc = editor.getDocument();
        var linkTag = document.createElement("link");
        linkTag.type = "text/css";
        linkTag.rel = "stylesheet";
        linkTag.href = "Content/Css/iframe-custom.css";
        iframeDoc.head.appendChild(linkTag);
    }
</script>

{% endhighlight %}

The new file named iframe-custom.css is created and moved to the content folder with the following styles.

{% highlight html %}
h1 {
    color: navy;
    margin-left: 20px;
}

ul { 
    display: block;
    list-style-type: square;
    margin-left: 10px;
}

ol {
    display: block;
    list-style-type: circle;
    margin-right: 10px;
}
{% endhighlight %}

N> Our RTE control editor section is an iframe. An iframe has another scope, so we can't access it to style using class which is defined in main document. To set the styles for the contents that kept inside the editor(iframe) we have to append the styles link in iframe head section.

## Content Editable

The editor provides option to control the editable behavior using [allowEditing](https://help.syncfusion.com/api/js/ejrte#members:allowediting) property. When the allowEditing property is set to false, the editor disables its editing functionality. 

{% highlight html %}

<textarea id ="editor"></textarea>

<script type ="text/javascript">

   $(function () {

            $("#editor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                allowEditing: false
            });

        });

</script>
{% endhighlight %}

The contentEditable attribute allows you to make any element of HTML content to become editable or non-editable.  

{% highlight html %}

<textarea id ="editor"></textarea>

<script type ="text/javascript">

 $(function () {

            $("#editor").ejRTE({
                value: "<p>The RichTextEditor (RTE) control enables you to edit the contents with insert table and images,</p>" +
                "<p> it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.</p>",
            });

            var editor = $("#editor").ejRTE("instance");
            var iframeDoc = editor.getDocument();
            var paragraph = $("p", iframeDoc.body);
            $($(paragraph)[1]).attr("contenteditable", "false");
        });

</script>

{% endhighlight %}

N> Content editable is fully compatible with latest browsers, to know more details, see [here](http://www.w3schools.com/tags/att_global_contenteditable.asp#).

## Submit Content

The editor allows you to process its content before it is being submitted to the server on form submit event. You can use this option to validate content on the client side to prevent invalid data from being submitted to the server.

This example shows how to encode the HTML content before form submit event.

{% highlight html %}

    <form>
        <textarea id ="editor"></textarea>
        <button type ="submit">Submit</button>
    </form>
    <script type ="text/javascript">

            $(function () {
            $("#editor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            });
        });

        $("form").on("submit", function () {

            var editor = $("#editor").data("ejRTE");
            var encoded = $('<div />').text(editor.model.value).html();
            $("#editor").val(encoded);

        });
    </script>

{% endhighlight %}

## Refresh

When you move the editor’s wrapper element into another DOM element, the editor needs to be reinitialized by the [refresh](https://help.syncfusion.com/api/js/ejrte#methods:refresh) method to retain its content. The method reload the content area and rebind the events of the editor. 

{% highlight html %}

    <textarea id="editor"></textarea>

    <div id="target"></div>

    <button onclick="appendTo()">Append To</button>
    <button onclick="refresh()">Refresh</button>
    
    <script type="text/javascript">
            var editor = null;
            $(function () {
                $("#editor").ejRTE({
                    value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                    " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                });
                editor = $("#editor").ejRTE("instance");
            });
            function appendTo() {
                editor._rteWapper.appendTo($("#target"))
            }
            function refresh() {
                editor.refresh()
            }
    </script>

{% endhighlight %}

## Persistence

The editor is capable to persist its content with HTML format. By default, the persistence support is disabled in the editor. When you set the [enablePersistence](https://help.syncfusion.com/api/js/ejrte#members:enablepersistence) property to true, the persistence will be enabled in the editor.

N>  [local storage](http://www.w3schools.com/html/html5_webstorage.asp#) is not supported below ie9 version, therefore persistence support is fallback to [cookie](http://www.w3schools.com/js/js_cookies.asp#).

{% highlight html %}

    <textarea id="editor"></textarea>

    <script type="text/javascript">
        $(function () {
            $("#editor").ejRTE({
                enablePersistence: true
            });
        });
    </script>

{% endhighlight %}

## Set Default Font Name and Size

* Set a default font name and font size to the font name and size drop-down programmatically.

N> <BR>
•	By default, the editor’s < iframe > is initialized with “Segoe UI” font name and 3(12pt) font size. <BR> 
•	To change it, select a different font name and font size from the drop-down in the editor’s toolbar. <BR>
•	To apply different font style for particular section of the content, select the text that you would like to change, and select a required font style from the drop-down to apply the changes to the selected text.<BR>


{% highlight html %}

<textarea id="editor"></textarea>
 
<script>
    $("#editor").ejRTE({
        value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images, it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        tools: {
            font: ["fontName", "fontSize", "fontColor", "backgroundColor"]
        },
         minWidth:"100px",
        isResponsive:true
    });

    var editor = $("#editor").ejRTE("instance");
    var dropdownObj = editor._fontStyleDDL.ejDropDownList("instance");
    dropdownObj.selectItemByIndex(7);
    var dropdownSize = editor._fontSizeDDL.ejDropDownList("instance");
    dropdownSize.selectItemByIndex(5);
</script>

{% endhighlight %}

* You can set default font for &lt; iframe &gt;’s body tag using [iframeAttributes](user-interface#iframe-attributes) property.

{% highlight html %}

<textarea id="editor"></textarea>
  
<script type="text/javascript">

    $(function () {

        $("#editor").ejRTE({
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            iframeAttributes: { style: "font-family:Arial;font-size:14px" }
        });

    });
</script>

{% endhighlight %}

* If you want to override the default font from CSS, create a style tag with CSS styles and append it to the &lt; iframe &gt;’s head tag of the editor.

{% highlight html %}

<textarea id="editor"></textarea>

<script type="text/javascript">

        $(function () {

            $("#editor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            });

            var css = "html,body{font-family:sans-serif;font-size:14px; }";
            var editorDoc = $("#editor").ejRTE("instance").getDocument();
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

## Adding Font Names and Font Size

If you want to add additional font names and font sizes to font drop-down, pass the font information as JSON data and bind it with instance of drop-down. 

{% highlight html %}

<textarea id="editor"></textarea>

<script type="text/javascript">
        
    $(function () {
        $("#editor").ejRTE({
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images, it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            tools: {
                font: ["fontName", "fontSize", "fontColor", "backgroundColor"]
            }
        });

        var editor = $("#editor").ejRTE("instance");
        editor.defaults.fontName.push({ text: "Calibri Light", value: "CalibriLight" }, { text: "Calibri", value: "Calibri" });
        editor.defaults.fontSize.push({ text: "8 (42pt)", value: "8" });
		var dropdownObj = editor._fontStyleDDL.ejDropDownList("instance");
		var dropdownSize = editor._fontSizeDDL.ejDropDownList("instance");
        dropdownObj.option({ "dataSource": editor.defaults.fontName });
		dropdownSize.option({ "dataSource": editor.defaults.fontSize });
        dropdownObj.selectItemByValue("CalibriLight");
		dropdownSize.selectItemByValue("8");
    });

</script>

{% endhighlight %}

## Apply Font color and Background color

If you want to apply font  color or background color for a selected content of RTE you can use font color and background color tools. These tools contains a color palette with basic colors along with an option called **"More colors.."** in order to choose custom colors from color picker dialog.You can apply transparent background color for selected text through **transparent** button available in background color palette.

{% highlight html %}

    <textarea id="editor"></textarea>

    <script type="text/javascript">
        
        $(function () {
            $("#editor").ejRTE({
              value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images, it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
              tools: {
                font: ["fontName", "fontSize", "fontColor", "backgroundColor"]
            }
              });

         });

    </script>

{% endhighlight %}

## Insert the content at cursor

If you want to insert/paste the content at the current cursor position (or) to replace the selected content with some formatting, you can use [pasteContent](https://help.syncfusion.com/api/js/ejrte#methods:pastecontent) method in the editor. you can use [getSelectedHtml](https://help.syncfusion.com/api/js/ejrte#methods:getselectedhtml) method to select the content.

{% highlight html %}

<textarea id="editor"></textarea>

<script type="text/javascript">

    $(function () {
        $("#editor").ejRTE({
            value:"The RichTextEditor (RTE) control enables you to edit the contents with insert table and images,"+
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        });
    });
    function pasteContent() {
        var editor = $("#editor").ejRTE("instance");
        var selectedHtml = editor.getSelectedHtml();
        editor.pasteContent("<p style ='background-color:yellow;color:skyblue'>" + selectedHtml + "</p>");
    }
</script>
    
{% endhighlight %}
