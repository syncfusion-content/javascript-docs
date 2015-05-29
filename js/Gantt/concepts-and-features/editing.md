---
layout: post
title: editing
description: editing
platform: js
control: Gantt
documentation: ug
---

# Editing

The **Gantt** control provides built-in support to add, insert and update the task inside **Gantt**. **Gantt** provides three types of editing, they are:

* Cell Editing

* Normal Editing

* Taskbar Editing

* Predecessor Editing



## Cell Editing

Update the task details through grid cell editing by setting **editMode** as **cellEditing**.

The following code example shows you how to enable **cellEditing** in **Gantt** control.



{% highlight js %}


$("#GanttContainer").ejGantt({
    //...
    editSettings: {
        allowEditing: true,
        editMode: "cellEditing"
    }
});


{% endhighlight %}







The output of **Gantt** with **cellEditing** is as follows.



{% include image.html url="\js\Gantt\concepts-and-features\editing_images\editing_img1.png" Caption="Figure 37: Gantt with cellEdit"%}

## Normal Editing

Update the task details through edit dialog by setting **EditMode** as **normal.**

The following code example shows you how to enable normal editing in **Gantt** control.



{% highlight js %}


$("#GanttContainer").ejGantt({
    //...
    editSettings: {
        allowEditing: true,
        editMode: "normal"   
 }
});


{% endhighlight %}







The following screenshot shows the output of normal editing.



{% include image.html url="\js\Gantt\concepts-and-features\editing_images\editing_img2.png" Caption="Figure 38: Normal Editing"%}

## Taskbar Editing

Update the task details by interactions such as resizing and dragging the taskbar. The following code example shows you how to enable taskbar resizing in **Gantt** control.



{% highlight js %}


$("#GanttContainer").ejGantt({
    //...
    allowGanttChartEditing:true
});


{% endhighlight %}









## Predecessor Editing

Update the predecessor details of a task using mouse interactions. The following code example shows how to enable predecessor editing.

{% highlight js %}


  $("#GanttContainer").ejGantt({
                //….
                dataSource: data,
                allowGanttChartEditing:true,
                predecessorMapping: "predecessor",
              });


{% endhighlight %}







The following screen shot shows the predecessor editing in **Gantt** control.

![C:\Users\labuser\Desktop\hello.png](editing_images\editing_img3.png)

_Figure_ _39__: Predecessor Editing_

