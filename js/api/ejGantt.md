---
layout: post
title: ejGantt
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Gantt control.










$(element).ejGantt<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;gantt id="gantt"&gt;Gantt&lt;/gantt&gt; 
 
&lt;script&gt;
// Create Gantt
$('#gantt').ejGantt();  
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








### addDialogFields<span class="type-signature type array">Array</span>
{:#members-adddialogfields}








Specifies the fields to be included in the add dialog in gantt




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    addDialogFields: [{ field: "taskId", editType: "stringedit" }]
 });            
&lt;/script&gt;</code>
</pre>






### allowColumnResize<span class="type-signature type boolean">boolean</span>
{:#members-allowcolumnresize}








Enables or disables the ability to resize column.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                   
        $("#gantt").ejGantt({ allowColumnResize:  true });                      * 
&lt;/script&gt;</code>
</pre>






### allowGanttChartEditing<span class="type-signature type boolean">boolean</span>
{:#members-allowganttchartediting}








Enables or Disables gantt chart editing in gantt




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    allowGanttChartEditing:true
 });            
&lt;/script&gt;</code>
</pre>






### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members-allowkeyboardnavigation}








Enables or Disables Keyboard navigation in gantt




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({ allowKeyboardNavigation : true});                 
&lt;/script&gt;</code>
</pre>






### allowMultiSorting<span class="type-signature type boolean">boolean</span>
{:#members-allowmultisorting}








Specifies enabling or disabling multiple soting for gantt columns




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({ allowMultiSorting : true});                       
&lt;/script&gt;</code>
</pre>






### allowSelection<span class="type-signature type boolean">boolean</span>
{:#members-allowselection}








Enables or disables the interactive selection of a row.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;   
        $("#gantt").ejGantt({ allowSelection:  true });                 * 
&lt;/script&gt;</code>
</pre>






### allowSorting<span class="type-signature type boolean">boolean</span>
{:#members-allowsorting}








Enables or disables sorting. When enabled, we can sort the column by clicking on the column.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#gantt").ejGantt({ allowSorting:  true });            
&lt;/script&gt;</code>
</pre>






### baselineColor<span class="type-signature type string">string</span>
{:#members-baselinecolor}








Specifies the baseline background color in gantt




Default Value:
{:.param}






* "#fba41c"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt(
 {
    baselineColor: "blue"
 });            
&lt;/script&gt;</code>
</pre>






### baselineEndDateMapping<span class="type-signature type string">string</span>
{:#members-baselineenddatemapping}








Specifies the mapping property path for baseline end date in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  baselineEndDateMapping : "BaselineEndDate" });
&lt;/script&gt;</code>
</pre>






### baselineStartDateMapping<span class="type-signature type string">string</span>
{:#members-baselinestartdatemapping}








Specifies the mapping property path for baseline start date of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  baselineStartDateMapping : "BaselineStartDate" });               
&lt;/script&gt;</code>
</pre>






### childMapping<span class="type-signature type string">string</span>
{:#members-childmapping}








Specifies the mapping property path for sub tasks in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  childMapping : "Children" });
&lt;/script&gt;</code>
</pre>






### connectorLineBackground<span class="type-signature type string">string</span>
{:#members-connectorlinebackground}








Specifies the background of connector lines in Gantt




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        connectorLineBackground : "#F2F2F2"});
&lt;/script&gt;</code>
</pre>






### connectorlineWidth<span class="type-signature type number">number</span>
{:#members-connectorlinewidth}








Specifies the width of the connector lines in gantt




Default Value:
{:.param}






* "1"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        connectorlineWidth : 1 });
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">string</span>
{:#members-cssclass}








Specify the CSS class for gantt to achieve custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt({  cssClass : "gradient-lime" });
&lt;/script&gt;</code>
</pre>






### dataSource<span class="type-signature type array">array</span>
{:#members-datasource}








Collection of data or hierarchical data to represent in gantt




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    dataSource:[{Id:2,TaskName:"Testing",startDate:"12/1/2000",Duration:5 }]    
 });            
&lt;/script&gt;</code>
</pre>






### dateFormat<span class="type-signature type string">string</span>
{:#members-dateformat}








Specifies the dateFormat for gantt , given format is displayed in tooltip , grid .




Default Value:
{:.param}






* "MM/dd/yyyy"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    dateFormat: "dd/MM/yyyy"
 });            
&lt;/script&gt;</code>
</pre>






