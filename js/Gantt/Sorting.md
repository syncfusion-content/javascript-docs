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

The Gantt control for JavaScript has built-in support for sorting one or more columns.

### Sorting Columns

Gantt allows the tasks to be sorted in ascending or descending order based on the selected column by enabling the `allowSorting` option in Gantt control. The following code example shows you how to enable sorting in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowSorting: true
    });

{% endhighlight %}

### Multicolumn sorting

Gantt allows you to sort multiple columns by clicking the desired column headers while holding the `CTRL` key. The following code example shows you how to enable multicolumn sorting in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowSorting: true
        allowMultiSorting: true
    });

{% endhighlight %}

The following screenshot shows the output of multicolumn sorting in Gantt control.

![](/js/Gantt/Sorting_images/Sorting_img1.png)

