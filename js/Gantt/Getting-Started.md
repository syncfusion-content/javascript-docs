---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Getting Started

This section explains briefly about how to create a Gantt chart in your application with JavaScript.

## Create your first Gantt in JavaScript

This tutorial explains about how to create a simple Gantt chart, add tasks or subtasks and set relationship between tasks during the design phase of a software project. The following screenshot displays the desired output after completing this tutorial.

![](/js/Gantt/Getting-Started_images/Getting-Started_img4.png)

## Adding script references
Create an HTML file and add the following template to the HTML file.

{% highlight html %}

    <!DOCTYPE html>

    <html xmlns="http://www.w3.org/1999/xhtml">

    <head>

        <title>Getting Started with Gantt Control for JavaScript</title>

        <!-- style sheet for default theme(flat azure) -->
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

        <!--scripts-->
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

        <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js "></script>

    </head>

    <body>
        <!--Add  Gantt control here-->
    </body>

    </html>

{% endhighlight %}

## Binding Gantt with data
Create data source for ejGantt.

{% highlight javascript %}

    var data = [{
        taskID: 1,
        taskName: "Design",
        startDate: "02/10/2014",
        endDate: "02/14/2014",
        duration: 6,          
        subtasks: [
            {
                taskID: 2,
                taskName: "Software Specification",
                startDate: "02/10/2014",
                endDate: "02/12/2014",
                duration: 4,
                progress: "60",
                resourceId: [2]
            },
            {
                taskID: 3,
                taskName: "Develop prototype",
                startDate: "02/10/2014",
                endDate: "02/12/2014",
                duration: 4,
                progress: "70",
                resourceId: [3]
            },
            {
                taskID: 4,
                taskName: "Get approval from customer",
                startDate: "02/12/2014",
                endDate: "02/14/2014",
                duration: 2,
                progress: "80",
                predecessor: "3FS",
                resourceId: [1]
            },
            {
                taskID: 5,
                taskName: "Design complete",
                startDate: "02/14/2014",
                endDate: "02/14/2014",
                duration: 0,
                predecessor: "4FS"
            }
        ]
    }];

{% endhighlight %}

## Initialize Gantt
Add a **&lt;div&gt;** element with in the &lt;Body&gt; tag.

{% highlight html %}

    <body>    
        <!--Add  Gantt control here-->    
        <div id="GanttContainer"></div>    
    </body>

{% endhighlight %}