### durationMapping<span class="type-signature type string">string</span>
{:#members-durationmapping}








Specifies the mapping property path for duration of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt({  durationMapping : "Duration" });
&lt;/script&gt;</code>
</pre>






### durationUnit<span class="type-signature type enum">enum</span>
{:#members-durationunit}








Specifies the duration unit for each tasks whether days or hours




Default Value:
{:.param}






* "day"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        durationUnit : day });
&lt;/script&gt;</code>
</pre>






### editDialogFields<span class="type-signature type array">Array</span>
{:#members-editdialogfields}








Specifies the fields to be included in the edit dialog in gantt




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    editDialogFields: [{ field: "taskId", editType: "stringedit" }]
 });            
&lt;/script&gt;</code>
</pre>






### editSettings<span class="type-signature type object">object</span>
{:#members-editsettings}








Specifies the editSettings options in gantt.











### editSettings.allowAdding<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-allowadding}








Enables or disables add record icon in gantt toolbar




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  editSettings:{allowAdding : true} });
&lt;/script&gt;</code>
</pre>






### editSettings.allowDeleting<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-allowdeleting}








Enables or disables delete icon in gantt toolbar




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  editSettings:{allowDeleting : true} });  
&lt;/script&gt;</code>
</pre>






### editSettings.allowEditing<span class="type-signature type boolean">boolean</span>
{:#members-editsettings-allowediting}








Specifies the option for enabling or disablig editing in gantt grid part




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  editSettings:{allowEditing : true} });   
&lt;/script&gt;</code>
</pre>






### editSettings.editMode<span class="type-signature type string">string</span>
{:#members-editsettings-editmode}








Specifies the editmode in gantt , "normal" is for dialog editing ,"cellEditing" is for cell type editing




Default Value:
{:.param}






* normal








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  editSettings:{editMode : "normal"} });
&lt;/script&gt;</code>
</pre>






### enableAltRow<span class="type-signature type boolean">boolean</span>
{:#members-enablealtrow}








Enables or Disables enableAltRow row effect in gantt




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({ enableAltRow : true});                    
&lt;/script&gt;</code>
</pre>






### enableCollapseAll<span class="type-signature type boolean">boolean</span>
{:#members-enablecollapseall}








Enables or disables the collapse all records when loading the gantt.




Default Value:
{:.param}






* "false"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    enableCollapseAll: false
 });            
&lt;/script&gt;</code>
</pre>






### enableContextMenu<span class="type-signature type boolean">boolean</span>
{:#members-enablecontextmenu}








Enables or disables the contextmenu for gantt , when enabled contextmenu appears on right clicking gantt




Default Value:
{:.param}






* "false"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    enableContextMenu: false
 });            
&lt;/script&gt;</code>
</pre>






### enableProgressBarResizing<span class="type-signature type boolean">boolean</span>
{:#members-enableprogressbarresizing}








Indicates whether we can edit the progress of a task interactively in gantt chart.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt({ enableProgressBarResizing:  true });                      
&lt;/script&gt;</code>
</pre>






### enableResize<span class="type-signature type boolean">boolean</span>
{:#members-enableresize}








Enables or disables the option for dynamically updating the Gantt size on window resizing




Default Value:
{:.param}






* "false"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    enableResize: false
 });            
&lt;/script&gt;</code>
</pre>






### enableTaskbarDragTooltip<span class="type-signature type boolean">boolean</span>
{:#members-enabletaskbardragtooltip}








Enables or disables tooltip while editing (dragging/resizing) the taskbar.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        enableTaskbarDragTooltip : true});
&lt;/script&gt;</code>
</pre>






### enableTaskbarTooltip<span class="type-signature type boolean">boolean</span>
{:#members-enabletaskbartooltip}








Enables or disables tooltip for taskbar.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  enableTaskbarTooltip : true });  
&lt;/script&gt;</code>
</pre>






### enableVirtualization<span class="type-signature type boolean">boolean</span>
{:#members-enablevirtualization}








Enables/Disables virtualization for rendering gantt items.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({ enableVirtualization : true});                    
&lt;/script&gt;</code>
</pre>






### endDateMapping<span class="type-signature type string">string</span>
{:#members-enddatemapping}








Specifies the mapping property path for end Date of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  endDateMapping : "EndDate" });   
&lt;/script&gt;</code>
</pre>






