---
layout: post
title: Grouping-Bar with PivotGrid widget for Syncfusion Essential JS
description: This document illustrates that how to enable grouping bar feature and its functionalities in JavaScript PivotGrid control with relational mode
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Grouping Bar

## Initialization
Grouping bar allows you to dynamically alter the report by filter, sort, and remove operations in the PivotGrid control. Based on the relational datasource and report bound to the PivotGrid control, the grouping bar will be automatically populated. You can enable the grouping bar option in the PivotGrid by setting the [`enableGroupingBar`](/api/js/ejpivotgrid#members:enablegroupingbar) property to true.

### Client mode

{% highlight js %}

  <script type="text/javascript">

  // Datasource

    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            dataSource: {
                data: pivotData,
                rows: [{
                    fieldName: "Country",
                    fieldCaption: "Country",
                    sortOrder: ej.PivotAnalysis.SortOrder.Ascending
                }, {
                    fieldName: "State",
                    fieldCaption: "State",
                    sortOrder: ej.PivotAnalysis.SortOrder.Descending
                }],
                columns: [{
                    fieldName: "Product",
                    fieldCaption: "Product"
                }],
                values: [{
                    fieldName: "Amount",
                    fieldCaption: "Amount"
                }, {
                    fieldName: "Quantity",
                    fieldCaption: "Quantity"
                }],
                filters: [{
                    fieldName: "Date",
                    fieldCaption: "Date",
                    filterItems: {
                        filterType: ej.PivotAnalysis.FilterType.Exclude,
                        values: ["FY 2005"]
                    }
                }]
            },
            enableGroupingBar: true
        });
    });
</script>


{% endhighlight %}

![Grouping bar support in JavaScript pivot grid control with relational client mode](Grouping-Bar_images/ClientsideGr.png)


### Server mode

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
       url: "/RelationalService",
        enableGroupingBar: true
    });
});

{% endhighlight %}

![Grouping bar support in JavaScript pivot grid control with relational server mode](Grouping-Bar_images/groupingbar.png)

## Drag and drop

You can alter the report on fly through the drag-and-drop operation.

![Drag and drop in JavaScript pivot grid control](Grouping-Bar_images/GBar_Rel.png)

## Context menu

You can also alter the report by using the context menu.

![Context menu in JavaScript pivot grid control](Grouping-Bar_images/CMenu_Rel.png)

## Searching values
Search option in the grouping bar allows you to search a specific value that needs to be filtered from the list of values in the filter pop-up window.

![Member editor dialog in JavaScript pivot grid control](Grouping-Bar_images/groupingbar-filter.png)

![Searching in JavaScript pivot grid control](Grouping-Bar_images/groupingbar-search.png)

## Filtering values
Filtering option in the grouping bar allows you to select a specific set of values that needs to be displayed in the PivotGrid control. At least, one value should be present in the checked state while filtering. Otherwise, “Ok” will be disabled.

![Member editor in JavaScript pivot grid control](Grouping-Bar_images/groupingbar-filter.png)

![Filtering in JavaScript pivot grid control](Grouping-Bar_images/groupingbar-filter1.png)

## Sorting values
Sorting option in the grouping bar allows you to arrange headers in ascending or descending order. Sorting option is applicable for fields that are available only in the row and column region. By default, headers are sorted in the ascending order. Regarding the sorting indicator, an up arrow denotes the ascending order and a down arrow denotes the descending order.

![Sorting icon in JavaScript pivot grid control](Grouping-Bar_images/groupingbar-sort.png)

![Sorted results in JavaScript pivot grid control](Grouping-Bar_images/groupingbar-sort-grid.png)

## Removing field
Remove option in the grouping bar allows you to completely remove a specific field from the PivotGrid control. Remove operation can be achieved either by clicking the remove icon in each field or by dragging and dropping the field out of the grouping bar region.

![Remove icon in JavaScript pivot grid control](Grouping-Bar_images/groupingbar-remove.png)

![Removed items in JavaScript pivot grid control](Grouping-Bar_images/groupingbar-remove-grid.png)


