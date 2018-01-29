---
layout: post
title: Update-Task-Id-Value
description: Update Task Id Value
platform: js
control: Gantt
documentation: ug
---

# Update task id value

Id value of Gantt tasks can be changed dynamically by using [`updateTaskId`](/api/js/ejgantt#methods:updatetaskid "updateTaskId(currentId, newId)") method. The below code example shows how to invoke this method on button click action.

{% highlight javascript %}
    $("#Gantt").ejGantt({
        //...
    });

    $("#update_task_id").click(function () {
        var ganttObj = $("#Gantt").ejGantt("instance");
        ganttObj.updateTaskId(5, 7);
    });

{% endhighlight %}

The below screen shows the output of above code example.

![](/js/Gantt/How-to/Update-Task-Id_images/Update-Task-Id_img1.png)
Before id update
{:.caption}

![](/js/Gantt/How-to/Update-Task-Id_images/Update-Task-Id_img2.png)
After id update
{:.caption}