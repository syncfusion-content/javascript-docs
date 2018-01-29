---
layout: post
title: Advanced Filtering and Sorting
description: advance filtering and sorting
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

![](AdvanceFiltering_images/sorting.png)

## Label filtering

Label filtering provides an option to filter the members of a field purely based on their caption. 

![](AdvanceFiltering_images/filtering.png)

![](AdvanceFiltering_images/filtering_dialog.png)


## Value filtering

Value filtering provides an option to filter members based on total values of the appropriate measure between the members of the level.

![](AdvanceFiltering_images/valuefilter.png)

![](AdvanceFiltering_images/valuefilter_dialog.png)
