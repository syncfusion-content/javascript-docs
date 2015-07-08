---
layout: post
title: ejGrid
documentation: API
platform: js
metaname: 
metacontent: 
---

The grid can be easily configured to the DOM element, such as div. you can create a grid with a highly customizable look and feel.










$(element).ejGrid<span class="signature">(options)</span>







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
<td class="description last">settings for grid</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create Grid
$('#Grid').ejGrid({
    dataSource: window.gridData
});         
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:jquery.easing.min.js


* module:jquery.globalize.min.js


* module:jsrender.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.grid.js


* module:ej.pager.js


* module:ej.scroller.js


* module:ej.waitingpopup.js


* module:ej.radiobutton.js


* module:ej.dropdownlist.js


* module:ej.dialog.js


* module:ej.button.js


* module:ej.autocomplete.js


* module:ej.checkbox.js


* module:ej.datepicker.js


* module:ej.datetimepicker.js


* module:ej.editor.js


* module:ej.toolbar.js




## Members








### allowCellMerging<span class="type-signature type boolean">boolean</span>
{:#members-allowcellmerging}








Gets or sets a value that indicates whether to customizing cell based on our needs.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowCellMerging:true,
});
&lt;/script&gt; </code>
</pre>






### allowGrouping<span class="type-signature type boolean">boolean</span>
{:#members-allowgrouping}








Gets or sets a value that indicates whether to enable dynamic grouping behavior. Grouping can be done by drag on drop desired columns to grid&rsquo;s GroupDropArea. This can be further customized through &ldquo;groupSettings&rdquo; property.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowGrouping:true                      
});
&lt;/script&gt; </code>
</pre>






### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members-allowkeyboardnavigation}








Gets or sets a value that indicates whether to enable keyboard support for performing grid actions. selectionType &ndash; Gets or sets a value that indicates whether to enable single row or multiple rows selection behavior in grid. Multiple selection can be done through by holding CTRL and clicking the grid rows




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowKeyboardNavigation:false
});
&lt;/script&gt; </code>
</pre>






### allowMultipleExporting<span class="type-signature type boolean">boolean</span>
{:#members-allowmultipleexporting}








Gets or sets a value that indicates whether to enable dynamic filtering behavior on grid. Filtering can be used to limit the records displayed using required criteria and this can be further customized through &ldquo;filterSettings&rdquo; property




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering:true                       
});
&lt;/script&gt;</code>
</pre>






### allowMultiSorting<span class="type-signature type boolean">boolean</span>
{:#members-allowmultisorting}








Gets or sets a value that indicates whether to enable multi columns sorting behavior in grid. Sort multiple columns by holding CTRL and click on the corresponding column header.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowSorting:true,
  allowMultiSorting:true
});
&lt;/script&gt; </code>
</pre>






### allowPaging<span class="type-signature type boolean">boolean</span>
{:#members-allowpaging}








This specifies the grid to show the paginated data. Also enables pager control at the bottom of grid for dynamic navigation through data source. Paging can be further customized through &ldquo;pageSettings&rdquo; property.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>            
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowPaging:true                      
});
&lt;/script&gt;                 </code>
</pre>






### allowReordering<span class="type-signature type boolean">boolean</span>
{:#members-allowreordering}








Gets or sets a value that indicates whether to enable the columns reordering behavior in the grid. Reordering can be done through by drag and drop the particular column from one index to another index within the grid.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>                     
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowReordering:true
});
&lt;/script&gt; </code>
</pre>






### allowResizeToFit<span class="type-signature type boolean">boolean</span>
{:#members-allowresizetofit}








Gets or sets a value that indicates whether the column is non resizeable. Column width is set automatically based on the content or header text which is large.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowResizeToFit:true,
});
&lt;/script&gt; </code>
</pre>






### allowResizing<span class="type-signature type boolean">boolean</span>
{:#members-allowresizing}








Gets or sets a value that indicates whether to enable dynamic resizabiliy of columns. . Resize the width of the columns by simply click and move the particular column header line




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowResizing:true,
    allowScrolling:true,
    scrollSettings:{width:300,height:300}
});
&lt;/script&gt; </code>
</pre>






### allowScrolling<span class="type-signature type boolean">boolean</span>
{:#members-allowscrolling}








Gets or sets a value that indicates whether to enable the scrollbar in the grid and view the records by scroll through the grid manually




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowScrolling:true,
  scrollSettings:{width:300,height:100}
});
&lt;/script&gt; </code>
</pre>






### allowSearching<span class="type-signature type boolean">boolean</span>
{:#members-allowsearching}








Gets or sets a value that indicates whether to enable dynamic searching behavior in grid. Currently search box can be enabled through &ldquo;toolbarSettings&rdquo;




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowSearching: true,
    toolbarSettings:{showToolbar:true,toolbarItems:[ej.Grid.ToolBarItems.Search]}
});
&lt;/script&gt; </code>
</pre>






### allowSelection<span class="type-signature type boolean">boolean</span>
{:#members-allowselection}








Gets or sets a value that indicates whether user can select rows on grid. On enabling feature, selected row will be highlighted.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSelection:true                      
});
&lt;/script&gt; </code>
</pre>






### allowSorting<span class="type-signature type boolean">boolean</span>
{:#members-allowsorting}








Gets or sets a value that indicates whether to enable the dynamic sorting behavior on grid data. Sorting can be done through clicking on particular column header.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true                       
});
&lt;/script&gt; </code>
</pre>






### allowTextWrap<span class="type-signature type boolean">boolean</span>
{:#members-allowtextwrap}








Gets or sets a value that indicates whether the Content will wrap to the next line if the content exceeds the boundary of the Column Cells.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowTextWrap:true                      
});
&lt;/script&gt; </code>
</pre>






### childGrid<span class="type-signature type object">object</span>
{:#members-childgrid}








This specifies the grid to add the grid control inside the grid row of the parent with expand/collapse options




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>            
&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
   childGrid: {
dataSource: window.employeeView,
queryString: "EmployeeID",
}
});
&lt;/script&gt;</code>
</pre>






### columns<span class="type-signature type array">array</span>
{:#members-columns}








Gets or sets an object that indicates to render the grid with specified columns




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData
});
var value = $("#Grid").ejGrid("option", "columns");
&lt;/script&gt; </code>
</pre>






### columns.allowEditing<span class="type-signature type boolean">boolean</span>
{:#members-columns-allowediting}








Gets or sets a value that indicates whether to enable editing behavior for particular column.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings:{allowEditing:true},
  columns:[{field:"OrderID"},{field:"CustomerID",allowEditing:false},{field:"ShipCity"}] 
});
&lt;/script&gt; </code>
</pre>






### columns.allowFiltering<span class="type-signature type boolean">boolean</span>
{:#members-columns-allowfiltering}








Gets or sets a value that indicates whether to enable dynamic filtering behavior for particular column.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowFiltering:true,
  columns:[{field:"OrderID"},{field:"CustomerID",allowFiltering:false},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.allowGrouping<span class="type-signature type boolean">boolean</span>
{:#members-columns-allowgrouping}








Gets or sets a value that indicates whether to enable dynamic grouping behavior for particular column.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowGrouping:true,
  columns:[{field:"OrderID"},{field:"CustomerID",allowGrouping:false},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.allowSorting<span class="type-signature type boolean">boolean</span>
{:#members-columns-allowsorting}








Gets or sets a value that indicates whether to enable dynamic sorting behavior for particular column.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowSorting:true,
  columns:[{field:"OrderID"},{field:"CustomerID",allowSorting:false},{field:"ShipCity"}] 
});
&lt;/script&gt; </code>
</pre>






### columns.commands<span class="type-signature type array">array</span>
{:#members-columns-commands}








Gets or sets an object that indicates to define a command column in the grid.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    editSettings:{allowEditing:true,allowAdding:true,allowDeleting:true},
    columns:[
           { field: "OrderID", isPrimaryKey: true },  
           { field: "EmployeeID" },
           {
              headerText: "Manage Records",
              commands: [
                  { type: ej.Grid.UnboundType.Edit, buttonOptions: { text: "Edit" } },
                  { type: ej.Grid.UnboundType.Delete, buttonOptions: { text: "Delete" } },
                  { type: ej.Grid.UnboundType.Save, buttonOptions: { text: "Save" } },
                  { type: ej.Grid.UnboundType.Cancel, buttonOptions: { text: "Cancel" } }
               ],
              isUnbound: true,
              width: 130
           }
    ] 
});
&lt;/script&gt; </code>
</pre>






### columns.commands.buttonOptions<span class="type-signature type object">object</span>
{:#members-columns-commands-buttonoptions}








Gets or sets an object that indicates to define all the button options which are available in ejButton.




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    editSettings:{allowEditing:true,allowAdding:true,allowDeleting:true},
    columns:[
           { field: "OrderID", isPrimaryKey: true },  
           { field: "EmployeeID" },
           {
              headerText: "Manage Records",
              commands: [
                  { type: ej.Grid.UnboundType.Edit, buttonOptions: { text: "Edit" } },
                  { type: ej.Grid.UnboundType.Delete, buttonOptions: { text: "Delete" } },
                  { type: ej.Grid.UnboundType.Save, buttonOptions: { text: "Save" } },
                  { type: ej.Grid.UnboundType.Cancel, buttonOptions: { text: "Cancel" } }
               ],
              isUnbound: true, width: 130
           }
    ] 
});
&lt;/script&gt; </code>
</pre>






### columns.commands.type<span class="type-signature type enum">enum</span>
{:#members-columns-commands-type}








Gets or sets a value that indicates to add the command column button. See unboundType




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    editSettings:{allowEditing:true,allowAdding:true,allowDeleting:true},
    columns:[
           { field: "OrderID", isPrimaryKey: true },  
           { field: "EmployeeID" },
           {
              headerText: "Manage Records",
              commands: [
                  { type: ej.Grid.UnboundType.Edit, buttonOptions: { text: "Edit" } },
                  { type: ej.Grid.UnboundType.Delete, buttonOptions: { text: "Delete" } },
                  { type: ej.Grid.UnboundType.Save, buttonOptions: { text: "Save" } },
                  { type: ej.Grid.UnboundType.Cancel, buttonOptions: { text: "Cancel" } }
               ],
              isUnbound: true, width: 130
           }
    ] 
});
&lt;/script&gt; </code>
</pre>






### columns.cssClass<span class="type-signature type string">string</span>
{:#members-columns-cssclass}








Gets or sets a value that indicates to provide custom css for an individual column.




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;style class="temp"&gt;
.temp{
color:green;}
&lt;/style&gt;
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",cssClass:"temp"},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.customAttributes<span class="type-signature type object">object</span>
{:#members-columns-customattributes}








Gets or sets a value that indicates the attribute values to the td element of a particular column




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;          
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",customAttributes:{"style":"color:red"}},{field:"Freight"}]
});
&lt;/script&gt;  </code>
</pre>






### columns.dataSource<span class="type-signature type array">array</span>
{:#members-columns-datasource}








Gets or sets a value that indicates to bind the external datasource to the particular column when columnEditType as "dropdownedit" and also it is used to bind the datasource to the foreign key column while editing the grid. //Where data is array of JSON objects of text and value for the drop-down and array of JSON objects for foreign key column.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;  
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",visible:false},{field:"ShipCity"}]
});
&lt;/script&gt;</code>
</pre>






### columns.defaultValue<span class="type-signature type string/number/boolean/date">string/number/boolean/date</span>
{:#members-columns-defaultvalue}








Gets or sets a value that indicates to display the specified default value while adding a new record to the grid




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;          
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings: {allowAdding: true},
  toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add] },
  columns:[{field:"OrderID"},{field:"CustomerID"},{field:"ShipCity",defaultValue:"ABC"}]
});
&lt;/script&gt;</code>
</pre>






### columns.disableHtmlEncode<span class="type-signature type boolean">boolean</span>
{:#members-columns-disablehtmlencode}








Gets or sets a value that indicates to render the grid content and header with an html elements




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    columns:[{field:"OrderID",headerText:"&lt;div&amp;gtOrder ID&lt;/div&gt;",disableHtmlEncode:true}
  });
&lt;/script&gt;</code>
</pre>






### columns.editParams<span class="type-signature type object">object</span>
{:#members-columns-editparams}








Gets or sets a value that indicates to customize ejNumericTextbox of an editable column. See editingType




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    editSettings:{allowEditing:true,allowAdding:true,allowDeleting:true},
    columns:[{ field: "OrderID"}, { field: "Freight", editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }}]
  });
&lt;/script&gt;  </code>
</pre>






### columns.editTemplate<span class="type-signature type object">object</span>
{:#members-columns-edittemplate}








Gets or sets a template that displays a custom editor used to edit column values. See editTemplate




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings:{allowEditing:true},
  columns:[{field:"OrderID"},{field:"CustomerID"},
            { field: "EmployeeID",editTemplate: { create: function () { return "&lt;input&gt;"; }, read: function (args) { return args.ejMaskEdit("get_StrippedValue"); }, write: function (args) { args.element.ejMaskEdit({ width: "100%" ,maskFormat: "9",value: args.rowdata !== undefined ? args.rowdata["EmployeeID"]: "" }); } } }]
});
&lt;/script&gt; </code>
</pre>






### columns.editType<span class="type-signature type enum">enum</span>
{:#members-columns-edittype}








Gets or sets a value that indicates to render the element(based on edit type) for editing the grid record. . See editingType




Default Value:
{:.param}






* ej.Grid.EditingType.String








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings:{allowEditing:true},
  columns:[{field:"OrderID"},{field:"CustomerID"},{field:"Freight",editType:ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }}]
});
&lt;/script&gt; </code>
</pre>






### columns.field<span class="type-signature type string">string</span>
{:#members-columns-field}








Gets or sets a value that indicates to display the columns in the grid mapping with column name of the dataSource.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"}]
});
&lt;/script&gt; </code>
</pre>






