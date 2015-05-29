---
layout: post
title: editing
description: editing
platform: js
control: TreeGrid
documentation: ug
---

# Editing

The **TreeGrid** control provides built-in support for **Editing** cell items. 

**Cell Editing**

Update the task details through grid **Cell Editing** by setting **editMode** as **cellEditing**.

The following code example shows you how to enable **cellEditing** in **TreeGrid** control.



{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
                //...
                editSettings: {

                    allowEditing: true,
                    editMode: "cellEditing"

                },
});


{% endhighlight %}







The output of **TreeGrid** with **cellEditing** is as follows.



{% include image.html url="\js\TreeGrid\concepts-and-features\editing_images\editing_img1.png" Caption="Figure 25: Cell Editing"%}



