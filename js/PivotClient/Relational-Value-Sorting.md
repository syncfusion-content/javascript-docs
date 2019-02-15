---
layout: post
title: Value-Sorting with PivotClient widget for Syncfusion Essential JS
description: value Sorting
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Value sorting

I> This feature is applicable only for the relational data source.

PivotClient provides support for value sorting that allows you to sort columns and rows based on value fields.

The headers of the column to be sorted are given in the [`headerText`](/api/js/ejpivotclient#members:valueSortSettings-headerText) property under [`valueSortSettings`](/api/js/ejpivotclient#members:valueSortSettings) in field wise order, separated by a string.  The string which is used to separate the headers is given in the [`headerDelimiters`](/api/js/ejpivotclient#members:valueSortSettings-headerDelimiters) property.

Also, you can sort the column by clicking the column header. By clicking the same header once again, the sorting direction will be reversed. The sorting operation is performed by the [`sortOrder`](/api/js/ejpivotclient#members:valueSortSettings-sortOrder) property.

The following code snippet shows how to sort values in descending order.

{% highlight js %}

    <script type="text/javascript">

    // Datasource

    $(function() {
        $("#PivotClient1").ejPivotClient({
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

The below screenshot shows PivotClient before applying value sorting.
![JavaScript pivot client control](Value-Sorting_images/Before.png)

The below screenshot shows PivotClient after applying value sorting.
![JavaScript pivot client control with value sorting](Value-Sorting_images/After.png)