---
 layout: post
 title: Properties,Methods and Events of Essential JS ejGrid Widget
 description: Methods,members and events avaliable in ejGrid
 documentation: API
 platform: js
 description: API reference for ejGrid
 keywords: ejGrid, API, Essential JS Grid
---
 
#ejGrid
The grid can be easily configured to the DOM element, such as div. you can create a grid with a highly customizable look and feel.

####Syntax
$(element).ejGrid(options)

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
<td class="name">options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for grid</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
// Create Grid
$('#Grid').ejGrid({
    dataSource: window.gridData
});         
</script>{% endhighlight %}



####Requires
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
* module:ej.menu.js
* module:ej.excelfilter.js


## Members

### allowCellMerging `Boolean`
{:#members:allowcellmerging}

Gets or sets a value that indicates whether to customizing cell based on our needs.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowCellMerging:true,
});
</script> 
{% endhighlight %}

### allowGrouping `Boolean`
{:#members:allowgrouping}

Gets or sets a value that indicates whether to enable dynamic grouping behavior. Grouping can be done by drag on drop desired columns to grid&rsquo;s GroupDropArea. This can be further customized through &ldquo;groupSettings&rdquo; property.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowGrouping:true                      
});
</script> 
{% endhighlight %}

### allowKeyboardNavigation `Boolean`
{:#members:allowkeyboardnavigation}

Gets or sets a value that indicates whether to enable keyboard support for performing grid actions. selectionType &ndash; Gets or sets a value that indicates whether to enable single row or multiple rows selection behavior in grid. Multiple selection can be done through by holding CTRL and clicking the grid rows

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowKeyboardNavigation:false
});
</script> 
{% endhighlight %}

### allowFiltering `Boolean`
{:#members:allowFiltering}

Gets or sets a value that indicates whether to enable dynamic filtering behavior on grid. Filtering can be used to limit the records displayed using required criteria and this can be further customized through &ldquo;filterSettings&rdquo; property

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering:true                       
});
</script>
{% endhighlight %}

### allowSorting `Boolean`
{:#members:allowsorting}

Gets or sets a value that indicates whether to enable the dynamic sorting behavior on grid data. Sorting can be done through clicking on particular column header.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true                       
});
</script> 
{% endhighlight %}

### allowMultiSorting `Boolean`
{:#members:allowmultisorting}

Gets or sets a value that indicates whether to enable multi columns sorting behavior in grid. Sort multiple columns by holding CTRL and click on the corresponding column header.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowSorting:true,
  allowMultiSorting:true
});
</script> 
{% endhighlight %}

### allowPaging `Boolean`
{:#members:allowpaging}

This specifies the grid to show the paginated data. Also enables pager control at the bottom of grid for dynamic navigation through data source. Paging can be further customized through &ldquo;pageSettings&rdquo; property.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}            
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowPaging:true                      
});
</script>                 
{% endhighlight %}

### allowReordering `Boolean`
{:#members:allowreordering}

Gets or sets a value that indicates whether to enable the columns reordering behavior in the grid. Reordering can be done through by drag and drop the particular column from one index to another index within the grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}                     
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowReordering:true
});
</script> 
{% endhighlight %}

### allowResizeToFit `Boolean`
{:#members:allowresizetofit}

Gets or sets a value that indicates whether the column is non resizable. Column width is set automatically based on the content or header text which is large.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowResizeToFit:true,
});
</script> 
{% endhighlight %}

### allowResizing `Boolean`
{:#members:allowresizing}

Gets or sets a value that indicates whether to enable dynamic resizable of columns. Resize the width of the columns by simply click and move the particular column header line

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowResizing:true,
    allowScrolling:true,
    scrollSettings:{width:300,height:300}
});
</script> 
{% endhighlight %}

### allowRowDragAndDrop `Boolean`
{:#members:allowrowdraganddrop}

Gets or sets a value that indicates whether to enable the rows reordering in Grid and drag & drop rows between multiple Grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}                     
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowRowDragAndDrop:true
});
</script> 
{% endhighlight %}

### allowScrolling `Boolean`
{:#members:allowscrolling}

Gets or sets a value that indicates whether to enable the scrollbar in the grid and view the records by scroll through the grid manually

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowScrolling:true,
  scrollSettings:{width:300,height:100}
});
</script> 
{% endhighlight %}

### allowSearching `Boolean`
{:#members:allowsearching}

Gets or sets a value that indicates whether to enable dynamic searching behavior in grid. Currently search box can be enabled through &ldquo;toolbarSettings&rdquo;

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowSearching: true,
    toolbarSettings:{showToolbar:true,toolbarItems:[ej.Grid.ToolBarItems.Search]}
});
</script> 
{% endhighlight %}

### allowSelection `Boolean`
{:#members:allowselection}

Gets or sets a value that indicates whether user can select rows on grid. On enabling feature, selected row will be highlighted.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSelection:true                      
});
</script> 
{% endhighlight %}

### allowTextWrap `Boolean`
{:#members:allowtextwrap}

Gets or sets a value that indicates whether the Content will wrap to the next line if the content exceeds the boundary of the Column Cells.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowTextWrap:true                      
});
</script> 
{% endhighlight %}

### allowMultipleExporting `Boolean`
{:#members:allowmultipleexporting}

Gets or sets a value that indicates whether to enable the multiple exporting behavior on grid data. 

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowMultipleExporting:true                       
});
</script> 
{% endhighlight %}

### commonWidth `Number`
{:#members:commonwidth}

Gets or sets a value that indicates to define common width for all the columns in the grid.

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   commonWidth:200                       
});
</script> 
{% endhighlight %}

### gridLines `enum`
{:#members:gridlines}

<ts name="ej.Grid.GridLines"/>

Gets or sets a value that indicates to enable the visibility of the grid lines.

#### Default Value:
{:.param}
* ej.Grid.GridLines.Both

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Both</td>
<td class="description">Displays both the horizontal and vertical grid lines.</td>
</tr>
<tr>
<td class="name">Horizontal</td>
<td class="description">Displays the horizontal grid lines only.</td>
</tr>
<tr>
<td class="name">Vertical</td>
<td class="description">Displays the vertical grid lines only.</td>
</tr>
<tr>
<td class="name">None</td>
<td class="description">No grid lines are displayed.</td>
</tr>
</table>

#### Example 
{% highlight html %}  
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   gridLines:ej.Grid.GridLines.Vertical                       
});
</script> 
{% endhighlight %}

### childGrid `Object`
{:#members:childgrid}

This specifies the grid to add the grid control inside the grid row of the parent with expand/collapse options

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}           
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
   childGrid: {
dataSource: window.employeeView,
queryString: "EmployeeID",
}
});
</script>
{% endhighlight %}

### columns.clipMode `enum`
{:#members:columns-clipmode}

<ts name="ej.Grid.ClipMode"/>

Sets the clip mode for Grid cell as ellipsis or clipped content(both header and content)

#### Default Value:
{:.param}
* ej.Grid.ClipMode.Clip

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Ellipsis</td>
<td class="description">Shows ellipsis for the overflown cell.</td>
</tr>
<tr>
<td class="name">Clip</td>
<td class="description">Truncate the text in the cell</td>
</tr> 
<tr>
<td class="name">EllipsisWithTooltip</td>
<td class="description">Shows ellipsis and tooltip for the overflown cell.</td>
</tr>   
</table>

#### Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    columns: [{ field: "ShipName", headerText: 'Ship Name', width: 130, clipMode: ej.Grid.ClipMode.Ellipsis}]                                
 });
</script> {% endhighlight %}

### columnLayout `enum`
{:#members:columnlayout}

<ts name="ej.Grid.ColumnLayout"/>

Used to enable or disable static width settings for column. If the columnLayout is set as fixed, then column width will be static.

#### Default Value:
{:.param}
* ej.Grid.ColumnLayout.Auto

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Auto</td>
<td class="description">Column layout is auto(based on width).</td>
</tr>
<tr>
<td class="name">Fixed</td>
<td class="description">Column layout is fixed(based on width).</td>
</tr> 
</table>

#### Example
{:.example}
{% highlight html %}           
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
   columnLayout:ej.Grid.ColumnLayout.Fixed,
    columns: [
       { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, width: 80  },
       { field: "CustomerID", headerText: "Customer ID", width: 90 },
             ],
});
</script>
{% endhighlight %}

### columns `Array`
{:#members:columns}

Gets or sets an object that indicates to render the grid with specified columns

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData
});
var value = $("#Grid").ejGrid("option", "columns");
</script> 
{% endhighlight %}

### columns.allowEditing `Boolean`
{:#members:columns-allowediting}

Gets or sets a value that indicates whether to enable editing behavior for particular column.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings:{allowEditing:true},
  columns:[{field:"OrderID"},{field:"CustomerID",allowEditing:false},{field:"ShipCity"}] 
});
</script> 
{% endhighlight %}

### columns.allowFiltering `Boolean`
{:#members:columns-allowfiltering}

Gets or sets a value that indicates whether to enable dynamic filtering behavior for particular column.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowFiltering:true,
  columns:[{field:"OrderID"},{field:"CustomerID",allowFiltering:false},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.allowGrouping `Boolean`
{:#members:columns-allowgrouping}

Gets or sets a value that indicates whether to enable dynamic grouping behavior for particular column.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowGrouping:true,
  columns:[{field:"OrderID"},{field:"CustomerID",allowGrouping:false},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.allowSorting `Boolean`
{:#members:columns-allowsorting}

Gets or sets a value that indicates whether to enable dynamic sorting behavior for particular column.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowSorting:true,
  columns:[{field:"OrderID"},{field:"CustomerID",allowSorting:false},{field:"ShipCity"}] 
});
</script> 
{% endhighlight %}

### columns.allowResizing `Boolean`
{:#members:columns-allowresizing}

Gets or sets a value that indicates whether to enable dynamic resizable for particular column.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowResizing:true,
  columns:[{field:"OrderID"},{field:"CustomerID",allowResizing:false},{field:"ShipCity"}] 
});
</script> 
{% endhighlight %}

### columns.commands `Array`
{:#members:columns-commands}

Gets or sets an object that indicates to define a command column in the grid.

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### columns.commands.buttonOptions `Object`
{:#members:columns-commands-buttonoptions}

Gets or sets an object that indicates to define all the button options which are available in ejButton.

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### columns.commands.type `enum`
{:#members:columns-commands-type}

<ts name="ej.Grid.UnboundType"/>

Gets or sets a value that indicates to add the command column button. See unboundType

#### Default Value:
{:.param}
* -

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Edit</td>
<td class="description">Unbound type is edit.</td>
</tr>
<tr>
<td class="name">Save</td>
<td class="description">Unbound type is save.</td>
</tr> 
<tr>
<td class="name">Delete</td>
<td class="description">Unbound type is delete.</td>
</tr> 
<tr>
<td class="name">Cancel</td>
<td class="description">Unbound type is cancel.</td>
</tr> 
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### columns.cssClass `String`
{:#members:columns-cssclass}

Gets or sets a value that indicates to provide custom CSS for an individual column.

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<style class="temp">
.temp{
color:green;
}
</style>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",cssClass:"temp"},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.customAttributes `Object`
{:#members:columns-customattributes}

Gets or sets a value that indicates the attribute values to the td element of a particular column

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>          
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",customAttributes:{"style":"color:red"}},{field:"Freight"}]
});
</script>  
{% endhighlight %}

### columns.dataSource `Array`
{:#members:columns-datasource}

Gets or sets a value that indicates to bind the external datasource to the particular column when column `editType` as `dropdownedit` and also it is used to bind the datasource to the foreign key column while editing the grid. //Where data is array of JSON objects of text and value for the drop-down and array of JSON objects for foreign key column.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>  
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },
  columns:[{field:"OrderID"},{field:"CustomerID",visible:false},{ field: "EmployeeID", foreignKeyField: "EmployeeID", foreignKeyValue: "FirstName", dataSource: window.employeeView, headerText: "First Name" }]
});
</script>
{% endhighlight %}


### columns.defaultValue `String|Number|Boolean|Date`
{:#members:columns-defaultvalue}

Gets or sets a value that indicates to display the specified default value while adding a new record to the grid

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>          
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings: {allowAdding: true},
  toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add] },
  columns:[{field:"OrderID"},{field:"CustomerID"},{field:"ShipCity",defaultValue:"ABC"}]
});
</script>
{% endhighlight %}

### columns.disableHtmlEncode `Boolean`
{:#members:columns-disablehtmlencode}

Gets or sets a value that indicates to render the grid content and header with an HTML elements

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    columns:[{field:"OrderID",headerText:"<div&amp;gtOrder ID</div>",disableHtmlEncode:true}]
  });
</script>
{% endhighlight %}

### columns.displayAsCheckBox `Boolean`
{:#members:columns-displayascheckbox}

Gets or sets a value that indicates to display a column value as checkbox or string

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    columns:[{field:"OrderID"}, {field:"Verified", displayAsCheckBox: false}]
  });
</script>
{% endhighlight %}

### columns.editParams `Object`
{:#members:columns-editparams}

Gets or sets a value that indicates to customize ejNumericTextbox of an editable column. See editingType

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    editSettings:{allowEditing:true,allowAdding:true,allowDeleting:true},
    columns:[{ field: "OrderID"}, { field: "Freight", editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }}]
  });
</script>  
{% endhighlight %}

### columns.editTemplate `Object`
{:#members:columns-edittemplate}

Gets or sets a template that displays a custom editor used to edit column values. See editTemplate

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings:{allowEditing:true},
  columns:[{field:"OrderID"},{field:"CustomerID"},
            { field: "EmployeeID",editTemplate: { create: function () { return "<input>"; }, read: function (args) { return args.ejMaskEdit("get_StrippedValue"); }, write: function (args) { args.element.ejMaskEdit({ width: "100%" ,maskFormat: "9",value: args.rowdata !== undefined ? args.rowdata["EmployeeID"]: "" }); } } }]
});
</script>
{% endhighlight %}

### columns.editType `enum`
{:#members:columns-edittype}

<ts name="ej.Grid.EditingType"/>

Gets or sets a value that indicates to render the element(based on edit type) for editing the grid record. See editingType

#### Default Value:
{:.param}
* ej.Grid.EditingType.String

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">String</td>
<td class="description">Specifies editing type as string edit.</td>
</tr>
<tr>
<td class="name">Boolean</td>
<td class="description">Specifies editing type as boolean edit.</td>
</tr> 
<tr>
<td class="name">Numeric</td>
<td class="description">Specifies editing type as numeric edit.</td>
</tr> 
<tr>
<td class="name">Dropdown</td>
<td class="description">Specifies editing type as dropdown edit.</td>
</tr> 
<tr>
<td class="name">DatePicker</td>
<td class="description">Specifies editing type as datepicker.</td>
</tr> 
<tr>
<td class="name">DateTimePicker</td>
<td class="description">Specifies editing type as datetime picker.</td>
</tr> 
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings:{allowEditing:true},
  columns:[{field:"OrderID"},{field:"CustomerID"},{field:"Freight",editType:ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }}]
});
</script> 
{% endhighlight %}

### columns.field `String`
{:#members:columns-field}

Gets or sets a value that indicates to display the columns in the grid mapping with column name of the dataSource.

#### Default Value:
{:.param}
* ""

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"}]
});
</script> 
{% endhighlight %}

### columns.foreignKeyField `String`
{:#members:columns-foreignkeyfield}

Gets or sets a value that indicates to define foreign key field name of the grid datasource.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>          
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"EmployeeID",foreignKeyField:"EmployeeID",foreignKeyValue:"FirstName",headerText:"FirstName",dataSource:window.employeeData },{field:"ShipCity"}]
});
</script>
{% endhighlight %}

### columns.foreignKeyValue `String`
{:#members:columns-foreignkeyvalue}

Gets or sets a value that indicates to bind the field which is in foreign column datasource based on the foreignKeyField

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>  
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"EmployeeID",foreignKeyField:"EmployeeID",foreignKeyValue:"FirstName",dataSource:window.employeeData,headerText:"FirstName"},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.format `String`
{:#members:columns-format}

Gets or sets a value that indicates the format for the text applied on the column

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>          
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID"},{field:"Freight",format:"{0:C}"}]
});
</script>  
{% endhighlight %}

