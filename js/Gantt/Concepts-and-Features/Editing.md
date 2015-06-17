---
layout: post
title: Editing
description: editing
platform: js
control: Gantt
documentation: ug
---

# Editing

The **Gantt** control provides built-in support to add, insert and update the task inside **Gantt**. **Gantt** provides three types of editing, they are:

*Cell Editing

*Normal Editing

*Taskbar Editing

*Predecessor Editing

### Cell Editing

Update the task details through grid cell editing by setting editMode as cellEditing.

The following code example shows you how to enable cellEditing in Gantt control.

{% highlight js %}


    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "cellEditing"
        }
    });


{% endhighlight %}



The output of Gantt with cellEditing is as follows.

{% include image.html url="/js/Gantt/Concepts-and-Features/Editing_images/Editing_img1.png" Caption="Gantt with cellEdit"%}

### Normal Editing

Update the task details through edit dialog by setting **EditMode** as normal.

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

{% include image.html url="/js/Gantt/Concepts-and-Features/Editing_images/Editing_img2.png" Caption="Normal Editing"%}

### Taskbar Editing

Update the task details by interactions such as resizing and dragging the taskbar. The following code example shows you how to enable taskbar resizing in **Gantt** control.

{% highlight js %}


    $("#GanttContainer").ejGantt({
        //...
        allowGanttChartEditing:true
    });


{% endhighlight %}

### Predecessor Editing

Update the predecessor details of a task using mouse interactions. The following code example shows how to enable predecessor editing.

{% highlight js %}


          $("#GanttContainer").ejGantt({
                //...
                dataSource: data,
                allowGanttChartEditing:true,
                predecessorMapping: "predecessor",
              });


{% endhighlight %}



The following screen shot shows the predecessor editing in **Gantt** control.

{% include image.html url="/js/Gantt/Concepts-and-Features/Editing_images/Editing_img3.png" Caption="Predecessor Editing"%}

