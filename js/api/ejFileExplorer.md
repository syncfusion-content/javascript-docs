---
layout: post
title: ejFileExplorer
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Html File Explorer control.










#### $(element).ejFileExplorer<span class="signature">(options)</span>







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
<td class="description last">settings for FileExplorer.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create File Explorer
$('#fileExplorer').ejFileExplorer({ 
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }
});
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:jquery.js


* module:jquery.globalize.js


* module:jquery.globalize.culture.en-US.js


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


* module:ej.grid.common.js


* module:ej.grid.base.js




### Members








#### ajaxAction<span class="type-signature type string">string</span>








Sets the Url of server side ajax handling method, which on going to handle file operation like Read, Delete, Renmae, Create, Upload, download, copy and Move in File Explorer.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with ajaxAction value specified.
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                       
});
&lt;/script&gt;</code>
</pre>






#### ajaxSettings<span class="type-signature type object">Object</span>








Using ajaxSettings property, we can customize the ajax settings. Normally we can customize following option in ajax handling data, url, type, async, contentType, dataType but here success function can't be customized. For upload and download API, we can customize url only.




Default Value:






* { read: {}, createFolder: {}, destroy: {}, rename: {}, paste: {}, getDetais: {}, download: {}, upload: {}}








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with ajaxSettings value specified.
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }
});
&lt;/script&gt;</code>
</pre>






#### cssClass<span class="type-signature type string">string</span>








Sets the root class for File explorer theme. This cssClass API helps to use custom skinning option for File explorer control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with cssClass value specified.
$('#fileExplorer').ejFileExplorer({ 
cssClass: 'gradient-lime',
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },
   });
&lt;/script&gt;</code>
</pre>






#### enableResize<span class="type-signature type boolean">boolean</span>








Enables/Disables the resize of file explorer, while window resizing




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with enableResize value specified.
$('#fileExplorer').ejFileExplorer({ 
 enableResize: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },                          
});
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Enables/Disables the Right to Left alignment support in file explorer




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with enableRTL value specified.
$('#fileExplorer').ejFileExplorer({ 
 enableRTL: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },                      
});
&lt;/script&gt;</code>
</pre>






#### fileTypes<span class="type-signature type string">string</span>








Allows specified type of files only to display in file explorer.




Default Value:






* "*.png,*.gif,*.jpg,*.jpeg"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Specifies the file types, which one need to allow in file explorer control
$('#fileExplorer').ejFileExplorer({ 
fileTypes: "*.png,*.gif,*.jpg,*.jpeg,*.docx",
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                       
});
&lt;/script&gt;</code>
</pre>






#### filterSettings<span class="type-signature type object">Object</span>








Gets or sets an object that indicates whether to customize the filtering behaviour of the file explorer











#### filterSettings.caseSensitiveSearch<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates to perform the filter operation with case sensitive




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Specifies the case sensitive for searching operation
$('#fileExplorer').ejFileExplorer({ 
caseSensitiveSearch: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }              
});
&lt;/script&gt;</code>
</pre>






#### filterSettings.filterType<span class="type-signature type enum">enum</span>








Sets the search filter type. There are several filter types are available such as "startswith", "contains", "endswith", "lessthan", "lessthanorequal", "greaterthan", "greaterthanorequal", "equal", "notequal". See <a href="global.html#filterType">filterType</a>




Default Value:






* ej.FileExplorer.filterType.StartsWith








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Specifies the filter types, which is used to filter the grid or list elements
$('#fileExplorer').ejFileExplorer({ 
filterType: "startswith",
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }           
});
&lt;/script&gt;</code>
</pre>






#### gridSettings<span class="type-signature type object">Object</span>








Gets or sets an object that indicates whether to customize the grid behaviour in the file explorer











#### gridSettings.allowSearching<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to enable dynamic searching behaviour in file explorer. Currently search box can be enabled through toolbar &#65533;tools&#65533;




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the allowSearching value specified for grid.
$('#fileExplorer').ejFileExplorer({ 
 gridSettings:{allowSearching:false},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                     
});
&lt;/script&gt;</code>
</pre>






#### gridSettings.allowSorting<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to enable the dynamic sorting behaviour on grid data. Sorting can be done through clicking on particular column header.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the allowSorting value specified for grid.
$('#fileExplorer').ejFileExplorer({ 
 gridSettings:{allowSorting:false},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                     
}); 
&lt;/script&gt;</code>
</pre>






