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








Enables or disables the ability to resize column.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                   
        $("#treegrid").ejTreeGrid({ allowColumnResize:  true });                        * 
</script>{% endhighlight %}







### allowDragAndDrop<span class="type-signature type boolean">boolean</span>
{:#members:allowdraganddrop}








To enable drag and drop the records.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<treegrid id="treegrid">treegrid</treegrid> 
 
<script>
        $("#treegrid").ejTreeGrid({  allowDragAndDrop : true });
</script>{% endhighlight %}







### allowFiltering<span class="type-signature type boolean">boolean</span>
{:#members:allowfiltering}








Enables or disables Filtering fields column wise.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<treegrid id="treegrid">treegrid</treegrid> 
 
<script>
        $("#treegrid").ejTreeGrid({  allowFiltering : true });
</script>{% endhighlight %}







### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members:allowkeyboardnavigation}








Enables or Disables Keyboard navigation in treegrid




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({ allowKeyboardNavigation : true});                   
</script>{% endhighlight %}







### allowMultiSorting<span class="type-signature type boolean">boolean</span>
{:#members:allowmultisorting}








Specifies enabling or disabling multiple sorting for tree grid columns




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({ allowMultiSorting : true});                 
</script>{% endhighlight %}







### allowSelection<span class="type-signature type boolean">boolean</span>
{:#members:allowselection}








Enables or disables the interactive selection of a row.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>   
        $("#treegrid").ejTreeGrid({ allowSelection:  true });                   * 
</script>{% endhighlight %}







### allowSorting<span class="type-signature type boolean">boolean</span>
{:#members:allowsorting}








Enables or disables sorting. When enabled, we can sort the column by clicking on the column.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<treegrid id="treegrid">treegrid</treegrid> 
 
<script>
        $("#treegrid").ejTreeGrid({ allowSorting : true });
</script>{% endhighlight %}







### altRowTemplateID<span class="type-signature type string">string</span>
{:#members:altrowtemplateid}








Specifies the alternate row template for each alternate TreeGrid row




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid(
 {
    altRowTemplateID: "altRowCustomTemplate"
 });            
</script>{% endhighlight %}







### columns<span class="type-signature type array">array</span>
{:#members:columns}








It is to specify data values to the field.





Example
{:.example}


{% highlight html %}
<div id="treegrid"></div> 
<script>                          
        $("#treegrid").ejTreeGrid(
 {
    columns: [{ field: "Name", headerText: "Name", isTemplateColumn: true, templateID: "customColumnTemplate" },
                          { field: "Type", headerText: "Type" },
                          { field: "DateCreated", headerText: "Date Created" },
                          { field: "DateModified", headerText: "Date Modified" }]       
 });            
</script>{% endhighlight %}







### columns.allowFiltering<span class="type-signature type boolean">boolean</span>
{:#members:columns-allowfiltering}








Enables or disables Filtering field for particular column.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
        $("#treegrid").ejTreeGrid({ columns: [{ allowFiltering: true },{allowFiltering: false }] });
</script>{% endhighlight %}







### columns.allowSorting<span class="type-signature type boolean">boolean</span>
{:#members:columns-allowsorting}








Enables or disables sorting for a particular column.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
        $("#treegrid").ejTreeGrid({ columns: [{ allowSorting: true },{allowSorting: false }]  });
</script>{% endhighlight %}







### columns.editType<span class="type-signature type string">string</span>
{:#members:columns-edittype}








Specify edit type of the column.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>  
 $("#treegrid").ejTreeGrid({columns: [{ editType: "stringedit"},{editType: "booleanedit"}]});
</script>{% endhighlight %}







### columns.field<span class="type-signature type string">string</span>
{:#members:columns-field}








Specify column field value from the data source.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({columns: [{ field: "Name"},{field: "Type"}]});
</script>{% endhighlight %}







### columns.filterEditType<span class="type-signature type string">string</span>
{:#members:columns-filteredittype}








Specify filter edit type of the column.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({columns: [{ filterEditType: "stringedit"},{filterEditType: "booleanedit"}]});
</script>{% endhighlight %}







### columns.headerText<span class="type-signature type string">string</span>
{:#members:columns-headertext}








Specify column Header Text value to be displayed in each column.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({columns: [{ headerText: "Name"},{headerText: "Type"}]});
</script>{% endhighlight %}







### columns.visible<span class="type-signature type boolean">boolean</span>
{:#members:columns-visible}








Specify column field visiblity.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({columns: [{ field: "name",visible: true},{field: "Type",visible: false}]});
</script>{% endhighlight %}







### contextMenuSettings<span class="type-signature type object">object</span>
{:#members:contextmenusettings}








Specifies the contextMenuSettings options.











### contextMenuSettings.contextMenuItems<span class="type-signature type array">array</span>
{:#members:contextmenusettings-contextmenuitems}








Specifies the list of context menu items to rendered in context menu




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>  
        $("#treegrid").ejTreeGrid({ contextMenuItems: [ej.TreeGrid.ContextMenuItems.Add,ej.TreeGrid.ContextMenuItems.Edit] });                   
</script>{% endhighlight %}







### contextMenuSettings.showContextMenu<span class="type-signature type boolean">boolean</span>
{:#members:contextmenusettings-showcontextmenu}








Specifies the state of enabling or disabling context menu




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>  
        $("#treegrid").ejTreeGrid(contextMenuSettings :{ showContextMenu:  true });                      
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Specify the CSS class to achieve tree grid custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({  cssClass : "gradient-lime" });
</script>{% endhighlight %}







### dataSource<span class="type-signature type array">array</span>
{:#members:datasource}








Collection of data or hierarchical data to represent in TreeGrid




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid(
 {
    dataSource:[{Id:2,TaskName:"Testing",startDate:"12/1/2000",Duration:5 }]    
 });            
</script>{% endhighlight %}







### dragTooltip<span class="type-signature type object">object</span>
{:#members:dragtooltip}








Specifies the drag Tooltip options.











### dragTooltip.showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:dragtooltip-showtooltip}








Specifies whether to show tooltip while draggging a row




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid(dragTooltip :{ showTooltip:  true });
</script>{% endhighlight %}







### dragTooltip.tooltipItems<span class="type-signature type array">array</span>
{:#members:dragtooltip-tooltipitems}








Specifies the list of tooltip items to rendered in tooltip




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>  
        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipItems: "TaskName","TaskID","StartDate" });                       
</script>{% endhighlight %}







### dragTooltip.tooltipTemplate<span class="type-signature type string">string</span>
{:#members:dragtooltip-tooltiptemplate}








Specifies the template for tooltip on mouseaction on row drag and drop




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipTemplate: "" });        
</script>{% endhighlight %}







### editSettings<span class="type-signature type object">object</span>
{:#members:editsettings}








Specifies the editSettings options in treegrid.











### editSettings.allowAdding<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowadding}








Enables or Disables add row icon in treegrid toolbar




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowAdding : true} });
</script>{% endhighlight %}







### editSettings.allowDeleting<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowdeleting}








Enables or disables delete row icon in toolbar




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowDeleting : true} });    
</script>{% endhighlight %}







### editSettings.allowEditing<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowediting}








Specifies the option for enabling / disablig editing in treegrid part




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowEditing : true} });     
</script>{% endhighlight %}







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








Specifies the position where have to add new row.




Default Value:
{:.param}






* top








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>   
 $("#treegrid").ejTreeGrid({  editSettings:{rowPosition : "aboveSelectedRow"} });
</script>{% endhighlight %}







### enableAltRow<span class="type-signature type boolean">boolean</span>
{:#members:enablealtrow}








Enables or Disables enableAltRow row effect in TreeGrid




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({ enableAltRow : false});                     
</script>{% endhighlight %}







### enableCollapseAll<span class="type-signature type boolean">boolean</span>
{:#members:enablecollapseall}








Enables or disables the collapse all menus for tree grid , when enabled all sub menus will disappears in tree grid




Default Value:
{:.param}






* "false"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid(
 {
    enableCollapseAll: false
 });            
</script>{% endhighlight %}







### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}








Specify the enableResize to tree grid.




Default Value:
{:.param}






* "false"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({enableResize:true});
</script>{% endhighlight %}







### enableVirtualization<span class="type-signature type boolean">boolean</span>
{:#members:enablevirtualization}








Enables or Disables virtualization for rendering TreeGrid items.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({ enableVirtualization : true});                      
</script>{% endhighlight %}







### filterBarMode<span class="type-signature type enum">enum</span>
{:#members:filterbarmode}








To change filterBarMode either immediate or onEnter.




Default Value:
{:.param}






* immediate








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
 
<script>
        $("#treegrid").ejTreeGrid({  filterBarMode : "onEnter" });
</script>{% endhighlight %}







### idMapping<span class="type-signature type string">string</span>
{:#members:idmapping}








Specifies the mapping property path for child Id in self reference datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  IdMapping : "ID" });                   
</script>{% endhighlight %}







### parentIdMapping<span class="type-signature type string">string</span>
{:#members:parentidmapping}








Specifies the mapping property path for parent Id in self reference datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  parentIdMapping : "ID" });             
</script>{% endhighlight %}







### query<span class="type-signature type object">object</span>
{:#members:query}








It receives query to retrieve data from the table (query is same as SQL).




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="treegrid"></div> 
<script>                          
        $("#treegrid").ejTreeGrid(
 {
    query:ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);      
 });            
</script>{% endhighlight %}







### rowHeight<span class="type-signature type number">number</span>
{:#members:rowheight}








Specifies the height of a single row in treegrid. Also, we need to set same height in the CSS style with class name e-rowcell.




Default Value:
{:.param}






* "30"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                          
        $("#treegrid").ejTreeGrid({  
                        rowHeight : 30,
                        });
</script>{% endhighlight %}







### rowTemplateID<span class="type-signature type string">string</span>
{:#members:rowtemplateid}








Specifies the row template for each TreeGrid row




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid(
 {
    rowTemplateID: "customTemplate"
 });            
</script>{% endhighlight %}







### selectedItem<span class="type-signature type numeric">numeric</span>
{:#members:selecteditem}








Specifies the selected row index.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({ selectedItem : 2});                 
</script>{% endhighlight %}







### selectedRowIndex<span class="type-signature type number">number</span>
{:#members:selectedrowindex}








Specifies the selected row Index in Treegrid , the row with given index is highlighted




Default Value:
{:.param}






* "-1"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid(
 {
    selectedRowIndex:2
 });            
</script>{% endhighlight %}







### selectionType<span class="type-signature type string">string</span>
{:#members:selectiontype}








Specifes the single or multiple row selection




Default Value:
{:.param}






* "single"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({ selectionType:"multiple" });                   
</script>{% endhighlight %}







### showColumnChooser<span class="type-signature type boolean">boolean</span>
{:#members:showcolumnchooser}








Enables or disables the column chooser.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>   
        $("#treegrid").ejTreeGrid({ showColumnChooser:  true });                        * 
</script>{% endhighlight %}







### showGridCellTooltip<span class="type-signature type boolean">boolean</span>
{:#members:showgridcelltooltip}








Specifies whether to show grid cell tooltip.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  
                        showGridCellTooltip : true});
</script>{% endhighlight %}







### showGridExpandCellTooltip<span class="type-signature type boolean">boolean</span>
{:#members:showgridexpandcelltooltip}








Specifies whether to show grid cell tooltip over expander cell alone.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>                  
        $("#treegrid").ejTreeGrid({  
                        showGridExpandCellTooltip : true});
</script>{% endhighlight %}







### sizeSettings<span class="type-signature type object">object</span>
{:#members:sizesettings}








Specifies the size options for Treegrid.











### sizeSettings.height<span class="type-signature type string">string</span>
{:#members:sizesettings-height}








Specify the height to tree grid.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({sizeSettings{height:'450px'}});
</script>{% endhighlight %}







### sizeSettings.width<span class="type-signature type string">string</span>
{:#members:sizesettings-width}








Specify the width to tree grid.




Default Value:
{:.param}






* "null"








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({sizeSettings{width:'500px'}});
</script>{% endhighlight %}







### sortSettings<span class="type-signature type object">object</span>
{:#members:sortsettings}








Specifes the sorting options for Treegrid.











### sortSettings.sortedColumns<span class="type-signature type array">array</span>
{:#members:sortsettings-sortedcolumns}








Specifes the sorted columns for Tree grid




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid({ sortSettings{sortedColumns : []}});            
</script>{% endhighlight %}







### toolbarSettings<span class="type-signature type object">object</span>
{:#members:toolbarsettings}








Specifies the toolbarSettings options.











### toolbarSettings.showToolBar<span class="type-signature type boolean">boolean</span>
{:#members:toolbarsettings-showtoolbar}








Specifies the state of enabling or disabling toolbar




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>  
        $("#treegrid").ejTreeGrid({ showToolBar:  true });                       
</script>{% endhighlight %}







### toolbarSettings.toolbarItems<span class="type-signature type array">array</span>
{:#members:toolbarsettings-toolbaritems}








Specifies the list of toolbar items to rendered in toolbar




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>  
        $("#treegrid").ejTreeGrid({ toolbarItems: [ej.TreeGrid.ToolbarItems.Add,ej.TreeGrid.ToolbarItems.Edit] });                       
</script>{% endhighlight %}







### treeColumnIndex<span class="type-signature type number">number</span>
{:#members:treecolumnindex}








Specifies the tree expander column index in tree grid




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="treegrid"></div> 
<script>          
        $("#treegrid").ejTreeGrid(
 {
    treeColumnIndex: 1
 });            
</script>{% endhighlight %}





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