### columns.foreignKeyField<span class="type-signature type string">string</span>
{:#members-columns-foreignkeyfield}








Gets or sets a value that indicates to define foreign key field name of the grid datasource.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;          
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"EmployeeID",foreignKeyField:"EmployeeID",foreignKeyValue:"FirstName",headerText:"FirstName",dataSource:window.employeeData },{field:"ShipCity"}]
});
&lt;/script&gt;</code>
</pre>






### columns.foreignKeyValue<span class="type-signature type string">string</span>
{:#members-columns-foreignkeyvalue}








Gets or sets a value that indicates to bind the field which is in foreign column datasource based on the foreignKeyField




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;  
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"EmployeeID",foreignKeyField:"EmployeeID",foreignKeyValue:"FirstName",dataSource:window.employeeData,headerText:"FirstName"},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.format<span class="type-signature type string">string</span>
{:#members-columns-format}








Gets or sets a value that indicates the format for the text applied on the column




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;          
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID"},{field:"Freight",format:"{0:C}"}]
});
&lt;/script&gt;  </code>
</pre>






### columns.headerTemplateID<span class="type-signature type string">string</span>
{:#members-columns-headertemplateid}








Gets or sets a value that indicates to add the template within the header element of the particular column.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;div id="customerTemplate"&gt;
&lt;span class="e-userlogin e-icon headericon"&gt;&lt;/span&gt;
 CUS ID
&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",headerTemplateID: "#customerTemplate"},{field:"CustomerID"},{field:"ShipCity"}]
});
&lt;/script&gt;</code>
</pre>






### columns.headerText<span class="type-signature type string">string</span>
{:#members-columns-headertext}








Gets or sets a value that indicates to display the title of that particular column.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",headerText:"Order ID"},{field:"CustomerID",headerText:"Customer ID"}]
});
&lt;/script&gt; </code>
</pre>






### columns.headerTextAlign<span class="type-signature type enum">enum</span>
{:#members-columns-headertextalign}








This defines the text alignment of a particular column header cell value. See headerTextAlign




Default Value:
{:.param}






* ej.TextAlign.Left








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",headerTextAlign:ej.TextAlign.Center},{field:"CustomerID",headerTextAlign:ej.TextAlign.Right},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.isFrozen<span class="type-signature type boolean">boolean</span>
{:#members-columns-isfrozen}








You can use this property to freeze selected columns in grid at the time of scrolling.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({             
  dataSource:window.gridData,
  allowScrolling: true,               
  scrollSettings:{width:500,height:100 }
  columns:[{field:"OrderID",isFrozen:true},{field:"CustomerID"},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.isIdentity<span class="type-signature type boolean">boolean</span>
{:#members-columns-isidentity}








Gets or sets a value that indicates thecolumn has an identity in the database.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",isIdentity:true},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.isPrimaryKey<span class="type-signature type boolean">boolean</span>
{:#members-columns-isprimarykey}








Gets or sets a value that indicates the column is act as a primary key(read-only) of the grid. The editing is performed based on the primary key column




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({             
  dataSource:window.gridData,
  editSettings:{allowEditing:true},
  columns:[{field:"OrderID",isPrimaryKey:true},{field:"CustomerID"},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.isUnbound<span class="type-signature type boolean">boolean</span>
{:#members-columns-isunbound}








Gets or sets a value that indicates whether to bind the column which are not in the datasource




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",isUnbound:false},{field:"CustomerID"},{field:"ShipCity",headerText:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.template<span class="type-signature type boolean">boolean</span>
{:#members-columns-template}








Gets or sets a value that indicates whether to enables column template for a particular column.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script id="columnTemplate" type="text/x-jsrender"&gt;
&lt;img src="styles/images/Employees/{{:EmployeeID}}.png" alt="{{:EmployeeID}}"/&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 dataSource:window.gridData,
 columns:[{headerText:"Employee",template:true,templateID:"#columnTemplate"},{field:"EmployeeID"}]
});
&lt;/script&gt;</code>
</pre>






### columns.templateID<span class="type-signature type string">string</span>
{:#members-columns-templateid}








Gets or sets a value that indicates to add the template as a particular column data .




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script id="columnTemplate" type="text/x-jsrender"&gt;
&lt;img src="styles/images/Employees/{{:EmployeeID}}.png" alt="{{:EmployeeID}}"/&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 dataSource:window.gridData,
 columns:[{headerText:"Employee",template:true,templateID:"#columnTemplate"},{field:"EmployeeID"}]
});
&lt;/script&gt;</code>
</pre>






### columns.textAlign<span class="type-signature type enum">enum</span>
{:#members-columns-textalign}








Gets or sets a value that indicates to align the text within the column. See textAlign




Default Value:
{:.param}






* ej.TextAlign.Left








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",textAlign:ej.TextAlign.Center},{field:"CustomerID",textAlign:ej.TextAlign.Right},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.type<span class="type-signature type string">string</span>
{:#members-columns-type}








Gets or sets a value that indicates to specify the datatype of the specified columns.




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    columns:[{ field: "OrderID"}, { field: "Verified",type: "boolean" }]
  });
&lt;/script&gt;  </code>
</pre>






### columns.validationRules<span class="type-signature type object">object</span>
{:#members-columns-validationrules}








Gets or sets a value that indicates to define constraints for saving data to the database.





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;          
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings: {allowEditing: true, allowAdding: true},
  columns:[{field:"OrderID", validationRules: { required: true, number: true }},{field:"CustomerID"},{field:"ShipCity"}] 
});
&lt;/script&gt; </code>
</pre>






### columns.visible<span class="type-signature type boolean">boolean</span>
{:#members-columns-visible}








Gets or sets a value that indicates whether this column is visible in the grid.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",visible:false},{field:"ShipCity"}]
});
&lt;/script&gt; </code>
</pre>






### columns.width<span class="type-signature type number">number</span>
{:#members-columns-width}








Gets or sets a value that indicates to define the width for a particular column in the grid.




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;          
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",width:50},{field:"CustomerID",width:"15%"},{field:"ShipCity",width:"70px"}]
});
&lt;/script&gt;</code>
</pre>






### contextMenuSettings<span class="type-signature type object">Object</span>
{:#members-contextmenusettings}








Gets or sets an object that indicates whether to customize the context menu behavior of the grid.











### contextMenuSettings.contextMenuItems<span class="type-signature type array">array</span>
{:#members-contextmenusettings-contextmenuitems}








Gets or sets a value that indicates whether to add the default context menu actions as a context menu items If enableContextMenu is true it will show all the items related to the target, if u want selected items from contextmenu u have to mention in the contextMenuItems




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowDeleting: true, allowEditing: true, allowAdding: true },
   allowGrouping: true,
   allowSorting: true,
   allowPaging: true,
   contextMenuSettings: { enableContextMenu: true, contextMenuItems:["Add Record,Edit Record,Delete Record"]  }
});
&lt;/script&gt;</code>
</pre>






### contextMenuSettings.customContextMenuItems<span class="type-signature type array">array</span>
{:#members-contextmenusettings-customcontextmenuitems}








Gets or sets a value that indicates whether to add custom contextMenu items within the toolbar to perform any action in the grid




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;style type="text/css" class="cssStyles"&gt;
&lt;/style&gt;
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData, 
  contextMenuSettings: { enableContextMenu: true, customContextMenuItems:["Hidden Columns,Visible Columns"]  }
});
&lt;/script&gt;</code>
</pre>






### contextMenuSettings.enableContextMenu<span class="type-signature type boolean">boolean</span>
{:#members-contextmenusettings-enablecontextmenu}








Gets or sets a value that indicates whether to enable the context menu action in the grid.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource: window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowDeleting: true, allowEditing: true, allowAdding: true },
   allowGrouping: true,
   allowSorting: true,
   allowPaging: true,
   contextMenuSettings: { enableContextMenu: true }
});
&lt;/script&gt; </code>
</pre>






### cssClass<span class="type-signature type string">string</span>
{:#members-cssclass}








Gets or sets a value that indicates to render the grid with custom theme. allowScrolling &ndash; Gets or sets a value that indicates whether to enable the scrollbar in the grid and view the records by scroll through the grid manually




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;style type="text/css"&gt;
   .gradient-green {
       font-family: cursive;
   }
   .gradient-green .e-alt_row {
       background: none repeat scroll 0 0 #71A409;
   }
&lt;/style&gt;
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   cssClass: "gradient-green"
});
&lt;/script&gt; </code>
</pre>






### dataSource<span class="type-signature type object">object</span>
{:#members-datasource}








Gets or sets the data to render the grid with records




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData
});
&lt;/script&gt; </code>
</pre>






### detailsTemplate<span class="type-signature type string">string</span>
{:#members-detailstemplate}








This specifies the grid to add the details row for the corresponding master row




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script id="templateData" type="text/x-jsrender"&gt;
&lt;table&gt;
&lt;tr&gt;
&lt;td&gt;
&lt;img src="styles/images/Employees/{{:EmployeeID}}.png" alt="{{:EmployeeID}}"/&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;/table&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  detailsTemplate:"#templateData",
  detailsDataBound: "detailGridData",
});             
&lt;/script&gt;             </code>
</pre>






### editSettings<span class="type-signature type object">Object</span>
{:#members-editsettings}








Gest or sets an object that indicates whether to customize the editing behavior of the grid.











### editSettings.allowAdding<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-allowadding}








Gets or sets a value that indicates whether to enable insert action in the editing mode.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowAdding: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["add"] }                             
});
&lt;/script&gt;                 </code>
</pre>






### editSettings.allowDeleting<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-allowdeleting}








Gets or sets a value that indicates whether to enable the delete action in the editing mode.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowDeleting: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["delete"] }      
});
&lt;/script&gt;                  </code>
</pre>






### editSettings.allowEditing<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-allowediting}








Gets or sets a value that indicates whether to enable the edit action in the editing mode.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }
});
&lt;/script&gt;              </code>
</pre>






### editSettings.allowEditOnDblClick<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-alloweditondblclick}








Gets or sets a value that indicates whether to enable the editing action while double click on the record




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>Defining editEvent with edit option:
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt; 
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, allowEditOnDblClick: false },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }      
});
&lt;/script&gt; </code>
</pre>






### editSettings.dialogEditorTemplateID<span class="type-signature type string">string</span>
{:#members-editsettings-dialogeditortemplateid}








This specifies the id of the template. This template can be used to display the data that you require to be edited using the Dialog Box




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>               
&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script id="template" type="text/template"&gt;
   &lt;table&gt;
       &lt;tr&gt;
           &lt;td&gt;OrderID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="OrderID" name="OrderID" value="{{: OrderID}}" disabled="disabled" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
       &lt;tr&gt;
           &lt;td&gt;CustomerID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="CustomerID" name="CustomerID" value="{{: CustomerID}}" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
       &lt;tr&gt;
           &lt;td&gt;EmployeeID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="EmployeeID" name="EmployeeID" value="{{: EmployeeID}}" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
   &lt;/table&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.DialogTemplate, dialogEditorTemplateID: "#template" },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
&lt;/script&gt;                </code>
</pre>






### editSettings.editMode<span class="type-signature type enum">enum</span>
{:#members-editsettings-editmode}








Gets or sets a value that indicates whether to define the mode of editing See editMode




Default Value:
{:.param}






* ej.Grid.EditMode.Normal








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.Dialog },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
&lt;/script&gt;                          </code>
</pre>






### editSettings.externalFormTemplateID<span class="type-signature type string">string</span>
{:#members-editsettings-externalformtemplateid}








- This specifies the id of the template. This template can be used to display the data that you require to be edited using the External edit form




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>               
&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script id="template" type="text/template"&gt;
   &lt;table&gt;
       &lt;tr&gt;
           &lt;td&gt;OrderID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="OrderID" name="OrderID" value="{{: OrderID}}" disabled="disabled" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
       &lt;tr&gt;
           &lt;td&gt;CustomerID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="CustomerID" name="CustomerID" value="{{: CustomerID}}" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
       &lt;tr&gt;
           &lt;td&gt;EmployeeID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="EmployeeID" name="EmployeeID" value="{{: EmployeeID}}" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
   &lt;/table&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.ExternalFormTemplate, externalFormTemplateID: "#template" },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
&lt;/script&gt;                </code>
</pre>






### editSettings.formPosition<span class="type-signature type enum">enum</span>
{:#members-editsettings-formposition}








This specifies to set the position of an External edit form either in the top-right or bottom-left of the grid




Default Value:
{:.param}






* ej.Grid.FormPosition.BottomLeft








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowAdding: true, allowEditing: true, editMode: ej.Grid.EditMode.ExternalForm, formPosition: ej.Grid.FormPosition.BottomLeft },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
&lt;/script&gt;    </code>
</pre>






### editSettings.inlineFormTemplateID<span class="type-signature type string">string</span>
{:#members-editsettings-inlineformtemplateid}








This specifies the id of the template. This template can be used to display the data that you require to be edited using the Inline edit form




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>               
&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script id="template" type="text/template"&gt;
   &lt;table&gt;
       &lt;tr&gt;
           &lt;td&gt;OrderID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="OrderID" name="OrderID" value="{{: OrderID}}" disabled="disabled" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
       &lt;tr&gt;
           &lt;td&gt;CustomerID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="CustomerID" name="CustomerID" value="{{: CustomerID}}" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
       &lt;tr&gt;
           &lt;td&gt;EmployeeID&lt;/td&gt;
           &lt;td&gt;
               &lt;input id="EmployeeID" name="EmployeeID" value="{{: EmployeeID}}" /&gt;&lt;/td&gt;
       &lt;/tr&gt;
   &lt;/table&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.InlineTemplateForm, inlineFormTemplateID: "#template" },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
&lt;/script&gt;                </code>
</pre>






