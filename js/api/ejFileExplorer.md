---
layout: post
title: ejFileExplorer
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html File Explorer control.










$(element).ejFileExplorer<span class="signature">(options)</span>







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
<td class="description last">settings for FileExplorer.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Create File Explorer
$('#fileExplorer').ejFileExplorer({ 
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",
});
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.min.js


* module:jquery.globalize.min.js


* module:jsrender.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.scroller.js


* module:ej.draggable.js


* module:ej.button.js


* module:ej.treeview.js


* module:ej.uploadbox.js


* module:ej.waitingpopup.js


* module:ej.dialog.js


* module:ej.splitter.js


* module:ej.toolbar.js


* module:ej.menu.js


* module:ej.fileexplorer.js


* module:ej.grid.edit.js


* module:ej.grid.filter.js


* module:ej.grid.selection.js


* module:ej.grid.sort.js


* module:ej.grid.dragAndDrop.js


* module:ej.grid.common.js


* module:ej.grid.base.js




## Members








### ajaxAction<span class="type-signature type string">string</span>
{:#members:ajaxaction}








Sets the Url of server side ajax handling method, which on going to handle file operation like Read, Remove, Rename, Create, Upload, Download, Copy and Move in File Explorer.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with ajaxAction value specified.
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}



### ajaxDataType<span class="type-signature type string">string</span>
{:#members:ajaxdatatype}

Specifies the data type of server side ajax handling method. 

Default Value:
{:.param}

* "json"

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with ajaxDataType value specified.
$('#fileExplorer').ejFileExplorer({
ajaxDataType: "jsonp",            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONPAction"
});
</script>{% endhighlight %}



### ajaxSettings<span class="type-signature type object">Object</span>
{:#members:ajaxsettings}








Using ajaxSettings property, we can customize the ajax configurations. Normally we can customize following option in ajax handling data, url, type, async, contentType, dataType and success. For upload, download and getImage API, we can customize url only.




Default Value:
{:.param}






* { read: {}, createFolder: {}, remove: {}, rename: {}, paste: {}, getDetails: {}, download: {}, upload: {}, getImage: {}}








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with ajaxSettings value specified.
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
ajaxSettings: {
    read: {
        url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONPAction",
        dataType: "jsonp"
    }
}
});
</script>{% endhighlight %}



