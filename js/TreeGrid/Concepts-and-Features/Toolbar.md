---
layout: post
title: Toolbar
description: toolbar
platform: js
control: TreeGrid
documentation: ug
---

# Toolbar

**TreeGrid** control contains toolbar options for adding, deleting and editing the records. You can customize the **TreeGrid****Toolbar** tools by using **toolbarSettings** API. 

In **TreeGrid** by using **rowPosition** API, the index position for the newly added row can be provided. Default value of the **rowPosition** property is **top**. The Enum values for **rowPosition** API are,

* top

* bottom

* aboveSelectedRow

* belowSelectedRow

You can enable toolbar for **TreeGrid**, using the following code example.

{% highlight js %}

$("#TreeGridcontainer").ejTreeGrid(

                       //...
    editSettings: {
                   //...
                    rowPosition:”aboveSelectedRow”
                   },  

    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [
                  ej.TreeGrid.ToolbarItems.Add,                                                      
                  ej.TreeGrid.ToolbarItems.Edit,
                  ej.TreeGrid.ToolbarItems.Delete, 
                  ej.TreeGrid.ToolbarItems.Update,             
                  ej.TreeGrid.ToolbarItems.Cancel,   
                  ej.TreeGrid.ToolbarItems.ExpandAll                               
                  ej.TreeGrid.ToolbarItems.CollapseAll
                       ],
                    }

                //...
             });


{% endhighlight %}



The following screenshot displays the toolbar option in **TreeGrid** control.

{% include image.html url="/js/TreeGrid/Concepts-and-Features/Toolbar_images/Toolbar_img1.png" Caption="Toolbar option in TreeGrid"%}

