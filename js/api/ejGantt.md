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


{% highlight html %}
 
<gantt id="gantt">Gantt</gantt> 
 
<script>
// Create Gantt
$('#gantt').ejGantt();  
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.globalize.js


* module:jquery.easing.1.3.js


* module:jsrender.js


* module:ej.web.all.js




## Members








### addDialogFields<span class="type-signature type array">Array</span>
{:#members:adddialogfields}








Specifies the fields to be included in the add dialog in gantt




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    addDialogFields: [{ field: "taskId", editType: "stringedit" }]
 });            
</script>{% endhighlight %}







### allowColumnResize<span class="type-signature type boolean">boolean</span>
{:#members:allowcolumnresize}








Enables or disables the ability to resize column.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                   
        $("#gantt").ejGantt({ allowColumnResize:  true });                      * 
</script>{% endhighlight %}







### allowGanttChartEditing<span class="type-signature type boolean">boolean</span>
{:#members:allowganttchartediting}








Enables or Disables gantt chart editing in gantt




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    allowGanttChartEditing:true
 });            
</script>{% endhighlight %}







### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members:allowkeyboardnavigation}








Enables or Disables Keyboard navigation in gantt




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ allowKeyboardNavigation : true});                 
</script>{% endhighlight %}







### allowMultiSorting<span class="type-signature type boolean">boolean</span>
{:#members:allowmultisorting}








Specifies enabling or disabling multiple soting for gantt columns




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ allowMultiSorting : true});                       
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
 
<div id="gantt"></div> 
<script>   
        $("#gantt").ejGantt({ allowSelection:  true });                 * 
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
 
<div id="gantt"></div> 
<script>        
        $("#gantt").ejGantt({ allowSorting:  true });            
</script>{% endhighlight %}







### baselineColor<span class="type-signature type string">string</span>
{:#members:baselinecolor}








Specifies the baseline background color in gantt




Default Value:
{:.param}






* "#fba41c"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt(
 {
    baselineColor: "blue"
 });            
</script>{% endhighlight %}







### baselineEndDateMapping<span class="type-signature type string">string</span>
{:#members:baselineenddatemapping}








Specifies the mapping property path for baseline end date in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  baselineEndDateMapping : "BaselineEndDate" });
</script>{% endhighlight %}







### baselineStartDateMapping<span class="type-signature type string">string</span>
{:#members:baselinestartdatemapping}








Specifies the mapping property path for baseline start date of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  baselineStartDateMapping : "BaselineStartDate" });               
</script>{% endhighlight %}







### childMapping<span class="type-signature type string">string</span>
{:#members:childmapping}








Specifies the mapping property path for sub tasks in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  childMapping : "Children" });
</script>{% endhighlight %}







### connectorLineBackground<span class="type-signature type string">string</span>
{:#members:connectorlinebackground}








Specifies the background of connector lines in Gantt




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        connectorLineBackground : "#F2F2F2"});
</script>{% endhighlight %}







### connectorlineWidth<span class="type-signature type number">number</span>
{:#members:connectorlinewidth}








Specifies the width of the connector lines in gantt




Default Value:
{:.param}






* "1"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        connectorlineWidth : 1 });
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Specify the CSS class for gantt to achieve custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  cssClass : "gradient-lime" });
</script>{% endhighlight %}







### dataSource<span class="type-signature type array">array</span>
{:#members:datasource}








Collection of data or hierarchical data to represent in gantt




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    dataSource:[{Id:2,TaskName:"Testing",startDate:"12/1/2000",Duration:5 }]    
 });            
</script>{% endhighlight %}







### dateFormat<span class="type-signature type string">string</span>
{:#members:dateformat}








Specifies the dateFormat for gantt , given format is displayed in tooltip , grid .




Default Value:
{:.param}






* "MM/dd/yyyy"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    dateFormat: "dd/MM/yyyy"
 });            
</script>{% endhighlight %}







### durationMapping<span class="type-signature type string">string</span>
{:#members:durationmapping}








Specifies the mapping property path for duration of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  durationMapping : "Duration" });
</script>{% endhighlight %}







### durationUnit<span class="type-signature type enum">enum</span>
{:#members:durationunit}








Specifies the duration unit for each tasks whether days or hours




Default Value:
{:.param}






* "day"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        durationUnit : day });
</script>{% endhighlight %}







