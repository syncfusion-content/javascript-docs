---
layout: post
title: Context-Menu
description: context menu
platform: js
control: Gantt
documentation: ug
---

# Context Menu

## Default Context Menu

The default context menu contains the following options.

* Task Details
* Add New Task
* Indent
* Outdent
* Delete

The following code example shows you how to enable the default context menu in Gantt control.

{% highlight js %}

    $("#GanttContainer").ejGantt({
        //...
        enableContextMenu:true
    });

{% endhighlight %}

The following screenshot shows the default Context menu in Gantt control.

![](/js/Gantt/Context-Menu_images/Context-Menu_img1.png)

## Custom Context Menu

You can add custom context menu option in Gantt control. The following code example shows you how to add the custom context menu option in Gantt control.

{% highlight js %}

    $("#GanttContainer").ejGantt({
        //...
        contextMenuOpen: function(args) {
            args.contextMenuItems.push({
                headerText: "ExpandAll",
                iconPath: "url(../images/Expand All.png)",
                evenHandler: function() {
                    //event handler for custom menu items
                }
            });
        }
    });

{% endhighlight %}

The screenshot of the custom context menu items in Gantt control is as follows.

![](/js/Gantt/Context-Menu_images/Context-Menu_img2.png)

