---
layout: post
title: Sequencing Tasks
description: sequencing tasks
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Serial Number

## How to enable serial number column in Gantt?

The serial or sequence number support in Gantt is used to index the tasks in a project. The Serial number column can be rendered by enabling the [`enableSerialNumber`](/api/js/ejgantt#members:enableSerialNumber) property. On enabling this property the serial number column will be displayed and the Task Id column will be hidden, the tasks will be identified using the serial numbers. Further the column values for task predecessors will also be displayed using the serial numbers of the corresponding tasks, instead of task IDs.

Code snippets for enabling the serial number is as follows.

{% highlight javascript %}

    $("#GanttSerialNumber").ejGantt({
        //...
        enableSerialNumber:true,
    });

{% endhighlight %}

The following screenshot displays the serial number column in Gantt control.

![](/js/Gantt/Serial-Number_images/Serial_img1.png)

The serial number column will be resequenced automatically on performing any actions which will change the row indexes of the tasks such as row deleting, adding, drag and drop.