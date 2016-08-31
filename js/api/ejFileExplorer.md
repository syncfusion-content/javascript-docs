---
layout: post
title: Properties, Methods and Events of ejFileExplorer Widget
description: API reference for ejFileExplorer
documentation: API
platform: js
keywords: FileExplorer, ejFileExplorer, syncfusion, FileExplorer api
---

# ejFileExplorer


FileExplorer provides a Windows Explorer-like functionality for any web application. It allows end-users to browse, select and upload files or change the folder structure by renaming, moving and deleting files or folders. File and folder management capabilities are fully customizable and can be disabled when necessary.



#### Syntax

{% highlight javascript %}

        $(element).ejFileExplorer(options)

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
<td class="description">settings for FileExplorer.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="fileExplorer"></div> 
 
<script>
// Create FileExplorer
$('#fileExplorer').ejFileExplorer({ 
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",
});
</script>

{% endhighlight %}







#### Requires


* module:jQuery


* module:jquery.easing.1.3.min.js


* module:jsrender.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.globalize.js


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


* module:ej.checkbox.js


* module:ej.splitbutton.js


* module:ej.grid.edit.js


* module:ej.grid.filter.js


* module:ej.grid.selection.js


* module:ej.grid.sort.js


* module:ej.grid.dragAndDrop.js


* module:ej.grid.common.js


* module:ej.grid.base.js




## Members



