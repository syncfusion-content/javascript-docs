---
layout: post
title: Properties, Methods and Events of ejTreeGrid Widget
description: Methods, members, events available in ejTreeGrid
documentation: API
platform: js
keywords: ejTreeGrid, API, Essential JS TreeGrid
---

# ejTreeGrid

 Custom Design for HTML TreeGrid control.


#### Syntax

{% highlight javascript %}

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

### allowPaging `boolean`
{:#members:allowpaging}

Enables/disables pagination of rows in TreeGrid

#### Default Value

* false


#### Example


{% highlight html %}

        $("#treegrid").ejTreeGrid({ allowPaging : true });
        
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


### childMapping `string`
{:#members:childmapping}

Specifies the mapping property path for sub tasks in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<script>                          
        $("#treegrid").ejTreeGrid({  childMapping : "Children" });
</script>

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

### columns.allowCellSelection `boolean`
{:#members:columns-allowcellselection}

Enables/disables cell selection.

#### Default Value:

* false


#### Example


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({ columns: [{ allowCellSelection: true },{allowCellSelection: false }]  });

{% endhighlight %}

### columns.editType `enum`
{:#members:columns-edittype}

<ts name = "ej.TreeGrid.EditingType"/>

Specifies the edit type of the column.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">String</td>
<td class="description">It Specifies String edit type.</td>
</tr>
<tr>
<td class="name">Boolean</td>
<td class="description">It Specifies Boolean edit type.</td>
</tr>
<tr>
<td class="name">Numeric</td>
<td class="description">It Specifies Numeric edit type.</td>
</tr>
<tr>
<td class="name">Dropdown</td>
<td class="description">It Specifies Dropdown edit type.</td>
</tr>
<tr>
<td class="name">DatePicker</td>
<td class="description">It Specifies DatePicker edit type.</td>
</tr>
<tr>
<td class="name">DateTimePicker</td>
<td class="description">It Specifies DateTimePicker edit type.</td>
</tr>
<tr>
<td class="name">Maskedit</td>
<td class="description">It Specifies Maskedit edit type.</td>
</tr>
</tbody>
</table>

#### Default Value:

* ej.TreeGrid.EditingType.String


#### Example


{% highlight html %}
 
 $("#treegrid").ejTreeGrid({columns: [{ editType: ej.TreeGrid.EditingType.String},{editType: ej.TreeGrid.EditingType.Boolean}]});

{% endhighlight %}


### columns.field `string`
{:#members:columns-field}

Specifies the name of the field from the dataSource to bind with this column.


#### Default Value:

* ""


#### Example


{% highlight html %}
      
        $("#treegrid").ejTreeGrid({columns: [{ field: "Name"},{field: "Type"}]});

{% endhighlight %}


### columns.filterEditType `enum`
{:#members:columns-filteredittype}

<ts name = "ej.TreeGrid.EditingType"/>

Specifies the type of the editor control to be used to filter the rows.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">String</td>
<td class="description">It Specifies String edit type.</td>
</tr>
<tr>
<td class="name">Boolean</td>
<td class="description">It Specifies Boolean edit type.</td>
</tr>
<tr>
<td class="name">Numeric</td>
<td class="description">It Specifies Numeric edit type.</td>
</tr>
<tr>
<td class="name">Dropdown</td>
<td class="description">It Specifies Dropdown edit type.</td>
</tr>
<tr>
<td class="name">DatePicker</td>
<td class="description">It Specifies DatePicker edit type.</td>
</tr>
<tr>
<td class="name">DateTimePicker</td>
<td class="description">It Specifies DateTimePicker edit type.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.TreeGrid.EditingType.String


#### Example


{% highlight html %}
       
        $("#treegrid").ejTreeGrid({columns: [{ filterEditType: ej.TreeGrid.EditingType.String},{filterEditType: ej.TreeGrid.EditingType.Boolean}]});

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

### columns.format `object`
{:#members:columns-format}

Specifies the display format of a column

#### Default Value

* null


#### Example

{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{ field: "Currency",  format: "{0:C2}" }, //... ]});

{% endhighlight %}


### columns.isTemplateColumn `boolean`

{:#members:columns-istemplatecolumn}

Specifies whether the column is a template column

#### Default Value

* false

#### Example

{% highlight html %}
         
     $("#treegrid").ejTreeGrid({columns: [{ field:"CustomColumn", isTemplateColumn: true, templateID: "customColumnTemplate"}]});

{% endhighlight %}


### columns.headerTextAlign `enum`
{:#members:columns-headertextalign}

<ts name = "ej.TextAlign"/>

Specifies the alignment of the column header text

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Left</td>
<td class="description">align the header text to the left</td>
</tr>
<tr>
<td class="name">Right</td>
<td class="description">align the header text to the right</td>
</tr>
<tr>
<td class="name">Justify</td>
<td class="description">To justify the header alignment</td>
</tr>
<tr>
<td class="name">Center</td>
<td class="description">align the header text to the center</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.TextAlign.Left

#### Example

{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{  headerTextAlign: ej.TextAlign.Center},{headerTextAlign: ej.TextAlign.Right}]});

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

### columns.textAlign `enum`
{:#members:columns-textalign}

<ts name = "ej.TextAlign"/>

Specifies the text alignment for the column

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Left</td>
<td class="description">align the content text to the left</td>
</tr>
<tr>
<td class="name">Right</td>
<td class="description">align the content text to the right</td>
</tr>
<tr>
<td class="name">Justify</td>
<td class="description">To justify the content alignment</td>
</tr>
<tr>
<td class="name">Center</td>
<td class="description">align the content text to the center</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.TextAlign.Left

#### Example

{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{  textAlign: ej.TextAlign.Center},{ textAlign: ej.TextAlign.Right}]});

{% endhighlight %}


### columns.templateID `String`

{:#members:columns-templateid}

Specifies the template for the TreeGrid column

#### Default Value

* ""

#### Example

{% highlight html %}
         
     $("#treegrid").ejTreeGrid({columns: [{ field:"CustomColumn", isTemplateColumn: true, templateID: "customColumnTemplate"}]});

{% endhighlight %}

### columns.allowEditing `boolean`

{:#members:columns-allowediting}

Enables or disables the ability to edit a row or cell.

#### Default Value

* false

#### Example

{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{  allowEditing: false }]});

{% endhighlight %}

### columnDialogFields `array`
{:#members:columndialogfields}

To Specify the column fields to be displayed in the dialog while inserting a column using column menu.

#### Default Value:
{:.param}

* []


#### Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>  
        $("#treegrid").ejTreeGrid({ columnDialogFields: ["field", "headerText", "editType", "width", "visible", "allowSorting", "textAlign", "headerTextAlign"] });                   
</script>

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

### cssClass `string`
{:#members:cssclass}

Specify the CSS class for TreeGrid to achieve custom theme.


#### Default Value:
{:.param}

* ""

#### Example
{:.example}


{% highlight html %}
 
<div id="treeGrid"></div> 
<script>          
        $("#treeGrid").ejTreeGrid({  cssClass : "gradient-lime" });
</script>

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
{:#members:headertextoverflow}

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

        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipItems: ["TaskName","TaskID","StartDate"] });                       

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

### editSettings.beginEditAction `enum`
{:#members:editsettings-begineditaction}

<ts name = "ej.TreeGrid.BeginEditAction"/>

Specifies the mouse action whether single click or double click to begin the editing

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">DblClick</td>
<td class="description">you can begin the editing at double click</td>
</tr>
<tr>
<td class="name">Click</td>
<td class="description">you can begin the editing at single click</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.TreeGrid.BeginEditAction.DblClick

#### Example


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid({  editSettings:{beginEditAction : ej.TreeGrid.BeginEditAction.Click} });

{% endhighlight %}

### editSettings.editMode `enum`
{:#members:editsettings-editmode}

<ts name = "ej.TreeGrid.EditMode"/>

specifies the edit mode in TreeGrid , "cellEditing" is for cell type editing and "rowEditing" is for entire row.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">CellEditing</td>
<td class="description">you can edit a cell.</td>
</tr>
<tr>
<td class="name">RowEditing</td>
<td class="description">you can edit a row.</td>
</tr>
</tbody>
</table>


#### Default Value

* ej.TreeGrid.EditMode.CellEditing


#### Example


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid({  editSettings:{editMode : ej.TreeGrid.EditMode.CellEditing} });

{% endhighlight %}


### editSettings.rowPosition `enum`
{:#members:editsettings-rowposition}

<ts name = "ej.TreeGrid.RowPosition"/>

Specifies the position where the new row has to be added.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Top</td>
<td class="description">you can add a new row at top.</td>
</tr>
<tr>
<td class="name">Bottom</td>
<td class="description">you can add a new row at bottom.</td>
</tr>
<tr>
<td class="name">Above</td>
<td class="description">you can add a new row to above selected row.</td>
</tr>
<tr>
<td class="name">Below</td>
<td class="description">you can add a new row to below selected row.</td>
</tr>
<tr>
<td class="name">Child</td>
<td class="description">you can add a new row as a child for selected row.</td>
</tr>
</tbody>
</table>


#### Default Value

* "top"


#### Example


{% highlight html %}
   
 $("#treegrid").ejTreeGrid({  editSettings:{rowPosition : ej.TreeGrid.RowPosition.Bottom} });

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


### filterSettings `object`
{:#members:filtersettings}

Options for filtering and customizing filter actions.

### filterSettings.filterBarMode `string`
{:#members:filtersettings-filterbarmode}

Specifies the mode on which column filtering should start

#### Default Value

* "immediate"


#### Example


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({  filterSettings: { filterBarMode : "onEnter"} });

{% endhighlight %}

### filterSettings.filteredColumns `array`
{:#members:filtersettings-filteredcolumns}

Specifies the column collection for filering the TreeGrid content on initial load

#### Default Value

* []

#### Example


{% highlight html %}
   
$("#treegrid").ejTreeGrid({
    filterSettings: {
        filteredColumns: [{
            value: "plan",
            field: "taskName",
            predicate: "and",
            operator: "startswith"
        }]
    },
});                   

{% endhighlight %}

### locale `string`
{:#members:locale}

Specifies the localization information to customize the User Interface (UI) to support regional language and culture


#### Default Value

* "en-US"


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  locale : "fr-FR" });                   

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

### isResponsive `boolean`
{:#members:isresponsive}

Enables or disables the responsiveness of TreeGrid


#### Default Value

* "false"


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  isResponsive : true });                   

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


### pageSettings `object`
{:#members:pagesettings}

Specifies the options for customizing the pager.


### pageSettings.pageCount `number`
{:#members:pagesettings-pagecount}

Using this property we can specify the number of pages should pager contains, according to this count TreeGrid height will be updated.


#### Default Value:
{:.param}

* 8


#### Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                          
        $("#treegrid").ejGantt({  
                        pageSettings:{pageCount: 10, }
                });
</script>              

{% endhighlight %}


### pageSettings.pageSize `number`
{:#members:pagesettings-pagesize}

This specifies the number of rows to display in each page.


#### Default Value:
{:.param}

* 12


#### Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  
                pageSettings:{pageSize : 10}
        });
</script>               

{% endhighlight %}

### pageSettings.totalRecordsCount `number`
{:#members:pagesettings-totalrecordscount}

Get the value of records which is bound to TreeGrid. The totalRecordsCount value is calculated based on the datasoure bound to TreeGrid.


#### Default Value:
{:.param}

* null


#### Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  
                        pageSettings:{totalRecordsCount : null}
                });
</script>               

{% endhighlight %}

### pageSettings.currentPage `number`
{:#members:pagesettings-currentpage}

Specifies the current page to display at load time.

#### Default Value:
{:.param}

* 1


#### Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  
                        pageSettings:{currentPage : 2}
                });
</script>               

{% endhighlight %}

### pageSettings.pageSizeMode `enum`
{:#members:pagesettings-pagesizemode}

<ts name = "ej.TreeGrid.PageSizeMode"/>

Specifies the mode of record count in a page, whether it should count all the records or the root to count zero level parent records.  

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">All</td>
<td class="description">To count all the parent and child records.</td>
</tr>
<tr>
<td class="name">Root</td>
<td class="description">To count the Zeroth level parent records.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.TreeGrid.PageSizeMode.All


#### Example


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({ pageSettings :{ pageSizeMode:ej.TreeGrid.PageSizeMode.Root } });                   

{% endhighlight %}


### pageSettings.template `string`
{:#members:pagesettings-template}

Specifies the Custom template for Pager control.


#### Default Value

* null


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({ pageSettings :{ template:"PageTemplate" }});        

{% endhighlight %}

### cellTooltipTemplate `string`
{:#members:celltooltiptemplate}

Specifies the template for cell tooltip


#### Default Value

* null


#### Example


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({ cellTooltipTemplate : "CellTooltipTemplate"});        

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

### selectionMode `enum`
{:#members:selectionmode}

<ts name = "ej.TreeGrid.SelectionMode"/>

Specifies the type of selection whether to select row or cell.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Row</td>
<td class="description">you can select a row.</td>
</tr>
<tr>
<td class="name">Cell</td>
<td class="description">you can select a cell.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.TreeGrid.SelectionMode.Row


#### Example


{% highlight html %}
          
<div id="treegrid"></div> 
<script>   
        $("#treegrid").ejTreeGrid({ selectionMode:ej.TreeGrid.SelectionMode.Row });                      * 
</script>           

{% endhighlight %}


### selectionType `enum`
{:#members:selectiontype}

<ts name = "ej.TreeGrid.SelectionType"/>

Specifies the type of selection whether to select single row or multiple rows.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Single</td>
<td class="description">you can select a single row.</td>
</tr>
<tr>
<td class="name">Multiple</td>
<td class="description">you can select a multiple row.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.TreeGrid.SelectionType.Single


#### Example


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({ selectionType:ej.TreeGrid.SelectionType.Multiple });                   

{% endhighlight %}

### showColumnOptions `boolean`
{:#members:showcolumnoptions}

Enables/disables the options for inserting , deleting and renaming  columns.

#### Default Value:
{:.param}

* false

#### Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>   
        $("#treegrid").ejTreeGrid({ showColumnOptions:  true });                      * 
</script>

{% endhighlight %}


### showColumnChooser `boolean`
{:#members:showcolumnchooser}

Controls the visibility of the menu button, which is displayed on the column header. Clicking on this button will show a popup menu. When you choose “Columns” item from this popup, a list box with column names will be shown, from which you can select/deselect a column name to control the visibility of the respective columns.


#### Default Value
{:.param}
* false


#### Example


{% highlight html %}
 
  
        $("#treegrid").ejTreeGrid({ showColumnChooser:  true });      
        
{% endhighlight %}

### showDetailsRow `boolean`
{:#members:showdetailsrow}

Specifies the visibility of details view


#### Default Value
{:.param}
* false


#### Example


{% highlight html %}
                 
$("#treegrid").ejTreeGrid({
    showDetailsRow: true
});

{% endhighlight %}

### showDetailsRowInfoColumn `boolean`
{:#members:showdetailsrowinfocolumn}

Specifies the visibility of the expander column which is used to expand or collapse the details view


#### Default Value
{:.param}
* false


#### Example


{% highlight html %}
                 
$("#treegrid").ejTreeGrid({
    showDetailsRowInfoColumn: true
});

{% endhighlight %}

### detailsTemplate `string`
{:#members:detailstemplate}

Specifies the template for details view


#### Default Value
{:.param}
* ""


#### Example


{% highlight html %}
                 
$("#treegrid").ejTreeGrid({
    detailsTemplate: "#detailsTemplate"
});

{% endhighlight %}

### detailsRowHeight `number`
{:#members:detailsrowheight}

Specifies the row height of the details view


#### Default Value
{:.param}
* 100

#### Example

{% highlight html %}
                 
$("#treegrid").ejTreeGrid({
    detailsRowHeight: "150",
});

{% endhighlight %}

### showSummaryRow `boolean`
{:#members:showsummaryrow}

Specifies the visibility of summary row

#### Default Value
{:.param}
* false

#### Example

{% highlight html %}
                 
$("#treegrid").ejTreeGrid({
    showSummaryRow: true
});
{% endhighlight %}

### showTotalSummary `boolean`
{:#members:showtotalsummary}

Specifies the visibility of total summary row for the corresponding summary column

#### Default Value
{:.param}
* false

#### Example

{% highlight html %}
                 
$("#treegrid").ejTreeGrid({
    showTotalSummary: true
});
{% endhighlight %}

### summaryRows `array`
{:#members:summaryrows}

Specifies the summary row collection object to be displayed

#### Default Value
{:.param}
* []

#### Example

{% highlight html %}
                 
$("#treegrid").ejTreeGrid({
    summaryRows: [{
        title: "Maximum",
        summaryColumns: [{
            summaryType: ej.TreeGrid.SummaryType.Maximum,
            dataMember: "TotalUnits",
            displayColumn: "TotalUnits",
            prefix: "Individual maximum unit = "
        }, {
            summaryType: ej.TreeGrid.SummaryType.Maximum,
            dataMember: "TotalCosts",
            displayColumn: "TotalCosts",
            prefix: "Individual maximum Cost = ",
            format: "{0:C}"
        }]
    }, ],
});
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
    showGridCellTooltip: true
});
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
    showGridExpandCellTooltip: true
});
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


### toolbarSettings.showToolbar `boolean`
{:#members:toolbarsettings-showtoolbar}

Shows/hides the toolbar.


#### Default Value:
{:.param}
* false


#### Example


{% highlight html %}
   
        $("#treegrid").ejTreeGrid({ showToolbar:  true });                       

{% endhighlight %}


### toolbarSettings.toolbarItems `array`
{:#members:toolbarsettings-toolbaritems}

<ts name = "ej.TreeGrid.ToolbarItems"/>

Specifies the list of toolbar items to be rendered in TreeGrid toolbar

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Add</td>
<td class="description">Enables the add icon in toolbar</td>
</tr>
<tr>
<td class="name">Edit</td>
<td class="description">Enables the edit icon in toolbar</td>
</tr>
<tr>
<td class="name">Delete</td>
<td class="description">Enables the edit icon in toolbar</td>
</tr>
<tr>
<td class="name">Update</td>
<td class="description">Enables the update icon in toolbar</td>
</tr>
<tr>
<td class="name">Cancel</td>
<td class="description">Enables the cancel icon in toolbar</td>
</tr>
<tr>
<td class="name">ExpandAll</td>
<td class="description">Enables the expand all icon in toolbar</td>
</tr>
<tr>
<td class="name">Collapse All</td>
<td class="description">Enables the collapse all icon in toolbar</td>
</tr>
<tr>
<td class="name">PdfExport</td>
<td class="description">Enables the pdf export icon in toolbar</td>
</tr>
<tr>
<td class="name">ExcelExport</td>
<td class="description">Enables the excel export icon in toolbar</td>
</tr>
</tbody>
</table>

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

### addRow(data, rowPosition)
{:#methods:addrow}

Adds a new row in TreeGrid, while allowAdding is set to true

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
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Item to add in TreeGrid row.</td>
</tr>
<tr>
<td class="name">rowPosition</td>
<td class="type">enum</td>
<td class="description">Defines in which position the row wants to be added</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create TreeGrid object
var treeGridObj = $("#treegrid").data("ejTreeGrid");
var data = {taskId:"40",taskName:"New Task 40",startDate:"2/20/2014",startDate:"2/25/2014"};
treeGridObj.addRecord(data, ej.TreeGrid.RowPosition.Child); // To add a task
</script>
{% endhighlight %}


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

### selectCells(Indexes,preservePreviousSelectedCell)
{:#methods:selectcells}

To select cell based on the cell and row index dynamically.

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
<td class="name">Indexes</td>
<td class="type">array</td>
<td class="description">array of cell indexes to be select</td>
</tr>
<tr>
<td class="name">preservePreviousSelectedCell</td>
<td class="type">boolean</td>
<td class="description">Defines that we need to preserve the previously selected cells or not</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create treegrid
var treegridObj = $("#treegrid").data("ejTreeGrid");
var indexes = [{rowIndex:4, cellIndex: 4}, {rowIndex: 3, cellIndex: 3}];
treegridObj.selectCells(indexes, true); // To add a task
</script>
{% endhighlight %}

### renameColumn(columnIndex,name)
{:#methods:renamecolumn}

To rename a column with the specified name

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
<td class="name">columnIndex</td>
<td class="type">number</td>
<td class="description">Index of the column to be renamed</td>
</tr>
<tr>
<td class="name">name</td>
<td class="type">string</td>
<td class="description">Header text of the column </td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create treegrid
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.renameColumn(1, "New Text"); // To re name the column
</script>
{% endhighlight %}

### deleteColumn(columnIndex)
{:#methods:deletecolumn}

To delete the specified column

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
<td class="name">columnIndex</td>
<td class="type">number</td>
<td class="description">Index of the column to be deleted</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create treegrid
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.deleteColumn(1); // To delete the specified column
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

{% endhighlight %}

### expandAtLevel(index)
{:#methods:expandatlevel}

Expands the records at specific hierarchical level

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
<td class="description">you can pass the level as index number to expand</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.expandAtLevel(2);
</script> 

{% endhighlight %}

### collapseAtLevel(index)
{:#methods:collapseatlevel}

Collapses the records at specific hierarchical level

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
<td class="description">you can pass the particular level as index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.collapseAtLevel(2);
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



### freezePrecedingColumns (field)
{:#methods:freezeprecedingcolumns}

Freeze all the columns preceding to the column specified by the field name.

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
<td class="name">field</td>
<td class="type">string</td>
<td class="description">Freeze all Columns before this field column.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.freezePrecedingColumns(field); 
</script>
{% endhighlight %}


### freezeColumn (field, isFrozen)
{:#methods:freezecolumn}

Freeze/unfreeze the specified column.

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
<td class="name">field</td>
<td class="type">string</td>
<td class="description">Freeze/Unfreeze this field column.</td>
</tr>
<tr>
<td class="name">isFrozen</td>
<td class="type">boolean</td>
<td class="description">Decides to Freeze/Unfreeze this field column.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.freezeColumn(field, isFrozen); 
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
<td class="description">Event parameters when TreeGrid is initialized:
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
<td class="type">number</td>
<td class="description">Returns the row index of collapsed record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of collapsed record..</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns Request Type.</td>
</tr>
<tr>
<td class="name">expanded</td>
<td class="type">boolean</td>
<td class="description">Returns state of a record whether it is in expanded or collapsed state.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the event type.</td>
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
<td class="type">number</td>
<td class="description">Returns the row index of collapsing record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of collapsing record..</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the event Type.</td>
</tr>
<tr>
<td class="name">expanded</td>
<td class="type">boolean</td>
<td class="description">Returns state of a record whether it is in expanded or collapsing state.</td>
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

### columnResized
{:#events:columnresized}


Triggered after a column resized

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
<td class="description">Arguments when columnResized event is triggered.
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
<td class="description">Returns the control model values.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the event Type.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type">object</td>
<td class="description">Returns the column data which is resized</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type">number</td>
<td class="description">Returns the index of the column being resized.</td>
</tr>
<tr>
<td class="name">newWidth</td>
<td class="type">number</td>
<td class="description">Returns resized column width after resized.</td>
</tr>
<tr>
<td class="name">oldWidth</td>
<td class="type">number</td>
<td class="description">Returns resized column width before resizing</td>
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
   columnResized: function (args) {}
});
</script>
{% endhighlight %}

### columnResizeStart
{:#events:columnresizestart}

Triggered while start to resize a column

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
<td class="description">Arguments when columnResizeStart event is triggered.
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
<td class="description">Returns the control model values.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the event Type.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type">object</td>
<td class="description">Returns the column data in which the resizing started</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type">number</td>
<td class="description">Returns the column index in which the resizing started</td>
</tr>
<tr>
<td class="name">oldWidth</td>
<td class="type">number</td>
<td class="description">Returns column width before dragging</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type">object </td>
<td class="description">Returns initial column element object.</td>
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
   columnResizeStart: function (args) {}
});
</script>
{% endhighlight %}

### columnResizeEnd
{:#events:columnresizeend}

Triggered when a column has been resized

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
<td class="description">Arguments when columnResizeEnd event is triggered.
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
<td class="description">Returns the control model values.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the event Type.</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type">object</td>
<td class="description">Returns the column data in which the resizing started</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type">number</td>
<td class="description">Returns the column index in which the resizing started</td>
</tr>
<tr>
<td class="name">extra</td>
<td class="type">number</td>
<td class="description">Returns the column width difference, before and after the resizing</td>
</tr>
<tr>
<td class="name">newWidth</td>
<td class="type">number</td>
<td class="description">Returns the new column width after resized</td>
</tr>
<tr>
<td class="name">oldWidth</td>
<td class="type">number</td>
<td class="description">Returns column width before dragging</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type">object </td>
<td class="description">Returns initial column element object.</td>
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
   columnResizeEnd: function (args) {}
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
<td class="type">array</td>
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

### create
{:#events:create}

Triggered when TreeGrid is rendered completely 

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
<td class="description">Arguments when create event is triggered.
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
   create: function (args) {}
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
<td class="type">number</td>
<td class="description">Returns the row index of expanded record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of expanded record..</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type">string</td>
<td class="description">Returns Request Type.</td>
</tr>
<tr>
<td class="name">expanded</td>
<td class="type">boolean</td>
<td class="description">Returns state of a record whether it is in expanded or expanded state.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the event type.</td>
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
<td class="type">number</td>
<td class="description">Returns the row index of expanding record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of expanding record..</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the event Type.</td>
</tr>
<tr>
<td class="name">expanded</td>
<td class="type">boolean</td>
<td class="description">Returns state of a record whether it is in expanded or collapsed state.</td>
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


Triggered while Treegrid is loaded

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
<td class="name">cellElement</td>
<td class="type">object</td>
<td class="description">Returns the selecting cell element.</td>
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
<td class="description">Returns the row element of rendering row.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of rendering row record.</td>
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
<td class="type">object</td>
<td class="description">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name">draggedRowIndex</td>
<td class="type">number</td>
<td class="description">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name">targetRow</td>
<td class="type">object</td>
<td class="description">Returns the row on which we are dragging.</td>
</tr>
<tr>
<td class="name">targetRowIndex</td>
<td class="type">number</td>
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
<td class="type">object</td>
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
<td class="type">object</td>
<td class="description">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name">draggedRowIndex</td>
<td class="type">number</td>
<td class="description">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name">targetRow</td>
<td class="type">object</td>
<td class="description">Returns the row which we are dropped to row.</td>
</tr>
<tr>
<td class="name">targetRowIndex</td>
<td class="type">number</td>
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

### cellSelecting
{:#events:cellselecting}

Triggered before selecting a cell

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
<td class="description">Arguments when cellSelecting event is triggered.
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
<td class="name">cellIndex</td>
<td class="type">number</td>
<td class="description">Returns the cell index on the selection.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type">number</td>
<td class="description">Returns the row index on the selection</td>
</tr>
<tr>
<td class="name">targetCell</td>
<td class="type">object</td>
<td class="description">Returns the selecting cell element</td>
</tr>
<tr>
<td class="name">targetRow</td>
<td class="type">object</td>
<td class="description">Returns the selecting row element</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the selecting record object</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the Gantt object Model</td>
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
   cellSelecting: function (args) {}
});
</script>
{% endhighlight %}

### cellSelected
{:#events:cellselected}

Triggered after selected a cell

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
<td class="description">Arguments when cellSelected event is triggered.
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
<td class="name">cellIndex</td>
<td class="type">number</td>
<td class="description">Returns the cell index on the selection.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type">number</td>
<td class="description">Returns the row index on the selection</td>
</tr>
<tr>
<td class="name">targetCell</td>
<td class="type">object</td>
<td class="description">Returns the selecting cell element</td>
</tr>
<tr>
<td class="name">targetRow</td>
<td class="type">object</td>
<td class="description">Returns the selecting row element</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the selecting record object</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the Gantt object Model</td>
</tr>
<tr>
<td class="name">previousData</td>
<td class="type">object</td>
<td class="description">Returns the previously selected row data</td>
</tr>
<tr>
<td class="name">previousCellIndex</td>
<td class="type">object</td>
<td class="description">Returns the previously selected cell index</td>
</tr>
<tr>
<td class="name">perviousRowIndex</td>
<td class="type">object</td>
<td class="description">Returns the previously selected row index</td>
</tr>
<tr>
<td class="name">previousTargetCell</td>
<td class="type">object</td>
<td class="description">Returns the previously selected cell element</td>
</tr>
<tr>
<td class="name">previousTargetRow</td>
<td class="type">object</td>
<td class="description">Returns the previously selected row element</td>
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
   cellSelected: function (args) {}
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
<td class="name">targetRow</td>
<td class="type">object</td>
<td class="description">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">number</td>
<td class="description">Returns the index of selecting row record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of selected record.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the event type.</td>
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
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data selecting record.</td>
</tr>
<tr>
<td class="name">recordIndex</td>
<td class="type">string</td>
<td class="description">Returns the index of selecting row record.</td>
</tr>
<tr>
<td class="name">targetRow</td>
<td class="type">object</td>
<td class="description">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name">previousData</td>
<td class="type">object</td>
<td class="description">Returns the previous selected data.</td>
</tr>
<tr>
<td class="name">previousIndex</td>
<td class="type">string</td>
<td class="description">Returns the previous selected row index.</td>
</tr>
<tr>
<td class="name">previousTreeGridRow</td>
<td class="type">object</td>
<td class="description">Returns the previous selected row element.</td>
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



### toolbarClick
{:#events:toolbarclick}

Triggered when toolbar item is clicked in TreeGrid.

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
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Arguments when toolbarClick event is triggered.
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
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the current item.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the TreeGrid model.</td>
</tr>
<tr>
<td class="name">itemName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the toolbar item on which mouse click has been performed</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
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
   toolbarClick: function (args) {}
});
</script>
{% endhighlight %}


