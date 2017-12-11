---
layout: post
title: Filtering
description: filtering
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Filtering

Filtering helps to view specific or related records from data source which meets a given filtering criteria. The `filterSettings` property in Gantt is used to set the filtering criteria at load time.

## Filter columns at initial load
It is possible to filter one or more columns at initial load by providing the field and filter query to the `filterSettings.filteredColumns` property. The following code example explains how to filter a column on initial load.

{% highlight js %}

$("#GanttContainer").ejGantt({
    //...
    filterSettings: {
        filteredColumns: [{
            value: "plan",
            field: "taskName",
            predicate: "and",
            operator: "startswith"
        }]
    },
});

{% endhighlight %}

The output of the filtering applied for a column is as follows.

![](Filtering_images/Filtering_img1.png)

## Filtering a specific column by public method

It is possible to filter columns dynamically by using the `filterColumn` public method. 
The below code snippet explains the above behavior.

{% highlight js %}

<button id="filterColumn">Filter Column</button>

<script type="text/javascript">
$("#GanttContainer").ejGantt({
    //...    
})

$("#filterColumn").click(function (args) {
       var obj = $("#GanttContainer").ejGantt("instance");
       obj.filterColumn("taskName", "startswith", "plan");
})
</script>

{% endhighlight %}


## Clearing the filter applied to Gantt

You can clear all the filtering condition done in the Gantt by using the `clearFiltering` public method. 
The below code snippet explains the above behavior.

{% highlight js %}

<button id="clearFilter">Clear Filter</button>

<script type="text/javascript">
$("#GanttContainer").ejGantt({
    //...    
})

$("#clearFilter").click(function (args) {
       var obj = $("#GanttContainer").ejGantt("instance");
       obj.clearFilter();
})
</script>

{% endhighlight %}