### ajaxAction `string`
{:#members:ajaxaction}



Sets the URL of server side AJAX handling method that handles file operation like Read, Remove, Rename, Create, Upload, Download, Copy and Move in FileExplorer.




#### Default Value







* ""








#### Example



{% highlight html %}
        
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with ajaxAction value specified.
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>

{% endhighlight %}



### ajaxDataType `string`
{:#members:ajaxdatatype}

Specifies the data type of server side AJAX handling method. 

#### Default Value


* "json"

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with ajaxDataType value specified.
        $('#fileExplorer').ejFileExplorer({
        ajaxDataType: "jsonp",            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONPAction"
        });
        </script>

{% endhighlight %}



### ajaxSettings `object`
{:#members:ajaxsettings}








By using ajaxSettings property, you can customize the AJAX configurations. Normally you can customize the following option in AJAX handling data, URL, type, async, contentType, dataType and success. For upload, download and getImage API, you can only customize URL.




#### Default Value







* { read: {}, createFolder: {}, remove: {}, rename: {}, paste: {}, getDetails: {}, download: {}, upload: {}, getImage: {}, search: {}}








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with ajaxSettings value specified.
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
        </script>

{% endhighlight %}


### allowMultiSelection `boolean`
{:#members:allowmultiselection}

The FileExplorer allows to select multiple files by enabling the allowMultiSelection property. You can perform multi selection by pressing the Ctrl key or Shift key. 

#### Default Value


* true

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with allowMultiSelection value specified.
        $('#fileExplorer').ejFileExplorer({
        allowMultiSelection: false,            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>
        
{% endhighlight %}



### cssClass `string`
{:#members:cssclass}








Sets the root class for FileExplorer theme. This cssClass API allows to use custom skinning option for File Explorer control. By defining the root class by using this API, you have to include this root class in CSS.




#### Default Value







* ""








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with cssClass value specified.
        $('#fileExplorer').ejFileExplorer({ 
        cssClass: 'gradient-lime',
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"      
        });
        </script>

{% endhighlight %}







### enableResize `boolean`
{:#members:enableresize}








Enables or disables the resize support in FileExplorer control.




#### Default Value







* false








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with enableResize value specified.
        $('#fileExplorer').ejFileExplorer({ 
        enableResize: true,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                   
        });
        </script>

{% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Enables or disables the Right to Left alignment support in FileExplorer control.




#### Default Value







* false








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with enableRTL value specified.
        $('#fileExplorer').ejFileExplorer({ 
        enableRTL: true,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
        });
        </script>

{% endhighlight %}







### fileTypes `string`
{:#members:filetypes}








Allows specified type of files only to display in FileExplorer control.




#### Default Value







* "*.*"








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Specifies the file types that one needs to allow in FileExplorer control
        $('#fileExplorer').ejFileExplorer({ 
        fileTypes: "*.png,*.gif,*.jpg,*.jpeg,*.docx",
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"               
        });
        </script>

{% endhighlight %}







### filterSettings `object`
{:#members:filtersettings}








By using filterSettings property, you can customize the search functionality of the search bar in FileExplorer control.











### filterSettings.caseSensitiveSearch `boolean`
{:#members:filtersettings-casesensitivesearch}








Enables or disables to perform the filter operation with case sensitive.




#### Default Value







* false








#### Example



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
        </script>

{% endhighlight %}







### filterSettings.filterType `enum`
{:#members:filtersettings-filtertype}



<ts name="ej.FilterType" />




Sets the search filter type. There are several filter types available such as "startswith", "contains", "endswith". See filterType.


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
StartsWith</td>
<td class="type">string</td>
<td class="default">startswith</td>
<td class="description">Enum for filter type startswith</td>
</tr>
<tr>
<td class="name">
Contains</td>
<td class="type">string</td>
<td class="default">contains</td>
<td class="description">Enum for filter type contains</td>
</tr>
<td class="name">
EndsWith</td>
<td class="type">string</td>
<td class="default">endswith</td>
<td class="description">Enum for filter type endswith</td>
</tr>
</tbody>
</table>

#### Default Value







* ej.FileExplorer.filterType.Contains








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Specifies the filter types that are used to filter the grid or list elements
        $('#fileExplorer').ejFileExplorer({
        filterSettings: { 
        filterType: "startswith",
        },
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"     
        });
        </script>

{% endhighlight %}







### gridSettings `object`
{:#members:gridsettings}








By using the gridSettings property, you can customize the grid behavior in the FileExplorer control.











### gridSettings.allowSorting `boolean`
{:#members:gridsettings-allowsorting}








Gets or sets a value that indicates whether to enable the dynamic sorting behavior on grid data. Sorting can be done through clicking on particular column header.




#### Default Value







* true








#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // Initialize the FileExplorer with the allowSorting value specified for grid.
        $('#fileExplorer').ejFileExplorer({ 
        gridSettings:{allowSorting:false},
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"               
        }); 
        </script>

{% endhighlight %}







### gridSettings.columns `array`
{:#members:gridsettings-columns}








Gets or sets an object that indicates to render the grid with specified columns. You can use this property same as the column property in Grid control.




#### Default Value







* [{ field: "name", headerText: "Name", width: "30%" }, { field: "dateModified", headerText: "Date Modified", width: "30%" }, { field: "type", headerText: "Type", width: "15%" }, { field: "size", headerText: "Size", width: "12%", textAlign: "right", headerTextAlign: "left" }]








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the columns value specified for grid.
        $('#fileExplorer').ejFileExplorer({ 
        gridSettings:{columns:[{ field: "name", headerText: "Name", width: 90 }, { field: "type", headerText: "Type", width: 95 }, { field: "size", headerText: "Size", width: 90 }]},
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"               
        }); 
        </script>

{% endhighlight %}







### height `string | number`
{:#members:height}








Specifies the height of FileExplorer control.




#### Default Value







* 400








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the height value specified.
        $('#fileExplorer').ejFileExplorer({   
        height: 450,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"            
        });
        </script>

{% endhighlight %}







### isResponsive `boolean`
{:#members:isresponsive}








Enables or disables the responsive support for FileExplorer control during the window resizing time.




#### Default Value







* false








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with isResponsive value specified.
        $('#fileExplorer').ejFileExplorer({
        isResponsive: true,
        width: "70%",
        height: "50%",
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>

{% endhighlight %}







### layout `enum`
{:#members:layout}



<ts name="ej.FileExplorer.layoutType"/>




Sets the file view type. There are three view types available such as Grid, Tile and Large icons. See layoutType.


<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Tile</td>
<td class="description">Supports to display files in tile view</td>
</tr>
<tr>
<td class="name">
Grid</td>
<td class="description">Supports to display files in grid view </td>
</tr>
<tr>
<td class="name">
LargeIcons</td>
<td class="description">Supports to display files as large icons</td>
</tr>
</tbody>
</table>

#### Default Value







* ej.FileExplorer.layoutType.Grid








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the layout value specified.
        $('#fileExplorer').ejFileExplorer({ 
        layout: "tile",
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                 
        }); 
        </script>

{% endhighlight %}







### locale `string`
{:#members:locale}








Sets the culture in FileExplorer.




#### Default Value







* "en-US"








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the culture value specified.
        $('#fileExplorer').ejFileExplorer({ 
        locale: "en-US",
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"               
        });
        </script>

{% endhighlight %}



### maxHeight `string | number`
{:#members:maxheight}

Sets the maximum height of FileExplorer control. 

#### Default Value


* null

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with maxHeight value specified.
        $('#fileExplorer').ejFileExplorer({
        maxHeight: 500,            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>

{% endhighlight %}


### maxWidth `string | number`
{:#members:maxwidth}

Sets the maximum width of FileExplorer control. 

#### Default Value


* null

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with maxWidth value specified.
        $('#fileExplorer').ejFileExplorer({
        maxWidth: 1000,            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>

{% endhighlight %}


### minHeight `string | number`
{:#members:minheight}

Sets the minimum height of FileExplorer control. 

#### Default Value


* "250px"

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with minHeight value specified.
        $('#fileExplorer').ejFileExplorer({
        minHeight: 300,            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>

{% endhighlight %}


### minWidth `string | number`
{:#members:minwidth}

Sets the minimum width of FileExplorer control. 

#### Default Value


* "400px"

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with minWidth value specified.
        $('#fileExplorer').ejFileExplorer({
        minWidth: 300,            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>

{% endhighlight %}



### path `string`
{:#members:path}








The property path denotes the filesystem path that are to be explored. The path for the filesystem can be physical path or relative path, but it has to be relevant to where the Web API is hosted.




#### Default Value







* ""








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Specifies the root folder path that has to be specified in FileExplorer control
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                                 
        });
        </script>

{% endhighlight %}



### selectedFolder `string`
{:#members:selectedfolder}

The selectedFolder is used to select the specified folder of FileExplorer control. 

#### Default Value


* ""

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with selectedFolder value specified.
        $('#fileExplorer').ejFileExplorer({
        selectedFolder: "http://mvc.syncfusion.com/ODataServices/FileBrowser/Food",            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>

{% endhighlight %}



### selectedItems `string | array`
{:#members:selecteditems}

The selectedItems is used to select the specified items (file, folder) of FileExplorer control. 

#### Default Value


* ""

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with selectedItems value specified.
        $('#fileExplorer').ejFileExplorer({
        selectedItems: ["Food", "Nature"],            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"
        });
        </script>

{% endhighlight %}


### showCheckbox `boolean`
{:#members:showcheckbox}


Enables or disables the checkbox option in FileExplorer control.


#### Default Value


* true


#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the showCheckbox value specified.
        $('#fileExplorer').ejFileExplorer({ 
        showCheckbox: false,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                     
        });
        </script>

{% endhighlight %}




### showContextMenu `boolean`
{:#members:showcontextmenu}








Enables or disables the context menu option in FileExplorer control.




#### Default Value







* true








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the showContextMenu value specified.
        $('#fileExplorer').ejFileExplorer({ 
        showContextMenu: false,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                     
        });
        </script>

{% endhighlight %}







### showFooter `boolean`
{:#members:showfooter}








Enables or disables the footer in FileExplorer control. The footer element displays the details of the current selected files and folders. And also the footer having the switcher to change the layout view.




#### Default Value







* true








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the showFooter value specified.
        $('#fileExplorer').ejFileExplorer({ 
        showFooter: false,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                   
        });
        </script>

{% endhighlight %}



### showRoundedCorner `boolean`
{:#members:showroundedcorner}


FileExplorer control is displayed with rounded corner when this property is set to true.


#### Default Value


* false


#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // Initialize the FileExplorer with the showRoundedCorner value specified.
        $('#fileExplorer').ejFileExplorer({ 
        showRoundedCorner: true,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
        });
        </script>

{% endhighlight %}



### showThumbnail `boolean`
{:#members:showthumbnail}


FileExplorer control is rendered with thumbnail preview of images in Tile and LargeIcons layout when this property set to true.


#### Default Value


* true


#### Example


{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // Initialize the FileExplorer with the showThumbnail value specified.
        $('#fileExplorer').ejFileExplorer({ 
        showThumbnail: false,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
        });
        </script>

{% endhighlight %}



### showToolbar `boolean`
{:#members:showtoolbar}








Shows or disables the toolbar in FileExplorer control.




#### Default Value







* true








#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // Initialize the FileExplorer with the showToolbar value specified.
        $('#fileExplorer').ejFileExplorer({ 
        showToolbar: false,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
        });
        </script>

{% endhighlight %}







### showNavigationPane `boolean`
{:#members:shownavigationpane}








Enables or disables the navigation pane in FileExplorer control. The navigation pane contains a tree view element that displays all the folders from the filesystem in a hierarchical manner. This is useful to a quick navigation of any folder in the filesystem.




#### Default Value







* true








#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // Initialize the FileExplorer with the showNavigationPane value specified.
        $('#fileExplorer').ejFileExplorer({ 
        showNavigationPane: false,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                 
        }); 
        </script>

{% endhighlight %}







### tools `object`
{:#members:tools}








The tools property is used to configure and group required toolbar items in FileExplorer control.




#### Default Value







* { creation: ["NewFolder"], navigation: ["Back", "Forward", "Upward"], addressBar: ["Addressbar"], editing: ["Refresh", "Upload", "Delete", "Rename", "Download"], copyPaste: ["Cut", "Copy", "Paste"], getProperties: ["Details"], searchBar: ["Searchbar"], layout: ["Layout"]}








#### Example



{% highlight html %}
            
            <div id="fileExplorer" ></div> 
            
            <script>
            // Initialize the FileExplorer with toolbar tools value specified.
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
            </script>

{% endhighlight %}







### toolsList `array`
{:#members:toolslist}








The toolsList property is used to arrange the toolbar items in the FileExplorer control.




#### Default Value







* ["layout", "creation", "navigation", "addressBar", "editing", "copyPaste", "getProperties", "searchBar"]








#### Example



{% highlight html %}
        
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with toolsList value specified.
        $('#fileExplorer').ejFileExplorer({ 
        toolsList: ["navigation", "creation", "addressBar", "editing", "copyPaste", "getProperties", "searchBar"],
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                 
        }); 
        </script>

{% endhighlight %}







### uploadSettings `object`
{:#members:uploadsettings}








Gets or sets an object that indicates whether to customize the upload behavior in the FileExplorer.











### uploadSettings.maxFileSize `number`
{:#members:uploadsettings-maxfilesize}








Specifies the maximum file size allowed to upload. It accepts the value in bytes.




#### Default Value







* 31457280








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the maxFileSize value specified for uploadbox.
        $('#fileExplorer').ejFileExplorer({ 
        uploadSettings:{maxFileSize:10000},
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
        }); 
        </script>

{% endhighlight %}







### uploadSettings.allowMultipleFile `boolean`
{:#members:uploadsettings-allowmultiplefile}








Enables or disables the multiple files upload. When it is enabled, you can upload multiple files at a time and when disabled, you can upload only one file at a time.




#### Default Value







* true








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the multipleFilesSelection value specified for uploadbox.
        $('#fileExplorer').ejFileExplorer({ 
        uploadSettings:{allowMultipleFile:false},
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
        }); 
        </script>

{% endhighlight %}

### uploadSettings.autoUpload `boolean`
{:#members:uploadsettings-autoupload}








Enables or disables the auto upload option while uploading files in FileExplorer control.




#### Default Value







* false








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with auto upload option as true.
        $('#fileExplorer').ejFileExplorer({ 
        uploadSettings:{autoUpload:true},
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                
        }); 
        </script>

{% endhighlight %}







### width `string | number`
{:#members:width}








Specifies the width of FileExplorer control.




#### Default Value







* 850








#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // Initialize the FileExplorer with the width value specified.
        $('#fileExplorer').ejFileExplorer({   
        width: 800,
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"                     
        });
        </script>

{% endhighlight %}





## Methods



### adjustSize()
{:#methods:adjustsize}


Refresh the size of FileExplorer control.

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // refresh the size of FileExplorer 
        $('#fileExplorer').ejFileExplorer({      
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"           
        });
        // Create FileExplorer instance
        var feObj = $("#fileExplorer").data("ejFileExplorer");
        feObj.adjustSize(); // refresh the size of file explorer               
        </script>

{% endhighlight %}



### disableMenuItem(item)
{:#methods:disablemenuitem}


Disable the particular context menu item.

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
item</td>
<td class="type"><span class="param-type">string | element</span></td>
<td class="description">Id of the menu item/ Menu element to be disabled </td>
</tr>
</tbody>
</table>

#### Example



{% highlight html %}
 
        <div id="fileExplorer"></div> 
        
        <script>
        // disable the context menu item 
        $('#fileExplorer').ejFileExplorer({      
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"           
        });
        // Create FileExplorer instance
        var feObj = $("#fileExplorer").data("ejFileExplorer");
        feObj.disableMenuItem("Upload"); // disable upload option                         
        </script>

{% endhighlight %}



### disableToolbarItem(item)
{:#methods:disabletoolbaritem}








Disable the particular toolbar item.


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
item</td>
<td class="type"><span class="param-type">string | element</span></td>
<td class="description">Id of the toolbar item/ Tool item element to be disabled </td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // disable the toolbar tool 
        $('#fileExplorer').ejFileExplorer({      
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction"           
        });
        // Create FileExplorer instance
        var feObj = $("#fileExplorer").data("ejFileExplorer");
        feObj.disableToolbarItem("Searchbar"); // disable search bar                           
        </script>

{% endhighlight %}




### enableMenuItem(item)
{:#methods:enablemenuitem}

Enable the particular context menu item.

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
item</td>
<td class="type"><span class="param-type">string | Element</span></td>
<td class="description">Id of the menu item/ Menu element to be Enabled </td>
</tr>
</tbody>
</table>

#### Example



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
        </script>

{% endhighlight %}



### enableToolbarItem(item)
{:#methods:enabletoolbaritem}








Enable the particular toolbar item


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
item</td>
<td class="type"><span class="param-type">string | Element</span></td>
<td class="description">Id of the tool item/ Tool item element to be Enabled </td>
</tr>
</tbody>
</table>



#### Example



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
        </script>

{% endhighlight %}



### refresh()
{:#methods:refresh}


Refresh the content of the selected folder in FileExplorer control.

#### Example



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
        </script>

{% endhighlight %}



### removeToolbarItem(item)
{:#methods:removetoolbaritem}








Remove the particular toolbar item.

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
item</td>
<td class="type"><span class="param-type">string | Element</span></td>
<td class="description">Id of the tool item/ tool item element to be removed </td>
</tr>
</tbody>
</table>



#### Example



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
        </script>

{% endhighlight %}



## Events



### beforeAjaxRequest
{:#events:beforeajaxrequest}

Fires before the AJAX request is performed.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the AJAX request data</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // beforeAjaxRequest event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        beforeAjaxRequest: function (args) {}
        });
        </script>

{% endhighlight %}



### beforeDownload
{:#events:beforedownload}



Fires before downloading the files.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
files</td>
<td class="type"><span class="param-type">string[]</span></td>
<td class="description">returns the downloaded file names.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
path</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // beforeDownload event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        beforeDownload: function (args) {}
        });
        </script>

{% endhighlight %}




### beforeOpen
{:#events:beforeopen}



Fires before files or folders open.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
itemType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the opened item type.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
path</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // beforeOpen event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        beforeOpen: function (args) {}
        });
        </script>

{% endhighlight %}



### beforeUpload
{:#events:beforeupload}



Fires before uploading the files.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
path</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // beforeUpload event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        beforeUpload: function (args) {}
        });
        </script>

{% endhighlight %}



### create
{:#events:create}


Fires when FileExplorer control was created




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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/><span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>



### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // copy event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        create: function (args) {}
        });
        </script>

{% endhighlight %}





### copy
{:#events:copy}



Fires when file or folder is copied successfully.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
name</td>
<td class="type">
<span class="param-type">string[]</span></td>
<td class="description">returns the name of copied file/folder.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details.</td>
</tr>
<tr>
<td class="name">
sourcePath</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the source path.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // copy event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        copy: function (args) {}
        });
        </script>

{% endhighlight %}



### createFolder
{:#events:createfolder}



Fires when new folder is created successfully in file system.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the AJAX response data</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // createFolder event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        createFolder: function (args) {}
        });
        </script>

{% endhighlight %}



### cut
{:#events:cut}



Fires when file or folder is cut successfully.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
name</td>
<td class="type"><span class="param-type">string[]</span></td>
<td class="description">returns the name of moved file or folder.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details.</td>
</tr>
<tr>
<td class="name">
sourcePath</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the source path.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // cut event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        cut: function (args) {}
        });
        </script>

{% endhighlight %}



### destroy
{:#events:destroy}








Fires when the FileExplorer is destroyed successfully.

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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/><span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // destroy event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        destroy: function (args) {}
        });
        </script>

{% endhighlight %}





### layoutChange
{:#events:layoutchange}



Fires when the file view type is changed.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
isInteraction</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return true when we change the layout via interaction, else false.</td>
</tr>
<td class="name">
layoutType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current view type.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // layoutChange event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        layoutChange: function (args) {}
        });
        </script>

{% endhighlight %}



### open
{:#events:open}



Fires when files are successfully opened.
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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
itemType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the opened item type.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
path</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
        
        <div id="fileExplorer" ></div> 
        
        <script>
        // open event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        open: function (args) {}
        });
        </script>

{% endhighlight %}



### paste
{:#events:paste}



Fires when a file or folder is pasted successfully.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
name</td>
<td class="type"><span class="param-type">string[]</span></td>
<td class="description">returns the name of moved/copied file or folder.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details.</td>
</tr>
<tr>
<td class="name">
targetFolder</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target folder item details.</td>
</tr>
<tr>
<td class="name">
targetPath</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the target path.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // paste event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        paste: function (args) {}
        });
        </script>

{% endhighlight %}



### remove
{:#events:remove}



Fires when file or folder is deleted successfully.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the AJAX response data.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
name</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the names of deleted items.</td>
</tr>
<tr>
<td class="name">
path</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the path of deleted item.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the removed item details.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // remove event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        remove: function (args) {}
        });
        </script>

{% endhighlight %}



### resize
{:#events:resize}


Fires when resizing is performed for FileExplorer.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the mouse move event args.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // resize event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        resize: function (args) {}
        });
        </script>

{% endhighlight %}



### resizeStart
{:#events:resizestart}


Fires when resizing is started for FileExplorer.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the mouse down event args.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // resizeStart event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        resizeStart: function (args) {}
        });
        </script>

{% endhighlight %}



### resizeStop
{:#events:resizestop}


Fires this event when the resizing is stopped for FileExplorer.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the mouse leave event args.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // resizeStop event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",      
        resizeStop: function (args) {}
        });
        </script>

{% endhighlight %}



### select
{:#events:select}



Fires when the items from grid view or tile view of FileExplorer control is selected.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the FileExplorer model.</td>
</tr>
<tr>
<td class="name">
name</td>
<td class="type"><span class="param-type">string[]</span></td>
<td class="description">returns the name of selected items.</td>
</tr>
<tr>
<td class="name">
path</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the path of selected items.</td>
</tr>
<tr>
<td class="name">
selectedItems</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item details</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // select event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",        
        select: function (args) {}
        });
        </script>

{% endhighlight %}


### templateRefresh
{:#events:templaterefresh}



Triggered when refresh the template column elements in the grid view of FileExplorer control.

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
<td class="description">Event parameters from FileExplorer
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
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
cell</td>
<td class="type"><ts ref="ej.FileExplorer.Model"/>
<span class="param-type">object</span></td>
<td class="description">Returns the cell object.</td>
</tr>
<tr>
<td class="name">
column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the column object.</td>
</tr>
<tr>
<td class="name">
data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the current row data.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the grid model of FileExplorer.</td>
</tr>
<tr>
<td class="name">
rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the current row index.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
        <div id="fileExplorer" ></div> 
        
        <script>
        // select event for FileExplorer
        $('#fileExplorer').ejFileExplorer({            
        path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
        ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction",        
        templateRefresh: function (args) {}
        });
        </script>

{% endhighlight %}