### highlightWeekends<span class="type-signature type boolean">boolean</span>
{:#members-highlightweekends}








Specifies whether to highlight the weekends in gantt .




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt({ highlightWeekends:  true });                      * 
&lt;/script&gt;</code>
</pre>






### holidays<span class="type-signature type array">array</span>
{:#members-holidays}








Collection of holidays with date, background and label information to be displayed in gantt.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt(
 {
   holidays:[{day:"12/2/2000",background:"cyan",label:"local holiday" }]        
 });            
&lt;/script&gt;</code>
</pre>






### includeWeekend<span class="type-signature type boolean">boolean</span>
{:#members-includeweekend}








Specifies whether to include weekends while calculating the duration of a task.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt({ includeWeekend:  true });                 
&lt;/script&gt;</code>
</pre>






### locale<span class="type-signature type string">string</span>
{:#members-locale}








Specify the locale for gantt




Default Value:
{:.param}






* "en-US"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt({  locale : "it-IT" });
&lt;/script&gt;</code>
</pre>






### milestoneMapping<span class="type-signature type string">string</span>
{:#members-milestonemapping}








Specifies the mapping property path for milestone in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  milestoneMapping : "milestone" });       
&lt;/script&gt;</code>
</pre>






### parentProgressbarBackground<span class="type-signature type string">string</span>
{:#members-parentprogressbarbackground}








Specifies the background of parent progressbar in gantt




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        parentProgressbarBackground : "#F2F2F2"});
&lt;/script&gt;</code>
</pre>






### parentTaskbarBackground<span class="type-signature type string">string</span>
{:#members-parenttaskbarbackground}








Specifies the background of parent taskbar in gantt




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        parentTaskbarBackground : "#F2F2F2"});
&lt;/script&gt;</code>
</pre>






### parentTaskIdMapping<span class="type-signature type string">string</span>
{:#members-parenttaskidmapping}








Specifies the mapping property path for parent task Id in selfreference datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  parentTaskIdMapping : "ID" });               
&lt;/script&gt;</code>
</pre>






### predecessorMapping<span class="type-signature type string">string</span>
{:#members-predecessormapping}








Specifies the mapping property path for predecessors of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  predecessorMapping : "predecessor" });           
&lt;/script&gt;</code>
</pre>






### progressbarBackground<span class="type-signature type string">string</span>
{:#members-progressbarbackground}








Specifies the background of progressbar in gantt




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt({  
                        progressbarBackground : "#F2F2F2"});
&lt;/script&gt;</code>
</pre>






### progressbarHeight<span class="type-signature type number">number</span>
{:#members-progressbarheight}








Specified the height of the progressbar in taskbar




Default Value:
{:.param}






* "100"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt({  
                        progressbarHeight : 100 });
&lt;/script&gt;</code>
</pre>






### progressbarTooltipTemplate<span class="type-signature type string">string</span>
{:#members-progressbartooltiptemplate}








Specifies the template for tooltip on resizing progressbar




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    progressbarTooltipTemplate: ""
 });            
&lt;/script&gt;</code>
</pre>






### progressbarTooltipTemplateId<span class="type-signature type string">string</span>
{:#members-progressbartooltiptemplateid}








Specifies the template ID for customized tooltip for progressbar editing in gantt




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt(
 {
    progressbarTooltipTemplateId: "tooltiptemplateID"
 });            
&lt;/script&gt;</code>
</pre>






### progressMapping<span class="type-signature type string">string</span>
{:#members-progressmapping}








Specifies the mapping property path for progress percentage of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  progressMapping : "progress" });                 
&lt;/script&gt;</code>
</pre>






### query<span class="type-signature type object">object</span>
{:#members-query}








It receives query to retrieve data from the table (query is same as SQL).




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt(
 {
    query:ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);      
 });            
&lt;/script&gt;</code>
</pre>






### renderBaseline<span class="type-signature type boolean">boolean</span>
{:#members-renderbaseline}








Enables or Disables rendering baselines in Gantt , when enabled baseline is rendered in gantt




Default Value:
{:.param}






* "false"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    renderBaseline: false
 });            
&lt;/script&gt;</code>
</pre>






### resourceIdMapping<span class="type-signature type string">string</span>
{:#members-resourceidmapping}








Specifies the mapping property name for resource ID in resource Collection in gantt




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt(
 {
    resourceIdMapping: "peopleID"
 });            
&lt;/script&gt;</code>
</pre>






### resourceInfoMapping<span class="type-signature type string">string</span>
{:#members-resourceinfomapping}








Specifies the mapping property path for resources of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  resourceInfoMapping : "resources" });    
&lt;/script&gt;</code>
</pre>






