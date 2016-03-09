---
layout: post
title: ejTreeGrid
description: Methods, members, events available in ejTreeGrid
documentation: API
platform: js
keywords: ejTreeGrid, API, Essential JS TreeGrid
---

# ejTreeGrid

 Custom Design for Html Tree grid control.


#### Syntax

{% highlight js %}

$(element).ejTreeGrid()

{% endhighlight %}

#### Example


{% highlight html %}
 
<treegrid id="treegrid">treegrid</treegrid> 
 
<script>
// Create TreeGrid
$('#treegrid').ejTreeGrid();    
</script>

{% endhighlight %}


#### Requires

* module:jQuery
* module:jquery.globalize.js
* module:jquery.easing.1.3.js
* module:jsrender.js
* module:ej.web.all.js


## Members


### allowColumnResize `boolean`
{:#members:allowcolumnresize}

Enables or disables the ability to resize the column width interactively.


#### Default Value

 * false


#### Example


{% highlight html %}   
              
        $("#treegrid").ejTreeGrid({ allowColumnResize:  true });
                                 
{% endhighlight %}


### allowDragAndDrop `boolean`
{:#members:allowdraganddrop}

Enables or disables the ability to drag and drop the row interactively to reorder the rows.


#### Default Value

* false


#### Example


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({  allowDragAndDrop : true });
        
{% endhighlight %}


### allowFiltering `boolean`
{:#members:allowfiltering}

Enables or disables the ability to filter the data on all the columns. Enabling this property will display a row with editor controls corresponding to each column. You can restrict filtering on particular column by disabling this property directly on that column instance itself.


#### Default Value

* false


#### Example


{% highlight html %}

        $("#treegrid").ejTreeGrid({  allowFiltering : true });
{% endhighlight %}


### allowKeyboardNavigation `boolean`
{:#members:allowkeyboardnavigation}

Enables or disables keyboard navigation.


#### Default Value

* true


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({ allowKeyboardNavigation : true});                   
{% endhighlight %}


### allowMultiSorting `boolean`
{:#members:allowmultisorting}

Enables or disables the ability to sort the rows based on multiple columns/fields by clicking on each column header. Rows will be sorted recursively on clicking the column headers.


#### Default Value

* false


#### Example


{% highlight html %}
                   
        $("#treegrid").ejTreeGrid({ allowMultiSorting : true});                 

{% endhighlight %}


### allowSelection `boolean`
{:#members:allowselection}

Enables or disables the ability to select a row interactively.


#### Default Value

* true


#### Example


{% highlight html %}
   
        $("#treegrid").ejTreeGrid({ allowSelection:  true });                    

{% endhighlight %}


### allowSorting `boolean`
{:#members:allowsorting}

Enables or disables the ability to sort the rows based on a single field/column by clicking on that column header. When enabled, rows can be sorted only by single field/column.


#### Default Value

* false


#### Example


{% highlight html %}

        $("#treegrid").ejTreeGrid({ allowSorting : true });
        
{% endhighlight %}


### altRowTemplateID `string`
{:#members:altrowtemplateid}

Specifies the id of the template that has to be applied for alternate rows.


#### Default Value

* ""


#### Example


{% highlight html %}
                   
        $("#treegrid").ejTreeGrid(
 {
    altRowTemplateID: "altRowCustomTemplate"
 });            

{% endhighlight %}


### columns `array`
{:#members:columns}

Option for adding columns; each column has the option to bind to a field in the dataSource.


#### Example


{% highlight html %}
                          
        $("#treegrid").ejTreeGrid(
 {
    columns: [{ field: "Name", headerText: "Name", isTemplateColumn: true, templateID: "customColumnTemplate" },
                          { field: "Type", headerText: "Type" },
                          { field: "DateCreated", headerText: "Date Created" },
                          { field: "DateModified", headerText: "Date Modified" }]       
 });            

{% endhighlight %}


### columns.allowFiltering `boolean`
{:#members:columns-allowfiltering}

Enables or disables the ability to filter the rows based on this column.


#### Default Value

* false


#### Example


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({ columns: [{ allowFiltering: true },{allowFiltering: false }] });
{% endhighlight %}


### columns.allowSorting `boolean`
{:#members:columns-allowsorting}

Enables or disables the ability to sort the rows based on this column/field.

#### Default Value:

* false


#### Example


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({ columns: [{ allowSorting: true },{allowSorting: false }]  });

{% endhighlight %}


### columns.editType `string`
{:#members:columns-edittype}

Specifies the edit type of the column.


#### Default Value:

* null


#### Example


{% highlight html %}
 
 $("#treegrid").ejTreeGrid({columns: [{ editType: "stringedit"},{editType: "booleanedit"}]});

{% endhighlight %}


### columns.field `string`
{:#members:columns-field}

Specifies the name of the field from the dataSource to bind with this column.


#### Default Value:

* null


#### Example


{% highlight html %}
      
        $("#treegrid").ejTreeGrid({columns: [{ field: "Name"},{field: "Type"}]});

{% endhighlight %}


### columns.filterEditType `string`
{:#members:columns-filteredittype}

Specifies the type of the editor control to be used to filter the rows.


#### Default Value

* null


#### Example


{% highlight html %}
       
        $("#treegrid").ejTreeGrid({columns: [{ filterEditType: "stringedit"},{filterEditType: "booleanedit"}]});

{% endhighlight %}


### columns.headerText `string`
{:#members:columns-headertext}

Header text of the column.


#### Default Value

* null


#### Example


{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{ headerText: "Name"},{headerText: "Type"}]});

{% endhighlight %}


### columns.visible `boolean`
{:#members:columns-visible}

Controls the visibility of the column.


#### Default Value

* true


#### Example


{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{ field: "name",visible: true},{field: "Type",visible: false}]});

{% endhighlight %}


### columns.headerTemplateID `String`

{:#members:columns-headertemplateid}

Specifies the header template value for the column header

#### Default Value

* ""

#### Example

{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{  headerTemplateID: "#dataTemplate1"},{ headerTemplateID: "#dataTemplate2"}]});

{% endhighlight %}

### columns.isFrozen `boolean`

{:#members:columns-isfrozen}

Specifies whether the column is frozen

#### Default Value

* false

#### Example

{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{  isFrozen: true}]});

{% endhighlight %}


### columns.allowFreezing `boolean`

{:#members:columns-allowfreezing}

Enables or disables the ability to freeze/unfreeze the columns

#### Default Value

* false

#### Example

{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{  allowFreezing: false }]});

{% endhighlight %}

### contextMenuSettings `object`
{:#members:contextmenusettings}

Options for displaying and customizing context menu items.


### contextMenuSettings.contextMenuItems `array`
{:#members:contextmenusettings-contextmenuitems}

Option for adding items to context menu.


#### Default Value

* []


#### Example


{% highlight html %}
   
        $("#treegrid").ejTreeGrid({ contextMenuItems: [ej.TreeGrid.ContextMenuItems.Add,ej.TreeGrid.ContextMenuItems.Edit] });                   

{% endhighlight %}


### contextMenuSettings.showContextMenu `boolean`
{:#members:contextmenusettings-showcontextmenu}

Shows/hides the context menu.


#### Default Value

* false


#### Example


{% highlight html %}
  
        $("#treegrid").ejTreeGrid(contextMenuSettings :{ showContextMenu:  true });                      

{% endhighlight %}


### dataSource `array`
{:#members:datasource}

Specifies hierarchical or self-referential data to populate the TreeGrid.


#### Default Value

* null


#### Example


{% highlight html %}
          
        $("#treegrid").ejTreeGrid(
 {
    dataSource:[{Id:2,TaskName:"Testing",startDate:"12/1/2000",Duration:5 }]    
 });            

{% endhighlight %}


### headerTextOverflow `string`
{:#members:headerTextOverflow}

Specifies whether to wrap the header text when it is overflown i.e., when it exceeds the header width.

#### Default Value

* "none"

#### Example


{% highlight html %}
         
        $("#treegrid").ejTreeGrid({ headerTextOverflow: "wrap"});

{% endhighlight %}


### dragTooltip `object`
{:#members:dragtooltip}

Options for displaying and customizing the tooltip. This tooltip will show the preview of the row that is being dragged.


### dragTooltip.showTooltip `boolean`
{:#members:dragtooltip-showtooltip}

Specifies whether to show tooltip while dragging a row.


#### Default Value

* true


#### Example


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid(dragTooltip :{ showTooltip:  true });

{% endhighlight %}


### dragTooltip.tooltipItems `array`
{:#members:dragtooltip-tooltipitems}

Option to add field names whose corresponding values in the dragged row needs to be shown in the preview tooltip.


#### Default Value

* []


#### Example


{% highlight html %}

        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipItems: "TaskName","TaskID","StartDate" });                       

{% endhighlight %}


### dragTooltip.tooltipTemplate `string`
{:#members:dragtooltip-tooltiptemplate}

Custom template for that tooltip that is shown while dragging a row.


#### Default Value

* null


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipTemplate: "" });        

{% endhighlight %}


### editSettings `object`
{:#members:editsettings}

Options for enabling and configuring the editing related operations. 


### editSettings.allowAdding `boolean`
{:#members:editsettings-allowadding}

Enables or disables the button to add new row in context menu as well as in toolbar.


#### Default Value

* true


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowAdding : true} });

{% endhighlight %}


### editSettings.allowDeleting `boolean`
{:#members:editsettings-allowdeleting}

Enables or disables the button to delete the selected row in context menu as well as in toolbar.


#### Default Value

* true


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowDeleting : true} });    

{% endhighlight %}


### editSettings.allowEditing `boolean`
{:#members:editsettings-allowediting}

Enables or disables the ability to edit a row or cell.


#### Default Value

* false


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowEditing : true} });     

{% endhighlight %}


### editSettings.editMode `string`
{:#members:editsettings-editmode}

specifies the edit mode in TreeGrid , "cellEditing" is for cell type editing and "rowEditing" is for entire row.


#### Default Value

* "cellEditing"


#### Example


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid({  editSettings:{editMode : "cellEditing"} });

{% endhighlight %}


### editSettings.rowPosition `string`
{:#members:editsettings-rowposition}

Specifies the position where the new row has to be added.


#### Default Value

* "top"


#### Example


{% highlight html %}
   
 $("#treegrid").ejTreeGrid({  editSettings:{rowPosition : "aboveSelectedRow"} });

{% endhighlight %}


### enableAltRow `boolean`
{:#members:enablealtrow}

Specifies whether to render alternate rows in different background colors.


#### Default Value

* true


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({ enableAltRow : false});                     

{% endhighlight %}


### enableCollapseAll `boolean`
{:#members:enablecollapseall}

Specifies whether to load all the rows in collapsed state when the TreeGrid is rendered for the first time.


#### Default Value

* false


#### Example


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid(
 {
    enableCollapseAll: false
 });            

{% endhighlight %}


### enableResize `boolean`
{:#members:enableresize}

Specifies whether to resize TreeGrid whenever window size changes.


#### Default Value

* false


#### Example


{% highlight html %}
        
        $("#treegrid").ejTreeGrid({enableResize:true});

{% endhighlight %}


### enableVirtualization `boolean`
{:#members:enablevirtualization}

Specifies whether to render only the visual elements that are visible in the UI. When you enable this property, it will reduce the loading time for loading large number of records. 


#### Default Value

* false


#### Example


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid({ enableVirtualization : true});                      

{% endhighlight %}


### filterBarMode `enum`
{:#members:filterbarmode}

Specifies if the filtering should happen immediately on each key press or only on pressing enter key.


#### Default Value

* "immediate"


#### Example


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({  filterBarMode : "onEnter" });

{% endhighlight %}


### idMapping `string`
{:#members:idmapping}

Specifies the name of the field in the dataSource, which contains the id of that row.


#### Default Value

* ""


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  IdMapping : "ID" });                   

{% endhighlight %}


### parentIdMapping `string`
{:#members:parentidmapping}

Specifies the name of the field in the dataSource, which contains the parent’s id. This is necessary to form a parent-child hierarchy, if the dataSource contains self-referential data.


#### Default Value

* ""


#### Example


{% highlight html %}
                
        $("#treegrid").ejTreeGrid({  parentIdMapping : "ID" });             

{% endhighlight %}


### query `object`
{:#members:query}

Specifies ej.Query to select data from the dataSource. This property is applicable only when the dataSource is ej.DataManager.


#### Default Value

* null


#### Example


{% highlight html %}
                          
        $("#treegrid").ejTreeGrid(
 {
    query:ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);      
 });            

{% endhighlight %}


### rowHeight `number`
{:#members:rowheight}

Specifies the height of a single row in tree grid. Also, we need to set same height in the CSS style with class name e-rowcell.


#### Default Value

* 30


#### Example


{% highlight html %}
                          
        $("#treegrid").ejTreeGrid({  
                        rowHeight : 30,
                        });
{% endhighlight %}



### rowTemplateID `string`
{:#members:rowtemplateid}

Specifies the id of the template to be applied for all the rows.


#### Default Value

* ""


#### Example


{% highlight html %}
                
        $("#treegrid").ejTreeGrid(
 {
    rowTemplateID: "customTemplate"
 });            

{% endhighlight %}


### selectedRowIndex `number`
{:#members:selectedrowindex}

Specifies the index of the selected row.


#### Default Value

* -1


#### Example


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid(
 {
    selectedRowIndex:2
 });            

{% endhighlight %}


### selectionType `string`
{:#members:selectiontype}

Specifies the type of selection whether to select single row or multiple rows.


#### Default Value

* "single"


#### Example


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({ selectionType:"multiple" });                   

{% endhighlight %}


### showColumnChooser `boolean`
{:#members:showcolumnchooser}

Controls the visibility of the menu button, which is displayed on the column header. Clicking on this button will show a popup menu. When you choose “Columns” item from this popup, a list box with column names will be shown, from which you can select/deselect a column name to control the visibility of the respective columns.


#### Default Value
{:.param}
* false


#### Example


{% highlight html %}
 
  
        $("#treegrid").ejTreeGrid({ showColumnChooser:  true });                        * 

{% endhighlight %}


### showGridCellTooltip `boolean`
{:#members:showgridcelltooltip}

Specifies whether to show tooltip when mouse is hovered on the cell.


#### Default Value
{:.param}
* true


#### Example


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid({  
                        showGridCellTooltip : true});

{% endhighlight %}


### showGridExpandCellTooltip `boolean`
{:#members:showgridexpandcelltooltip}

Specifies whether to show tooltip for the cells, which has expander button.


#### Default Value
{:.param}
* true


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  
                        showGridExpandCellTooltip : true});

{% endhighlight %}


### sizeSettings `object`
{:#members:sizesettings}

Options for setting width and height for TreeGrid.


### sizeSettings.height `string`
{:#members:sizesettings-height}

Height of the TreeGrid.


#### Default Value
{:.param}
* null


#### Example


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({sizeSettings{height:'450px'}});

{% endhighlight %}


### sizeSettings.width `string`
{:#members:sizesettings-width}

Width of the TreeGrid.


#### Default Value
{:.param}

* null


#### Example


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({sizeSettings{width:'500px'}});

{% endhighlight %}


### sortSettings `object`
{:#members:sortsettings}

Options for sorting the rows.


### sortSettings.sortedColumns `array`
{:#members:sortsettings-sortedcolumns}

Option to add columns based on which the rows have to be sorted recursively.


#### Default Value:
{:.param}
* []


#### Example


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({ sortSettings{sortedColumns : []}});            

{% endhighlight %}




### toolbarSettings `object`
{:#members:toolbarsettings}

Options for displaying and customizing the toolbar items.


### toolbarSettings.showToolBar `boolean'
{:#members:toolbarsettings-showtoolbar}

Shows/hides the toolbar.


#### Default Value:
{:.param}
* false


#### Example


{% highlight html %}
   
        $("#treegrid").ejTreeGrid({ showToolBar:  true });                       

{% endhighlight %}


### toolbarSettings.toolbarItems `array`
{:#members:toolbarsettings-toolbaritems}

Option to add items to the toolbar.


#### Default Value:
{:.param}
* []


#### Example


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({ toolbarItems: [ej.TreeGrid.ToolbarItems.Add,ej.TreeGrid.ToolbarItems.Edit] });                       

{% endhighlight %}


### treeColumnIndex `number`
{:#members:treecolumnindex}

Specifies the index of the column that needs to have the expander button. By default, cells in the first column contain the expander button.


#### Default Value:
{:.param}
* 0


#### Example


{% highlight html %}
         
        $("#treegrid").ejTreeGrid(
 {
    treeColumnIndex: 1
 });            

{% endhighlight %}



## Methods

### clearSelection(index)
{:#methods:clearselection}

To clear all the selection in TreeGrid

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
<td class="name">index</td>
<td class="type">number</td>
<td class="description">you can pass a row index to clear the row selection.</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.clearSelection(2);
</script>
{% endhighlight %}


{% highlight html %}
 
 <div id="treegrid"></div> 
 
<script>
// To clear the selection
$("#treegrid").ejTreeGrid("clearSelection",2);  
</script>

{% endhighlight %}


### collapseAll()
{:#methods:collapseall}

To collapse all the parent items in tree grid

#### Example

{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.collapseAll(); // To collapse all parent items in tree grid
</script>
{% endhighlight %}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// To expand all items
$("#treegrid").ejTreeGrid("collapseAll");       
</script>

{% endhighlight %}


### hideColumn(headerText)
{:#methods:hidecolumn}

To hide the column by using header text

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
<td class="name">headerText</td>
<td class="type">string</td>
<td class="description">you can pass a header text of a column to hide.</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.hideColumn("Task Name");
</script> 
</script>
{% endhighlight %}


### refresh(dataSource, query)
{:#methods:refresh}

To refresh the changes in tree grid

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
<td class="name">dataSource</td>
<td class="type">array</td>
<td class="description">Pass which data source you want to show in tree grid</td>
</tr>
<tr>
<td class="name">query</td>
<td class="type">object</td>
<td class="description">Pass which data you want to show in tree grid</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create treegrid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
var dataManager = ej.DataManager(projectData);
var query = ej.Query().select(["taskID", "taskName", "startDate", "endDate", "subtasks", "progress", "duration"]);
treegridObj.refresh(dataManager, query) // To refresh the tree grid content
</script>
{% endhighlight %}



### freezePrecedingColumns ()
{:#methods:freezeprecedingcolumns}

Freeze all the columns preceding to the column specified by the field name.

#### Example

{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.freezePrecedingColumns(field); 
</script>
{% endhighlight %}


{% highlight html %}
 
 <div id="treegrid"></div> 
 
<script>
// Save the edited cell
$("#treegrid").ejTreeGrid("freezePrecedingColumns" , field);  
</script>
{% endhighlight %}



### freezeColumn ()

{:#methods:freezecolumn}

Freeze/unfreeze the specified column.

#### Example

{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.freezeColumn(field, isFrozen); 
</script>
{% endhighlight %}


{% highlight html %}
 
 <div id="treegrid"></div> 
 
<script>
// Save the edited cell
$("#treegrid").ejTreeGrid("freezeColumn" , field , isFrozen);  
</script>
{% endhighlight %}


### saveCell()
{:#methods:savecell}

To save the edited cell in TreeGrid


#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.saveCell(); 
</script>
{% endhighlight %}


{% highlight html %}
 
 <div id="treegrid"></div> 
 
<script>
// Save the edited cell
$("#treegrid").ejTreeGrid("saveCell");  
</script>
{% endhighlight %}


### search(searchString)
{:#methods:search}

To search an item with search string provided at the run time

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
<td class="name">searchString</td>
<td class="type">string</td>
<td class="description">you can pass a searchString to search the tree grid</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.search("Plan"); // To search a Plan string in tree grid data
</script>

{% endhighlight %}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// To search a task
$("#treegrid").ejTreeGrid("search","Plan");     
</script>

{% endhighlight %}


### showColumn(headerText)
{:#methods:showcolumn}

To show the column by using header text

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
<td class="name">headerText</td>
<td class="type">string</td>
<td class="description">you can pass a header text of a column to show.</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.showColumn("Task Name");
</script> 

{% endhighlight %}


### sortColumn(columnName, columnSortDirection)
{:#methods:sortcolumn}

To sorting the data based on the particular fields

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
<td class="name">columnName</td>
<td class="type">string</td>
<td class="description">you can pass a name of column to sort.</td>
</tr>
<tr>
<td class="name">columnSortDirection</td>
<td class="type">string</td>
<td class="description">you can pass a sort direction to sort the column.</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.sortColumn("Start Date", ej.sortOrder.Descending); // To sort the data
</script>
{% endhighlight %}


{% highlight html %}
 
 <div id="treegrid"></div> 
 
<script>
// Sort the particular field.
$("#treegrid").ejTreeGrid("sortColumn","Start Date", ej.sortOrder.Descending);  
</script>
{% endhighlight %}


## Events

### actionBegin
{:#events:actionbegin}

Triggered before every success event of TreeGrid action.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters before completing the sorting operation in TreeGrid:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type">string</td>
<td class="description">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">columnSortDirection</td>
<td class="type">string</td>
<td class="description">Returns the direction of sorting ascending or descending.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters while performing expand operation:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">keyValue</td>
<td class="type">string</td>
<td class="description">Returns the value of expanding parent element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters while performing collapse operation:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">keyValue</td>
<td class="type">string</td>
<td class="description">Returns the value of collapsing parent element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters before completing the delete operation:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">string</td>
<td class="description">Returns the data or deleting element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   actionBegin: function (args) {}
});
</script>
{% endhighlight %}


### actionComplete
{:#events:actioncomplete}


Triggered for every TreeGrid action success event.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters when treegrid is initialized:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the grid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters after perform the sorting in grid tree is completed:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type">string</td>
<td class="description">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">columnSortDirection</td>
<td class="type">string</td>
<td class="description">Returns the direction of sorting ascending or descending</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters after searching completed:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">keyValue</td>
<td class="type">string</td>
<td class="description">Returns the value of searched element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters while performing after completing the delete operation is completed:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">string</td>
<td class="description">Returns the data of deleted element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters after the add operation completed:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">string</td>
<td class="description">Returns the data added element.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">number</td>
<td class="description">Returns selected record index</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Event parameters after the edit operation completed:
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">string</td>
<td class="description">Returns the data added element.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">number</td>
<td class="description">Returns selected record index</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   actionComplete: function (args) {}
});
</script>
{% endhighlight %}


### beginEdit
{:#events:beginedit}

Triggered while enter the edit mode in the TreeGrid cell

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when beginEdit event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">rowElement</td>
<td class="type">object</td>
<td class="description">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name">cellElement</td>
<td class="type">object</td>
<td class="description">Returns the Element of editing cell.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of current cell record.</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type">number</td>
<td class="description">Returns the column Index of cell belongs.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   beginEdit: function (args) {}
});
</script>
{% endhighlight %}


### collapsed
{:#events:collapsed}


Triggered after collapsed the TreeGrid record

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when collapsed event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">object</td>
<td class="description">Returns the row index of collapsed record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of edited cell record..</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   collapsed: function (args) {}
});
</script>
{% endhighlight %}


### collapsing
{:#events:collapsing}


Triggered while collapsing the TreeGrid record

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when collapsing event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">object</td>
<td class="description">Returns the row index of collapsing record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of edited cell record..</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#TreeGrid").ejTreeGrid({
   collapsing: function (args) {}
});
</script>
{% endhighlight %}


### contextMenuOpen
{:#events:contextmenuopen}


Triggered while Context Menu is rendered in TreeGrid control

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when context menu is rendered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">contextMenuItems</td>
<td class="type">boolean</td>
<td class="description">Returns the default context menu items to which we add custom items.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   contextMenuOpen: function (args) {}
});
</script>
{% endhighlight %}


### endEdit
{:#events:endedit}


Triggered after saved the modified cellValue in TreeGrid

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when endEdit event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">rowElement</td>
<td class="type">object</td>
<td class="description">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name">cellElement</td>
<td class="type">object</td>
<td class="description">Returns the Element of editing cell.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of edited cell record.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type">string</td>
<td class="description">Returns the column name of edited cell belongs.</td>
</tr>
<tr>
<td class="name">columnObject</td>
<td class="type">object</td>
<td class="description">Returns the column object of edited cell belongs.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   endEdit: function (args) {}
});
</script>

{% endhighlight %}


### expanded
{:#events:expanded}


Triggered after expand the record

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when expanded event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">object</td>
<td class="description">Returns the row index of record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of edited cell record..</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   expanded: function (args) {}
});
</script>
{% endhighlight %}



### expanding
{:#events:expanding}


Triggered while expanding the TreeGrid record

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when expanding event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">object</td>
<td class="description">Returns the row index of record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of edited cell record..</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   expanding: function (args) {}
});
</script>
{% endhighlight %}


### load
{:#events:load}


Triggered while TreeGrid is loaded

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when load event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   load: function (args) {}
});
</script>
{% endhighlight %}


### queryCellInfo
{:#events:querycellinfo}


Triggered while rendering each cell in the TreeGrid

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when queryCellInfo event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">rowElement</td>
<td class="type">object</td>
<td class="description">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name">cellValue</td>
<td class="type">string</td>
<td class="description">Returns the value of cell.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of current cell record.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type">object</td>
<td class="description">Returns the column of cell belongs.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   queryCellInfo: function (args) {}
});
</script>
{% endhighlight %}


### rowDataBound
{:#events:rowdatabound}


Triggered while rendering each row

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when rowDataBound event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">rowElement</td>
<td class="type">object</td>
<td class="description">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of edited cell record.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowDataBound: function (args) {}
});
</script>
{% endhighlight %}


### rowDrag
{:#events:rowdrag}


Triggered while dragging a row in TreeGrid control

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when dragging a row.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggedRow</td>
<td class="type">boolean</td>
<td class="description">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name">draggedRowIndex</td>
<td class="type">boolean</td>
<td class="description">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name">targetRow</td>
<td class="type">boolean</td>
<td class="description">Returns the row on which we are dragging.</td>
</tr>
<tr>
<td class="name">targetRowIndex</td>
<td class="type">boolean</td>
<td class="description">Returns the row index on which we are dragging.</td>
</tr>
<tr>
<td class="name">canDrop</td>
<td class="type">boolean</td>
<td class="description">Returns that we can drop over that record or not.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowDrag: function (args) {}
});
</script>
{% endhighlight %}


### rowDragStart
{:#events:rowdragstart}


Triggered while start to drag row in TreeGrid control

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when drag starts.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggedRow</td>
<td class="type">boolean</td>
<td class="description">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name">draggedRowIndex</td>
<td class="type">boolean</td>
<td class="description">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowDragStart: function (args) {}
});
</script>
{% endhighlight %}


### rowDragStop
{:#events:rowdragstop}


Triggered while drop a row in TreeGrid control

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when dragging a row.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggedRow</td>
<td class="type">boolean</td>
<td class="description">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name">draggedRowIndex</td>
<td class="type">boolean</td>
<td class="description">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name">targetRow</td>
<td class="type">boolean</td>
<td class="description">Returns the row which we are dropped to row.</td>
</tr>
<tr>
<td class="name">targetRowIndex</td>
<td class="type">boolean</td>
<td class="description">Returns the row index which we are dropped to row.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowDragStop: function (args) {}
});
</script>
{% endhighlight %}


### rowSelected
{:#events:rowselected}


Triggered after the row is selected.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when rowSelected event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">rowElement</td>
<td class="type">object</td>
<td class="description">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">string</td>
<td class="description">Returns the index of selecting row record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of selected record.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowSelected: function (args) {}
});
</script>
{% endhighlight %}


### rowSelecting
{:#events:rowselecting}


Triggered before the row is going to be selected.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description">Arguments when rowSelecting event is triggered.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">rowElement</td>
<td class="type">object</td>
<td class="description">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">string</td>
<td class="description">Returns the index of selecting row record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data selecting record.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowSelecting: function (args) {}
});
</script>
{% endhighlight %}



### toolBarClick
{:#events:toolbarclick}

Triggered when toolbar item is clicked in TreeGrid.

<table class="params">
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentTarget{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
itemName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the toolbar item on which mouse click has been performed</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   toolBarClick: function (args) {}
});
</script>
{% endhighlight %}