### columns.headerTemplateID `String`
{:#members:columns-headertemplateid}

Gets or sets a value that indicates to add the template within the header element of the particular column.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<div id="customerTemplate">
<span class="e-userlogin e-icon headericon"></span>
 CUS ID
</div>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",headerTemplateID: "#customerTemplate"},{field:"CustomerID"},{field:"ShipCity"}]
});
</script>
{% endhighlight %}

### columns.headerText `String`
{:#members:columns-headertext}

Gets or sets a value that indicates to display the title of that particular column.

#### Default Value:
{:.param}
* ""

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",headerText:"Order ID"},{field:"CustomerID",headerText:"Customer ID"}]
});
</script> 
{% endhighlight %}

### columns.headerTextAlign `enum`
{:#members:columns-headertextalign}

<ts ref="ej.TextAlign"/>

This defines the text alignment of a particular column header cell value. See headerTextAlign

#### Default Value:
{:.param}
* ej.TextAlign.Left

<table>
Add a comment to this line
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Center</td>
<td class="description">Header text is centered.</td>
</tr>
<tr>
<td class="name">Justify</td>
<td class="description">Header text is justified.</td>
</tr> 
<tr>
<td class="name">Left</td>
<td class="description">Header text is aligned to the left.</td>
</tr> 
<tr>
<td class="name">Right</td>
<td class="description">Header text is aligned to the right.</td>
</tr>   
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",headerTextAlign:ej.TextAlign.Center},{field:"CustomerID",headerTextAlign:ej.TextAlign.Right},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.isFrozen `Boolean`
{:#members:columns-isfrozen}

You can use this property to freeze selected columns in grid at the time of scrolling.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({             
  dataSource:window.gridData,
  allowScrolling: true,               
  scrollSettings:{width:500,height:100 }
  columns:[{field:"OrderID",isFrozen:true},{field:"CustomerID"},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.isIdentity `Boolean`
{:#members:columns-isidentity}

Gets or sets a value that indicates the column has an identity in the database.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",isIdentity:true},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.isPrimaryKey `Boolean`
{:#members:columns-isprimarykey}

Gets or sets a value that indicates the column is act as a primary key(read-only) of the grid. The editing is performed based on the primary key column

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({             
  dataSource:window.gridData,
  editSettings:{allowEditing:true},
  columns:[{field:"OrderID",isPrimaryKey:true},{field:"CustomerID"},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.showInColumnChooser `Boolean`
{:#members:columns-showincolumnchooser}

Used to hide the particular column in column chooser by giving value as false.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
 showColumnChooser:true,
    columns:[{field:"OrderID"},{field:"CustomerID",showInColumnChooser:false},{field:"ShipCity"}] 
});
});
</script> 
{% endhighlight %}

### columns.template `Boolean|String`
{:#members:columns-template}

Gets or sets a value that indicates whether to enables column template for a particular column.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script id="columnTemplate" type="text/x-jsrender">
<img src="styles/images/Employees/{{"{{"}}:EmployeeID{{}}}}.png" alt="{{"{{"}}:EmployeeID{{}}}}"/>
</script>
<script>
$("#Grid").ejGrid({
 dataSource:window.gridData,
 columns:[{field:"OrderID",headerText:"TemplateColumn",template:"<span>{{"{{"}}:EmployeeID{{}}}}</span>"},
          {field:"EmployeeID",headerText:"Employee",template:true,templateID:"#columnTemplate"} ]
});
</script>
{% endhighlight %}

### columns.textAlign `enum`
{:#members:columns-textalign}

<ts ref=" ej.TextAlign"/>

Gets or sets a value that indicates to align the text within the column. See textAlign

#### Default Value:
{:.param}
* ej.TextAlign.Left

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Center</td>
<td class="description">Text is centered.</td>
</tr>
<tr>
<td class="name">Justify</td>
<td class="description">Text is justified.</td>
</tr> 
<tr>
<td class="name">Left</td>
<td class="description">Text is aligned to the left.</td>
</tr> 
<tr>
<td class="name">Right</td>
<td class="description">Text is aligned to the right.</td>
</tr>   
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",textAlign:ej.TextAlign.Center},{field:"CustomerID",textAlign:ej.TextAlign.Right},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}


### columns.tooltip `string`
{:#members:columns-tooltip}

Sets the template for Tooltip in Grid Columns(both header and content)

Default Value:
{:.param}
* null

#### Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script type="text/template" id="colTip">
  {{"{{"}}:value {{}}}}
  </script>
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   columns: [{ field: "ShipName", headerText: 'Ship Name', width: 130, tooltip:"#colTip"}] 
     });
</script> {% endhighlight %}

### columns.type `String`
{:#members:columns-type}

Gets or sets a value that indicates to specify the data type of the specified columns.

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    columns:[{ field: "OrderID"}, { field: "Verified",type: "boolean" }]
  });
</script>  
{% endhighlight %}

### columns.validationRules `Object`
{:#members:columns-validationrules}

Gets or sets a value that indicates to define constraints for saving data to the database.

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>          
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  editSettings: {allowEditing: true, allowAdding: true},
  columns:[{field:"OrderID", validationRules: { required: true, number: true }},{field:"CustomerID"},{field:"ShipCity"}] 
});
</script> 
{% endhighlight %}

### columns.visible `Boolean`
{:#members:columns-visible}

Gets or sets a value that indicates whether this column is visible in the grid.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID"},{field:"CustomerID",visible:false},{field:"ShipCity"}]
});
</script> 
{% endhighlight %}

### columns.width `Number`
{:#members:columns-width}

Gets or sets a value that indicates to define the width for a particular column in the grid.

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>          
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field:"OrderID",width:50},{field:"CustomerID",width:"15%"},{field:"ShipCity",width:"70px"}]
});
</script>
{% endhighlight %}

### contextMenuSettings `Object`
{:#members:contextmenusettings}

Gets or sets an object that indicates whether to customize the context menu behavior of the grid.

### contextMenuSettings.contextMenuItems `Array`
{:#members:contextmenusettings-contextmenuitems}

Gets or sets a value that indicates whether to add the default context menu actions as a context menu items If enableContextMenu is true it will show all the items related to the target, if you want selected items from contextmenu you have to mention in the contextMenuItems

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowDeleting: true, allowEditing: true, allowAdding: true },
   allowGrouping: true,
   allowSorting: true,
   allowPaging: true,
   contextMenuSettings: { enableContextMenu: true, contextMenuItems:["Add Record,Edit Record,Delete Record"]  }
});
</script>
{% endhighlight %}

### contextMenuSettings.customContextMenuItems `Array`
{:#members:contextmenusettings-customcontextmenuitems}

Gets or sets a value that indicates whether to add custom contextMenu items within the toolbar to perform any action in the grid

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<style type="text/css" class="cssStyles">
</style>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData, 
  contextMenuSettings: { enableContextMenu: true, customContextMenuItems:["Hidden Columns,Visible Columns"]  }
});
</script>
{% endhighlight %}

### contextMenuSettings.enableContextMenu `Boolean`
{:#members:contextmenusettings-enablecontextmenu}

Gets or sets a value that indicates whether to enable the context menu action in the grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource: window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowDeleting: true, allowEditing: true, allowAdding: true },
   allowGrouping: true,
   allowSorting: true,
   allowPaging: true,
   contextMenuSettings: { enableContextMenu: true }
});
</script> 
{% endhighlight %}

### contextMenuSettings.subContextMenu `Array`
{:#members:contextmenusettings-subcontextmenu}

Used to get or set the subMenu to the corresponding custom context menu item.

### contextMenuSettings.subContextMenu.contextMenuItem `string`
{:#members:contextmenusettings-subcontextmenu-contextmenuitem}

Used to get or set the corresponding custom context menu item to which the submenu to be appended.

#### Default Value:
{:.param}
* null

### contextMenuSettings.subContextMenu.subMenu `Array`
{:#members:contextmenusettings-subcontextmenu-submenu}

Used to get or set the sub menu items to the custom context menu item.

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },
   contextMenuSettings: { enableContextMenu: true, customContextMenuItems: ["Hide Column"],
   subContextMenu: [{ contextMenuItem: "Hide Column", subMenu: ["OrderID", "CustomerID", "EmployeeID"] }] 
  },          
});
</script>
{% endhighlight %}


### contextMenuSettings.disableDefaultItems `Boolean`
{:#members:contextmenusettings-disabledefaultitems}

Gets or sets a value that indicates whether to disable the default context menu items in the grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource: window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowDeleting: true, allowEditing: true, allowAdding: true },
   allowGrouping: true,
   allowSorting: true,
   allowPaging: true,
   contextMenuSettings: { enableContextMenu: true, customContextMenuItems:["Hidden Columns,Visible Columns"], disableDefaultItems: true }
});
</script> 
{% endhighlight %}


### cssClass `String`
{:#members:cssclass}

Gets or sets a value that indicates to render the grid with custom theme. 

#### Default Value:
{:.param}
* ""

#### Example
{:.example}
{% highlight html %}
 
<div id="Grid"></div>
<style type="text/css">
   .gradient-green {
       font-family: cursive;
   }
   .gradient-green .e-alt_row {
       background: none repeat scroll 0 0 #71A409;
   }
</style>
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   cssClass: "gradient-green"
});
</script> 
{% endhighlight %}

### dataSource `Object`
{:#members:datasource}

Gets or sets the data to render the grid with records

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData
});
</script> 
{% endhighlight %}

### detailsTemplate `String`
{:#members:detailstemplate}
This specifies the grid to add the details row for the corresponding master row

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script id="templateData" type="text/x-jsrender">
<table>
<tr>
<td>
<img src="styles/images/Employees/{{"{{"}}:EmployeeID{{}}}}.png" alt="{{"{{"}}:EmployeeID{{}}}}"/>
</td>
</tr>
</table>
</script>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  detailsTemplate:"#templateData",
  detailsDataBound: "detailGridData",
});             
</script>            
{% endhighlight %}

### editSettings `Object`
{:#members:editsettings}

Gets or sets an object that indicates whether to customize the editing behavior of the grid.

### editSettings.allowAdding `Boolean`
{:#members:editsettings-allowadding}

Gets or sets a value that indicates whether to enable insert action in the editing mode.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowAdding: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["add"] }                             
});
</script>                
{% endhighlight %}

### editSettings.allowDeleting `Boolean`
{:#members:editsettings-allowdeleting}

Gets or sets a value that indicates whether to enable the delete action in the editing mode.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowDeleting: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["delete"] }      
});
</script>                  
{% endhighlight %}

### editSettings.allowEditing `Boolean`
{:#members:editsettings-allowediting}

Gets or sets a value that indicates whether to enable the edit action in the editing mode.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }
});
</script>             
{% endhighlight %}

### editSettings.allowEditOnDblClick `Boolean`
{:#members:editsettings-alloweditondblclick}

Gets or sets a value that indicates whether to enable the editing action while double click on the record

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
Defining editEvent with edit option:
<div id="Grid"></div> 
<script> 
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, allowEditOnDblClick: false },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }      
});
</script> 
{% endhighlight %}

### editSettings.dialogEditorTemplateID `String`
{:#members:editsettings-dialogeditortemplateid}

This specifies the id of the template. This template can be used to display the data that you require to be edited using the Dialog Box

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}               
<div id="Grid"></div>
<script id="template" type="text/template">
   <table>
       <tr>
           <td>OrderID</td>
           <td>
               <input id="OrderID" name="OrderID" value="{{"{{"}}:OrderID{{}}}}" disabled="disabled" /></td>
       </tr>
       <tr>
           <td>CustomerID</td>
           <td>
               <input id="CustomerID" name="CustomerID" value="{{"{{"}}:CustomerID{{}}}}" /></td>
       </tr>
       <tr>
           <td>EmployeeID</td>
           <td>
               <input id="EmployeeID" name="EmployeeID" value="{{"{{"}}:EmployeeID{{}}}}" /></td>
       </tr>
   </table>
</script>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.DialogTemplate, dialogEditorTemplateID: "#template" },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
</script>                
{% endhighlight %}

### editSettings.editMode `enum`
{:#members:editsettings-editmode}

<ts name="ej.Grid.EditMode"/>

Gets or sets a value that indicates whether to define the mode of editing See editMode

#### Default Value:
{:.param}
* ej.Grid.EditMode.Normal

<table>
Add a comment to this line
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Normal</td>
<td class="description">Edit mode is normal.</td>
</tr>
<tr>
<td class="name">Dialog</td>
<td class="description">Edit mode is dialog.</td>
</tr>  
<tr>
<td class="name">DialogTemplate</td>
<td class="description">Edit mode is dialog template.</td>
</tr> 
<tr>
<td class="name">Batch</td>
<td class="description">Edit mode is batch.</td>
</tr> 
<tr>
<td class="name">InlineForm</td>
<td class="description">Edit mode is inline form.</td>
</tr> 
<tr>
<td class="name">InlineTemplateForm</td>
<td class="description">Edit mode is inline template form.</td>
</tr> 
<tr>
<td class="name">ExternalForm</td>
<td class="description">Edit mode is external form.</td>
</tr> 
<tr>
<td class="name">ExternalFormTemplate</td>
<td class="description">Edit mode is external form template.</td>
</tr> 
</table>

#### Example
{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.Dialog },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
</script>                          
{% endhighlight %}

### editSettings.externalFormTemplateID `String`
{:#members:editsettings-externalformtemplateid}

This specifies the id of the template. This template can be used to display the data that you require to be edited using the External edit form

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}               
<div id="Grid"></div>
<script id="template" type="text/template">
   <table>
       <tr>
           <td>OrderID</td>
           <td>
               <input id="OrderID" name="OrderID" value="{{"{{"}}:OrderID{{}}}}" disabled="disabled" /></td>
       </tr>
       <tr>
           <td>CustomerID</td>
           <td>
               <input id="CustomerID" name="CustomerID" value="{{"{{"}}:CustomerID{{}}}}" /></td>
       </tr>
       <tr>
           <td>EmployeeID</td>
           <td>
               <input id="EmployeeID" name="EmployeeID" value="{{"{{"}}:EmployeeID{{}}}}" /></td>
       </tr>
   </table>
</script>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.ExternalFormTemplate, externalFormTemplateID: "#template" },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
</script>                
{% endhighlight %}

### editSettings.formPosition `enum`
{:#members:editsettings-formposition}

<ts name="ej.Grid.FormPosition"/>

This specifies to set the position of an External edit form either in the top-right or bottom-left of the grid

#### Default Value:
{:.param}
* ej.Grid.FormPosition.BottomLeft

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">BottomLeft</td>
<td class="description">Form position is bottomleft.</td>
</tr>
<tr>
<td class="name">TopRight</td>
<td class="description">Form position is topright.</td>
</tr> 
</table>

#### Example
{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowAdding: true, allowEditing: true, editMode: ej.Grid.EditMode.ExternalForm, formPosition: ej.Grid.FormPosition.BottomLeft },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
</script>    
{% endhighlight %}

### editSettings.inlineFormTemplateID `String`
{:#members:editsettings-inlineformtemplateid}

This specifies the id of the template. This template can be used to display the data that you require to be edited using the Inline edit form

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}               
<div id="Grid"></div>
<script id="template" type="text/template">
   <table>
       <tr>
           <td>OrderID</td>
           <td>
               <input id="OrderID" name="OrderID" value="{{"{{"}}:OrderID{{}}}}" disabled="disabled" /></td>
       </tr>
       <tr>
           <td>CustomerID</td>
           <td>
               <input id="CustomerID" name="CustomerID" value="{{"{{"}}:CustomerID{{}}}}" /></td>
       </tr>
       <tr>
           <td>EmployeeID</td>
           <td>
               <input id="EmployeeID" name="EmployeeID" value="{{"{{"}}:EmployeeID{{}}}}" /></td>
       </tr>
   </table>
</script>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.InlineTemplateForm, inlineFormTemplateID: "#template" },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit"] }                             
});
</script>                
{% endhighlight %}

### editSettings.rowPosition `enum`
{:#members:editsettings-rowposition}

<ts name="ej.Grid.RowPosition"/>

This specifies to set the position of an adding new row either in the top or bottom of the grid

#### Default Value:
{:.param}
* ej.Grid.RowPosition.Top

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Top</td>
<td class="description">Specifies position of add new row as top.</td>
</tr>
<tr>
<td class="name">Bottom</td>
<td class="description">Specifies position of add new row as bottom.</td>
</tr> 
</table>

#### Example
{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, allowAdding:true, rowPosition:"bottom" },
    toolbarSettings: { showToolbar: true, toolbarItems: ["add"]  },                             
});
</script>                          
{% endhighlight %}

### editSettings.showConfirmDialog `Boolean`
{:#members:editsettings-showconfirmdialog}

Gets or sets a value that indicates whether the confirm dialog has to be shown while saving or discarding the batch changes

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.Batch, showConfirmDialog:false },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit","update","cancel"] }                             
});
</script>                          
{% endhighlight %}

### editSettings.showDeleteConfirmDialog `Boolean`
{:#members:editsettings-showdeleteconfirmdialog}

Gets or sets a value that indicates whether the confirm dialog has to be shown while deleting record

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowDeleting: true, showDeleteConfirmDialog:true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit","update","cancel"] }                             
});
</script>                          
{% endhighlight %}

### editSettings.titleColumn `String`
{:#members:editsettings-titleColumn}

Gets or sets a value that indicates whether the title for edit form is different from the primarykey column.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowAdding: true, showAddNewRow: true, editMode: ej.Grid.EditMode.Dialog, titleColumn: "CustomerID"},
    toolbarSettings: { showToolbar: true, toolbarItems: ["edit","update","cancel"] }                             
});
</script>                 
{% endhighlight %}

### editSettings.showAddNewRow `Boolean`
{:#members:editsettings-showaddnewrow}

Gets or sets a value that indicates whether to display the add new form by default in the grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    editSettings: { allowAdding: true, showAddNewRow: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["add"] }                             
});
</script>                 
{% endhighlight %}

### enableAltRow `Boolean`
{:#members:enablealtrow}

Gets or sets a value that indicates whether to enable the alternative rows differentiation in the grid records based on corresponding theme.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  enableAltRow:true,
});
</script> 
{% endhighlight %}

### enableAutoSaveOnSelectionChange `Boolean`
{:#members:enableautosaveonselectionchange}

Gets or sets a value that indicates whether to enable the save action in the grid through row selection

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    editSettings: { allowEditing: true },
    toolbarSettings: { showToolbar: true, toolbarItems: ["cancel", "save"]},
    columns: [{ field: "OrderID", isPrimaryKey: true }, { field: "CustomerID" }, { field: "ShipCity" }],
    enableAutoSaveOnSelectionChange: false
});
</script> 
{% endhighlight %}

### enableHeaderHover `Boolean`
{:#members:enableheaderhover}

Gets or sets a value that indicates whether to enable mouse over effect on the corresponding column header cell of the grid

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   enableHeaderHover:true
});
</script> 
{% endhighlight %}

### enablePersistence `Boolean`
{:#members:enablepersistence}

Gets or sets a value that indicates whether to persist the grid model state in page using applicable medium i.e., HTML5 localStorage or cookies

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping: true,
    enablePresistence:true
});
</script> 
{% endhighlight %}

### enableResponsiveRow `Boolean`
{:#members:enableresponsiverow}

Gets or sets a value that indicates whether the grid rows has to be rendered as detail view in mobile mode

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}       
<div id="Grid"></div>  
<script type="text/javascript"> 
$("#Grid").ejGrid({
  dataSource: window.gridData,
                isResponsive: true,
                enableResponsiveRow: true    
});  
</script>
{% endhighlight %}

### enableRowHover `Boolean`
{:#members:enablerowhover}

Gets or sets a value that indicates whether to enable mouse over effect on corresponding grid row.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   enableRowHover:true
});
</script> 
{% endhighlight %}

### enableRTL `Boolean`
{:#members:enablertl}

Align content in the grid control from right to left by setting the property as true.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  enableRTL:true,
});
</script> 
{% endhighlight %}

### enableTouch `Boolean`
{:#members:enabletouch}

To Disable the mouse swipe property as false.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    enableTouch:false
});
</script> 
{% endhighlight %}

### filterSettings `Object`
{:#members:filtersettings}

Gets or sets an object that indicates whether to customize the filtering behavior of the grid

### filterSettings.enableCaseSensitivity `Boolean`
{:#members:filtersettings-enablecasesensitivity}

Gets or sets a value that indicates to perform the filter operation with case sensitive in excel styled filter menu mode

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
    allowFiltering: true, 
    filterSettings: { enableCaseSensitivity:true, filterType:"excel"}                       
});
</script>
{% endhighlight %}

### filterSettings.filterBarMode `enum`
{:#members:filtersettings-filterbarmode}

<ts name="ej.Grid.FilterBarMode"/>

This specifies the grid to starts the filter action while typing in the filterBar or after pressing the enter key. based on the filterBarMode. See filterBarMode

#### Default Value:
{:.param}
* ej.Grid.FilterBarMode.Immediate

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Immediate</td>
<td class="description">Initiate filter operation on typing the filter query.</td>
</tr>
<tr>
<td class="name">OnEnter</td>
<td class="description">Initiate filter operation after Enter key is pressed.</td>
</tr> 
</table>


#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering: true, 
   filterSettings:{ filterBarMode: ej.Grid.FilterBarMode.OnEnter }                
});
</script>
{% endhighlight %}