#### gridSettings.columns<span class="type-signature type array">array</span>








Gets or sets an object that indicates to render the grid with specified columns, we can use this property same as column property in grid control




Default Value:






* [{ field: "name", headerText: "Name", width: 140 }, { field: "type", headerText: "Type", width: 95 }, { field: "size", headerText: "Size", width: 90 }, { field: "dateModified", headerText: "Date Modified", width: 140 }]








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the columns value specified for grid.
$('#fileExplorer').ejFileExplorer({ 
 gridSettings:{columns:[{ field: "name", headerText: "Name", width: 90 }, { field: "type", headerText: "Type", width: 95 }, { field: "size", headerText: "Size", width: 90 }]},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                     
}); 
&lt;/script&gt;</code>
</pre>






#### height<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Specifies the height of file explorer control




Default Value:






* 400








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the height value specified.
$('#fileExplorer').ejFileExplorer({   
height: 450,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                    
});
&lt;/script&gt;</code>
</pre>






#### isResponsive<span class="type-signature type boolean">boolean</span>








Enables/Disables the responsive support for FileExplorer control during the window resizing time.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with isResponsive value specified.
$('#fileExplorer').ejFileExplorer({ 
 isResponsive: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                      
});
&lt;/script&gt;</code>
</pre>






#### layout<span class="type-signature type enum">enum</span>








Sets the file view type. There are two view types are available such as &#65533;grid&#65533;, &#65533;tile&#65533; See layoutType




Default Value:






* ej.FileExplorer.layoutType.Grid








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the layout value specified.
$('#fileExplorer').ejFileExplorer({ 
layout: "grid",
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                      
}); 
&lt;/script&gt;</code>
</pre>






#### locale<span class="type-signature type string">string</span>








Sets the culture in FileExplorer.




Default Value:






* "en-US"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the culture value specified.
$('#fileExplorer').ejFileExplorer({ 
locale: "en-US",
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                    
});
&lt;/script&gt;</code>
</pre>






#### path<span class="type-signature type string">string</span>








Specifies the folder path to display in file Explorer,specified path will be consider as root path in file explorer




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Specifies the root folder path, which is need to specified in file explorer control
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }
ajaxAction: "@Url.Content("~/ImageBrowser/FileAction")"                           
});
&lt;/script&gt;</code>
</pre>






#### showContextMenu<span class="type-signature type boolean">boolean</span>








Enables/Disable the context menu option in file explorer control




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the showContextMenu value specified.
$('#fileExplorer').ejFileExplorer({ 
 showContextMenu: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                          
});
&lt;/script&gt;</code>
</pre>






#### showFooter<span class="type-signature type boolean">boolean</span>








Enables/Disable the file insert option in file explorer control




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the showFooter value specified.
$('#fileExplorer').ejFileExplorer({ 
showFooter: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                        
});
&lt;/script&gt;</code>
</pre>






#### showLayout<span class="type-signature type boolean">boolean</span>








Enables/Disable the file view in file explorer control




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the showLayout value specified.
$('#fileExplorer').ejFileExplorer({ 
showLayout: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                       
}); 
&lt;/script&gt;</code>
</pre>






#### showToolbar<span class="type-signature type boolean">boolean</span>








Shows/Disable the toolbar in file explorer control




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the showToolbar value specified.
$('#fileExplorer').ejFileExplorer({ 
 showToolbar: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                     
});
&lt;/script&gt;</code>
</pre>






#### showTreeview<span class="type-signature type boolean">boolean</span>








Enables/Disable the tree view in file explorer control




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the showTreeview value specified.
$('#fileExplorer').ejFileExplorer({ 
showTreeview: true,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                      
}); 
&lt;/script&gt;</code>
</pre>






#### tools<span class="type-signature type object">object</span>








Sets the tools in File Explorer.




Default Value:






* { creation:["NewFolder", "Open"], navigation: ["Back", "Forward"], addressBar: ["Addressbar"], editing: ["Refresh", "Upload", "Delete", "Rename", "Download"], copyPaste: ["Cut", "Copy", "Paste"], getProperties: ["Details"], searchBar: ["Searchbar"] }








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with toolbar tools value specified.
$('#fileExplorer').ejFileExplorer({ 
tools: {
  creation:["NewFolder", "Open"],
  navigation: ["Back", "Forward"],
  addressBar: ["Addressbar"],
  editing: ["Refresh", "Upload", "Delete", "Rename", "Download"],
  copyPaste: ["Cut", "Copy", "Paste"],
  getProperties: ["Details"],
  searchBar: ["Searchbar"]
},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }             
});
&lt;/script&gt;</code>
</pre>






