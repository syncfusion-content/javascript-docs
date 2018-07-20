---
layout: post
title: Sorting
description: sorting
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Sorting

The Gantt control for JavaScript has in-built support for sorting one or more columns.

## Sorting Columns

Gantt allows the tasks to be sorted in ascending or descending order based on the selected column by enabling the [`allowSorting`](/api/js/ejgantt#members:allowsorting) option in Gantt control. The following code example shows you how to enable sorting in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowSorting: true
    });

{% endhighlight %}

## Multicolumn sorting

Gantt allows you to sort multiple columns by clicking the desired column headers while holding the <kbd>CTRL</kbd> key and it can be enabled by using [`allowMultiSorting`](/api/js/ejgantt#members:allowmultisorting) property. The following code example shows you how to enable multicolumn sorting in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowSorting: true,
        allowMultiSorting: true
    });

{% endhighlight %}

The following screenshot shows the output of multicolumn sorting in Gantt control.

![](/js/Gantt/Sorting_images/Sorting_img1.png)

## Sorting column on Gantt initialization

Gantt control can be rendered with sorted columns initially, this can be achieved by using [`sortSettings`](/api/js/ejgantt#members:sortsettings) property. We can add columns which are sorted initially in [`sortedColumns`](/api/js/ejgantt#members:sortsettings-sortedcolumns "sortSettings.sortedColumns") collection. [`sortedColumns`](/api/js/ejgantt#members:sortsettings-sortedcolumns "sortSettings.sortedColumns") collection was defined with [`field`](/api/js/ejgantt#members:sortsettings-sortedcolumns-field "sortSettings.sortedColumns.field") and [`direction`](/api/js/ejgantt#members:sortsettings-sortedcolumns-direction "sortSettings.sortedColumns.direction") properties. The following code example shows how to add sorted column on Gantt initialization.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowSorting: true,
        sortSettings: {
            sortedColumns: [
                { field: "taskName", direction: ej.sortOrder.Descending }
            ]
        },
    });

{% endhighlight %}

The following screenshot shows the output of above code example.

![](/js/Gantt/Sorting_images/Sorting_img2.png)

## Sorting column dynamically

Columns in Gantt control can be sorted dynamically by using [`sortColumn`](/api/js/ejgantt#methods:sortcolumn "sortColumn(mappingName, columnSortDirection)") method. The following code example shows how to invoke the [`sortColumn`](/api/js/ejgantt#methods:sortcolumn "sortColumn(mappingName, columnSortDirection)") method on button click action.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowSorting: true,
    });

    $("#sort_column").click(function(){ 
        $("#GanttContainer").ejGantt("sortColumn", "taskID", ej.sortOrder.Descending);
    });

{% endhighlight %}

The following screenshot shows the output of above code example.

![](/js/Gantt/Sorting_images/Sorting_img3.png)
Before Sorting
{:.caption}

![](/js/Gantt/Sorting_images/Sorting_img4.png)
After Sorting
{:.caption}

N> when sorting a column using this method, previously sorted columns are cleared.

## Sorting multiple columns dynamically

Multiple columns in Gantt can be sorted dynamically by using `setModel` method with [`sortSetting`](/api/js/ejgantt#members:sortsettings) property. The following code example shows how to use this method.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowSorting: true,
        allowMultiSorting: true

    });

    $("#sort_column").click(function() {
        var sortedColumns = [
             { field: "taskID", direction: ej.sortOrder.Descending },
             { field: "taskName", direction: ej.sortOrder.Descending }
            ];
        var sortSettings = {
                sortedColumns: sortedColumns
            };
        var ganttObj = $("#GanttContainer").ejGantt("instance");
            ganttObj.setModel({ "sortSettings": sortSettings });
    });

{% endhighlight %}

The following screenshot shows the output of the above code example.

![](/js/Gantt/Sorting_images/Sorting_img3.png)
Before Sorting
{:.caption}

![](/js/Gantt/Sorting_images/Sorting_img5.png)
After Sorting
{:.caption}

## Clear all the sorting dynamically

In Gantt it is possible to clear all the sorted columns and return to previous position by using [`clearSorting`](/api/js/ejgantt#methods:clearsorting) public method.
The following code snippet show how to remove all the sorting in button click.

{% highlight javascript %}

<div id="gantt"></div> 
 
<script>
var ganttObject = $("#gantt").data("ejGantt");
ganttObject.clearSorting();
</script>

{% endhighlight %}