### resourceNameMapping<span class="type-signature type string">string</span>
{:#members-resourcenamemapping}








Specifies the mapping property path for resource name of a task in gantt




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    resourceNameMapping: "EmployeeName"
 });            
&lt;/script&gt;</code>
</pre>






### resources<span class="type-signature type array">array</span>
{:#members-resources}








Collection of data regarding resources involved in entire project




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
   resources:[{id:1; name:"jack" }]     
 });            
&lt;/script&gt;</code>
</pre>






### roundOffDayworkingTime<span class="type-signature type boolean">boolean</span>
{:#members-roundoffdayworkingtime}








Specifies whether rounding off the day working time edits




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        roundOffDayworkingTime : true });
&lt;/script&gt;</code>
</pre>






### rowHeight<span class="type-signature type number">number</span>
{:#members-rowheight}








Specifies the height of a single row in gantt. Also, we need to set same height in the CSS style with class name e-rowcell.




Default Value:
{:.param}






* "30"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        rowHeight : 30,
                        });
&lt;/script&gt;</code>
</pre>






### scheduleEndDate<span class="type-signature type string">string</span>
{:#members-scheduleenddate}








Specifies end date of the gantt schedule. By default, end date will be rounded to its next Saturday.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt(
 {
    scheduleEndDate:"12/2/2000"
 });            
&lt;/script&gt;</code>
</pre>






### scheduleHeaderSettings<span class="type-signature type object">object</span>
{:#members-scheduleheadersettings}








Specifies the options for customizing schedule header.











### scheduleHeaderSettings.dayHeaderFormat<span class="type-signature type string">string</span>
{:#members-scheduleheadersettings-dayheaderformat}








Specified the format for day view in schedule header




Default Value:
{:.param}






* "ddd"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{dayHeaderFormat : "ddd" }
                });
&lt;/script&gt;              </code>
</pre>






### scheduleHeaderSettings.hourHeaderFormat<span class="type-signature type string">string</span>
{:#members-scheduleheadersettings-hourheaderformat}








Specified the format for Hour view in schedule header




Default Value:
{:.param}






* "HH"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{hourHeaderFormat : 'HH'}
                });
&lt;/script&gt;               </code>
</pre>






### scheduleHeaderSettings.minutesPerInterval<span class="type-signature type enum">enum</span>
{:#members-scheduleheadersettings-minutesperinterval}








Specifies the number of minutes per interval




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{minutesPerInterval : "oneMinute"}});              
&lt;/script&gt;              </code>
</pre>






### scheduleHeaderSettings.monthHeaderFormat<span class="type-signature type string">string</span>
{:#members-scheduleheadersettings-monthheaderformat}








Specified the format for month view in schedule header




Default Value:
{:.param}






* "MMM"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{monthHeaderFormat : "MMM" }
               });
&lt;/script&gt;              </code>
</pre>






### scheduleHeaderSettings.scheduleHeaderType<span class="type-signature type enum">enum</span>
{:#members-scheduleheadersettings-scheduleheadertype}








Specifies the schedule mode




Default Value:
{:.param}






* "week"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{scheduleHeaderType : "week"}
               });
&lt;/script&gt;              </code>
</pre>






### scheduleHeaderSettings.weekendBackground<span class="type-signature type string">string</span>
{:#members-scheduleheadersettings-weekendbackground}








Specified the background for weekends in gantt




Default Value:
{:.param}






* "#F2F2F2"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{weekendBackground : "#F2F2F2"}});
&lt;/script&gt;</code>
</pre>






### scheduleHeaderSettings.weekHeaderFormat<span class="type-signature type string">string</span>
{:#members-scheduleheadersettings-weekheaderformat}








Specified the format for week view in schedule header




Default Value:
{:.param}






* "ddd"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{weekHeaderFormat : "MMM dd , yyyy" }
               });
&lt;/script&gt;</code>
</pre>






### scheduleHeaderSettings.yearHeaderFormat<span class="type-signature type string">string</span>
{:#members-scheduleheadersettings-yearheaderformat}








Specified the format for year view in schedule header




Default Value:
{:.param}






* "yyyy"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{yearHeaderFormat : "yyyy" }
               });
&lt;/script&gt;               </code>
</pre>