### editSettings.rowPosition<span class="type-signature type enum">enum</span>
{:#members-editsettings-rowposition}








This specifies to set the position of an adding new row either in the top or bottom of the grid




Default Value:
{:.param}






* ej.Grid.RowPosition.top








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, allowAdding:true, rowPosition:"bottom" },
    toolbarSettings: { showToolbar: true, toolbarItems: ["add"]  },                             
});
&lt;/script&gt;                          </code>
</pre>






### editSettings.showConfirmDialog<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-showconfirmdialog}








Gets or sets a value that indicates whether the confirm dialog has to be shown while saving or discarding the batch changes




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.Batch, showConfirmDialog:false },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit","update","cancel"] }                             
});
&lt;/script&gt;                          </code>
</pre>






### editSettings.showDeleteConfirmDialog<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-showdeleteconfirmdialog}








Gets or sets a value that indicates whether the confirm dialog has to be shown while deleting record




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowDeleting: true, showDeleteConfirmDialog:true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit","update","cancel"] }                             
});
&lt;/script&gt;                          </code>
</pre>






### enableAltRow<span class="type-signature type boolean">boolean</span>
{:#members-enablealtrow}








Gets or sets a value that indicates whether to enable the alternative rows differentiation in the grid records based on corresponding theme.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  enableAltRow:true,
});
&lt;/script&gt; </code>
</pre>






### enableAutoSaveOnSelectionChange<span class="type-signature type boolean">boolean</span>
{:#members-enableautosaveonselectionchange}








Gets or sets a value that indicates whether to enable the save action in the grid through row selection




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    editSettings: { allowEditing: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["cancel", "save"]},
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    enableAutoSaveOnSelectionChange: false
});
&lt;/script&gt; </code>
</pre>






### enableHeaderHover<span class="type-signature type boolean">boolean</span>
{:#members-enableheaderhover}








Gets or sets a value that indicates whether to enable mouse over effect on the corresponding column header cell of the grid




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   enableHeaderHover:true
});
&lt;/script&gt; </code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members-enablepersistence}








Gets or sets a value that indicates whether to persist the grid model state in page using applicable medium i.e., HTML5 localStorage or cookies




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping: true,
    enablePresistence:true
});
&lt;/script&gt; </code>
</pre>






### enableResponsiveRow<span class="type-signature type boolean">boolean</span>
{:#members-enableresponsiverow}








Gets or sets a value that indicates whether the grid rows has to be rendered as detail view in mobile mode




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>       
&lt;div id="Grid"&gt;&lt;/div&gt; 
 
&lt;script type="text/javascript"&gt; 
$("#Grid").ejGrid({
  dataSource: window.gridData,
                isResponsive: true,
                enableResponsiveRow: true    
});  
&lt;/script&gt;</code>
</pre>






### enableRowHover<span class="type-signature type boolean">boolean</span>
{:#members-enablerowhover}








Gets or sets a value that indicates whether to enable mouse over effect on corresponding grid row.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   enableRowHover:true
});
&lt;/script&gt; </code>
</pre>






### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members-enablertl}








Align content in the grid control from right to left by setting the property as true.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  enableRTL:true,
});
&lt;/script&gt; </code>
</pre>






### enableTouch<span class="type-signature type boolean">boolean</span>
{:#members-enabletouch}








To Disable the mouse swipe property as false.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    enableTouch:false
});
&lt;/script&gt; </code>
</pre>






### filterSettings<span class="type-signature type object">Object</span>
{:#members-filtersettings}








Gets or sets an object that indicates whether to customize the filtering behavior of the grid











### filterSettings.enableCaseSensitivity<span class="type-signature type boolean">boolean</span>
{:#members-filtersettings-enablecasesensitivity}








Gets or sets a value that indicates to perform the filter operation with case sensitive in excel styled filter menu mode




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
    allowFiltering: true, 
    filterSettings: { enableCaseSensitivity:true, filterType:"excel"}                       
});
&lt;/script&gt;</code>
</pre>






### filterSettings.filterBarMode<span class="type-signature type enum">enum</span>
{:#members-filtersettings-filterbarmode}








This specifies the grid to starts the filter action while typing in the filterBar or after pressing the enter key. based on the filterBarMode. See filterBarMode




Default Value:
{:.param}






* ej.Grid.FilterBarMode.Immediate








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering: true, 
   filterSettings:{ filterBarMode: ej.Grid.FilterBarMode.OnEnter }                
});
&lt;/script&gt;</code>
</pre>






### filterSettings.filteredColumns<span class="type-signature type object">object</span>
{:#members-filtersettings-filteredcolumns}








Gets or sets a value that indicates whether to define the filtered columns details programmatically at initial load




Default Value:
{:.param}






* []














### filterSettings.filterType<span class="type-signature type enum">enum</span>
{:#members-filtersettings-filtertype}








This specifies the grid to show the filterBar or filterMenu to the grid records. See <a href="global.html#filterType">filterType</a>




Default Value:
{:.param}






* ej.Grid.FilterType.FilterBar








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering: true, 
   filterSettings: {  filterType: "menu" }                     
});
&lt;/script&gt;</code>
</pre>






### filterSettings.maxFilterChoices<span class="type-signature type number">number</span>
{:#members-filtersettings-maxfilterchoices}








Gets or sets a value that indicates the maximum number of filter choices that can be showed in the excel styled filter menu.




Default Value:
{:.param}






* 1000








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
    allowFiltering: true, 
    filterSettings: { maxFilterChoices:200, filterType:"excel"}                       
});
&lt;/script&gt;</code>
</pre>






### filterSettings.showFilterBarMessage<span class="type-signature type boolean">boolean</span>
{:#members-filtersettings-showfilterbarmessage}








This specifies the grid to show the filter text within the grid pager itself.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering: true, 
   filterSettings: {  showFilterBarStatus: true }                        
});
&lt;/script&gt;</code>
</pre>






### filterSettings.showPredicate<span class="type-signature type boolean">boolean</span>
{:#members-filtersettings-showpredicate}








Gets or sets a value that indicates whether to enable the predicate options in the filtering menu




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
    allowFiltering: true, 
    filterSettings: { showPredicate:true, filterType:"menu"}                       
});
&lt;/script&gt;</code>
</pre>






### groupSettings<span class="type-signature type object">Object</span>
{:#members-groupsettings}








Gets or sets an object that indicates whether to customize the grouping behavior of the grid.











### groupSettings.captionFormat<span class="type-signature type string">string</span>
{:#members-groupsettings-captionformat}








Gets or sets a value that customize the group caption format.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{captionFormat: "{{:field}} - {{:key}} : {{:count}} {{if count == 1 }} item {{else}} items {{/if}}"}                          
});
&lt;/script&gt; </code>
</pre>






### groupSettings.enableDropAreaAnimation<span class="type-signature type boolean">boolean</span>
{:#members-groupsettings-enabledropareaanimation}








Gets or sets a value that indicates whether to enable the animation effects to the group drop area




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowGrouping: true,
   enableDropAreaAnimation:true                        
});
&lt;/script&gt;            </code>
</pre>






### groupSettings.enableDropAreaAutoSizing<span class="type-signature type boolean">boolean</span>
{:#members-groupsettings-enabledropareaautosizing}








Gets or sets a value that indicates whether to enable animation button option in the group drop area of the grid.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{enableDropAreaAutoSizing: true}
});
&lt;/script&gt; </code>
</pre>






### groupSettings.groupedColumns<span class="type-signature type object">object</span>
{:#members-groupsettings-groupedcolumns}








Gets or sets a value that indicates whether to add grouped columns programmatically at initial load




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{groupedColumns:["OrderID"]}
});
&lt;/script&gt; </code>
</pre>






### groupSettings.showDropArea<span class="type-signature type boolean">boolean</span>
{:#members-groupsettings-showdroparea}








Gets or sets a value that indicates whether to show the group droparea just above the column header. It can be used to avoid ungrouping the already grouped column using groupsettings.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{showDropArea:false, groupedColumns: ["ShipCity"]},
    columns: [{ field: "OrderID" }, { field: "CustomerID" }, { field: "ShipCity" }]
});
&lt;/script&gt;   </code>
</pre>






### groupSettings.showGroupedColumn<span class="type-signature type boolean">boolean</span>
{:#members-groupsettings-showgroupedcolumn}








Gets or sets a value that indicates whether to hide the grouped columns from the grid




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{showGroupedColumn:false}
});
&lt;/script&gt; </code>
</pre>






### groupSettings.showToggleButton<span class="type-signature type boolean">boolean</span>
{:#members-groupsettings-showtogglebutton}








&ndash; Gets or sets a value that indicates whether to showthe group button image(toggle button)in the column header and also in the grouped column in the group drop area . It can be used to group/ungroup the columns by click on the toggle button.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{showToggleButton:true}
});
&lt;/script&gt;   </code>
</pre>






### groupSettings.showUngroupButton<span class="type-signature type boolean">boolean</span>
{:#members-groupsettings-showungroupbutton}








Gets or sets a value that indicates whether to enable the close button in the grouped column which is in the group drop area to ungroup the grouped column




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{showToggleButton: true, showUngroupButton:true}
});
&lt;/script&gt; </code>
</pre>






### isResponsive<span class="type-signature type boolean">boolean</span>
{:#members-isresponsive}








Gets or sets a value that indicates whether the grid design has be to made responsive.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>       
&lt;div id="Grid"&gt;&lt;/div&gt; 
 
&lt;script type="text/javascript"&gt; 
$("#Grid").ejGrid({
  dataSource: window.gridData,
                isResponsive: true 
});  
&lt;/script&gt;</code>
</pre>






### keySettings<span class="type-signature type object">object</span>
{:#members-keysettings}








This specifies to change the key in keyboard interaction to grid control




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>            
&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
   keySettings: {
saveRequest: "83",
moveCellRight: "13",
}
});
&lt;/script&gt;</code>
</pre>






### locale<span class="type-signature type string">string</span>
{:#members-locale}








Gets or sets a value that indicates whether to customizing the user interface (UI) as locale-specific in order to display regional data i.e. in a language and culture specific to a particular country or region.




Default Value:
{:.param}






* "en-US"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
ej.Pager.locale["es-ES"] = {
   pagerInfo: "{0} de {1} p&aacute;ginas ({2} art&iacute;culos)"
};
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowPaging:true,
  locale : "es-ES" 
});
&lt;/script&gt;             </code>
</pre>






### minWidth<span class="type-signature type number">number</span>
{:#members-minwidth}








Gets or sets a value that indicates whether to set the minimum width of the responsive grid while isResponsive property is true and enableResponsiveRow property is set as false.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData, 
  minWidth: 990,
  isResponsive: true
});
&lt;/script&gt;</code>
</pre>






### pageSettings<span class="type-signature type object">Object</span>
{:#members-pagesettings}








Gets or sets an object that indicates whether to modify the pager default configuration.











### pageSettings.currentPage<span class="type-signature type number">number</span>
{:#members-pagesettings-currentpage}








Gets or sets a value that indicates whether to define which page to display currently in the grid




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true,   
    pageSettings: { currentPage: 1 }
});
&lt;/script&gt;</code>
</pre>






### pageSettings.enableQueryString<span class="type-signature type boolean">boolean</span>
{:#members-pagesettings-enablequerystring}








Gets or sets a value that indicates whether to pass the current page information as a query string along with the url while navigating to other page.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true,   
    pageSettings: {enableQueryString: true }
});
&lt;/script&gt;</code>
</pre>






### pageSettings.enableTemplates<span class="type-signature type bool">bool</span>
{:#members-pagesettings-enabletemplates}








Gets or sets a value that indicates whether to enables pager template for the grid.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script id="pagerTemplate" type="text/x-jsrender"&gt;
 &lt;input type="text" id="txtPageNumber"  value="" style="width: 45px; border: none; cursor: text" /&gt;
&lt;input type="button" value="Go" style="border: none; cursor: pointer" id="btnGo" onclick="gotoPage(this)" /&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 dataSource:window.gridData,
 pageSettings:{enableTemplates:true,template:"#pagerTemplate"}
});
&lt;/script&gt;</code>
</pre>






### pageSettings.pageCount<span class="type-signature type number">number</span>
{:#members-pagesettings-pagecount}








Gets or sets a value that indicates whether to define the number of pages displayed in the pager for navigation




Default Value:
{:.param}






* 8








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    allowPaging: true,    
    pageSettings: { pageCount: 1 }
});
&lt;/script&gt;</code>
</pre>






### pageSettings.pageSize<span class="type-signature type number">number</span>
{:#members-pagesettings-pagesize}








Gets or sets a value that indicates whether to define the number of records displayed per page




Default Value:
{:.param}






* 12








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,
    allowPaging: true,   
    pageSettings: { pageSize: 2 }
});
&lt;/script&gt;</code>
</pre>






### pageSettings.showDefaults<span class="type-signature type bool">bool</span>
{:#members-pagesettings-showdefaults}








Gets or sets a value that indicates whether to enables default pager for the grid.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script id="pagerTemplate" type="text/x-jsrender"&gt;
 &lt;input type="text" id="txtPageNumber"  value="" style="width: 45px; border: none; cursor: text" /&gt;
&lt;input type="button" value="Go" style="border: none; cursor: pointer" id="btnGo" /&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 dataSource:window.gridData,
 pageSettings:{showDefaults:true,enableTemplates:true,templateID:"#pagerTemplate"}
});
&lt;/script&gt;</code>
</pre>






### pageSettings.template<span class="type-signature type string">string</span>
{:#members-pagesettings-template}








Gets or sets a value that indicates to add the template as a pager template for grid.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script id="pagerTemplate" type="text/x-jsrender"&gt;
 &lt;input type="text" id="txtPageNumber"  value="" style="width: 45px; border: none; cursor: text" /&gt;
&lt;input type="button" value="Go" style="border: none; cursor: pointer" id="btnGo" /&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 dataSource:window.gridData,
 pageSettings:{enableTemplates:true,template:"#pagerTemplate"}
});
&lt;/script&gt;</code>
</pre>






