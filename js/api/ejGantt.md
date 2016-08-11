---
layout: post
title: Properties, Methods and Events of ejGantt Widget
description: Methods, members, events available in ejGantt
documentation: API
platform: js
keywords: ejGantt, API, Essential JS Gantt
---

# ejGantt.

The Essential JavaScript Gantt control is designed to visualize and edit the project schedule, and track the project progress. 


#### Syntax

{% highlight javascript %}

$(element).ejGantt();

{% endhighlight %}

$(element).ejGantt<span class="signature">()</span>

#### Example
{:.example}


{% highlight html %}
 
<gantt id="gantt">Gantt</gantt> 
 
<script>
// Create Gantt
$('#gantt').ejGantt();  
</script>

{% endhighlight %}


#### Requires
{:.require}

* module:jQuery
* module:jquery.globalize.js
* module:jquery.easing.1.3.js
* module:jsrender.js
* module:ej.web.all.js


## Members

### addDialogFields `Array`
{:#members:adddialogfields}

Specifies the fields to be included in the add dialog in Gantt


#### Default Value:
{:.param}

* []


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    addDialogFields: [{ field: "taskId", editType: "stringedit" }]
 });            
</script>

{% endhighlight %}


### allowColumnResize `boolean`
{:#members:allowcolumnresize}

Enables or disables the ability to resize column.


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                   
        $("#gantt").ejGantt({ allowColumnResize:  true });                      * 
</script>

{% endhighlight %}


### allowGanttChartEditing `boolean`
{:#members:allowganttchartediting}

Enables or Disables Gantt chart editing in Gantt


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    allowGanttChartEditing:true
 });            
</script>

{% endhighlight %}


### allowKeyboardNavigation `boolean`
{:#members:allowkeyboardnavigation}

Enables or Disables Keyboard navigation in Gantt


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ allowKeyboardNavigation : true});                 
</script>

{% endhighlight %}


### allowMultiSorting `boolean`
{:#members:allowmultisorting}

Specifies enabling or disabling multiple sorting for Gantt columns


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ allowMultiSorting : true});                       
</script>

{% endhighlight %}


### allowSelection `boolean`
{:#members:allowselection}

Enables or disables the interactive selection of a row.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>   
        $("#gantt").ejGantt({ allowSelection:  true });                 * 
</script>

{% endhighlight %}


### allowSorting `boolean`
{:#members:allowsorting}

Enables or disables sorting. When enabled, we can sort the column by clicking on the column.


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>        
        $("#gantt").ejGantt({ allowSorting:  true });            
</script>

{% endhighlight %}


### allowDragAndDrop `boolean`
{:#members:allowdraganddrop}

Enables or disables the ability to drag and drop the row interactively to reorder the rows


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>        
        $("#gantt").ejGantt({ allowDragAndDrop:  true });            
</script>

{% endhighlight %}


### enablePredecessorValidation `boolean`
{:#members:enablepredecessorvalidation}

Enable or disable predecessor validation. When it is true, all the task's start and end dates are aligned based on its predecessors start and end dates.

#### Default Value:
{:.param}

* true

#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>        
        $("#gantt").ejGantt({ enablePredecessorValidation:  false });            
</script>

{% endhighlight %}


### baselineColor `string`
{:#members:baselinecolor}

Specifies the baseline background color in Gantt


#### Default Value:
{:.param}

* "#fba41c"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt(
 {
    baselineColor: "blue"
 });            
</script>

{% endhighlight %}


### baselineEndDateMapping `string`
{:#members:baselineenddatemapping}

Specifies the mapping property path for baseline end date in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  baselineEndDateMapping : "BaselineEndDate" });
</script>

{% endhighlight %}


### baselineStartDateMapping `string`
{:#members:baselinestartdatemapping}

Specifies the mapping property path for baseline start date of a task in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  baselineStartDateMapping : "BaselineStartDate" });               
</script>

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
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  childMapping : "Children" });
</script>

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
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ columnDialogFields: ["field", "headerText", "editType", "width", "visible", "allowSorting", "textAlign", "headerTextAlign"] });                   
</script>

{% endhighlight %}

### connectorLineBackground `string`
{:#members:connectorlinebackground}

Specifies the background of connector lines in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        connectorLineBackground : "#F2F2F2"});
</script>

{% endhighlight %}


### connectorlineWidth `number`
{:#members:connectorlinewidth}

Specifies the width of the connector lines in Gantt


#### Default Value:
{:.param}

* 1


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        connectorlineWidth : 1 });
</script>

{% endhighlight %}


### cssClass `string`
{:#members:cssclass}

Specify the CSS class for Gantt to achieve custom theme.


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  cssClass : "gradient-lime" });
</script>

{% endhighlight %}


### dragTooltip `object`
{:#members:dragtooltip}

Option for customizing the drag tooltip while reordering the rows.


### dragTooltip.showTooltip `boolean`
{:#members:dragtooltip-showtooltip}

Specifies option to enable/disable tooltip while drag and drop a row.


#### Default Value

* true


#### Example


{% highlight html %}

<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  dragTooltip : { showTooltip:  true } });
</script>
{% endhighlight %}


### dragTooltip.tooltipItems `array`
{:#members:dragtooltip-tooltipitems}

Specifies the data source fields to be displayed in the drag tooltip.


#### Default Value

* []


#### Example


{% highlight html %}
                    
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  dragTooltip : { tooltipItems: "TaskName","TaskID","StartDate" } });
</script>

{% endhighlight %}


### dragTooltip.tooltipTemplate `string`
{:#members:dragtooltip-tooltiptemplate}

Specifies the custom template for drag tooltip.


#### Default Value

* null


#### Example

{% highlight html %}               
                    
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  dragTooltip : { tooltipTemplate: "" } });
</script>
{% endhighlight %}