### scheduleStartDate<span class="type-signature type string">string</span>
{:#members-schedulestartdate}








Specifies start date of the gantt schedule. By default, start date will be rounded to its previous Sunday.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt(
 {
    scheduleStartDate:"12/2/2000"
 });            
&lt;/script&gt;</code>
</pre>






### selectedItem<span class="type-signature type number">number</span>
{:#members-selecteditem}








Specifies the selected row index in gantt




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt(
 {
    selectedItem: 2
 });            
&lt;/script&gt;</code>
</pre>






### selectedRowIndex<span class="type-signature type number">number</span>
{:#members-selectedrowindex}








Specifies the selected row Index in gantt , the row with given index will highlighted




Default Value:
{:.param}






* "-1"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    selectedRowIndex:2
 });            
&lt;/script&gt;</code>
</pre>






### showColumnChooser<span class="type-signature type boolean">boolean</span>
{:#members-showcolumnchooser}








Enables or disables the column chooser.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;   
        $("#gantt").ejGantt({ showColumnChooser:  true });                      * 
&lt;/script&gt;</code>
</pre>






### showGridCellTooltip<span class="type-signature type boolean">boolean</span>
{:#members-showgridcelltooltip}








Specifies whether to show grid cell tooltip.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        showGridCellTooltip : true});
&lt;/script&gt;</code>
</pre>






### showGridExpandCellTooltip<span class="type-signature type boolean">boolean</span>
{:#members-showgridexpandcelltooltip}








Specifies whether to show grid cell tooltip over expander cell alone.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        showGridExpandCellTooltip : true});
&lt;/script&gt;</code>
</pre>






### showProgressStatus<span class="type-signature type boolean">boolean</span>
{:#members-showprogressstatus}








Specifies whether display task progress inside taskbar.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        showProgressStatus : true});
&lt;/script&gt;</code>
</pre>






### showResourceNames<span class="type-signature type boolean">boolean</span>
{:#members-showresourcenames}








Specifies whether to display resource names for a task beside taskbar.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        showResourceNames : true});
&lt;/script&gt;</code>
</pre>






### showTaskNames<span class="type-signature type boolean">boolean</span>
{:#members-showtasknames}








Specifies whether to display task name beside task bar.




Default Value:
{:.param}






* "true"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt({  
                        showTaskNames : true});
&lt;/script&gt;</code>
</pre>






### sizeSettings<span class="type-signature type object">object</span>
{:#members-sizesettings}








Specifies the size option of gantt control.











### sizeSettings.height<span class="type-signature type string">string</span>
{:#members-sizesettings-height}








Specifies the height of gantt control




Default Value:
{:.param}






* "450px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    sizeSettings:{height: "700px"}
 });            
&lt;/script&gt;</code>
</pre>






### sizeSettings.width<span class="type-signature type string">string</span>
{:#members-sizesettings-width}








Specifies the width of gantt control




Default Value:
{:.param}






* "1000px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    sizeSettings:{width: "700px"}
 });            
&lt;/script&gt;</code>
</pre>






