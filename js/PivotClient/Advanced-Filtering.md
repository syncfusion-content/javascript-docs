---
layout: post
title: Advanced Filtering and Sorting
description: advanced filtering and sorting
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Advanced filtering and sorting

It allows you to filter and sort the field members in the pivot client.

### Client mode

In client mode, you can enable the advanced filtering and sorting option in the pivot client by setting the [`enableAdvancedFilter`](/api/js/ejpivotclient#members:datasource-enableadvancedfilter) property under the [`dataSource`] to true.

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

![](AdvanceFiltering_images/sorting.png)

## Label filtering

The label filtering provides an option to filter the members of the field purely based on their caption.

![](AdvanceFiltering_images/filtering.png)

![](AdvanceFiltering_images/filtering_dialog.png)


## Value filtering

The value filtering provides an option to filter the members based on total values of the appropriate measure between the members of the level. 

![](AdvanceFiltering_images/valuefilter.png)

![](AdvanceFiltering_images/valuefilter_dialog.png)
