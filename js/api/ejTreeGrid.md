---
layout: post
title: ejTreeGrid
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Tree grid control.










$(element).ejTreeGrid<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<treegrid id="treegrid">treegrid</treegrid> 
 
<script>
// Create TreeGrid
$('#treegrid').ejTreeGrid();    
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.globalize.js


* module:jquery.easing.1.3.js


* module:jsrender.js


* module:ej.web.all.js




## Members








### allowColumnResize<span class="type-signature type boolean">boolean</span>
{:#members:allowcolumnresize}








Enables or disables the ability to resize the column width interactively.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}   
              
        $("#treegrid").ejTreeGrid({ allowColumnResize:  true });
                                 
{% endhighlight %}







### allowDragAndDrop<span class="type-signature type boolean">boolean</span>
{:#members:allowdraganddrop}








Enables or disables the ability to drag and drop the row interactively to reorder the rows.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({  allowDragAndDrop : true });
        
{% endhighlight %}







### allowFiltering<span class="type-signature type boolean">boolean</span>
{:#members:allowfiltering}








Enables or disables the ability to filter the data on all the columns. Enabling this property will display a row.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}

        $("#treegrid").ejTreeGrid({  allowFiltering : true });
{% endhighlight %}







### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members:allowkeyboardnavigation}








Enables or disables keyboard navigation.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({ allowKeyboardNavigation : true});                   
{% endhighlight %}







### allowMultiSorting<span class="type-signature type boolean">boolean</span>
{:#members:allowmultisorting}








Enables or disables the ability to sort the rows based on multiple columns/fields by clicking on each column header. Rows will be sorted recursively on clicking the column headers.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
                   
        $("#treegrid").ejTreeGrid({ allowMultiSorting : true});                 

{% endhighlight %}







### allowSelection<span class="type-signature type boolean">boolean</span>
{:#members:allowselection}








Enables or disables the ability to select a row interactively.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
   
        $("#treegrid").ejTreeGrid({ allowSelection:  true });                    

{% endhighlight %}







### allowSorting<span class="type-signature type boolean">boolean</span>
{:#members:allowsorting}








Enables or disables the ability to sort the rows based on a single field/column by clicking on that column header. When enabled, rows can be sorted only by single field/column.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}

        $("#treegrid").ejTreeGrid({ allowSorting : true });
        
{% endhighlight %}







### altRowTemplateID<span class="type-signature type string">string</span>
{:#members:altrowtemplateid}








Specifies the id of the template that has to be applied for alternate rows.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
                   
        $("#treegrid").ejTreeGrid(
 {
    altRowTemplateID: "altRowCustomTemplate"
 });            

{% endhighlight %}







### columns<span class="type-signature type array">array</span>
{:#members:columns}








Option for adding columns; each column has the option to bind to a field in the dataSource.





Example
{:.example}


{% highlight html %}
                          
        $("#treegrid").ejTreeGrid(
 {
    columns: [{ field: "Name", headerText: "Name", isTemplateColumn: true, templateID: "customColumnTemplate" },
                          { field: "Type", headerText: "Type" },
                          { field: "DateCreated", headerText: "Date Created" },
                          { field: "DateModified", headerText: "Date Modified" }]       
 });            

{% endhighlight %}







### columns.allowFiltering<span class="type-signature type boolean">boolean</span>
{:#members:columns-allowfiltering}








Enables or disables the ability to filter the rows based on this column.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({ columns: [{ allowFiltering: true },{allowFiltering: false }] });
{% endhighlight %}







### columns.allowSorting<span class="type-signature type boolean">boolean</span>
{:#members:columns-allowsorting}








Enables or disables the ability to sort the rows based on this column/field.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({ columns: [{ allowSorting: true },{allowSorting: false }]  });

{% endhighlight %}







### columns.editType<span class="type-signature type string">string</span>
{:#members:columns-edittype}








Specifies the edit type of the column.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
 
 $("#treegrid").ejTreeGrid({columns: [{ editType: "stringedit"},{editType: "booleanedit"}]});

{% endhighlight %}







### columns.field<span class="type-signature type string">string</span>
{:#members:columns-field}








Specifies the name of the field from the dataSource to bind with this column.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
      
        $("#treegrid").ejTreeGrid({columns: [{ field: "Name"},{field: "Type"}]});

{% endhighlight %}







### columns.filterEditType<span class="type-signature type string">string</span>
{:#members:columns-filteredittype}








Specifies the type of the editor control to be used to filter the rows.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
       
        $("#treegrid").ejTreeGrid({columns: [{ filterEditType: "stringedit"},{filterEditType: "booleanedit"}]});

{% endhighlight %}







### columns.headerText<span class="type-signature type string">string</span>
{:#members:columns-headertext}








Header text of the column.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{ headerText: "Name"},{headerText: "Type"}]});

{% endhighlight %}







### columns.visible<span class="type-signature type boolean">boolean</span>
{:#members:columns-visible}








Controls the visibility of the column.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
         
        $("#treegrid").ejTreeGrid({columns: [{ field: "name",visible: true},{field: "Type",visible: false}]});

{% endhighlight %}







### contextMenuSettings<span class="type-signature type object">object</span>
{:#members:contextmenusettings}








Options for displaying and customizing context menu items.











### contextMenuSettings.contextMenuItems<span class="type-signature type array">array</span>
{:#members:contextmenusettings-contextmenuitems}








Options for displaying and customizing context menu items.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
   
        $("#treegrid").ejTreeGrid({ contextMenuItems: [ej.TreeGrid.ContextMenuItems.Add,ej.TreeGrid.ContextMenuItems.Edit] });                   

{% endhighlight %}







### contextMenuSettings.showContextMenu<span class="type-signature type boolean">boolean</span>
{:#members:contextmenusettings-showcontextmenu}








Shows/hides the context menu.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
  
        $("#treegrid").ejTreeGrid(contextMenuSettings :{ showContextMenu:  true });                      

{% endhighlight %}







### dataSource<span class="type-signature type array">array</span>
{:#members:datasource}








Specifies hierarchical or self-referential data to populate the TreeGrid.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
          
        $("#treegrid").ejTreeGrid(
 {
    dataSource:[{Id:2,TaskName:"Testing",startDate:"12/1/2000",Duration:5 }]    
 });            

{% endhighlight %}







### dragTooltip<span class="type-signature type object">object</span>
{:#members:dragtooltip}








Options for displaying and customizing the tooltip. This tooltip will show the preview of the row that is being dragged.











### dragTooltip.showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:dragtooltip-showtooltip}








Specifies whether to show tooltip while dragging a row.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid(dragTooltip :{ showTooltip:  true });

{% endhighlight %}







### dragTooltip.tooltipItems<span class="type-signature type array">array</span>
{:#members:dragtooltip-tooltipitems}








Option to add field names whose corresponding values in the dragged row needs to be shown in the preview tooltip.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}

        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipItems: "TaskName","TaskID","StartDate" });                       

{% endhighlight %}







### dragTooltip.tooltipTemplate<span class="type-signature type string">string</span>
{:#members:dragtooltip-tooltiptemplate}








Custom template for that tooltip that is shown while dragging a row.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipTemplate: "" });        

{% endhighlight %}







### editSettings<span class="type-signature type object">object</span>
{:#members:editsettings}








Options for enabling and configuring the editing related operations. 











### editSettings.allowAdding<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowadding}








Enables or disables the button to add new row in context menu as well as in toolbar.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowAdding : true} });

{% endhighlight %}







### editSettings.allowDeleting<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowdeleting}








Enables or disables the button to delete the selected row in context menu as well as in toolbar.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowDeleting : true} });    

{% endhighlight %}







### editSettings.allowEditing<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowediting}








Enables or disables the ability to edit a row or cell.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowEditing : true} });     

{% endhighlight %}







### editSettings.editMode<span class="type-signature type string">string</span>
{:#members:editsettings-editmode}








specifies the editmode in treegrid , "cellEditing" is for cell type editing and "rowEditing" is for entire row.




Default Value:
{:.param}






* cellEditing








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  editSettings:{editMode : "cellEditing"} });
</script>{% endhighlight %}







### editSettings.rowPosition<span class="type-signature type string">string</span>
{:#members:editsettings-rowposition}








Specifies the position where the new row has to be added.




Default Value:
{:.param}






* top








Example
{:.example}


{% highlight html %}
   
 $("#treegrid").ejTreeGrid({  editSettings:{rowPosition : "aboveSelectedRow"} });

{% endhighlight %}







### enableAltRow<span class="type-signature type boolean">boolean</span>
{:#members:enablealtrow}








Specifies whether to render alternate rows in different background colors.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({ enableAltRow : false});                     

{% endhighlight %}







### enableCollapseAll<span class="type-signature type boolean">boolean</span>
{:#members:enablecollapseall}








Specifies whether to load all the rows in collapsed state when the TreeGrid is rendered for the first time.




Default Value:
{:.param}






* "false"








Example
{:.example}


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid(
 {
    enableCollapseAll: false
 });            

{% endhighlight %}







### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}








Specifies whether to resize TreeGrid whenever window size changes.




Default Value:
{:.param}






* "false"








Example
{:.example}


{% highlight html %}
        
        $("#treegrid").ejTreeGrid({enableResize:true});

{% endhighlight %}







### enableVirtualization<span class="type-signature type boolean">boolean</span>
{:#members:enablevirtualization}








Specifies whether to render only the visual elements that are visible in the UI. When you enable this property, it will reduce the loading time for loading large number of records. 




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid({ enableVirtualization : true});                      

{% endhighlight %}







### filterBarMode<span class="type-signature type enum">enum</span>
{:#members:filterbarmode}








Specifies if the filtering should happen immediately on each key press or only on pressing enter key.




Default Value:
{:.param}






* immediate








Example
{:.example}


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({  filterBarMode : "onEnter" });

{% endhighlight %}







### idMapping<span class="type-signature type string">string</span>
{:#members:idmapping}








Specifies the name of the field in the dataSource, which contains the id of that row.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  IdMapping : "ID" });                   

{% endhighlight %}







### parentIdMapping<span class="type-signature type string">string</span>
{:#members:parentidmapping}








Specifies the name of the field in the dataSource, which contains the parent’s id. This is necessary to form a parent-child hierarchy, if the dataSource contains self-referential data.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
                
        $("#treegrid").ejTreeGrid({  parentIdMapping : "ID" });             

{% endhighlight %}







### query<span class="type-signature type object">object</span>
{:#members:query}








Specifies ej.Query to select data from the dataSource. This property is applicable only when the dataSource is ej.DataManager.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
                          
        $("#treegrid").ejTreeGrid(
 {
    query:ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);      
 });            

{% endhighlight %}







### rowHeight<span class="type-signature type number">number</span>
{:#members:rowheight}








Specifies the height of a single row in tree grid. Also, we need to set same height in the CSS style with class name e-rowcell.




Default Value:
{:.param}






* "30"








Example
{:.example}


{% highlight html %}
                          
        $("#treegrid").ejTreeGrid({  
                        rowHeight : 30,
                        });
{% endhighlight %}







### rowTemplateID<span class="type-signature type string">string</span>
{:#members:rowtemplateid}








Specifies the id of the template to be applied for all the rows.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
                
        $("#treegrid").ejTreeGrid(
 {
    rowTemplateID: "customTemplate"
 });            

{% endhighlight %}







### selectedRowIndex<span class="type-signature type number">number</span>
{:#members:selectedrowindex}








Specifies the index of the selected row.




Default Value:
{:.param}






* "-1"








Example
{:.example}


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid(
 {
    selectedRowIndex:2
 });            

{% endhighlight %}







### selectionType<span class="type-signature type string">string</span>
{:#members:selectiontype}








Specifies the type of selection whether to select single row or multiple rows.




Default Value:
{:.param}






* "single"








Example
{:.example}


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({ selectionType:"multiple" });                   

{% endhighlight %}







### showColumnChooser<span class="type-signature type boolean">boolean</span>
{:#members:showcolumnchooser}








Controls the visibility of the menu button, which is displayed on the column header. Clicking on this button will show a popup menu. When you choose “Columns” item from this popup, a list box with column names will be shown, from which you can select/deselect a column name to control the visibility of the respective columns.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
  
        $("#treegrid").ejTreeGrid({ showColumnChooser:  true });                        * 

{% endhighlight %}







### showGridCellTooltip<span class="type-signature type boolean">boolean</span>
{:#members:showgridcelltooltip}








Specifies whether to show tooltip when mouse is hovered on the cell.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
                 
        $("#treegrid").ejTreeGrid({  
                        showGridCellTooltip : true});

{% endhighlight %}







### showGridExpandCellTooltip<span class="type-signature type boolean">boolean</span>
{:#members:showgridexpandcelltooltip}








Specifies whether to show tooltip for the cells, which has expander button.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
                  
        $("#treegrid").ejTreeGrid({  
                        showGridExpandCellTooltip : true});

{% endhighlight %}







### sizeSettings<span class="type-signature type object">object</span>
{:#members:sizesettings}








Options for setting width and height for TreeGrid.











### sizeSettings.height<span class="type-signature type string">string</span>
{:#members:sizesettings-height}








Height of the TreeGrid.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({sizeSettings{height:'450px'}});

{% endhighlight %}







### sizeSettings.width<span class="type-signature type string">string</span>
{:#members:sizesettings-width}








Width of the TreeGrid.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({sizeSettings{width:'500px'}});

{% endhighlight %}







### sortSettings<span class="type-signature type object">object</span>
{:#members:sortsettings}








Options for sorting the rows.











### sortSettings.sortedColumns<span class="type-signature type array">array</span>
{:#members:sortsettings-sortedcolumns}








Option to add columns based on which the rows have to be sorted recursively.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
          
        $("#treegrid").ejTreeGrid({ sortSettings{sortedColumns : []}});            

{% endhighlight %}







### toolbarSettings<span class="type-signature type object">object</span>
{:#members:toolbarsettings}








Options for displaying and customizing the toolbar items.











### toolbarSettings.showToolBar<span class="type-signature type boolean">boolean</span>
{:#members:toolbarsettings-showtoolbar}








Shows/hides the toolbar.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
   
        $("#treegrid").ejTreeGrid({ showToolBar:  true });                       

{% endhighlight %}







### toolbarSettings.toolbarItems<span class="type-signature type array">array</span>
{:#members:toolbarsettings-toolbaritems}








Option to add items to the toolbar.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
        $("#treegrid").ejTreeGrid({ toolbarItems: [ej.TreeGrid.ToolbarItems.Add,ej.TreeGrid.ToolbarItems.Edit] });                       

{% endhighlight %}







### treeColumnIndex<span class="type-signature type number">number</span>
{:#members:treecolumnindex}








Specifies the index of the column that needs to have the expander button. By default, cells in the first column contain the expander button.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
         
        $("#treegrid").ejTreeGrid(
 {
    treeColumnIndex: 1
 });            

{% endhighlight %}





## Methods








### clearSelection<span class="signature">(index)</span>
{:#methods:clearselection}








To clear all the selection in treegrid

<table class="params">
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
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">you can pass a row index to clear the row selection</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.clearSelection(2);
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="treegrid"></div> 
 
<script>
// To clear the selection
$("#treegrid").ejTreeGrid("clearSelection",2);  
</script>{% endhighlight %}







### collapseAll<span class="signature">()</span>
{:#methods:collapseall}








To collapse all the parent items in tree grid





Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.collapseAll(); // To collapse all parent items in tree grid
</script>{% endhighlight %}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// To expand all items
$("#treegrid").ejTreeGrid("collapseAll");       
</script>{% endhighlight %}







### hideColumn<span class="signature">(headerText)</span>
{:#methods:hidecolumn}








To hide the column by using header text

<table class="params">
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
headerText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a header text of a column to hide</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.hideColumn("Task Name");
</script> 
</script>{% endhighlight %}







### refresh<span class="signature">(dataSource, query)</span>
{:#methods:refresh}








To refresh the changes in tree grid

<table class="params">
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
dataSource{% endhighlight %}</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass which data source you want to show in tree grid</td>
</tr>
<tr>
<td class="name">{% highlight html %}
query{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Pass which data you want to show in tree grid</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create treegrid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
var dataManager = ej.DataManager(projectData);
var query = ej.Query().select(["taskID", "taskName", "startDate", "endDate", "subtasks", "progress", "duration"]);
treegridObj.refresh(dataManager, query) // To refresh the tree grid content
</script>{% endhighlight %}







### saveCell<span class="signature">()</span>
{:#methods:savecell}








To save the edited cell in treegrid





Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.saveCell(); 
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="treegrid"></div> 
 
<script>
// Save the edited cell
$("#treegrid").ejTreeGrid("saveCell");  
</script>{% endhighlight %}







### search<span class="signature">(searchString)</span>
{:#methods:search}








To search an item with search string provided at the run time

<table class="params">
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
searchString{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a searchString to search the tree grid</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.search("Plan"); // To search a Plan string in tree grid data
</script>{% endhighlight %}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// To search a task
$("#treegrid").ejTreeGrid("search","Plan");     
</script>{% endhighlight %}







### showColumn<span class="signature">(headerText)</span>
{:#methods:showcolumn}








To show the column by using header text

<table class="params">
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
headerText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a header text of a column to show</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.showColumn("Task Name");
</script> {% endhighlight %}







### sortColumn<span class="signature">(columnName, columnSortDirection)</span>
{:#methods:sortcolumn}








To sorting the data based on the particular fields

<table class="params">
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
columnName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a name of column to sort</td>
</tr>
<tr>
<td class="name">{% highlight html %}
columnSortDirection{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a sort direction to sort the column</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.sortColumn("Start Date", ej.sortOrder.Descending); // To sort the data
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="treegrid"></div> 
 
<script>
// Sort the particular field.
$("#treegrid").ejTreeGrid("sortColumn","Start Date", ej.sortOrder.Descending);  
</script>{% endhighlight %}





## Events








### actionBegin
{:#events:actionbegin}








Triggered before every success event of Treegrid action.

<table class="params">
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
<td class="description last">Event parameters before completing the sorting operation in TreeGrid:
<table class="params">
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
columnName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
columnSortDirection{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the direction of sorting ascending or descending</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters while performing expand operation:
<table class="params">
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
keyValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of expanding parent element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters while performing collapse operation:
<table class="params">
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
keyValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of collapsing parent element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters before completing the delete operation:
<table class="params">
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
data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data or deleting element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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




Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#treegrid").ejTreeGrid({
   actionBegin: function (args) {}
});
</script>{% endhighlight %}







### actionComplete
{:#events:actioncomplete}








Triggered for every Treegrid action success event.

<table class="params">
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
<td class="description last">Event parameters when treegrid is initialized:
<table class="params">
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the grid model.</td>
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
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters after perform the sorting in grid tree is completed:
<table class="params">
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
columnName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current grouped column field name.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
columnSortDirection{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the direction of sorting ascending or descending</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters after searching completed:
<table class="params">
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
keyValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of searched element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters while performing after completing the delete operation is completed:
<table class="params">
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
data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data od deleted element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters after the add operation completed:
<table class="params">
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
data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data added element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
recordIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns selected record index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters after the edit operation completed:
<table class="params">
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
data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data added element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
recordIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns selected record index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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
 
<div id="gantt"></div> 
<script>
$("#treegrid").ejTreeGrid({
   actionComplete: function (args) {}
});
</script>{% endhighlight %}







### beginEdit
{:#events:beginedit}








Triggered while enter the edit mode in the treegrid cell

<table class="params">
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Element of editing cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of current cell record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
columnIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the column Index of cell belongs.</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   beginEdit: function (args) {}
});
</script>{% endhighlight %}







### collapsed
{:#events:collapsed}








Triggered after collapsed the TreeGrid record

<table class="params">
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
<td class="description last">Arguments when collapsed event is triggered.
<table class="params">
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
recordIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row index of collapsed record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of edited cell record..</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   collapsed: function (args) {}
});
</script>{% endhighlight %}







### collapsing
{:#events:collapsing}








Triggered while collapsing the TreeGrid record

<table class="params">
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
<td class="description last">Arguments when collapsing event is triggered.
<table class="params">
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
recordIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row index of collapsing record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of edited cell record..</td>
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
 
<div id="treegrid"></div> 
<script>
$("#TreeGrid").ejTreeGrid({
   collapsing: function (args) {}
});
</script>{% endhighlight %}







### contextMenuOpen
{:#events:contextmenuopen}








Triggered while Context Menu is rendered in TreeGrid control

<table class="params">
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
<td class="description last">Arguments when context menu is rendered.
<table class="params">
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
contextMenuItems{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the default context menu items to which we add custom items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   contextMenuOpen: function (args) {}
});
</script>{% endhighlight %}







### endEdit
{:#events:endedit}








Triggered after saved the modified cellValue in treegrid

<table class="params">
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Element of editing cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of edited cell record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
columnName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column name of edited cell belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
columnObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object of edited cell belongs.</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   endEdit: function (args) {}
});
</script>{% endhighlight %}







### expanded
{:#events:expanded}








Triggered after expand the record

<table class="params">
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
<td class="description last">Arguments when expanded event is triggered.
<table class="params">
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
recordIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row index of record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of edited cell record..</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   expanded: function (args) {}
});
</script>{% endhighlight %}







### expanding
{:#events:expanding}








Triggered while expanding the TreeGrid record

<table class="params">
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
<td class="description last">Arguments when expanding event is triggered.
<table class="params">
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
recordIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row index of record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of edited cell record..</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   expanding: function (args) {}
});
</script>{% endhighlight %}







### load
{:#events:load}








Triggered while Treegrid is loaded

<table class="params">
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model</td>
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




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   load: function (args) {}
});
</script>{% endhighlight %}







### queryCellInfo
{:#events:querycellinfo}








Triggered while rendering each cell in the treegrid

<table class="params">
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
<td class="description last">Arguments when queryCellInfo event is triggered.
<table class="params">
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
rowElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of current cell record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
column{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column of cell belongs.</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   queryCellInfo: function (args) {}
});
</script>{% endhighlight %}







### rowDataBound
{:#events:rowdatabound}








Triggered while rendering each row

<table class="params">
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
<td class="description last">Arguments when rowDataBound event is triggered.
<table class="params">
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
rowElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of edited cell record.</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowDataBound: function (args) {}
});
</script>{% endhighlight %}







### rowDrag
{:#events:rowdrag}








Triggered while dragging a row in TreeGrid control

<table class="params">
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
<td class="description last">Arguments when dragging a row.
<table class="params">
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
draggedRow{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
draggedRowIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
targetRow{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row on which we are dragging.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
targetRowIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index on which we are dragging.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
canDrop{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns that we can drop over that record or not.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowDrag: function (args) {}
});
</script>{% endhighlight %}







### rowDragStart
{:#events:rowdragstart}








Triggered while start to drag row in TreeGrid control

<table class="params">
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
<td class="description last">Arguments when drag starts.
<table class="params">
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
draggedRow{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
draggedRowIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowDragStart: function (args) {}
});
</script>{% endhighlight %}







### rowDragStop
{:#events:rowdragstop}








Triggered while drop a row in TreeGrid control

<table class="params">
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
<td class="description last">Arguments when dragging a row.
<table class="params">
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
draggedRow{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
draggedRowIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
targetRow{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row which we are dropped to row.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
targetRowIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index which we are dropped to row.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
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




Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowDragStop: function (args) {}
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
recordIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the index of selecting row record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of selected record.</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
recordIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the index of selecting row record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data selecting record.</td>
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
 
<div id="treegrid"></div> 
<script>
$("#treegrid").ejTreeGrid({
   rowSelecting: function (args) {}
});
</script>{% endhighlight %}