### filterSettings.filteredColumns `Array`
{:#members:filtersettings-filteredcolumns}

Gets or sets a value that indicates whether to define the filtered columns details programmatically at initial load

#### Default Value:
{:.param}
* []

### filterSettings.filteredColumns.field `string`
{:#members:filtersettings-filteredcolumns-field}

Gets or sets a value that indicates whether to define the field name of the column to be filter.

### filterSettings.filteredColumns.operator `enum`
{:#members:filtersettings-filteredcolumns-operator}

<ts ref="ej.FilterOperators"/>

Gets or sets a value that indicates whether to define the filter condition to filtered column.

#### Default Value:
{:.param}
* -

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">startsWith</td>
<td class="description">Specifies the filter operator as startswith.</td>
</tr>
<tr>
<td class="name">endsWith</td>
<td class="description">Specifies the filter operator as endswith.</td>
</tr> 
<tr>
<td class="name">contains</td>
<td class="description">Specifies the filter operator as contains.</td>
</tr> 
<tr>
<td class="name">equal</td>
<td class="description">Specifies the filter operator as equal.</td>
</tr> 
<tr>
<td class="name">notEqual</td>
<td class="description">Specifies the filter operator as notequal.</td>
</tr> 
<tr>
<td class="name">greaterThan</td>
<td class="description">Specifies the filter operator as greaterthan.</td>
</tr> 
<tr>
<td class="name">greaterThanOrEqual</td>
<td class="description">Specifies the filter operator as greaterthanorequal.</td>
</tr> 
<tr>
<td class="name">lessThan</td>
<td class="description">Specifies the filter operator as lessthan.</td>
</tr> 
<tr>
<td class="name">lessThanOrEqual</td>
<td class="description">Specifies the filter operator as Lessthanorequal.</td>
</tr> 
</table>

### filterSettings.filteredColumns.predicate `string`
{:#members:filtersettings-filteredcolumns-predicate}

Gets or sets a value that indicates whether to define the predicate as and/or.

### filterSettings.filteredColumns.value `string|number`
{:#members:filtersettings-filteredcolumns-value}

Gets or sets a value that indicates whether to define the value to be filtered in a column.

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering: true, 
   filterSettings: {  filterType: "menu", filteredColumns: [{ field: "ShipCity", operator: "startswith", value: "re", predicate: "and" }] }                     
});
</script>
{% endhighlight %}

### filterSettings.filterType `enum`
{:#members:filtersettings-filtertype}

<ts name="ej.Grid.FilterType"/>

This specifies the grid to show the filterBar or filterMenu to the grid records. See <a href="global.html#filterType">filterType</a>

#### Default Value:
{:.param}
* ej.Grid.FilterType.FilterBar

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Menu</td>
<td class="description">Specifies the filter type as menu.</td>
</tr>
<tr>
<td class="name">Excel</td>
<td class="description">Specifies the filter type as excel.</td>
</tr> 
<tr>
<td class="name">FilterBar</td>
<td class="description">Specifies the filter type as filterbar.</td>
</tr> 
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering: true, 
   filterSettings: {  filterType: "menu" }                     
});
</script>
{% endhighlight %}

### filterSettings.maxFilterChoices `Number`
{:#members:filtersettings-maxfilterchoices}

Gets or sets a value that indicates the maximum number of filter choices that can be showed in the excel styled filter menu.

#### Default Value:
{:.param}
* 1000

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
    allowFiltering: true, 
    filterSettings: { maxFilterChoices:200, filterType:"excel"}                       
});
</script>
{% endhighlight %}

### filterSettings.showFilterBarMessage `Boolean`
{:#members:filtersettings-showfilterbarmessage}

This specifies the grid to show the filter text within the grid pager itself.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowFiltering: true, 
   filterSettings: {  showFilterBarStatus: true }                        
});
</script>
{% endhighlight %}

### filterSettings.showPredicate `Boolean`
{:#members:filtersettings-showpredicate}

Gets or sets a value that indicates whether to enable the predicate options in the filtering menu

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
    allowFiltering: true, 
    filterSettings: { showPredicate:true, filterType:"menu"}                       
});
</script>
{% endhighlight %}

### groupSettings `Object`
{:#members:groupsettings}

Gets or sets an object that indicates whether to customize the grouping behavior of the grid.

### groupSettings.captionFormat `String`
{:#members:groupsettings-captionformat}

Gets or sets a value that customize the group caption format.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{captionFormat: "{{:field}} - {{:key}} : {{:count}} {{if count == 1 }} item {{else}} items {{/if}}"}                          
});
</script> 
{% endhighlight %}

### groupSettings.enableDropAreaAutoSizing `Boolean`
{:#members:groupsettings-enabledropareaautosizing}

Gets or sets a value that indicates whether to enable animation button option in the group drop area of the grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{enableDropAreaAutoSizing: true}
});
</script> 
{% endhighlight %}

### groupSettings.groupedColumns `Array`
{:#members:groupsettings-groupedcolumns}

Gets or sets a value that indicates whether to add grouped columns programmatically at initial load

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{groupedColumns:["OrderID"]}
});
</script> 
{% endhighlight %}

### groupSettings.showDropArea `Boolean`
{:#members:groupsettings-showdroparea}

Gets or sets a value that indicates whether to show the group drop area just above the column header. It can be used to avoid ungrouping the already grouped column using `groupSettings`.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{showDropArea:false, groupedColumns: ["ShipCity"]},
    columns: [{ field: "OrderID" }, { field: "CustomerID" }, { field: "ShipCity" }]
});
</script>   
{% endhighlight %}

### groupSettings.showGroupedColumn `Boolean`
{:#members:groupsettings-showgroupedcolumn}

Gets or sets a value that indicates whether to hide the grouped columns from the grid

#### Default Value:
{:.param}
* false

#### Example
{:.example}


{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{showGroupedColumn:false}
});
</script> 
{% endhighlight %}

### groupSettings.showToggleButton `Boolean`
{:#members:groupsettings-showtogglebutton}

Gets or sets a value that indicates whether to show the group button image(toggle button)in the column header and also in the grouped column in the group drop area . It can be used to group/ungroup the columns by click on the toggle button.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{showToggleButton:true}
});
</script>   
{% endhighlight %}

### groupSettings.showUngroupButton `Boolean`
{:#members:groupsettings-showungroupbutton}

Gets or sets a value that indicates whether to enable the close button in the grouped column which is in the group drop area to ungroup the grouped column

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowGrouping:true,
    groupSettings:{showToggleButton: true, showUngroupButton:true}
});
</script> 
{% endhighlight %}

### isResponsive `Boolean`
{:#members:isresponsive}

Gets or sets a value that indicates whether the grid design has be to made responsive.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}       
<div id="Grid"></div> 
 
<script type="text/javascript"> 
$("#Grid").ejGrid({
  dataSource: window.gridData,
                isResponsive: true 
});  
</script>
{% endhighlight %}

### keySettings `Object`
{:#members:keysettings}

This specifies to change the key in keyboard interaction to grid control

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}            
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
   keySettings: {
saveRequest: "83",
moveCellRight: "13",
}
});
</script>
{% endhighlight %}

### locale `String`
{:#members:locale}

Gets or sets a value that indicates whether to customizing the user interface (UI) as locale-specific in order to display regional data i.e. in a language and culture specific to a particular country or region.

#### Default Value:
{:.param}
* "en-US"

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
ej.Pager.locale["es-ES"] = {
   pagerInfo: "{0} de {1} p&aacute;ginas ({2} art&iacute;culos)"
};
$("#Grid").ejGrid({
  dataSource:window.gridData,
  allowPaging:true,
  locale : "es-ES" 
});
</script>             
{% endhighlight %}

### minWidth `Number`
{:#members:minwidth}

Gets or sets a value that indicates whether to set the minimum width of the responsive grid while isResponsive property is true and enableResponsiveRow property is set as false.

#### Default Value:
{:.param}
* 0

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData, 
  minWidth: 990,
  isResponsive: true
});
</script>
{% endhighlight %}

### mediaSettings `Object`
{:#members:mediasettings}

Gets or sets an object that indicates whether to modify the media query default configuration.

### mediaSettings.phone `Number`
{:#members:mediaSettings-phone}

Gets or sets a value that indicates whether the grid rows has to be rendered as detail view in mobile mode while enableResponsiveRow property is set as true and also need to set same value for max-width in ejgrid.responsive.css file

#### Default Value:
{:.param}
* 320

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true, 
    isResponsive: true,
    enableResponsiveRow: true, 
    mediaSettings: { phone: 340 }
});
</script>
{% endhighlight %}

### pageSettings `Object`
{:#members:pagesettings}

Gets or sets an object that indicates whether to modify the pager default configuration.

### pageSettings.currentPage `Number`
{:#members:pagesettings-currentpage}

Gets or sets a value that indicates whether to define which page to display currently in the grid

#### Default Value:
{:.param}
* 1

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true,   
    pageSettings: { currentPage: 1 }
});
</script>
{% endhighlight %}

### pageSettings.enableQueryString `Boolean`
{:#members:pagesettings-enablequerystring}

Gets or sets a value that indicates whether to pass the current page information as a query string along with the URL while navigating to other page.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true,   
    pageSettings: {enableQueryString: true }
});
</script>
{% endhighlight %}

### pageSettings.enableTemplates `Boolean`
{:#members:pagesettings-enabletemplates}

Gets or sets a value that indicates whether to enables pager template for the grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script id="pagerTemplate" type="text/x-jsrender">
 <input type="text" id="txtPageNumber"  value="" style="width: 45px; border: none; cursor: text" />
<input type="button" value="Go" style="border: none; cursor: pointer" id="btnGo" onclick="gotoPage(this)" />
</script>
<script>
$("#Grid").ejGrid({
 dataSource:window.gridData,
 pageSettings:{enableTemplates:true,template:"#pagerTemplate"}
});
</script>
{% endhighlight %}

### pageSettings.pageCount `Number`
{:#members:pagesettings-pagecount}

Gets or sets a value that indicates whether to define the number of pages displayed in the pager for navigation

#### Default Value:
{:.param}
* 8

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    allowPaging: true,    
    pageSettings: { pageCount: 1 }
});
</script>
{% endhighlight %}

### pageSettings.pageSize `Number`
{:#members:pagesettings-pagesize}

Gets or sets a value that indicates whether to define the number of records displayed per page

#### Default Value:
{:.param}
* 12

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,
    allowPaging: true,   
    pageSettings: { pageSize: 2 }
});
</script>
{% endhighlight %}

