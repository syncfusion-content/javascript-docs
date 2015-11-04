---
layout: post
title: User Interface
description: User Interface
platform: js
control: RTE
documentation: ug

---
# User Interface

The editor user interface (UI) is designed with the toolbar, content area (iframe), and footer elements.

## Toolbar

The editor’s toolbar contains buttons and dropdowns that help you to format your content.

### Toolbar Items

The following table lists the available buttons and dropdowns on the toolbar:

<table>
<tr>
<td>
**Name******<br/><br/></td><td>
**Summary******<br/><br/></td><td>
**Initialization******<br/><br/></td><td>
**IsDefault****?******<br/><br/></td></tr>
<tr>
<td>
Font<br/><br/></td><td>
Applies font type, size, and color to the content.<br/><br/></td><td>
tools: { <br/>font: ["fontName", "fontSize", "fontColor", "backgroundColor"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
Font style<br/><br/></td><td>
Applies bold, italic, underline, and strikethrough formatting to the content.<br/><br/></td><td>
tools: {<br/>style: ["bold", "italic", "underline", "strikethrough"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Alignment<br/><br/></td><td>
Align the content with left, center, and right margin. <br/><br/></td><td>
tools: {<br/>alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
List<br/><br/></td><td>
Create a new list item (bulleted/numbered).<br/><br/></td><td>
tools: {<br/>lists: ["unorderedList", "orderedList"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Indents<br/><br/></td><td>
Allows to increase/decrease the indent level of the content. <br/><br/></td><td>
tools: {<br/>indenting: ["outdent", "indent"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Undo/Redo Action<br/><br/></td><td>
Allows to undo/redo the actions<br/><br/></td><td>
tools: {<br/>doAction: ["undo", "redo"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Hyperlink<br/><br/></td><td>
Creates a hyperlink to a text or image to a specific location in the content.<br/><br/></td><td>
tools: {<br/>links: ["createLink","removeLink"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Images<br/><br/></td><td>
Inserts an image from an online source or local computer.<br/><br/></td><td>
tools: {<br/>images: ["image"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Media<br/><br/></td><td>
Allows to embed a video into the document.<br/><br/></td><td>
tools: {<br/>media: ["video"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Table<br/><br/></td><td>
Allows to add or modify Tables.<br/><br/></td><td>
tools: {<br/>tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Paragraph<br/><br/></td><td>
Inserts a new paragraph<br/><br/></td><td>
tools: {<br/>paragraph: ["paragraph"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
Casing<br/><br/></td><td>
Change the case of selected text in the content<br/><br/></td><td>
tools: {<br/>casing: ["upperCase", "lowerCase"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
Scripts<br/><br/></td><td>
Makes the selected text as superscript (higher) or subscript (lower).<br/><br/></td><td>
tools: {<br/>effects: ["superscript", "subscript"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
Format<br/><br/></td><td>
Clears the formatting options like bold, italic, underline and more.<br/><br/></td><td>
tools: {<br/>formatStyle: ["format"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Clipboard Actions<br/><br/></td><td>
Controls the clipboard actions by applying specific action on the selected content.<br/><br/></td><td>
tools: {<br/>clipboard: ["cut", "copy", "paste"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
</table>
### Customize Toolbar

You can customize and rearrange items (buttons and dropdowns) by adding, removing, and enabling/disabling on the editor’s toolbar. 

#### Rearrange Group

The toolbar contains groups, which are similar or related functionalities of toolbar items for efficient access. By default, the groups are arranged using the following order:

{% highlight js %}
toolsList: ["formatStyle", "font", "style", "effects", "alignment", "lists", "indenting", "clipboard", "doAction", 
"clear", "links", "images", "media", "tables", "casing", "customTools", "view"]
{% endhighlight %}

The group can be rearranged on customization using the **[toolsList](http://help.syncfusion.com/js/api/ejrte#members:toolslist)** property.



{% highlight js %}
$(function () {
$("#texteditor").ejRTE({
toolsList: ["links", "lists", "doAction", "style", "images"],
tools: {
style: ["bold", "italic"],
lists: ["unorderedList", "orderedList"],
doAction: ["undo", "redo"],
links: ["createLink","removeLink"],
images: ["image"]
}
});

});
{% endhighlight %}

N> If you are not specify any group in **toolsList** property, the editor will create the toolbar with default group.

#### Add Toolbar item

The editor’s toolbar can be extended through the **customTools** option, which renders the custom toolbar items along with the built-in toolbar items. 

{% highlight js %}
$("#texteditor").ejRTE({

toolsList: ["customTools"],
tools: {
customTools: [{
name: "insertcode",

text: "insertcode",
tooltip: "Insert code snippets",
css: "e-rte-toolbar-icon insertcode",
action: function () {
var rte = $("#texteditor").data("ejRTE");
// handle the execute action on click the custom tool
}
}]
}
});
{% endhighlight %}

Define the CSS that will be applied to the custom tool.

{% highlight html %}
.e-rte-toolbar-icon.insertcode:before {
content: "\e780";
font-size: 18px;
margin: 3px;
}
{% endhighlight %}

N> The CSS class that defined for custom tool is directly applies to the newly added toolbar item. 

#### Remove Toolbar item

To remove a particular toolbar item, pass the id of a toolbar item to the [removeToolbarItem](http://help.syncfusion.com/js/api/ejrte#methods:removetoolbaritem) method.

{% highlight js %}
var rte = $("#texteditor").data("ejRTE");
rte.removeToolbarItem("video");
{% endhighlight %}

N> This method completely removes the DOM element along with the events bounded to it.

#### Enable/Disable Toolbar item

The state of each toolbar item can be controlled by calling the client-side methods such as [enableToolbarItem](http://help.syncfusion.com/js/api/ejrte#methods:enabletoolbaritem) and [disableToolbatItem](http://help.syncfusion.com/js/api/ejrte#methods:disabletoolbaritem).

{% highlight js %}
var rte = $("#texteditor").data("ejRTE");
rte.disableToolbarItem("video");
{% endhighlight %}

{% highlight js %}
var rte = $("#texteditor").data("ejRTE");
rte.enableToolbarItem("video");
{% endhighlight %}

N> If a toolbar item is in disabled state, then it will not have any interactivity including mouse hover.

### Show/Hide Toolbar

The toolbar can be initially set to visible or hidden within the editor using [showToolbar](http://help.syncfusion.com/js/api/ejrte#members:showtoolbar "") API. Default value is “true”.

{% highlight js %}
$("#texteditor").ejRTE({
showToolbar: false
});
{% endhighlight %}

## Content Area

The editor creates the iframe element as the content area on control initialization, it is used to display and editing the content. In Content Area, the editor displays only the body tag of a &lt; iframe &gt; document. To set or modify details in the <head> tag, use [Source view](#_HTML_View "") of the editor.

### Iframe Attributes

The editor allows you to passing an additional attributes to body tag of a &lt; iframe &gt; element using [iframeAttributes](http://help.syncfusion.com/js/api/ejrte#members:iframeattribute) property. The property contains name/value pairs in string format, it is used to override the default appearance of the content area. For example, the content area’s font, color, margins, and background can be overridden using iframeAttributes property. You can specifies the editable behavior (content editable) of the content also in this property. For more information about the content editable, see [content editable](#_ContentEditable).

{% highlight js %}
$(function () {

$("#texteditor").ejRTE({
value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
" it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
iframeAttribute: "background-color:#e0ffff;color:#6495ed;"
});

});
{% endhighlight %}

### Adding CSS File

The editor offers you to add external CSS file to style the &lt; iframe &gt; element.  You can change the appearance of editor’s content using an external CSS file. For example, apply default styles for headings (h1, h2, etc.) and lists (bulleted or numbered) of the editor’s content. 

{% highlight js %}
$(function () {

$("#texteditor").ejRTE({
value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
" it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
});

});

function addCssToIframe() {
var editor = $("#texteditor").ejRTE("instance");
var iframeDoc = editor.getDocument();
var linkTag = document.createElement("link");
linkTag.type = "text/css";
linkTag.rel = "stylesheet";
linkTag.href = "Content/Css/iframe-custom.css";
iframeDoc.head.appendChild(linkTag);
}
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

### Content Editable

The editor provides option to control the editable behavior using [allowEditing](http://help.syncfusion.com/js/api/ejrte#members:allowediting) property. When the allowEditing property is set to false, the editor disables its editing functionality. 

{% highlight html %}

<textarea id="texteditor"></textarea>

<script type="text/javascript">

$(function () {

$("#texteditor").ejRTE({
value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
" it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
allowEditing: false
});

});

</script>
{% endhighlight %}

The contentEditable attribute allows you to make any element of HTML content to become editable or non-editable.  

{% highlight html %}

<textarea id="texteditor"></textarea>

<script type="text/javascript">

$(function () {

$("#texteditor").ejRTE({
value: "<p>The RichTextEditor (RTE) control enables you to edit the contents with insert table and images,</p>" +
"<p> it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.</p>",
});

var editor = $("#texteditor").ejRTE("instance");
var iframeDoc = editor.getDocument();
var paragraph = $("p", iframeDoc.body);
$($(paragraph)[1]).attr("contenteditable", "false");
});

</script>
{% endhighlight %}

N> Content editable is fully compatible with latest browsers, to know more details, see [here](http://www.w3schools.com/tags/att_global_contenteditable.asp#).

## Footer

This option allows you to specify which footer elements should display at the bottom of the editor. The available footer elements are listed below:

1. HTML View
2. HTML Tag Info
3. Characters Count / Word Count 
4. Clear Format
5. Resizer

{% highlight js %}
$("#texteditor").ejRTE({
showFooter: true
});
{% endhighlight %}

### Source View

Source view displays the HTML code of the content in a separate dialog. Source view allows you to view and edit the HTML Tags, scripts, and styles directly. If you made any modification in Source view directly, click **Update** button to synchronize with Design view.

You can paste HTML text into Source view. If you cut or copy from HTML source such as page source of Browser, paste as HTML (without escape characters) into Source view. 

{% highlight js %}
$("#texteditor").ejRTE({
showFooter:true,
showHtmlSource: true
});
{% endhighlight %}

N> Source view is useful for working directly with raw HTML text, so this tool is mainly used for advanced users who would like to have more control over the source of their content. 

### HTML Tag Info

The HTML tag info tool that shows the path of currently selected tag along with hierarchy of parent tags to which it belongs. The tag information is displayed at the bottom of the editor. It is used to determine which element has the focus in the editor’s content. 

{% highlight js %}
$("#texteditor").ejRTE({
showFooter: true,
showHtmlTagInfo: true
});
{% endhighlight %}

N> The outermost tag is the body tag of &lt; iframe &gt; element in design view, so it shows the path from currently selected path to the body tag.

### Characters Count/Word Count

The editor automatically counts the number of characters and words in the content while you type. The characters and words count displayed at the bottom of the editor. You can limit the number of characters in your content using [maxLength](http://help.syncfusion.com/js/api/ejrte#members:maxlength) property. By default, the editor sets the characters limit value as 7000 characters.

{% highlight html %}

<textarea id="texteditor"></textarea>
<script type="text/javascript">
$(function () {

$("#texteditor").ejRTE({
showFooter: true,
showWordCount: true,
showCharCount: true,
maxLength: 500
});

});
</script>
{% endhighlight %}

N> The editor counts the characters by including the space, and this validation occurs while pasting the content into the editor also.

### Clear Format

The clear format tool is useful to remove all formatting styles (such as bold, italic, underline, color, superscript, subscript, and more) from currently selected text. As a result, all the text formatting will be cleared and return to its default formatting styles. When you set the [showClearFormat](http://help.syncfusion.com/js/api/ejrte#members:showclearformat) property to true, the clear format tool will be displayed at bottom of the editor.

{% highlight js %}
$("#texteditor").ejRTE({
showFooter: true,
showClearFormat: true
});
{% endhighlight %}

### Resize Handle

When you set the [enableResize](http://help.syncfusion.com/js/api/ejrte#members:enableresize) property to true, resize handle will be displayed at bottom-right corner of the editor. You can drag the handle to change its size. On resizing, the editor will automatically adjust the toolbar, content area, and footer within it accordingly. Resize limits can be defined via [minHeight](http://help.syncfusion.com/js/api/ejrte#members:minheight), [maxHeight](http://help.syncfusion.com/js/api/ejrte#members:maxheight), [minWidth](http://help.syncfusion.com/js/api/ejrte#members:minwidth), and [maxWidth](http://help.syncfusion.com/js/api/ejrte#members:maxwidth) properties. You can specify the size of the editor programmatically through the [height](http://help.syncfusion.com/js/api/ejrte#members:height) and [width](http://help.syncfusion.com/js/api/ejrte#members:width) properties. 

{% highlight js %}
$("#texteditor").ejRTE({
showFooter: true,
enableResize: true,
width: 600, minWidth: 250, maxWidth: 750,
height: 300, minHeight: 250, maxHeight: 500
});
{% endhighlight %}

N> When you set the enableRTL property to true, the resize handle will automatically positioned to the bottom-left corner of the editor.

