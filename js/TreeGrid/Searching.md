---
layout: post
title: Searching
description: TreeGrid Searching
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

## Searching

The TreeGrid control has an option to search its content using toolbar search box. The toolbar search box can be enabled by using the [`toolbarSettings.toolbarItems`](/api/js/ejtreegrid#members:toolbarsettings-toolbaritems) property. The following code example explains how to integrate search textbox in toolbar.

{% highlight js %}

$("#TreegridContainer").ejTreeGrid ({
    //...
    toolbarSettings:{
        showToolbar: true,
        toolbarItems:  [ ej.TreeGrid.ToolbarItems.Search ],
    }
    //...
});

{% endhighlight %}

The below screenshot shows TreeGrid search with `plan` key word.
![](/js/TreeGrid/Searching_images/Searching_img1.png)