### pageSettings.showDefaults `Boolean`
{:#members:pagesettings-showdefaults}

Gets or sets a value that indicates whether to enables default pager for the grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script id="pagerTemplate" type="text/x-jsrender">
 <input type="text" id="txtPageNumber"  value="" style="width: 45px; border: none; cursor: text" />
<input type="button" value="Go" style="border: none; cursor: pointer" id="btnGo" />
</script>
<script>
$("#Grid").ejGrid({
 dataSource:window.gridData,
 pageSettings:{showDefaults:true,enableTemplates:true,templateID:"#pagerTemplate"}
});
</script>
{% endhighlight %}

### pageSettings.template `String`
{:#members:pagesettings-template}

Gets or sets a value that indicates to add the template as a pager template for grid.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script id="pagerTemplate" type="text/x-jsrender">
 <input type="text" id="txtPageNumber"  value="" style="width: 45px; border: none; cursor: text" />
<input type="button" value="Go" style="border: none; cursor: pointer" id="btnGo" />
</script>
<script>
$("#Grid").ejGrid({
 dataSource:window.gridData,
 pageSettings:{enableTemplates:true,template:"#pagerTemplate"}
});
</script>
{% endhighlight %}

### pageSettings.totalPages `Number`
{:#members:pagesettings-totalpages}

Get the value of total number of pages in the grid. The totalPages value is calculated based on page size and total records of grid

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>
<div id="print"></div>
<script>
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true    
});
var value = $("#Grid").ejGrid("option", "pageSettings.totalPages");
$("#print").text("TotalPages: " + value);
</script>
{% endhighlight %}

### pageSettings.totalRecordsCount `Number`
{:#members:pagesettings-totalrecordscount}

Get the value of total number of records which is bound to the grid. The totalRecordsCount value is calculated based on dataSource bound to the grid.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>
<div id="print"></div>
<script>
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true
});
var value = $("#Grid").ejGrid("option", "pageSettings.totalRecordsCount");
$("#print").text("TotalRecordsCount: " + value);
</script>
{% endhighlight %}

### pageSettings.printMode `enum`
{:#members:pagesettings-printmode}

<ts name="ej.Grid.PrintMode"/>

Gets or sets a value that indicates whether to define the number of pages to print

#### Default Value:
{:.param}
* ej.Grid.PrintMode.AllPages

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">AllPages</td>
<td class="description">Prints all pages.</td>
</tr>
<tr>
<td class="name">CurrentPage</td>
<td class="description">Prints current page.</td>
</tr>  
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowPaging:true,
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.PrintGrid] },
   pageSettings:{printMode:ej.Grid.PrintMode.CurrentPage},
});
</script>
{% endhighlight %}

### query `Object`
{:#members:query}

Query the dataSource from the table for Grid.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}       
<div id="Grid"></div> 
 
<script type="text/javascript">
var queryOrder=ej.Query().select(["OrderID", "CustomerID"]); 
$("#Grid").ejGrid({
  dataSource: window.gridData,
  query: queryOrder
});  
</script>
{% endhighlight %}

### resizeSettings `Object`
{:#members:resizeSettings}

Gets or sets an object that indicates whether to modify the resizing behaviour.
### resizeSettings.resizeMode `enum`
{:#members:resizeSettings-resizeMode}

<ts name="ej.Grid.ResizeMode"/>

Gets or sets a value that indicates whether to define the mode of resizing.
Accepting types are "normal", "nextcolumn" and "control".

#### Default Value:
{:.param}
* ej.Grid.ResizeMode.Normal

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Normal</td>
<td class="description">New column size will be adjusted by all other Columns</td>
</tr>
<tr>
<td class="name">NextColumn</td>
<td class="description">New column Size will be adjusted using next column.</td>
</tr>
<tr>
<td class="name">Control</td>
<td class="description">New column Size will be adjusted using entire control</td>
</tr>
</table>

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowPaging: true, 
    allowResizing: true,  
    resizeSettings: { resizeMode: "control" }
});
</script>
{% endhighlight %}

### rowTemplate `String`
{:#members:rowtemplate}

Gets or sets a value that indicates to render the grid with template rows. The template row must be a table row. That table row must have the JavaScript render binding format ({{:columnName}}) then the grid data source binds the data to the corresponding table row of the template.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script id="templateData" type="text/x-jsrender">
<tr>
<td>
<img src="styles/images/Employees/{{"{{"}}:EmployeeID{{}}}}.png" alt="{{"{{"}}:EmployeeID{{}}}}"/>
</td>
<td>
{{"{{"}}:EmployeeID{{}}}}
</td>
</tr>
</script>
<script>
$("#Grid").ejGrid({
 dataSource:window.gridData,
  rowTemplate:"#templateData",
  columns:[{headerText:"Employeephoto"},{field:"EmployeeID",headerText:"EmployeeID"}],
});
</script>
{% endhighlight %}

### rowDropSettings `Object`
{:#members:rowdropsettings}

Gets or sets an object that indicates whether to customize the drag and drop behavior of the grid rows    

### rowDropSettings.dropTargetID `object`
{:#members:rowdropsettings-droptargetid}

This specifies the grid to drop the grid rows only at particular target element.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowRowDragAndDrop: true,
   rowDropSettings: { dropTargetID: "#DestGrid" }
});
</script> 
{% endhighlight %}

### rowDropSettings.dragMapper `string`
{:#members:rowdropsettings-dragmapper}

This helps in mapping server-side action when rows are dragged from Grid.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowRowDragAndDrop: true,
   rowDropSettings: { dropTargetID: "#DestGrid", dragMapper: "Home/DragHandler" }
});
</script> 
{% endhighlight %}

### rowDropSettings.dropMapper `string`
{:#members:rowdropsettings-dropmapper}

This helps in mapping server-side action when rows are dropped in Grid.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowRowDragAndDrop: true,
   rowDropSettings: { dropTargetID: "#DestGrid", dropMapper: "Home/DragHandler" }
});
</script> 
{% endhighlight %}

### searchSettings `Object`
{:#members:searchsettings}

Gets or sets an object that indicates whether to customize the searching behavior of the grid

### searchSettings.fields `object`
{:#members:searchsettings-fields}

This specify the grid to search for the value in particular columns that is mentioned in the field.

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSearching: true,
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Search] },
   searchSettings: { fields:["OrderID","CustomerID","EmployeeID"], key:"VINET"}
});
</script> 
{% endhighlight %}

### searchSettings.key `string`
{:#members:searchsettings-key}

This specifies the grid to search the particular data that is mentioned in the key.

#### Default Value:
{:.param}
* ""

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSearching: true,
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Search] },
   searchSettings: { key:"VINET" }
});
</script> 
{% endhighlight %}

### searchSettings.operator `string`
{:#members:searchsettings-operator}

It specifies the grid to search the records based on operator.

**List of enum type operators**
1. ej.FilterOperators.contain
2. ej.FilterOperators.equal
3. ej.FilterOperators.notEqual
4. ej.FilterOperators.startsWith
5. ej.FilterOperators.endsWith

#### Default Value:
{:.param}
* contains

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSearching: true,
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Search] },
   searchSettings: { operator:"contains", key:"VINET"}
});
</script> 
{% endhighlight %}

### searchSettings.ignoreCase `boolean`
{:#members:searchsettings-ignorecase}

It enables or disables case-sensitivity while searching the search key in grid.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSearching: true,
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Search] },
   searchSettings: { ignoreCase: true, key:"VINET" }
});
</script> 
{% endhighlight %}

### selectedRecords `Array`
{:#members:selectedrecords}

Gets a value that indicates whether the grid model to hold multiple selected records . selectedRecords can be used to displayed hold the single or multiple selected records using &ldquo;selectedRecords&rdquo; property

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
});                       
</script>
<script>
// display single or multiple selected records
$("#Grid").ejGrid("model.selectedRecords")        
</script>
{% endhighlight %}

### selectedRowIndex `Number`
{:#members:selectedrowindex}

Gets or sets a value that indicates to select the row while initializing the grid

#### Default Value:
{:.param}
* -1

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    selectedRowIndex:1
});
</script> 
{% endhighlight %}

### selectionSettings `Object`
{:#members:selectionsettings}

This property is used to configure the selection behavior of the grid.

### selectionSettings.enableToggle `Boolean`
{:#members:selectionsettings-enabletoggle}

Gets or sets a value that indicates whether to enable the toggle selection behavior for row, cell and column.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:  window.gridData,
    allowSelection: true,   
    selectionSettings: {enableToggle: true }
});
</script>
{% endhighlight %}

### selectionSettings.selectionMode `enum`
{:#members:selectionsettings-selectionmode}

<ts name="ej.Grid.SelectionMode"/>

Gets or sets a value that indicates whether to add the default selection actions as a selection mode.See selectionMode

#### Default Value:
{:.param}
* ["row"]

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Row</td>
<td class="description">Selection is row basis.</td>
</tr>
<tr>
<td class="name">Cell</td>
<td class="description">Selection is cell basis.</td>
</tr>  
<tr>
<td class="name">Column</td>
<td class="description">Selection is column basis.</td>
</tr> 
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSelection: true,   
   selectionSettings: {selectionMode: ["row","cell","column"] }
});
</script>
{% endhighlight %}

### selectionType `enum`
{:#members:selectiontype}

<ts name="ej.Grid.SelectionType"/>

The row selection behavior of grid. Accepting types are "single" and "multiple".

#### Default Value:
{:.param}
* ej.Grid.SelectionType.Single

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Single</td>
<td class="description">Specifies the selection type as single.</td>
</tr>
<tr>
<td class="name">Multiple</td>
<td class="description">Specifies the selection type as multiple.</td>
</tr>  
</table>

#### Example
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   selectionType:"multiple"
});
</script> 
{% endhighlight %}

### scrollSettings `Object`
{:#members:scrollsettings}

Gets or sets an object that indicates whether to customize the scrolling behavior of the grid.

### scrollSettings.allowVirtualScrolling `Boolean`
{:#members:scrollsettings-allowvirtualscrolling}

This specify the grid to to view data that you require without buffering the entire load of a huge database

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{width:300,height:100,allowVirtualScrolling:true}
});
</script> 
{% endhighlight %}

### scrollSettings.enableTouchScroll `Boolean`
{:#members:scrollsettings-enabletouchscroll}

This specify the grid to enable/disable touch control for scrolling.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{ enableTouchScroll:true }
});
</script> 
{% endhighlight %}

### scrollSettings.frozenColumns `Number`
{:#members:scrollsettings-frozencolumns}

This specify the grid to freeze particular columns at the time of scrolling.

#### Default Value:
{:.param}
* 0

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowScrolling: true,               
    scrollSettings:{width:500,height:100,frozenColumns:2 }
});  
</script> 
{% endhighlight %}

### scrollSettings.frozenRows `Number`
{:#members:scrollsettings-frozenrows}

This specify the grid to freeze particular rows at the time of scrolling.

#### Default Value:
{:.param}
* 0

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    allowScrolling: true,               
    scrollSettings:{width:300,height:200,frozenRows:2 }
});
</script> 
{% endhighlight %}

### scrollSettings.height `Number`
{:#members:scrollsettings-height}

This specify the grid to show the vertical scroll bar, to scroll and view the grid contents.

#### Default Value:
{:.param}
* 0

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{ height:100 }
});
</script> 
{% endhighlight %}

### scrollSettings.virtualScrollMode `enum`
{:#members:scrollsettings-virtualscrollmode}

<ts name="ej.Grid.VirtualScrollMode"/>

This is used to define the mode of virtual scrolling in grid. See virtualScrollMode

#### Default Value:
{:.param}
* ej.Grid.VirtualScrollMode.Normal

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Normal</td>
<td class="description">virtual scroll mode is normal.</td>
</tr>
<tr>
<td class="name">Continuous</td>
<td class="description">virtual scroll mode is continuous.</td>
</tr>  
</table>

#### Example
{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
    dataSource: window.gridData,                     
    allowScrolling:true,
    scrollSettings:{ width:500 , height: 550 , allowVirtualScrolling:true, virtualScrollMode:ej.Grid.VirtualScrollMode.Normal }
});
</script>                          
{% endhighlight %}

### scrollSettings.width `Number`
{:#members:scrollsettings-width}

This specify the grid to show the horizontal scroll bar, to scroll and view the grid contents

#### Default Value:
{:.param}
* 250

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{ width:300 }
});
</script> 
{% endhighlight %}

### scrollSettings.scrollOneStepBy `Number`
{:#members:scrollsettings-scrollonestepby}
 
This specify the scroll down pixel of mouse wheel, to scroll mouse wheel and view the grid contents.

#### Default Value:
{:.param}
* 57

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowScrolling: true,
   scrollSettings:{ scrollOneStepBy:100 }
});
</script> 
{% endhighlight %}

### showColumnChooser `Boolean`
{:#members:showcolumnchooser}
Gets or sets a value that indicates whether to enable column chooser on grid. On enabling feature able to show/hide grid columns

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
            
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    showColumnChooser:true                      
});
</script>                 
{% endhighlight %}

### showStackedHeader `Boolean`
{:#members:showstackedheader}

Gets or sets a value that indicates stacked header should be shown on grid layout when the property &ldquo;stackedHeaderRows&rdquo; is set.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### showSummary `Boolean`
{:#members:showsummary}

Gets or sets a value that indicates summary rows should be shown on grid layout when the property &ldquo;summaryRows&rdquo; is set

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    dataSource:window.gridData,
    columns: [{ field: "OrderID"}, { field: "Freight" }, { field: "ShipCity" }],
    showSummary:true,
    summaryRows:[{ title: "sum", summaryColumns: [{summaryType:ej.Grid.SummaryType.Count,displayColumn:"Freight",dataMember:"Freight"}]}]       
});
</script>  
{% endhighlight %}

### sortSettings `Object`
{:#members:sortsettings}

Gets or sets a value that indicates whether to customize the sorting behavior of the grid.

### sortSettings.sortedColumns `Array`
{:#members:sortsettings-sortedcolumns}

Gets or sets a value that indicates whether to define the direction and field to sort the column.


### sortSettings.sortedColumns.direction `String`
{:#members:sortsettings-sortedcolumns-direction}

Gets or sets a value that indicates whether to define the direction to sort the column.

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>          
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field: "OrderID"},{field: "EmployeeID"}],
  sortSettings: {sortedColumns: [{field:"EmployeeID", direction:"descending"}] }                    
});
</script>  
{% endhighlight %}

### sortSettings.sortedColumns.field `String`
{:#members:sortsettings-sortedcolumns-field}

Gets or sets a value that indicates whether to define the field name of the column to be sort

#### Default Value:
{:.param}
* -

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div>          
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData,
  columns:[{field: "OrderID"},{field: "EmployeeID"}],
  sortSettings: {sortedColumns: [{field:"EmployeeID"}] }             
});
</script>  
{% endhighlight %}

