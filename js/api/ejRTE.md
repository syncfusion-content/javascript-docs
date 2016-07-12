---
layout: post
title: Properties, Methods and Events of ejRTE Widget
description: API reference for ejRTE
documentation: API
platform: js
keywords: RTE, ejRTE, syncfusion, RTE api  
---

# ejRTE




Rich text editor is a component that help you to display or edit the content including tables, hyperlinks, paragraphs, lists, video, and images. The editor supports file and folder management using FileExplorer component.




#### Syntax

{% highlight javascript %}

$(element).ejRTE(options)

{% endhighlight %}





<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">settings for RTE.</td>
</tr>
</tbody>
</table>

#### Example:


{% highlight html %}
 
<textarea id="rteSample">       
<p><b>Description:</b></p>
            <p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >   <script>
// Creates the RTE
$("#rteSample").ejRTE();
</script>  

{% endhighlight %}


#### Requires


* module:jQuery

* module:jquery.easing.1.3.js

* module:jquery.js

* module:jquery.globalize.js

* module:jquery.globalize.culture.en-US.js

* module:ej.core.js

* module:ej.data.js

* module:ej.rte.js

* module:ej.button.js

* module:ej.togglebutton.js

* module:ej.colorpicker.js

* module:ej.slider.js

* module:ej.splitbutton.js

* module:ej.checkbox.js

* module:ej.radiobutton.js

* module:ej.dropdownlist.js

* module:ej.dialog.js

* module:ej.toolbar.js

* module:ej.editor.js

* module:ej.menu.js

* module:ej.tab.js

* module:ej.scroller.js

* module:ej.draggable.js

* module:ej.treeview.js

* module:ej.waitingpopup.js

* module:ej.uploadbox.js

* module:ej.splitter.js

* module:ej.fileexplorer.js

* module:ej.grid.base.js

* module:ej.grid.common.js

* module:ej.grid.edit.js

* module:ej.grid.filter.js

* module:ej.grid.selection.js

* module:ej.grid.sort.js


### Members