### dataSource `array`
{:#members:datasource}

Collection of data or hierarchical data to represent in Gantt


#### Default Value:
{:.param}

* null


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    dataSource:[{Id:2,TaskName:"Testing",startDate:"12/1/2000",Duration:5 }]    
 });            
</script>

{% endhighlight %}

### dateFormat `string`
{:#members:dateformat}

Specifies the dateFormat for Gantt , given format is displayed in tooltip , Grid .


#### Default Value:
{:.param}

* "MM/dd/yyyy"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    dateFormat: "dd/MM/yyyy"
 });            
</script>

{% endhighlight %}


### durationMapping `string`
{:#members:durationmapping}

Specifies the mapping property path for duration of a task in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  durationMapping : "Duration" });
</script>

{% endhighlight %}


### durationUnit `enum`
{:#members:durationunit}

<ts name = "ej.Gantt.DurationUnit"/>

Specifies the duration unit for each tasks whether days or hours or minutes

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Day</td>
<td class="description">Sets the Duration Unit as day.</td>
</tr>
<tr>
<td class="name">Hour</td>
<td class="description">Sets the Duration Unit as hour.</td>
</tr>
<tr>
<td class="name">Minute</td>
<td class="description">Sets the Duration Unit as minute.</td>
</tr>
</tbody>
</table>

#### Default Value:
{:.param}

* ej.Gantt.DurationUnit.Day


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        durationUnit : ej.Gantt.DurationUnit.Hour });
</script>

{% endhighlight %}


### editDialogFields `Array`
{:#members:editdialogfields}

Specifies the fields to be included in the edit dialog in Gantt


#### Default Value:
{:.param}

* []


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    editDialogFields: [{ field: "taskId", editType: "stringedit" }]
 });            
</script>

{% endhighlight %}

### splitterSettings `object`
{:#members:splittersettings}

Option to configure the splitter position.


### splitterSettings.position `string`
{:#members:splittersettings-position}

Specifies position of the splitter in Gantt , splitter can be placed either based on percentage values or pixel values.

#### Default Value:
{:.param}

* ""

#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  splitterSettings:{position : "300px"} });
</script>

{% endhighlight %}


### splitterSettings.index `string`
{:#members:splittersettings-index}

Specifies the position of splitter in Gantt, based on column index in Gantt.

#### Default Value:
{:.param}

* ""

#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  splitterSettings:{index : "3"} });
</script>

{% endhighlight %}



### editSettings `object`
{:#members:editsettings}

Specifies the editSettings options in Gantt.


### editSettings.allowAdding `boolean`
{:#members:editsettings-allowadding}

Enables or disables add record icon in Gantt toolbar


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{allowAdding : true} });
</script>

{% endhighlight %}


### editSettings.allowDeleting `boolean`
{:#members:editsettings-allowdeleting}

Enables or disables delete icon in Gantt toolbar


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{allowDeleting : true} });  
</script>

{% endhighlight %}


### editSettings.allowEditing `boolean`
{:#members:editsettings-allowediting}

Specifies the option for enabling or disabling editing in Gantt grid part


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{allowEditing : true} });   
</script>

{% endhighlight %}

### editSettings.allowIndent `boolean`
{:#members:editsettings-allowindent}

Specifies the option for enabling or disabling indent action in Gantt.


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{allowIndent : true} });   
</script>

{% endhighlight %}

### editSettings.allowOutdent `boolean`
{:#members:editsettings-allowoutdent}

Specifies the option for enabling or disabling outdent action in Gantt

#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{allowOutdent : true} });   
</script>

{% endhighlight %}


### editSettings.editMode `string`
{:#members:editsettings-editmode}

Specifies the edit mode in Gantt, "normal" is for dialog editing ,"cellEditing" is for cell type editing


#### Default Value:
{:.param}

* normal


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{editMode : "normal"} });
</script>

{% endhighlight %}

### enableAltRow `boolean`
{:#members:enablealtrow}

Enables or Disables enableAltRow row effect in Gantt


#### Default Value:
{:.param}

* true

#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ enableAltRow : true});                    
</script>

{% endhighlight %}


### enableWBS `boolean`
{:#members:enablewbs}

Enables/disables work breakdown structure column. 


#### Default Value:
{:.param}

* false

#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ enableWBS : true});                    
</script>

{% endhighlight %}

### enableWBSPredecessor `boolean`
{:#members:enablewbspredecessor}

Enables/disables WBS predecessor column. 


#### Default Value:
{:.param}

* false

#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ enableWBSPredecessor : true});                    
</script>

{% endhighlight %}

### enableCollapseAll `boolean`
{:#members:enablecollapseall}

Enables or disables the collapse all records when loading the Gantt.


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    enableCollapseAll: false
 });            
</script>

{% endhighlight %}

### leftTaskLabelMapping `string`
{:#members:lefttasklabelmapping}

Specifies the data source field name to be displayed as left task label

#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    leftTaskLabelMapping: "taskId",
 });            
</script>

{% endhighlight %}

### rightTaskLabelMapping `string`
{:#members:righttasklabelmapping}

Specifies the data source field name to be displayed as right task label


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    rightTaskLabelMapping: "taskName",
 });            
</script>

{% endhighlight %}

### leftTaskLabelTemplate `string`
{:#members:lefttasklabeltemplate}

Specifies the template for left task label


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    leftTaskLabelTemplate: "#customTaskLeftLabel",
 });            
</script>

{% endhighlight %}

### rightTaskLabelTemplate `string`
{:#members:righttasklabeltemplate}

Specifies the template for right task label


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    rightTaskLabelTemplate: "#customTaskRightLabel",
 });            
