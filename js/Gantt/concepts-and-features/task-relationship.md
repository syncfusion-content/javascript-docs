---
layout: post
title: task-relationship
description: task relationship
platform: js
control: Gantt
documentation: ug
---

# Task Relationship

You can show the relationship between two tasks in Gantt control. These relationships are categorized into four types based on the start and finish date of the task.

*  Start to Start(SS)

              You cannot start a task until the other task also starts.

![C:\Users\Rajasekar\Desktop\SS.png](task-relationship_images\task-relationship_img1.png)

* Start to Finish(SF)

You cannot finish a task until the other task is started.

![C:\Users\Rajasekar\Desktop\SF.png](task-relationship_images\task-relationship_img2.png)

* Finish to Start(FS)

             You cannot start a task until the other task is completed.

![C:\Users\Rajasekar\Desktop\FS.png](task-relationship_images\task-relationship_img3.png)



* Finish to Finish(FF)

    You cannot finish a task until the other task is completed.

![C:\Users\Rajasekar\Desktop\FF.png](task-relationship_images\task-relationship_img4.png)

The following code example shows you how to show the predecessor in the **Gantt** control.



{% highlight js %}


$("#GanttContainer ").ejGantt({
    //…
    predecessorMapping: "predecessor"
});


{% endhighlight %}







The following screenshot displays the output of the above code. 



{% include image.html url="\js\Gantt\concepts-and-features\task-relationship_images\task-relationship_img5.png" Caption="Figure 48: Task relationship"%}

