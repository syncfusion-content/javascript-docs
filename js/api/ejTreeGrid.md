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

<pre class="prettyprint">
<code> 
&lt;treegrid id="treegrid"&gt;treegrid&lt;/treegrid&gt; 
 
&lt;script&gt;
// Create TreeGrid
$('#treegrid').ejTreeGrid();    
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:jquery.globalize.js


* module:jquery.easing.1.3.js


* module:jsrender.js


* module:ej.web.all.js




## Members








### allowColumnResize<span class="type-signature type boolean">boolean</span>
{:#allowcolumnresize}
{:#allowColumnResize}








Enables or disables the ability to resize column.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                   
        $("#treegrid").ejTreeGrid({ allowColumnResize:  true });                        * 
&lt;/script&gt;</code>
</pre>






### allowDragAndDrop<span class="type-signature type boolean">boolean</span>
{:#allowdraganddrop}
{:#allowDragAndDrop}








To enable drag and drop the records.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;treegrid id="treegrid"&gt;treegrid&lt;/treegrid&gt; 
 
&lt;script&gt;
        $("#treegrid").ejTreeGrid({  allowDragAndDrop : true });
&lt;/script&gt;</code>
</pre>






### allowFiltering<span class="type-signature type boolean">boolean</span>
{:#allowfiltering}
{:#allowFiltering}








Enables or disables Filtering fields column wise.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;treegrid id="treegrid"&gt;treegrid&lt;/treegrid&gt; 
 
&lt;script&gt;
        $("#treegrid").ejTreeGrid({  allowFiltering : true });
&lt;/script&gt;</code>
</pre>






### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#allowkeyboardnavigation}
{:#allowKeyboardNavigation}








Enables or Disables Keyboard navigation in treegrid




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({ allowKeyboardNavigation : true});                   
&lt;/script&gt;</code>
</pre>






### allowMultiSorting<span class="type-signature type boolean">boolean</span>
{:#allowmultisorting}
{:#allowMultiSorting}








Specifies enabling or disabling multiple sorting for tree grid columns




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({ allowMultiSorting : true});                 
&lt;/script&gt;</code>
</pre>






### allowSelection<span class="type-signature type boolean">boolean</span>
{:#allowselection}
{:#allowSelection}








Enables or disables the interactive selection of a row.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;   
        $("#treegrid").ejTreeGrid({ allowSelection:  true });                   * 
&lt;/script&gt;</code>
</pre>






### allowSorting<span class="type-signature type boolean">boolean</span>
{:#allowsorting}
{:#allowSorting}








Enables or disables sorting. When enabled, we can sort the column by clicking on the column.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;treegrid id="treegrid"&gt;treegrid&lt;/treegrid&gt; 
 
&lt;script&gt;
        $("#treegrid").ejTreeGrid({ allowSorting : true });
&lt;/script&gt;</code>
</pre>






### altRowTemplateID<span class="type-signature type string">string</span>
{:#altrowtemplateid}
{:#altRowTemplateID}








Specifies the alternate row template for each alternate TreeGrid row




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid(
 {
    altRowTemplateID: "altRowCustomTemplate"
 });            
&lt;/script&gt;</code>
</pre>






### columns<span class="type-signature type array">array</span>
{:#columns}
{:#columns}








It is to specify data values to the field.





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#treegrid").ejTreeGrid(
 {
    columns: [{ field: "Name", headerText: "Name", isTemplateColumn: true, templateID: "customColumnTemplate" },
                          { field: "Type", headerText: "Type" },
                          { field: "DateCreated", headerText: "Date Created" },
                          { field: "DateModified", headerText: "Date Modified" }]       
 });            
&lt;/script&gt;</code>
</pre>






### columns.allowFiltering<span class="type-signature type boolean">boolean</span>
{:#columns-allowfiltering}
{:#columns-allowFiltering}








Enables or disables Filtering field for particular column.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#treegrid").ejTreeGrid({ columns: [{ allowFiltering: true },{allowFiltering: false }] });
&lt;/script&gt;</code>
</pre>






### columns.allowSorting<span class="type-signature type boolean">boolean</span>
{:#columns-allowsorting}
{:#columns-allowSorting}








Enables or disables sorting for a particular column.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#treegrid").ejTreeGrid({ columns: [{ allowSorting: true },{allowSorting: false }]  });
&lt;/script&gt;</code>
</pre>






### columns.editType<span class="type-signature type string">string</span>
{:#columns-edittype}
{:#columns-editType}








Specify edit type of the column.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;  
 $("#treegrid").ejTreeGrid({columns: [{ editType: "stringedit"},{editType: "booleanedit"}]});
&lt;/script&gt;</code>
</pre>






### columns.field<span class="type-signature type string">string</span>
{:#columns-field}
{:#columns-field}








Specify column field value from the data source.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({columns: [{ field: "Name"},{field: "Type"}]});
&lt;/script&gt;</code>
</pre>






### columns.filterEditType<span class="type-signature type string">string</span>
{:#columns-filteredittype}
{:#columns-filterEditType}








Specify filter edit type of the column.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({columns: [{ filterEditType: "stringedit"},{filterEditType: "booleanedit"}]});
&lt;/script&gt;</code>
</pre>






### columns.headerText<span class="type-signature type string">string</span>
{:#columns-headertext}
{:#columns-headerText}








Specify column Header Text value to be displayed in each column.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({columns: [{ headerText: "Name"},{headerText: "Type"}]});
&lt;/script&gt;</code>
</pre>






### columns.visible<span class="type-signature type boolean">boolean</span>
{:#columns-visible}
{:#columns-visible}








Specify column field visiblity.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({columns: [{ field: "name",visible: true},{field: "Type",visible: false}]});
&lt;/script&gt;</code>
</pre>






### contextMenuSettings<span class="type-signature type object">object</span>
{:#contextmenusettings}
{:#contextMenuSettings}








Specifies the contextMenuSettings options.











### contextMenuSettings.contextMenuItems<span class="type-signature type array">array</span>
{:#contextmenusettings-contextmenuitems}
{:#contextMenuSettings-contextMenuItems}








Specifies the list of context menu items to rendered in context menu




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#treegrid").ejTreeGrid({ contextMenuItems: [ej.TreeGrid.ContextMenuItems.Add,ej.TreeGrid.ContextMenuItems.Edit] });                   
&lt;/script&gt;</code>
</pre>






### contextMenuSettings.showContextMenu<span class="type-signature type boolean">boolean</span>
{:#contextmenusettings-showcontextmenu}
{:#contextMenuSettings-showContextMenu}








Specifies the state of enabling or disabling context menu




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#treegrid").ejTreeGrid(contextMenuSettings :{ showContextMenu:  true });                      
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">string</span>
{:#cssclass}
{:#cssClass}








Specify the CSS class to achieve tree grid custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({  cssClass : "gradient-lime" });
&lt;/script&gt;</code>
</pre>






### dataSource<span class="type-signature type array">array</span>
{:#datasource}
{:#dataSource}








Collection of data or hierarchical data to represent in TreeGrid




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid(
 {
    dataSource:[{Id:2,TaskName:"Testing",startDate:"12/1/2000",Duration:5 }]    
 });            
&lt;/script&gt;</code>
</pre>






### dragTooltip<span class="type-signature type object">object</span>
{:#dragtooltip}
{:#dragTooltip}








Specifies the drag Tooltip options.











### dragTooltip.showTooltip<span class="type-signature type boolean">boolean</span>
{:#dragtooltip-showtooltip}
{:#dragTooltip-showTooltip}








Specifies whether to show tooltip while draggging a row




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid(dragTooltip :{ showTooltip:  true });
&lt;/script&gt;</code>
</pre>






### dragTooltip.tooltipItems<span class="type-signature type array">array</span>
{:#dragtooltip-tooltipitems}
{:#dragTooltip-tooltipItems}








Specifies the list of tooltip items to rendered in tooltip




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipItems: "TaskName","TaskID","StartDate" });                       
&lt;/script&gt;</code>
</pre>






### dragTooltip.tooltipTemplate<span class="type-signature type string">string</span>
{:#dragtooltip-tooltiptemplate}
{:#dragTooltip-tooltipTemplate}








Specifies the template for tooltip on mouseaction on row drag and drop




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid(dragTooltip :{ tooltipTemplate: "" });        
&lt;/script&gt;</code>
</pre>






### editSettings<span class="type-signature type object">object</span>
{:#editsettings}
{:#editSettings}








Specifies the editSettings options in treegrid.











### editSettings.allowAdding<span class="type-signature type boolean">boolean</span>
{:#editsettings-allowadding}
{:#editSettings-allowAdding}








Enables or Disables add row icon in treegrid toolbar




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowAdding : true} });
&lt;/script&gt;</code>
</pre>






### editSettings.allowDeleting<span class="type-signature type boolean">boolean</span>
{:#editsettings-allowdeleting}
{:#editSettings-allowDeleting}








Enables or disables delete row icon in toolbar




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowDeleting : true} });    
&lt;/script&gt;</code>
</pre>






### editSettings.allowEditing<span class="type-signature type boolean">boolean</span>
{:#editsettings-allowediting}
{:#editSettings-allowEditing}








Specifies the option for enabling / disablig editing in treegrid part




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({  editSettings:{allowEditing : true} });     
&lt;/script&gt;</code>
</pre>






### editSettings.editMode<span class="type-signature type string">string</span>
{:#editsettings-editmode}
{:#editSettings-editMode}








specifies the editmode in treegrid , "cellEditing" is for cell type editing and "rowEditing" is for entire row.




Default Value:
{:.param}






* cellEditing








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({  editSettings:{editMode : "cellEditing"} });
&lt;/script&gt;</code>
</pre>






### editSettings.rowPosition<span class="type-signature type string">string</span>
{:#editsettings-rowposition}
{:#editSettings-rowPosition}








Specifies the position where have to add new row.




Default Value:
{:.param}






* top








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;   
 $("#treegrid").ejTreeGrid({  editSettings:{rowPosition : "aboveSelectedRow"} });
&lt;/script&gt;</code>
</pre>






### enableAltRow<span class="type-signature type boolean">boolean</span>
{:#enablealtrow}
{:#enableAltRow}








Enables or Disables enableAltRow row effect in TreeGrid




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({ enableAltRow : false});                     
&lt;/script&gt;</code>
</pre>






### enableCollapseAll<span class="type-signature type boolean">boolean</span>
{:#enablecollapseall}
{:#enableCollapseAll}








Enables or disables the collapse all menus for tree grid , when enabled all sub menus will disappears in tree grid




Default Value:
{:.param}






* "false"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid(
 {
    enableCollapseAll: false
 });            
&lt;/script&gt;</code>
</pre>






### enableResize<span class="type-signature type boolean">boolean</span>
{:#enableresize}
{:#enableResize}








Specify the enableResize to tree grid.




Default Value:
{:.param}






* "false"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({enableResize:true});
&lt;/script&gt;</code>
</pre>






### enableVirtualization<span class="type-signature type boolean">boolean</span>
{:#enablevirtualization}
{:#enableVirtualization}








Enables or Disables virtualization for rendering TreeGrid items.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({ enableVirtualization : true});                      
&lt;/script&gt;</code>
</pre>






### filterBarMode<span class="type-signature type enum">enum</span>
{:#filterbarmode}
{:#filterBarMode}








To change filterBarMode either immediate or onEnter.




Default Value:
{:.param}






* immediate








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#treegrid").ejTreeGrid({  filterBarMode : "onEnter" });
&lt;/script&gt;</code>
</pre>






### idMapping<span class="type-signature type string">string</span>
{:#idmapping}
{:#idMapping}








Specifies the mapping property path for child Id in self reference datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({  IdMapping : "ID" });                   
&lt;/script&gt;</code>
</pre>






### parentIdMapping<span class="type-signature type string">string</span>
{:#parentidmapping}
{:#parentIdMapping}








Specifies the mapping property path for parent Id in self reference datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({  parentIdMapping : "ID" });             
&lt;/script&gt;</code>
</pre>






### query<span class="type-signature type object">object</span>
{:#query}
{:#query}








It receives query to retrieve data from the table (query is same as SQL).




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#treegrid").ejTreeGrid(
 {
    query:ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);      
 });            
&lt;/script&gt;</code>
</pre>






### rowHeight<span class="type-signature type number">number</span>
{:#rowheight}
{:#rowHeight}








Specifies the height of a single row in treegrid. Also, we need to set same height in the CSS style with class name e-rowcell.




Default Value:
{:.param}






* "30"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#treegrid").ejTreeGrid({  
                        rowHeight : 30,
                        });
&lt;/script&gt;</code>
</pre>






### rowTemplateID<span class="type-signature type string">string</span>
{:#rowtemplateid}
{:#rowTemplateID}








Specifies the row template for each TreeGrid row




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid(
 {
    rowTemplateID: "customTemplate"
 });            
&lt;/script&gt;</code>
</pre>






### selectedItem<span class="type-signature type numeric">numeric</span>
{:#selecteditem}
{:#selectedItem}








Specifies the selected row index.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({ selectedItem : 2});                 
&lt;/script&gt;</code>
</pre>






### selectedRowIndex<span class="type-signature type number">number</span>
{:#selectedrowindex}
{:#selectedRowIndex}








Specifies the selected row Index in Treegrid , the row with given index is highlighted




Default Value:
{:.param}






* "-1"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid(
 {
    selectedRowIndex:2
 });            
&lt;/script&gt;</code>
</pre>






### selectionType<span class="type-signature type string">string</span>
{:#selectiontype}
{:#selectionType}








Specifes the single or multiple row selection




Default Value:
{:.param}






* "single"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({ selectionType:"multiple" });                   
&lt;/script&gt;</code>
</pre>






### showColumnChooser<span class="type-signature type boolean">boolean</span>
{:#showcolumnchooser}
{:#showColumnChooser}








Enables or disables the column chooser.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;   
        $("#treegrid").ejTreeGrid({ showColumnChooser:  true });                        * 
&lt;/script&gt;</code>
</pre>






### showGridCellTooltip<span class="type-signature type boolean">boolean</span>
{:#showgridcelltooltip}
{:#showGridCellTooltip}








Specifies whether to show grid cell tooltip.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({  
                        showGridCellTooltip : true});
&lt;/script&gt;</code>
</pre>






### showGridExpandCellTooltip<span class="type-signature type boolean">boolean</span>
{:#showgridexpandcelltooltip}
{:#showGridExpandCellTooltip}








Specifies whether to show grid cell tooltip over expander cell alone.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#treegrid").ejTreeGrid({  
                        showGridExpandCellTooltip : true});
&lt;/script&gt;</code>
</pre>






### sizeSettings<span class="type-signature type object">object</span>
{:#sizesettings}
{:#sizeSettings}








Specifies the size options for Treegrid.











### sizeSettings.height<span class="type-signature type string">string</span>
{:#sizesettings-height}
{:#sizeSettings-height}








Specify the height to tree grid.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({sizeSettings{height:'450px'}});
&lt;/script&gt;</code>
</pre>






### sizeSettings.width<span class="type-signature type string">string</span>
{:#sizesettings-width}
{:#sizeSettings-width}








Specify the width to tree grid.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({sizeSettings{width:'500px'}});
&lt;/script&gt;</code>
</pre>






### sortSettings<span class="type-signature type object">object</span>
{:#sortsettings}
{:#sortSettings}








Specifes the sorting options for Treegrid.











### sortSettings.sortedColumns<span class="type-signature type array">array</span>
{:#sortsettings-sortedcolumns}
{:#sortSettings-sortedColumns}








Specifes the sorted columns for Tree grid




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid({ sortSettings{sortedColumns : []}});            
&lt;/script&gt;</code>
</pre>






### toolbarSettings<span class="type-signature type object">object</span>
{:#toolbarsettings}
{:#toolbarSettings}








Specifies the toolbarSettings options.











### toolbarSettings.showToolBar<span class="type-signature type boolean">boolean</span>
{:#toolbarsettings-showtoolbar}
{:#toolbarSettings-showToolBar}








Specifies the state of enabling or disabling toolbar




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#treegrid").ejTreeGrid({ showToolBar:  true });                       
&lt;/script&gt;</code>
</pre>






### toolbarSettings.toolbarItems<span class="type-signature type array">array</span>
{:#toolbarsettings-toolbaritems}
{:#toolbarSettings-toolbarItems}








Specifies the list of toolbar items to rendered in toolbar




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#treegrid").ejTreeGrid({ toolbarItems: [ej.TreeGrid.ToolbarItems.Add,ej.TreeGrid.ToolbarItems.Edit] });                       
&lt;/script&gt;</code>
</pre>






### treeColumnIndex<span class="type-signature type number">number</span>
{:#treecolumnindex}
{:#treeColumnIndex}








Specifies the tree expander column index in tree grid




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#treegrid").ejTreeGrid(
 {
    treeColumnIndex: 1
 });            
&lt;/script&gt;</code>
</pre>




## Methods








### clearSelection<span class="signature">(index)</span>
{:#clearselection}
{:#clearSelection}








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
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">you can pass a row index to clear the row selection</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.clearSelection(2);
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To clear the selection
$("#treegrid").ejTreeGrid("clearSelection",2);  
&lt;/script&gt;</code>
</pre>






### collapseAll<span class="signature">()</span>
{:#collapseall}
{:#collapseAll}








To collapse all the parent items in tree grid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.collapseAll(); // To collapse all parent items in tree grid
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To expand all items
$("#treegrid").ejTreeGrid("collapseAll");       
&lt;/script&gt;</code>
</pre>






### hideColumn<span class="signature">(headerText)</span>
{:#hidecolumn}
{:#hideColumn}








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
<td class="name"><code>headerText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a header text of a column to hide</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.hideColumn("Task Name");
&lt;/script&gt; 
&lt;/script&gt;</code>
</pre>






### refresh<span class="signature">(dataSource, query)</span>
{:#refresh}
{:#refresh}








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
<td class="name"><code>dataSource</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Pass which data source you want to show in tree grid</td>
</tr>
<tr>
<td class="name"><code>query</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Pass which data you want to show in tree grid</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create treegrid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
var dataManager = ej.DataManager(projectData);
var query = ej.Query().select(["taskID", "taskName", "startDate", "endDate", "subtasks", "progress", "duration"]);
treegridObj.refresh(dataManager, query) // To refresh the tree grid content
&lt;/script&gt;</code>
</pre>






### saveCell<span class="signature">()</span>
{:#savecell}
{:#saveCell}








To save the edited cell in treegrid





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.saveCell(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Save the edited cell
$("#treegrid").ejTreeGrid("saveCell");  
&lt;/script&gt;</code>
</pre>






### search<span class="signature">(searchString)</span>
{:#search}
{:#search}








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
<td class="name"><code>searchString</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a searchString to search the tree grid</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.search("Plan"); // To search a Plan string in tree grid data
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To search a task
$("#treegrid").ejTreeGrid("search","Plan");     
&lt;/script&gt;</code>
</pre>






### showColumn<span class="signature">(headerText)</span>
{:#showcolumn}
{:#showColumn}








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
<td class="name"><code>headerText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a header text of a column to show</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.showColumn("Task Name");
&lt;/script&gt; </code>
</pre>






### sortColumn<span class="signature">(columnName, columnSortDirection)</span>
{:#sortcolumn}
{:#sortColumn}








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
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a name of column to sort</td>
</tr>
<tr>
<td class="name"><code>columnSortDirection</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a sort direction to sort the column</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Tree Grid object
var treegridObj = $("#treegrid").data("ejTreeGrid");
treegridObj.sortColumn("Start Date", ej.sortOrder.Descending); // To sort the data
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="treegrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Sort the particular field.
$("#treegrid").ejTreeGrid("sortColumn","Start Date", ej.sortOrder.Descending);  
&lt;/script&gt;</code>
</pre>




## Events








### actionBegin
{:#actionbegin}
{:#actionBegin}








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
<td class="name"><code>argument</code></td>
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
<td class="description last">Returns the treegrid model.</td>
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
<td class="description last">Returns the direction of sorting ascending or descending</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>keyValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of expanding parent element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>keyValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of collapsing parent element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data or deleting element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   actionBegin: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### actionComplete
{:#actioncomplete}
{:#actionComplete}








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
<td class="name"><code>argument</code></td>
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
<td class="description last">Returns the treegrid model.</td>
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
<td class="description last">Returns the direction of sorting ascending or descending</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>keyValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of searched element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data od deleted element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data added element.</td>
</tr>
<tr>
<td class="name"><code>recordIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns selected record index</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data added element.</td>
</tr>
<tr>
<td class="name"><code>recordIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns selected record index</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   actionComplete: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### beginEdit
{:#beginedit}
{:#beginEdit}








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
<td class="name"><code>rowElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name"><code>cellElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Element of editing cell.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of current cell record.</td>
</tr>
<tr>
<td class="name"><code>columnIndex</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   beginEdit: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### collapsed
{:#collapsed}
{:#collapsed}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>recordIndex</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row index of collapsed record.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   collapsed: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### collapsing
{:#collapsing}
{:#collapsing}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>recordIndex</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row index of collapsing record.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#TreeGrid").ejTreeGrid({
   collapsing: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### contextMenuOpen
{:#contextmenuopen}
{:#contextMenuOpen}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>contextMenuItems</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the default context menu items to which we add custom items.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   contextMenuOpen: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### endEdit
{:#endedit}
{:#endEdit}








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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>rowElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name"><code>cellElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Element of editing cell.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of edited cell record.</td>
</tr>
<tr>
<td class="name"><code>columnName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the column name of edited cell belongs.</td>
</tr>
<tr>
<td class="name"><code>columnObject</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   endEdit: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### expanded
{:#expanded}
{:#expanded}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>recordIndex</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row index of record.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   expanded: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### expanding
{:#expanding}
{:#expanding}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>recordIndex</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row index of record.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   expanding: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### load
{:#load}
{:#load}








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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model</td>
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
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   load: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### queryCellInfo
{:#querycellinfo}
{:#queryCellInfo}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>rowElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name"><code>cellValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of cell.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of current cell record.</td>
</tr>
<tr>
<td class="name"><code>column</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   queryCellInfo: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowDataBound
{:#rowdatabound}
{:#rowDataBound}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>rowElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row element of editing cell.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   rowDataBound: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowDrag
{:#rowdrag}
{:#rowDrag}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>draggedRow</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name"><code>draggedRowIndex</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name"><code>targetRow</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row on which we are dragging.</td>
</tr>
<tr>
<td class="name"><code>targetRowIndex</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index on which we are dragging.</td>
</tr>
<tr>
<td class="name"><code>canDrop</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns that we can drop over that record or not.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   rowDrag: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowDragStart
{:#rowdragstart}
{:#rowDragStart}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>draggedRow</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name"><code>draggedRowIndex</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   rowDragStart: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowDragStop
{:#rowdragstop}
{:#rowDragStop}








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>draggedRow</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row which we start to drag.</td>
</tr>
<tr>
<td class="name"><code>draggedRowIndex</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index which we start to drag.</td>
</tr>
<tr>
<td class="name"><code>targetRow</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row which we are dropped to row.</td>
</tr>
<tr>
<td class="name"><code>targetRowIndex</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the row index which we are dropped to row.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the treegrid model.</td>
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
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   rowDragStop: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowSelected
{:#rowselected}
{:#rowSelected}








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
<td class="name"><code>rowElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name"><code>recordIndex</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the index of selecting row record.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   rowSelected: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowSelecting
{:#rowselecting}
{:#rowSelecting}








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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>rowElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selecting row element.</td>
</tr>
<tr>
<td class="name"><code>recordIndex</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the index of selecting row record.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="treegrid"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#treegrid").ejTreeGrid({
   rowSelecting: function (args) {}
});
&lt;/script&gt;</code>
</pre>