### editDialogFields<span class="type-signature type array">Array</span>
{:#members:editdialogfields}








Specifies the fields to be included in the edit dialog in gantt




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    editDialogFields: [{ field: "taskId", editType: "stringedit" }]
 });            
</script>{% endhighlight %}







### editSettings<span class="type-signature type object">object</span>
{:#members:editsettings}








Specifies the editSettings options in gantt.











### editSettings.allowAdding<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowadding}








Enables or disables add record icon in gantt toolbar




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{allowAdding : true} });
</script>{% endhighlight %}







### editSettings.allowDeleting<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowdeleting}








Enables or disables delete icon in gantt toolbar




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{allowDeleting : true} });  
</script>{% endhighlight %}







### editSettings.allowEditing<span class="type-signature type boolean">boolean</span>
{:#members:editsettings-allowediting}








Specifies the option for enabling or disablig editing in gantt grid part




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{allowEditing : true} });   
</script>{% endhighlight %}







### editSettings.editMode<span class="type-signature type string">string</span>
{:#members:editsettings-editmode}








Specifies the editmode in gantt , "normal" is for dialog editing ,"cellEditing" is for cell type editing




Default Value:
{:.param}






* normal








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  editSettings:{editMode : "normal"} });
</script>{% endhighlight %}







### enableAltRow<span class="type-signature type boolean">boolean</span>
{:#members:enablealtrow}








Enables or Disables enableAltRow row effect in gantt




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ enableAltRow : true});                    
</script>{% endhighlight %}







### enableCollapseAll<span class="type-signature type boolean">boolean</span>
{:#members:enablecollapseall}








Enables or disables the collapse all records when loading the gantt.




Default Value:
{:.param}






* "false"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    enableCollapseAll: false
 });            
</script>{% endhighlight %}







### enableContextMenu<span class="type-signature type boolean">boolean</span>
{:#members:enablecontextmenu}








Enables or disables the contextmenu for gantt , when enabled contextmenu appears on right clicking gantt




Default Value:
{:.param}






* "false"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    enableContextMenu: false
 });            
</script>{% endhighlight %}







### enableProgressBarResizing<span class="type-signature type boolean">boolean</span>
{:#members:enableprogressbarresizing}








Indicates whether we can edit the progress of a task interactively in gantt chart.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ enableProgressBarResizing:  true });                      
</script>{% endhighlight %}







### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}








Enables or disables the option for dynamically updating the Gantt size on window resizing




Default Value:
{:.param}






* "false"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    enableResize: false
 });            
</script>{% endhighlight %}







### enableTaskbarDragTooltip<span class="type-signature type boolean">boolean</span>
{:#members:enabletaskbardragtooltip}








Enables or disables tooltip while editing (dragging/resizing) the taskbar.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        enableTaskbarDragTooltip : true});
</script>{% endhighlight %}







### enableTaskbarTooltip<span class="type-signature type boolean">boolean</span>
{:#members:enabletaskbartooltip}








Enables or disables tooltip for taskbar.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  enableTaskbarTooltip : true });  
</script>{% endhighlight %}







### enableVirtualization<span class="type-signature type boolean">boolean</span>
{:#members:enablevirtualization}








Enables/Disables virtualization for rendering gantt items.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({ enableVirtualization : true});                    
</script>{% endhighlight %}







### endDateMapping<span class="type-signature type string">string</span>
{:#members:enddatemapping}








Specifies the mapping property path for end Date of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  endDateMapping : "EndDate" });   
</script>{% endhighlight %}







### highlightWeekends<span class="type-signature type boolean">boolean</span>
{:#members:highlightweekends}








Specifies whether to highlight the weekends in gantt .




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ highlightWeekends:  true });                      * 
</script>{% endhighlight %}







### holidays<span class="type-signature type array">array</span>
{:#members:holidays}








Collection of holidays with date, background and label information to be displayed in gantt.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt(
 {
   holidays:[{day:"12/2/2000",background:"cyan",label:"local holiday" }]        
 });            
</script>{% endhighlight %}







### includeWeekend<span class="type-signature type boolean">boolean</span>
{:#members:includeweekend}








Specifies whether to include weekends while calculating the duration of a task.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ includeWeekend:  true });                 
</script>{% endhighlight %}







### locale<span class="type-signature type string">string</span>
{:#members:locale}








Specify the locale for gantt




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  locale : "it-IT" });
</script>{% endhighlight %}