</script>

{% endhighlight %}

### enableContextMenu `boolean`
{:#members:enablecontextmenu}

Enables or disables the contextmenu for Gantt , when enabled contextmenu appears on right clicking Gantt


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    enableContextMenu: false
 });            
</script>

{% endhighlight %}


### enableProgressBarResizing `boolean`
{:#members:enableprogressbarresizing}

Indicates whether we can edit the progress of a task interactively in Gantt.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ enableProgressBarResizing:  true });                      
</script>

{% endhighlight %}


### enableResize `boolean`
{:#members:enableresize}

Enables or disables the option for dynamically updating the Gantt size on window resizing


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    enableResize: false
 });            
</script>

{% endhighlight %}


### enableTaskbarDragTooltip `boolean`
{:#members:enabletaskbardragtooltip}

Enables or disables tooltip while editing (dragging/resizing) the taskbar.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        enableTaskbarDragTooltip : true});
</script>

{% endhighlight %}


### enableTaskbarTooltip `boolean`
{:#members:enabletaskbartooltip}

Enables or disables tooltip for taskbar.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  enableTaskbarTooltip : true });  
</script>

{% endhighlight %}


### enableVirtualization `boolean`
{:#members:enablevirtualization}

Enables/Disables virtualization for rendering Gantt items.


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ enableVirtualization : true});                    
</script>

{% endhighlight %}


### endDateMapping `string`
{:#members:enddatemapping}

Specifies the mapping property path for end Date of a task in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  endDateMapping : "EndDate" });   
</script>

{% endhighlight %}


### highlightWeekends `boolean`
{:#members:highlightweekends}

Specifies whether to highlight the weekends in Gantt .


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ highlightWeekends:  true });                      * 
</script>

{% endhighlight %}


### holidays `array`
{:#members:holidays}

Collection of holidays with date, background and label information to be displayed in Gantt.


#### Default Value:
{:.param}

* []


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt(
 {
   holidays:[{day:"12/2/2000",background:"cyan",label:"local holiday" }]        
 });            
</script>

{% endhighlight %}


### includeWeekend `boolean`
{:#members:includeweekend}

Specifies whether to include weekends while calculating the duration of a task.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ includeWeekend:  true });                 
</script>

{% endhighlight %}


### locale `string`
{:#members:locale}

Specify the locale for Gantt


#### Default Value:
{:.param}

* "en-US"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  locale : "it-IT" });
</script>

{% endhighlight %}


### milestoneMapping `string`
{:#members:milestonemapping}

Specifies the mapping property path for milestone in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  milestoneMapping : "milestone" });       
</script>

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
 
<div id="gantt"></div> 
<script>   
        $("#gantt").ejGantt({ showColumnOptions:  true });                      * 
</script>

{% endhighlight %}

### parentTaskbarTemplate `string`
{:#members:parenttaskbartemplate}

Specifies the template for parent taskbar


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    parentTaskbarTemplate: "ParentTaskbarTemplate"
 });            
</script>

{% endhighlight %}

### selectionType `enum`
{:#members:selectiontype}

<ts name = "ej.Gantt.SelectionType"/>

Specifies the row selection type.

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

* ej.Gantt.SelectionType.Single


#### Example


{% highlight html %}
          
<div id="gantt"></div> 
<script>   
        $("#gantt").ejGantt({ selectionType:ej.Gantt.SelectionType.Multiple });                      * 
</script>           

{% endhighlight %}

### parentProgressbarBackground `string`
{:#members:parentprogressbarbackground}

Specifies the background of parent progressbar in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        parentProgressbarBackground : "#F2F2F2"});
</script>

{% endhighlight %}


### parentTaskbarBackground `string`
{:#members:parenttaskbarbackground}

Specifies the background of parent taskbar in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        parentTaskbarBackground : "#F2F2F2"});
</script>

{% endhighlight %}


### parentTaskIdMapping `string`
{:#members:parenttaskidmapping}

Specifies the mapping property path for parent task Id in self reference datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  parentTaskIdMapping : "ID" });               
</script>

{% endhighlight %}


### predecessorMapping `string`
{:#members:predecessormapping}

Specifies the mapping property path for predecessors of a task in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  predecessorMapping : "predecessor" });           
</script>

{% endhighlight %}


### progressbarBackground `string`
{:#members:progressbarbackground}

Specifies the background of progressbar in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({  
                        progressbarBackground : "#F2F2F2"});
</script>

{% endhighlight %}


### progressbarHeight `number`
{:#members:progressbarheight}


Specified the height of the progressbar in taskbar


#### Default Value:
{:.param}

* 100


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  
                        progressbarHeight : 100 });
</script>

{% endhighlight %}


### progressbarTooltipTemplate `string`
{:#members:progressbartooltiptemplate}

Specifies the template for tooltip on resizing progressbar


#### Default Value:
{:.param}

* null


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    progressbarTooltipTemplate: ""
 });            
</script>

{% endhighlight %}


### progressbarTooltipTemplateId `string`
{:#members:progressbartooltiptemplateid}

Specifies the template ID for customized tooltip for progressbar editing in Gantt


#### Default Value:
{:.param}

* null


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt(
 {
    progressbarTooltipTemplateId: "tooltiptemplateID"
 });            
</script>

{% endhighlight %}


### progressMapping `string`
{:#members:progressmapping}

Specifies the mapping property path for progress percentage of a task in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  progressMapping : "progress" });                 
</script>

{% endhighlight %}


### query `object`
{:#members:query}

It receives query to retrieve data from the table (query is same as SQL).


#### Default Value:
{:.param}

* null


#### Example
{:.example}


{% highlight html %}
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt(
 {
    query:ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);      
 });            
