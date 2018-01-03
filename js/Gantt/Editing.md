---
layout: post
title: Editing
description: editing
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Editing

The Gantt control provides in-built support to add, insert and update the tasks. The following are the types of editing available in Gantt.

* Cell Editing
* Normal Editing
* Taskbar Editing
* Predecessor Editing

## Cell Editing

Update the task details through grid cell editing by setting [editMode](/api/js/ejgantt#members:editsettings-editmode "editSettings.editMode") as `cellEditing`.

The following code example shows you how to enable the `cellEditing` in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "cellEditing"
        }
    });

{% endhighlight %}

The output of Gantt with cellEditing is as follows.

![](/js/Gantt/Editing_images/Editing_img1.png)

## Normal Editing

Update the task details through edit dialog by setting [editMode](/api/js/ejgantt#members:editsettings-editmode "editSettings.editMode") as `normal`.

The following code example shows you how to enable normal editing in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "normal"
        }
    });

{% endhighlight %}

The following screenshot shows the output of `normal` editing.

![](/js/Gantt/Editing_images/Editing_img2.png)

## Taskbar Editing

Update the task details by interactions such as resizing and dragging the taskbar. Taskbar editing can be enabled by setting [allowGanttChartEditing](/api/js/ejgantt#members:allowganttchartediting) as `true`. The following code example shows you how to enable taskbar resizing in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowGanttChartEditing: true
    });

{% endhighlight %}

You can also enable or disable the progressbar resizing by using the [enableProgressbarResizing](/api/js/ejgantt#members:enableprogressbarresizing). The following code example shows how to disable this property.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        enableProgressBarResizing: false,
    });

{% endhighlight %}

## Predecessor Editing

Update the predecessor details of a task using mouse interactions. The following code example shows how to enable predecessor editing.

{% highlight javascript %}

          $("#GanttContainer").ejGantt({
              //...
              dataSource: data,
              allowGanttChartEditing: true,
              predecessorMapping: "predecessor",
          });

{% endhighlight %}

The following screen shot shows the predecessor editing in Gantt control.

![](/js/Gantt/Editing_images/Editing_img3.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/editing) here to view the online demo sample for editing in Gantt.

## Delete confirmation message

Delete confirmation message is used to get the confirmation from the user before delete the record. This confirmation message can be enabled by setting [showDeleteConfirmDialog](/api/js/ejgantt#members:editsettings-showdeleteconfirmdialog "editSettings.showDeleteConfirmDialog") property as `true`.

The following code snippet explains how to enable delete confirmation message in Gantt.

{% highlight js %}

$("#Gantt").ejGantt({
     //...
    editSettings: {
        allowDeleting: true,
	    showDeleteConfirmDialog: true
    },
    //...
});


{% endhighlight %}

![](/js/Gantt/Editing_images/deleteConfirmation.png)

The above screen shot shows the appearance of delete confirmation message in Gantt.