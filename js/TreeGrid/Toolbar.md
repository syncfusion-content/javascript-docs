---
layout: post
title: Toolbar
description: toolbar
platform: js
control: TreeGrid
documentation: ug
---

# Toolbar

TreeGrid control contains toolbar options for adding, deleting and editing the records. You can customize the TreeGrid toolbar by using [`toolbarSettings`](/js/api/ejtreegrid#toolbarsettingsspan-classtype-signature-type-objectobjectspan "toolbarSettings") property. 

In TreeGrid by using [`rowPosition`](/js/api/ejtreegrid#editsettingsrowpositionspan-classtype-signature-type-stringstringspan "editSettings.rowPosition") property, the index position for the newly added row can be provided. Default value of the `rowPosition` property is `top`. The enumeration values for `rowPosition` properties are,

* top
* bottom
* aboveSelectedRow
* belowSelectedRow

You can enable toolbar for TreeGrid, using the following code example.

{% highlight js %}

    $("#TreeGridcontainer").ejTreeGrid(

    //...
    editSettings: {
        //...
        rowPosition: "aboveSelectedRow"
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

The following screenshot displays the toolbar option in TreeGrid control.

![](/js/TreeGrid/Toolbar_images/Toolbar_img1.png)