### allowEditing `boolean`
{:#members:allowediting}

Enables/disables the editing of the content.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea id="rteSample">  
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p>
        </textarea><script>
    // Initializes the RTE with the specified allowEditing value.
    $("#rteSample").ejRTE({ allowEditing: false });
</script>
{% endhighlight %}

### allowKeyboardNavigation `boolean`
{:#members:allowkeyboardnavigation}





RTE control can be accessed through the keyboard shortcut keys.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in 
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea > <script>
    // Initializes the RTE with the specified allowKeyboardNavigation value.
    $("#rteSample").ejRTE({ allowKeyboardNavigation: false });
</script>
{% endhighlight %}




### autoFocus  `boolean`
{:#members:autoFocus }




When the property is set to true, it focuses the RTE at the time of rendering.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in 
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified autoFocus value.
    $("#rteSample").ejRTE({ autoFocus: true });
    </script>
{% endhighlight %}




### autoHeight  `boolean`
{:#members:autoHeight }




Based on the content size, its height is adjusted instead of adding the scrollbar.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea id="rteSample">  
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea><script>
    // Initializes the RTE with the specified autoHeight value.
    $("#rteSample").ejRTE({ autoHeight: true });
</script>
{% endhighlight %}




### colorCode `object`
{:#members:colorcode}





Sets the colorCode to display the color of the fontColor and backgroundColor in the font tools of the RTE.


#### Default Value




* ["000000", "FFFFFF", "C4C4C4", "ADADAD", "595959", "262626", "4f81bd", "dbe5f1", "b8cce4", "95b3d7", "366092", "244061", "c0504d", "f2dcdb", "e5b9b7", "d99694", "953734",
"632423", "9bbb59", "ebf1dd", "d7e3bc", "c3d69b", "76923c", "4f6128", "8064a2", "e5e0ec", "ccc1d9", "b2a2c7", "5f497a", "3f3151", "f79646", "fdeada", "fbd5b5", "fac08f","e36c09", "974806"]





#### Example



{% highlight html %}
 <textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified colorCode value.
    $("#rteSample").ejRTE({
        toolsList: ["font"],
        tools: {
            font: ["fontColor", "backgroundColor"]
        },
        colorCode: [
                    "000000", "FFFFFF", "C4C4C4", "ADADAD", "595959", "262626", "4f81bd", "dbe5f1", "b8cce4", "95b3d7", "366092", "244061", "c0504d", "f2dcdb", "e5b9b7", "d99694", "953734","632423", "9bbb59", "ebf1dd", "d7e3bc", "c3d69b", "76923c", "4f6128", "8064a2", "e5e0ec", "ccc1d9", "b2a2c7", "5f497a", "3f3151", "f79646", "fdeada", "fbd5b5", "fac08f",
                    "e36c09", "974806"
            ]
    });
    </script>
{% endhighlight %}




### colorPaletteColumns `number`
{:#members:colorpalettecolumns}




The number of columns given are rendered in the color palate popup.


#### Default Value




* 6




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
        // Initializes the RTE with the specified colorPaletteColumns value.
        $("#rteSample").ejRTE({
            toolsList: ["font"],
            tools: {
                font: ["fontColor", "backgroundColor"]
            },
            colorPaletteColumns: 10
        });
    </script>
{% endhighlight %}




### colorPaletteRows `number`
{:#members:colorpaletterows}



The number of rows given are rendered in the color palate popup.


#### Default Value




* 6




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea><script>
    // Initializes the RTE with the specified 'colorPaletteRows' value. 
        $("#rteSample").ejRTE({
            toolsList: ["font"],
            tools: {
                font: ["fontColor", "backgroundColor"]
            },
            colorPaletteRows: 5
        });
</script>
{% endhighlight %}




### cssClass `string`
{:#members:cssclass}




Sets the root class for the RTE theme. This cssClass API helps the usage of custom skinning option for the RTE control by including this root class in CSS.

#### Default Value




* ""




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    //Initializes the RTE with the specified cssClass value.
    $("#rteSample").ejRTE({ cssClass: 'gradient-lime' });
</script>
{% endhighlight %}




### enabled `boolean`
{:#members:enabled}





Enables/disables the RTE control’s accessibility or interaction.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified enabled value.
    $("#rteSample").ejRTE({ enabled: false });
</script>
{% endhighlight %}




### enableHtmlEncode  `boolean`
{:#members:enableHtmlEncode }





When the property is set to true, it returns the encrypted text.


#### Default Value




* false




#### Example



{% highlight html %}
 <textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified enabled value.
    $("#rteSample").ejRTE({ enableHtmlEncode: false });
</script>
{% endhighlight %}




### enablePersistence `boolean`
{:#members:enablepersistence}




Maintain the values of the RTE after page reload.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified enablePersistence value.
    $("#rteSample").ejRTE({ enablePersistence: false });
</script>
{% endhighlight %}




### enableResize `boolean`
{:#members:enableresize}





Shows the resize icon and enables the resize option in the RTE.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified enableResize value.
    $("#rteSample").ejRTE({ enableResize: true });
</script>
{% endhighlight %}




### enableRTL `boolean`
{:#members:enablertl}




Shows the RTE in the RTL direction.


#### Default Value




* false




#### Example



{% highlight html %}
 <textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified enableRTL value .
    $("#rteSample").ejRTE({ enableRTL: true });
</script>
{% endhighlight %}



### enableXHTML `boolean`
{:#members:enablexhtml}





Formats the contents based on the XHTML rules.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified enableXHTML value.
    $("#rteSample").ejRTE({ enableXHTML: true });
</script>
{% endhighlight %}




### enableTabKeyNavigation  `boolean`
{:#members:enableTabKeyNavigation }





Enables the tab key action with the RichTextEditor content. 


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified enableTabKeyNavigation value.
    $("#rteSample").ejRTE({ enableTabKeyNavigation: false });
</script>
{% endhighlight %}





### externalCSS `string`
{:#members:externalcss}




Load the external CSS file inside Iframe.


#### Default Value




* null




#### Example


{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified enableXHTML value.
    $("#rteSample").ejRTE({ externalCSS:"default.css"});
</script>
{% endhighlight %}



### fileBrowser `object`
{:#members:filebrowser}





This API allows to enable the file browser support in the RTE control to browse, create, delete and upload the files in the specified current directory.


#### Default Value




* null




#### Example



{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
// Initializes the RTE with the fileBrowser value specified.
$("#rteSample").ejRTE({  fileBrowser: {
  filePath: "../FileExplorerContent/",
 extensionAllow: "*.png, *.doc, *.pdf, *.txt, *.docx",
ajaxAction: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/",
}});
</script>
{% endhighlight %}




### fileBrowser.ajaxAction `string`
{:#members:filebrowser-ajaxaction}




This API is used to receive the server-side handler for file related operations.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified fileBrowser’s ajaxAction value.
    $("#rteSample").ejRTE({ fileBrowser: {
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction"
    }
    });
</script>
{% endhighlight %}




### fileBrowser.extensionAllow `string`
{:#members:filebrowser-extensionallow}




Specifies the file type extension shown in the file browser window.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified fileBrowser’s extensionAllow value.
    $("#rteSample").ejRTE({ fileBrowser: {
        extensionAllow: "*.doc,*.docx,*.pdf,*.txt"
    }
    });
</script>
{% endhighlight %}




### fileBrowser.filePath `string`
{:#members:filebrowser-filepath}


Specifies the directory to perform operations like create, delete and rename folder and files, and upload the selected files to the current directory.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified fileBrowser’s filePath value.
    $("#rteSample").ejRTE({ fileBrowser: {
        filePath: "../FileExplorerContent/"
    }
    });
</script>
{% endhighlight %}



### fontName `object`
{:#members:fontname}



Sets the fontName in the RTE.


#### Default Value




* {text: "Segoe UI", value: "Segoe UI" },
{text: "Arial", value: "Arial,Helvetica,sans-serif" },
{text: "Courier New", value: "Courier New,Courier,Monospace" },
{text: "Georgia", value: "Georgia,serif" },
{text: "Impact", value: "Impact,Charcoal,sans-serif" },
{text: "Lucida Console", value: "Lucida Console,Monaco,Monospace" },
{text: "Tahoma", value: "Tahoma,Geneva,sans-serif" },
{text: "Times New Roman", value: "Times New Roman" },
{text: "Trebuchet MS", value: "Trebuchet MS,Helvetica,sans-serif" }, 
{text: "Verdana", value: "Verdana,Geneva,sans-serif"}





#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
// Initializes the RTE with the fontName value specified.
$("#rteSample").ejRTE({ fontName: [
                { text: "Segoe UI", value: "Segoe UI"},
                { text: "Arial", value: "Arial,Helvetica,sans-serif"},
                { text: "Courier New", value: "Courier New,Courier,monospace"},
                { text: "Georgia", value: "Georgia,serif"},
                { text: "Impact", value: "Impact,Charcoal,sans-serif"},
                { text: "Lucida Console", value: "Lucida Console,Monaco,monospace"},
                { text: "Tahoma", value: "Tahoma,Geneva,sans-serif"},
                { text: "Times New Roman", value: "Times New Roman"},
                { text: "Trebuchet MS", value: "Trebuchet MS,Helvetica,sans-serif"},
                { text: "Verdana", value: "Verdana,Geneva,sans-serif"}]}); 
</script>
                
{% endhighlight %}



### fontSize `object`
{:#members:fontsize}




Sets the fontSize in the RTE.


#### Default Value




* { text: "1", value: "1" },
{ text: "2 (10pt)", value: "2" },
{ text: "3 (12pt)", value: "3" },
{ text: "4 (14pt)", value: "4" },
{ text: "5 (18pt)", value: "5" },
{ text: "6 (24pt)", value: "6" },
{ text: "7 (36pt)", value: "7" }




#### Example



{% highlight html %}

 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
// Initializes the RTE with the specified fontSize value.
$("#rteSample").ejRTE({ fontSize: [
                {
                    text: "1",
                    value: "1"
                },
                {
                    text: "2 (10pt)",
                    value: "2"
                },
                {
                    text: "3 (12pt)",
                    value: "3"
                },
                {
                    text: "4 (14pt)",
                    value: "4"
                },
                {
                    text: "5 (18pt)",
                    value: "5"
                },
                {
                    text: "6 (24pt)",
                    value: "6"
                },
                {
                    text: "7 (36pt)",
                    value: "7"
                }
]});
</script> {% endhighlight %}




### format `string`
{:#members:format}





Sets the format in the RTE.


#### Default Value




* { text: "Paragraph", value: "&lt;p&gt;", spriteCssClass: "e-paragraph" },
{ text: "Quotation", value: "&lt;blockquote&gt;", spriteCssClass: "e-quotation" },
{ text: "Heading 1", value: "&lt;h1&gt;", spriteCssClass: "e-h1" },
{ text: "Heading 2", value: "&lt;h2&gt;", spriteCssClass: "e-h2" },
{ text: "Heading 3", value: "&lt;h3&gt;", spriteCssClass: "e-h3" },
{ text: "Heading 4", value: "&lt;h4&gt;", spriteCssClass: "e-h4" },
{ text: "Heading 5", value: "&lt;h5&gt;", spriteCssClass: "e-h5" },
{ text: "Heading 6", value: "&lt;h6&gt;", spriteCssClass: "e-h6"}





#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
// Initializes the RTE with the specified format value.
$("#rteSample").ejRTE({format: [
                { text: "Paragraph", value: "<p>", spriteCssClass: "e-paragraph" },
                { text: "Quotation", value: "<blockquote>", spriteCssClass: "e-quotation" }, 
                { text: "Heading 1", value: "<h1>", spriteCssClass: "e-h1" }, 
                { text: "Heading 2", value: "<h2>", spriteCssClass: "e-h2" }, 
                { text: "Heading 3", value: "<h3>", spriteCssClass: "e-h3" }, 
                { text: "Heading 4", value: "<h4>", spriteCssClass: "e-h4" }, 
                { text: "Heading 5", value: "<h5>", spriteCssClass: "e-h5" }, 
                { text: "Heading 6", value: "<h6>", spriteCssClass: "e-h6" } ]}); 
                </script>
                {% endhighlight %}


### height `string`  `number`
{:#members:height}





Defines the height of the RTE textbox.


#### Default Value




* 370




#### Example



{% highlight html %}

<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    //Initializes the RTE height property with the specified value 
    $("#rteSample").ejRTE({ height: 250 });
</script>
{% endhighlight %}




### htmlAttributes `object`
{:#members:htmlattributes}





Specifies the HTML Attributes of the ejRTE.


#### Default Value




* {}




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
// Initializes the RTE with the specified HtmlAttributes.
    $("#rteSample").ejRTE({ htmlAttributes: { readOnly: "readOnly"} });
</script>
{% endhighlight %}




### iframeAttributes `object`
{:#members:iframeattributes}





Sets the given attributes to the iframe body element.


#### Default Value




* {}




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initialize the RTE with the specified iframeAttributes value .
    $("#rteSample").ejRTE({ iframeAttributes:{ style :"color:#5C5C5C" }});
</script>
{% endhighlight %}




### imageBrowser `object`
{:#members:imagebrowser}





This API allows the image browser to support in the RTE control to browse, create, delete, and upload the image files to the specified current directory.


#### Default Value




* null




#### Example



{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
// Initializes the RTE with the specified imageBrowser value.
$("#rteSample").ejRTE({  imageBrowser: {
  filePath: "../FileExplorerContent/",
 extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx",
ajaxAction: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/",
}});
</script>
{% endhighlight %}




### imageBrowser.ajaxAction `string`
{:#members:imagebrowser-ajaxaction}





This API is used to receive the server-side handler for the file related operations.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
// Initializes the RTE with the imageBrowser with the specified ajaxAction value.
$("#rteSample").ejRTE({  imageBrowser: {
  ajaxAction: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/"
}});
</script>
{% endhighlight %}




### imageBrowser.extensionAllow `string`
{:#members:imagebrowser-extensionallow}





Specifies the file type extension shown in the image browser window.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the imageBrowser with the specified extension value.
    $("#rteSample").ejRTE({ imageBrowser: {
        extensionAllow: "*.doc,*.docx,*.tiff,*.jpeg"
    }
    });
</script>
{% endhighlight %}




### imageBrowser.filePath `string`
{:#members:imagebrowser-filepath}





Specifies the directory to perform operations like create, delete and rename folder and files, and upload the selected images to the current directory.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified imageBrowser filePath value.
    $("#rteSample").ejRTE({ imageBrowser: {
        filePath: "../FileExplorerContent/"
    }
    });
</script>
{% endhighlight %}




### isResponsive `boolean`
{:#members:isresponsive}





Enables/disables responsive support for the RTE control toolbar items during the window resizing time.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea   id="rteSample">  
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified isResponsive value.
    $("#rteSample").ejRTE({ isResponsive: true });
</script>
{% endhighlight %}




### locale `string`
{:#members:locale}





Sets the culture in the RTE when you set the localization values are needs to be assigned to the corresponding text as follows.  


#### Default Value




* "en-US"




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified culture value.
ej.RTE.Locale["en-US"] = {
        bold: "Bold",
        italic: "Italic",
        underline: "Underline",
        strikethrough: "Strikethrough",
        superscript: "Superscript",
        subscript: "Subscript",
        justifyCenter: "Align text center",
        justifyLeft: "Align text left",
        justifyRight: "Align text right",
        justifyFull: "Justify",
        unorderedList: "Insert unordered list",
        orderedList: "Insert ordered list",
        indent: "Increase Indent",
        fileBrowser: "File Browser",
        outdent: "Decrease Indent",
        cut: "Cut",
        copy: "Copy",
        paste: "Paste",
        paragraph: "Paragraph",
        undo: "Undo",
        redo: "Redo",
        upperCase: "Upper Case",
        lowerCase: "Lower Case",
        clearAll: "Clear All",
        clearFormat: "Clear Format",
        createLink: "Insert/Edit hyperlink",
        removeLink: "remove hyperlink",
        image: "Insert image",
        video: "Insert video",
        editTable: "Edit Table Properties",
        embedVideo: "Paste your embed code below",
        viewHtml: "View HTML",
        fontName: "Select font family",
        fontSize: "Select font size",
        fontColor: "Select color",
        format: "Format",
        backgroundColor: "Background color",
        style: "Styles",
        deleteAlert: "Are you sure you want to clear all the contents?",
        copyPastAlert: "Your browser doesn't support direct access to the clipboard. Please use the Ctrl+X/C/V keyboard shortcuts instead.",
        videoError: "The text area can not be empty",
        imageWebUrl: "Web Address",
        imageAltText: "Image description",
        dimensions: "Dimensions",
        constrainProportions: "Constrain Proportions",
        linkWebUrl: "Web Address",
        imageLink: "Image as Link",
        imageBorder: "Image Border",
        imageStyle: "Style",
        linkText: "Text",
        linkToolTip: "Tooltip",
        html5Support: "This tool icon only enabled in HTML5 supported browsers",
        linkOpenInNewWindow: "Open link in new window",
        tableColumns: "No.of Columns",
        tableRows: "No.of Rows",
        tableWidth: "Width",
        tableHeight: "Height",
        tableCellSpacing: "Cell spacing",
        tableCellPadding: "Cell padding",
        tableBorder: "Border",
        tableCaption: "Caption",
        tableAlignment: "Alignment",
        textAlign: "Text align",
        dialogUpdate: "Update",
        dialogInsert: "Insert",
        dialogCancel: "Cancel",
        dialogApply: "Apply",
        dialogOk: "Ok",
        createTable: "Insert table",
        addColumnLeft: "Add column on the left",
        addColumnRight: "Add column on the right",
        addRowAbove: "Add row above",
        addRowBelow: "Add row below",
        deleteRow: "Delete row",
        deleteColumn: "Delete column",
        deleteTable: "Delete the table",
        customTable: "Create custom table...",
        characters: "Characters",
        words: "Words",
        general: "General",
        advanced: "Advanced",
        table: "Table",
        row: "Row",
        column: "Column",
        cell: "Cell",
        solid: "Solid",
        dotted: "Dotted",
        dashed: "Dashed",
        doubled: "Doubled",
        maximize:"Maximize",
	    resize: "Minimize",
	    swatches: "Swatches"
  };
    $("#rteSample").ejRTE({ locale: "en-US" });
</script>
{% endhighlight %}




### maxHeight `string`  `number`
{:#members:maxheight}




Sets the maximum height for the RTE outer wrapper element.


#### Default Value




* null




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified maxHeight value.
    $("#rteSample").ejRTE({ maxHeight: 900 });
</script>
{% endhighlight %}




### maxLength `number`
{:#members:maxlength}




Sets the maximum length for the RTE outer wrapper element.


#### Default Value




* 7000




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the maxLength value specified.
    $("#rteSample").ejRTE({ maxLength: 900 });
</script>
{% endhighlight %}




### maxWidth `string`  `number`
{:#members:maxwidth}





Sets the maximum width for the RTE outer wrapper element.


#### Default Value




* null




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified maxWidth value.
    $("#rteSample").ejRTE({ maxWidth: 900 });
</script>
{% endhighlight %}




### minHeight `string`  `number`
{:#members:minheight}





Sets the minimum height for the RTE outer wrapper element.


#### Default Value




* 280




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified minHeight value.
    $("#rteSample").ejRTE({ minHeight: 900 });
</script>
{% endhighlight %}




### minWidth `string`  `number`
{:#members:minwidth}




Sets the minimum width for the RTE outer wrapper element.


#### Default Value




* 400




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified minWidth value .
    $("#rteSample").ejRTE({ minWidth: 900 });
</script>
{% endhighlight %}




### name `string`
{:#members:name}





Sets the name in the RTE. When the name value is not initialized, the ID value is assigned to the name.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified name value.
    $("#rteSample").ejRTE({ name: "ecommentblog" });
</script>
{% endhighlight %}




### showClearAll `boolean`
{:#members:showclearall}





Shows ClearAll icon in the RTE footer.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showClearAll value.
    $("#rteSample").ejRTE({ showClearAll: false });
</script>
{% endhighlight %}



### showClearFormat `boolean`
{:#members:showclearformat}





Shows the clear format in the RTE footer.


#### Default Value




* true




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showClearFormat value.
    $("#rteSample").ejRTE({ showClearFormat: false });
</script>
{% endhighlight %}




### showCustomTable `boolean`
{:#members:showcustomtable}




Shows the Custom Table in the RTE.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showCustomTable value.
    $("#rteSample").ejRTE({showCustomTable: true});
</script>
{% endhighlight %}




### showContextMenu  `boolean`
{:#members:showContextMenu}




Shows custom contextmenu with the RTE. 


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showContextMenu value.
    $("#rteSample").ejRTE({ showContextMenu: false });
</script>

{% endhighlight %}





### showDimensions `boolean`
{:#members:showdimensions}





This API is used to set the default dimensions for the image and video. When this property is set to true, the image and video dialog displays the dimension option.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showDimensions value.
    $("#rteSample").ejRTE({ showDimensions: false });
</script>
{% endhighlight %}




### showFontOption `boolean`
{:#members:showfontoption}




Shows the FontOption in the RTE.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showFontOption value.
    $("#rteSample").ejRTE({ showFontOption: false });
</script>
{% endhighlight %}




### showFooter `boolean`
{:#members:showfooter}





Shows footer in the RTE. When the footer is enabled, it displays the HTML tag, word Count, character count, clear format, resize icon and clear all the content icons, by default.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showFooter value.
    $("#rteSample").ejRTE({ showFooter: true });
</script>
{% endhighlight %}




### showHtmlSource `boolean`
{:#members:showhtmlsource}




Shows the HtmlSource in the RTE footer.


#### Default Value




* false




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showHtmlSource value.
    $("#rteSample").ejRTE({ showHtmlSource: false });
</script>
{% endhighlight %}




### showHtmlTagInfo `boolean`
{:#members:showhtmltaginfo}




When the cursor is placed or when the text is selected in the RTE, it displays the tag info in the footer.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showHtmlTagInfo value.
    $("#rteSample").ejRTE({ showHtmlTagInfo: false });
</script>
{% endhighlight %}




### showToolbar `boolean`
{:#members:showtoolbar}




Shows the toolbar in the RTE.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showToolbar value.
    $("#rteSample").ejRTE({ showToolbar: false });
</script>
{% endhighlight %}




### showCharCount `boolean`
{:#members:showCharCount }


Counts the total characters and displays it in the RTE footer.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showCharCount value.
    $("#rteSample").ejRTE({showFooter: true , showCharCount: false });
</script>
{% endhighlight %}







### showWordCount  `boolean`
{:#members:showWordCount  }




Counts the total words and displays it in the RTE footer.


#### Default Value




* True




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified showWordCount value.
    $("#rteSample").ejRTE({showFooter: true , showWordCount: false });
</script>
{% endhighlight %}




### tableColumns `number`
{:#members:tablecolumns}





The given number of columns render the insert table pop.


#### Default Value




* 10




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified 'tableColumns' value.
    $("#rteSample").ejRTE({ tableColumns: 10 });
</script>
 {% endhighlight %}




### tableRows `number`
{:#members:tablerows}




The given number of rows render the insert table pop.


#### Default Value




* 8




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified 'tableColumns' value.
    $("#rteSample").ejRTE({ tableRows: 10 });
</script>
{% endhighlight %}




### tools `object`
{:#members:tools}




Sets the tools in the RTE and gets the inner display order of the corresponding group element. Tools are dependent on the toolsList property. 


#### Default Value




* formatStyle: ["format"], 
style: ["bold", "italic", "underline", "strikethrough"], 
alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"],  
lists: ["unorderedList", "orderedList"],
indenting: ["outdent", "indent"],
doAction: ["undo", "redo"],
links: ["createLink","removeLink"],
images: ["image"],
media: ["video"], 
tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", addColumnRight", "deleteRow", "deleteColumn", "deleteTable"]],
view:[“fullScreen”,"zoomIn","zoomOut"],
print:["print"]





#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea><script>
    // Initializes the RTE with the specified tools’ value.
    $("#rteSample").ejRTE({ tools: {
                formatStyle: ["format"],
                font: ["fontName", "fontSize", "fontColor", "backgroundColor"],
                style: ["bold", "italic", "underline", "strikethrough"],
                alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"],
                clipboard: ["cut", "copy", "paste"],
                clear: ["clearFormat", "clearAll"],
                lists: ["unorderedList", "orderedList"],
                indenting: ["outdent", "indent"],
                doAction: ["undo", "redo"],
                effects:["superscript","subscript"]
                links: ["createLink","removeLink"],
                images: ["image"],
                media: ["video"],
                view: ["fullScreen","zoomIn","zoomOut"],
                casing:["upperCase", "lowerCase"],
                tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"],
                print: ["print"]
            }   
    });
    </script>
{% endhighlight %}




### tools.alignment `object`
{:#members:tools-alignment}



Specifies the alignment tools and the display order of this tool in the RTE toolbar.




#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified alignment tools value.
    $("#rteSample").ejRTE({ tools: {
            alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"]                
            }    
    });
    </script>
{% endhighlight %}




### tools.casing  `array`
{:#members:tools-casing }



Specifies the casing tools and the display order of this tool in the RTE toolbar.




#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified casing tools value.
    $("#rteSample").ejRTE({ tools: {
            casing:["upperCase", "lowerCase"]         
            }    
    });
    </script>
{% endhighlight %}




### tools.clear   `array`
{:#members:tools-clear  }



Specifies the clear tools and the display order of this tool in the RTE toolbar.




#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified clear tools value.
    $("#rteSample").ejRTE({ tools: {
            clear: ["clearFormat", "clearAll"]         
            }    
    });
    </script>
{% endhighlight %}




### tools.clipboard `array`
{:#members:tools-clipboard}




Specifies the clipboard tools and the display order of this tool in the RTE toolbar.




#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified clipboard tools value.
    $("#rteSample").ejRTE({ tools: {
            clipboard: ["cut", "copy", "paste"]         
            }    
    });
    </script>
{% endhighlight %}




### tools.edit `array`
{:#members:tools-edit}




Specifies the edit tools and the displays tool in the RTE toolbar.




#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified edit tools value.
    $("#rteSample").ejRTE({ tools: {
            edit: ["findAndReplace"]         
            }    
    });
    </script>
{% endhighlight %}




### tools.doAction `array`
{:#members:tools-doaction}



Specifies the doAction tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea><script>
    // Initializes the RTE with the specified doAction tools value.
    $("#rteSample").ejRTE({ tools: {
            doAction: ["undo", "redo"]         
            }    
    });
    </script>
{% endhighlight %}



### tools.effects `array`
{:#members:tools-effects}




Specifies the effect of tools and the display order of this tool in RTE toolbar.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
// Initialize the RTE with the specified tools with effects value.
$("#rteSample").ejRTE({  tools: {
effects: ["superscript", "subscript"]
}});
</script>{% endhighlight %}



### tools.font `array`
{:#members:tools-font}




Specifies the font tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified font tools value.
    $("#rteSample").ejRTE({ tools: {
            font: ["fontName", "fontSize", "fontColor", "backgroundColor"]         
            }    
    });
    </script>
{% endhighlight %}



### tools.formatStyle `array`
{:#members:tools-formatstyle}



Specifies the formatStyle tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified formatStyle tools value.
    $("#rteSample").ejRTE({ tools: {
            formatStyle: ["format"]         
            }    
    });
    </script>
{% endhighlight %}




### tools.images `array`
{:#members:tools-images}


Specifies the image tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified image tools value.
    $("#rteSample").ejRTE({ tools: {
            images: ["image"]         
            }    
    });
    </script>
{% endhighlight %}




### tools.indenting `array`
{:#members:tools-indenting}


Specifies the indent tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified indent tools value.
    $("#rteSample").ejRTE({ tools: {
            indenting: ["outdent", "indent"]        
            }    
    });
    </script>
{% endhighlight %}




### tools.links `array`
{:#members:tools-links}


Specifies the link tools and the display order of this tool in the RTE toolbar.


#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified link tools value.
    $("#rteSample").ejRTE({ tools: {
            links: ["createLink","removeLink"]        
            }    
    });
    </script>
{% endhighlight %}




### tools.lists `array`
{:#members:tools-lists}



Specifies the list tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified list tools value.
    $("#rteSample").ejRTE({ tools: {
            lists: ["unorderedList", "orderedList"]        
            }    
    });
    </script>
{% endhighlight %}



### tools.media `array`
{:#members:tools-media}


Specifies the media tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified media tools value.
    $("#rteSample").ejRTE({ tools: {
            media: ["video"]
            }    
    });
    </script>
{% endhighlight %}




### tools.style `array`
{:#members:tools-style}



Specifies the style tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified style tools value.
    $("#rteSample").ejRTE({ tools: {
            style: ["bold", "italic", "underline", "strikethrough"]
            }    
    });
    </script>
{% endhighlight %}




### tools.tables `array`
{:#members:tools-tables}



Specifies the table tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified table tools value.
    $("#rteSample").ejRTE({ tools: {
            tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"]
            }    
    });
    </script>
{% endhighlight %}



### tools.view `array`
{:#members:tools-view}


Specifies the view tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified view tools value.
    $("#rteSample").ejRTE({ tools: {
            view: ["fullScreen","zoomIn","zoomOut"]
            }    
    });
    </script>
{% endhighlight %}



### tools.print `array`
{:#members:tools-print}


Specifies the print tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %}
 
 
<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified print tools value.
    $("#rteSample").ejRTE({ tools: {
            print: ["print"]
            }    
    });
    </script>
{% endhighlight %}

### tools.customOrderedList `array`
{:#members:tools-customOrderedList }


Specifies the customOrderedList tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customOrderedList tools value.
    $("#rteSample").ejRTE({ tools: {
            customOrderedList: [{
                        name: "orderedInsert",
                        tooltip: "Custom OrderedList",
                        css: "e-rte-toolbar-icon e-rte-listitems customOrdered",
	                    text: "Lower-Greek",
                        listStyle:"lower-greek"
                    }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customOrderedList.name `string`
{:#members:tools-customOrderedList-name }


Specifies the name for customOrderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customOrderedList name value.
    $("#rteSample").ejRTE({ tools: {
            customOrderedList: [{
                        name: "orderedInsert",
                        tooltip: "Custom OrderedList",
                        css: "e-rte-toolbar-icon e-rte-listitems customOrdered",
	                    text: "Lower-Greek",
                        listStyle:"lower-greek"
                    }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customOrderedList.tooltip `string`
{:#members:tools-customOrderedList-tooltip }


Specifies the title for customOrderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customOrderedList tooltip value.
    $("#rteSample").ejRTE({ tools: {
            customOrderedList: [{
                        name: "orderedInsert",
                        tooltip: "Custom OrderedList",
                        css: "e-rte-toolbar-icon e-rte-listitems customOrdered",
	                    text: "Lower-Greek",
                        listStyle:"lower-greek"
                    }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customOrderedList.css `string`
{:#members:tools-customOrderedList-css }


Specifies the styles for customOrderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customOrderedList css value.
    $("#rteSample").ejRTE({ tools: {
            customOrderedList: [{
                        name: "orderedInsert",
                        tooltip: "Custom OrderedList",
                        css: "e-rte-toolbar-icon e-rte-listitems customOrdered",
	                    text: "Lower-Greek",
                        listStyle:"lower-greek"
                    }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customOrderedList.text `string`
{:#members:tools-customOrderedList-text }


Specifies the text for customOrderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customOrderedList text value.
    $("#rteSample").ejRTE({ tools: {
            customOrderedList: [{
                        name: "orderedInsert",
                        tooltip: "Custom OrderedList",
                        css: "e-rte-toolbar-icon e-rte-listitems customOrdered",
	                    text: "Lower-Greek",
                        listStyle:"lower-greek"
                    }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customOrderedList.listStyle `string`
{:#members:tools-customOrderedList-listStyle }


Specifies the list style for customOrderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customOrderedList list style value.
    $("#rteSample").ejRTE({ tools: {
            customOrderedList: [{
                        name: "orderedInsert",
                        tooltip: "Custom OrderedList",
                        css: "e-rte-toolbar-icon e-rte-listitems customOrdered",
	                    text: "Lower-Greek",
                        listStyle:"lower-greek"
                    }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customOrderedList.listImage `string`
{:#members:tools-customOrderedList-listImage }


Specifies the image for customOrderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customOrderedList image value.
    $("#rteSample").ejRTE({ tools: {
            customOrderedList: [{
                        name: "orderInsert",
                        tooltip: "Custom OrderList",
                        css: "e-rte-toolbar-icon e-rte-listitems customOrder",
	                    text: "Lower-Greek",
                        listImage:"url('../content/images/rte/Smiley-GIF.gif')"                              
          }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customUnorderedList `array`
{:#members:tools-customUnorderedList }


Specifies the customUnOrderedList tools and the display order of this tool in the RTE toolbar.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customUnorderedList tools value.
    $("#rteSample").ejRTE({ tools: {
            customUnorderedList: [{
                        name: "unOrderedInsert",
                        tooltip: "Custom UnOrderedList",
                        css: "e-rte-toolbar-icon e-rte-unlistitems customUnOrdered",
	                    text: "Smiley",
                        listImage:"url('../content/images/rte/Smiley-GIF.gif')"                    
                 }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customUnorderedList.name `string`
{:#members:tools-customUnorderedList-name }


Specifies the name for customUnorderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customUnorderedList name value.
    $("#rteSample").ejRTE({ tools: {
                        customUnorderedList: [{
                        name: "UnorderedInsert",
                        tooltip: "Custom UnorderedList",
                        css: "e-rte-toolbar-icon e-rte-unlistitems customunOrdered",
	                    text: "Smiley",
                        listImage:"url('../content/images/rte/Smiley-GIF.gif')"                   
            }]    
            }    
    });
    </script>
{% endhighlight %}



### tools.customUnorderedList.tooltip `string`
{:#members:tools-customUnorderedList-tooltip }


Specifies the title for customUnorderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customUnorderedList tooltip value.
    $("#rteSample").ejRTE({ tools: {
              customUnorderedList: [{
                        name: "UnorderedInsert",
                        tooltip: "Custom UnorderedList",
                        css: "e-rte-toolbar-icon e-rte-unlistitems customUnordered",
	                    text: "Smiley",
                        listImage:"url('../content/images/rte/Smiley-GIF.gif')"                  
            }]           
        }    
    });
    </script>
{% endhighlight %}



### tools.customUnorderedList.css `string`
{:#members:tools-customUnorderedList-css }


Specifies the styles for customUnorderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customUnorderedList css value.
    $("#rteSample").ejRTE({ tools: {
            customUnorderedList: [{
                        name: "UnorderedInsert",
                        tooltip: "Custom UnorderedList",
                        css: "e-rte-toolbar-icon e-rte-unlistitems customUnordered",
	                    text: "Smiley",
                        listImage:"url('../content/images/rte/Smiley-GIF.gif')"                
            }]  
            }    
    });
    </script>
{% endhighlight %}



### tools.customUnorderedList.text `string`
{:#members:tools-customUnorderedList-text }


Specifies the text for customUnorderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customUnorderedList text value.
    $("#rteSample").ejRTE({ tools: {
          customUnorderedList: [{
                        name: "UnorderedInsert",
                        tooltip: "Custom UnorderedList",
                        css: "e-rte-toolbar-icon e-rte-unlistitems customUnordered",
	                    text: "Smiley",
                        listImage:"url('../content/images/rte/Smiley-GIF.gif')"           
            }]  
            }    
    });
    </script>
{% endhighlight %}



### tools.customUnorderedList.listStyle `string`
{:#members:tools-customUnorderedList-listStyle }


Specifies the list style for customUnorderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customUnorderedList list style value.
    $("#rteSample").ejRTE({ tools: {
          customUnorderedList: [{
                        name: "UnorderedInsert",
                        tooltip: "Custom UnorderedList",
                        css: "e-rte-toolbar-icon e-rte-unlistitems customUnordered",
	                    text: "Smiley",
                        listStyle:"circle"           
         }]
            }    
    });
    </script>
{% endhighlight %}



### tools.customUnorderedList.listImage `string`
{:#members:tools-customUnorderedList-listImage }


Specifies the image for customUnorderedList item.



#### Example



{% highlight html %} 


<textarea id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>
   <script>
    // Initializes the RTE with the specified customUnorderedList image value.
    $("#rteSample").ejRTE({ tools: {
            customUnorderedList: [{
                        name: "UnorderedInsert",
                        tooltip: "Custom UnorderedList",
                        css: "e-rte-toolbar-icon e-rte-unlistitems customUnordered",
	                    text: "Smiley",
                        listImage:"url('../content/images/rte/Smiley-GIF.gif')"           
            }]  
            }    
    });
    </script>
{% endhighlight %}




### toolsList `array`
{:#members:toolslist}


Specifies the list of groups and order of those groups displayed in the RTE toolbar.  The toolsList property is used to get the root group order and tools property is used to get the inner order of the corresponding groups displayed. When the value is not specified, it gets its default display order and tools.


#### Default Value




* ["formatStyle", "font", "style", "effects", "alignment", "lists", "indenting", "clipboard", "doAction", "clear", "links", "images", "media", "tables", "casing","view", "customTools","print","edit"]




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea > <script>
    // Initializes the RTE with the specified toolsList value.
    $("#rteSample").ejRTE({toolsList: ["formatStyle", "font", "style", "effects", "alignment", "lists", "indenting", "clipboard", "doAction", "clear", "links", "images", "media", "tables", "casing", "customTools","print"]
 });
</script>
{% endhighlight %}



### undoStackLimit `number`
{:#members:undostacklimit}


Gets the undo stack limit.


#### Default Value




* 50




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initializes the RTE with the specified 'undoStackLimit' value.
    $("#rteSample").ejRTE({ undoStackLimit: 70 });
</script>
{% endhighlight %}




### value `string`
{:#members:value}




The given string value is displayed in the editable area.


#### Default Value




* null




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
// Initializes the RTE with the value specified.
$("#rteSample").ejRTE({value: "The Rich Text Editor (RTE) control is an easy to render in client side. Customer easy to edit the contents, insert table, images and get the HTML content for the displayed content." });
</script>{% endhighlight %}



### validationRules  `object`
{:#members:validationrules}




Sets the jQuery validation rules to the Rich Text Editor.


#### Default Value




* null




#### Example


{% highlight html %}
 <textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in 
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<textarea   id="rteSample1">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in 
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea > <script>
    // Initializes the RTE with the specified ValidationRules.
     $("#rteSample").ejRTE({
         allowEditing: true,
         validationRules: {
                required: true,                
                minlength:15,
                maxlength: 150,
                minWordCount: 3,
                maxWordCount:50
         }});
         
        $("#rteSample1").ejRTE({
         allowEditing: true,
         validationRules: {
                equalTo: "#rteSample"
         }});
</script>
{% endhighlight %}



### validationMessage  `object`
{:#members:validationmessage}

Sets the jQuery validation error message to the Rich Text Editor. 


#### Default Value




* null




#### Example


{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in 
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea > <script>
    // Initializes the RTE with the specified ValidationRules and ValidationMessage.
     $("#rteSample").ejRTE({
         allowEditing: true,
         validationRules: {
                required: true,                
                minlength:15,
                maxlength: 150,
                minWordCount: 3,
                maxWordCount:50
         },
         validationMessage: {
                required: "Required RTE value",
                minlength:"Minimum content length not reached."
         }});         
</script>
{% endhighlight %}





### width `string`  `number`
{:#members:width}



Defines the width of the RTE textbox.


#### Default Value




* 786




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea > <script>
//Initializes the specified RTE width property value
        $("#rteSample").ejRTE({ width: 500 });
</script>{% endhighlight %}

### zoomStep `string`  `number`
{:#members:zoomStep}



Increases and decreases the contents zoom range in percentage


#### Default Value




* 0.05




#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea > <script>
//Initializes the specified RTE zoomStep property value
            $("#rteSample").ejRTE({tools: { view:[“zoomIn”,”zoomOut”]}, zoomStep: 0.1 });
</script>{% endhighlight %}


## Methods


### createRange()
{:#methods:createRange}


Returns the range object.


#### Example



{% highlight html %}
 
<textarea   id="rteSample">                    
    <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.createRange(); //Returns the range object
</script>
{% endhighlight %}

### disable()
{:#methods:disable}





Disables the RTE control.



#### Example



{% highlight html %}
<textarea   id="rteSample">
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.disable(); // Disables the RTE
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("disable");// Disables the RTE
</script>{% endhighlight %}




### disableToolbarItem()
{:#methods:disabletoolbaritem}


Disables the corresponding tool in the RTE ToolBar.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea ><script>
    $("#rteSample").ejRTE();
        // Creates the RTE.
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.disableToolbarItem("createTable"); // Disables toolbar item.
</script>Note: Those using the release version before 13.3, please refer to the following<script>
    $("#rteSample").ejRTE();
  // Creates the RTE.
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.disableToolbarItem("rteSample createTable"); // Disables toolbar item.
</script>
{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea ><script>
    $("#rteSample").ejRTE();
    // Creates the RTE.
    $("#rteSample").ejRTE("disableToolbarItem", "createTable"); // Disables toolbar item        
</script>Note: Those using the release version before 13.3, please refer to the following<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    $("#rteSample").ejRTE("disableToolbarItem", "rteSamplecreateTable"); // Disables toolbar item
</script>
{% endhighlight %}




### enable()
{:#methods:enable}


Enables the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">
     <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
$("#rteSample").ejRTE();
// Creates the RTE.
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.enable(); // Enables RTE
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("enable");// Enables RTE
</script>{% endhighlight %}




### enableToolbarItem()
{:#methods:enabletoolbaritem}



Enables the corresponding tool in the toolbar when the tool is disabled.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                   
     <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.enableToolbarItem("createTable"); // Enables toolbar item
</script>

Note: When using the release version before 13.3, refer to the following.
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.enableToolbarItem("rteSamplecreateTable"); // Enables toolbar item
</script>
{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    $("#rteSample").ejRTE("enableToolbarItem", "createTable"); // Enables toolbar item        
</script>
Note: When you are using our release version before 13.3, refer to the following
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    $("#rteSample").ejRTE("enableToolbarItem", " rteSamplecreateTable "); // Enables toolbar item        
</script>
{% endhighlight %}




### executeCommand()
{:#methods:executecommand}



Performs the action value based on the given command. 



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                    
    <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.executeCommand("bold", true); // Gets the content as string from rte
</script>{% endhighlight %}




### focus()
{:#methods:focus}



Focuses the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                      
  <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.focus(); // Focuses the RTE.
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("focus");// Focuses the RTE.    
</script>{% endhighlight %}




### getCommandStatus()
{:#methods:getcommandstatus}



Gets the command status of the selected text based on the given comment in the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                   
 <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.getCommandStatus(("bold");  // Gets the bold status form selected text in RTE.
</script>{% endhighlight %}


### getDocument()
{:#methods:getDocument}


Gets the HTML string from the RTE control.


#### Example



{% highlight html %}
 
<textarea   id="rteSample">                    
    <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.getDocument(); // Gets the HTML string from the RTE.
</script>
{% endhighlight %}


### getHtml()
{:#methods:gethtml}



Gets the HTML string from the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                       
 <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.getHtml(); // Gets the html string from the rte.
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("getHtml");// Gets the html string from the rte.       
</script>{% endhighlight %}




### getSelectedHtml()
{:#methods:getselectedhtml}



Gets the selected HTML string from the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.getSelectedHtml(); // Gets the content as string from rte
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("getSelectedHtml");// GetSelectedHtml from rte        
</script>{% endhighlight %}




### getText()
{:#methods:gettext}


Gets the content as string from the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                      
  <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE.
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.getText(); // Gets the content as string from the RTE.
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("getText");// getText from rte        
</script>{% endhighlight %}




### hide()
{:#methods:hide}



Hides the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                        
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.hide(); // Hides the rte
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("hide");// Hides the rte       
</script>{% endhighlight %}




### insertMenuOption()
{:#methods:insertMenuOption}



Inserts new item to the target contextmenu node. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
option </td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">
Object data’s for inserting the new item to the context menu.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
newItem </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">
Target menu item text.
</td>
</tr>
<tr>
<td class="name">
targetItem </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">
Target menu item text
</td>
</tr>
<tr>
<td class="name">
insertType </td>
<td class="type"><span class="param-type">string </span></td>
<td class="description">
Menu item insertion type - insert||insertAfter||insertBefore”.
</td>
</tr>
<tr>
<td class="name">
menuType </td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">
menu visibility types.
-	 text:boolean, image: boolean, hyperlink: boolean, table: boolean 

</td>
</tr>
<tr>
<td class="name">
spriteCssClass </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">
Sprite CSS class name for menu item icon.
</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example



{% highlight html %}
 
<textarea   id="rteSample">                        
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");// Inserts new item to the contextmenu
rteeObj.insertMenuOption({newItem:"Show Table Details",targetItem:"Table Properties", insertType:("insertAfter"), menuType:{text:false,image:false,hyperlink:false,table:true},spriteCssClass:"e-rte-toolbar-icon tableProperties"}); 
</script>
{% endhighlight %}



### pasteContent()
{:#methods:pasteContent}


This method helps to insert/paste the content at the current cursor (caret) position or the selected content to be replaced with our text by passing the value as parameter to the pasteContent method in the Editor.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                    
    <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.pasteContent("place the content in current cursor position/replace the selected text "); 
</script>
{% endhighlight %}



### refresh()
{:#methods:refresh}



Refreshes the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                    
    <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.refresh(); // Refreshes the rte
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("refresh");// Refreshes the rte       
</script>{% endhighlight %}


### removeMenuOption ()
{:#methods:removeMenuOption}




Removes the target menu item from the RTE contextmenu.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
option </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">
Target Node text.
</td>
</tr>
</tbody>
</table>

#### Example



{% highlight html %}
 
<textarea   id="rteSample">                 
       <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.removeMenuOption("Target"); 
</script>
{% endhighlight %}


### removeToolbarItem()
{:#methods:removetoolbaritem}




Removes the given tool from the RTE Toolbar.


#### Example



{% highlight html %}
 
<textarea   id="rteSample">                 
       <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.removeToolbarItem("createTable"); // Removes the toolbar item
</script>
Note: When you use the release version before 13.3, refer to the following
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.removeToolbarItem("rteSamplecreateTable"); // Removes toolbar item
</script>
{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    $("#rteSample").ejRTE("removeToolbarItem", "createTable"); // Removes the toolbar item        
</script>
Note: When using the release version before 13.3, refer to the following

<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    $("#rteSample").ejRTE("removeToolbarItem", "rteSamplecreateTable"); // Remove the toolbar item        
</script>
{% endhighlight %}




### selectAll()
{:#methods:selectAll}


Selects all the contents within the RTE.


#### Example



{% highlight html %}
 
<textarea   id="rteSample">                    
    <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    rteeObj.selectAll(); 
</script>
{% endhighlight %}


### selectRange()
{:#methods:selectRange}


Selects the contents in the given range.


#### Example



{% highlight html %}
 
<textarea   id="rteSample">                    
    <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
    $("#rteSample").ejRTE();
    // Creates the RTE
    var rteeObj = $("#rteSample").data("ejRTE");
    var range = rteeObj.createRange();
    var tag = rteeObj.getDocument().getElementsByTagName("p");           
    if (!editor._isIE8()) {
        range.setStart(tag[0], 0);
        range.setEnd(tag[1], 1);
    }
    else {
       range = editor.getDocument().body.createTextRange()
       range.moveToElementText(tag[1]);
    }
    range.selectRange(range);
</script>
{% endhighlight %}


### setColorPickerType()
{:#methods:setcolorpickertype}



Sets the color picker model type rendered initially in the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                       
 <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.setColorPickerType("picker"); // Sets the picker mode
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("setColorPickerType","picker");// Sets the picker mode        
</script>{% endhighlight %}




### setHtml()
{:#methods:sethtml}



Sets the HTML string from the RTE control.



#### Example



{% highlight html %}
 
<textarea   id="rteSample">                     
  </textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.setHtml("The Rich Text Editor (RTE) control is an easy to render in client side."); // Sets the html string to the rte
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("setHtml","The Rich Text Editor (RTE) control is an easy to render in client side.");// sets the html string to the rte    
</script>{% endhighlight %}




### show()
{:#methods:show}

Displays the RTE control.


#### Example



{% highlight html %}
 
<textarea   id="rteSample">                    
    <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.show(); // Shows the rte
</script>{% endhighlight %}


{% highlight html %}
 
<textarea   id="rteSample">          
<p><b>Description:</b></p>
<p>The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. </p></textarea >
<script>
$("#rteSample").ejRTE();
// Creates the RTE
$("#rteSample").ejRTE("show");// Shows the rte       
</script>{% endhighlight %}


## Events

### change
{:#events:change}

Fires when changed successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the RTE model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//changes the event for RTE
$("#rteSample").ejRTE({ 
        change: function(args) {}
});      
</script>{% endhighlight %}



### create
{:#events:create}

Fires when the RTE is created successfully

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the RTE model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//creates an event for RTE
$("#rteSample").ejRTE({ 
        create: function(args) {}
});      
</script>{% endhighlight %}


### contextMenuClick  
{:#events:contextMenuClick  }

Fires when mouse click on menu items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns clicked menu item text.</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">returns clicked menu item element.</td>
</tr>
<tr>
<td class="name">
selectedItem</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the selected item.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//contextMenuClick event for RTE
$("#rteSample").ejRTE({ 
        contextMenuClick: function(args) {
            
        }
});
   
</script>{% endhighlight %}

### destroy
{:#events:destroy}

Fires before the RTE is destroyed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the RTE model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//Executes the event for RTE
$("#rteSample").ejRTE({ 
        destroy: function(args) {}
});   
</script>   
{% endhighlight %}


### execute
{:#events:execute}

Fires when the commands are executed successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the RTE model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//Executes the event for RTE
$("#rteSample").ejRTE({ 
        execute: function(args) {}
});   
</script>   {% endhighlight %}


### keydown
{:#events:keydown}

Fires when the keydown action is successful.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the RTE model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//keydown event for RTE
$("#rteSample").ejRTE({ 
        keydown: function(args) {}
});  
</script>    {% endhighlight %}

### keyup
{:#events:keyup}

Fires when the keyup action is successful.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the RTE model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//keyup event for RTE
$("#rteSample").ejRTE({ 
        keyup: function(args) {}
});  
</script>    {% endhighlight %}


### preRender
{:#events:preRender}

Fires before the RTE Edit area is rendered and after the toolbar is rendered.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the RTE model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//preRender event for RTE
$("#rteSample").ejRTE({ 
        preRender: function(args) {}
});   
</script>   {% endhighlight %}

### select
{:#events:select}

Fires when the text is selected in the text area

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the RTE model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the event object</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea >     
<script>
$("#rteSample").ejRTE();
//select event for RTE
$("#rteSample").ejRTE({ 
        select: function(args) {}
});   
</script>   

{% endhighlight %}






