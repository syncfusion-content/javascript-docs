---
layout: post
title: Grouping-Bar
description: grouping bar
platform: js
control: PivotGrid
documentation: ug
---

# Grouping Bar

I> This feature is applicable only for relational datasource.

## Initialization 
Grouping Bar allows user to dynamically alter the report by filter, sort and remove operations in the PivotGrid control. Based on the datasource and report bound to the PivotGrid control, Grouping Bar will be automatically populated. You can enable Grouping Bar option in PivotGrid by setting the `enableGroupingBar` property to true.

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
        url: "../wcf/RelationalService.svc",
        enableGroupingBar: true
    });
});

{% endhighlight %}

![](Grouping-Bar_images/groupingbar.png)

## Filtering Values
Filtering option available in Grouping Bar allows you to select a specific set of values that needs to be displayed in the PivotGrid control. Atleast one value needed to be in checked state while filtering otherwise “Ok” button will be disabled.

![](Grouping-Bar_images/groupingbar-filter.png)

![](Grouping-Bar_images/groupingbar-filter1.png)

## Sorting Values
Sorting option available in Grouping Bar allows you to arrange headers either in ascending or descending order. Sorting option is applicable for fields available only in Row and Column region. By default, headers are sorted in ascending order. Regarding sorting indicator, up arrow denotes ascending order and down arrow denotes descending order.

![](Grouping-Bar_images/groupingbar-sort.png)

![](Grouping-Bar_images/groupingbar-sort-grid.png)

## Removing Field
Remove option available in the Grouping Bar allows you to completely remove a specific field from the PivotGrid control. Remove operation can be either achieved by clicking remove icon available inside each field or by dragging and dropping field out of Grouping Bar region.

![](Grouping-Bar_images/groupingbar-remove.png)

![](Grouping-Bar_images/groupingbar-remove-grid.png)