</script>

{% endhighlight %}


### renderBaseline `boolean`
{:#members:renderbaseline}

Enables or Disables rendering baselines in Gantt , when enabled baseline is rendered in Gantt


#### Default Value:
{:.param}

* "false"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    renderBaseline: false
 });            
</script>

{% endhighlight %}


### resourceIdMapping `string`
{:#members:resourceidmapping}

Specifies the mapping property name for resource ID in resource Collection in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt(
 {
    resourceIdMapping: "peopleID"
 });            
</script>

{% endhighlight %}


### resourceInfoMapping `string`
{:#members:resourceinfomapping}

Specifies the mapping property path for resources of a task in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  resourceInfoMapping : "resources" });    
</script>

{% endhighlight %}


### resourceNameMapping `string`
{:#members:resourcenamemapping}


Specifies the mapping property path for resource name of a task in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    resourceNameMapping: "EmployeeName"
 });            
</script>

{% endhighlight %}


### resources `array`
{:#members:resources}

Collection of data regarding resources involved in entire project


#### Default Value:
{:.param}

* []


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
   resources:[{id:1; name:"jack" }]     
 });            
</script>

{% endhighlight %}


### roundOffDayworkingTime `boolean`
{:#members:roundoffdayworkingtime}


Specifies whether rounding off the day working time edits


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        roundOffDayworkingTime : true });
</script>

{% endhighlight %}


### rowHeight `number`
{:#members:rowheight}

Specifies the height of a single row in Gantt. Also, we need to set same height in the CSS style with class name e-rowcell.


#### Default Value:
{:.param}

* 30


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        rowHeight : 30,
                        });
</script>

{% endhighlight %}



### scheduleEndDate `string`
{:#members:scheduleenddate}


Specifies end date of the Gantt schedule. By default, end date will be rounded to its next Saturday.


#### Default Value:
{:.param}

* null


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt(
 {
    scheduleEndDate:"12/2/2000"
 });            
</script>

{% endhighlight %}


### scheduleHeaderSettings `object`
{:#members:scheduleheadersettings}

Specifies the options for customizing schedule header.


### scheduleHeaderSettings.dayHeaderFormat `string`
{:#members:scheduleheadersettings-dayheaderformat}

Specified the format for day view in schedule header


#### Default Value:
{:.param}

* "ddd"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{dayHeaderFormat : "ddd" }
                });
</script>              

{% endhighlight %}


### scheduleHeaderSettings.hourHeaderFormat `string`
{:#members:scheduleheadersettings-hourheaderformat}

Specified the format for Hour view in schedule header


#### Default Value:
{:.param}

* "HH"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{hourHeaderFormat : 'HH'}
                });
</script>               

{% endhighlight %}


### scheduleHeaderSettings.minutesPerInterval `enum`
{:#members:scheduleheadersettings-minutesperinterval}

<ts name = "ej.Gantt.minutesPerInterval"/>

Specifies the number of minutes per interval

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Auto</td>
<td class="description">Sets the interval automatically according with schedule start and end date.</td>
</tr>
<tr>
<td class="name">OneMinute</td>
<td class="description">Sets one minute intervals per hour.</td>
</tr>
<tr>
<td class="name">FiveMinutes</td>
<td class="description">Sets Five minute intervals per hour.</td>
</tr>
<tr>
<td class="name">FifteenMinutes</td>
<td class="description">Sets fifteen minute intervals per hour.</td>
</tr>
<tr>
<td class="name">ThirtyMinutes</td>
<td class="description">Sets thirty minute intervals per hour.</td>
</tr>
</tbody>
</table>

#### Default Value:
{:.param}

* ej.Gantt.minutesPerInterval.Auto


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{minutesPerInterval : ej.Gantt.minutesPerInterval.OneMinute}});              
</script>              

{% endhighlight %}


### scheduleHeaderSettings.monthHeaderFormat `string`
{:#members:scheduleheadersettings-monthheaderformat}

Specified the format for month view in schedule header


#### Default Value:
{:.param}

* "MMM"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{monthHeaderFormat : "MMM" }
               });
</script>              

{% endhighlight %}


### scheduleHeaderSettings.scheduleHeaderType `enum`
{:#members:scheduleheadersettings-scheduleheadertype}

<ts name = "ej.Gantt.ScheduleHeaderType"/>

Specifies the schedule mode

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Year</td>
<td class="description">Sets year Schedule Mode.</td>
</tr>
<tr>
<td class="name">Month</td>
<td class="description">Sets month Schedule Mode.</td>
</tr>
<tr>
<td class="name">Week</td>
<td class="description">Sets week Schedule Mode.</td>
</tr>
<tr>
<td class="name">Day</td>
<td class="description">Sets day Schedule Mode.</td>
</tr>
<tr>
<td class="name">Hour</td>
<td class="description">Sets hour Schedule Mode.</td>
</tr>
</tbody>
</table>

#### Default Value:
{:.param}

* ej.Gantt.ScheduleHeaderType.Week


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
    $("#gantt").ejGantt({  
               scheduleHeaderSettings:{scheduleHeaderType : ej.Gantt.ScheduleHeaderType.Month}
    });
</script>              

{% endhighlight %}

### scheduleHeaderSettings.timescaleStartDateMode `enum`
{:#members:scheduleheadersettings-timescalestartdatemode}

<ts name = "ej.Gantt.TimescaleRoundMode"/>

Specifies the round-off mode for the start date in schedule header.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Auto</td>
<td class="description">The round-off value will be automatically calculated based on the data source values.</td>
</tr>
<tr>
<td class="name">Week</td>
<td class="description">Schedule header start date will round-off to the immediate week.</td>
</tr>
<tr>
<td class="name">Month</td>
<td class="description">Schedule headers start date will round off to the immediate month</td>
</tr>
<tr>
<td class="name">Year</td>
<td class="description">Schedule headers start date will round off to the immediate year</td>
</tr>
</tbody>
</table>

#### Default Value:
{:.param}

* ej.Gantt.TimescaleRoundMode.Auto


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{timescaleStartDateMode : ej.Gantt.TimescaleRoundMode.Week}
                });              