### allowMultiSelection<span class="type-signature type boolean">boolean</span>
{:#members:allowmultiselection}

The file explorer allows the user to select multiple files by enabling the allowMultiSelection property. The multi selection can be done by pressing the Ctrl key or Shift key. 

Default Value:
{:.param}

* true

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with allowMultiSelection value specified.
$('#fileExplorer').ejFileExplorer({
allowMultiSelection: false,            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}



### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Sets the root class for File Explorer theme. This cssClass API helps to use custom skinning option for File Explorer control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with cssClass value specified.
$('#fileExplorer').ejFileExplorer({ 
cssClass: 'gradient-lime',
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"      
});
</script>{% endhighlight %}







### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}








Enables/Disables the resize support in File Explorer control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with enableResize value specified.
$('#fileExplorer').ejFileExplorer({ 
enableResize: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                   
});
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Enables/Disables the Right to Left alignment support in File Explorer control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with enableRTL value specified.
$('#fileExplorer').ejFileExplorer({ 
enableRTL: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
});
</script>{% endhighlight %}







### fileTypes<span class="type-signature type string">string</span>
{:#members:filetypes}








Allows specified type of files only to display in File Explorer control.




Default Value:
{:.param}






* "*.*"








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Specifies the file types, which one need to allow in File Explorer control
$('#fileExplorer').ejFileExplorer({ 
fileTypes: "*.png,*.gif,*.jpg,*.jpeg,*.docx",
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"               
});
</script>{% endhighlight %}







### filterSettings<span class="type-signature type object">Object</span>
{:#members:filtersettings}








Using filterSettings property, we can customize the search functionality of the searchbar in File Explorer control.











### filterSettings.caseSensitiveSearch<span class="type-signature type boolean">boolean</span>
{:#members:filtersettings-casesensitivesearch}








Enable/Disable to perform the filter operation with case sensitive.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Specifies the case sensitive for searching operation
$('#fileExplorer').ejFileExplorer({ 
filterSettings: {
  caseSensitiveSearch: true,
},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"     
});
</script>{% endhighlight %}







### filterSettings.filterType<span class="type-signature type enum">enum</span>
{:#members:filtersettings-filtertype}








Sets the search filter type. There are several filter types are available such as "startswith", "contains", "endswith". See <a href="global.html#filterType">filterType</a>




Default Value:
{:.param}






* ej.FileExplorer.filterType.Contains








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Specifies the filter types, which is used to filter the grid or list elements
$('#fileExplorer').ejFileExplorer({
filterSettings: { 
filterType: "startswith",
},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"     
});
</script>{% endhighlight %}







### gridSettings<span class="type-signature type object">Object</span>
{:#members:gridsettings}








Using the gridSettings property, we can customize the grid behavior in the File Explorer control.











### gridSettings.allowSorting<span class="type-signature type boolean">boolean</span>
{:#members:gridsettings-allowsorting}








Gets or sets a value that indicates whether to enable the dynamic sorting behavior on grid data. Sorting can be done through clicking on particular column header.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// Initialize the File explorer with the allowSorting value specified for grid.
$('#fileExplorer').ejFileExplorer({ 
gridSettings:{allowSorting:false},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"               
}); 
</script>{% endhighlight %}







### gridSettings.columns<span class="type-signature type array">array</span>
{:#members:gridsettings-columns}








Gets or sets an object that indicates to render the grid with specified columns, we can use this property same as column property in grid control




Default Value:
{:.param}






* [{ field: "name", headerText: "Name", width: "25%" }, { field: "type", headerText: "Type", width: "20%" }, { field: "dateModified", headerText: "Date Modified", width: "35%" }, { field: "size", headerText: "Size", width: "15%", textAlign: "right", headerTextAlign: "left" }]








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File explorer with the columns value specified for grid.
$('#fileExplorer').ejFileExplorer({ 
gridSettings:{columns:[{ field: "name", headerText: "Name", width: 90 }, { field: "type", headerText: "Type", width: 95 }, { field: "size", headerText: "Size", width: 90 }]},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"               
}); 
</script>{% endhighlight %}







### height<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:height}








Specifies the height of File Explorer control




Default Value:
{:.param}






* 400








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with the height value specified.
$('#fileExplorer').ejFileExplorer({   
height: 450,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"            
});
</script>{% endhighlight %}







### isResponsive<span class="type-signature type boolean">boolean</span>
{:#members:isresponsive}








Enables/Disables the responsive support for FileExplorer control during the window resizing time.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File explorer with isResponsive value specified.
$('#fileExplorer').ejFileExplorer({
isResponsive: true,
width: "70%",
height: "50%",
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}







### layout<span class="type-signature type enum">enum</span>
{:#members:layout}








Sets the file view type. There are two view types are available such as grid, tile. See layoutType




Default Value:
{:.param}






* ej.FileExplorer.layoutType.Grid








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with the layout value specified.
$('#fileExplorer').ejFileExplorer({ 
layout: "tile",
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                 
}); 
</script>{% endhighlight %}







### locale<span class="type-signature type string">string</span>
{:#members:locale}








Sets the culture in FileExplorer.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with the culture value specified.
$('#fileExplorer').ejFileExplorer({ 
locale: "en-US",
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"               
});
</script>{% endhighlight %}



### maxHeight<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:maxheight}

Set the maximum height of File Explorer control. 

Default Value:
{:.param}

* null

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with maxHeight value specified.
$('#fileExplorer').ejFileExplorer({
maxHeight: 500,            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}


### maxWidth<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:maxwidth}

Set the maximum width of File Explorer control. 

Default Value:
{:.param}

* null

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with maxWidth value specified.
$('#fileExplorer').ejFileExplorer({
maxWidth: 1000,            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}


### minHeight<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:minheight}

Set the minimum height of File Explorer control. 

Default Value:
{:.param}

* 250

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with minHeight value specified.
$('#fileExplorer').ejFileExplorer({
minHeight: 300,            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}


### minWidth<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:minwidth}

Set the minimum width of File Explorer control. 

Default Value:
{:.param}

* 400

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with minWidth value specified.
$('#fileExplorer').ejFileExplorer({
minWidth: 300,            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}



### path<span class="type-signature type string">string</span>
{:#members:path}








The property path denotes the filesystem path which we are going to explore. The path for the filesystem can be physical path or relative path, but it should be relevant to where the Web API hosted.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Specifies the root folder path, which is need to specified in file explorer control
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                                 
});
</script>{% endhighlight %}



### selectedFolder<span class="type-signature type string">String</span>
{:#members:selectedfolder}

The selectedFolder is used to select the specified folder of File Explorer control. 

Default Value:
{:.param}

* ""

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with selectedFolder value specified.
$('#fileExplorer').ejFileExplorer({
selectedFolder: "http://mvc.syncfusion.com/ODataServices/FileBrowser/Food",            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}



### selectedItems<span class="type-signature type string">String</span><span class="type-signature type array">Array</span>
{:#members:selecteditems}

The selectedItems is used to select the specified items (file, folder) of File Explorer control. 

Default Value:
{:.param}

* ""

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with selectedItems value specified.
$('#fileExplorer').ejFileExplorer({
selectedItems: ["Food", "Nature"],            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
});
</script>{% endhighlight %}



### showContextMenu<span class="type-signature type boolean">boolean</span>
{:#members:showcontextmenu}








Enables/Disable the context menu option in File Explorer control.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File explorer with the showContextMenu value specified.
$('#fileExplorer').ejFileExplorer({ 
showContextMenu: false,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                     
});
</script>{% endhighlight %}







### showFooter<span class="type-signature type boolean">boolean</span>
{:#members:showfooter}








Enables/Disable the footer in File Explorer control.The footer element displays the details of the current selected files and folders. And the footer having the switcher to change the layout view.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with the showFooter value specified.
$('#fileExplorer').ejFileExplorer({ 
showFooter: false,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                   
});
</script>{% endhighlight %}









### showToolbar<span class="type-signature type boolean">boolean</span>
{:#members:showtoolbar}








Shows/Disable the toolbar in File Explorer control.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// Initialize the File explorer with the showToolbar value specified.
$('#fileExplorer').ejFileExplorer({ 
showToolbar: false,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
});
</script>{% endhighlight %}







### showNavigationPane<span class="type-signature type boolean">boolean</span>
{:#members:shownavigationpane}








Enables/Disable the navigation pane in File Explorer control. The navigation pane contains the tree view element which displays all the folders from the filesystem in a hierarchical manner. This is useful to a quick navigation of any folder in the filesystem.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// Initialize the File Explorer with the showNavigationPane value specified.
$('#fileExplorer').ejFileExplorer({ 
showNavigationPane: false,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                 
}); 
</script>{% endhighlight %}







### tools<span class="type-signature type object">object</span>
{:#members:tools}








The tools property is used to configure and group required toolbar items in File Explorer control.




Default Value:
{:.param}






* { creation:["NewFolder", "Open"], navigation: ["Back", "Forward", "Upward"], addressBar: ["Addressbar"], editing: ["Refresh", "Upload", "Delete", "Rename", "Download"], copyPaste: ["Cut", "Copy", "Paste"], getProperties: ["Details"], searchBar: ["Searchbar"] }








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// Initialize the File Explorer with toolbar tools value specified.
$('#fileExplorer').ejFileExplorer({ 
tools: {
  creation:["NewFolder", "Open"],
  navigation: ["Back", "Forward", "Upward"],
  addressBar: ["Addressbar"],
  editing: ["Refresh", "Upload", "Delete", "Rename", "Download"],
  copyPaste: ["Cut", "Copy", "Paste"],
  getProperties: ["Details"],
  searchBar: ["Searchbar"]
},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"        
});
</script>{% endhighlight %}







### toolsList<span class="type-signature type array">array</span>
{:#members:toolslist}








The toolsList property is used to arrange the toolbar items in File Explorer control.




Default Value:
{:.param}






* ["creation", "navigation", "addressBar", "editing", "copyPaste", "getProperties", "searchBar"]








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with toolsList value specified.
$('#fileExplorer').ejFileExplorer({ 
toolsList: ["navigation", "creation", "addressBar", "editing", "copyPaste", "getProperties", "searchBar"],
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                 
}); 
</script>{% endhighlight %}







### uploadSettings<span class="type-signature type object">Object</span>
{:#members:uploadsettings}








Gets or sets an object that indicates whether to customize the upload behavior in the File Explorer.











### uploadSettings.maxFileSize<span class="type-signature type number">number</span>
{:#members:uploadSettings-maxfilesize}








Specifies the maximum file size allowed to upload. It accepts the value in bytes.




Default Value:
{:.param}






* 31457280








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File Explorer with the maxFileSize value specified for uploadbox.
$('#fileExplorer').ejFileExplorer({ 
uploadSettings:{maxFileSize:10000},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
}); 
</script>{% endhighlight %}







### uploadSettings.allowMultipleFile<span class="type-signature type boolean">boolean</span>
{:#members:uploadSettings-allowmultiplefile}








Enables or disables the multiple files upload. When it enabled the user can upload multiple files at a time, when disables user can upload only one file at a time.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File explorer with the multipleFilesSelection value specified for uploadbox.
$('#fileExplorer').ejFileExplorer({ 
 uploadSettings:{allowMultipleFile:false},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
}); 
</script>{% endhighlight %}

### uploadSettings.autoUpload<span class="type-signature type boolean">boolean</span>
{:#members:uploadSettings-autoupload}








Enables/Disables the auto upload option, while uploading files in FileExplorer control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File explorer with auto upload option as true.
$('#fileExplorer').ejFileExplorer({ 
uploadSettings:{autoUpload:true},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
}); 
</script>{% endhighlight %}







### width<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:width}








Specifies the width of File Explorer control.




Default Value:
{:.param}






* 850








Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Initialize the File explorer with the width value specified.
$('#fileExplorer').ejFileExplorer({   
width: 800,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                     
});
</script>{% endhighlight %}





## Methods



### adjustSize<span class="signature">()</span>
{:#methods:adjustsize}


Refresh the size of File Explorer control.

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// refresh the size of file explorer 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"           
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.adjustSize(); // refresh the size of file explorer               
</script>{% endhighlight %}



### disableMenuItem<span class="signature">()</span>
{:#methods:disablemenuitem}


Disable the particular context menu item

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// diable the context menu item 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"           
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.disableMenuItem("Upload"); // disable upload option                         
</script>{% endhighlight %}



### disableToolbarItem<span class="signature">()</span>
{:#methods:disabletoolbaritem}








Disable the particular toolbar item





Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// diable the toolbar tool 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"           
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.disableToolbarItem("Searchbar"); // disable search bar                           
</script>{% endhighlight %}




### enableMenuItem<span class="signature">()</span>
{:#methods:enablemenuitem}

Enable the particular context menu item

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// enable the context menu item 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"            
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.enableMenuItem("Upload"); // enable upload option in context menu                     
</script>{% endhighlight %}



### enableToolbarItem<span class="signature">()</span>
{:#methods:enabletoolbaritem}








Enable the particular toolbar item





Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// enable the toolbar tool 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"            
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.enableToolbarItem("Searchbar"); // enable search bar                     
</script>{% endhighlight %}



### refresh<span class="signature">()</span>
{:#methods:refresh}


Refresh the content of the selected folder in File Explorer control.

Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// refresh the content of selected folder 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"           
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.refresh(); // refresh the content of selected folder               
</script>{% endhighlight %}



### removeToolbarItem<span class="signature">()</span>
{:#methods:removetoolbaritem}








Remove the particular toolbar item





Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// remove the toolbar tool 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"            
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.removeToolbarItem("Searchbar"); // remove search bar                     
</script>{% endhighlight %}



## Events



### beforeAjaxRequest
{:#events:beforeajaxrequest}

Fires while before ajax request has been performed

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ajax response data</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// beforeAjaxRequest event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
beforeAjaxRequest: function (args) {}
});
</script>{% endhighlight %}



### beforeDownload
{:#events:beforedownload}



Fires while before downloading the files.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
files{% endhighlight %}</td>
<td class="type"><span class="param-type">string[]</span></td>
<td class="description last">returns the downloaded file names</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
path{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// beforeDownload event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
beforeDownload: function (args) {}
});
</script>{% endhighlight %}




### beforeOpen
{:#events:beforeopen}



Fires while files/ folders before opens

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
itemType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the opened item type</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
path{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// beforeOpen event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
beforeOpen: function (args) {}
});
</script>{% endhighlight %}



### beforeUpload
{:#events:beforeupload}



Fires while before uploading the files

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
path{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// beforeUpload event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
beforeUpload: function (args) {}
});
</script>{% endhighlight %}



### copy
{:#events:copy}



Fires while file or folder has been copied successfully

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string[]</span></td>
<td class="description last">returns the name of copied file/folder</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
sourcePath{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the source path</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// copy event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
copy: function (args) {}
});
</script>{% endhighlight %}



### createFolder
{:#events:createfolder}



Fires when new folder has been created sucessfully in file system

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ajax response data</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// createFolder event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
createFolder: function (args) {}
});
</script>{% endhighlight %}



### cut
{:#events:cut}



Fires while file or folder has been cut successfully

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string[]</span></td>
<td class="description last">returns the name of moved file/folder</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
sourcePath{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the source path</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// cut event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
cut: function (args) {}
});
</script>{% endhighlight %}



### layoutChange
{:#events:layoutchange}



Fires when the file view type has been changed

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
layoutType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current view type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// layoutChange event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
layoutChange: function (args) {}
});
</script>{% endhighlight %}



### open
{:#events:open}



Fires while files has been opened successfully

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
itemType{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the opened item type</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
path{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// open event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
open: function (args) {}
});
</script>{% endhighlight %}



### paste
{:#events:paste}



Fires while file or folder has been pasted successfully

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string[]</span></td>
<td class="description last">returns the name of moved file/folder</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
targetFolder{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target folder item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
targetPath{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the target path</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// paste event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
paste: function (args) {}
});
</script>{% endhighlight %}



### remove
{:#events:remove}



Fires when file or folder has been deleted sucessfully

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ajax response data</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the names of deleted items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
path{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the path of deleted item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// remove event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
remove: function (args) {}
});
</script>{% endhighlight %}



### resize
{:#events:resize}


Fires this event when the resizing is performed for fileexplorer

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the mouse move event args</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// resize event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
resize: function (args) {}
});
</script>{% endhighlight %}



### resizeStart
{:#events:resizestart}


Fires this event when the resizing is started for fileexplorer

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the mouse down event args</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// resizeStart event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
resizeStart: function (args) {}
});
</script>{% endhighlight %}



### resizeStop
{:#events:resizestop}


Fires this event when the resizing is stopped for fileexplorer

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the mouse leave event args</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// resizeStop event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
resizeStop: function (args) {}
});
</script>{% endhighlight %}



### select
{:#events:select}



Fires when the items from grid view or tile view of fileexplorer control has been selected.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from FileExplorer
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of clicked item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
path{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the path of clicked item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="fileExplorer" ></div> 
 
<script>
// select event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",        
select: function (args) {}
});
</script>{% endhighlight %}




