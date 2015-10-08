---
layout: post
title: ejRTE
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html TextArea control.





$(element).ejRTE<span class="signature">(options)</span>




<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for RTE.</td>
</tr>
</tbody>
</table>

Example:
{:.example}

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


Requires
{:.require}


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



### allowEditing<span class="type-signature type boolean">boolean</span>
{:#members:allowediting}

Enables/disables the editing of the content.


Default Value:
{:.param}



* True




Example
{:.example}


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

### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members:allowkeyboardnavigation}





RTE control can be accessed through the keyboard shortcut keys.


Default Value:
{:.param}



* True




Example
{:.example}


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




### autoFocus <span class="type-signature type boolean">boolean</span>
{:#members:autoFocus }




When the property is set to true, it focuses the RTE at the time of rendering.


Default Value:
{:.param}



* false




Example
{:.example}


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




### autoHeight <span class="type-signature type boolean">boolean</span>
{:#members:autoHeight }




Based on the content size, its height is adjusted instead of adding the scrollbar.


Default Value:
{:.param}



* false




Example
{:.example}


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




### colorCode<span class="type-signature type object">object</span>
{:#members:colorcode}





Sets the colorCode to display the color of the fontColor and backgroundColor in the font tools of the RTE.


Default Value:
{:.param}



* ["000000", "FFFFFF", "C4C4C4", "ADADAD", "595959", "262626", "4f81bd", "dbe5f1", "b8cce4", "95b3d7", "366092", "244061", "c0504d", "f2dcdb", "e5b9b7", "d99694", "953734",
"632423", "9bbb59", "ebf1dd", "d7e3bc", "c3d69b", "76923c", "4f6128", "8064a2", "e5e0ec", "ccc1d9", "b2a2c7", "5f497a", "3f3151", "f79646", "fdeada", "fbd5b5", "fac08f","e36c09", "974806"]





Example
{:.example}


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




### colorPaletteColumns<span class="type-signature type number">number</span>
{:#members:colorpalettecolumns}




The number of columns given are rendered in the color palate popup.


Default Value:
{:.param}



* 6




Example
{:.example}


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




### colorPaletteRows<span class="type-signature type number">number</span>
{:#members:colorpaletterows}



The number of rows given are rendered in the color palate popup.


Default Value:
{:.param}



* 6




Example
{:.example}


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




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Sets the root class for the RTE theme. This cssClass API helps the usage of custom skinning option for the RTE control by including this root class in CSS.

Default Value:
{:.param}



* ""




Example
{:.example}


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




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}





Enables/disables the RTE control’s accessibility or interaction.


Default Value:
{:.param}



* True




Example
{:.example}


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




### enableHtmlEncode <span class="type-signature type boolean">boolean</span>
{:#members:enableHtmlEncode }





When the property is set to true, it returns the encrypted text.


Default Value:
{:.param}



* false




Example
{:.example}


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




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Maintain the values of the RTE after page reload.


Default Value:
{:.param}



* false




Example
{:.example}


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




### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}





Shows the resize icon and enables the resize option in the RTE.


Default Value:
{:.param}



* True




Example
{:.example}


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




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Shows the RTE in the RTL direction.


Default Value:
{:.param}



* false




Example
{:.example}


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




### enableXHTML<span class="type-signature type boolean">boolean</span>
{:#members:enablexhtml}





Formats the contents based on the XHTML rules.


Default Value:
{:.param}



* false




Example
{:.example}


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




### fileBrowser<span class="type-signature type object">object</span>
{:#members:filebrowser}





This API allows to enable the file browser support in the RTE control to browse, create, delete and upload the files in the specified current directory.


Default Value:
{:.param}



* null




Example
{:.example}


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




### fileBrowser.ajaxAction<span class="type-signature type string">string</span>
{:#members:filebrowser-ajaxaction}




This API is used to receive the server-side handler for file related operations.


Default Value:
{:.param}



* ""




Example
{:.example}


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




### fileBrowser.extensionAllow<span class="type-signature type string">string</span>
{:#members:filebrowser-extensionallow}




Specifies the file type extension shown in the file browser window.



Example
{:.example}


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




### fileBrowser.filePath<span class="type-signature type string">string</span>
{:#members:filebrowser-filepath}


Specifies the directory to perform operations like create, delete and rename folder and files, and upload the selected files to the current directory.



Example
{:.#example}


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



### fontName<span class="type-signature type object">object</span>
{:#members:fontname}



Sets the fontName in the RTE.


Default Value:
{:.param}



* {text: "Segoe UI", value: "Segoe UI" },
{text: "Arial", value: "Arial,Helvetica,sans-serif" },
{text: "Courier New", value: "Courier New,Courier,monospace" },
{text: "Georgia", value: "Georgia,serif" },
{text: "Impact", value: "Impact,Charcoal,sans-serif" },
{text: "Lucida Console", value: "Lucida Console,Monaco,monospace" },
{text: "Tahoma", value: "Tahoma,Geneva,sans-serif" },
{text: "Times New Roman", value: "Times New Roman" },
{text: "Trebuchet MS", value: "Trebuchet MS,Helvetica,sans-serif" }, 
{text: "Verdana", value: "Verdana,Geneva,sans-serif"}





Example
{:.#example}


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



### fontSize<span class="type-signature type object">object</span>
{:#members:fontsize}




Sets the fontSize in the RTE.


Default Value:
{:.param}



* { text: "1", value: "1" },
{ text: "2 (10pt)", value: "2" },
{ text: "3 (12pt)", value: "3" },
{ text: "4 (14pt)", value: "4" },
{ text: "5 (18pt)", value: "5" },
{ text: "6 (24pt)", value: "6" },
{ text: "7 (36pt)", value: "7" }




Example
{:#example:}


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




### format<span class="type-signature type string">string</span>
{:#members:format}





Sets the format in the RTE.


Default Value:
{:.param}



* { text: "Paragraph", value: "&lt;p&gt;", spriteCssClass: "e-paragraph" },
{ text: "Quotation", value: "&lt;blockquote&gt;", spriteCssClass: "e-quotation" },
{ text: "Heading 1", value: "&lt;h1&gt;", spriteCssClass: "e-h1" },
{ text: "Heading 2", value: "&lt;h2&gt;", spriteCssClass: "e-h2" },
{ text: "Heading 3", value: "&lt;h3&gt;", spriteCssClass: "e-h3" },
{ text: "Heading 4", value: "&lt;h4&gt;", spriteCssClass: "e-h4" },
{ text: "Heading 5", value: "&lt;h5&gt;", spriteCssClass: "e-h5" },
{ text: "Heading 6", value: "&lt;h6&gt;", spriteCssClass: "e-h6"}





Example
{:.example}


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


### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:height}





Defines the height of the RTE textbox.


Default Value:
{:.param}



* 370




Example
{:#example:}


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




### htmlAttributes<span class="type-signature type object">object</span>
{:#members:htmlattributes}





Specifies the HTML Attributes of the ejRTE.


Default Value:
{:.param}



* {}




Example
{:.example}


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




### iframeAttribute<span class="type-signature type string">object</span>
{:#members:iframeattribute}





Sets the given attributes to the iframe body element.


Default Value:
{:.param}



* {}




Example
{:.example}


{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea ><script>
    // Initialize the RTE with the specified iframeAttribute value .
    $("#rteSample").ejRTE({ iframeAttribute:{ style :"color:#5C5C5C" }});
</script>
{% endhighlight %}




### imageBrowser<span class="type-signature type object">object</span>
{:#members:imagebrowser}





This API allows the image browser to support in the RTE control to browse, create, delete, and upload the image files to the specified current directory.


Default Value:
{:.param}



* null




Example
{:.example}


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




### imageBrowser.ajaxAction<span class="type-signature type string">string</span>
{:#members:imagebrowser-ajaxaction}





This API is used to receive the server-side handler for the file related operations.



Example
{:.example}


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




### imageBrowser.extensionAllow<span class="type-signature type string">string</span>
{:#members:imagebrowser-extensionallow}





Specifies the file type extension shown in the image browser window.



Example
{:.example}


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




### imageBrowser.filePath<span class="type-signature type string">string</span>
{:#members:imagebrowser-filepath}





Specifies the directory to perform operations like create, delete and rename folder and files, and upload the selected images to the current directory.



Example
{:.example}


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




### isResponsive<span class="type-signature type boolean">boolean</span>
{:#members:isresponsive}





Enables/disables responsive support for the RTE control toolbar items during the window resizing time.


Default Value:
{:.param}



* false




Example
{:.example}


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




### locale<span class="type-signature type string">string</span>
{:#members:locale}





Sets the culture in the RTE when you set the localization values are needs to be assigned to the corresponding text as follows.  


Default Value:
{:.param}



* "en-US"




Example
{:.example}


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




### maxHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:maxheight}




Sets the maximum height for the RTE outer wrapper element.


Default Value:
{:.param}



* null




Example
{:.example}


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




### maxLength<span class="type-signature type number">number</span>
{:#members:maxlength}




Sets the maximum length for the RTE outer wrapper element.


Default Value:
{:.param}



* 7000




Example
{:.example}


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




### maxWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:maxwidth}





Sets the maximum width for the RTE outer wrapper element.


Default Value:
{:.param}



* null




Example
{:.example}


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




### minHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:minheight}





Sets the minimum height for the RTE outer wrapper element.


Default Value:
{:.param}



* 280




Example
{:.example}


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




### minWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:minwidth}




Sets the minimum width for the RTE outer wrapper element.


Default Value:
{:.param}



* 400




Example
{:.example}


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




### name<span class="type-signature type string">string</span>
{:#members:name}





Sets the name in the RTE. When the name value is not initialized, the ID value is assigned to the name.


Default Value:
{:.param}



* ""




Example
{:.example}


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




### showClearAll<span class="type-signature type boolean">boolean</span>
{:#members:showclearall}





Shows ClearAll icon in the RTE footer.


Default Value:
{:.param}



* false




Example
{:.example}


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




### showClearFormat<span class="type-signature type boolean">boolean</span>
{:#members:showclearformat}





Shows the clear format in the RTE footer.


Default Value:
{:.param}



* true




Example
{:.example}


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




### showCustomTable<span class="type-signature type boolean">boolean</span>
{:#members:showcustomtable}




Shows the Custom Table in the RTE.


Default Value:
{:.param}



* True




Example
{:.example}


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




### showDimensions<span class="type-signature type boolean">boolean</span>
{:#members:showdimensions}





This API is used to set the default dimensions for the image and video. When this property is set to true, the image and video dialog displays the dimension option.


Default Value:
{:.param}



* false




Example
{:.example}


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




### showFontOption<span class="type-signature type boolean">boolean</span>
{:#members:showfontoption}




Shows the FontOption in the RTE.


Default Value:
{:.param}



* True




Example
{:.example}


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




### showFooter<span class="type-signature type boolean">boolean</span>
{:#members:showfooter}





Shows footer in the RTE. When the footer is enabled, it displays the html tag, word Count, character count, clear format, resize icon and clear all the content icons, by default.


Default Value:
{:.param}



* false




Example
{:.example}


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




### showHtmlSource<span class="type-signature type boolean">boolean</span>
{:#members:showhtmlsource}




Shows the HtmlSource in the RTE footer.


Default Value:
{:.param}



* false




Example
{:.example}


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




### showHtmlTagInfo<span class="type-signature type boolean">boolean</span>
{:#members:showhtmltaginfo}




When the cursor is placed or when the text is selected in the RTE, it displays the tag info in the footer.


Default Value:
{:.param}



* True




Example
{:.example}


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




### showToolbar<span class="type-signature type boolean">boolean</span>
{:#members:showtoolbar}




Shows the toolbar in the RTE.


Default Value:
{:.param}



* True




Example
{:.example}


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




### showCharCount<span class="type-signature type boolean">boolean</span>
{:#members:showCharCount }


Counts the total characters and displays it in the RTE footer.


Default Value:
{:.param}



* True




Example
{:.example}


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







### showWordCount <span class="type-signature type boolean">boolean</span>
{:#members:showWordCount  }




Counts the total words and displays it in the RTE footer.


Default Value:
{:.param}



* True




Example
{:.example}


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




### tableColumns<span class="type-signature type number">number</span>
{:#members:tablecolumns}





The given number of columns render the insert table pop.


Default Value:
{:.param}



* 10




Example
{:.example}


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




### tableRows<span class="type-signature type number">number</span>
{:#members:tablerows}




The given number of rows render the insert table pop.


Default Value:
{:.param}



* 8




Example
{:.example}


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




### tools<span class="type-signature type object">object</span>
{:#members:tools}




Sets the tools in the RTE and gets the inner display order of the corresponding group element. Tools are dependent on the toolsList property. 


Default Value:
{:.param}



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
view:[“fullScreen”]





Example
{:.example}


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
                view:[“fullScreen”]
                view: ["fullScreen"],
                casing:["upperCase", "lowerCase"],
                tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"]
            }   
    });
    </script>
{% endhighlight %}




### tools.alignment<span class="type-signature type object">Object</span>
{:#members:tools-alignment}



Specifies the alignment tools and the display order of this tool in the RTE toolbar.




Example
{:.example}


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




### tools.casing <span class="type-signature type object">Object</span>
{:#members:tools-casing }



Specifies the casing tools and the display order of this tool in the RTE toolbar.




Example
{:.example}


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




### tools.clear  <span class="type-signature type object">Object</span>
{:#members:tools-clear  }



Specifies the clear tools and the display order of this tool in the RTE toolbar.




Example
{:.example}


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




### tools.clipboard<span class="type-signature type object">Object</span>
{:#members:tools-clipboard}




Specifies the clipboard tools and the display order of this tool in the RTE toolbar.




Example
{:.example}


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




### tools.doAction<span class="type-signature type object">Object</span>
{:#members:tools-doaction}



Specifies the doAction tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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



### tools.effects<span class="type-signature type object">Object</span>
{:#members:tools-effects}




Specifies the effect of tools and the display order of this tool in RTE toolbar.



Example
{:.example}


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



### tools.font<span class="type-signature type object">Object</span>
{:#members:tools-font}




Specifies the font tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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



### tools.formatStyle<span class="type-signature type object">Object</span>
{:#members:tools-formatstyle}



Specifies the formatStyle tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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




### tools.images<span class="type-signature type object">Object</span>
{:#members:tools-images}


Specifies the image tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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




### tools.indenting<span class="type-signature type object">Object</span>
{:#members:tools-indenting}


Specifies the indent tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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




### tools.links<span class="type-signature type object">Object</span>
{:#members:tools-links}


Specifies the link tools and the display order of this tool in the RTE toolbar.


Example
{:.example}


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




### tools.lists<span class="type-signature type object">Object</span>
{:#members:tools-lists}



Specifies the list tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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



### tools.media<span class="type-signature type object">Object</span>
{:#members:tools-media}


Specifies the media tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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




### tools.style<span class="type-signature type object">Object</span>
{:#members:tools-style}



Specifies the style tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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




### tools.tables<span class="type-signature type object">Object</span>
{:#members:tools-tables}



Specifies the table tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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



### tools.view<span class="type-signature type object">Object</span>
{:#members:tools-view}


Specifies the view tools and the display order of this tool in the RTE toolbar.



Example
{:.example}


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
            view: ["fullScreen"]
            }    
    });
    </script>
{% endhighlight %}




### toolsList<span class="type-signature type object">object</span>
{:#members:toolslist}


Specifies the list of groups and order of those groups displayed in the RTE toolbar.  The toolsList property is used to get the root group order and tools property is used to get the inner order of the corresponding groups displayed. When the value is not specified, it gets its default display order and tools.


Default Value:
{:.param}



* ["formatStyle", "font", "style", "effects", "alignment", "lists", "indenting", "clipboard", "doAction", "clear", "links", "images", "media", "tables", "casing","view", "customTools"]




Example
{:.example}


{% highlight html %}
 
<textarea   id="rteSample">     
<p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea > <script>
    // Initializes the RTE with the specified toolsList value.
    $("#rteSample").ejRTE({toolsList: ["formatStyle", "font", "style", "effects", "alignment", "lists", "indenting", "clipboard", "doAction", "clear", "links", "images", "media", "tables", "casing", "customTools"]
 });
</script>
{% endhighlight %}



### undoStackLimit<span class="type-signature type number">number</span>
{:#members:undostacklimit}


Gets the undo stack limit.


Default Value:
{:.param}



* 50




Example
{:.example}


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




### value<span class="type-signature type string">string</span>
{:#members:value}




The given string value is displayed in the editable area.


Default Value:
{:.param}



* null




Example
{:.example}


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




### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}



Defines the width of the RTE textbox.


Default Value:
{:.param}



* 786




Example
{:.example}


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



## Methods


### createRange<span class="signature">()</span>
{:#methods:createRange}


Returns the range object.


Example
{:.example}


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

### disable<span class="signature">()</span>
{:#methods:disable}





Disables the RTE control.



Example
{:.example}


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




### disableToolbarItem<span class="signature">()</span>
{:#methods:disabletoolbaritem}


Disables the corresponding tool in the RTE ToolBar.



Example
{:.example}


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




### enable<span class="signature">()</span>
{:#methods:enable}


Enables the RTE control.



Example
{:.example}


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




### enableToolbarItem<span class="signature">()</span>
{:#methods:enabletoolbaritem}



Enables the corresponding tool in the toolbar when the tool is disabled.



Example
{:.example}


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




### executeCommand<span class="signature">()</span>
{:#methods:executecommand}



Performs the action value based on the given command. 



Example
{:.example}


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




### focus<span class="signature">()</span>
{:#methods:focus}



Focuses the RTE control.



Example
{:.example}


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




### getCommandStatus<span class="signature">()</span>
{:#methods:getcommandstatus}



Gets the command status of the selected text based on the given comment in the RTE control.



Example
{:.example}


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


### getDocument<span class="signature">()</span>
{:#methods:getDocument}


Gets the HTML string from the RTE control.


Example
{:.example}


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


### getHtml<span class="signature">()</span>
{:#methods:gethtml}



Gets the HTML string from the RTE control.



Example
{:.example}


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




### getSelectedHtml<span class="signature">()</span>
{:#methods:getselectedhtml}



Gets the selected html string from the RTE control.



Example
{:.example}


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




### getText<span class="signature">()</span>
{:#methods:gettext}


Gets the content as string from the RTE control.



Example
{:.example}


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




### hide<span class="signature">()</span>
{:#methods:hide}



Hides the RTE control.



Example
{:.example}


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

### pasteContent<span class="signature">()</span>
{:#methods:pasteContent}


This method helps to insert/paste the content at the current cursor (caret) position or the selected content to be replaced with our text by passing the value as parameter to the pasteContent method in the Editor.



Example
{:.example}


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



### refresh<span class="signature">()</span>
{:#methods:refresh}



Refreshes the RTE control.



Example
{:.example}


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




### removeToolbarItem<span class="signature">()</span>
{:#methods:removetoolbaritem}




Removes the given tool from the RTE ToolBbar.


Example
{:.example}


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




### selectAll<span class="signature">()</span>
{:#methods:selectAll}


Selects all the contents within the RTE.


Example
{:.example}


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


### selectRange<span class="signature">()</span>
{:#methods:selectRange}


Selects the contents in the given range.


Example
{:.example}


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


### setColorPickerType<span class="signature">()</span>
{:#methods:setcolorpickertype}



Sets the colorpicker model type rendered initially in the RTE control.



Example
{:.example}


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




### setHtml<span class="signature">()</span>
{:#methods:sethtml}



Sets the HTML string from the RTE control.



Example
{:.example}


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




### show<span class="signature">()</span>
{:#methods:show}

Displays the RTE control.


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the RTE model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the RTE model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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



### destroy
{:#events:destroy}




Fires before the RTE is destroyed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the RTE model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the RTE model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the RTE model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the RTE model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">When the event is canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the RTE model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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






