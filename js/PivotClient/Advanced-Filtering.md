---
layout: post
title: Advanced Filtering | Sorting | PivotClient | Syncfusion JS
description: This document illustrates that how to define advance filtering and sorting with respective to the modes in JavaScript PivotClient control
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Advanced filtering and sorting

It allows you to filter and sort the field members in the pivot client.

### Client mode

In client mode, you can enable the advanced filtering and sorting option in the pivot client by setting the [`enableAdvancedFilter`](/api/js/ejpivotclient#members:datasource-enableadvancedfilter) property under the [`dataSource`](/api/js/ejpivotclient#members:datasource) to true.

{% highlight html %}

<div id="PivotClient1"></div>
<script>
    $("#PivotClient1").ejPivotClient({
        dataSource: {
            //...
            enableAdvancedFilter: true
        }
    });
</script>

{% endhighlight %}

### Server mode

In server mode, you can enable the advanced filtering and sorting option in the pivot client by setting the [`enableAdvancedFilter`](/api/js/ejpivotclient#members:enableadvancedfilter) property to true.

{% highlight html %}

<div id="PivotClient1"></div>
<script>
    $("#PivotClient1").ejPivotClient({
        //...
        enableAdvancedFilter: true
    });
</script>

{% endhighlight %}

## Sorting

Sorting provides an option to sort the members of the field either in the ascending or descending order.

![Sorting options in JavaScript pivot client control](AdvanceFiltering_images/sorting.png)

## Label filtering

The label filtering provides an option to filter the members of the field purely based on their caption.

![Label filtering options in JavaScript pivot client control](AdvanceFiltering_images/filtering.png)

![Label filter dialog in JavaScript pivot client control](AdvanceFiltering_images/filtering_dialog.png)


## Value filtering

The value filtering provides an option to filter the members based on total values of the appropriate measure between the members of the level.

![Value filtering options in JavaScript pivot client control](AdvanceFiltering_images/valuefilter.png)

![Value filter dialog in JavaScript pivot client control](AdvanceFiltering_images/valuefilter_dialog.png)