</script>              

{% endhighlight %}

### scheduleHeaderSettings.weekendBackground `string`
{:#members:scheduleheadersettings-weekendbackground}

Specified the background for weekends in Gantt


#### Default Value:
{:.param}

* "#F2F2F2"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{weekendBackground : "#F2F2F2"}});
</script>

{% endhighlight %}


### scheduleHeaderSettings.weekHeaderFormat `string`
{:#members:scheduleheadersettings-weekheaderformat}

Specified the format for week view in schedule header


#### Default Value:
{:.param}

* "ddd"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{weekHeaderFormat : "MMM dd , yyyy" }
               });
</script>

{% endhighlight %}


### scheduleHeaderSettings.yearHeaderFormat `string`
{:#members:scheduleheadersettings-yearheaderformat}

Specified the format for year view in schedule header


#### Default Value:
{:.param}

* "yyyy"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{yearHeaderFormat : "yyyy" }
               });
</script>               

{% endhighlight %}


### scheduleStartDate `string`
{:#members:schedulestartdate}

Specifies start date of the Gantt schedule. By default, start date will be rounded to its previous Sunday.


#### Default Value:
{:.param}

* null


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt(
 {
    scheduleStartDate:"12/2/2000"
 });            
</script>

{% endhighlight %}


### selectedRowIndex `number`
{:#members:selectedrowindex}

Specifies the selected row Index in Gantt , the row with given index will highlighted


#### Default Value:
{:.param}

* -1


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    selectedRowIndex:2
 });            
</script>

{% endhighlight %}


### showColumnChooser `boolean`
{:#members:showcolumnchooser}

Enables or disables the column chooser.


#### Default Value:
{:.param}

* false


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>   
        $("#gantt").ejGantt({ showColumnChooser:  true });                      * 
</script>

{% endhighlight %}



### showGridCellTooltip `boolean`
{:#members:showgridcelltooltip}

Specifies whether to show grid cell tooltip.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showGridCellTooltip : true});
</script>

{% endhighlight %}


### showGridExpandCellTooltip `boolean`
{:#members:showgridexpandcelltooltip}

Specifies whether to show grid cell tooltip over expander cell alone.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showGridExpandCellTooltip : true});
</script>

{% endhighlight %}


### showProgressStatus `boolean`
{:#members:showprogressstatus}

Specifies whether display task progress inside taskbar.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showProgressStatus : true});
</script>

{% endhighlight %}


### showResourceNames `boolean`
{:#members:showresourcenames}

Specifies whether to display resource names for a task beside taskbar.


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showResourceNames : true});
</script>

{% endhighlight %}


### showTaskNames `boolean`
{:#members:showtasknames}

Specifies whether to display task name beside task bar.


#### Default Value:
{:.param}


* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showTaskNames : true});
</script>

{% endhighlight %}


### sizeSettings `object`
{:#members:sizesettings}

Specifies the size option of Gantt control.


### sizeSettings.height `string`
{:#members:sizesettings-height}


Specifies the height of Gantt control


#### Default Value:
{:.param}

* "450px"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    sizeSettings:{height: "700px"}
 });            
</script>

{% endhighlight %}


### sizeSettings.width `string`
{:#members:sizesettings-width}

Specifies the width of Gantt control


#### Default Value:
{:.param}

* "1000px"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    sizeSettings:{width: "700px"}
 });            
</script>

{% endhighlight %}