### milestoneMapping<span class="type-signature type string">string</span>
{:#members:milestonemapping}








Specifies the mapping property path for milestone in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  milestoneMapping : "milestone" });       
</script>{% endhighlight %}







### parentProgressbarBackground<span class="type-signature type string">string</span>
{:#members:parentprogressbarbackground}








Specifies the background of parent progressbar in gantt




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        parentProgressbarBackground : "#F2F2F2"});
</script>{% endhighlight %}







### parentTaskbarBackground<span class="type-signature type string">string</span>
{:#members:parenttaskbarbackground}








Specifies the background of parent taskbar in gantt




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        parentTaskbarBackground : "#F2F2F2"});
</script>{% endhighlight %}







### parentTaskIdMapping<span class="type-signature type string">string</span>
{:#members:parenttaskidmapping}








Specifies the mapping property path for parent task Id in selfreference datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  parentTaskIdMapping : "ID" });               
</script>{% endhighlight %}







### predecessorMapping<span class="type-signature type string">string</span>
{:#members:predecessormapping}








Specifies the mapping property path for predecessors of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  predecessorMapping : "predecessor" });           
</script>{% endhighlight %}







### progressbarBackground<span class="type-signature type string">string</span>
{:#members:progressbarbackground}








Specifies the background of progressbar in gantt




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({  
                        progressbarBackground : "#F2F2F2"});
</script>{% endhighlight %}







### progressbarHeight<span class="type-signature type number">number</span>
{:#members:progressbarheight}








Specified the height of the progressbar in taskbar




Default Value:
{:.param}






* "100"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  
                        progressbarHeight : 100 });
</script>{% endhighlight %}







### progressbarTooltipTemplate<span class="type-signature type string">string</span>
{:#members:progressbartooltiptemplate}








Specifies the template for tooltip on resizing progressbar




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    progressbarTooltipTemplate: ""
 });            
</script>{% endhighlight %}







### progressbarTooltipTemplateId<span class="type-signature type string">string</span>
{:#members:progressbartooltiptemplateid}








Specifies the template ID for customized tooltip for progressbar editing in gantt




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt(
 {
    progressbarTooltipTemplateId: "tooltiptemplateID"
 });            
</script>{% endhighlight %}







### progressMapping<span class="type-signature type string">string</span>
{:#members:progressmapping}








Specifies the mapping property path for progress percentage of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  progressMapping : "progress" });                 
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
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt(
 {
    query:ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);      
 });            
</script>{% endhighlight %}







### renderBaseline<span class="type-signature type boolean">boolean</span>
{:#members:renderbaseline}








Enables or Disables rendering baselines in Gantt , when enabled baseline is rendered in gantt




Default Value:
{:.param}






* "false"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    renderBaseline: false
 });            
</script>{% endhighlight %}







### resourceIdMapping<span class="type-signature type string">string</span>
{:#members:resourceidmapping}








Specifies the mapping property name for resource ID in resource Collection in gantt




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt(
 {
    resourceIdMapping: "peopleID"
 });            
</script>{% endhighlight %}







### resourceInfoMapping<span class="type-signature type string">string</span>
{:#members:resourceinfomapping}








Specifies the mapping property path for resources of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  resourceInfoMapping : "resources" });    
</script>{% endhighlight %}







### resourceNameMapping<span class="type-signature type string">string</span>
{:#members:resourcenamemapping}








Specifies the mapping property path for resource name of a task in gantt




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    resourceNameMapping: "EmployeeName"
 });            
</script>{% endhighlight %}







### resources<span class="type-signature type array">array</span>
{:#members:resources}








Collection of data regarding resources involved in entire project




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
   resources:[{id:1; name:"jack" }]     
 });            
</script>{% endhighlight %}







### roundOffDayworkingTime<span class="type-signature type boolean">boolean</span>
{:#members:roundoffdayworkingtime}








Specifies whether rounding off the day working time edits




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        roundOffDayworkingTime : true });
</script>{% endhighlight %}







### rowHeight<span class="type-signature type number">number</span>
{:#members:rowheight}








Specifies the height of a single row in gantt. Also, we need to set same height in the CSS style with class name e-rowcell.




Default Value:
{:.param}






* "30"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        rowHeight : 30,
                        });
</script>{% endhighlight %}







