---
layout: post
title: Task-Relationship
description: task relationship
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Task Relationship

You can show the relationship between two tasks in Gantt control. These relationships are categorized into four types based on the start and finish date of the task.

## Start to Start(SS)

You cannot start a task until the other task also starts.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img1.png)

## Start to Finish(SF)

You cannot finish a task until the other task is started.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img2.png)

## Finish to Start(FS)

You cannot start a task until the other task is completed.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img3.png)

## Finish to Finish(FF)

You cannot finish a task until the other task is completed.

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img4.png)

The following code example shows you how to show the predecessor in the Gantt control.

{% highlight javascript %}

    $("#GanttContainer ").ejGantt({
        //...
        predecessorMapping: "predecessor"
    });
    
{% endhighlight %}

The following screenshot displays the output of the above code. 

![](/js/Gantt/Task-Relationship_images/Task-Relationship_img5.png)