### selectedCellIndexes `array`
{:#members:selectedcellindexes}

Specifies the selected cell information on rendering Gantt.

### selectedCellIndexes.rowIndex `number`
{:#members:selectedcellindexes-rowIndex}


Specifies the row index of the cell to be selected Gantt control


#### Default Value:
{:.param}

* ""

### selectedCellIndexes.cellIndex `number`
{:#members:selectedcellindexes-cellIndex}

Specifies the cell index to be selected in the row.


#### Default Value:
{:.param}

* " "

#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    selectedCellIndexes:[{rowIndex: 2, cellIndex: 3}];
 });            
</script>

{% endhighlight %}

### sortSettings `object`
{:#members:sortsettings}

Specifies the sorting options for Gantt.


### sortSettings.sortedColumns `array`
{:#members:sortsettings-sortedcolumns}

Specifies the sorted columns for Gantt


#### Default Value:
{:.param}

* []


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({ sortSettings{sortedColumns : []}});                  
</script>

{% endhighlight %}


### splitterPosition `string`
{:#members:splitterposition}

Specifies splitter position in Gantt.


#### Default Value:
{:.param}

* null


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                                  
        $("#gantt").ejGantt({  splitterPosition : "50%" });     
</script>

{% endhighlight %}


### startDateMapping `string`
{:#members:startdatemapping}


Specifies the mapping property path for start date of a task in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                                  
        $("#gantt").ejGantt({  startDateMapping : "startdate" });                
</script>

{% endhighlight %}


### stripLines `array`
{:#members:striplines}

Specifies the options for striplines


#### Default Value:
{:.param}

* []


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(stripLines: [
   {
    day: "12/2/2000,
    label: "Project Release",
    lineStyle: "dotted",
    lineColor: "Darkblue",
    lineWidth: 2
  }
]); 
</script>

{% endhighlight %}


### taskbarBackground `string`
{:#members:taskbarbackground}

Specifies the background of the taskbar in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({  
                        taskbarBackground : "#F2F2F2"});
</script>

{% endhighlight %}


### taskbarEditingTooltipTemplate `string`
{:#members:taskbareditingtooltiptemplate}

Specifies the template script for customized tooltip for taskbar editing in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    taskbarEditingTooltipTemplate: "tooltiptemplate"
 });            
</script>

{% endhighlight %}


### taskbarEditingTooltipTemplateId `string`
{:#members:taskbareditingtooltiptemplateid}


Specifies the template Id for customized tooltip for taskbar editing in Gantt


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    taskbarEditingTooltipTemplateId: "TooltipTemplateId"
 });            
</script>

{% endhighlight %}


### taskbarTooltipTemplate `string`
{:#members:taskbartooltiptemplate}

Specifies the template for tooltip on mouse action on taskbars


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    taskbarTooltipTemplate: "TooltipTemplate"
 });            
</script>

{% endhighlight %}

### taskbarTemplate `string`
{:#members:taskbartemplate}

To Specify the JsRender script Id to customize the task bar with our preference


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    taskbarTemplate: "TaskbarTemplate"
 });            
</script>

{% endhighlight %}


### milestoneTemplate `string`
{:#members:milestonetemplate}

To Specify the JsRender script Id to customize the mile stone with our preference


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    milestoneTemplate: "MilestoneTemplate"
 });            
</script>

{% endhighlight %}

### readOnly `boolean`
{:#members:readonly}

Enables or disables Gantt to read-only mode

#### Default Value:
{:.param}

* "false"

#### Example
{:.example}

{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    readOnly: "true"
 });            
</script>

{% endhighlight %}

### taskbarTooltipTemplateId `string`
{:#members:taskbartooltiptemplateid}

Specifies the template id for tooltip on mouse action on taskbars


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    taskbarTooltipTemplateId: "TooltipTemplateId"
 });            
</script>

{% endhighlight %}


### taskIdMapping `string`
{:#members:taskidmapping}

Specifies the mapping property path for task Id in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                                  
        $("#gantt").ejGantt({  taskIdMapping : "ID" }); 
</script>

{% endhighlight %}


### taskNameMapping `string`
{:#members:tasknamemapping}

Specifies the mapping property path for task name in datasource


#### Default Value:
{:.param}

* ""


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  taskNameMapping : "Name" });     
</script>

{% endhighlight %}


### toolbarSettings `object`
{:#members:toolbarsettings}

Specifies the toolbarSettings options.


### toolbarSettings.showToolBar `boolean`
{:#members:toolbarsettings-showtoolbar}

Specifies the state of enabling or disabling toolbar


#### Default Value:
{:.param}

* true


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ showToolBar:  true });                     
</script>

{% endhighlight %}


### toolbarSettings.toolbarItems `array`
{:#members:toolbarsettings-toolbaritems}

<ts name = "ej.Gantt.ToolbarItems"/>

Specifies the list of toolbar items to be rendered in Gantt toolbar

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
<td class="name">Search</td>
<td class="description">Enables the search icon in toolbar</td>
</tr>
<tr>
<td class="name">Indent</td>
<td class="description">Enables the indent icon in toolbar</td>
</tr>
<tr>
<td class="name">Outdent</td>
<td class="description">Enables the outdent icon in toolbar</td>
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
<td class="name">PrevTimeSpan</td>
<td class="description">Enables the previous time span icon in toolbar</td>
</tr>
<tr>
<td class="name">NextTimeSpan</td>
<td class="description">Enables the next time span icon in toolbar</td>
</tr>
</tbody>
</table>

#### Default Value:
{:.param}
* []

#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ toolbarSettings: { toolbarItems: [ej.Gantt.ToolbarItems.Add,ej.Gantt.ToolbarItems.Edit] } });                   
</script>

{% endhighlight %}


### treeColumnIndex `number`
{:#members:treecolumnindex}

Specifies the tree expander column in Gantt


#### Default Value:
{:.param}

* 0


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    treeColumnIndex: 1
 });            
</script>

{% endhighlight %}

### selectionMode `enum`
{:#members:selectionmode}

<ts name = "ej.Gantt.SelectionMode"/>

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

* ej.Gantt.SelectionMode.Row


#### Example


{% highlight html %}
          
<div id="gantt"></div> 
<script>   
        $("#gantt").ejGantt({ selectionMode:ej.Gantt.SelectionMode.Row });                      * 
</script>           

{% endhighlight %}

### weekendBackground `string`
{:#members:weekendbackground}

Specifies the weekendBackground color in Gantt


#### Default Value:
{:.param}

* "#F2F2F2"


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    weekendBackground: "blue"
 });            
</script>

{% endhighlight %}


### workingTimeScale `enum`
{:#members:workingtimescale}

<ts name = "ej.Gantt.workingTimeScale"/>

Specifies the working time schedule of day

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">TimeScale8Hours</td>
<td class="description">Sets eight hour timescale.</td>
</tr>
<tr>
<td class="name">TimeScale24Hours</td>
<td class="description">Sets twenty four hour timescale.</td>
</tr>
</tbody>
</table>

#### Default Value:
{:.param}

* ej.Gantt.workingTimeScale.TimeScale8Hours


#### Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        workingTimeScale : ej.Gantt.workingTimeScale.TimeScale24Hours
            });
</script>

{% endhighlight %}


## Methods

