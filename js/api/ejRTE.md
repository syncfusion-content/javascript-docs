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
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for RTE.</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;       
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
            &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Create RTE
$("#rteSample").ejRTE();
&lt;/script&gt;</code>
</pre>



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


## Members




### allowEditing<span class="type-signature type boolean">boolean</span>
{:#members:allowediting}




Enables/Disables the editing of the content.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;  
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the allowEditing value specified.
$("#rteSample").ejRTE({ allowEditing: false });
&lt;/script&gt;</code>
</pre>



### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members:allowkeyboardnavigation}




RTE control comments can access through keyboard shortcut keys.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the allowKeyboardNavigation value specified.
$("#rteSample").ejRTE({allowKeyboardNavigation: false });
&lt;/script&gt;</code>
</pre>



### colorCode<span class="type-signature type object">object</span>
{:#members:colorcode}




Sets the colorCode in RTE.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the colorCode value specified.
$("#rteSample").ejRTE({ colorCode: [
                                    "000000", "FFFFFF", "C4C4C4", "ADADAD", "595959", "262626", "4f81bd", "dbe5f1", "b8cce4", "95b3d7", "366092", "244061", "c0504d", "f2dcdb", "e5b9b7", "d99694", "953734",
                                    "632423", "9bbb59", "ebf1dd", "d7e3bc", "c3d69b", "76923c", "4f6128", "8064a2", "e5e0ec", "ccc1d9", "b2a2c7", "5f497a", "3f3151", "f79646", "fdeada", "fbd5b5", "fac08f",
                                    "e36c09", "974806"
            ]});
&lt;/script&gt;</code>
</pre>



### colorPaletteColumns<span class="type-signature type number">number</span>
{:#members:colorpalettecolumns}




Given number for columns render the color palete pop up.


Default Value:
{:.param}



* 6




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the 'colorPaletteColumns' value specified.
$("#rteSample").ejRTE({colorPaletteColumns: 70 });
&lt;/script&gt;</code>
</pre>



### colorPaletteRows<span class="type-signature type number">number</span>
{:#members:colorpaletterows}




Given number for rows render the color palete pop up.


Default Value:
{:.param}



* 6




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the 'colorPaletteRows' value specified.
$("#rteSample").ejRTE({colorPaletteRows: 70 });
&lt;/script&gt;</code>
</pre>



### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Sets the root class for RTE theme. This cssClass API helps to use custom skinning option for RTE control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
//Initialize the RTE with the cssClass value specified
        $("#rteSample").ejRTE({ cssClass: 'gradient-lime'});
&lt;/script&gt;</code>
</pre>



### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




Enable | Disable the RTE control accessible or interaction..


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the enabled value specified.
$("#rteSample").ejRTE({enabled: false });
&lt;/script&gt;</code>
</pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




enablePersistence the values in RTE.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the enablePersistence value specified.
$("#rteSample").ejRTE({enablePersistence: false });
&lt;/script&gt;</code>
</pre>



### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}




Shows enableResize in RTE.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the enableResize value specified.
$("#rteSample").ejRTE({enableResize: false });
&lt;/script&gt;</code>
</pre>



### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




shows enableRTL in RTE.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the enableRTL value specified.
$("#rteSample").ejRTE({enableRTL: true });
&lt;/script&gt;</code>
</pre>



### enableXHTML<span class="type-signature type boolean">boolean</span>
{:#members:enablexhtml}




Enable | Disable the RTE control exporting Xhtml


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the enableXHTML value specified.
$("#rteSample").ejRTE({enableXHTML: true });
&lt;/script&gt;</code>
</pre>



### fileBrowser<span class="type-signature type object">object</span>
{:#members:filebrowser}




This API allows to enable the file browser support in RTE control to browse, create delete and upload the files in specified current directory.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the fileBrowser value specified.
$("#rteSample").ejRTE({  fileBrowser: {
  filePath: "../FileExplorerContent/",
 extensionAllow: "*.png, *.doc, *.pdf, *.txt, *.docx",
ajaxAction: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/",
}});
&lt;/script&gt;</code>
</pre>



### fileBrowser.ajaxAction<span class="type-signature type string">string</span>
{:#members:filebrowser-ajaxaction}




This API is used to receive the server side handler for file related operations.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the fileBrowser value specified.
$("#rteSample").ejRTE({  fileBrowser: {
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction"
}});
&lt;/script&gt;</code>
</pre>



### fileBrowser.extensionAllow<span class="type-signature type string">string</span>
{:#members:filebrowser-extensionallow}




To specify the file type extension to be shown in image browser window.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the fileBrowser value specified.
$("#rteSample").ejRTE({  fileBrowser: {
extensionAllow: "*.doc,*.docx,*.pdf,*.txt"
}});
&lt;/script&gt;</code>
</pre>



### fileBrowser.filePath<span class="type-signature type string">string</span>
{:#members:filebrowser-filepath}




Specify the directory to perform the operation like create, delete and rename folder &amp; files, upload the selected files to the current directory..



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the fileBrowser value specified.r
$("#rteSample").ejRTE({  fileBrowser: {
 filePath: "../FileExplorerContent/"
}});
&lt;/script&gt;</code>
</pre>



### fontName<span class="type-signature type object">object</span>
{:#members:fontname}




Sets the fontName in RTE.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the fontName value specified.
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
&lt;/script&gt;
                
</code>
</pre>




### fontSize<span class="type-signature type object">object</span>
{:#members:fontSize}



Sets the fontSize in RTE.


Default Value:
{:.param}



* null




Example
{:#example:}

<pre class="prettyprint">
<code><code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the fontSize value specified.
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
&lt;/script&gt; </code></code>
</pre>



### format<span class="type-signature type string">string</span>
{:#members:format}




Sets the format in RTE.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the format value specified.
$("#rteSample").ejRTE({format: [
                { text: "Paragraph", value: "&lt;p&gt;", spriteCssClass: "e-paragraph" },
                { text: "Quotation", value: "&lt;blockquote&gt;", spriteCssClass: "e-quotation" }, 
                { text: "Heading 1", value: "&lt;h1&gt;", spriteCssClass: "e-h1" }, 
                { text: "Heading 2", value: "&lt;h2&gt;", spriteCssClass: "e-h2" }, 
                { text: "Heading 3", value: "&lt;h3&gt;", spriteCssClass: "e-h3" }, 
                { text: "Heading 4", value: "&lt;h4&gt;", spriteCssClass: "e-h4" }, 
                { text: "Heading 5", value: "&lt;h5&gt;", spriteCssClass: "e-h5" }, 
                { text: "Heading 6", value: "&lt;h6&gt;", spriteCssClass: "e-h6" } ]}); 
                &lt;/script&gt;
                </code>
{:#members:}

</pre>


### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:}




Defines the height of the RTE textbox.


Default Value:
{:.param}



* 370




Example
{:#example:}

<pre class="prettyprint">
<code>
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
//Initialize the RTE height property with the  value specified
        $("#rteSample").ejRTE({ height: 250 });
&lt;/script&gt;</code>
</pre>



### htmlAttributes<span class="type-signature type object">object</span>
{:#members:htmlattributes}




Specifies the HTML Attributes of the ejRTE


Default Value:
{:.param}



* {}




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the HtmlAttributes  specified.
$("#rteSample").ejRTE({htmlAttributes: {readOnly : "readOnly" });
&lt;/script&gt;</code>
</pre>



### iframeAttribute<span class="type-signature type string">string</span>
{:#members:iframeattribute}




Sets the iframe attribute in RTE.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the iframeAttribute value specified.
$("#rteSample").ejRTE({iframeAttribute: "color:#000" });
&lt;/script&gt;</code>
</pre>



### imageBrowser<span class="type-signature type object">object</span>
{:#members:imagebrowser}




This API allows to enable the image browser support in RTE control to browse, create delete and upload the image files in specified current directory.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the imageBrowser value specified.
$("#rteSample").ejRTE({  imageBrowser: {
  filePath: "../FileExplorerContent/",
 extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx",
ajaxAction: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/",
}});
&lt;/script&gt;</code>
</pre>



### imageBrowser.ajaxAction<span class="type-signature type string">string</span>
{:#members:imagebrowser-ajaxaction}




This API is used to receive the server side handler for file related operations.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the imageBrowser value specified.
$("#rteSample").ejRTE({  imageBrowser: {
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction"
}});
&lt;/script&gt;</code>
</pre>



### imageBrowser.extensionAllow<span class="type-signature type string">string</span>
{:#members:imagebrowser-extensionallow}




To specify the file type extension to be shown in image browser window.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the imageBrowser value specified.
$("#rteSample").ejRTE({  imageBrowser: {
extensionAllow: "*.doc,*.docx,*.tiff,*.jpeg"
}});
&lt;/script&gt;</code>
</pre>



### imageBrowser.filePath<span class="type-signature type string">string</span>
{:#members:imagebrowser-filepath}




Specify the directory to perform the operation like create, delete and rename folder &amp; files, upload the selected images to the current directory..



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the imageBrowser value specified.
$("#rteSample").ejRTE({  imageBrowser: {
 filePath: "../FileExplorerContent/"
}});
&lt;/script&gt;</code>
</pre>



### imageBrowser.uploadAction<span class="type-signature type string">string</span>
{:#members:imagebrowser-uploadaction}




Specifies the action which has to be performed after the file is pushed for uploading. Here we have to mention the server address which has to perform this action.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the imageBrowser value specified.
$("#rteSample").ejRTE({  imageBrowser: {
uploadAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
}});
&lt;/script&gt;</code>
</pre>



### imageBrowser.uploadAction<span class="type-signature type string">string</span>
{:#members:imagebrowser-uploadaction}




Specifies the action which has to be performed after the file is pushed for uploading. Here we have to mention the server address which has to perform this action.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
// Initialize the RTE with the imageBrowser value specified.
$("#rteSample").ejRTE({  imageBrowser: {
uploadAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
}});
&lt;/script&gt;</code>
</pre>



### isResponsive<span class="type-signature type boolean">boolean</span>
{:#members:isresponsive}




Enables/Disables the responsive support for RTE control toolbar items during the window resizing time.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;  
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the isResponsive value specified.
$("#rteSample").ejRTE({ isResponsive: true });
&lt;/script&gt;</code>
</pre>



### locale<span class="type-signature type string">string</span>
{:#members:locale}




Sets the culture in RTE.


Default Value:
{:.param}



* "en-US"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the culture value specified.
$("#rteSample").ejRTE({locale: "en-US" });
&lt;/script&gt;</code>
</pre>



### maxHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:maxheight}




Set the maximum height for RTE outer wrapper element.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the maxHeight value specified.
$("#rteSample").ejRTE({ maxHeight: 900});
&lt;/script&gt;</code>
</pre>



### maxLength<span class="type-signature type number">number</span>
{:#members:maxlength}




Set the max Length for RTE text.


Default Value:
{:.param}



* 7000




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the maxLength value specified.
$("#rteSample").ejRTE({ maxLength: 900});
&lt;/script&gt;</code>
</pre>



### maxWidth<span class="type-signature type number">number</span>
{:#members:maxwidth}




Set the maximum width for RTE outer wrapper element.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;  
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the maxWidth value specified.
$("#rteSample").ejRTE({ maxWidth: 900});
&lt;/script&gt;</code>
</pre>



### minHeight<span class="type-signature type number">number</span>
{:#members:minheight}




Set the minimum height for RTE outer wrapper element.


Default Value:
{:.param}



* 280




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the maxWidth value specified.
$("#rteSample").ejRTE({ minHeight: 900});
&lt;/script&gt;</code>
</pre>



### minWidth<span class="type-signature type number">number</span>
{:#members:minwidth}




Set the minimum width for RTE outer wrapper element.


Default Value:
{:.param}



* 400




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the minWidth value specified.
$("#rteSample").ejRTE({ minWidth: 900});
&lt;/script&gt;</code>
</pre>



### name<span class="type-signature type string">string</span>
{:#members:name}




Sets the name in RTE.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the name value specified.
$("#rteSample").ejRTE({name: "ecommentblog" });
&lt;/script&gt;</code>
</pre>



### showClearAll<span class="type-signature type boolean">boolean</span>
{:#members:showclearall}




Shows ClearAll in RTE.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showClearAll value specified.
$("#rteSample").ejRTE({showClearAll: false });
&lt;/script&gt;</code>
</pre>



### showClearFormat<span class="type-signature type boolean">boolean</span>
{:#members:showclearformat}




Sets the iframe attribute in RTE.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the iframeAttribute value specified.
$("#rteSample").ejRTE({showClearFormat:true });
&lt;/script&gt;</code>
</pre>



### showCustomTable<span class="type-signature type boolean">boolean</span>
{:#members:showcustomtable}




Shows CustomTable in RTE.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showCustomTable value specified.
$("#rteSample").ejRTE({showCustomTable: false });
&lt;/script&gt;</code>
</pre>



### showDimensions<span class="type-signature type boolean">boolean</span>
{:#members:showdimensions}




Shows Dimensions in RTE.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showDimensions value specified.
$("#rteSample").ejRTE({showDimensions: false });
&lt;/script&gt;</code>
</pre>



### showFontOption<span class="type-signature type boolean">boolean</span>
{:#members:showfontoption}




Shows FontOption in RTE.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showFontOption value specified.
$("#rteSample").ejRTE({showFontOption: false });
&lt;/script&gt;</code>
</pre>



### showFooter<span class="type-signature type boolean">boolean</span>
{:#members:showfooter}




Shows footer in RTE.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showFooter value specified.
$("#rteSample").ejRTE({showFooter: true });
&lt;/script&gt;</code>
</pre>



### showHtmlSource<span class="type-signature type boolean">boolean</span>
{:#members:showhtmlsource}




Shows HtmlSource in RTE.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showHtmlSource value specified.
$("#rteSample").ejRTE({showHtmlSource: false });
&lt;/script&gt;</code>
</pre>



### showHtmlTagInfo<span class="type-signature type boolean">boolean</span>
{:#members:showhtmltaginfo}




Shows HtmlTagInfo in RTE.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showHtmlTagInfo value specified.
$("#rteSample").ejRTE({showHtmlTagInfo: false });
&lt;/script&gt;</code>
</pre>



### showToolbar<span class="type-signature type boolean">boolean</span>
{:#members:showtoolbar}




Shows toolbar in RTE.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showToolbar value specified.
$("#rteSample").ejRTE({showToolbar: false });
&lt;/script&gt;</code>
</pre>



### showWordCount<span class="type-signature type boolean">boolean</span>
{:#members:showwordcount}




Shows WordCount in RTE.


Default Value:
{:.param}



* True




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the showWordCount value specified.
$("#rteSample").ejRTE({showWordCount: false });
&lt;/script&gt;</code>
</pre>



### tableColumns<span class="type-signature type number">number</span>
{:#members:tablecolumns}




Given number for columns render the insert table pop.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the 'tableColumns' value specified.
$("#rteSample").ejRTE({tableColumns: 70 });
&lt;/script&gt; </code>
</pre>



### tableRows<span class="type-signature type number">number</span>
{:#members:tablerows}




Given number for rows render the insert table pop.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the 'tableRows' value specified.
$("#rteSample").ejRTE({tableRows: 70 });
&lt;/script&gt;</code>
</pre>



### tools<span class="type-signature type object">object</span>
{:#members:tools}




Sets the tools in RTE.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
  //font: ["fontName", "fontSize", "fontColor", "backgroundColor"],
 formatStyle: ["format"],
style: ["bold", "italic", "underline", "strikethrough"],
alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"],
lists: ["unorderedList", "orderedList"],
indenting: ["outdent", "indent"],
doAction: ["undo", "redo"],
links: ["createLink"],
images: ["image", "video"],
tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"]
}});
&lt;/script&gt;</code>
</pre>



### tools.alignment<span class="type-signature type object">Object</span>
{:#members:tools-alignment}




Include font alignment options in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"]
}});
&lt;/script&gt;</code>
</pre>



### tools.doAction<span class="type-signature type object">Object</span>
{:#members:tools-doaction}




Include action options in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
doAction: ["undo", "redo"]
}});
&lt;/script&gt;</code>
</pre>



### tools.formatStyle<span class="type-signature type object">Object</span>
{:#members:tools-formatstyle}




Include Format styles in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
 formatStyle: ["format"]
}});
&lt;/script&gt;</code>
</pre>



### tools.images<span class="type-signature type object">Object</span>
{:#members:tools-images}




Include image and video options in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
images: ["image", "video"]
}});
&lt;/script&gt;</code>
</pre>



### tools.indenting<span class="type-signature type object">Object</span>
{:#members:tools-indenting}




Include text indenting options in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
indenting: ["outdent", "indent"]
}});
&lt;/script&gt;</code>
</pre>



### tools.links<span class="type-signature type object">Object</span>
{:#members:tools-links}




Include links options in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
links: ["createLink"]
}});
&lt;/script&gt;</code>
</pre>



### tools.lists<span class="type-signature type object">Object</span>
{:#members:tools-lists}




Include list type options in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
lists: ["unorderedList", "orderedList"]
}});
&lt;/script&gt;</code>
</pre>



### tools.style<span class="type-signature type object">Object</span>
{:#members:tools-style}




Include font styles in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
style: ["bold", "italic", "underline", "strikethrough"]
}});
&lt;/script&gt;</code>
</pre>



### tools.tables<span class="type-signature type object">Object</span>
{:#members:tools-tables}




Include tables options in RTE toolbar.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the tools value specified.
$("#rteSample").ejRTE({  tools: {
tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"]
}});
&lt;/script&gt;</code>
</pre>



### toolsList<span class="type-signature type object">object</span>
{:#members:toolslist}




Sets the toolsList in RTE.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the toolsList value specified.
$("#rteSample").ejRTE({ toolsList: ["formatStyle", "font", "style", "scripts", "alignment", "lists", "indenting", "copyPaste", "doAction", "clear", "links", "images", "tables", "casing", "customTool"]});
&lt;/script&gt;</code>
</pre>



### undoStackLimit<span class="type-signature type number">number</span>
{:#members:undostacklimit}




Undo operation provide the number of step limit.


Default Value:
{:.param}



* 50




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the 'undoStackLimit' value specified.
$("#rteSample").ejRTE({undoStackLimit: 70 });
&lt;/script&gt;</code>
</pre>



### value<span class="type-signature type string">string</span>
{:#members:value}




Given string value to display in the editable area.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
// Initialize the RTE with the 'value' value specified.
$("#rteSample").ejRTE({value: "The Rich Text Editor (RTE) control is an easy to render in client side. Customer easy to edit the contents, insert table, images and get the HTML content for the displayed content." });
&lt;/script&gt;</code>
</pre>



### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}




Defines the width of the RTE textbox.


Default Value:
{:.param}



* 786




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
//Initialize the RTE width property with the  value specified
        $("#rteSample").ejRTE({ width: 500 });
&lt;/script&gt;</code>
</pre>


## Methods




### disable<span class="signature">()</span>
{:#methods:disable}




disable the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code>&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.disable(); // disable RTE
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("disable");// disable RTE
&lt;/script&gt;</code>
</pre>



### disableToolbarItem<span class="signature">()</span>
{:#methods:disabletoolbaritem}




disable the RTE toolbar item.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.disableToolbarItem("rteSamplecreateTable"); // disable toolbar item
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("disableToolbarItem","rteSamplecreateTable");// disable toolbar item        
&lt;/script&gt;</code>
</pre>



### enable<span class="signature">()</span>
{:#methods:enable}




enable the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
     &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.enable(); // enable RTE
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("enable");// enable RTE
&lt;/script&gt;</code>
</pre>



### enableToolbarItem<span class="signature">()</span>
{:#methods:enabletoolbaritem}




enable the RTE toolbar item.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                   
     &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.enableToolbarItem("rteSamplecreateTable"); // enable toolbar item
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("enableToolbarItem","rteSamplecreateTable");// enable toolbar item        
&lt;/script&gt;</code>
</pre>



### executeCommand<span class="signature">()</span>
{:#methods:executecommand}




gets the content as string from the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                    
    &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.executeCommand("bold", true); // gets the content as string from rte
&lt;/script&gt;</code>
</pre>



### focus<span class="signature">()</span>
{:#methods:focus}




focus the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                      
  &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.focus(); // gets the content as string from rte
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("focus");// enable toolbar item        
&lt;/script&gt;</code>
</pre>



### getCommandStatus<span class="signature">()</span>
{:#methods:getcommandstatus}




gets the command status of the given RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                   
 &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.getCommandStatus(arguments); // gets the content as string from rte
&lt;/script&gt;</code>
</pre>



### getHtml<span class="signature">()</span>
{:#methods:gethtml}




gets the HTML string from the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                       
 &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.getHtml(); // gets the html string from rte
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("getHtml");// getHtml from rte        
&lt;/script&gt;</code>
</pre>



### getSelectedHtml<span class="signature">()</span>
{:#methods:getselectedhtml}




gets the command status of the given RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.getSelectedHtml(); // gets the content as string from rte
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("getSelectedHtml");// getSelectedHtml from rte        
&lt;/script&gt;</code>
</pre>



### getText<span class="signature">()</span>
{:#methods:gettext}




gets the content as string from the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                      
  &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.getText(); // gets the content as string from rte
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("getText");// getText from rte        
&lt;/script&gt;</code>
</pre>



### hide<span class="signature">()</span>
{:#methods:hide}




Hides the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                        
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.hide(); // hides rte
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("hide");// hides rte       
&lt;/script&gt;</code>
</pre>



### refresh<span class="signature">()</span>
{:#methods:refresh}




refresh the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                    
    &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.refresh(); // refresh rte
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("refresh");// refresh rte       
&lt;/script&gt;</code>
</pre>



### removeToolbarItem<span class="signature">()</span>
{:#methods:removetoolbaritem}




removes the RTE toolbar item.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                 
       &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.removeToolbarItem("rteSamplecreateTable"); // remove toolbar item
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("removeToolbarItem","rteSamplecreateTable");// remove toolbar item        
&lt;/script&gt;</code>
</pre>



### setColorPickerType<span class="signature">()</span>
{:#methods:setcolorpickertype}




Set the colorpicker model type to be rendered initially in the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                       
 &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.setColorPickerType("picker"); // set the picker mode
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("setColorPickerType","picker");// set the picker mode        
&lt;/script&gt;</code>
</pre>



### setHtml<span class="signature">()</span>
{:#methods:sethtml}




sets the HTML string from the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                     
  &lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.setHtml("The Rich Text Editor (RTE) control is an easy to render in client side."); // sets the html string to rte
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("setHtml","The Rich Text Editor (RTE) control is an easy to render in client side.");// sets the html string to rte    
&lt;/script&gt;</code>
</pre>



### show<span class="signature">()</span>
{:#methods:show}




Displays the RTE control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;                    
    &lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
var rteeObj  = $("#rteSample").data("ejRTE");
rteeObj.show(); // shows rte
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;          
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
&lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
            client side. Customer easy to edit the contents and get the HTML content for
            the displayed content. A rich text editor control provides users with a toolbar
            that helps them to apply rich text formats to the text entered in the text
            area. &lt;/p&gt;&lt;/textarea &gt;
&lt;script&gt;
$("#rteSample").ejRTE();
// Create RTE
$("#rteSample").ejRTE("show");// shows rte       
&lt;/script&gt;</code>
</pre>


## Events




### change
{:#events:change}




Fires when change successfully.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the RTE model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
$("#rteSample").ejRTE();
//change event for RTE
$("#rteSample").ejRTE({ 
        change: function(args) {}
});      
&lt;/script&gt;</code>
</pre>



### execute
{:#events:execute}




Fires when execute successfully.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the RTE model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
$("#rteSample").ejRTE();
//execute event for RTE
$("#rteSample").ejRTE({ 
        execute: function(args) {}
});   
&lt;/script&gt;   </code>
</pre>



### keydown
{:#events:keydown}




Fires when keydown successfully.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the RTE model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
$("#rteSample").ejRTE();
//keydown event for RTE
$("#rteSample").ejRTE({ 
        keydown: function(args) {}
});  
&lt;/script&gt;    </code>
</pre>



### keyup
{:#events:keyup}




Fires when keyup successfully.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the RTE model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;textarea   id="rteSample"&gt;     
&lt;p&gt;&lt;b&gt;Description:&lt;/b&gt;&lt;/p&gt;
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;&lt;/textarea &gt;     
&lt;script&gt;
$("#rteSample").ejRTE();
//keyup event for RTE
$("#rteSample").ejRTE({ 
        keyup: function(args) {}
});  
&lt;/script&gt;    </code>
</pre>