### pageSettings.totalPages<span class="type-signature type number">number</span>
{:#members-pagesettings-totalpages}








Get the value of total number of pages in the grid. The totalPages value is calculated based on pagesize and totalrecords of grid




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;div id="print"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true    
});
var value = $("#Grid").ejGrid("option", "pageSettings.totalPages");
$("#print").text("TotalPages: " + value);
&lt;/script&gt;</code>
</pre>






### pageSettings.totalRecordsCount<span class="type-signature type number">number</span>
{:#members-pagesettings-totalrecordscount}








Get the value of total number of records which is bound to the grid. The totalRecordsCount value is calculated based on dataSource bound to the grid.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;div id="print"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true
});
var value = $("#Grid").ejGrid("option", "pageSettings.totalRecordsCount");
$("#print").text("TotalRecordsCount: " + value);
&lt;/script&gt;</code>
</pre>






### query<span class="type-signature type object">object</span>
{:#members-query}








Query the dataSource from the table for Grid.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>       
&lt;div id="Grid"&gt;&lt;/div&gt; 
 
&lt;script type="text/javascript"&gt;
var queryOrder=ej.Query().select(["OrderID", "CustomerID"]); 
$("#Grid").ejGrid({
  dataSource: window.gridData,
  query: queryOrder
});  
&lt;/script&gt;</code>
</pre>






### rowTemplate<span class="type-signature type string">string</span>
{:#members-rowtemplate}








Gets or sets a value that indicates to render the grid with template rows. The template row must be a table row. That table row must have the JavaScript render binding format ({{:columnName}}) then the grid data source binds the data to the corresponding table row of the template.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script id="templateData" type="text/x-jsrender"&gt;
&lt;tr&gt;
&lt;td&gt;
&lt;img src="styles/images/Employees/{{:EmployeeID}}.png" alt="{{:EmployeeID}}"/&gt;
&lt;/td&gt;
&lt;td&gt;
{{:EmployeeID}}
&lt;/td&gt;
&lt;/tr&gt;
&lt;/script&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 dataSource:window.gridData,
  rowTemplate:"#templateData",
  columns:[{headerText:"Employeephoto"},{field:"EmployeeID",headerText:"EmployeeID"}],
});
&lt;/script&gt;</code>
</pre>






### scrollSettings<span class="type-signature type object">Object</span>
{:#members-scrollsettings}








Gets or sets an object that indicates whether to customize the scrolling behavior of the grid.











### scrollSettings.allowVirtualScrolling<span class="type-signature type boolean">boolean</span>
{:#members-scrollsettings-allowvirtualscrolling}








This specify the grid to to view data that you require without buffering the entire load of a huge database




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{width:300,height:100,allowVirtualScrolling:true}
});
&lt;/script&gt; </code>
</pre>






### scrollSettings.enableTouchScroll<span class="type-signature type boolean">boolean</span>
{:#members-scrollsettings-enabletouchscroll}








This specify the grid to enable/disable touch control for scrolling.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{ enableTouchScroll:true }
});
&lt;/script&gt; </code>
</pre>






### scrollSettings.frozenColumns<span class="type-signature type number">number</span>
{:#members-scrollsettings-frozencolumns}








This specify the grid to freeze particular columns at the time of scrolling.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowScrolling: true,               
    scrollSettings:{width:500,height:100,frozenColumns:2 }
});  
&lt;/script&gt; </code>
</pre>






### scrollSettings.frozenRows<span class="type-signature type number">number</span>
{:#members-scrollsettings-frozenrows}








This specify the grid to freeze particular rows at the time of scrolling.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowScrolling: true,               
    scrollSettings:{width:300,height:200,frozenRows:2 }
});
&lt;/script&gt; </code>
</pre>






### scrollSettings.height<span class="type-signature type number">number</span>
{:#members-scrollsettings-height}








This specify the grid to show the vertical scroll bar, to scroll and view the grid contents.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{ height:100 }
});
&lt;/script&gt; </code>
</pre>






### scrollSettings.virtualScrollMode<span class="type-signature type enum">enum</span>
{:#members-scrollsettings-virtualscrollmode}








This is used to define the mode of virtual scrolling in grid. See virtualScrollMode




Default Value:
{:.param}






* ej.Grid.VirtualScrollMode.Normal








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource: window.gridData,                     
    allowScrolling:true,
    scrollSettings:{ width:500 , height: 550 , allowVirtualScrolling:true, virtualScrollMode:ej.Grid.VirtualScrollMode.Normal }
});
&lt;/script&gt;                          </code>
</pre>






### scrollSettings.width<span class="type-signature type number">number</span>
{:#members-scrollsettings-width}








This specify the grid to show the horizontal scroll bar, to scroll and view the grid contents




Default Value:
{:.param}






* 250








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{ width:300 }
});
&lt;/script&gt; </code>
</pre>






### selectedRecords<span class="type-signature type array">array</span>
{:#members-selectedrecords}








Gets a value that indicates whether the grid model to hold multiple selected records . selectedRecords can be used to displayed hold the single or multiple selected records using &ldquo;selectedRecords&rdquo; property




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
});                       
&lt;/script&gt;
&lt;script&gt;
// display single or multiple selected records
$("#Grid").ejGrid("model.selectedRecords")        
&lt;/script&gt;</code>
</pre>






### selectedRowIndex<span class="type-signature type number">number</span>
{:#members-selectedrowindex}








Gets or sets a value that indicates to select the row while initializing the grid




Default Value:
{:.param}






* -1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    selectedRowIndex:1
});
&lt;/script&gt; </code>
</pre>






### selectionSettings<span class="type-signature type object">Object</span>
{:#members-selectionsettings}








This property is used to configure the selection behavior of the grid.











### selectionSettings.enableToggle<span class="type-signature type boolean">boolean</span>
{:#members-selectionsettings-enabletoggle}








Gets or sets a value that indicates whether to enable the toggle selction behavior for row, cell and column.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowSelection: true,   
    selectionSettings: {enableToggle: true }
});
&lt;/script&gt;</code>
</pre>






### selectionSettings.selectionMode<span class="type-signature type enum">enum</span>
{:#members-selectionsettings-selectionmode}








Gets or sets a value that indicates whether to add the default selection actions as a seleciton mode.See selectionMode




Default Value:
{:.param}






* ["row"]








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSelection: true,   
   selectionSettings: {selectionMode: ["row","cell","column"] }
});
&lt;/script&gt;</code>
</pre>






### selectionType<span class="type-signature type enum">enum</span>
{:#members-selectiontype}








The row selection behavior of grid. Accepting types are "single" and "multiple".




Default Value:
{:.param}






* ej.Grid.SelectionType.Single








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   selectionType:"multiple"
});
&lt;/script&gt; </code>
</pre>






### showAddNewRow<span class="type-signature type boolean">boolean</span>
{:#members-showaddnewrow}








This specifies to add new editable row dynamically at the either top or bottom of the grid.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
dataSource:window.gridData,
columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
editSettings: { allowEditing: true, allowAdding:true, rowPosition:"bottom", showAddNewRow: true },
});
&lt;/script&gt; </code>
</pre>






### showAddNewRow<span class="type-signature type boolean">boolean</span>
{:#members-showaddnewrow}








This specifies to add new editable row dynamically at the top or bottom of the grid.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
dataSource:window.gridData,
columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
editSettings: { allowEditing: true, allowAdding:true, rowPosition:"bottom", showAddNewRow: true },
});
&lt;/script&gt; </code>
</pre>






### showColumnChooser<span class="type-signature type boolean">boolean</span>
{:#members-showcolumnchooser}








Gets or sets a value that indicates whether to enable column chooser on grid. On enabling feature able to show/hide grid columns




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>            
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    showColumnChooser:true                      
});
&lt;/script&gt;                 </code>
</pre>






### showStackedHeader<span class="type-signature type boolean">boolean</span>
{:#members-showstackedheader}








Gets or sets a value that indicates stacked header should be shown on grid layout when the property &ldquo;stackedHeaderRows&rdquo; is set.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true,
   showStackedHeader:true,
   stackedHeaderRows:[{stackedHeaderColumns:[{headerText:"ID &amp; Freight",column:"CustomerID"}
         ,{headerText:"Frieght",column:"Freight,EmployeeID,OrderDate"}
         ,{headerText:"Date &amp; Location Top Level",column:"ShipCity"}
           ]}
          ],
   columns: [
      { field: "CustomerID", headerText: "Customer ID", width: 80 },
       { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
      { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
       { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
      { field: "ShipCity", headerText: "Ship City", width: 110 }
      ]
});
&lt;/script&gt; </code>
</pre>






### showSummary<span class="type-signature type boolean">boolean</span>
{:#members-showsummary}








Gets or sets a value that indicates summary rows should be shown on grid layout when the property &ldquo;summaryRows&rdquo; is set




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    dataSource:window.gridData,
    columns: [{ field: "OrderID"}, { field: "Freight" }, { field: "ShipCity" }],
    showSummary:true,
    summaryRows:[{ title: "sum", summaryColumns: [{summaryType:ej.Grid.SummaryType.Count,displayColumn:"Freight",dataMember:"Freight"}]}]       
});
&lt;/script&gt;  </code>
</pre>






### sortSettings<span class="type-signature type object">Object</span>
{:#members-sortsettings}








Gets or sets a value that indicates whether to customize the sorting behavior of the grid.











### sortSettings.sortedColumns.direction<span class="type-signature type string">string</span>
{:#members-sortsettings-sortedcolumns-direction}








Gets or sets a value that indicates whether to define the direction to sort the column.




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;          
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field: "OrderID"},{field: "EmployeeID"}],
  sortSettings: {sortedColumns: [{field:"EmployeeID", direction:"descending"}] }                    
});
&lt;/script&gt;  </code>
</pre>






### sortSettings.sortedColumns.field<span class="type-signature type string">string</span>
{:#members-sortsettings-sortedcolumns-field}








Gets or sets a value that indicates whether to define the field name of the column to be sort




Default Value:
{:.param}






* -








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;          
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field: "OrderID"},{field: "EmployeeID"}],
  sortSettings: {sortedColumns: [{field:"EmployeeID"}] }             
});
&lt;/script&gt;  </code>
</pre>






### stackedHeaderRows<span class="type-signature type array">array</span>
{:#members-stackedheaderrows}








Gets or sets an object that indicates to managing the collection of stacked header rows for the grid.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true,
   showStackedHeader:true,
   stackedHeaderRows:[{stackedHeaderColumns:[{headerText:"ID &amp; Freight",column:"CustomerID"}
         ,{headerText:"Frieght",column:"Freight,EmployeeID,OrderDate"}
         ,{headerText:"Date &amp; Location Top Level",column:"ShipCity"}
           ]}
          ],
   columns: [
      { field: "CustomerID", headerText: "Customer ID", width: 80 },
       { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
      { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
       { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
      { field: "ShipCity", headerText: "Ship City", width: 110 }
      ]
});
&lt;/script&gt; </code>
</pre>






### stackedHeaderRows.stackedHeaderColumns<span class="type-signature type array">array</span>
{:#members-stackedheaderrows-stackedheadercolumns}








Gets or sets a value that indicates whether to add stacked header columns into the stacked header rows




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true,
   showStackedHeader:true,
   stackedHeaderRows:[{stackedHeaderColumns:[{headerText:"ID &amp; Freight",column:"CustomerID"}
         ,{headerText:"Frieght",column:"Freight,EmployeeID,OrderDate"}
         ,{headerText:"Date &amp; Location Top Level",column:"ShipCity"}
           ]}
          ],
   columns: [
      { field: "CustomerID", headerText: "Customer ID", width: 80 },
       { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
      { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
       { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
      { field: "ShipCity", headerText: "Ship City", width: 110 }
      ]
});
&lt;/script&gt; </code>
</pre>






### stackedHeaderRows.stackedHeaderColumns.column<span class="type-signature type string">string</span>
{:#members-stackedheaderrows-stackedheadercolumns-column}








Gets or sets a value that indicates the header text for the particular stacked header column.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true,
   showStackedHeader:true,
   stackedHeaderRows:[{stackedHeaderColumns:[{headerText:"ID &amp; Freight",column:"CustomerID"}
         ,{headerText:"Frieght",column:"Freight,EmployeeID,OrderDate"}
         ,{headerText:"Date &amp; Location Top Level",column:"ShipCity"}
           ]}
          ],
   columns: [
      { field: "CustomerID", headerText: "Customer ID", width: 80 },
       { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
      { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
       { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
      { field: "ShipCity", headerText: "Ship City", width: 110 }
      ]
});
&lt;/script&gt; </code>
</pre>






### stackedHeaderRows.stackedHeaderColumns.cssClass<span class="type-signature type string">string</span>
{:#members-stackedheaderrows-stackedheadercolumns-cssclass}








Gets or sets a value that indicates class to the corresponding stackedHeaderColumn.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt;       
&lt;style class="temp"&gt;
.temp{
color:green;}
&lt;/style&gt;
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true,
   showStackedHeader:true,
   stackedHeaderRows:[{stackedHeaderColumns:[{headerText:"ID &amp; Freight",column:"CustomerID", cssClass:
         "temp"},{headerText:"Frieght",column:"Freight,EmployeeID,OrderDate"}
         ,{headerText:"Date &amp; Location Top Level",column:"ShipCity"}
           ]}
          ],
   columns: [
      { field: "CustomerID", headerText: "Customer ID", width: 80 },
      { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
      { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
      { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign:           ej.TextAlign.Right },
      { field: "ShipCity", headerText: "Ship City", width: 110 }
      ]
});
&lt;/script&gt; </code>
</pre>






### stackedHeaderRows.stackedHeaderColumns.headerText<span class="type-signature type string">string</span>
{:#members-stackedheaderrows-stackedheadercolumns-headertext}








Gets or sets a value that indicates the header text for the particular stacked header column.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true,
   showStackedHeader:true,
   stackedHeaderRows:[{stackedHeaderColumns:[{headerText:"ID &amp; Freight",column:"CustomerID"}
         ,{headerText:"Frieght",column:"Freight,EmployeeID,OrderDate"}
         ,{headerText:"Date &amp; Location Top Level",column:"ShipCity"}
           ]}
          ],
   columns: [
      { field: "CustomerID", headerText: "Customer ID", width: 80 },
       { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
      { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
       { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
      { field: "ShipCity", headerText: "Ship City", width: 110 }
      ]
});
&lt;/script&gt; </code>
</pre>






### stackedHeaderRows.stackedHeaderColumns.textAlign<span class="type-signature type string">string</span>
{:#members-stackedheaderrows-stackedheadercolumns-textalign}








Gets or sets a value that indicates the text alignment of the corresponding headerText.




Default Value:
{:.param}






* ej.TextAlign.Left








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true,
   showStackedHeader:true,
   stackedHeaderRows:[{stackedHeaderColumns:[{headerText:"ID &amp; Freight",column:"CustomerID", textalign: 
         ej.TextAlign.Right},{headerText:"Frieght",column:"Freight,EmployeeID,OrderDate"}
         ,{headerText:"Date &amp; Location Top Level",column:"ShipCity"}
           ]}
          ],
   columns: [
      { field: "CustomerID", headerText: "Customer ID", width: 80 },
      { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
      { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
      { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
      { field: "ShipCity", headerText: "Ship City", width: 110 }
      ]
});
&lt;/script&gt; </code>
</pre>






### summaryRows<span class="type-signature type array">array</span>
{:#members-summaryrows}








Gets or sets an object that indicates to managing the collection of summary rows for the grid.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,
     showSummary: true,
     columns:[{field: "OrderID"},{field: "Freight"}],
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }]
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.showCaptionSummary<span class="type-signature type boolean">boolean</span>
{:#members-summaryrows-showcaptionsummary}








Gets or sets a value that indicates whether to show the summary value within the group caption area for the corresponding summary column while grouping the column




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,  
     columns:[{field: "OrderID"},{field: "Freight"}],
     allowGrouping: true,
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }],
        showCaptionSummary: true
     }]                                    
});
&lt;/script&gt;           </code>
</pre>






### summaryRows.showTotalSummary<span class="type-signature type boolean">boolean</span>
{:#members-summaryrows-showtotalsummary}








Gets or sets a value that indicates whether to show the total summary value the for the corresponding summary column. The summary row is added after the grid content.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData, 
     columns:[{field: "OrderID"},{field: "Freight"}],
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }],
        showTotalSummary: true
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.summaryColumns<span class="type-signature type object">object</span>
{:#members-summaryrows-summarycolumns}








Gets or sets a value that indicates whether to add summary columns into the summary rows.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData, 
     columns:[{field: "OrderID"},{field: "Freight"}],
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }]
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.summaryColumns.customSummaryValue<span class="type-signature type string">string</span>
{:#members-summaryrows-summarycolumns-customsummaryvalue}








Gets or sets a value that indicates the text displayed in the summary column as a value




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,
     columns:[{field: "OrderID"},{field: "Freight"}],
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Custom,
           displayColumn: "Freight",
           dataMember: "Freight",
           customSummaryValue : "Currency"
        }]
     }]                                    
});    
&lt;/script&gt; </code>
</pre>






