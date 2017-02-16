---
layout: post
title: Advanced Filtering and Sorting
description: advanced filtering and sorting
platform: js
control: PivotClient
documentation: ug
---

# Advanced Filtering & Sorting

I> These features are not applicable for Relational datasource bound from server-side. 

It allows to filter and sort the field members in PivotClient.

### Client Mode

In client mode, you can enable Advanced Filtering and Sorting option in PivotClient by setting the [`enableAdvancedFilter`](/api/js/ejpivotclient#members:enableAdvancedFilter) property under [`dataSource`] to true.

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

### Server Mode

In server mode, you can enable the Advanced Filtering and Sorting option in PivotClient by setting the [`enableAdvancedFilter`](/api/js/ejpivotclient#members:enableAdvancedFilter) property to true.

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

Sorting provides an option to sort the members of a field either in ascending or descending order. 

I> This option isn't applicable for OLAP datasource bound from server-side. 

![](AdvanceFiltering_images/sorting.png)

## Label Filtering

Label filtering provides an option to filter the members of a field purely based on their caption. 

![](AdvanceFiltering_images/filtering.png)

![](AdvanceFiltering_images/filtering_dialog.png)


## Value Filtering

Value filtering provides an option to filter members based on the total values of the appropriate measure between the members of the level. 

![](AdvanceFiltering_images/valuefilter.png)

![](AdvanceFiltering_images/valuefilter_dialog.png)
