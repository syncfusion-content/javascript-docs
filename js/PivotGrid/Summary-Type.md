---
layout: post
title: Summary-Type with PivotGrid widget for Syncfusion Essential JS
description: summary type
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Summary Type

I> This feature is applicable only for the relational datasource at client mode.

Allow you to specify the required [`layout`](/api/js/ejpivotgrid#members:layout) that should be used in summary cells of the PivotGrid. “Sum” is the default summary type. Following are the supported summary types:

* Sum
* Average
* Count
* Min
* Max

{% highlight js %}

$(function () {
    $("#PivotGrid1").ejPivotGrid({
        dataSource: {
            data: pivotData,
            //……
            values: [{
                fieldName: "Amount",
                fieldCaption: "Amount",
                summaryType: ej.PivotAnalysis.SummaryType.Average
            },
            {
                fieldName: "Quantity",
                fieldCaption: "Quantity",
                summaryType: ej.PivotAnalysis.SummaryType.Sum
            }
            ],
            //……
        },
    });
});
{% endhighlight %}

{% include image.html url="/js/PivotGrid/Getting-Started_images/purejssummarytype.png" %}


