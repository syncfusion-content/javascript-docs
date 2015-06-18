---
layout: post
title: Context-Menu
description: context menu
platform: js
control: Gantt
documentation: ug
---

# Context Menu

**Default Context Menu**

The default context menu contains the following options.

* Task Details

* Add New Task

* Indent

* Outdent

* Delete

The following code example shows you how to enable the default context menu in **Gantt** control.

{% highlight js %}

    $("#GanttContainer").ejGantt({
        //...
        enableContextMenu:true
    });

{% endhighlight %}

The following screenshot shows the **Default Context Menu** in **Gantt** control.

{% include image.html url="/js/Gantt/Context-Menu_images/Context-Menu_img1.png" Caption="Default Context Menu"%}

**Custom Context Menu**

You can add custom context menu option in **Gantt** control. The following code example shows you how to add the custom context menu option in **Gantt** control.

{% highlight js %}

    $("#GanttContainer").ejGantt({
        //...
        contextMenuOpen: function (args) {
            args.contextMenuItems.push(
            {
                headerText: "ExpandAll",
                iconPath: "url(../images/Expand All.png)",
                evenHandler: function () {
                    //event handler for custom menu items
                }
            });
        }
    });

{% endhighlight %}

The screenshot of the **Custom Context Menu** items in **Gantt** control is as follows.

{% include image.html url="/js/Gantt/Context-Menu_images/Context-Menu_img2.png" Caption="Custom Context Menu"%}

