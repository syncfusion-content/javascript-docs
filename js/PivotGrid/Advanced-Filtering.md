---
layout: post
title: Advanced Filtering | Sorting | PivotGrid |Syncfusion | JS
description: This document describes how to define advance filtering and sorting with respective to the modes in JavaScript PivotGrid control
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Advanced filtering and sorting

It allows you to filter and sort field members in the pivot grid.

### Client mode

In client mode, you can enable the advanced filtering and sorting option in the pivot grid by setting the [`enableAdvancedFilter`](/api/js/ejpivotgrid#members:enableadvancedfilter) property to true.

{% highlight html %}

<div id="PivotGrid1"></div>
<script>
    $("#PivotGrid1").ejPivotGrid({
            //...
            enableAdvancedFilter: true
    });
</script>

{% endhighlight %}

### Server mode

In server mode, you can enable the advanced filtering and sorting option in the pivot grid by setting the [`enableAdvancedFilter`](/api/js/ejpivotgrid#members:enableadvancedfilter) property to true.

{% highlight html %}

<div id="PivotGrid1"></div>
<script>
    $("#PivotGrid1").ejPivotGrid({
        //...
        enableAdvancedFilter: true
    });
</script>

{% endhighlight %}

## Sorting

Sorting provides an option to sort the members of a field either in ascending or descending order.

![Sorting options in JavaScript pivot grid control](AdvanceFiltering_images/sorting.png)

## Label filtering

Label filtering provides an option to filter the members of a field purely based on their caption.

![Label filtering options in JavaScript pivot grid control](AdvanceFiltering_images/filtering.png)

![Label filter dialog in JavaScript pivot grid control](AdvanceFiltering_images/filtering_dialog.png)


## Value filtering

Value filtering provides an option to filter members based on total values of the appropriate measure between the members of the level.

![Value filtering options in JavaScript pivot grid control](AdvanceFiltering_images/valuefilter.png)

![Value filter dialog in JavaScript pivot grid control](AdvanceFiltering_images/valuefilter_dialog.png)
