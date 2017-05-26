---
layout: post
title: Value-Sorting
description: value Sorting
platform: js
control: PivotGrid
documentation: ug
---

# Value Sorting

I> This feature is applicable for Relational datasource.

Value Sorting allows to sort columns and rows based on value fields.

The headers of the column to be sorted is given in the 'headerText' property under 'valueSortSettings' in field wise order separated by a string.  The string which is used to separate the headers is given in the property 'headerDelimiters'.
Also you can sort column by clicking the column header. On clicking the same header once again will reverse the sorting direction.

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

![](Value-Sorting_images/Before.png) 

![](Value-Sorting_images/After.png) 