### addRecord(data, rowPosition)
{:#methods:addrecord}

To add item in Gantt

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
<td class="description">Item to add in Gantt row.</td>
</tr>
<tr>
<td class="name">rowPosition</td>
<td class="type">enum</td>
<td class="description">Defines in which position the row wants to add</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
var data = {taskId:"40",taskName:"New Task 40",startDate:"2/20/2014",startDate:"2/25/2014"};
ganttObj.addRecord(data, ej.Gantt.AddRowPosition.Child); // To add a task
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
<td class="description">Defines that we need to preserve the previously selected cells of not</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
var indexes = [{rowIndex:4, cellIndex: 4}, {rowIndex: 3, cellIndex: 3}];
ganttObj.selectCells(indexes, true); // To add a task
</script>
{% endhighlight %}


### setSplitterIndex(index)
{:#methods:setsplitterindex}

Positions the splitter by the specified column index.

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
<td class="type">Number</td>
<td class="description">Set the splitter position based on column index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt object
var ganttObj = $("#gantt").data("ejGantt");
gantObj.setSplitterIndex(3); // Set splitter position after column index 3
</script>
{% endhighlight %}

### cancelEdit()
{:#methods:canceledit}

To cancel the edited state of an item in Gantt

#### Example

{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt object
var ganttObj = $("#gantt").data("ejGantt");
gantObj.cancelEdit(); // To cancel edited
</script>
{% endhighlight %}

### collapseAllItems()
{:#methods:collapseallitems}

To collapse all the parent items in Gantt


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.collapseAllItems(); // To collapse all parent items in Gantt
</script>
{% endhighlight %}

### deleteItem()
{:#methods:deleteitem}

To delete a selected item in Gantt


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.deleteItem(); // To delete a task
</script>
{% endhighlight %}


### destroy()
{:#methods:destroy}

destroy the Gantt widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create gantt Object
var ganttObj = $("#gantt").data("ejGantt");
ganttObj.destroy(); // destroy the gantt
</script>
{% endhighlight %}


### expandAllItems()
{:#methods:expandallitems}

To Expand all the parent items in Gantt


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt Object
var ganttObj = $("#gantt").data("ejGantt");
gantObj.expandAllItems(); // To expand all parent items in Gantt
</script>
{% endhighlight %}


### expandCollapseRecord(taskId)
{:#methods:expandcollapserecord}

To expand and collapse an item in Gantt using item's ID

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
<td class="name">taskId</td>
<td class="type">Number</td>
<td class="description">Expand or Collapse a record based on task id.</td>
</tr>
</tbody>
</table>

#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt object.
var ganttObj = $("#gantt").data("ejGantt");
gantObj.expandCollapseRecord(23); // To expand collapse an item
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
<td class="description">you can pass a header text of a column to hide</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<gantt id="gantt">Gantt</gantt> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.hideColumn("Task Name");
</script>
{% endhighlight %}


### indentItem()
{:#methods:indentitem}

To indent a selected item in Gantt


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.indentItem(); // To indent a selected item in Gantt
</script>
{% endhighlight %}


### openAddDialog()
{:#methods:openadddialog}

To Open the dialog to add new task to the Gantt


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt Object.
var ganttObj = $("#gantt").data("ejGantt");
gantObj.openAddDialog(); // To open the add dialog
</script>
{% endhighlight %}


### openEditDialog()
{:#methods:openeditdialog}

To Open the dialog to edit existing task to the Gantt


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt object
var ganttObj = $("#gantt").data("ejGantt");
gantObj.openEditDialog(); // To open the add dialog
</script>
{% endhighlight %}


### outdentItem()
{:#methods:outdentitem}

To outdent a selected item in Gantt


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.outdentItem(); // To outdent a selected item in Gantt
</script>
{% endhighlight %}


### saveEdit()
{:#methods:saveedit}

To save the edited state of an item in Gantt


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.saveEdit(); // To save edited state of an item
</script>
{% endhighlight %}


### searchItem(searchString)
{:#methods:searchitem}

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
<td class="description">you can pass a text to search in Gantt Control.</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt Object
var ganttObj = $("#gantt").data("ejGantt");
gantObj.searchItem($("#text").val()); // To search a task
</script>
{% endhighlight %}


### setSplitterPosition(width)
{:#methods:setsplitterposition}

To set the grid width in Gantt

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
<td class="name">width</td>
<td class="type">string</td>
<td class="description">you can give either percentage or pixels value</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("setSplitterPosition","40%");
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
<td class="description">you can pass a header text of a column to show</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<gantt id="gantt">Gantt</gantt> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.showColumn("Task Name");
</script>
{% endhighlight %}


## Events


### actionBegin
{:#events:actionbegin}

Triggered for every Gantt action before its starts.

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
<td class="description">Event parameters when Gantt is initialized:
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
<td class="description">Event parameters while perform sorting in grid tree action starts:
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
<td class="description">Returns the Gantt model.</td>
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
<td class="description">Event parameters while searching action starts:
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
<td class="description">Returns the value of searching element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the Gantt model.</td>
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
<td class="description">Event parameters while performing the delete operation starts:
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
<td class="description">Returns the data of deleting element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the Gantt model.</td>
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
<td class="description">Event parameters while performing the add operation starts:
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
<td class="description">Returns the data adding element.</td>
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
<td class="description">Event parameters while performing the edit operation starts:
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
<td class="description">Returns the data editing element</td>
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   actionBegin: function (args) {}
});
</script>
{% endhighlight %}


### actionComplete
{:#events:actioncomplete}

Triggered for every Gantt action success event.

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
<td class="description">Event parameters when Gantt is initialized:
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
<td class="description">Event parameters after perform the sorting in TreeGrid is completed:
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
<td class="description">Returns the Gantt model.</td>
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
<td class="description">Returns the Gantt model.</td>
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
<td class="description">Returns the Gantt model.</td>
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   beginEdit: function (args) {}
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   cellSelected: function (args) {}
});
</script>
{% endhighlight %}


### rowDrag
{:#events:rowdrag}


Triggered while dragging a row in Gantt control

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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   rowDrag: function (args) {}
});
</script>
{% endhighlight %}


### rowDragStart
{:#events:rowdragstart}


Triggered while start to drag row in Gantt control

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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   rowDragStart: function (args) {}
});
</script>
{% endhighlight %}


### rowDragStop
{:#events:rowdragstop}


Triggered while drop a row in Gantt control

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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   rowDragStop: function (args) {}
});
</script>
{% endhighlight %}



### collapsed
{:#events:collapsed}


Triggered after collapsed the Gantt record

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
<td class="type">Number</td>
<td class="description">Returns the row index of collapsed record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of collapsed record.</td>
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
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   collapsed: function (args) {}
});
</script>
{% endhighlight %}


### collapsing
{:#events:collapsing}

Triggered while collapsing the Gantt record

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
<td class="type">Number</td>
<td class="description">Returns the row index of collapsing record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of edited cell record..</td>
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   collapsing: function (args) {}
});
</script>
{% endhighlight %}


### contextMenuOpen
{:#events:contextmenuopen}

Triggered while Context Menu is rendered in Gantt control

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
<td class="description">Returns the Gantt model.</td>
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   contextMenuOpen: function (args) {}
});
</script>
{% endhighlight %}


### endEdit
{:#events:endedit}

Triggered after save the modified cellValue in Gantt.

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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
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
<td class="description">Returns the row index of record.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of expanded record.</td>
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
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   expanded: function (args) {}
});
</script>
{% endhighlight %}


### expanding
{:#events:expanding}

Triggered while expanding the Gantt record

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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   expanding: function (args) {}
});
</script>
{% endhighlight %}


### load
{:#events:load}

Triggered while Gantt is loaded

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
<td class="description">Returns the Gantt model</td>
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   queryCellInfo: function (args) {}
});
</script>
{% endhighlight %}


### queryTaskbarInfo
{:#events:querytaskbarinfo}

Triggered while rendering each taskbar in the Gantt 

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
<td class="description">Arguments when queryTaskbarInfo event is triggered.
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
<td class="name">TaskbarBackground</td>
<td class="type">string</td>
<td class="description">Returns the taskbar background of current item.</td>
</tr>
<tr>
<td class="name">ProgressbarBackground</td>
<td class="type">string</td>
<td class="description">Returns the progressbar background of current item.</td>
</tr>
<tr>
<td class="name">parentTaskbarBackground</td>
<td class="type">string</td>
<td class="description">Returns the parent taskbar background of current item.</td>
</tr>
<tr>
<td class="name">parentProgressbarBackground</td>
<td class="type">string</td>
<td class="description">Returns the parent progressbar background of current item.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type">object</td>
<td class="description">Returns the data of the record.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   queryTaskbarInfo: function (args) {}
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
<td class="description">Returns the data of rendering row record..</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   rowDataBound: function (args) {}
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
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
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
<td class="name">targetChartRow</td>
<td class="type">object</td>
<td class="description">Returns the selecting row chart element.</td>
</tr>
<tr>
<td class="name">targetGridRow</td>
<td class="type">object</td>
<td class="description">Returns the selecting row grid element.</td>
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
<td class="name">previousChartRow</td>
<td class="type">object</td>
<td class="description">Returns the previous selected row chart element.</td>
</tr>
<tr>
<td class="name">previousGridRow</td>
<td class="type">object</td>
<td class="description">Returns the previous selected row grid element.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   rowSelecting: function (args) {}
});
</script>
{% endhighlight %}


### taskbarEdited
{:#events:taskbaredited}

Triggered after completing the editing operation in taskbar

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
<td class="description">Arguments when taskbarEdited event is triggered.
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
<td class="description">Returns the data of edited record.</td>
</tr>
<tr>
<td class="name">previousData</td>
<td class="type">object</td>
<td class="description">Returns the previous data value of edited record.</td>
</tr>
<tr>
<td class="name">dragging</td>
<td class="type">boolean</td>
<td class="description">Returns 'true' if taskbar is dragged.</td>
</tr>
<tr>
<td class="name">leftResizing</td>
<td class="type">boolean</td>
<td class="description">Returns 'true' if taskbar is left resized.</td>
</tr>
<tr>
<td class="name">rightResizing</td>
<td class="type">boolean</td>
<td class="description">Returns 'true' if taskbar is right resized.</td>
</tr>
<tr>
<td class="name">progressResizing</td>
<td class="type">boolean</td>
<td class="description">Returns 'true' if taskbar is progress resized.</td>
</tr>
<tr>
<td class="name">editingFields</td>
<td class="type">object</td>
<td class="description">Returns the field values of record being edited.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the Gantt model.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   taskbarEdited: function (args) {}
});
</script>
{% endhighlight %}


### taskbarEditing
{:#events:taskbarediting}

Triggered while editing the Gantt chart (dragging, resizing the taskbar )

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
<td class="description">Arguments when taskbarEditing event is triggered.
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
<td class="description">Returns the Gantt model.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type">object</td>
<td class="description">Returns the row object being edited.</td>
</tr>
<tr>
<td class="name">editingFields</td>
<td class="type">object</td>
<td class="description">Returns the field values of record being edited.</td>
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   taskbarEditing: function (args) {}
});
</script>
{% endhighlight %}


### toolbarClick
{:#events:toolbarclick}

Triggered when toolbar item is clicked in Gantt.

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
<td class="description last">Arguments when toolbarClick event is triggered.
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
<td class="description">Returns the Gantt model.</td>
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   toolbarClick: function (args) {}
});
</script>
{% endhighlight %}

