---
layout: post
title: Summary-Type
description: summary type
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Summary Type

I> This feature is applicable only for Relational datasource only at Client Mode.

Allow us to specify the required [`layout`](/api/js/ejpivotgrid#members:layout) that PivotGrid should use in its summary cells. “Sum” is the default summary type. Following summary types that are supported:

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


