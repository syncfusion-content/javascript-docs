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

It is possible to disable sorting for a specific column by setting [`allowSorting`](/api/js/ejtreegrid#members:columns-allowsorting "columns.allowSorting") as false in the column definition.

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

