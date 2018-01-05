---
layout: post
title: Context-Menu
description: context menu
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---
# Context Menu

## Default Menu Items

Context menu in Gantt has the following default menu items.

* Task Details
* Add New Task
* Indent
* Outdent
* Delete

Context menu in Gantt can be enabled by using [`enableContextMenu`](/api/js/ejgantt#members:enablecontextmenu) property.
The following code example explains how to enable the context menu in Gantt control.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
    enableContextMenu: true
});

{% endhighlight %}

The following screenshot shows the default context menu in Gantt control.

![](/js/Gantt/Context-Menu_images/Context-Menu_img1.png)

## Custom Menu Item

It is possible to add a custom context menu item in Gantt control by using [`contextMenuOpen`](/api/js/ejgantt#events:contextmenuopen) event. The following code example explains on how to add the custom context menu item.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    contextMenuOpen: function(args) {

        args.contextMenuItems.push({

            headerText: "Expand/Collapse",

            menuId: "expand",

            iconPath: "url(Expand-02-WF.png)",

            eventHandler: function() {

                //event handler for custom menu items

            }

        });

    }

});

{% endhighlight %}

The screenshot of the custom context menu items in Gantt control is as follows.

![](/js/Gantt/Context-Menu_images/Context-Menu_img2.png)

### Custom menu item with sub menu item

It is possible to create a custom menu item with a sub menu, by mapping the parentMenuId property from the contextMenuItems argument in the [`contextMenuOpen`](/api/js/ejgantt#events:contextmenuopen) event.

The following code example explains on how to add sub context menu for custom menu items.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    contextMenuOpen: function(args) {

        args.contextMenuItems.push({

            headerText: "Expand/Collapse",

            menuId: "expand",

            iconPath: "url(Navigation-Up-02-WF.png)",

            eventHandler: function() {

                //event handler for custom menu items

            }

        });

        args.contextMenuItems.push({

            headerText: "ExpandAll",

            menuId: "expandAll",

            parentMenuId: "expand",

            iconPath: "url(Expand-02-WF.png)",

            eventHandler: function() {

                //event handler for custom menu items

            }

        });

        args.contextMenuItems.push({

            headerText: "CollapseAll",

            menuId: "collapseAll",

            parentMenuId: "expand",

            iconPath: "url(shrink2.png)",

            eventHandler: function() {

                //event handler for custom menu items

            }

        });

    },
    
});
{% endhighlight %}

The screenshot of the custom context menu items in Gantt control is as follows.

![](/js/Gantt/Context-Menu_images/Context-Menu_img3.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/contextmenu/customcontextmenu) here to view the online demo sample for custom context menu in Gantt.
