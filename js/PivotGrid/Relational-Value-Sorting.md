---
layout: post
title: Value-Sorting with PivotGrid widget for Syncfusion Essential JS
description: This document illustrates that how to define value sorting and its functionalities in JavaScript Pivotgrid control
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Value sorting

I> This feature is applicable for the relational data source.

The value sorting allows you to sort columns and rows based on value fields.

The headers of the column to be sorted are given in the [`headerText`](/api/js/ejpivotgrid#members:valueSortSettings-headerText) property under [`valueSortSettings`](/api/js/ejpivotgrid#members:valueSortSettings) in field wise order, separated by a string.  The string which is used to separate the headers is given in the [`headerDelimiters`](/api/js/ejpivotgrid#members:valueSortSettings-headerDelimiters) property.
Also, you can sort the column by clicking the column header. By clicking the same header once again, will reverse the sorting direction. The sorting operation is performed by this property [`sortOrder`](/api/js/ejpivotgrid#members:valueSortSettings-sortOrder)

{% highlight js %}

  <script type="text/javascript">

  // Datasource

    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            dataSource: {
                data: pivotData,
                rows: [{
                    fieldName: "Country",
                    fieldCaption: "Country"
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
            },
            valueSortSettings: {
                headerText: "Bike##Quantity",
                headerDelimiters: "##",
                sortOrder: ej.PivotAnalysis.SortOrder.Descending
               }
        });
    });
</script>


{% endhighlight %}

The below screenshot shows pivot grid before applying value sorting.

![JavaScript pivot grid control before applying value sorting](Value-Sorting_images/Before.png)

The below screenshot shows pivot grid after applying value sorting.

![JavaScript pivot grid control after applying value sorting](Value-Sorting_images/After.png)