### stackedHeaderRows `Array`
{:#members:stackedheaderrows}

Gets or sets an object that indicates to managing the collection of stacked header rows for the grid.

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### stackedHeaderRows.stackedHeaderColumns `Array`
{:#members:stackedheaderrows-stackedheadercolumns}

Gets or sets a value that indicates whether to add stacked header columns into the stacked header rows

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### stackedHeaderRows.stackedHeaderColumns.column `Object`
{:#members:stackedheaderrows-stackedheadercolumns-column}

Gets or sets a value that indicates the header text for the particular stacked header column.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowSorting:true,
   showStackedHeader:true,
   stackedHeaderRows:[{stackedHeaderColumns:[{headerText:"ID &amp; Freight",column:"CustomerID"}
         ,{headerText:"Frieght",column:["Freight","EmployeeID","OrderDate"]}
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
</script>
{% endhighlight %}

### stackedHeaderRows.stackedHeaderColumns.cssClass `String`
{:#members:stackedheaderrows-stackedheadercolumns-cssclass}

Gets or sets a value that indicates class to the corresponding stackedHeaderColumn.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div>       
<style class="temp">
.temp{
color:green;
}
</style>
<script>
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
</script> 
{% endhighlight %}

### stackedHeaderRows.stackedHeaderColumns.headerText `String`
{:#members:stackedheaderrows-stackedheadercolumns-headertext}

Gets or sets a value that indicates the header text for the particular stacked header column.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### stackedHeaderRows.stackedHeaderColumns.textAlign `String`
{:#members:stackedheaderrows-stackedheadercolumns-textalign}

Gets or sets a value that indicates the text alignment of the corresponding headerText.

#### Default Value:
{:.param}
* ej.TextAlign.Left

#### Example
{:.example}
{% highlight html %}  
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows `Array`
{:#members:summaryrows}

Gets or sets an object that indicates to managing the collection of summary rows for the grid.

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.showCaptionSummary `Boolean`
{:#members:summaryrows-showcaptionsummary}

Gets or sets a value that indicates whether to show the summary value within the group caption area for the corresponding summary column while grouping the column

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script>           
{% endhighlight %}

### summaryRows.showGroupSummary `Boolean`
{:#members:summaryrows-showgroupsummary}

Gets or sets a value that indicates whether to show the group summary value for the corresponding summary column while grouping a column

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
        showGroupSummary: true
     }]                                    
});
</script>           
{% endhighlight %}

### summaryRows.showTotalSummary `Boolean`
{:#members:summaryrows-showtotalsummary}

Gets or sets a value that indicates whether to show the total summary value the for the corresponding summary column. The summary row is added after the grid content.

#### Default Value:
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns `Array`
{:#members:summaryrows-summarycolumns}

Gets or sets a value that indicates whether to add summary columns into the summary rows.

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns.customSummaryValue `String`
{:#members:summaryrows-summarycolumns-customsummaryvalue}

Gets or sets a value that indicates the text displayed in the summary column as a value

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns.dataMember `String`
{:#members:summaryrows-summarycolumns-datamember}

This specifies summary column used to perform the summary calculation

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns.displayColumn `String`
{:#members:summaryrows-summarycolumns-displaycolumn}

Gets or sets a value that indicates to define the target column at which to display the summary.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns.format `String`
{:#members:summaryrows-summarycolumns-format}

Gets or sets a value that indicates the format for the text applied on the column

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns.prefix `String`
{:#members:summaryrows-summarycolumns-prefix}

Gets or sets a value that indicates the text displayed before the summary column value

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns.suffix `String`
{:#members:summaryrows-summarycolumns-suffix}

Gets or sets a value that indicates the text displayed after the summary column value

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns.summaryType `enum`
{:#members:summaryrows-summarycolumns-summarytype}

<ts name="ej.Grid.SummaryType"/>

Gets or sets a value that indicates the type of calculations to be performed for the corresponding summary column

#### Default Value:
{:.param}
* []

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Average</td>
<td class="description">Summary type is average.</td>
</tr>
<tr>
<td class="name">Minimum</td>
<td class="description">Summary type is minimum.</td>
</tr>  
<tr>
<td class="name">Maximum</td>
<td class="description">Summary type is maximum.</td>
</tr>  
<tr>
<td class="name">Count</td>
<td class="description">Summary type is count.</td>
</tr>  
<tr>
<td class="name">Sum</td>
<td class="description">Summary type is sum.</td>
</tr>  
<tr>
<td class="name">Custom</td>
<td class="description">Summary type is custom.</td>
</tr>  
<tr>
<td class="name">TrueCount</td>
<td class="description">Summary type is true count.</td>
</tr>  
<tr>
<td class="name">FalseCount</td>
<td class="description">Summary type is false count.</td>
</tr>  
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script> 
{% endhighlight %}

### summaryRows.summaryColumns.template `String`
{:#members:summaryRows-summaryColumns-template}

Gets or sets a value that indicates to add the template for the summary value of dataMember given.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script id="templateData" type="text/x-jsrender">
     Freight has Average of {{"{{"}}:summaryValue{{}}}} in  dollars
</script>
<script>
$("#Grid").ejGrid({
     dataSource: window.gridData,
     showSummary: true,
     summaryRows: [{ 
         title: "Average",
         summaryColumns: [{ 
             summaryType: ej.Grid.SummaryType.Average, 
             displayColumn: "Freight", 
             dataMember: "Freight",  
             template: "#templateData",
             format: "{0:C2}"
         }]
      }],
     columns: [{ field: "OrderID" },{ field: "EmployeeID" },{ field: "Freight", format: "{0:C}" }]
});
</script>
{% endhighlight %}


### summaryRows.title `String`
{:#members:summaryrows-title}

This specifies the grid to show the title for the summary rows.

#### Default Value:
{:.param}
* ""

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
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
</script>
{% endhighlight %}

### summaryRows.titleColumn `String`
{:#members:summaryrows-titleColumn}

This specifies the grid to show the title of summary row in the specified column.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
     dataSource:window.gridData,  
     showSummary: true,
     columns:[{field: "OrderID"},{field: "EmployeeID"},{field: "Freight"}],
     summaryRows: [{
        title: "Sum",
        titleColumn: "EmployeeID",
        summaryColumns: [{
           summaryType: ej.Grid.SummaryType.Sum,
           displayColumn: "Freight",
           dataMember: "Freight"
        }]
     }]                                    
});
</script>
{% endhighlight %}

### textWrapSettings `Object`
{:#members:textwrapsettings}

Gets or sets an object that indicates whether to auto wrap the grid header or content or both

### textWrapSettings.wrapMode `enum`
{:#members:textWrapSettings-wrapmode}

<ts name="ej.Grid.WrapMode"/>

This specifies the grid to apply the auto wrap for grid content or header or both.

#### Default Value:
{:.param}
* ej.Grid.WrapMode.Both

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Both</td>
<td class="description">Auto wrap is applied for both content and header.</td>
</tr>
<tr>
<td class="name">Content</td>
<td class="description">Auto wrap is applied only for content.</td>
</tr>  
<tr>
<td class="name">Header</td>
<td class="description">Auto wrap is applied only for header.</td>
</tr> 
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   allowTextWrap: true, 
   textWrapSettings:{ wrapMode: ej.Grid.WrapMode.Both }                
});
</script>
{% endhighlight %}

### toolbarSettings `Object`
{:#members:toolbarsettings}

Gets or sets an object that indicates whether to enable the toolbar in the grid and add toolbar items

### toolbarSettings.customToolbarItems `Array`
{:#members:toolbarsettings-customtoolbaritems}

Gets or sets a value that indicates whether to add custom toolbar items within the toolbar to perform any action in the grid

#### Default Value:
{:.param}
* []

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<style type="text/css" class="cssStyles">
  .Expand:before
  {
    content:"\e627";
  }
</style>
<script>
$("#Grid").ejGrid({
  dataSource:window.gridData, 
  toolbarSettings:{showToolbar:true,customToolbarItems:["Expand"]}
});
</script>
{% endhighlight %}

### toolbarSettings.showToolbar `Boolean`
{:#members:toolbarsettings-showtoolbar}

Gets or sets a value that indicates whether to enable toolbar in the grid.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource: window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowEditing: true },
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Edit] }
});
</script> 
{% endhighlight %}

### toolbarSettings.toolbarItems `Array`
{:#members:toolbarsettings-toolbaritems}

<ts name="ej.Grid.ToolBarItems"/>

Gets or sets a value that indicates whether to add the default editing actions as a toolbar items

#### Default Value:
{:.param}
* []

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Add</td>
<td class="description">Toolbar item is add.</td>
</tr>
<tr>
<td class="name">Edit</td>
<td class="description">Toolbar item is edit.</td>
</tr>  
<tr>
<td class="name">Delete</td>
<td class="description">Toolbar item is delete.</td>
</tr>  
<tr>
<td class="name">Update</td>
<td class="description">Toolbar item is update.</td>
</tr>  
<tr>
<td class="name">Cancel</td>
<td class="description">Toolbar item is cancel.</td>
</tr>  
<tr>
<td class="name">Search</td>
<td class="description">Toolbar item is search.</td>
</tr>  
<tr>
<td class="name">PdfExport</td>
<td class="description">Toolbar item is pdfExport.</td>
</tr>  
<tr>
<td class="name">PrintGrid</td>
<td class="description">Toolbar item is printGrid.</td>
</tr>  
<tr>
<td class="name">WordExport</td>
<td class="description">Toolbar item is wordExport.</td>
</tr>  
</table>

#### Example
{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   dataSource:window.gridData,
   columns:[{field: "OrderID", isPrimaryKey: true},{field: "EmployeeID"}],
   editSettings: { allowDeleting: true, allowEditing: true, allowAdding: true },
   toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] }
});
</script>
{% endhighlight %}

## Methods

### addIgnoreOnExport(propertyNames)
{:#methods:addignoreonexport}

Adds a grid model property which is to be ignored upon exporting.

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
<td class="name">propertyNames</td>
<td class="type"><span class="param-type">Array</span></td>
<td class="description last">Pass the array of parameters which need to be ignored on exporting </td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void


####Example

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a request to ignore the filterSettings property upon exporting
gridObj.addIgnoreOnExport("filterSettings"); 
</script>
{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a request to ignore the filterSettings property upon exporting
$("#Grid").ejGrid("addIgnoreOnExport","filterSettings");       
</script>
{% endhighlight %}

### addRecord()
{:#methods:addrecord}

Add a new record in grid control when allowAdding is set as true.

#### Returns:
{:#methods:returns:}

Void

####Example

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an add new record request to the grid
gridObj.addRecord(); 
</script>
{% endhighlight %}


{% highlight html %}
 
<script>
// add new record to the grid
$("#Grid").ejGrid("addRecord");       
</script>
{% endhighlight %}

### addRecord(data,\[serverChange\])
{:#methods:addrecord}

Add a new record in grid control when allowAdding is set as true.

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
<td class="name">data</td>
<td class="type"><span class="param-type">Array</span></td>
<td class="description last">Pass the array of added Records</td>
</tr>
<tr>
<td class="name">serverChange</td>
<td class="type"><span class="param-type">Array</span></td>
<td class="description last"><span class="optional">optional</span>If we pass serverChange as true, send post to server side for server action.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an add new record request to the grid
gridObj.addRecord({"OrderID":12333});
</script>
{% endhighlight %}


{% highlight html %}
 
<script>
// add new record to the grid
$("#Grid").ejGrid("addRecord",{OrderID:12333})       
</script>
{% endhighlight %}



### batchCancel()
{:#methods:batchcancel}

Cancel the modified changes in grid control when edit mode is "batch".

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.batchCancel();
// Cancel added, edited, and deleted changes made in grid
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Cancel added, edited, and deleted changes made in grid
$("#Grid").ejGrid("batchCancel");
</script>
{% endhighlight %}


### batchSave()
{:#methods:batchsave}

Save the modified changes to data source in grid control when edit mode is "batch".

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Save added, edited, and deleted changes to source of data
gridObj.batchSave(); 
</script>
{% endhighlight %}


{% highlight html %}
 
<script>
// Save added, edited, and deleted changes to source of data
$("#Grid").ejGrid("batchSave");
</script>
{% endhighlight %}



### cancelEdit()
{:#methods:canceledit}

Send a cancel request in grid.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a cancel request to the grid
gridObj.cancelEdit(); 
</script>
{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a cancel request to the grid
$("#Grid").ejGrid("cancelEdit");        
</script>
{% endhighlight %}



### cancelEditCell()
{:#methods:canceleditcell}

Send a cancel request to the edited cell in grid.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a cancel request to the edited cell in  grid
gridObj.cancelEditCell();   
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a cancel request to the edited cell in grid
$("#Grid").ejGrid("cancelEditCell");        
</script>{% endhighlight %}




### clearCellSelection()
{:#methods:clearcellselection}

It is used to clear all the cell selection.

#### Returns:
{:#methods:returns:}

Boolean

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearCellSelection();  // clears all of the cell selection
</script>
{% endhighlight %}


{% highlight html %}
 
<script>         
// clears all of the cell selection
$("#Grid").ejGrid("clearCellSelection");        
</script>{% endhighlight %}

### clearCellSelection(rowIndex,columnIndex)
{:#methods:clearcellselection}

It is used to clear specified cell selection based on the rowIndex and columnIndex provided.

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
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to pass the row index of the cell</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to pass the column index of the cell.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Boolean

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearCellSelection(1,2);  // clears specified the cell selection
</script>
{% endhighlight %}


{% highlight html %}
 
<script>         
// clears all of the cell selection
$("#Grid").ejGrid("clearCellSelection",1,2);        
</script>{% endhighlight %}


### clearColumnSelection(\[index\])
{:#methods:clearcolumnselection}


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
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last"><span class="optional">optional</span> If index of the column is specified then it will remove the selection from the particular column else it will clears all of the column selection</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Boolean

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearColumnSelection(2);  // Removes the selection based on the column index
gridObj.clearColumnSelection();  // clears all of the column selection
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Removes the selection based on the column index
$("#Grid").ejGrid("clearColumnSelection", 2);   
// clears all of the column selection
$("#Grid").ejGrid("clearColumnSelection");        
</script>

{% endhighlight %}



### clearFiltering(field)
{:#methods:clearfiltering}

It is used to clear all the filtering done.

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
<td class="name">field</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"> If field of the column is specified then it will clear the  particular filtering column</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearFiltering("EmployeeID"); //clears the filtering based on the fieldName passed
gridObj.clearFiltering();  // clears all the filtering
</script>{% endhighlight %}


{% highlight html %}
 
<script>         
$("#Grid").ejGrid("clearFiltering","EmployeeID");// clears the filtering based on the fieldName passed
$("#Grid").ejGrid("clearFiltering"); // clears all the filtering
</script>{% endhighlight %}

### clearSearching()
{:#methods:clearsearching}

Clear the searching from the grid

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Clears the searching from the grid
gridObj.clearSearching(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Clears the searching from the grid
$("#Grid").ejGrid("clearSearching");        
</script>{% endhighlight %}

### clearSelection(\[index\])
{:#methods:clearselection}


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
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last"><span class="optional">optional</span> If index of the row is specified then it will remove the selection from the particular row else it will clears all of the row selection</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Boolean


####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearSelection(2);  // Removes the selection based on the row index
gridObj.clearSelection();  // clears all of the row selection
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Removes the selection based on the row index
$("#Grid").ejGrid("clearSelection", 2);   
// clears all of the row selection
$("#Grid").ejGrid("clearSelection");        
</script>{% endhighlight %}


### clearSorting()
{:#methods:clearsorting}

Clear the sorting from columns in the grid

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Clears the sorting from columns in the grid
gridObj.clearSorting(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Clears the sorting from columns in the grid
$("#Grid").ejGrid("clearSorting");        
</script>{% endhighlight %}


### collapseAll()
{:#methods:collapseall}

Collapse all the group caption rows in grid

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Collapse all the group caption rows
gridObj.collapseAll(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Collapse all the group caption rows
$("#Grid").ejGrid("collapseAll");        
</script>{% endhighlight %}


### collapseGroupDropArea()
{:#methods:collapsegroupdroparea}

Collapse the group drop area in grid

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Collapse the group drop area of the grid
gridObj.collapseGroupDropArea(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Collapse the group drop area of the grid
$("#Grid").ejGrid("collapseGroupDropArea");        
</script>{% endhighlight %}



### columns(columnDetails, \[action\])
{:#methods:columns}

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
<td class="name">columnDetails</td>
<td class="type"><span class="param-type">array/string</span></td>
<td class="description last">Pass array of columns or string of field name to add/remove the column in grid</td>
</tr>
<tr>
<td class="name">action</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"><span class="optional">optional</span> Pass add/remove action to be performed. By default "add" action will perform</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void


####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// remove grid column
gridObj.columns("OrderID", "remove");
// Add new column into grid or modified already existing column in the grid.
gridObj.columns("CustomerID", "add"); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// remove grid column
$("#Grid").ejGrid("columns","OrderID", "remove");   
// Add new column into grid or modified already existing column in the grid.                    
$("#Grid").ejGrid("columns","CustomerID", "add");                       
</script>{% endhighlight %}



### dataSource(datasource,\[templateRefresh\])
{:#methods:datasource}

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
<td class="name">datasource</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass new data source to the grid</td>
</tr>
<tr>
<td class="name">templateRefresh</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last"><span class="optional">optional</span> When templateRefresh is set true, both header and contents get refreshed</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void


####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Refreshes the grid data source
gridObj.dataSource(data); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Refreshes the grid data source
$("#Grid").ejGrid("dataSource", data);        
</script>{% endhighlight %}


### deleteRecord(fieldName, data)
{:#methods:deleterecord}

Delete a record in grid control when allowDeleting is set as true

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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the primary key field Name of the column</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass the JSON data of record need to be delete.</td>
</tr>
</tbody>
</table>


#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a delete record request to the grid
gridObj.deleteRecord("OrderID", { OrderID: 10249, EmployeeID: 3 }); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a delete record request to the grid
$("#Grid").ejGrid("deleteRecord", "OrderID", { OrderID: 10249, EmployeeID: 3 });        
</script>{% endhighlight %}


### destroy()
{:#methods:destroy}

Destroy the grid widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
var gridObj = $("#Grid").data("ejGrid");
gridObj.destroy(); // destroy the Grid
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// destroy the Grid
$("#Grid").ejGrid("destroy");        
</script>{% endhighlight %}

### editCell(index, fieldName)
{:#methods:editcell}

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
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass row index to edit particular cell</td>
</tr>
<tr>
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column to perform batch edit</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void


####Example
{:.example}


{% highlight html %}
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Edit particular cell based on row index and column field name
gridObj.editCell(2, "OrderID"); 
</script>{% endhighlight %}


{% highlight html %}
<script>
// Edit particular cell based on row index and column field name
$("#Grid").ejGrid("editCell", 2, "OrderID");
</script>{% endhighlight %}


### endEdit()
{:#methods:endedit}

Send a save request in grid.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a save request to the grid
gridObj.endEdit(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a save request to the grid
$("#Grid").ejGrid("endEdit");        
</script>{% endhighlight %}


### expandAll()
{:#methods:expandall}

Expand all the group caption rows in grid.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Expand all the group caption rows
gridObj.expandAll(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Expand all the group caption rows
$("#Grid").ejGrid("expandAll");        
</script>{% endhighlight %}


### expandCollapse($target)
{:#methods:expandcollapse}


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
<td class="name">$target</td>
<td class="type"><span class="param-type">jQuery</span></td>
<td class="description last">Pass the target object to expand/collapse the row based on its row state</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Element


####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Expands or collapses the row based on the row state
gridObj.expandCollapse($("tr td.recordplusexpand > div").first());  
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Expands or collapses the row based on the row state
$("#Grid").ejGrid("expandCollapse", $("tr td.recordplusexpand > div").first());        
</script>{% endhighlight %}


### expandGroupDropArea()
{:#methods:expandgroupdroparea}

Expand the group drop area in grid.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Expands the group drop area of the grid
gridObj.expandGroupDropArea(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Expands the group drop area of the grid
$("#Grid").ejGrid("expandGroupDropArea");        
</script>{% endhighlight %}

### export(action, \[serverEvent\], \[multipleExport\], \[gridIds\])
{:#methods:export}

Export the grid content to excel, word or PDF document.

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
<td class="name">action</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the controller action name corresponding to exporting</td>
</tr>
<tr>
<td class="name">serverEvent</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"><span class="optional">optional</span>ASP server event name corresponding to exporting</td>
</tr>
<tr>
<td class="name">multipleExport</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last"><span class="optional">optional</span>Pass the multiple exporting value as true/false</td>
</tr>
<tr>
<td class="name">gridIds</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last"><span class="optional">optional</span>Pass the array of the gridIds to be filtered</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an exporting request
gridObj.export("/api/GridExport/ExcelExport"); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends an exporting request
$("#Grid").ejGrid("export","/api/GridExport/ExcelExport");        
</script>{% endhighlight %}

### export(action, \[serverEvent\], \[multipleExport\])
{:#methods:export}

Export the grid content to excel, word or PDF document.

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
<td class="name">action</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the controller action name corresponding to exporting</td>
</tr>
<tr>
<td class="name">serverEvent</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"><span class="optional">optional</span>ASP server event name corresponding to exporting</td>
</tr>
<tr>
<td class="name">multipleExport</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last"><span class="optional">optional</span>Pass the multiple exporting value as true/false</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an exporting request
gridObj.export("/api/GridExport/ExcelExport"); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends an exporting request
$("#Grid").ejGrid("export","/api/GridExport/ExcelExport");        
</script>{% endhighlight %}

### filterColumn(fieldName, filterOperator, filterValue, predicate, \[matchcase\],\[actualFilterValue\])
{:#methods:filtercolumn}


Send a filtering request to filter one column in grid.

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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass the field name of the column</td>
</tr>
<tr>
<td class="name">filterOperator</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">string/integer/dateTime operator</td>
</tr>
<tr>
<td class="name">filterValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the value to be filtered in a column</td>
</tr>
<tr>
<td class="name">predicate</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the predicate as and/or</td>
</tr>
<tr>
<td class="name">matchcase</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last"><span class="optional">optional</span> Pass the match case value as true/false</td>
</tr>
<tr>
<td class="name">actualFilterValue</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last"><span class="optional">optional</span>actualFilterValue denote the filter object of current filtered columns.
Pass the value to filtered in a column</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a filtering request to the grid
gridObj.filterColumn("OrderID","equal","10248","and", true);
</script>{% endhighlight %}


{% highlight html %}
<script>
// Sends a filtering request to the grid
$("#Grid").ejGrid("filterColumn","OrderID","equal","10248","and", true);
</script>{% endhighlight %}


### filterColumn(filterCollection)
{:#methods:filtercolumn}


Send a filtering request to filter single or multiple column in grid.

<table class="param">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">filterQueries</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass array of filterColumn query for performing filter operation</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a filtering request to the grid
gridObj.filterColumn([{field:"OrderID",operator:"lessthan",value:"10266",predicate:"and", matchcase:true},{field:"EmployeeID",operator:"equal",value:2,predicate:"and", matchcase:true}]);

</script>{% endhighlight %}


{% highlight html %}
<script>
// Sends a filtering request to the grid
$("#Grid").ejGrid("filterColumn",[{field:"OrderID",operator:"lessthan",value:"10266",predicate:"and", matchcase:true},{field:"EmployeeID",operator:"equal",value:2,predicate:"and", matchcase:true}]);
</script>{% endhighlight %}


### getBatchChanges()
{:#methods:getbatchchanges}

Get the batch changes of edit, delete and add operations of grid.

#### Returns:
{:#methods:returns:}

Object

#### Example
{:.example}


{% highlight html %}
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the edit, delete, and add changes of a grid
gridObj.getBatchChanges(); 
</script>{% endhighlight %}


{% highlight html %}
<script>
// Gets the edit, delete, and add changes of a grid
$("#Grid").ejGrid("getBatchChanges");        
</script>{% endhighlight %}


### getBrowserDetails()
{:#methods:getbrowserdetails}

Get the browser details

#### Returns:
{:#methods:returns:}

Object

####Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the browser details of the application being run
gridObj.getBrowserDetails(); 
</script>{% endhighlight %}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Gets the browser details of the application being run
$("#Grid").ejGrid("getBrowserDetails");        
</script>{% endhighlight %}


### getColumnByField(fieldName)
{:#methods:getcolumnbyfield}


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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column to get the corresponding column object</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Object

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column details based on the given field name
gridObj.getColumnByField("OrderID");
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the column details based on the given field name
$("#Grid").ejGrid("getColumnByField", "OrderID");        
</script>{% endhighlight %} 

### getColumnByHeaderText(headerText)
{:#methods:getcolumnbyheadertext}

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
<td class="name">headerText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the header text of the column to get the corresponding column object</td>
</tr>
</tbody>
</table>


#### Returns:
{:#methods:returns:}

Object


#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column details based on the given headerText
gridObj.getColumnByHeaderText("Order ID"); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the column details based on the given headerText
$("#Grid").ejGrid("getColumnByHeaderText", "Order ID");        
</script>{% endhighlight %}


### getColumnByIndex(columnIndex)
{:#methods:getcolumnbyindex}

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
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the index of the column to get the corresponding column object</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Object

#### Example
{:.example}

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column details based on the given column index
gridObj.getColumnByIndex(1); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the column details based on the given column index
$("#Grid").ejGrid("getColumnByIndex", 1);        
</script>{% endhighlight %}

### getColumnFieldNames()
{:#methods:getcolumnfieldnames}

Get the list of field names from column collection in grid.

#### Returns:
{:#methods:returns:}

Array

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column field names based on the given index
gridObj.getColumnFieldNames(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the column field names based on the given index
$("#Grid").ejGrid("getColumnFieldNames");        
</script>{% endhighlight %}

### getColumnIndexByField(fieldName)
{:#methods:getcolumnindexbyfield}


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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column to get the corresponding column index</td>
</tr>
</tbody>
</table>


#### Returns:
{:#methods:returns:}

Number


####Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column index based on the given field name
gridObj.getColumnIndexByField("OrderID"); 
</script>{% endhighlight %}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Gets the column index based on the given field name
$("#Grid").ejGrid("getColumnIndexByField", "OrderID");        
</script>{% endhighlight %}


### getContent()
{:#methods:getcontent}

Get the content div element of grid.

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets content of grid control
gridObj.getContent(); 
</script>
{% endhighlight %}


{% highlight html %}
 
<script>
// Gets content of grid control
$("#Grid").ejGrid("getContent");        
</script>
{% endhighlight %}


### getContentTable()
{:#methods:getcontenttable}

Get the content table element of grid

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets content table of grid control
gridObj.getContentTable();
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets content table of grid control
$("#Grid").ejGrid("getContentTable");        
</script>{% endhighlight %}

### getCurrentEditCellData()
{:#methods:getcurrenteditcelldata}

Get the data of currently edited cell value in "batch" edit mode

#### Returns:
{:#methods:returns:}

Object

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Get data of currently edited cell value
gridObj.getCurrentEditCellData(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Get data of currently edited cell value
$("#Grid").ejGrid("getCurrentEditCellData");        
</script>{% endhighlight %}


### getCurrentIndex()
{:#methods:getcurrentindex}

Get the current page index in grid pager.

#### Returns:
{:#methods:returns:}

Number


####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the current page index in grid
gridObj.getCurrentIndex();  
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the current page index in grid
$("#Grid").ejGrid("getCurrentIndex");   
</script>{% endhighlight %}


### getCurrentViewData()
{:#methods:getcurrentviewdata}

Get the current page data source of grid.

#### Returns:
{:#methods:returns:}

Array

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets current view data of grid control
gridObj.getCurrentViewData(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets current view data of grid control
$("#Grid").ejGrid("getCurrentViewData");        
</script>{% endhighlight %}

### getFieldNameByHeaderText(headerText)
{:#methods:getfieldnamebyheadertext}

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
<td class="name">headerText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass header text of the column to get its corresponding field name</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

String

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the column field name from the given headerText
gridObj.getFieldNameByHeaderText("Order ID"); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the column field name from the given headerText
$("#Grid").ejGrid("getFieldNameByHeaderText", "Order ID");
</script>{% endhighlight %}


### getFilterBar()
{:#methods:getfilterbar}

Get the filter bar of grid

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets filter bar of grid control
gridObj.getFilterBar(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets filter bar of grid control
$("#Grid").ejGrid("getFilterBar");        
</script>{% endhighlight %}


### getFilteredRecords()
{:#methods:getfilteredrecords}

Get the records filtered or searched in Grid

#### Returns:
{:#methods:returns:}

Array

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the filtered or searched records in Grid
gridObj.getFilteredRecords();  
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the filtered or searched records in Grid
$("#Grid").ejGrid("getFilteredRecords");   
</script>{% endhighlight %}

### getFooterContent()
{:#methods:getfootercontent}

Get the footer content of grid.

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid footer content of grid control
gridObj.getFooterContent(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets grid footer content of grid control
$("#Grid").ejGrid("getFooterContent");        
</script>{% endhighlight %}


### getFooterTable()
{:#methods:getfootertable}

Get the footer table element of grid.

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid footer table of grid control
gridObj.getFooterTable(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets grid footer table of grid control
$("#Grid").ejGrid("getFooterTable");        
</script>{% endhighlight %}

### getHeaderContent()
{:#methods:getheadercontent}

Get the header content div element of grid.

#### Returns:
{:#methods:returns:}

Element

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid header content of grid control
gridObj.getHeaderContent(); 
</script>
{% endhighlight %}


{% highlight html %}
 
<script>
// Gets grid header content of grid control
$("#Grid").ejGrid("getHeaderContent");        
</script>
{% endhighlight %}


### getHeaderTable()
{:#methods:getheadertable}

Get the header table element of grid

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.getHeaderTable(); 
// Gets header table of grid control
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets header table of grid control
$("#Grid").ejGrid("getHeaderTable");        
</script>{% endhighlight %}


### getHeaderTextByFieldName(field)
{:#methods:getheadertextbyfieldname}

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
<td class="name">field</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass field name of the column to get its corresponding header text</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

String

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.getHeaderTextByFieldName("OrderID"); // Gets the column header text from the given field name
</script>{% endhighlight %}

{% highlight html %}
 
<script>
// Gets the column header text from the given field name
$("#Grid").ejGrid("getHeaderTextByFieldName", "OrderID");
</script>{% endhighlight %}


### getHiddenColumnNames()
{:#methods:gethiddencolumnnames}

Get the names of all the hidden column collections in grid.

#### Returns:
{:#methods:returns:}

Array

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets names of all the hidden column collections
gridObj.getHiddenColumnNames(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets names of all the hidden column collections
$("#Grid").ejGrid("getHiddenColumnNames");        
</script>{% endhighlight %}


### getIndexByRow($tr)
{:#methods:getindexbyrow}


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
<td class="name">$tr</td>
<td class="type"><span class="param-type">jQuery</span></td>
<td class="description last">Pass the tr element in grid content to get its row index</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Number


####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the row index based on the given row
gridObj.getIndexByRow($(".gridcontent tr").first()); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the row index based on the given row
$("#Grid").ejGrid("getIndexByRow", $(".gridcontent tr").first());        
</script>{% endhighlight %}


### getPager()
{:#methods:getpager}

Get the pager of grid.

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid pager of grid control
gridObj.getPager(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets grid pager of grid control
$("#Grid").ejGrid("getPager");        
</script>{% endhighlight %}


### getPrimaryKeyFieldNames()
{:#methods:getprimarykeyfieldnames}

Get the names of primary key columns in Grid

#### Returns:
{:#methods:returns:}

Array


####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the names of primary key columns
gridObj.getPrimaryKeyFieldNames(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the names of primary key columns
$("#Grid").ejGrid("getPrimaryKeyFieldNames");        
</script>{% endhighlight %}


### getRowByIndex(from, to)
{:#methods:getrowbyindex}


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
<td class="name">from</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the from index from which the rows to be returned</td>
</tr>
<tr>
<td class="name">to</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the to index to which the rows to be returned</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the rows from the specified row index 
gridObj.getRowByIndex(3, 6);  
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the rows from the specified row index
$("#Grid").ejGrid("getRowByIndex", 3, 6);   
</script>{% endhighlight %}


### getRowHeight()
{:#methods:getrowheight}

Get the row height of grid.

#### Returns:
{:#methods:returns:}

Number

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the row height of the grid
gridObj.getRowHeight();  
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the row height of the grid
$("#Grid").ejGrid("getRowHeight");   
</script>{% endhighlight %}


### getRows()
{:#methods:getrows}

Get the rows(tr element)of grid which is displayed in the current page.

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets grid rows of grid control
gridObj.getRows(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets grid rows of grid control
$("#Grid").ejGrid("getRows");        
</script>{% endhighlight %}


### getScrollObject()
{:#methods:getscrollobject}

Get the scroller object of grid.


#### Returns:
{:#methods:returns:}

Object

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets scroll object of grid control
gridObj.getScrollObject(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets scroll object of grid control
$("#Grid").ejGrid("getScrollObject");        
</script>{% endhighlight %}


### getSelectedRecords()
{:#methods:getselectedrecords}

Get the selected records details in grid.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the selected row list
gridObj.getSelectedRecords();
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the selected row list
$("#Grid").ejGrid("getSelectedRecords");        
</script>{% endhighlight %}


### getVisibleColumnNames()
{:#methods:getvisiblecolumnnames}

Get the names of all the visible column collections in grid

#### Returns:
{:#methods:returns:}

Array

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Gets the names of all the visible column collections
gridObj.getVisibleColumnNames(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Gets the names of all the visible column collections
$("#Grid").ejGrid("getVisibleColumnNames");        
</script>{% endhighlight %}

### gotoPage(pageIndex)
{:#methods:gotopage}

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
<td class="name">pageIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the page index to perform paging at specified page index</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a paging request to the grid with specified page index
gridObj.gotoPage(3);
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a paging request to the grid with specified page index
$("#Grid").ejGrid("gotoPage", 3);        
</script>{% endhighlight %}


### groupColumn(fieldName)
{:#methods:groupcolumn}

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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field Name of the column to be grouped in grid control</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a group column request to the grid
gridObj.groupColumn("OrderID"); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a group column request to the grid
$("#Grid").ejGrid("groupColumn", "OrderID");        
</script>{% endhighlight %}

### hideColumns(headerText)
{:#methods:hidecolumns}

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
<td class="name">headerText</td>
<td class="type"><span class="param-type">array/string</span></td>
<td class="description last">you can pass either array of header text of various columns or a header text of a column to hide</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.hideColumns("Order ID"); // Hides column based on the given header text of the column
gridObj.hideColumns(["Order ID", "Customer ID"]); // Hide columns based on the array of header text of the columns given
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Hide column based on the given header text of the column
$("#Grid").ejGrid("hideColumns", "Order ID"); 
// Hide columns based on the array of header text of the columns given
$("#Grid").ejGrid("hideColumns", ["Order ID", "Customer ID"]);                  
</script>{% endhighlight %}


### print()
{:#methods:print}

Print the grid control

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// It prints the grid.
gridObj.print(); 
</script>{% endhighlight %}


{% highlight html %}
 
<div id="Grid"></div&amp;dgt; 
<script>
// It prints the grid.
$("#Grid").ejGrid("print");        
</script>{% endhighlight %}


### refreshBatchEditChanges()
{:#methods:refreshbatcheditchanges}

It is used to refresh and reset the changes made in "batch" edit mode

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.refreshBatchEditChanges(); 
// It is used to refresh and reset the changes made in batch edit mode
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// It is used to refresh and reset the changes made in batch edit mode
$("#Grid").ejGrid("refreshBatchEditChanges");
</script>{% endhighlight %}



### refreshContent(\[templateRefresh\])
{:#methods:refreshcontent}


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
<td class="name">templateRefresh</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last"><span class="optional">optional</span> When templateRefresh is set true, template and grid contents both are refreshed in grid else only grid content is refreshed</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void


####Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.refreshContent(); // Refreshes the grid contents only
gridObj.refreshContent(true); // Refreshes the template and grid contents
</script>{% endhighlight %}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Refreshes the grid contents only
$("#Grid").ejGrid("refreshContent");        
// Refreshes the template and grid contents
$("#Grid").ejGrid("refreshContent", true);        
</script>{% endhighlight %}


### refreshTemplate()
{:#methods:refreshtemplate}

Refresh the template of the grid

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Refreshes the template of the grid control
gridObj.refreshTemplate(); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Refreshes the template of the grid control.
$("#Grid").ejGrid("refreshTemplate");        
</script>{% endhighlight %}


### refreshToolbar()
{:#methods:refreshtoolbar}

Refresh the toolbar items in grid.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Refreshes the toolbar items state
gridObj.refreshToolbar(); 
</script>{% endhighlight %}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Refreshes the toolbar items state
$("#Grid").ejGrid("refreshToolbar");        
</script>{% endhighlight %}

### removeSortedColumns(fieldName)
{:#methods:removesortedcolumns}

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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">array/string</span></td>
<td class="description last">Pass array of field names of the columns to remove a collection of sorted columns or pass a string of field name to remove a column from sorted column collections</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Removes a column from sorted column collections
gridObj.removeSortedColumns("OrderID"); 
// Removes specified collection of columns from sorted column collections
gridObj.removeSortedColumns(["CustomerID", "ShipCity"]); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Removes a column from sorted column collections
$("#Grid").ejGrid("removeSortedColumns", "OrderID");        
// Removes specified collection of columns from sorted column collections
$("#Grid").ejGrid("removeSortedColumns", ["CustomerID", "ShipCity"]);        
</script>{% endhighlight %}


### render()
{:#methods:render}


Creates a grid control

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// It renders the grid.
gridObj.render(); 
</script>{% endhighlight %}


{% highlight html %}
 
<div id="Grid"></div&amp;dgt; 
<script>
// It renders the grid.
$("#Grid").ejGrid("render");        
</script>{% endhighlight %}


### reorderColumns(fromFieldName, toFieldName)
{:#methods:reordercolumns}

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
<td class="name">fromFieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the from field name of the column needs to be changed</td>
</tr>
<tr>
<td class="name">toFieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the to field name of the column needs to be changed</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Reorders the column based on the given index
gridObj.reorderColumns("OrderID", "CustomerID"); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Reorders the column based on the given index
$("#Grid").ejGrid("reorderColumns", "OrderID", "CustomerID");
</script>{% endhighlight %}


### resetModelCollections()
{:#methods:resetmodelcollections}

Reset the model collections like pageSettings, groupSettings, filterSettings, sortSettings and summaryRows.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Reset model collections
gridObj.resetModelCollections(); 
</script>{% endhighlight %}

{% highlight html %}
 
<script>
// Reset model collections
$("#Grid").ejGrid("resetModelCollections");
</script>{% endhighlight %}

### resizeColumns(column,width)
{:#methods:resizecolumns}

Resize the columns by giving column name and width for the corresponding one.

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
<td class="name">column</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the column name that needs to be changed</td>
</tr>
<tr>
<td class="name">width</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the width to resize the particular columns</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// ResizeColumns
gridObj.resizeColumns("OrderID",width); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// ResizeColumns
$("#Grid").ejGrid("resizeColumns","OrderID",width);
</script>{% endhighlight %}


### rowHeightRefresh()
{:#methods:rowheightrefresh}

Resolves row height issue when unbound column is used with FrozenColumn

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.rowHeightRefresh(); // Resolves row height issue
</script>{% endhighlight %}


{% highlight html %}
 
<div id="Grid"></div> 
<script>         
// Resolves row height issue
$("#Grid").ejGrid("rowHeightRefresh");   
</script>{% endhighlight %}


### saveCell()
{:#methods:savecell}

Save the particular edited cell in grid.

#### Returns:
{:#methods:returns:}

Boolean

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Save the edited cell
gridObj.saveCell(); 
</script>{% endhighlight %}


{% highlight html %}

<script>

// Save the edited cell
$("#Grid").ejGrid("saveCell);
</script>{% endhighlight %}

### saveCell(preventSaveEvent)
{:#methods:savecell}

We can prevent the client side cellSave event triggering by passing the preventSaveEvent argument as true.

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
<td class="name">preventSaveEvent</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last"><span class="optional">optional</span>If we pass preventSaveEvent as true, it prevents the client side cellSave event triggering </td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Prevent save the edited cell
gridObj.saveCell(true); 
</script>{% endhighlight %}


{% highlight html %}
<script>
// Prevent save the edited cell
$("#Grid").ejGrid("saveCell",true);
</script>{% endhighlight %}



###  setDimension(height, width)
{:#methods:setdimension}
 
Set dimension for grid with corresponding to grid parent.


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
<td class="name">height</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the height of the grid container</td>
</tr>
<tr>
<td class="name">width</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the width of the grid container</td>
</tr>
</tbody>
</table>


#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}

<pre class="prettyprint">
<code>&lt;script&gt;
// Create grid object.
 var gridObj = $("#Grid").data("ejGrid");
   gridObj.setDimension(300,400); // Set grid dimension
  &lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>
  &lt;script&gt;
 //Set grid dimension based on providing height and width
 &lt;/script&gt;</code>
</pre>

### setWidthToColumns()
{:#methods:setwidthtocolumns}

Send a request to grid to refresh the width set to columns

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a request to the grid to refresh columns width
gridObj.setWidthToColumns(); 
</script>
{% endhighlight %}


{% highlight html %}
<script>
// Sends a request to the grid to refresh columns width
$("#Grid").ejGrid("setWidthToColumns");        
</script>{% endhighlight %}

### search(searchString)
{:#methods:search}

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
<td class="name">searchString</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the string to search in Grid records</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a search request to the grid
gridObj.search("France"); 
</script>{% endhighlight %}


{% highlight html %}
<script>
// Sends a search request to the grid
$("#Grid").ejGrid("search", "France");        
</script>{% endhighlight %}


### selectCells(rowCellIndexes)
{:#methods:selectcells}

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
<td class="name">rowCellIndexes</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">It is used to set the starting index of row and indexes of cells for that corresponding row for selecting cells.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects cells based on the given index
gridObj.selectCells([[1, [4, 3, 2]]]); 
</script>{% endhighlight %}

{% highlight html %}
 
<script>
// Selects cells based on the given index
$("#Grid").ejGrid("selectCells", [[1, [4, 3, 2]]]);
</script>{% endhighlight %}


### selectColumns(fromIndex)
{:#methods:selectcolumns}


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
<td class="name">fromIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to set the starting index of column for selecting columns.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects columns based on the given index
gridObj.selectColumns(1,4); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Selects columns based on the given index
$("#Grid").ejGrid("selectColumns", 1, 4);
</script>{% endhighlight %}

### selectColumns(columnIndex,\[toIndex\])
{:#methods:selectcolumns}

Select the specified columns in grid based on Index provided.

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
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to set the starting index of column for selecting columns.</td>
</tr>
<tr>
<td class="name">toIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last"><span class="optional">optional</span>It is used to set the ending index of column for selecting columns.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Boolean

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects columns based on the given index
gridObj.selectColumns(1,4); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Selects columns based on the given index
$("#Grid").ejGrid("selectColumns", 1, 4);
</script>{% endhighlight %}

### selectRows(fromIndex, toIndex)
{:#methods:selectrows}

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
<td class="name">fromIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to set the starting index of row for selecting rows.</td>
</tr>
<tr>
<td class="name">toIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to set the ending index of row for selecting rows.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects rows based on the given index
gridObj.selectRows(1, 4); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Selects rows based on the given index
$("#Grid").ejGrid("selectRows", 1, 4);
</script>{% endhighlight %}

### selectRows(from,to,\[target\])
{:#methods:selectrows}

Select specified rows in grid based on Index provided.

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
<td class="name">from</td>
<td class="type"><span class="param-type">array/number</span></td>
<td class="description last">It is used to set the starting index of row for selecting rows.</td>
</tr>
<tr>
<td class="name">to</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last"><span class="optional">optional</span>It is used to set the ending index of row for selecting rows.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last"><span class="optional">optional</span>Target element which is clicked.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects rows based on the given index
gridObj.selectRows(1, 4); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Selects rows based on the given index
$("#Grid").ejGrid("selectRows", 1, 4);
</script>{% endhighlight %}


### selectRows(rowIndexes)
{:#methods:selectRows}

Select rows in grid.

<table class="param">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIndexes</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass array of rowIndexes for selecting rows</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Selects rows based on the given array of indexes
gridObj.selectRows([1,3,5,7]);

</script>{% endhighlight %}


{% highlight html %}
<script>
// Selects rows based on the given array of indexes
$("#Grid").ejGrid("selectRows",[{1,3,5,7}]);
</script>{% endhighlight %}


### setCellText()
{:#methods:setcelltext}

Used to update a particular cell value.

N> It will work only for Local Data.This method applicable for all editMode's except batch edit mode.

#### setCellText(rowIndex, cellIndex, value)
{:#methods:setcelltext}

Used to update a particular cell value based on specified rowIndex and cellIndex values.

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
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">string/number</span></td>
<td class="description last">It is used to set the index of row.</td>
</tr>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">string/number</span></td>
<td class="description last">It is used to set the index of cell.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string/number</span></td>
<td class="description last">It is used to set the value for the cell based on specified row and cell Index.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}

{% highlight html %}

<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// update a particular cell value
gridObj.setCellText(0, 1, "GREYER");
</script>{% endhighlight %}

{% highlight html %}

<script>
// update a particular cell value
$("#Grid").ejGrid("setCellText", 0, 1, "GREYER");
</script>{% endhighlight %}


#### setCellText(primaryKeyValue, field, value)
{:#methods:setcelltext}

Used to update a particular cell value based on specified primarykeyvalue and fieldname

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
<td class="name">primaryKeyValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">It is used to set the primarykey value for selecting the corresponding row cell.</td>
</tr>
<tr>
<td class="name">field</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">It is used to set the field name for selecting the corresponding column cell.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">It is used to set the value for the cell based on specified primaryKeyValue and field name.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// update a particular cell value
gridObj.setCellText(10248,"EmployeeID", "GREYER");
</script>{% endhighlight %}

{% highlight html %}
 
<script>
// update a particular cell value
$("#Grid").ejGrid("setCellText", 10248, "EmployeeID", "GREYER");
</script>{% endhighlight %}


### setCellValue(index, fieldName, cellValue)
{:#methods:setcellvalue}

Used to update a particular cell value based on specified row Index and the fieldName.

N> It will working only for batch edit mode.  

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
<td class="name">Index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">It is used to set the index for selecting the row.</td>
</tr>
<tr>
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">It is used to set the field name for selecting column.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">It is used to set the value for the selected cell.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %} 

<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
//Used to update a particular cell value
gridObj.setCellValue(1,"EmployeeID", "GREYER");
</script>{% endhighlight %}

{% highlight html %}
 
<script>
//Used to update a particular cell value
$("#Grid").ejGrid("setCellValue", 1, "EmployeeID", "GREYER");
</script>{% endhighlight %}


### setValidationToField(fieldName, rules)
{:#methods:setvalidationtofield}

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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Specify the field name of the column to set validation rules</td>
</tr>
<tr>
<td class="name">rules</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Specify the validation rules for the field</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// It is used to set validation to a field during editing
gridObj.setValidationToField("OrderID", { required: true }); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// It is used to set validation to a field during editing
$("#Grid").ejGrid("setValidationToField", "OrderID", { required: true });
</script>{% endhighlight %}


### showColumns(headerText)
{:#methods:showcolumns}

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
<td class="name">headerText</td>
<td class="type"><span class="param-type">array/string</span></td>
<td class="description last">you can pass either array of header text of various columns or a header text of a column to show</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.showColumns("Order ID"); // Shows column based on the given header text of the column
gridObj.showColumns(["Order ID", "Customer ID"]); // Shows columns based on the array of header text of the columns given
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Shows column based on the given header text of the column
$("#Grid").ejGrid("showColumns", "Order ID"); 
// Shows columns based on the array of header text of the columns given
$("#Grid").ejGrid("showColumns", ["Order ID", "Customer ID"]);                  
</script>{% endhighlight %}

### sortColumn(columnName, \[sortingDirection\])
{:#methods:sortcolumn}


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
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field name of the column as columnName for which sorting have to be performed</td>
</tr>
<tr>
<td class="name">sortingDirection</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"><span class="optional">optional</span> Pass the sort direction ascending/descending by which the column have to be sort. By default it is sorting in an ascending order</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
gridObj.sortColumn("OrderID", "ascending"); // Sends a sorting request to the grid with specified columnName and sortDirection
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a sorting request to the grid with specified columnName and sortDirection
$("#Grid").ejGrid("sortColumn", "OrderID", "ascending");        
</script>{% endhighlight %}


### startEdit($tr)
{:#methods:startedit}

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
<td class="name">$tr</td>
<td class="type"><span class="param-type">jQuery</span></td>
<td class="description last">Pass the tr- selected row element to be edited in grid</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Element

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an edit record request to the grid
gridObj.startEdit($(".gridcontent tr").first()); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends an edit record request to the grid
$("#Grid").ejGrid("startEdit", $(".gridcontent tr").first());        
</script>{% endhighlight %}


### ungroupColumn(fieldName)
{:#methods:ungroupcolumn}

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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the field Name of the column to be ungrouped from grouped column collection</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends an ungroup column request to the grid
gridObj.ungroupColumn("OrderID"); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends an ungroup column request to the grid
$("#Grid").ejGrid("ungroupColumn", "OrderID");        
</script>{% endhighlight %}


### updateRecord(fieldName, data)
{:#methods:updaterecord}

Update a edited record in grid control when allowEditing is set as true.

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
<td class="name">fieldName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the primary key field Name of the column</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass the edited JSON data of record need to be update.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Sends a update record request to the grid
gridObj.updateRecord("OrderID", { OrderID: 10249, EmployeeID: 3 }); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// Sends a update record request to the grid
$("#Grid").ejGrid("updateRecord", "OrderID", { OrderID: 10249, EmployeeID: 3 });        
</script>{% endhighlight %}

### windowonresize()
{:#methods:windowonresize}

It adapts grid to its parent element or to the browsers window.

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}

{% highlight html %}
 
<script>
// Create grid object.
var gridObj = $("#Grid").data("ejGrid");
// Used for resizing the grid window
gridObj.windowonresize(); 
</script>{% endhighlight %}

{% highlight html %}
 
<script>
// Used for resizing the grid window
$("#Grid").ejGrid("windowonresize");        
</script>{% endhighlight %}


## Events

### actionBegin
{:#events:actionbegin}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentPage</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current selected page number.</td>
</tr>
<tr>
<td class="name">previousPage</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected page number.</td>
</tr>
<tr>
<td class="name">endIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the end row index of that current page.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">startIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the start row index of that current page.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">columnSortDirection</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column sort direction.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current edited row.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current action event type.</td>
</tr>
<tr>
<td class="name">primaryKey</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key.</td>
</tr>
<tr>
<td class="name">primaryKeyValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">selectedRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected row index.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">tr</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns selected row for delete.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentFilteringColumn</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current filtering column field name.</td>
</tr>
<tr>
<td class="name">currentFilterObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current filtering object.</td>
</tr>
<tr>
<td class="name">filterCollection</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns filter details.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr> 
<tr>
<td class="name">argument</td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current column field name.</td>
</tr>
<tr>
<td class="name">columnType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns type of the column like number, string and so on.</td>
</tr>
<tr>
<td class="name">filtermodel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterbeforeopen".</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">dataSource</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dataSource.</td>
</tr>
<tr>
<td class="name">filtermodel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">query</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query manager.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterchoicerequest".</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">dataSource</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dataSource.</td>
</tr>
<tr>
<td class="name">filtermodel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">query</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query manager.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterchoicesearch".</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current column field name.</td>
</tr>
<tr>
<td class="name">columnType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns type of the column like number, string and so on.</td>
</tr>
<tr>
<td class="name">filtermodel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name">isCustomFilter</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the customfilter option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterbeforeopen".</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}
{% highlight html %} 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   actionBegin: function (args){}
});
</script>{% endhighlight %}

### actionComplete
{:#events:actioncomplete}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentPage</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current selected page number.</td>
</tr>
<tr>
<td class="name">previousPage</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected page number.</td>
</tr>
<tr>
<td class="name">endIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the end row index of that current page.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">startIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the start row index of the current page.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current sorted column field name.</td>
</tr>
<tr>
<td class="name">columnSortDirection</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column sort direction.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current edited row.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">primaryKey</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key.</td>
</tr>
<tr>
<td class="name">primaryKeyValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name">selectedRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selectedRow index.</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">tr</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns selected row for delete.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns empty record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentFilteringColumn</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current filtering column field name.</td>
</tr>
<tr>
<td class="name">currentFilterObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current filtering object.</td>
</tr>
<tr>
<td class="name">filterCollection</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns filter details.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr> 
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">dataSource</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dataSource.</td>
</tr>
<tr>
<td class="name">filtermodel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterchoicerequest".</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current column field name.</td>
</tr>
<tr>
<td class="name">columnType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns type of the column like number, string and so on.</td>
</tr>
<tr>
<td class="name">filtermodel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterafteropen".</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">dataSource</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dataSource.</td>
</tr>
<tr>
<td class="name">filtermodel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterchoicesearch".</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">
columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current column field name.</td>
</tr>
<tr>
<td class="name">columnType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns type of the column like number, string and so on.</td>
</tr>
<tr>
<td class="name">filtermodel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the excel filter model.</td>
</tr>
<tr>
<td class="name">isCustomFilter</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the customfilter option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type as "filterafteropen".</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




####Example
{:.example}


{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   actionComplete: function (args) {}
}); 
</script>{% endhighlight %}


### actionFailure
{:#events:actionfailure}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
<td class="description last">Arguments in actionFailure when grid is initialized.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
<td class="description last">Arguments in actionFailure after grid paging action is completed.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentPage</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current selected page number.</td>
</tr>
<tr>
<td class="name">previousPage</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected page number.</td>
</tr>
<tr>
<td class="name">endIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the end row index of that current page.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">startIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the start row index of the current page.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after grid sorting action is completed.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current sorted column field name.</td>
</tr>
<tr>
<td class="name">columnSortDirection</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column sort direction.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after grid grouping action is completed.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after grid record editing action is completed.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current edited row.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">primaryKey</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key.</td>
</tr>
<tr>
<td class="name">primaryKeyValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after grid record save action is completed.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name">selectedRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selectedRow index.</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after grid record delete action is completed.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">tr</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns selected row for delete.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after add new record action is completed.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns empty record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after grid filtering action is completed.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentFilteringColumn</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current filtering column field name.</td>
</tr>
<tr>
<td class="name">currentFilterObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current filtering object.</td>
</tr>
<tr>
<td class="name">filterCollection</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns filter details.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   actionFailure: function (args) {}
}); 
</script>{% endhighlight %}


### batchAdd
{:#events:batchadd}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">columnObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column index.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element.</td>
</tr>
<tr>
<td class="name">primaryKey</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the primaryKey.</td>
</tr>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   batchAdd: function (args) {}
});
</script>{% endhighlight %}

### batchDelete
{:#events:batchdelete}


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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">primaryKey</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the primary key.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row Index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   batchDelete: function (args) {}
});
</script>{% endhighlight %}


### beforeBatchAdd
{:#events:beforebatchadd}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">defaultData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the default data object.</td>
</tr>
<tr>
<td class="name">primaryKey</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the primaryKey.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   beforeBatchAdd: function (args) {}
});
</script>{% endhighlight %}

### beforeBatchDelete
{:#events:beforebatchdelete}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">primaryKey</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the primaryKey.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row data.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   beforeBatchDelete: function (args) {}
});
</script>{% endhighlight %}


### beforeBatchSave
{:#events:beforebatchsave}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">batchChanges</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the changed record object.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   beforeBatchSave: function (args) {}
});
</script>{% endhighlight %}


### beginEdit
{:#events:beginedit}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current edited row.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">primaryKey</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the primary key.</td>
</tr>
<tr>
<td class="name">primaryKeyValue</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the primary key value.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   beginEdit: function (args) {}
});
</script>{% endhighlight %}


### cellEdit
{:#events:celledit}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">validationRules</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the validation rules.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column name.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the cell value.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row data object.</td>
</tr>
<tr>
<td class="name">previousValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the previous value of the cell.</td>
</tr>
<tr>
<td class="name">columnObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
<tr>
<td class="name">isForeignKey</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns isForeignKey option value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   cellEdit: function (args) {}
});
</script>{% endhighlight %}

### cellSave
{:#events:cellsave}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column name.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the cell value.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row data object.</td>
</tr>
<tr>
<td class="name">previousValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the previous value of the cell.</td>
</tr>
<tr>
<td class="name">columnObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
<tr>
<td class="name">isForeignKey</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns isForeignKey option value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   cellSave: function (args) {}
});
</script>{% endhighlight %}

### cellSelected
{:#events:cellselected}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected cell index value.</td>
</tr>
<tr>
<td class="name">previousRowCellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected cell index value.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected cell element.</td>
</tr>
<tr>
<td class="name">previousRowCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected cell element.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name">selectedRowCellIndex</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the selected row cell index values.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   cellSelected: function (args) {}
});
</script>{% endhighlight %}

### cellSelecting
{:#events:cellselecting}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected cell index value.</td>
</tr>
<tr>
<td class="name">previousRowCellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected cell index value.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected cell element.</td>
</tr>
<tr>
<td class="name">previousRowCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected cell element.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name">previousRowCellIndex</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the previously selected row cell index values</td>
</tr>
<tr>
<td class="name">isCtrlKeyPressed</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns whether the ctrl key is pressed while selecting cell</td>
</tr>
<tr>
<td class="name">isShiftKeyPressed</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns whether the shift key is pressed while selecting cell</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   cellSelecting: function (args) {}
});
</script>{% endhighlight %}


### columnDrag
{:#events:columndrag}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggableType</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable column object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns target elements based on mouse move position.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   columnDrag: function (args) {}
});
</script>{% endhighlight %}

### columnDragStart
{:#events:columndragstart}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggableType</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable column object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drag start element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    columnDragStart: function (args) {}
});
</script>{% endhighlight %}

### columnDrop
{:#events:columndrop}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggableType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable column object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns dropped dragged element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
 columnDrop: function (args) {}
});
</script>{% endhighlight %}

### rowDrag
{:#events:rowdrag}

Triggered when the row is being dragged.

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
<td class="description last">Arguments when rowDrag event is triggered.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggableType</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable row object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns target elements based on mouse move position.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns JSON data of dragged rows.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   rowDrag: function (args) {}
});
</script>{% endhighlight %}

### rowDragStart
{:#events:rowdragstart}

Triggered when row dragging begins.

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
<td class="description last">Arguments when rowDragStart event is triggered.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggableType</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable row object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drag start element cell.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the JSON data of dragged rows.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
    rowDragStart: function (args) {}
});
</script>{% endhighlight %}

### rowDrop
{:#events:rowdrop}

Triggered when the row is dropped.

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
<td class="description last">Arguments when rowDrop event is triggered.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggableType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns draggable element type.</td>
</tr>
<tr>
<td class="name">rows</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the draggable row object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current mouse position cell element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the JSON data of dragged rows.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
 rowDrop: function (args) {}
});
</script>{% endhighlight %}


### columnSelected
{:#events:columnselected}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected cell index value.</td>
</tr>
<tr>
<td class="name">previousColumnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected column index value.</td>
</tr>
<tr>
<td class="name">headerCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected header cell element.</td>
</tr>
<tr>
<td class="name">prevColumnHeaderCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected header cell element.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns corresponding column object (JSON).</td>
</tr>
<tr>
<td class="name">selectedColumnsIndex</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the selected columns values.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   columnSelected: function (args) {}
});
</script>{% endhighlight %}

### columnSelecting
{:#events:columnselecting}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected column index value.</td>
</tr>
<tr>
<td class="name">previousColumnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected column index value.</td>
</tr>
<tr>
<td class="name">headerCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected header cell element.</td>
</tr>
<tr>
<td class="name">prevColumnHeaderCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected header cell element.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns corresponding column object (JSON).</td>
</tr>
<tr>
<td class="name">previousColumnIndex</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the previously selected column index values</td>
</tr>
<tr>
<td class="name">isCtrlKeyPressed</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns whether the ctrl key is pressed while selecting cell</td>
</tr>
<tr>
<td class="name">isShiftKeyPressed</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns whether the shift key is pressed while selecting cell</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   columnSelecting: function (args) {}
});
</script>{% endhighlight %}

### contextClick
{:#events:contextclick}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the status of contextmenu item which denotes its enabled state</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target item.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   contextClick: function (args) {}
});
</script>{% endhighlight %}

### contextOpen
{:#events:contextopen}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the status of contextmenu item which denotes its enabled state</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target item.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   contextOpen: function (args) {}
});
</script>{% endhighlight %}

### create
{:#events:create}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
   create: function (args){}
});
</script>{% endhighlight %}


### dataBound
{:#events:databound}

Triggered when the grid is bound with data during initial rendering.

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
 dataBound: function (args) {}
});
</script>{% endhighlight %}

### destroy
{:#events:destroy}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   destroy: function (args) {}
});
</script>{% endhighlight %}

### detailsCollapse
{:#events:detailscollapse}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">detailsRow</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns detail row element.</td>
</tr>
<tr>
<td class="name">masterData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns master row of detail row record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">masterRow</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns master row element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   detailsCollapse: function (args) {}
});
</script>{% endhighlight %}

### detailsDataBound
{:#events:detailsdatabound}


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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">detailsElement</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns details row element.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the details row data.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
   detailsDataBound: function (args){}
});
</script>{% endhighlight %}

### detailsExpand
{:#events:detailsexpand}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">detailsRow</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns detail row element.</td>
</tr>
<tr>
<td class="name">masterData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns master row of detail row record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">masterRow</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns master row element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
 <div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   detailsExpand: function (args) {}
});
</script>{% endhighlight %}

### endAdd
{:#events:endadd}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns added data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   endAdd: function (args) {}
});
</script>{% endhighlight %}

### endDelete
{:#events:enddelete}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   endDelete: function (args) {}
});
</script>{% endhighlight %}

### endEdit
{:#events:endedit}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns modified data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   endEdit: function (args) {}
});
</script>{% endhighlight %}


### load
{:#events:load}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   load: function (args) {}
});
</script>{% endhighlight %}

### mergeCellInfo
{:#events:mergecellinfo}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid cell.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current row record object (JSON).</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the text value in the cell.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">rowMerge</td>
<td class="type"><span class="param-type">void</span></td>
<td class="description last">Method to merge Grid rows.</td>
</tr>
<tr>
<td class="name">colMerge</td>
<td class="type"><span class="param-type">void</span></td>
<td class="description last">Method to merge Grid columns.</td>
</tr>
<tr>
<td class="name">merge</td>
<td class="type"><span class="param-type">void</span></td>
<td class="description last">Method to merge Grid rows and columns.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   mergeCellInfo: function (args){}
});
</script>{% endhighlight %}

### queryCellInfo
{:#events:querycellinfo}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid cell.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current row record object (JSON).</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the text value in the cell.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   queryCellInfo: function (args){}
});
</script>{% endhighlight %}

### recordClick
{:#events:recordclick}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index of the selected row.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the jQuery object of the current selected row.</td>
</tr>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected cell.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the cell index value.</td>
</tr>
<tr>
<td class="name">cellValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the corresponding cell value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the Header text of the column corresponding to the selected cell.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   recordClick: function (args) {}
});
</script>{% endhighlight %}

### recordDoubleClick
{:#events:recorddoubleclick}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index of the selected row.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the jQuery object of the current selected row.</td>
</tr>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected cell.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected cell index value.</td>
</tr>
<tr>
<td class="name">cellValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the corresponding cell value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the Header text of the column corresponding to the selected cell.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   recordDoubleClick: function (args) {}
});
</script>{% endhighlight %}

### resized
{:#events:resized}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column index.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid object.</td>
</tr>
<tr>
<td class="name">oldWidth</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the old width value.</td>
</tr>
<tr>
<td class="name">newWidth</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the new width value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   resized: function (args) {}
});
</script>{% endhighlight %}

### resizeEnd
{:#events:resizeend}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column index.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid object.</td>
</tr>
<tr>
<td class="name">oldWidth</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the old width value.</td>
</tr>
<tr>
<td class="name">newWidth</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the new width value.</td>
</tr>
<tr>
<td class="name">extra</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the extra width value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   resizeEnd: function (args) {}
});
</script>{% endhighlight %}


### resizeStart
{:#events:resizestart}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column index.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid object.</td>
</tr>
<tr>
<td class="name">oldWidth</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the old width value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   resizeStart: function (args) {}
});
</script>{% endhighlight %}

### rightClick
{:#events:rightclick}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index of the selected row.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected row.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected row data object.</td>
</tr>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the cell index of the selected cell.</td>
</tr>
<tr>
<td class="name">cellValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the cell value.</td>
</tr>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}


{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   rightClick: function (args) {}
});
</script>{% endhighlight %}

### rowDataBound
{:#events:rowdatabound}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns grid row.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current row record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
   rowDataBound: function (args){}
});
</script>{% endhighlight %}

### rowSelected
{:#events:rowselected}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name">foreignKeyData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the foreign key record object (JSON).</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the row index of the selected row.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current selected row.</td>
</tr>
<tr>
<td class="name">prevRow</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected row element.</td>
</tr>
<tr>
<td class="name">prevRowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected row index.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
 
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   rowSelected: function (args) {}
});
</script>{% endhighlight %}


### rowSelecting
{:#events:rowselecting}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selected row index value.</td>
</tr>
<tr>
<td class="name">row</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selected row element.</td>
</tr>
<tr>
<td class="name">prevRow</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous selected row element.</td>
</tr>
<tr>
<td class="name">prevRowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the previous selected row index.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   rowSelecting: function (args) {}
});
</script>{% endhighlight %}


### templateRefresh
{:#events:templaterefresh}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cell object.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current row data.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current row index.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div>
<script>
$("#Grid").ejGrid({
 templateRefresh: function (args) {}
});
</script>{% endhighlight %}

### toolBarClick
{:#events:toolbarclick}

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
<td class="name">argument</td>
<td class="type"><ts name="ej.Grid.Model"/><span class="param-type">Object</span></td>
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the status of toolbar item which denotes its enabled state</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target item.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">gridModel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
</tr>
<tr>
<td class="name">toolbarData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the toolbar object of the selected toolbar element.</td>
</tr>
<tr>
<td class="name">itemId</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the Id of the current toolbar element.</td>
</tr>
<tr>
<td class="name">itemIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the index of the current toolbar element.</td>
</tr>
<tr>
<td class="name">itemName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the current toolbar element.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="Grid"></div> 
<script>
$("#Grid").ejGrid({
   toolbarClick: function (args) {}
});
</script>{% endhighlight %}

