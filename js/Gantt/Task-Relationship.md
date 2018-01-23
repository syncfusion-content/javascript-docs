---
layout: post
title: Task-Dependency
description: task dependencies
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Task Dependencies

Task dependencies or task relationship can be established between two task in Gantt. This dependencies effect the project schedule, if we change the predecessor of one task it will affect the successor task, which effect next task and so on.

## Task Relationship Types

Task relationships are categorized into four types based on the start and finish date of the task.

### Start to Start(SS)

You cannot start a task until the other task also starts.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img1.png)

### Start to Finish(SF)

You cannot finish a task until the other task is started.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img2.png)

### Finish to Start(FS)

You cannot start a task until the other task is completed.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img3.png)

### Finish to Finish(FF)

You cannot finish a task until the other task is completed.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img4.png)


## Define task relationship

Task relationships are defined in data source as string value and this values are mapped to Gantt control by using [`predecessorMapping`](/api/js/ejgantt#members:predecessormapping) property. The following code example shows you how to enable the predecessor in the Gantt control.

{% highlight javascript %}

var data = [
    //...
    {
        taskID: 4, 
        taskName: "Develop prototype"
        //...
    },
    {
        taskID: 5, 
        taskName: "Get approval from customer",
        predecessor: "4FS",
        //...
    },
    {
        taskID: 6,
        taskName: "Design complete",
        predecessor: "5FS",
        //...
    }
];

$("#GanttContainer").ejGantt({
    //...
    dataSource: data,
    predecessorMapping: "predecessor",
});

{% endhighlight %}

The following screenshot displays the output of the above code. 

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img5.png)

## Predecessor offset with duration units

In Gantt, predecessor offset can be defined with the following duration units. 

* Day
* Hour
* Minute

We can define offset with various offset duration units for predecessors by using the below code example.

{% highlight javascript %}

var data = [
    //...
    {
        //...
        predecessor: "3FS+2d",
    },
    { 
        //...
        predecessor: "3FS+16h"
    },
    { 
        //...
        predecessor: "3FS+960m"
    }
];
$("#GanttContainer").ejGantt({
    //...
    dataSource: data,
    predecessorMapping: "predecessor",
});

{% endhighlight %}

The following screen shot depicts the duration unit support in the predecessor offset.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img6.png)

## Enable/disable predecessor validation

By default Gantt tasks date values are validated as per predecessor task and it's relationship type, we can disable/enable this validation by using [`enablePredecessorValidation`](/api/js/ejgantt#members:enablepredecessorvalidation) property. The following code example shows how to disable predecessor validation in Gantt.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
    dataSource: data,
    predecessorMapping: "predecessor",
    enablePredecessorValidation: false,
});

{% endhighlight %}

The below screenshot shows the output of above code example.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img8.png)
Predecessor validation disabled mode
{:.caption}

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img9.png)
Predecessor validation enabled mode
{:.caption}

## Validate predecessor links on editing

In Gantt, it is possible to validate the taskbar editing based on the predecessor connections. Below are the following ways to validate the taskbar editing.

* Using actionBegin event 
* Using validation dialog

### Using actionBegin event


The [`actionBegin`](/api/js/ejgantt#events:actionbegin) event with requestType argument as **validateLinkedTask** will be triggered when editing a task with predecessor links.

It is possible to validate the editing within the [`actionBegin`](/api/js/ejgantt#events:actionbegin) event using the **validateMode** event argument. The validateMode event argument has the following properties.

<table>
<tr>
<td>
Argument<br/><br/></td><td>
Default value<br/><br/></td><td>
Description<br/><br/></td></tr>
<tr>
<td>
args.validateMode.respectLink<br/><br/></td><td>
false<br/><br/></td><td>
In this validation mode, the predecessor links will be considered as high priority. With this mode enabled, when the successor task is moved before predecessor task’s end date, the editing will be reverted and dates will be validated based on the dependency links.<br/><br/><br/><br/></td></tr>
<tr>
<td>
args.validateMode.removeLink<br/><br/></td><td>
false<br/><br/></td><td>
In this validation mode, the taskbar editing will be considered as high priority, where in the case of inappropriate task dates the dependency links will be removed and tasks will be moved to the edited date.<br/><br/><br/><br/></td></tr>
<tr>
<td>
args.validateMode.preserveLinkWithEditing<br/><br/></td><td>
true<br/><br/></td><td>
In this validation mode, taskbar editing will be considered along with the dependency links. There will be no validations in task editing.<br/><br/><br/><br/></td></tr>
</table>

By default, the **preserveLinkWithEditing** validation mode will be enabled thus the validations will not occur when editing the linked tasks. 

The below code snippet explains enabling the **respectLink** validation mode while editing the linked tasks in the [`actionBegin`](/api/js/ejgantt#events:actionbegin) event.


{% highlight javascript %}

$("#GanttContainer").ejGantt({
    actionBegin: function(args) {
        if (args.requestType == "validateLinkedTask") {
            args.validateMode.respectLink = true;
        }
    },
});

{% endhighlight %}

### Using validation dialog

When disabling all the validation modes in the [`actionBegin`](/api/js/ejgantt#events:actionbegin) event, a validation popup will be displayed prompting the user to select the validation mode to validate taskbar editing.

This validation popup will display different options based on the successor task’s start date after editing.

If the user moved the successor task, that starts after predecessor task’s end date then the dialog will be rendered with below options,

* Cancel, Keep the existing link.
* Remove the link and move the task to start on edited date.
* Move the task to start on edited date and keep the link.

If the user moved the successor task, that starts before the predecessor task’s end date then the dialog will be rendered with below options.

* Cancel, Keep the existing link.
* Remove the link and move the task to start on edited date.

The following code example explains this.


{% highlight javascript %}

$("#GanttContainer").ejGantt({
    actionBegin: function(args) {
        if (args.requestType == "validateLinkedTask") {
            args.validateMode.preserveLinkWithEditing = false;
        }
    },
});

{% endhighlight %}

In this case, if the user dragging action violated the predecessor type then the following dialog will be rendered to perform operation.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img7.png)

