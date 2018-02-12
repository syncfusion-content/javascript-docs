---
layout: post
title: Sorting
description: sorting
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Sorting

The TreeGrid control for JavaScript has in-built support for Sorting one or more columns.

### Sorting Columns

TreeGrid allows the items to be sorted in ascending or descending order based on the selected column by enabling the [`allowSorting`](/api/js/ejtreegrid#members:allowsorting) property in TreeGrid control. The following code example shows you how to enable Sorting in TreeGrid control.

{% highlight js %}

         $("#TreeGridContainer").ejTreeGrid({
             //...
             allowSorting: true,
         });

{% endhighlight %}

The TreeGrid columns can also be sorted with custom actions by using the [`sortColumn`](https://help.syncfusion.com/api/js/ejtreegrid#methods:sortcolumn "sortColumn") method, where the column field name and the sort order should be passed as the method parameters. And the sorting can be cleared using the method [`clearSorting`](https://help.syncfusion.com/api/js/ejtreegrid#methods:clearsorting "clearSorting"), calling this method will clear sorting for all the columns in TreeGrid.

### Multicolumn sorting

TreeGrid allows you to sort multiple columns by clicking the desired column headers while holding the `Ctrl` key. The following code example shows you how to enable **Multicolumn sorting** in the TreeGrid control.

{% highlight js %}

         $("#TreeGridContainer").ejTreeGrid({
                //...
                allowSorting: true,
                allowMultiSorting: true,
         });


{% endhighlight %}

The following screenshot shows the output of multicolumn sorting in TreeGrid control.

![](/js/TreeGrid/Sorting_images/Sorting_img1.png)

### Disable sorting for specific column

It is possible to disable sorting for a specific column by setting [`allowSorting`](/api/js/ejtreegrid#members:columns-allowsorting "columns.allowSorting") as `false` in the column definition.

The below code snippet demonstrates this.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "taskID", headerText: "Task Id"},
                { field: "taskName", headerText: "Task Name",allowSorting: false },
                { field: "startDate", headerText: "Start Date"},
                { field: "endDate", headerText: "End Date" }
            ]
        })
    });

{% endhighlight %}


### Sort column at initial load

In TreeGrid, It is possible to render the control with sorted columns, this can be achieve by using [`sortSettings`](/api/js/ejtreegrid#members:sortsettings) property. We can add columns which are sorted initially in [`sortedColumns`](/api/js/ejtreegrid#members:sortsettings-sortedcolumns "sortSettings.sortedColumns") collection. [`sortedColumns`](/api/js/ejtreegrid#members:sortsettings-sortedcolumns "sortSettings.sortedColumns") collection was defined with [`field`](/api/js/ejtreegrid#members:sortsettings-sortedcolumns-field "sortSettings.sortedColumns.field") and [`direction`](/api/js/ejtreegrid#members:sortsettings-sortedcolumns-direction "sortSettings.sortedColumns.direction") properties.

The following code shows how to add sorted column in TreeGrid.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            allowSorting: true,
            sortSettings: {
                sortedColumns: [
                    { field: "taskName", direction: ej.sortOrder.Descending }
                ]
            },
            //...
        })
    });

{% endhighlight %}

![](/js/TreeGrid/Sorting_images/Sorting_img2.png)

The above screenshot shows TreeGrid rendered with descending order of `Task Name` column.
{:.caption}