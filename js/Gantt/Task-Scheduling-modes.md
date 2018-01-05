---
layout: post
title: Task-scheduling-modes
description: Task scheduling modes
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Task Scheduling Modes

The Gantt provides support for automatic and manual task scheduling modes. Scheduling mode of a task is used to indicate whether the start and end dates of a task will be automatically validated or not. Using the property [`taskSchedulingMode`](/api/js/ejgantt#members:taskschedulingmode) we can able to change the scheduling mode of a task. The following are the enumeration values that can be set to the property [`taskSchedulingMode`](/api/js/ejgantt#members:taskschedulingmode).

* auto
* manual
* custom

## Automatically Scheduled Tasks

When the [`taskSchedulingMode`](/api/js/ejgantt#members:taskschedulingmode) property is set as `auto` scheduling mode, all the tasks in the project will be rendered as automatically scheduled tasks. Thus the start and end dates of the tasks in the project will be automatically validated. The tasks will be automatically scheduled based on the factors such as dependencies between the tasks, non-working days like holidays and weekends. Tasks automatically recalculate the scheduling date when its predecessor task has been affected. But still we can schedule the tasks and reset the start and end dates by manual editing. Summary tasks will also be automatically scheduled, but its start date, end date and duration values cannot be edited manually. 

{% highlight javascript %}

$("#GanttContainer").ejGantt({

    //...

    taskSchedulingMode: ej.Gantt.TaskSchedulingMode.Auto

});

{% endhighlight %}

N> Automatic scheduling mode is the default task scheduling mode in Gantt.

## Manually Scheduled Tasks

When the [`taskSchedulingMode`](/api/js/ejgantt#members:taskschedulingmode) property is set as `manual` scheduling mode, all the tasks in the project will be rendered as manually scheduled tasks. Thus the dates of the tasks will not get validated automatically by the system. The tasks will not get rescheduled and dates will not be recalculated automatically based on the factors such as task dependencies and non-working days and hence manual scheduled tasks will lie on weekends and holidays. We can restrict this mode in predecessor editing alone, that is we can make to automatically validate the dates of the manual tasks on predecessor editing by enabling the property [`validateManualTasksOnLinking`](/api/js/ejgantt#members:validatemanualtasksonlinking). By enabling this property, the dates of the manual tasks will recalculate automatically, when its predecessor tasks' dates have been changed.

{% highlight javascript %}

$("#GanttContainer").ejGantt({

    //...

    taskSchedulingMode: ej.Gantt.TaskSchedulingMode.Manual,

    validateManualTasksOnLinking: false,

    //...

});

{% endhighlight %}

## Custom

When the [`taskSchedulingMode`](/api/js/ejgantt#members:taskschedulingmode) property is set as `custom`, the scheduling mode for each tasks will be mapped form the data source field. The property [`taskSchedulingModeMapping`](/api/js/ejgantt#members:taskschedulingmodemapping) is used to map the scheduling mode field from the data source.

{% highlight javascript %}

 var data = [{
         "TaskID": 1,
         "TaskName": "Parent Task 1",
         "StartDate": new Date("02/23/2014"),
         "EndDate": new Date("02/27/2014"),
         "Progress": "40",
         `"isManual": true,`
         "Children": [{
                 "TaskID": 2,
                 "TaskName": "Child Task 1",
                 "StartDate": new Date("02/23/2014"),
                 "EndDate": new Date("02/27/2014"),
                 "Progress": "40"
             },
             {
                 "TaskID": 3,
                 "TaskName": "Child Task 2",
                 "StartDate": new Date("02/23/2014"),
                 "EndDate": new Date("02/27/2014"),
                 "Progress": "40",
                 `"isManual": true`
             }
         ]
     },
     //...
 ]

$("#GanttContainer").ejGantt({

    dataSource: data,

    //...
    taskSchedulingMode: ej.Gantt.TaskSchedulingMode.Custom,
    
    taskSchedulingModeMapping: "isManual", //Mapping type of task mode to Gantt

});

{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/schedulingconcepts/taskschedulemodes) here to view the online demo sample for task scheduling modes.

The following screen shot depicts a project with custom scheduling mode, where both automatic and manual scheduling modes are mapped to the tasks.

![](/js/Gantt/Task-Scheduling-modes_images/Task-Scheduling-modes_img1.png)