### scheduleEndDate<span class="type-signature type string">string</span>
{:#members:scheduleenddate}








Specifies end date of the gantt schedule. By default, end date will be rounded to its next Saturday.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt(
 {
    scheduleEndDate:"12/2/2000"
 });            
</script>{% endhighlight %}







### scheduleHeaderSettings<span class="type-signature type object">object</span>
{:#members:scheduleheadersettings}








Specifies the options for customizing schedule header.











### scheduleHeaderSettings.dayHeaderFormat<span class="type-signature type string">string</span>
{:#members:scheduleheadersettings-dayheaderformat}








Specified the format for day view in schedule header




Default Value:
{:.param}






* "ddd"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{dayHeaderFormat : "ddd" }
                });
</script>              {% endhighlight %}







### scheduleHeaderSettings.hourHeaderFormat<span class="type-signature type string">string</span>
{:#members:scheduleheadersettings-hourheaderformat}








Specified the format for Hour view in schedule header




Default Value:
{:.param}






* "HH"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{hourHeaderFormat : 'HH'}
                });
</script>               {% endhighlight %}







### scheduleHeaderSettings.minutesPerInterval<span class="type-signature type enum">enum</span>
{:#members:scheduleheadersettings-minutesperinterval}








Specifies the number of minutes per interval




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{minutesPerInterval : "oneMinute"}});              
</script>              {% endhighlight %}







### scheduleHeaderSettings.monthHeaderFormat<span class="type-signature type string">string</span>
{:#members:scheduleheadersettings-monthheaderformat}








Specified the format for month view in schedule header




Default Value:
{:.param}






* "MMM"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{monthHeaderFormat : "MMM" }
               });
</script>              {% endhighlight %}







### scheduleHeaderSettings.scheduleHeaderType<span class="type-signature type enum">enum</span>
{:#members:scheduleheadersettings-scheduleheadertype}








Specifies the schedule mode




Default Value:
{:.param}






* "week"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{scheduleHeaderType : "week"}
               });
</script>              {% endhighlight %}







### scheduleHeaderSettings.weekendBackground<span class="type-signature type string">string</span>
{:#members:scheduleheadersettings-weekendbackground}








Specified the background for weekends in gantt




Default Value:
{:.param}






* "#F2F2F2"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{weekendBackground : "#F2F2F2"}});
</script>{% endhighlight %}







### scheduleHeaderSettings.weekHeaderFormat<span class="type-signature type string">string</span>
{:#members:scheduleheadersettings-weekheaderformat}








Specified the format for week view in schedule header




Default Value:
{:.param}






* "ddd"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{weekHeaderFormat : "MMM dd , yyyy" }
               });
</script>{% endhighlight %}







### scheduleHeaderSettings.yearHeaderFormat<span class="type-signature type string">string</span>
{:#members:scheduleheadersettings-yearheaderformat}








Specified the format for year view in schedule header




Default Value:
{:.param}






* "yyyy"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        scheduleHeaderSettings:{yearHeaderFormat : "yyyy" }
               });
</script>               {% endhighlight %}







### scheduleStartDate<span class="type-signature type string">string</span>
{:#members:schedulestartdate}








Specifies start date of the gantt schedule. By default, start date will be rounded to its previous Sunday.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt(
 {
    scheduleStartDate:"12/2/2000"
 });            
</script>{% endhighlight %}







### selectedItem<span class="type-signature type number">number</span>
{:#members:selecteditem}








Specifies the selected row index in gantt




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt(
 {
    selectedItem: 2
 });            
</script>{% endhighlight %}







### selectedRowIndex<span class="type-signature type number">number</span>
{:#members:selectedrowindex}








Specifies the selected row Index in gantt , the row with given index will highlighted




Default Value:
{:.param}






* "-1"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    selectedRowIndex:2
 });            
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
 
<div id="gantt"></div> 
<script>   
        $("#gantt").ejGantt({ showColumnChooser:  true });                      * 
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
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
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
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showGridExpandCellTooltip : true});
</script>{% endhighlight %}







### showProgressStatus<span class="type-signature type boolean">boolean</span>
{:#members:showprogressstatus}








Specifies whether display task progress inside taskbar.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showProgressStatus : true});
</script>{% endhighlight %}







### showResourceNames<span class="type-signature type boolean">boolean</span>
{:#members:showresourcenames}








Specifies whether to display resource names for a task beside taskbar.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showResourceNames : true});
</script>{% endhighlight %}







