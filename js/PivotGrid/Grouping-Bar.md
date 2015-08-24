---
layout: post
title: Grouping-Bar
description: grouping bar
platform: js
control: PivotGrid
documentation: ug
---

#Grouping Bar

N> This feature is applicable only for Relational datasource.

Grouping bar support in the PivotGrid control allows you to filter, sort, and remove members of relational data loaded in the PivotGrid control. The grouped report can also be changed dynamically using drag and drop operations.

The following code example illustrates on enabling Grouping bar within the PivotGrid control.

{% highlight js %}

$(function () {
    $("#PivotGrid").ejPivotGrid({
        url: "../wcf/RelationalService.svc",
        enableGroupingBar: true,
        afterServiceInvoke: "onServiceInvokes"
     });
});

function onServiceInvokes(args) {
    if (args.action == "initialize")
        $("#PivotSchemaDesigner").ejPivotSchemaDesigner({
            pivotControl: this,
            layout: ej.PivotSchemaDesigner.Layouts.Excel
        });
}

{% endhighlight %}

{% include image.html url="/js/PivotGrid/Grouping-Bar_images/Grouping-Bar_img1.png" %}

The following operations can be done using Grouping bar:

##Filtering

Filtering option available in Grouping bar allows you to select a specific set of values that needs to be displayed in the PivotGrid control and hides the rest. By default, filtering option is applicable only for Row, Column and Filter areas.

##Sorting

Sorting option available in Grouping bar allows you to sort values besides the respective PivotItem in the PivotGrid control. This option is applicable for PivotItems available only in Row and Column areas. The sort indicator present inside the button indicates whether the values are in ascending or descending order. Naturally, the up arrow indicates ascending order and the down arrow indicates descending order. By default, values are sorted in ascending order.

##Remove

Remove option available in the Grouping bar allows you to remove a specific PivotItem from the PivotGrid control.