### sortSettings<span class="type-signature type object">object</span>
{:#members-sortsettings}








Specifies the sorting options for gantt.











### sortSettings.sortedColumns<span class="type-signature type array">array</span>
{:#members-sortsettings-sortedcolumns}








Specifies the sorted columns for gantt




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt({ sortSettings{sortedColumns : []}});                  
&lt;/script&gt;</code>
</pre>






### splitterPosition<span class="type-signature type string">string</span>
{:#members-splitterposition}








Specifies splitter position in gantt.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                                  
        $("#gantt").ejGantt({  splitterPosition : "50%" });     
&lt;/script&gt;</code>
</pre>






### startDateMapping<span class="type-signature type string">string</span>
{:#members-startdatemapping}








Specifies the mapping property path for start date of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                                  
        $("#gantt").ejGantt({  startDateMapping : "startdate" });                
&lt;/script&gt;</code>
</pre>






### stripLines<span class="type-signature type string">string</span>
{:#members-striplines}








Specifies the options for striplines




Default Value:
{:.param}






* "[]"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(stripLines: [
   {
    day: "12/2/2000,
    label: "Project Release",
    lineStyle: "dotted",
    lineColor: "Darkblue",
    lineWidth: 2
  }
]); 
&lt;/script&gt;</code>
</pre>






### taskbarBackground<span class="type-signature type string">string</span>
{:#members-taskbarbackground}








Specifies the background of the taskbar in gantt




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt({  
                        taskbarBackground : "#F2F2F2"});
&lt;/script&gt;</code>
</pre>






### taskbarEditingTooltipTemplate<span class="type-signature type string">string</span>
{:#members-taskbareditingtooltiptemplate}








Specifies the template script for customized tooltip for taskbar editing in gantt




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    taskbarEditingTooltipTemplate: "tooltiptemplate"
 });            
&lt;/script&gt;</code>
</pre>






### taskbarEditingTooltipTemplateId<span class="type-signature type string">string</span>
{:#members-taskbareditingtooltiptemplateid}








Specifies the template Id for customized tooltip for taskbar editing in gantt




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    taskbarEditingTooltipTemplateId: "TooltipTemplateId"
 });            
&lt;/script&gt;</code>
</pre>






### taskbarTooltipTemplate<span class="type-signature type string">string</span>
{:#members-taskbartooltiptemplate}








Specifies the template for tooltip on mouseaction on taskbars




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                  
        $("#gantt").ejGantt(
 {
    taskbarTooltipTemplate: ""
 });            
&lt;/script&gt;</code>
</pre>






### taskbarTooltipTemplateId<span class="type-signature type string">string</span>
{:#members-taskbartooltiptemplateid}








Specifies the template id for tooltip on mouseaction on taskbars




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    taskbarTooltipTemplateId: ""
 });            
&lt;/script&gt;</code>
</pre>






### taskIdMapping<span class="type-signature type string">string</span>
{:#members-taskidmapping}








Specifies the mapping property path for task Id in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                                  
        $("#gantt").ejGantt({  taskIdMapping : "ID" }); 
&lt;/script&gt;</code>
</pre>






### taskNameMapping<span class="type-signature type string">string</span>
{:#members-tasknamemapping}








Specifies the mapping property path for task name in datasource




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt({  taskNameMapping : "Name" });     
&lt;/script&gt;</code>
</pre>






### toolbarSettings<span class="type-signature type object">object</span>
{:#members-toolbarsettings}








Specifies the toolbarSettings options.











### toolbarSettings.showToolBar<span class="type-signature type boolean">boolean</span>
{:#members-toolbarsettings-showtoolbar}








Specifies the state of enabling or disabling toolbar




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt({ showToolBar:  true });                     
&lt;/script&gt;</code>
</pre>






### toolbarSettings.toolbarItems<span class="type-signature type array">array</span>
{:#members-toolbarsettings-toolbaritems}








Specifies the list of toolbar items to rendered in toolbar




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;  
        $("#gantt").ejGantt({ toolbarItems: [ej.Gantt.ToolbarItems.Add,ej.Gantt.ToolbarItems.Edit] });                   
&lt;/script&gt;</code>
</pre>






### treeColumnIndex<span class="type-signature type number">number</span>
{:#members-treecolumnindex}








Specifies the tree expander column in gantt




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    treeColumnIndex: 1
 });            
&lt;/script&gt;</code>
</pre>






### weekendBackground<span class="type-signature type string">string</span>
{:#members-weekendbackground}








Specifies the weekendBackground color in gantt




Default Value:
{:.param}






* "#F2F2F2"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#gantt").ejGantt(
 {
    weekendBackground: "blue"
 });            
&lt;/script&gt;</code>
</pre>






### workingTimeScale<span class="type-signature type enum">enum</span>
{:#members-workingtimescale}








Specifies the working time schedule of day




Default Value:
{:.param}






* "TimeScale24"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;                          
        $("#gantt").ejGantt({  
                        workingTimeScale : "TimeScale24Hours" 
            });
&lt;/script&gt;</code>
</pre>




## Methods








### addRecord<span class="signature">()</span>
{:#methods-addrecord}








To add item in gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
var data = {taskId:"40",taskName:"New Task 40",startDate:"2/20/2014",startDate:"2/25/2014"};
gantObj.ejGantt("addRecord",data); // To add a task
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To add an item
var data = {taskId:"40",taskName:"New Task 40",startDate:"2/20/2014",startDate:"2/25/2014"};
$("#gantt").ejGantt("addRecord",data);  
&lt;/script&gt;</code>
</pre>






### cancelEdit<span class="signature">()</span>
{:#methods-canceledit}








To cancel the edited state of an item in gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("cancelEdit"); // To cancel edited
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To outdent a selected item in gantt
$("#gantt").ejGantt("cancelEdit");      
&lt;/script&gt;</code>
</pre>






### collapseAllItems<span class="signature">()</span>
{:#methods-collapseallitems}








To collapse all the parent items in gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("collapseAllItems"); // To collapse all parent items in gantt
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To expand all items
$("#gantt").ejGantt("collapseAllItems");        
&lt;/script&gt;</code>
</pre>






### deleteItem<span class="signature">()</span>
{:#methods-deleteitem}








To delete a selected item in gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("deleteItem"); // To delete a task
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To delete an item
$("#gantt").ejGantt("deleteItem");      
&lt;/script&gt;</code>
</pre>






### destroy<span class="signature">()</span>
{:#methods-destroy}








destroy the gantt widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create gantt
var gantt = $("#gantt").data("ejGantt");
gantt.destroy(); // destroy the gantt
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// enable the gantt
$("#gantt").ejGantt("destroy"); 
&lt;/script&gt;</code>
</pre>






### expandAllItems<span class="signature">()</span>
{:#methods-expandallitems}








To Expand all the parent items in gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("expandAllItems"); // To expand all parent items in gantt
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To expand all items
$("#gantt").ejGantt("expandAllItems");  
&lt;/script&gt;</code>
</pre>






### expandCollapseRecord<span class="signature">()</span>
{:#methods-expandcollapserecord}








To expand and collapse an item in gantt using item's ID





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("expandCollapseRecord" , "23"); // To expand collapse an item
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To expand collapse an item
$("#gantt").ejGantt("expandCollapseRecord" , "23");     
&lt;/script&gt;</code>
</pre>






### hideColumn<span class="signature">(width)</span>
{:#methods-hidecolumn}








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
<td class="name"><code>width</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a header text of a column to hide</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;gantt id="gantt"&gt;Gantt&lt;/gantt&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("hideColumn","Task Name");
&lt;/script&gt;</code>
</pre>






### indentItem<span class="signature">()</span>
{:#methods-indentitem}








To indent a selected item in gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("indentItem"); // To indent a selected item in gantt
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To indent a selected item in gantt
$("#gantt").ejGantt("indentItem");      
&lt;/script&gt;</code>
</pre>






### openAddDialog<span class="signature">()</span>
{:#methods-openadddialog}








To Open the dialog to add new task to the gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("openAddDialog"); // To open the add dialog
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// open Add dialog
$("#gantt").ejGantt("openAddDialog");   
&lt;/script&gt;</code>
</pre>






### openEditDialog<span class="signature">()</span>
{:#methods-openeditdialog}








To Open the dialog to edit existing task to the gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("openEditDialog"); // To open the add dialog
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// open Add dialog
$("#gantt").ejGantt("openEditDialog");  
&lt;/script&gt;</code>
</pre>






### outdentItem<span class="signature">()</span>
{:#methods-outdentitem}








To outdent a selected item in gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("outdentItem"); // To outdent a selected item in gantt
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To outdent a selected item in gantt
$("#gantt").ejGantt("outdentItem");     
&lt;/script&gt;</code>
</pre>






### saveEdit<span class="signature">()</span>
{:#methods-saveedit}








To save the edited state of an item in gantt





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("saveEdit"); // To save edited state of an item
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To expand collapse an item
$("#gantt").ejGantt("saveEdit");        
&lt;/script&gt;</code>
</pre>






### searchItem<span class="signature">()</span>
{:#methods-searchitem}








To search an item with search string provided at the run time





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("searchItem",$("#text").val()); // To search a task
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// To search a task
$("#gantt").ejGantt("searchItem",$("#text").val());     
&lt;/script&gt;</code>
</pre>






### setSplitterPosition<span class="signature">(width)</span>
{:#methods-setsplitterposition}








To set the grid width in gantt

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>width</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can give either percentage or pixels value</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="gantt"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("setSplitterPosition","40%");
&lt;/script&gt;</code>
</pre>






### showColumn<span class="signature">(width)</span>
{:#methods-showcolumn}








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
<td class="name"><code>width</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a header text of a column to show</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;gantt id="gantt"&gt;Gantt&lt;/gantt&gt; 
 
&lt;script&gt;
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("showColumn","Task Name");
&lt;/script&gt;</code>
</pre>




## Events








### actionBegin
{:#events-actionbegin}








Triggered for every gantt action before its starts.

<table class="params">
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
<td class="description last">Event parameters when gantt is initialized:
<table class="params">
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
<td class="description last">Event parameters while perform sorting in grid tree action starts:
<table class="params">
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
<td class="description last">Returns the gantt model.</td>
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
<td class="description last">Event parameters while searching action starts:
<table class="params">
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
<td class="description last">Returns the value of searching element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the gantt model.</td>
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
<td class="description last">Event parameterswhile performing the delete operation starts:
<table class="params">
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
<td class="description last">Returns the data od deleting element.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the gantt model.</td>
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
<td class="description last">Event parameters while performing the add operation starts:
<table class="params">
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
<td class="description last">Returns the data adding element.</td>
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
<td class="description last">Event parameters while performing the edit operation starts:
<table class="params">
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
<td class="description last">Returns the data edting element</td>
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
$("#gantt").ejGantt({
   actionBegin: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### actionComplete
{:#events-actioncomplete}








Triggered for every gantt action success event.

<table class="params">
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
<td class="description last">Event parameters when gantt is initialized:
<table class="params">
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
<td class="description last">Returns the gantt model.</td>
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
<td class="description last">Returns the gantt model.</td>
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
<td class="description last">Event parameterswhile performing after completing the delete operation is completed:
<table class="params">
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
<td class="description last">Returns the gantt model.</td>
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
$("#gantt").ejGantt({
   actionComplete: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### beginEdit
{:#events-beginedit}








Triggered while enter the edit mode in the tree grid cell

<table class="params">
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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   beginEdit: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### collapsed
{:#events-collapsed}








Triggered after collapsed the gantt record

<table class="params">
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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   collapsed: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### collapsing
{:#events-collapsing}








Triggered while collapsing the gantt record

<table class="params">
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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   collapsing: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### contextMenuOpen
{:#events-contextmenuopen}








Triggered while Context Menu is rendered in Gantt control

<table class="params">
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
<td class="description last">Returns the gantt model.</td>
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
$("#gantt").ejGantt({
   contextMenuOpen: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### endEdit
{:#events-endedit}








Triggered after save the modified cellValue in gantt.

<table class="params">
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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   endEdit: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### expanded
{:#events-expanded}








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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   expanded: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### expanding
{:#events-expanding}








Triggered while expanding the gantt record

<table class="params">
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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   expanding: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### load
{:#events-load}








Triggered while gantt is loaded

<table class="params">
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
<td class="description last">Returns the gantt model</td>
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
$("#gantt").ejGantt({
   load: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### queryCellInfo
{:#events-querycellinfo}








Triggered while rendering each cell in the tree grid

<table class="params">
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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   queryCellInfo: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### queryTaskbarInfo
{:#events-querytaskbarinfo}








Triggered while rendering each taskbar in the gantt chart

<table class="params">
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
<td class="description last">Arguments when queryTaskbarInfo event is triggered.
<table class="params">
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
<td class="name"><code>TaskbarBackground</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the taskbar background of current item.</td>
</tr>
<tr>
<td class="name"><code>ProgressbarBackground</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the progressbar background of current item.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of the record.</td>
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
$("#gantt").ejGantt({
   queryTaskbarInfo: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### rowDataBound
{:#events-rowdatabound}








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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   rowDataBound: function (args) {}
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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
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
&lt;div id="gantt"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#gantt").ejGantt({
   rowSelecting: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### taskbarEdited
{:#events-taskbaredited}








Triggered after completing the editing operation in taskbar

<table class="params">
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
<td class="description last">Arguments when taskbarEdited event is triggered.
<table class="params">
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
<td class="description last">Returns the data of edited record.</td>
</tr>
<tr>
<td class="name"><code>previousData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous data value of edited record.</td>
</tr>
<tr>
<td class="name"><code>dragging</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns 'true' if taskbar is dragged.</td>
</tr>
<tr>
<td class="name"><code>leftResizing</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns 'true' if taskbar is left resized.</td>
</tr>
<tr>
<td class="name"><code>rightResizing</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns 'true' if taskbar is right resized.</td>
</tr>
<tr>
<td class="name"><code>progressResizing</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns 'true' if taskbar is progress resized.</td>
</tr>
<tr>
<td class="name"><code>editingFields</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the field values of record being edited.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the gantt model.</td>
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
$("#gantt").ejGantt({
   taskbarEdited: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### taskbarEditing
{:#events-taskbarediting}








Triggered while editing the gantt chart (dragging, resizing the taskbar )

<table class="params">
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
<td class="description last">Arguments when taskbarEditing event is triggered.
<table class="params">
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
<td class="description last">Returns the gantt model.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row object being edited.</td>
</tr>
<tr>
<td class="name"><code>editingFields</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the field values of record being edited.</td>
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
$("#gantt").ejGantt({
   taskbarEditing: function (args) {}
});
&lt;/script&gt;</code>
</pre>