### showTaskNames<span class="type-signature type boolean">boolean</span>
{:#members:showtasknames}








Specifies whether to display task name beside task bar.




Default Value:
{:.param}






* "true"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt({  
                        showTaskNames : true});
</script>{% endhighlight %}







### sizeSettings<span class="type-signature type object">object</span>
{:#members:sizesettings}








Specifies the size option of gantt control.











### sizeSettings.height<span class="type-signature type string">string</span>
{:#members:sizesettings-height}








Specifies the height of gantt control




Default Value:
{:.param}






* "450px"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    sizeSettings:{height: "700px"}
 });            
</script>{% endhighlight %}







### sizeSettings.width<span class="type-signature type string">string</span>
{:#members:sizesettings-width}








Specifies the width of gantt control




Default Value:
{:.param}






* "1000px"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    sizeSettings:{width: "700px"}
 });            
</script>{% endhighlight %}







### sortSettings<span class="type-signature type object">object</span>
{:#members:sortsettings}








Specifies the sorting options for gantt.











### sortSettings.sortedColumns<span class="type-signature type array">array</span>
{:#members:sortsettings-sortedcolumns}








Specifies the sorted columns for gantt




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({ sortSettings{sortedColumns : []}});                  
</script>{% endhighlight %}







### splitterPosition<span class="type-signature type string">string</span>
{:#members:splitterposition}








Specifies splitter position in gantt.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                                  
        $("#gantt").ejGantt({  splitterPosition : "50%" });     
</script>{% endhighlight %}







### startDateMapping<span class="type-signature type string">string</span>
{:#members:startdatemapping}








Specifies the mapping property path for start date of a task in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                                  
        $("#gantt").ejGantt({  startDateMapping : "startdate" });                
</script>{% endhighlight %}







### stripLines<span class="type-signature type string">string</span>
{:#members:striplines}








Specifies the options for striplines




Default Value:
{:.param}






* "[]"








Example
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
</script>{% endhighlight %}







### taskbarBackground<span class="type-signature type string">string</span>
{:#members:taskbarbackground}








Specifies the background of the taskbar in gantt




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({  
                        taskbarBackground : "#F2F2F2"});
</script>{% endhighlight %}







### taskbarEditingTooltipTemplate<span class="type-signature type string">string</span>
{:#members:taskbareditingtooltiptemplate}








Specifies the template script for customized tooltip for taskbar editing in gantt




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    taskbarEditingTooltipTemplate: "tooltiptemplate"
 });            
</script>{% endhighlight %}







### taskbarEditingTooltipTemplateId<span class="type-signature type string">string</span>
{:#members:taskbareditingtooltiptemplateid}








Specifies the template Id for customized tooltip for taskbar editing in gantt




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    taskbarEditingTooltipTemplateId: "TooltipTemplateId"
 });            
</script>{% endhighlight %}







### taskbarTooltipTemplate<span class="type-signature type string">string</span>
{:#members:taskbartooltiptemplate}








Specifies the template for tooltip on mouseaction on taskbars




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                  
        $("#gantt").ejGantt(
 {
    taskbarTooltipTemplate: ""
 });            
</script>{% endhighlight %}







### taskbarTooltipTemplateId<span class="type-signature type string">string</span>
{:#members:taskbartooltiptemplateid}








Specifies the template id for tooltip on mouseaction on taskbars




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    taskbarTooltipTemplateId: ""
 });            
</script>{% endhighlight %}







### taskIdMapping<span class="type-signature type string">string</span>
{:#members:taskidmapping}








Specifies the mapping property path for task Id in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                                  
        $("#gantt").ejGantt({  taskIdMapping : "ID" }); 
</script>{% endhighlight %}







### taskNameMapping<span class="type-signature type string">string</span>
{:#members:tasknamemapping}








Specifies the mapping property path for task name in datasource




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt({  taskNameMapping : "Name" });     
</script>{% endhighlight %}







### toolbarSettings<span class="type-signature type object">object</span>
{:#members:toolbarsettings}








Specifies the toolbarSettings options.











### toolbarSettings.showToolBar<span class="type-signature type boolean">boolean</span>
{:#members:toolbarsettings-showtoolbar}








Specifies the state of enabling or disabling toolbar




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ showToolBar:  true });                     
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
 
<div id="gantt"></div> 
<script>  
        $("#gantt").ejGantt({ toolbarItems: [ej.Gantt.ToolbarItems.Add,ej.Gantt.ToolbarItems.Edit] });                   
</script>{% endhighlight %}







### treeColumnIndex<span class="type-signature type number">number</span>
{:#members:treecolumnindex}








Specifies the tree expander column in gantt




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    treeColumnIndex: 1
 });            
</script>{% endhighlight %}







### weekendBackground<span class="type-signature type string">string</span>
{:#members:weekendbackground}








Specifies the weekendBackground color in gantt




Default Value:
{:.param}






* "#F2F2F2"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>          
        $("#gantt").ejGantt(
 {
    weekendBackground: "blue"
 });            
</script>{% endhighlight %}







### workingTimeScale<span class="type-signature type enum">enum</span>
{:#members:workingtimescale}








Specifies the working time schedule of day




Default Value:
{:.param}






* "TimeScale24"








Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
<script>                          
        $("#gantt").ejGantt({  
                        workingTimeScale : "TimeScale24Hours" 
            });
</script>{% endhighlight %}





## Methods








### addRecord<span class="signature">()</span>
{:#methods:addrecord}








To add item in gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
var data = {taskId:"40",taskName:"New Task 40",startDate:"2/20/2014",startDate:"2/25/2014"};
gantObj.ejGantt("addRecord",data); // To add a task
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To add an item
var data = {taskId:"40",taskName:"New Task 40",startDate:"2/20/2014",startDate:"2/25/2014"};
$("#gantt").ejGantt("addRecord",data);  
</script>{% endhighlight %}







### cancelEdit<span class="signature">()</span>
{:#methods:canceledit}








To cancel the edited state of an item in gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("cancelEdit"); // To cancel edited
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To outdent a selected item in gantt
$("#gantt").ejGantt("cancelEdit");      
</script>{% endhighlight %}







### collapseAllItems<span class="signature">()</span>
{:#methods:collapseallitems}








To collapse all the parent items in gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("collapseAllItems"); // To collapse all parent items in gantt
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To expand all items
$("#gantt").ejGantt("collapseAllItems");        
</script>{% endhighlight %}







### deleteItem<span class="signature">()</span>
{:#methods:deleteitem}








To delete a selected item in gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("deleteItem"); // To delete a task
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To delete an item
$("#gantt").ejGantt("deleteItem");      
</script>{% endhighlight %}







### destroy<span class="signature">()</span>
{:#methods:destroy}








destroy the gantt widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create gantt
var gantt = $("#gantt").data("ejGantt");
gantt.destroy(); // destroy the gantt
</script>{% endhighlight %}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// enable the gantt
$("#gantt").ejGantt("destroy"); 
</script>{% endhighlight %}







### expandAllItems<span class="signature">()</span>
{:#methods:expandallitems}








To Expand all the parent items in gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("expandAllItems"); // To expand all parent items in gantt
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To expand all items
$("#gantt").ejGantt("expandAllItems");  
</script>{% endhighlight %}







### expandCollapseRecord<span class="signature">()</span>
{:#methods:expandcollapserecord}








To expand and collapse an item in gantt using item's ID





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("expandCollapseRecord" , "23"); // To expand collapse an item
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To expand collapse an item
$("#gantt").ejGantt("expandCollapseRecord" , "23");     
</script>{% endhighlight %}







### hideColumn<span class="signature">(width)</span>
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
width{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a header text of a column to hide</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<gantt id="gantt">Gantt</gantt> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("hideColumn","Task Name");
</script>{% endhighlight %}







### indentItem<span class="signature">()</span>
{:#methods:indentitem}








To indent a selected item in gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("indentItem"); // To indent a selected item in gantt
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To indent a selected item in gantt
$("#gantt").ejGantt("indentItem");      
</script>{% endhighlight %}







### openAddDialog<span class="signature">()</span>
{:#methods:openadddialog}








To Open the dialog to add new task to the gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("openAddDialog"); // To open the add dialog
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// open Add dialog
$("#gantt").ejGantt("openAddDialog");   
</script>{% endhighlight %}







### openEditDialog<span class="signature">()</span>
{:#methods:openeditdialog}








To Open the dialog to edit existing task to the gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("openEditDialog"); // To open the add dialog
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// open Add dialog
$("#gantt").ejGantt("openEditDialog");  
</script>{% endhighlight %}







### outdentItem<span class="signature">()</span>
{:#methods:outdentitem}








To outdent a selected item in gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("outdentItem"); // To outdent a selected item in gantt
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To outdent a selected item in gantt
$("#gantt").ejGantt("outdentItem");     
</script>{% endhighlight %}







### saveEdit<span class="signature">()</span>
{:#methods:saveedit}








To save the edited state of an item in gantt





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("saveEdit"); // To save edited state of an item
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To expand collapse an item
$("#gantt").ejGantt("saveEdit");        
</script>{% endhighlight %}







### searchItem<span class="signature">()</span>
{:#methods:searchitem}








To search an item with search string provided at the run time





Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("searchItem",$("#text").val()); // To search a task
</script>{% endhighlight %}


{% highlight html %}
 
 <div id="gantt"></div> 
 
<script>
// To search a task
$("#gantt").ejGantt("searchItem",$("#text").val());     
</script>{% endhighlight %}







### setSplitterPosition<span class="signature">(width)</span>
{:#methods:setsplitterposition}








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
<td class="name">{% highlight html %}
width{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can give either percentage or pixels value</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="gantt"></div> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("setSplitterPosition","40%");
</script>{% endhighlight %}







### showColumn<span class="signature">(width)</span>
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
width{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">you can pass a header text of a column to show</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<gantt id="gantt">Gantt</gantt> 
 
<script>
// Create Gantt
var ganttObj = $("#gantt").data("ejGantt");
gantObj.ejGantt("showColumn","Task Name");
</script>{% endhighlight %}





## Events








### actionBegin
{:#events:actionbegin}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="description last">Returns the gantt model.</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
keyValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the value of searching element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the gantt model.</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data od deleting element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the gantt model.</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data adding element.</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the data edting element</td>
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
$("#gantt").ejGantt({
   actionBegin: function (args) {}
});
</script>{% endhighlight %}







### actionComplete
{:#events:actioncomplete}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="description last">Returns the gantt model.</td>
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
<td class="description last">Returns the gantt model.</td>
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
<td class="description last">Returns the gantt model.</td>
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
$("#gantt").ejGantt({
   actionComplete: function (args) {}
});
</script>{% endhighlight %}







### beginEdit
{:#events:beginedit}








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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   beginEdit: function (args) {}
});
</script>{% endhighlight %}







### collapsed
{:#events:collapsed}








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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   collapsed: function (args) {}
});
</script>{% endhighlight %}







### collapsing
{:#events:collapsing}








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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   collapsing: function (args) {}
});
</script>{% endhighlight %}







### contextMenuOpen
{:#events:contextmenuopen}








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
<td class="description last">Returns the gantt model.</td>
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
$("#gantt").ejGantt({
   contextMenuOpen: function (args) {}
});
</script>{% endhighlight %}







### endEdit
{:#events:endedit}








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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   expanded: function (args) {}
});
</script>{% endhighlight %}







### expanding
{:#events:expanding}








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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   expanding: function (args) {}
});
</script>{% endhighlight %}







### load
{:#events:load}








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
<td class="description last">Returns the gantt model</td>
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
$("#gantt").ejGantt({
   load: function (args) {}
});
</script>{% endhighlight %}







### queryCellInfo
{:#events:querycellinfo}








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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   queryCellInfo: function (args) {}
});
</script>{% endhighlight %}







### queryTaskbarInfo
{:#events:querytaskbarinfo}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
TaskbarBackground{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the taskbar background of current item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
ProgressbarBackground{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the progressbar background of current item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   queryTaskbarInfo: function (args) {}
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   rowDataBound: function (args) {}
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
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
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   rowSelecting: function (args) {}
});
</script>{% endhighlight %}







### taskbarEdited
{:#events:taskbaredited}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data of edited record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
previousData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous data value of edited record.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
dragging{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns 'true' if taskbar is dragged.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
leftResizing{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns 'true' if taskbar is left resized.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rightResizing{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns 'true' if taskbar is right resized.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
progressResizing{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns 'true' if taskbar is progress resized.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
editingFields{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the field values of record being edited.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="gantt"></div> 
<script>
$("#gantt").ejGantt({
   taskbarEdited: function (args) {}
});
</script>{% endhighlight %}







### taskbarEditing
{:#events:taskbarediting}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the gantt model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the row object being edited.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
editingFields{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the field values of record being edited.</td>
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
$("#gantt").ejGantt({
   taskbarEditing: function (args) {}
});
</script>{% endhighlight %}