### summaryRows.summaryColumns.dataMember<span class="type-signature type string">string</span>
{:#members-summaryrows-summarycolumns-datamember}








This specifies summary column used to perform the summary calculation




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,
     columns:[{field: "OrderID"},{field: "Freight"}],
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }]
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.summaryColumns.displayColumn<span class="type-signature type string">string</span>
{:#members-summaryrows-summarycolumns-displaycolumn}








Gets or sets a value that indicates to define the target column at which to display the summary.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,
     columns:[{field: "OrderID"},{field: "Freight"}],
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }]
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.summaryColumns.format<span class="type-signature type string">string</span>
{:#members-summaryrows-summarycolumns-format}








Gets or sets a value that indicates the format for the text applied on the column




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,
     columns:[{field: "OrderID"},{field: "Freight"}],
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight",
           format: "{0:C2}"
        }]
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.summaryColumns.prefix<span class="type-signature type string">string</span>
{:#members-summaryrows-summarycolumns-prefix}








Gets or sets a value that indicates the text displayed before the summary column value




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight",
           prefix : "Currency:"
        }]
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.summaryColumns.suffix<span class="type-signature type string">string</span>
{:#members-summaryrows-summarycolumns-suffix}








Gets or sets a value that indicates the text displayed after the summary column value




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,
     columns:[{field: "OrderID"},{field: "Freight"}],
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight",
           suffix: "/-"
        }]
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.summaryColumns.summaryType<span class="type-signature type object">object</span>
{:#members-summaryrows-summarycolumns-summarytype}








Gets or sets a value that indicates the type of calculations to be performed for the corresponding summary column




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData, 
     columns:[{field: "OrderID"},{field: "Freight"}],
     showSummary: true,
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }]
     }]                                    
});
&lt;/script&gt; </code>
</pre>






### summaryRows.title<span class="type-signature type string">string</span>
{:#members-summaryrows-title}








This specifies the grid to show the title for the summary rows.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
     dataSource:window.gridData,  
     showSummary: true,
     columns:[{field: "OrderID"},{field: "Freight"}],
     summaryRows: [{
        title: "Sum",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }]
     }]                                    
});
&lt;/script&gt;</code>
</pre>






### toolbarSettings<span class="type-signature type object">Object</span>
{:#members-toolbarsettings}








Gets or sets an object that indicates whether to enable the toolbar in the grid and add toolbar items











### toolbarSettings.customToolbarItems<span class="type-signature type object">object</span>
{:#members-toolbarsettings-customtoolbaritems}








Gets or sets a value that indicates whether to add custom toolbar items within the toolbar to perform any action in the grid




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;style type="text/css" class="cssStyles"&gt;
  .Expand:before
  {
    content:"\e627";
  }
&lt;/style&gt;
&lt;script&gt;
$("#Grid").ejGrid({
  dataSource:window.gridData, 
  toolbarSettings:{showToolbar:true,customToolbarItems:["Expand"]}
});
&lt;/script&gt;</code>
</pre>






### toolbarSettings.showToolbar<span class="type-signature type boolean">boolean</span>
{:#members-toolbarsettings-showtoolbar}








Gets or sets a value that indicates whether to enable toolbar in the grid.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource: window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowEditing: true },
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Edit] }
});
&lt;/script&gt; </code>
</pre>






### toolbarSettings.toolbarItems<span class="type-signature type enum">enum</span>
{:#members-toolbarsettings-toolbaritems}








Gets or sets a value that indicates whether to add the default editing actions as a toolbar items




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   dataSource:window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowDeleting: true, allowEditing: true, allowAdding: true },
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] }
});
&lt;/script&gt;</code>
</pre>




## Methods