#### toolsList<span class="type-signature type array">array</span>








Sets the toolsList in File Explorer. It mapped with tool types, which is available in tools property




Default Value:






* ["navigation", "addressBar", "editing", "copyPaste", "getProperties", "searchBar"]








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with toolsList value specified.
$('#fileExplorer').ejFileExplorer({ 
toolsList: ["creation","navigation", "addressBar", "editing", "copyPaste", "getProperties", "searchBar"],
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                      
}); 
&lt;/script&gt;</code>
</pre>






#### uploadBoxSettings<span class="type-signature type object">Object</span>








Gets or sets an object that indicates whether to customize the upload behaviour in the file explorer











#### uploadBoxSettings.fileSize<span class="type-signature type number">number</span>








Specifies the file size in bytes for uploading the file. This could be mentioned in number format.




Default Value:






* 31457280








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the fileSize value specified for uploadbox.
$('#fileExplorer').ejFileExplorer({ 
 uploadBoxSettings:{fileSize:10000},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                     
}); 
&lt;/script&gt;</code>
</pre>






#### uploadBoxSettings.multipleFilesSelection<span class="type-signature type boolean">boolean</span>








Enables/Disables the Multiple file selection, while uploading files in FileExplorer control.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the multipleFilesSelection value specified for uploadbox.
$('#fileExplorer').ejFileExplorer({ 
 uploadBoxSettings:{multipleFilesSelection:false},
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                     
}); 
&lt;/script&gt;</code>
</pre>






#### width<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Specifies the width of file explorer control




Default Value:






* 827








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// Initialize the File explorer with the width value specified.
$('#fileExplorer').ejFileExplorer({   
width: 810,
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                          
});
&lt;/script&gt;</code>
</pre>




### Methods








#### disableToolbarItem<span class="signature">()</span>








Disable the particular toolbar item





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// diable the toolbar tool 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.disableToolbarItem("fileExplorerSearchbar"); // disable search bar                           
&lt;/script&gt;</code>
</pre>






#### enableToolbarItem<span class="signature">()</span>








Enable the particular toolbar item





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// enable the toolbar tool 
$('#fileExplorer').ejFileExplorer({      
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   }                 
});
// Create FileExplorer instance
var feObj = $("#fileExplorer").data("ejFileExplorer");
feObj.enableToolbarItem("fileExplorerSearchbar"); // enable search bar                     
&lt;/script&gt;</code>
</pre>




### Events








#### copy








Fires while file or folder has been copied from one place to another place sucesfully

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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of copied file/folder</td>
</tr>
<tr>
<td class="name"><code>targetPath</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the target path</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// copy event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },
copy: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### createFolder








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// createFolder event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },
createFolder: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### layoutChange








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>layoutType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current view type.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// layoutChange event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },
layoutChange: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### move








Fires while file or folder has been moved from one place to another place sucesfully

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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of moved file/folder</td>
</tr>
<tr>
<td class="name"><code>targetPath</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the target path</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// move event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },
move: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### open








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>path</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the path of currently opened item.</td>
</tr>
<tr>
<td class="name"><code>itemType</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the opened item type</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// open event for File explorer
$('#fileExplorer').ejFileExplorer({            
* path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",         
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },
open: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### remove








Fires when file or folder ahs been deleted sucessfully

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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>path</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the path of deleted item</td>
</tr>
<tr>
<td class="name"><code>itemType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the deleted item type.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// remove event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },
remove: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### select








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the FileExplorer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of clicked item</td>
</tr>
<tr>
<td class="name"><code>itemType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of clicked item.</td>
</tr>
<tr>
<td class="name"><code>path</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the path of clicked item.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="fileExplorer" &gt;&lt;/div&gt; 
 
&lt;script&gt;
// select event for File explorer
$('#fileExplorer').ejFileExplorer({            
path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",           
ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction",      
ajaxSettings: {
       upload: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
       },
       download: {
           url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
       }
   },
select: function (args) {}
});
&lt;/script&gt;</code>
</pre>



