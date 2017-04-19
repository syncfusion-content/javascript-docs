---
layout: post
title: Toolbar
description: toolbar
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Toolbar

Gantt control contains toolbar options for editing, searching, expanding and collapsing all records, indent, out dent, delete and add task. You can enable toolbar using the following code example.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        toolbarSettings: {
            showToolbar: true,
            toolbarItems: [
                ej.Gantt.ToolbarItems.Add, //TO ADD THE NEW TASK 
                ej.Gantt.ToolbarItems.Edit, //TO MODIFY THE SELECTED TASK DETAILS
                ej.Gantt.ToolbarItems.Delete, //TO DELETE THE SELECTED TASK
                ej.Gantt.ToolbarItems.Update, //TO SAVE THE MODIFIED TASK DETAILS
                ej.Gantt.ToolbarItems.Cancel, //TO CANCEL THE MODIFIED TASK DETAILS
                ej.Gantt.ToolbarItems.Indent, //TO INDENT THE SELECTED TASK 
                ej.Gantt.ToolbarItems.Outdent, //TO OUTDENT THE SELECTED TASK
                ej.Gantt.ToolbarItems.ExpandAll, //TO EXPAND ALL THE TASKS IN GANTT
                ej.Gantt.ToolbarItems.CollapseAll, //TO COLLAPSE ALL THE TASK IN GANTT
                ej.Gantt.ToolbarItems.Search, //TO FIND THE TASK
            ],
        }
    });


{% endhighlight %}

The following screenshot shows the toolbar option in Gantt control.

![](/js/Gantt/Toolbar_images/Toolbar_img1.png)