### addRecord<span class="signature">()</span>
{:#methods-addrecord}








Add a new record in grid control even allowAdding is set as false.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an add new record request to the grid
gridObj.addRecord(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// add new record to the grid
$("#Editing").ejGrid("addRecord",{OrderID:12333})       
&lt;/script&gt;</code>
</pre>






### batchCancel<span class="signature">()</span>
{:#methods-batchcancel}








Cancel the modified changes in grid control when edit mode is "batch".





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.batchCancel();
// Cancel added, edited, and deleted changes made in grid
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Cancel added, edited, and deleted changes made in grid
$("#Grid").ejGrid("batchCancel");
&lt;/script&gt;</code>
</pre>






### batchSave<span class="signature">()</span>
{:#methods-batchsave}








Save the modified changes to data source in grid control when edit mode is "batch".





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Save added, edited, and deleted changes to source of data
gridObj.batchSave(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Save added, edited, and deleted changes to source of data
$("#Grid").ejGrid("batchSave");
&lt;/script&gt;</code>
</pre>






### cancelEdit<span class="signature">()</span>
{:#methods-canceledit}








Send a cancel request in grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a cancel request to the grid
gridObj.cancelEdit(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends a cancel request to the grid
$("#Grid").ejGrid("cancelEdit");        
&lt;/script&gt;</code>
</pre>






### clearCellSelection<span class="signature">()</span>
{:#methods-clearcellselection}








It is used to clear all the cell selection.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearCellSelection();  // clears all of the cell selection
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;         
// clears all of the cell selection
$("#Grid").ejGrid("clearCellSelection");        
&lt;/script&gt;</code>
</pre>






### clearColumnSelection<span class="signature">(<span class="optional">index</span>)</span>
{:#methods-clearcolumnselection}








It is used to clear all the row selection or at specific row selection based on the index provided.

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
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last"><span class="optional">optional</span> If index of the column is specified then it will remove the selection from the particular column else it will clears all of the column selection</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearColumnSelection(2);  // Removes the selection based on the column index
gridObj.clearColumnSelection();  // clears all of the column selection
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Removes the selection based on the column index
$("#Grid").ejGrid("clearColumnSelection", 2);   
// clears all of the column selection
$("#Grid").ejGrid("clearColumnSelection");        
&lt;/script&gt;</code>
</pre>






### clearSelection<span class="signature">(<span class="optional">index</span>)</span>
{:#methods-clearselection}








Clear all the row selection or at specific row selection based on the index provided

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
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last"><span class="optional">optional</span> If index of the row is specified then it will remove the selection from the particular row else it will clears all of the row selection</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearSelection(2);  // Removes the selection based on the row index
gridObj.clearSelection();  // clears all of the row selection
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Removes the selection based on the row index
$("#Grid").ejGrid("clearSelection", 2);   
// clears all of the row selection
$("#Grid").ejGrid("clearSelection");        
&lt;/script&gt;</code>
</pre>






### clearSorting<span class="signature">()</span>
{:#methods-clearsorting}








Clear the sorting from columns in the grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Clears the sorting from columns in the grid
gridObj.clearSorting(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Clears the sorting from columns in the grid
$("#Grid").ejGrid("clearSorting");        
&lt;/script&gt;</code>
</pre>






### collapseAll<span class="signature">()</span>
{:#methods-collapseall}








Collapse all the group caption rows in grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Collapse all the group caption rows
gridObj.collapseAll(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Collapse all the group caption rows
$("#Grid").ejGrid("collapseAll");        
&lt;/script&gt;</code>
</pre>






### collapseGroupDropArea<span class="signature">()</span>
{:#methods-collapsegroupdroparea}








Collapse the group drop area in grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Collapse the group drop area of the grid
gridObj.collapseGroupDropArea(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Collapse the group drop area of the grid
$("#Grid").ejGrid("collapseGroupDropArea");        
&lt;/script&gt;</code>
</pre>






### columns<span class="signature">(columndetails, <span class="optional">action</span>)</span>
{:#methods-columns}








Add or remove columns in grid column collections

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
<td class="name"><code>columndetails</code></td>
<td class="type"><span class="param-type">array/string</span></td>
<td class="description last">Pass array of columns or string of field name to add/remove the column in grid</td>
</tr>
<tr>
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"><span class="optional">optional</span> Pass add/remove action to be performed. By default "add" action will perform</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// remove grid column
gridObj.columns("OrderID", "remove");
// Add new column into grid or modified already existing column in the grid.
gridObj.columns("CustomerID", "add"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// remove grid column
$("#Grid").ejGrid("columns","OrderID", "remove");   
// Add new column into grid or modified already existing column in the grid.                    
$("#Grid").ejGrid("columns","CustomerID", "add");                       
&lt;/script&gt;</code>
</pre>






### dataSource<span class="signature">(datasource)</span>
{:#methods-datasource}








Refresh the grid with new data source

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
<td class="name"><code>datasource</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass new data source to the grid</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Refreshes the grid data source
gridObj.dataSource(data); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Refreshes the grid data source
$("#Grid").ejGrid("dataSource", data);        
&lt;/script&gt;</code>
</pre>






### deleteRecord<span class="signature">(fieldName, data)</span>
{:#methods-deleterecord}








Delete a record in grid control even allowDeleting is set as false

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the primary key field Name of the column</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass the json data of record need to be delete.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a delete record request to the grid
gridObj.deleteRecord("OrderID", { OrderID: 10249, EmployeeID: 3 }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends a delete record request to the grid
$("#Grid").ejGrid("deleteRecord", "OrderID", { OrderID: 10249, EmployeeID: 3 });        
&lt;/script&gt;</code>
</pre>






### destroy<span class="signature">()</span>
{:#methods-destroy}








Destroy the grid widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
var gridObj = $("#Grid").data("ejGrid");
gridObj.destroy(); // destroy the Grid
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// destroy the Grid
$("#Grid").ejGrid("destroy");        
&lt;/script&gt;</code>
</pre>






### editCell<span class="signature">(index, fieldName)</span>
{:#methods-editcell}








Edit a particular cell based on the row index and field name provided in "batch" edit mode.

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
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass row index to edit particular cell</td>
</tr>
<tr>
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column to perform batch edit</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Edit particular cell based on row index and column field name
gridObj.editCell(2, "OrderID"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
// Edit particular cell based on row index and column field name
$("#Grid").ejGrid("editCell", 2, "OrderID");
&lt;/script&gt;</code>
</pre>






### endEdit<span class="signature">()</span>
{:#methods-endedit}








Send a save request in grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a save request to the grid
gridObj.endEdit(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends a save request to the grid
$("#Grid").ejGrid("endEdit");        
&lt;/script&gt;</code>
</pre>






### expandAll<span class="signature">()</span>
{:#methods-expandall}








Expand all the group caption rows in grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Expand all the group caption rows
gridObj.expandAll(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Expand all the group caption rows
$("#Grid").ejGrid("expandAll");        
&lt;/script&gt;</code>
</pre>






### expandCollapse<span class="signature">($target)</span>
{:#methods-expandcollapse}








Expand or collapse the row based on the row state in grid

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
<td class="name"><code>$target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Pass the target object to expand/collapse the row based on its row state</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Expands or collapses the row based on the row state
gridObj.expandCollapse($("tr td.recordplusexpand &gt; div").first());  
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Expands or collapses the row based on the row state
$("#Grid").ejGrid("expandCollapse", $("tr td.recordplusexpand &gt; div").first());        
&lt;/script&gt;</code>
</pre>






### expandGroupDropArea<span class="signature">()</span>
{:#methods-expandgroupdroparea}








Expand the group drop area in grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Expands the group drop area of the grid
gridObj.expandGroupDropArea(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Expands the group drop area of the grid
$("#Grid").ejGrid("expandGroupDropArea");        
&lt;/script&gt;</code>
</pre>






### filterColumn<span class="signature">(fieldName, filterOperator, filterValue, predicate, <span class="optional">matchcase</span>)</span>
{:#methods-filtercolumn}








Send a filtering request to grid.

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column</td>
</tr>
<tr>
<td class="name"><code>filterOperator</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">string/integer/dateTime operator</td>
</tr>
<tr>
<td class="name"><code>filterValue</code></td>
<td class="type"><span class="param-type">string/number</span></td>
<td class="description last">Pass the value to be filtered in a column</td>
</tr>
<tr>
<td class="name"><code>predicate</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the predicate as and/or</td>
</tr>
<tr>
<td class="name"><code>matchcase</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last"><span class="optional">optional</span> Pass the match case valueas true/false</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a filtering request to the grid
gridObj.filterColumn("OrderID","equal","10248","and", true);
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
// Sends a filtering request to the grid
$("#Grid").ejGrid("filterColumn","OrderID","equal","10248","and", true);
&lt;/script&gt;</code>
</pre>






### getBatchChanges<span class="signature">()</span>
{:#methods-getbatchchanges}








Get the batch changes of edit, delete and add operations of grid.





Example
{:.example}

<pre class="prettyprint">
<code>&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the edit, delete, and add changes of a grid
gridObj.getBatchChanges(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
// Gets the edit, delete, and add changes of a grid
$("#Grid").ejGrid("getBatchChanges");        
&lt;/script&gt;</code>
</pre>






### getBrowserDetails<span class="signature">()</span>
{:#methods-getbrowserdetails}








Get the browser details





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the browser details of the application being run
gridObj.getBrowserDetails(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Gets the browser details of the application being run
$("#Grid").ejGrid("getBrowserDetails");        
&lt;/script&gt;</code>
</pre>






### getColumnByField<span class="signature">(fieldName)</span>
{:#methods-getcolumnbyfield}








Get the column details based on the given field in grid

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column to get the corresponding column object</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods-returns:}

Object


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column details based on the given field name
gridObj.getColumnByField("OrderID");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the column details based on the given field name
$("#Grid").ejGrid("getColumnByField", "OrderID");        
&lt;/script&gt;</code>
</pre>






### getColumnByHeaderText<span class="signature">(headerText)</span>
{:#methods-getcolumnbyheadertext}








Get the column details based on the given header text in grid.

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
<td class="name"><code>headerText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the header text of the column to get the corresponding column object</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods-returns:}

Object


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column details based on the given headerText
gridObj.getColumnByHeaderText("Order ID"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the column details based on the given headerText
$("#Grid").ejGrid("getColumnByHeaderText", "Order ID");        
&lt;/script&gt;</code>
</pre>






### getColumnByIndex<span class="signature">(columnIndex)</span>
{:#methods-getcolumnbyindex}








Get the column details based on the given column index in grid

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
<td class="name"><code>columnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the index of the column to get the corresponding column object</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods-returns:}

Object


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column details based on the given column index
gridObj.getColumnByIndex(1); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the column details based on the given column index
$("#Grid").ejGrid("getColumnByIndex", 1);        
&lt;/script&gt;</code>
</pre>






### getColumnFieldNames<span class="signature">()</span>
{:#methods-getcolumnfieldnames}








Get the list of field names from column collection in grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column field names based on the given index
gridObj.getColumnFieldNames(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the column field names based on the given index
$("#Grid").ejGrid("getColumnFieldNames");        
&lt;/script&gt;</code>
</pre>






### getColumnIndexByField<span class="signature">(fieldName)</span>
{:#methods-getcolumnindexbyfield}








Get the column index of the given field in grid.

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column to get the corresponding column index</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods-returns:}

Index


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column index based on the given field name
gridObj.getColumnIndexByField("OrderID"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Gets the column index based on the given field name
$("#Grid").ejGrid("getColumnIndexByField", "OrderID");        
&lt;/script&gt;</code>
</pre>






### getContent<span class="signature">()</span>
{:#methods-getcontent}








Get the content div element of grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets content of grid control
gridObj.getContent(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets content of grid control
$("#Grid").ejGrid("getContent");        
&lt;/script&gt;</code>
</pre>






### getContentTable<span class="signature">()</span>
{:#methods-getcontenttable}








Get the content table element of grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets content table of grid control
gridObj.getContentTable();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets content table of grid control
$("#Grid").ejGrid("getContentTable");        
&lt;/script&gt;</code>
</pre>






### getCurrentEditCellData<span class="signature">()</span>
{:#methods-getcurrenteditcelldata}








Get the data of currently edited cell value in "batch" edit mode





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Get data of currently edited cell value
gridObj.getCurrentEditCellData(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Get data of currently edited cell value
$("#Grid").ejGrid("getCurrentEditCellData");        
&lt;/script&gt;</code>
</pre>






### getCurrentIndex<span class="signature">()</span>
{:#methods-getcurrentindex}








Get the current page index in grid pager.





#### Returns:
{:#methods-returns:}

PageIndex


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the current page index in grid
gridObj.getCurrentIndex();  
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the current page index in grid
$("#Grid").ejGrid("getCurrentIndex");   
&lt;/script&gt;</code>
</pre>






### getCurrentViewData<span class="signature">()</span>
{:#methods-getcurrentviewdata}








Get the current page data source of grid..





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets current view data of grid control
gridObj.getCurrentViewData(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets current view data of grid control
$("#Grid").ejGrid("getCurrentViewData");        
&lt;/script&gt;</code>
</pre>






### getFieldNameByHeaderText<span class="signature">(headerText)</span>
{:#methods-getfieldnamebyheadertext}








Get the column field name from the given header text in grid.

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
<td class="name"><code>headerText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass header text of the column to get its corresponding field name</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column field name from the given headerText
gridObj.getFieldNameByHeaderText("Order ID"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the column field name from the given headerText
$("#Grid").ejGrid("getFieldNameByHeaderText", "Order ID");
&lt;/script&gt;</code>
</pre>






### getFilterBar<span class="signature">()</span>
{:#methods-getfilterbar}








Get the filter bar of grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets filter bar of grid control
gridObj.getFilterBar(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets filter bar of grid control
$("#Grid").ejGrid("getFilterBar");        
&lt;/script&gt;</code>
</pre>






### getFilteredRecords<span class="signature">()</span>
{:#methods-getfilteredrecords}








Get the records filtered or searched in Grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the filtered or searched records in Grid
gridObj.getFilteredRecords();  
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the filtered or searched records in Grid
$("#Grid").ejGrid("getFilteredRecords");   
&lt;/script&gt;</code>
</pre>






### getFooterContent<span class="signature">()</span>
{:#methods-getfootercontent}








Get the footer content of grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid footer content of grid control
gridObj.getFooterContent(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets grid footer content of grid control
$("#Grid").ejGrid("getFooterContent");        
&lt;/script&gt;</code>
</pre>






### getFooterTable<span class="signature">()</span>
{:#methods-getfootertable}








Get the footer table element of grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid footer table of grid control
gridObj.getFooterTable(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets grid footer table of grid control
$("#Grid").ejGrid("getFooterTable");        
&lt;/script&gt;</code>
</pre>






### getHeaderContent<span class="signature">()</span>
{:#methods-getheadercontent}








Get the header content div element of grid..





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid header content of grid control
gridObj.getHeaderContent(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets grid header content of grid control
$("#Grid").ejGrid("getHeaderContent");        
&lt;/script&gt;</code>
</pre>






### getHeaderTable<span class="signature">()</span>
{:#methods-getheadertable}








Get the header table element of grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.getHeaderTable(); 
// Gets header table of grid control
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets header table of grid control
$("#Grid").ejGrid("getHeaderTable");        
&lt;/script&gt;</code>
</pre>






### getHeaderTextByFieldName<span class="signature">(field)</span>
{:#methods-getheadertextbyfieldname}








Get the column header text from the given field name in grid.

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
<td class="name"><code>field</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass field name of the column to get its corresponding header text</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.getHeaderTextByFieldName("OrderID"); // Gets the column header text from the given field name
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the column header text from the given field name
$("#Grid").ejGrid("getHeaderTextByFieldName", "OrderID");
&lt;/script&gt;</code>
</pre>






### getHiddenColumnNames<span class="signature">()</span>
{:#methods-gethiddencolumnnames}








Get the names of all the hidden column collections in grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets names of all the hidden column collections
gridObj.getHiddenColumnNames(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets names of all the hidden column collections
$("#Grid").ejGrid("getHiddenColumnNames");        
&lt;/script&gt;</code>
</pre>






### getIndexByRow<span class="signature">($tr)</span>
{:#methods-getindexbyrow}








Get the row index based on the given tr element in grid.

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
<td class="name"><code>$tr</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Pass the tr element in grid content to get its row index</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods-returns:}

index


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the row index based on the given row
gridObj.getIndexByRow($(".gridcontent tr").first()); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the row index based on the given row
$("#Grid").ejGrid("getIndexByRow", $(".gridcontent tr").first());        
&lt;/script&gt;</code>
</pre>






### getPager<span class="signature">()</span>
{:#methods-getpager}








Get the pager of grid..





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid pager of grid control
gridObj.getPager(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets grid pager of grid control
$("#Grid").ejGrid("getPager");        
&lt;/script&gt;</code>
</pre>






### getPrimaryKeyFieldNames<span class="signature">()</span>
{:#methods-getprimarykeyfieldnames}








Get the names of primary key columns in Grid





#### Returns:
{:#methods-returns:}

key fields


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the names of primary key columns
gridObj.getPrimaryKeyFieldNames(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the names of primary key columns
$("#Grid").ejGrid("getPrimaryKeyFieldNames");        
&lt;/script&gt;</code>
</pre>






### getRowByIndex<span class="signature">(from, to)</span>
{:#methods-getrowbyindex}








Get the rows(tr element) from the given from and to row index in grid

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
<td class="name"><code>from</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the from index from which the rows to be returned</td>
</tr>
<tr>
<td class="name"><code>to</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the to index to which the rows to be returned</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the rows from the specified row index 
gridObj.getRowByIndex(3, 6);  
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the rows from the specified row index
$("#Grid").ejGrid("getRowByIndex", 3, 6);   
&lt;/script&gt;</code>
</pre>






### getRowHeight<span class="signature">()</span>
{:#methods-getrowheight}








Get the row height of grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the row height of the grid
gridObj.getRowHeight();  
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the row height of the grid
$("#Grid").ejGrid("getRowHeight");   
&lt;/script&gt;</code>
</pre>






### getRows<span class="signature">()</span>
{:#methods-getrows}








Get the rows(tr element)of grid which is displayed in the current page.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid rows of grid control
gridObj.getRows(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets grid rows of grid control
$("#Grid").ejGrid("getRows");        
&lt;/script&gt;</code>
</pre>






### getScrollObject<span class="signature">()</span>
{:#methods-getscrollobject}








Get the scroller object of grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets scroll object of grid control
gridObj.getScrollObject(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets scroll object of grid control
$("#Grid").ejGrid("getScrollObject");        
&lt;/script&gt;</code>
</pre>






### getSelectedRecords<span class="signature">()</span>
{:#methods-getselectedrecords}








Get the selected records details in grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the selected row list
gridObj.getSelectedRecords();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the selected row list
$("#Grid").ejGrid("getSelectedRecords");        
&lt;/script&gt;</code>
</pre>






### getVisibleColumnNames<span class="signature">()</span>
{:#methods-getvisiblecolumnnames}








Get the names of all the visible column collections in grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the names of all the visible column collections
gridObj.getVisibleColumnNames(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Gets the names of all the visible column collections
$("#Grid").ejGrid("getVisibleColumnNames");        
&lt;/script&gt;</code>
</pre>






### gotoPage<span class="signature">(pageIndex)</span>
{:#methods-gotopage}








Send a paging request to specified page in grid

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
<td class="name"><code>pageIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the page index to perform paging at specified page index</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a paging request to the grid with specified page index
gridObj.gotoPage(3);
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends a paging request to the grid with specified page index
$("#Grid").ejGrid("gotoPage", 3);        
&lt;/script&gt;</code>
</pre>






### groupColumn<span class="signature">(fieldName)</span>
{:#methods-groupcolumn}








Send a column grouping request in grid.

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field Name of the column to be grouped in grid control</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a group column request to the grid
gridObj.groupColumn("OrderID"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends a group column request to the grid
$("#Grid").ejGrid("groupColumn", "OrderID");        
&lt;/script&gt;</code>
</pre>






### hideColumns<span class="signature">(headerText)</span>
{:#methods-hidecolumns}








Hide columns from the grid based on the header text

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
<td class="name"><code>headerText</code></td>
<td class="type"><span class="param-type">array/string</span></td>
<td class="description last">you can pass either array of header text of various columns or a header text of a column to hide</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.hideColumns("Order ID"); // Hides column based on the given header text of the column
gridObj.hideColumns(["Order ID", "Customer ID"]); // Hide columns based on the array of header text of the columns given
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Hide column based on the given header text of the column
$("#Grid").ejGrid("hideColumns", "Order ID"); 
// Hide columns based on the array of header text of the columns given
$("#Grid").ejGrid("hideColumns", ["Order ID", "Customer ID"]);                  
&lt;/script&gt;</code>
</pre>






### print<span class="signature">()</span>
{:#methods-print}








Print the grid control





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// It prints the grid.
gridObj.print(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&amp;dgt; 
&lt;script&gt;
// It prints the grid.
$("#Grid").ejGrid("print");        
&lt;/script&gt;</code>
</pre>






### refreshBatchEditChanges<span class="signature">()</span>
{:#methods-refreshbatcheditchanges}








It is used to refresh and reset the changes made in "batch" edit mode





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.refreshBatchEditChanges(); 
// It is used to refresh and reset the changes made in batch edit mode
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// It is used to refresh and reset the changes made in batch edit mode
$("#Grid").ejGrid("refreshBatchEditChanges");
&lt;/script&gt;</code>
</pre>






### refreshContent<span class="signature">(<span class="optional">templateRefresh</span>)</span>
{:#methods-refreshcontent}








Refresh the grid contents. The template refreshment is based on the argument passed along with this method

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
<td class="name"><code>templateRefresh</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last"><span class="optional">optional</span> When templateRefresh is set true, template and grid contents both are refreshed in grid else only grid content is refreshed</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.refreshContent(); // Refreshes the grid contents only
gridObj.refreshContent(true); // Refreshes the template and grid contents
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Refreshes the grid contents only
$("#Grid").ejGrid("refreshContent");        
// Refreshes the template and grid contents
$("#Grid").ejGrid("refreshContent", true);        
&lt;/script&gt;</code>
</pre>






### refreshTemplate<span class="signature">()</span>
{:#methods-refreshtemplate}








Refresh the template of the grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Refreshes the template of the grid control
gridObj.refreshTemplate(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Refreshes the template of the grid control.
$("#Grid").ejGrid("refreshTemplate");        
&lt;/script&gt;</code>
</pre>






### refreshToolbar<span class="signature">()</span>
{:#methods-refreshtoolbar}








Refresh the toolbar items in grid.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Refreshes the toolbar items state
gridObj.refreshToolbar(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Refreshes the toolbar items state
$("#Grid").ejGrid("refreshToolbar");        
&lt;/script&gt;</code>
</pre>






### removeSortedColumns<span class="signature">(fieldName)</span>
{:#methods-removesortedcolumns}








Remove a column or collection of columns from a sorted column collections in grid.

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">array/string</span></td>
<td class="description last">Pass array of field names of the columns to remove a collection of sorted columns or pass a string of field name to remove a column from sorted column collections</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Removes a column from sorted column collections
gridObj.removeSortedColumns("OrderID"); 
// Removes specified collection of columns from sorted column collections
gridObj.removeSortedColumns(["CustomerID", "ShipCity"]); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Removes a column from sorted column collections
$("#Grid").ejGrid("removeSortedColumns", "OrderID");        
// Removes specified collection of columns from sorted column collections
$("#Grid").ejGrid("removeSortedColumns", ["CustomerID", "ShipCity"]);        
&lt;/script&gt;</code>
</pre>






### render<span class="signature">()</span>
{:#methods-render}








Creates a grid control





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// It renders the grid.
gridObj.render(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&amp;dgt; 
&lt;script&gt;
// It renders the grid.
$("#Grid").ejGrid("render");        
&lt;/script&gt;</code>
</pre>






### reorderColumns<span class="signature">(fromFieldName, toFieldName)</span>
{:#methods-reordercolumns}








Re-order the column in grid

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
<td class="name"><code>fromFieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the from field name of the column needs to be changed</td>
</tr>
<tr>
<td class="name"><code>toFieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the to field name of the column needs to be changed</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Reorders the column based on the given index
gridObj.reorderColumns("OrderID", "CustomerID"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Reorders the column based on the given index
$("#Grid").ejGrid("reorderColumns", "OrderID", "CustomerID");
&lt;/script&gt;</code>
</pre>






### resetModelCollections<span class="signature">()</span>
{:#methods-resetmodelcollections}








Reset the model collections like pageSettings, groupSettings, filterSettings, sortSettings and summaryRows.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Reset model collections
gridObj.resetModelCollections(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Reset model collections
$("#Grid").ejGrid("resetModelCollections");
&lt;/script&gt;</code>
</pre>






### rowHeightRefresh<span class="signature">()</span>
{:#methods-rowheightrefresh}








Resolves row height issue when unbound column is used with FrozenColumn





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.rowHeightRefresh(); // Resolves row height issue
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;         
// Resolves row height issue
$("#Grid").ejGrid("rowHeightRefresh");   
&lt;/script&gt;</code>
</pre>






### search<span class="signature">(searchString)</span>
{:#methods-search}








Send a search request to grid with specified string passed in it

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
<td class="name"><code>searchString</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the string to search in Grid records</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a search request to the grid
gridObj.search("France"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
// Sends a search request to the grid
$("#Grid").ejGrid("search", "France");        
&lt;/script&gt;</code>
</pre>






### selectCells<span class="signature">(rowCellIndexes)</span>
{:#methods-selectcells}








Select cells in grid.

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
<td class="name"><code>rowCellIndexes</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">It is used to set the starting index of row and indexes of cells for that corresponding row for selecting cells.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects cells based on the given index
gridObj.selectCells([[1, [4, 3, 2]]]); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Selects cells based on the given index
$("#Grid").ejGrid("selectCells", [[1, [4, 3, 2]]]);
&lt;/script&gt;</code>
</pre>






### selectColumns<span class="signature">(fromIndex)</span>
{:#methods-selectcolumns}








Select columns in grid.

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
<td class="name"><code>fromIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to set the starting index of column for selecting columns.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects columns based on the given index
gridObj.selectColumns(1,4); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Selects columns based on the given index
$("#Grid").ejGrid("selectColumns", 1, 4);
&lt;/script&gt;</code>
</pre>






### selectRows<span class="signature">(fromIndex, toIndex)</span>
{:#methods-selectrows}








Select rows in grid.

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
<td class="name"><code>fromIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to set the starting index of row for selecting rows.</td>
</tr>
<tr>
<td class="name"><code>toIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to set the ending index of row for selecting rows.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects rows based on the given index
gridObj.selectRows(1, 4); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Selects rows based on the given index
$("#Grid").ejGrid("selectRows", 1, 4);
&lt;/script&gt;</code>
</pre>






### setValidationToField<span class="signature">(fieldName, rules)</span>
{:#methods-setvalidationtofield}








Set validation to a field during editing.

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Specify the field name of the column to set validation rules</td>
</tr>
<tr>
<td class="name"><code>rules</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Specify the validation rules for the field</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// It is used to set validation to a field during editing
gridObj.setValidationToField("OrderID", { required: true }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// It is used to set validation to a field during editing
$("#Grid").ejGrid("setValidationToField", "OrderID", { required: true });
&lt;/script&gt;</code>
</pre>






### showColumns<span class="signature">(headerText)</span>
{:#methods-showcolumns}








Show columns in the grid based on the header text

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
<td class="name"><code>headerText</code></td>
<td class="type"><span class="param-type">array/string</span></td>
<td class="description last">you can pass either array of header text of various columns or a header text of a column to show</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.showColumns("Order ID"); // Shows column based on the given header text of the column
gridObj.showColumns(["Order ID", "Customer ID"]); // Shows columns based on the array of header text of the columns given
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Shows column based on the given header text of the column
$("#Grid").ejGrid("showColumns", "Order ID"); 
// Shows columns based on the array of header text of the columns given
$("#Grid").ejGrid("showColumns", ["Order ID", "Customer ID"]);                  
&lt;/script&gt;</code>
</pre>






### sortColumn<span class="signature">(columnName, <span class="optional">sortingDirection</span>)</span>
{:#methods-sortcolumn}








Send a sorting request in grid.

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
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column as columnName for which sorting have to be performed</td>
</tr>
<tr>
<td class="name"><code>sortingDirection</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"><span class="optional">optional</span> Pass the sort direction ascending/descending by which the column have to be sort. By default it is sorting in an ascending order</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.sortColumn("OrderID", "ascending"); // Sends a sorting request to the grid with specified columnName and sortDirection
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends a sorting request to the grid with specified columnName and sortDirection
$("#Grid").ejGrid("sortColumn", "OrderID", "ascending");        
&lt;/script&gt;</code>
</pre>






### startEdit<span class="signature">($tr)</span>
{:#methods-startedit}








Send an edit record request in grid

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
<td class="name"><code>$tr</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Pass the tr- selected row element to be edited in grid</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an edit record request to the grid
gridObj.startEdit($(".gridcontent tr").first()); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends an edit record request to the grid
$("#Grid").ejGrid("startEdit", $(".gridcontent tr").first());        
&lt;/script&gt;</code>
</pre>






### ungroupColumn<span class="signature">(fieldName)</span>
{:#methods-ungroupcolumn}








Un-group a column from grouped columns collection in grid

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field Name of the column to be ungrouped from grouped column collection</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an ungroup column request to the grid
gridObj.ungroupColumn("OrderID"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends an ungroup column request to the grid
$("#Grid").ejGrid("ungroupColumn", "OrderID");        
&lt;/script&gt;</code>
</pre>






### updateRecord<span class="signature">(fieldName, data)</span>
{:#methods-updaterecord}








Update a edited record in grid control even allowEditing is set as false.

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
<td class="name"><code>fieldName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the primary key field Name of the column</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass the edited json data of record need to be update.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a update record request to the grid
gridObj.updateRecord("OrderID", { OrderID: 10249, EmployeeID: 3 }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
// Sends a update record request to the grid
$("#Grid").ejGrid("updateRecord", "OrderID", { OrderID: 10249, EmployeeID: 3 });        
&lt;/script&gt;</code>
</pre>




## Events








### actionBegin
{:#events-actionbegin}








Triggered for every grid action before its starts.

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
<td class="description last">Event parameters when grid is initialized:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid paging action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentPage</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current selected page number.</td>
</tr>
<tr>
<td class="name"><code>previousPage</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected page number.</td>
</tr>
<tr>
<td class="name"><code>endIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the end row index of that current page.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>startIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the start row index of that current page.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid sorting action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>columnSortDirection</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column sort direction.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid grouping action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid record editing action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current edited row.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current action event type.</td>
</tr>
<tr>
<td class="name"><code>primaryKey</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key.</td>
</tr>
<tr>
<td class="name"><code>primaryKeyValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid record save action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>selectedRow</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected row index.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid record cancel action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid record delete action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>tr</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns selected row for delete.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when add new record action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid filtering action starts:
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentFilteringColumn</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current filtering column field name.</td>
</tr>
<tr>
<td class="name"><code>filterCollection</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns filter details.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid excel filtering action starts:</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid request type as "filterbeforeopen"
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current column field name.</td>
</tr>
<tr>
<td class="name"><code>columnType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns type of the column like number, string and so on.</td>
</tr>
<tr>
<td class="name"><code>filtermodel</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterbeforeopen".</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid request type as "filterchoicerequest"
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>dataSource</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dataSource.</td>
</tr>
<tr>
<td class="name"><code>filtermodel</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>query</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query manager.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterchoicerequest".</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid request type as "filterchoicesearch"
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>dataSource</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dataSource.</td>
</tr>
<tr>
<td class="name"><code>filtermodel</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>query</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query manager.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterchoicesearch".</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid request type as "filterbeforeopen"
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current column field name.</td>
</tr>
<tr>
<td class="name"><code>columnType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns type of the column like number, string and so on.</td>
</tr>
<tr>
<td class="name"><code>filtermodel</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name"><code>isCustomFilter</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the customfilter option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterbeforeopen".</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   actionBegin: function (args){}
});
&lt;/script&gt;</code>
</pre>






### actionComplete
{:#events-actioncomplete}








Triggered for every grid action success event.

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
<td class="description last">Arguments in actionComplete when grid is initialized.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments in actionComplete after grid paging action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentPage</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current selected page number.</td>
</tr>
<tr>
<td class="name"><code>previousPage</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected page number.</td>
</tr>
<tr>
<td class="name"><code>endIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the end row index of that current page.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>startIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the start row index of the current page.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid sorting action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current sorted column field name.</td>
</tr>
<tr>
<td class="name"><code>columnSortDirection</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column sort direction.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid grouping action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid record editing action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current edited row.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>primaryKey</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key.</td>
</tr>
<tr>
<td class="name"><code>primaryKeyValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid record save action is completed.
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>selectedRow</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selectedRow index.</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid record cancel action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid record delete action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>tr</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns selected row for delete.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after add new record action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns empty record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid filtering action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentFilteringColumn</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current filtering column field name.</td>
</tr>
<tr>
<td class="name"><code>filterCollection</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns filter details.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid excel filtering action end:</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid request type as "filterchoicerequest"
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>dataSource</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dataSource.</td>
</tr>
<tr>
<td class="name"><code>filtermodel</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterchoicerequest".</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid request type as "filterafteropen"
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current column field name.</td>
</tr>
<tr>
<td class="name"><code>columnType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns type of the column like number, string and so on.</td>
</tr>
<tr>
<td class="name"><code>filtermodel</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterafteropen".</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid request type as "filterchoicesearch"
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>dataSource</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dataSource.</td>
</tr>
<tr>
<td class="name"><code>filtermodel</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterchoicesearch".</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when grid request type as "filterafteropen"
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current column field name.</td>
</tr>
<tr>
<td class="name"><code>columnType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns type of the column like number, string and so on.</td>
</tr>
<tr>
<td class="name"><code>filtermodel</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name"><code>isCustomFilter</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the customfilter option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterafteropen".</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   actionComplete: function (args) {}
}); 
&lt;/script&gt;</code>
</pre>






### actionFailure
{:#events-actionfailure}








Triggered for every grid action server failure event.

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
<td class="description last">Arguments in actionComplete when grid is initialized.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments in actionComplete after grid paging action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentPage</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current selected page number.</td>
</tr>
<tr>
<td class="name"><code>previousPage</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected page number.</td>
</tr>
<tr>
<td class="name"><code>endIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the end row index of that current page.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>startIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the start row index of the current page.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid sorting action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current sorted column field name.</td>
</tr>
<tr>
<td class="name"><code>columnSortDirection</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column sort direction.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid grouping action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid record editing action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current edited row.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>primaryKey</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key.</td>
</tr>
<tr>
<td class="name"><code>primaryKeyValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid record save action is completed.
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>selectedRow</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selectedRow index.</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid record delete action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>tr</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns selected row for delete.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after add new record action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns empty record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionComplete after grid filtering action is completed.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentFilteringColumn</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current filtering column field name.</td>
</tr>
<tr>
<td class="name"><code>filterCollection</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns filter details.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   actionFailure: function (args) {}
}); 
&lt;/script&gt;</code>
</pre>






### batchAdd
{:#events-batchadd}








Triggered when record batch add.

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
<td class="description last">Arguments when batchAdd event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>columnObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>columnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column index.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element.</td>
</tr>
<tr>
<td class="name"><code>primaryKey</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the primaryKey.</td>
</tr>
<tr>
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   batchAdd: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### batchDelete
{:#events-batchdelete}








Triggered when record batch delete.

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
<td class="description last">Arguments when batchDelete event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   batchDelete: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### beforeBatchAdd
{:#events-beforebatchadd}








Triggered before the batch add.

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
<td class="description last">Arguments when beforeBatchAdd event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>defaultData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the default data object.</td>
</tr>
<tr>
<td class="name"><code>primaryKey</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primaryKey.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   beforeBatchAdd: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### beforeBatchDelete
{:#events-beforebatchdelete}








Triggered before the batch delete.

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
<td class="description last">Arguments when beforeBatchDelete event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>primaryKey</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primaryKey.</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row data.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   beforeBatchDelete: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### beforeBatchSave
{:#events-beforebatchsave}








Triggered before the batch save.

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
<td class="description last">Arguments when beforeBatchSave event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>batchChanges</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the changed record object.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   beforeBatchSave: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### beginEdit
{:#events-beginedit}








Triggered before the record is going to be edited.

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
<td class="description last">Arguments when beginEdit event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current edited row.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>primaryKey</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key.</td>
</tr>
<tr>
<td class="name"><code>primaryKeyValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   beginEdit: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### cellEdit
{:#events-celledit}








Triggered when record cell edit.

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
<td class="description last">Arguments when cellEdit event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>validationRules</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the validation rules.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column name.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the cell value.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row data object.</td>
</tr>
<tr>
<td class="name"><code>previousValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the previous value of the cell.</td>
</tr>
<tr>
<td class="name"><code>columnObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
<tr>
<td class="name"><code>isForeignKey</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns isForeignKey option value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   cellEdit: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### cellSave
{:#events-cellsave}








Triggered when record cell save.

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
<td class="description last">Arguments when cellSave event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column name.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the cell value.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row data object.</td>
</tr>
<tr>
<td class="name"><code>previousValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the previous value of the cell.</td>
</tr>
<tr>
<td class="name"><code>columnObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
<tr>
<td class="name"><code>isForeignKey</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns isForeignKey option value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   cellSave: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### cellSelected
{:#events-cellselected}








Triggered after the cell is selected.

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
<td class="description last">Arguments when cellSelecting event is triggered.
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
<td class="name"><code>cellIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected cell index value.</td>
</tr>
<tr>
<td class="name"><code>previousRowCellIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected cell index value.</td>
</tr>
<tr>
<td class="name"><code>currentCell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected cell element.</td>
</tr>
<tr>
<td class="name"><code>previousRowCell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected cell element.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>selectedRowCellIndex</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the selected row cell index values.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   cellSelected: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### cellSelecting
{:#events-cellselecting}








Triggered before the cell is going to be selected.

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
<td class="description last">Arguments when cellSelecting event is triggered.
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
<td class="name"><code>cellIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected cell index value.</td>
</tr>
<tr>
<td class="name"><code>previousRowCellIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected cell index value.</td>
</tr>
<tr>
<td class="name"><code>currentCell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected cell element.</td>
</tr>
<tr>
<td class="name"><code>previousRowCell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected cell element.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>previousRowCellIndex</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the previously selected row cell index values</td>
</tr>
<tr>
<td class="name"><code>isCtrlKeyPressed</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns whether the ctrl key is pressed while selecting cell</td>
</tr>
<tr>
<td class="name"><code>isShiftKeyPressed</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns whether the shift key is pressed while selecting cell</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   cellSelecting: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### columnDrag
{:#events-columndrag}








Triggered when the column is being dragged.

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
<td class="description last">Arguments when columnDrag event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>draggableType</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable column object.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns target elements based on mouse move position.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   columnDrag: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### columnDragStart
{:#events-columndragstart}








Triggered when column dragging begins.

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
<td class="description last">Arguments when columnDragStart event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>draggableType</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable column object.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drag start element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
    columnDragStart: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### columnDrop
{:#events-columndrop}








Triggered when the column is dropped.

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
<td class="description last">Arguments when columnDrop event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>draggableType</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable column object.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns dropped dragged element.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 columnDrop: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### columnSelected
{:#events-columnselected}








Triggered after the column is selected.

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
<td class="description last">Arguments when columnSelected event is triggered.
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
<td class="name"><code>columnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected cell index value.</td>
</tr>
<tr>
<td class="name"><code>previousColumnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected column index value.</td>
</tr>
<tr>
<td class="name"><code>headerCell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected header cell element.</td>
</tr>
<tr>
<td class="name"><code>prevColumnHeaderCell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected header cell element.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns corresponding column object (JSON).</td>
</tr>
<tr>
<td class="name"><code>selectedColumnsIndex</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the selected columns values.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   columnSelected: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### columnSelecting
{:#events-columnselecting}








Triggered before the column is going to be selected.

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
<td class="description last">Arguments when columnSelecting event is triggered.
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
<td class="name"><code>columnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected column index value.</td>
</tr>
<tr>
<td class="name"><code>previousColumnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected column index value.</td>
</tr>
<tr>
<td class="name"><code>headerCell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected header cell element.</td>
</tr>
<tr>
<td class="name"><code>prevColumnHeaderCell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected header cell element.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns corresponding column object (JSON).</td>
</tr>
<tr>
<td class="name"><code>previousColumnIndex</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the previously selected column index values</td>
</tr>
<tr>
<td class="name"><code>isCtrlKeyPressed</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns whether the ctrl key is pressed while selecting cell</td>
</tr>
<tr>
<td class="name"><code>isShiftKeyPressed</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns whether the shift key is pressed while selecting cell</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   columnSelecting: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### contextClick
{:#events-contextclick}








Triggered when context menu item is clicked

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
<td class="description last">Arguments when contextClick event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentTarget</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the status of contextmenu item which denotes its enabled state</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target item.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   contextClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### contextOpen
{:#events-contextopen}








Triggered before the context menu is opened.

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
<td class="description last">Arguments when contextOpen event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentTarget</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the status of contextmenu item which denotes its enabled state</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target item.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   contextOpen: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### create
{:#events-create}








Triggered when the grid is rendered completely.

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
<td class="description last">Event parameters from grid
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
   create: function (args){}
});
&lt;/script&gt;</code>
</pre>






### dataBound
{:#events-databound}








Triggered the grid is bound with data during initial rendering.

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
<td class="description last">Arguments when dataBound event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 dataBound: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### destroy
{:#events-destroy}








Triggered when grid going to destroy.

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
<td class="description last">Arguments when destroy event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   destroy: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### detailsCollapse
{:#events-detailscollapse}








Triggered when detail template row is clicked to collapse.

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
<td class="description last">Arguments when detailsCollapse event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>detailsRow</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns detail row element.</td>
</tr>
<tr>
<td class="name"><code>masterData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns master row of detail row record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>masterRow</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns master row element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   detailsCollapse: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### detailsDataBound
{:#events-detailsdatabound}








Triggered detail template row is initialized.

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
<td class="description last">Event parameters from grid
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>detailsElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns details row element.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the details row data.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
   detailsDataBound: function (args){}
});
&lt;/script&gt;</code>
</pre>






### detailsExpand
{:#events-detailsexpand}








Triggered when detail template row is clicked to expand.

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
<td class="description last">Arguments when detailsExpand event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>detailsRow</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns detail row element.</td>
</tr>
<tr>
<td class="name"><code>masterData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns master row of detail row record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>masterRow</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns master row element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   detailsExpand: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### endAdd
{:#events-endadd}








Triggered after the record is added.

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
<td class="description last">Arguments when endAdd event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns added data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   endAdd: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### endDelete
{:#events-enddelete}








Triggered after the record is deleted.

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
<td class="description last">Arguments when endDelete event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   endDelete: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### endEdit
{:#events-endedit}








Triggered after the record is edited.

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
<td class="description last">Arguments when endEdit event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns modified data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   endEdit: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### load
{:#events-load}








Triggered initial load.

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
<td class="description last">Arguments when load event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   load: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### mergeCellInfo
{:#events-mergecellinfo}








Triggered every time a request is made to access particular cell information, element and data.

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
<td class="description last">Event parameters from grid
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
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid cell.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current row record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the text value in the cell.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>rowMerge</code></td>
<td class="type"><span class="param-type">mergeRowback</span></td>
<td class="description last">Returns the merge rows in grid.</td>
</tr>
<tr>
<td class="name"><code>colMerge</code></td>
<td class="type"><span class="param-type">mergeColback</span></td>
<td class="description last">Returns the merge column in grid.</td>
</tr>
<tr>
<td class="name"><code>merge</code></td>
<td class="type"><span class="param-type">merge</span></td>
<td class="description last">Returns the merge the rows and columns in grid.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   mergeCellInfo: function (args){}
});
&lt;/script&gt;</code>
</pre>






### queryCellInfo
{:#events-querycellinfo}








Triggered every time a request is made to access particular cell information, element and data.

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
<td class="description last">Event parameters from grid
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
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid cell.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current row record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the text value in the cell.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   queryCellInfo: function (args){}
});
&lt;/script&gt;</code>
</pre>






### recordClick
{:#events-recordclick}








Triggered when record is clicked.

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
<td class="description last">Arguments when recordClick event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index of the selected row.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected row.</td>
</tr>
<tr>
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected cell.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   recordClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### recordDoubleClick
{:#events-recorddoubleclick}








Triggered when record is double clicked.

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
<td class="description last">Arguments when recordDoubleClick event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index of the selected row.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected row.</td>
</tr>
<tr>
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected cell.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   recordDoubleClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### resized
{:#events-resized}








Triggered after column resized.

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
<td class="description last">Arguments when resized event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>columnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column index.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid object.</td>
</tr>
<tr>
<td class="name"><code>oldWidth</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the old width value.</td>
</tr>
<tr>
<td class="name"><code>newWidth</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the new width value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   resized: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### resizeEnd
{:#events-resizeend}








Triggered when column resize end.

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
<td class="description last">Arguments when resizeEnd event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>columnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column index.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid object.</td>
</tr>
<tr>
<td class="name"><code>oldWidth</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the old width value.</td>
</tr>
<tr>
<td class="name"><code>newWidth</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the new width value.</td>
</tr>
<tr>
<td class="name"><code>extra</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the extra width value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   resizeEnd: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### resizeStart
{:#events-resizestart}








Triggered when column resize start.

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
<td class="description last">Arguments when resizeStart event is triggered.
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>columnIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column index.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid object.</td>
</tr>
<tr>
<td class="name"><code>oldWidth</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the old width value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   resizeStart: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rightClick
{:#events-rightclick}








Triggered when right clicked on grid element.

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
<td class="description last">Arguments when rightClick event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index of the selected row.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected row.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected row data object.</td>
</tr>
<tr>
<td class="name"><code>cellIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the cell index of the selected cell.</td>
</tr>
<tr>
<td class="name"><code>cellValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the cell value.</td>
</tr>
<tr>
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   rightClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowDataBound
{:#events-rowdatabound}








Triggered every time a request is made to access row information, element and data.

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
<td class="description last">Event parameters from grid
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
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid row.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current row record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
   rowDataBound: function (args){}
});
&lt;/script&gt;</code>
</pre>






### rowSelected
{:#events-rowselected}








Triggered after the row is selected.

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
<td class="description last">Arguments when rowSelected event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>foreignKeyData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index of the selected row.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected row.</td>
</tr>
<tr>
<td class="name"><code>prevRow</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected row element.</td>
</tr>
<tr>
<td class="name"><code>prevRowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected row index.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   rowSelected: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowSelecting
{:#events-rowselecting}








Triggered before the row is going to be selected.

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
<td class="description last">Arguments when rowSelecting event is triggered.
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
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected row index value.</td>
</tr>
<tr>
<td class="name"><code>row</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected row element.</td>
</tr>
<tr>
<td class="name"><code>prevRow</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected row element.</td>
</tr>
<tr>
<td class="name"><code>prevRowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected row index.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   rowSelecting: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### templateRefresh
{:#events-templaterefresh}








Triggered when refresh the template column elements in the Grid.

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
<td class="description last">Arguments when templateRefresh event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>cell</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current row data.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>rowIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current row index.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt;
&lt;script&gt;
$("#Grid").ejGrid({
 templateRefresh: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### toolBarClick
{:#events-toolbarclick}








Triggered when toolbar item is clicked in grid.

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
<td class="description last">Arguments when toolBarClick event is triggered.
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
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentTarget</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the status of toolbar item which denotes its enabled state</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target item.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#Grid").ejGrid({
   toolbarClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>



