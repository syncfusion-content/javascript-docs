---
layout: post
title: Context-Menu
description: context menu
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Context Menu

The **Context menu** in TreeGrid control is used to manipulate (add, edit and delete) the tree grid rows. In TreeGrid, context menu can be enabled with the [`contextMenuSettings`](/api/js/ejtreegrid#members:contextmenusettings) property. The [`contextMenuSettings`](/api/js/ejtreegrid#members:contextmenusettings) property contains two inner properties [`showContextMenu`](/api/js/ejtreegrid#members:contextmenusettings-showcontextmenu "contextMenuSettings.showContextMenu") and [`contextMenuItems`](/api/js/ejtreegrid#members:contextmenusettings-contextmenuitems "contextMenuSettings.contextMenuItems").

The [`showContextMenu`](/api/js/ejtreegrid#members:contextmenusettings-showcontextmenu "contextMenuSettings.showContextMenu") property is used to **enable or disable** the context menu, default value for this property is `false`.

The [`contextMenuItems`](/api/js/ejtreegrid#members:contextmenusettings-contextmenuitems "contextMenuSettings.contextMenuItems") property is used to add the menu items to context menu, this property renders `Add` and `Delete` options by default when the menu items are not provided.

{% highlight js %}

        $("#treegrid1").ejTreeGrid(
        {   
           // ...     
            editSettings:{allowEditing: true , editMode:"rowEditing"},
            contextMenuSettings:{showContextMenu: true 
                                contextMenuItems:[ "add","edit","delete"]},
            // ...             
        });

{% endhighlight %}

The following screenshot displays the Context menu in TreeGrid control.

![](/js/TreeGrid/Context-Menu_images/Context-Menu_img1.png)

# Header Context Menu
Header context menu can be enabled by setting [`showContextMenu`](/api/js/ejtreegrid#members:contextmenusettings-showcontextmenu "contextMenuSettings.showContextMenu") as `true`. The default value of the [`showContextMenu`](/api/js/ejtreegrid#members:contextmenusettings-showcontextmenu "contextMenuSettings.showContextMenu") property is false.

Following options are shown in header context menu. 

* **Column Chooser** - Display all the column names; you can enable or disable a column by select or deselect the respective column name in the column chooser menu. This option is default option of header context menu.
* **Sort Ascending & Sort Descending** - Used to sort the items in the column. These menu options will be displayed only when you enable the [`allowSorting`](/api/js/ejtreegrid#members:allowsorting) property. To perform multilevel sorting, the [`allowMultiSorting`](/api/js/ejtreegrid#members:allowmultisorting) property should be enabled.
* **Freeze, Unfreeze & Freeze Preceding Columns** - Used to freeze or unfreeze the columns. These set of menu options will be displayed in all the columns when [`isFrozen`](/api/js/ejtreegrid#members:columns-isfrozen "columns.isFrozen") property is enabled in any of the columns. However you can control the visibility of these menu options in a particular column by enabling/disabling the [`allowFreezing`](/api/js/ejtreegrid#members:columns-allowfreezing "columns.allowFreezing") property of that specific column.

The below code snippet explains how to enable header context menu in TreeGrid

{% highlight js %}
    $("#treegrid1").ejTreeGrid(
    {   
        // ...     
        contextMenuSettings:{showContextMenu: true },
        // ...             
    });

{% endhighlight %}


The following screenshot displays the Header context menu in TreeGrid control.

![](/js/TreeGrid/Context-Menu_images/Context-Menu_img2.png)

### ContextMenu Customization

Context menu can be customized by adding a new custom menu item to it. In TreeGrid, context menu can be customized using the [`contextMenuOpen`](https://help.syncfusion.com/api/js/ejtreegrid#events:contextmenuopen "contextMenuOpen") client-side event. This event is triggered when the context menu is rendered with mouse right click action. The following properties are available in the event.

* headerText: Display text for menu item.
* menuId: provides ID field for the created DOM element for custom menu item.
* iconPath: Image location for menu item.
* eventHandler: Client-side event for menu item click.

{% highlight js %}

        $("#treegrid1").ejTreeGrid({
            // ...     
            contextMenuSettings: {
                showContextMenu: true
            },
            contextMenuOpen: customMenu,
            // ...             
        });

        function customMenu(args) {
            args.contextMenuItems.push({
                headerText: "Custom Menu",
                menuId: "customMenu",
                iconPath: "url(.../images/customMenu.png)",
                eventHandler: customMenuClick,
            });
            if(args.headerContextMenuItems){
                args.headerContextMenuItems.push.apply({
                    headerText: "Delete Column",
                    menuId: "Delete",
                    iconPath: "url(.../images/customMenu.png)",
                    eventHandler: customHeaderMenuClick,
                });
            }
        }

        function customMenuClick(args) {
            // ...
        }

        function customHeaderMenuClick(args) {
            // ...
        }

{% endhighlight %}

The following screenshot displays the customization of Context menu in TreeGrid control.

![](/js/TreeGrid/Context-Menu_images/Context-Menu_img2.jpg)