Initialize the Gantt with data source created in the last step. To render Gantt tasks we need to set the value for [`taskIdMapping`](/api/js/ejgantt#members:taskidmapping), [`taskNameMapping`](/api/js/ejgantt#members:tasknamemapping), [`startDateMapping`](/api/js/ejgantt#members:startdatemapping), [`endDateMapping`](/api/js/ejgantt#members:enddatemapping)/[`durationMapping`](/api/js/ejgantt#members:durationmapping), [`progressMapping`](/api/js/ejgantt#members:progressmapping), [`childMapping`](/api/js/ejgantt#members:childmapping) properties.


{% highlight javascript %}

    $(function() {
        $("#GanttContainer").ejGantt({
            dataSource: data, //Provides data source for Gantt
            taskIdMapping: "taskID", //Provide name of the property which contains task id in the data source
            taskNameMapping: "taskName", //Provide name of the property which contains task name in the data source
            scheduleStartDate: "02/01/2014", //Provide schedule header start date
            scheduleEndDate: "03/14/2014", //Provide schedule header end date
            startDateMapping: "startDate", //Provide name of the property which contains start date of the task in the data source
            durationMapping: "duration", //Provide name of the property which contains duration of the task in the data source
            progressMapping: "progress", //Provide name of the property which contains progress of the task in the data source
            childMapping: "subtasks", //Provide name of the property which contains subtask of the task in the data source
        });
    });

{% endhighlight %}

A Gantt chart is created as shown in the following screen shot.

![](/js/Gantt/Getting-Started_images/Getting-Started_img5.png)

## Enable Toolbar

Gantt control contains toolbar options to edit, search, expand or collapse all records, indent, outdent, delete and add a task. You can enable toolbar using the [`toolbarSettings`](/api/js/ejgantt#members:toolbarsettings "toolbarSettings") property.

{% highlight javascript %}
$("#GanttContainer").ejGantt({
    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [
            ej.Gantt.ToolbarItems.Add,
            ej.Gantt.ToolbarItems.Edit,
            ej.Gantt.ToolbarItems.Delete,
            ej.Gantt.ToolbarItems.Update,
            ej.Gantt.ToolbarItems.Cancel,
            ej.Gantt.ToolbarItems.Indent,
            ej.Gantt.ToolbarItems.Outdent,
            ej.Gantt.ToolbarItems.ExpandAll,
            ej.Gantt.ToolbarItems.CollapseAll,
            ej.Gantt.ToolbarItems.Search
        ],
    }
});

{% endhighlight %}

The following screen shot displays a Tool bar in Gantt control:

![](/js/Gantt/Getting-Started_images/Getting-Started_img6.png)

N>  Add, edit and delete options are enabled when enabling the [`allowEditing`](/api/js/ejgantt#members:editsettings-allowediting "editSettings.allowEditing"), [`allowAdding`](/api/js/ejgantt#members:editsettings-allowadding "editSettings.allowAdding") and [`allowDeleting`](/api/js/ejgantt#members:editsettings-allowdeleting "editSettings.allowDeleting") properties in the edit options.

## Enable Sorting

The Gantt control has sorting functionality to arrange the tasks in ascending or descending order based on a particular column.

### Multicolumn Sorting

You can enable the multicolumn sorting in Gantt by setting the [`allowSorting`](/api/js/ejgantt#members:allowsorting) and [`allowMultiSorting`](/api/js/ejgantt#members:allowmultisorting "allowMultiSorting") as `true`. You can sort multiple columns in Gantt, by selecting the desired column header while holding the <kbd>CTRL</kbd> key.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
         //...
         allowSorting:true,
         allowMultiSorting: true,
    });

{% endhighlight %}

## Enable Editing

You can enable editing using the [`editSettings`](/api/js/ejgantt#members:editsettings) and [`allowGanttChartEditing`](/api/js/ejgantt#members:allowganttchartediting) options.

### Cell Editing

Modify the task details through the grid cell editing by setting the [`editMode`](/api/js/ejgantt#members:editsettings-editmode "editSettings.editMode") as `cellEditing`.

### Normal Editing

Modify the task details through the edit dialog by setting the [`editMode`](/api/js/ejgantt#members:editsettings-editmode "editSettings.editMode") as `normal`.

### Taskbar Editing

Modify the task details through user interaction such as resizing and dragging the taskbar by setting the [`allowGanttChartEditing`](/api/js/ejgantt#members:allowganttchartediting) as `true`.

### Predecessor Editing

Modify the predecessor details of a task using mouse interactions by setting the [`allowGanttChartEditing`](/api/js/ejgantt#members:allowganttchartediting "allowGanttChartEditing") as `true` and setting value for the [`predecessorMapping`](/api/js/ejgantt#members:predecessormapping) property.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowGanttChartEditing:true, //enable the taskbar editing 
        predecessorMapping:"predecessor" ,// Predecessor editing 
        editSettings: {
            allowEditing: true,
            allowAdding: true,
            allowDeleting: true,
            editMode:"normal",
        },
    });

{% endhighlight %}

The following screen shot displays a Gantt control with dialog editing option.

![](/js/Gantt/Getting-Started_images/Getting-Started_img7.png)

N>  By default `cellEditing` and `normal` editing operations are performed through double-click action and it can be changed to click action by setting [`beginEditAction`](/api/js/ejgantt#members:editsettings-begineditaction "editSettings.beginEditAction") property as `click`.

## Enable Context Menu

You can enable the context menu in Gantt, by setting the [`enableContextMenu`](/api/js/ejgantt#members:enablecontextmenu "enableContextMenu") as `true`.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({   
        //...
        enableContextMenu:true
    });

{% endhighlight %}

The following screen shot displays Gantt chart in which Context menu option is enabled:

![](/js/Gantt/Getting-Started_images/Getting-Started_img8.png)

## Enable Column Menu

You can enable the column menu in Gantt, by setting the [`showColumnChooser`](/api/js/ejgantt#members:showcolumnchooser "showColumnChooser") as `true`.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({   
        //...
        showColumnChooser:true
    });


{% endhighlight %}

The following screen shot displays Gantt control in which column chooser option is enabled:

![](/js/Gantt/Getting-Started_images/Getting-Started_img11.png)

## Provide tasks relationship

In Gantt, you have the predecessor support to show the relationship between two different tasks.

* **Start to Start (SS)** - You cannot start a task until the other task also starts.
* **Start to Finish (SF)** - You cannot finish a task until the other task finishes.
* **Finish to Start (FS)** - You cannot start a task until the other task completes.
* **Finish to Finish (FF)** - You cannot finish a task until the other task completes.

You can show the relationship in tasks, by using the [`predecessorsMapping`](/api/js/ejgantt#members:predecessormapping "predecessorsMapping") property as shown in the following code example.

{% highlight javascript %}

    $("# GanttContainer ").ejGantt({                
       //...
       predecessorMapping: "predecessor"
    });

{% endhighlight %}

The following screenshot displays the relationship between tasks.

![](/js/Gantt/Getting-Started_images/Getting-Started_img9.png)

## Provide Resources

In Gantt control, you can display and assign the resource for each task. Create a collection of `JSON` object, which contains id and name of the resource and assign it to the [`resources`](/api/js/ejgantt#members:resources "resources") property. Then, specify the field name for id and name of the resource in the resource collection to [`resourceIdMapping`](/api/js/ejgantt#members:resourceidmapping "resourceIdMapping") and [`resourceNameMapping`](/api/js/ejgantt#members:resourcenamemapping "resourceNameMapping") options. The name of the field, which contains the actual resources assigned for a particular task in the [`dataSource`](/api/js/ejgantt#members:datasource) is specified using the [`resourceInfoMapping`](/api/js/ejgantt#members:resourceinfomapping "resourceInfoMapping").

1.Create the resource collection to be displayed in ejGantt.

{% highlight javascript %}

    var projectResources =[{
        resourceId: 1,
        resourceName: "Project Manager"
    },{
        resourceId: 2,
        resourceName: "Software Analyst"
    },{
        resourceId: 3,
        resourceName: "Developer"
    },{
        resourceId: 4,
        resourceName: "Testing Engineer"
    }];

{% endhighlight %}

2.Initialize the Gantt with resources created in last step. 

{% highlight javascript %}

    $("# GanttContainer ").ejGantt({
        //...
        resourceInfoMapping: "resourceId", //Field name which contains resource details for the task 
        resourceNameMapping: "resourceName",//resource Name mapping
        resourceIdMapping: "resourceId",//resource Id Mapping
        resources: projectResources,//resource collection dataSource
    });

{% endhighlight %}

The following screenshot displays resource allocation for tasks in Gantt chart.

![](/js/Gantt/Getting-Started_images/Getting-Started_img10.png)

By following these steps, you have learned how to provide data source to Gantt chart, how to configure Gantt to set task relationships, assign resources for each task and add toolbar with necessary buttons.

## Highlight Weekend

In Gantt, you can on or off weekends high lighting by setting the [`highlightWeekEnds`](/api/js/ejgantt#members:highlightweekends "highlightWeekEnds") as `true` or `false`.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({   
        //...
        highlightWeekEnds:false
    });

{% endhighlight %}

The following screen shot displays Gantt chart in which highlight weekends is disabled:

![](/js/Gantt/Getting-Started_images/Getting-Started_img12.png)

## Define dimension of Gantt

By default Gantt control was rendered with `100%` width and `450px` height, we can define the dimension of Gantt control by using [`sizeSettings`](/api/js/ejgantt#members:sizesettings) property. Gantt control width and height can be defined by either [`height`](/api/js/ejgantt#members:sizesettings-height "sizeSettings.height") and [`width`](/api/js/ejgantt#members:sizesettings-width "sizeSettings.width") properties or by defining inline style in Gantt container element. The below code example shows how to define width and height for Gantt control.

{% highlight html %}

<!--<div id="GanttContainer" style="width:700px;height:350px"></div>-->
<div id="GanttContainer"></div>

<script>
    $("#GanttContainer").ejGantt({   
        //...
        sizeSettings:{
            width: "700px",
            height: "350px"
        }
    });
</script>

{% endhighlight %}

N> Gantt control will automatically update the width and height value based on container element on window resize action, this can be enabled by setting [`isResponsive`](/api/js/ejgantt#members:isresponsive) property as `true` for this [`height`](/api/js/ejgantt#members:sizesettings-height "sizeSettings.height") and [`width`](/api/js/ejgantt#members:sizesettings-width "sizeSettings.width") value will be defined in percentage.

## Add notes in tasks

In Gantt, we can add additional information about the tasks, this information can be defined in data source and this field was mapped to Gantt control by using [`notesMapping`](/api/js/ejgantt#members:notesmapping) property. Notes values can be defined as string or in HTML string format. This notes content was displayed in `Notes` column and notes value can be updated by using cell editing and dialog editing. The following code example shows how to use the [`notesMapping`](/api/js/ejgantt#members:notesmapping) property.

{% highlight javascript %}

var data = [
    //...
    {
        taskID: 4, 
        taskName: "Develop prototype",
        notesContent: "we can show additional information here",
        //...
    },
    //...
];

$("#GanttContainer").ejGantt({
    //...
    dataSource: data,
    notesMapping: "notesContent",
});

{% endhighlight %}

The below screenshot shows the output of above code example.
![](/js/Gantt/Getting-Started_images/Getting-Started_img13.png)
Notes column in Gantt
{:.caption}

![](/js/Gantt/Getting-Started_images/Getting-Started_img14.png)
Editing notes in edit dialog
{:.caption}

N> Notes value was displayed as plain text in Grid part and also when we edit the notes value by cell editing, value was stored as string value. We can use edit dialog to update the notes value of task in HTML string format.

## Milestones in Gantt

Milestones are used to denote the important event/stages in project management. Milestones start date and end date value will be same and duration value was `0`. Gantt tasks are rendered as milestone if the task duration value was `0` and we will define task was milestone or not in data source and this field was mapped to Gantt by using [`milestoneMapping`](/api/js/ejgantt#members:milestonemapping) property. The below code example shows how to use this property.

{% highlight javascript %}

var data = [
    //...
    {
        taskID: 4, 
        taskName: "Develop prototype",
        isMileStone: false,
        //..
    },
    {
        taskID: 5, 
        taskName: "Get approval from customer",
        startDate: new Date("02/10/2014"),
        endDate: new Date("02/14/2014"),
        duration: 2,
        isMileStone: true,
    },
    //...
];

$("#GanttContainer").ejGantt({
    //...
    dataSource: data,
    milestoneMapping: "isMileStone",
});

{% endhighlight %}

The below screenshot shows the output of above code example.
![](/js/Gantt/Getting-Started_images/Getting-Started_img15.png)