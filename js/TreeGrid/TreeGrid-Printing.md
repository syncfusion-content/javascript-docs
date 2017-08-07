---
layout: post
title: TreeGrid-Printing
description: treegrid printing
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---
# TreeGrid Printing


TreeGrid provides support to print the contents. To print the TreeGrid the print toolbar item must be added to [toolbarSettings.toolbarItems](/api/js/ejgantt#members:toolbarsettings-toolbaritems) property. The below code example shows how to enable print in TreeGrid.

{% highlight js %}
 
<div id="TreeGridContainer"></div>
<script type="text/javascript">
    $("#TreeGridContainer").ejTreeGrid({
        toolbarSettings: {
            showToolbar: true,
            toolbarItems: [
                ej.TreeGrid.ToolbarItems.Print
            ]
        },
    })


{% endhighlight %}

The print preview window will be opened by clicking on this toolbar icon. 

## Print Mode

It is possible to set the printMode in [pageSettings](/api/js/ejgantt#members:pagesettings) property, to give printing preference, as to print current page alone or all the pages in case of paging enabled in TreeGrid. The following code example explains this.


{% highlight js %}
 
<div id="TreeGridContainer"></div>
<script type="text/javascript">
    $("#TreeGridContainer").ejTreeGrid({
        toolbarSettings: {
            showToolbar: true,
            toolbarItems: [
                ej.TreeGrid.ToolbarItems.Print
            ]
        },
        allowPaging: true,
        pageSettings: {
            printMode: ej.TreeGrid.PrintMode.CurrentPage
        },
    })

{% endhighlight %}

In this case only the visible records in the current page will be send to printing.

## beforePrint Event 

beforePrint event will be triggered once after printing initiated in TreeGrid. This event contains the treegrid element which is going to be printing. The following code explains this.

{% highlight js %}
 
<div id="TreeGridContainer"></div>
<script type="text/javascript">
    $("#TreeGridContainer").ejTreeGrid({
        toolbarSettings: {
            showToolbar: true,
            toolbarItems: [
                ej.TreeGrid.ToolbarItems.Print
            ]
        },
        beforePrint: function(args) {
            // will be triggered before printing the TreeGrid
        },
    })

{% endhighlight %}
