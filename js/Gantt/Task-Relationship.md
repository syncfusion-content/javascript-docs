---
layout: post
title: Task-Relationship
description: task relationship
platform: js
control: Gantt
documentation: ug
---

# Task Relationship

You can show the relationship between two tasks in Gantt control. These relationships are categorized into four types based on the start and finish date of the task.

**Start to Start(SS)**

You cannot start a task until the other task also starts.

{% include image.html url="/js/Gantt/Task-Relationship_images/Task-Relationship_img1.png" Caption="Start to Start(SS)"%}

**Start to Finish(SF)**

You cannot finish a task until the other task is started.

{% include image.html url="/js/Gantt/Task-Relationship_images/Task-Relationship_img2.png" Caption="Start to Finish(SF)"%}

**Finish to Start(FS)**

You cannot start a task until the other task is completed.

{% include image.html url="/js/Gantt/Task-Relationship_images/Task-Relationship_img3.png" Caption="Finish to Start(FS)"%}

**Finish to Finish(FF)**

You cannot finish a task until the other task is completed.

{% include image.html url="/js/Gantt/Task-Relationship_images/Task-Relationship_img4.png" Caption="Finish to Finish(FF)"%}

The following code example shows you how to show the predecessor in the **Gantt** control.

{% highlight js %}


    $("#GanttContainer ").ejGantt({
        //...
        predecessorMapping: "predecessor"
    });


{% endhighlight %}



The following screenshot displays the output of the above code. 

{% include image.html url="/js/Gantt/Task-Relationship_images/Task-Relationship_img5.png" Caption="Task relationship"%}

