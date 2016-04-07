---
layout: post
title: Number format
description: Number format
platform: js
control: PivotGrid
documentation: ug
---

# Number format 

I> This feature is applicable only for Relational datasource only at Client Mode.

The PivotGrid widget values could be formatted to number, decimal, currency, percentage, date and time etc… by setting the `format` option.

{% highlight js %}

<!--Create a tag which acts as a container for PivotGrid-->
 <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"></div>

$(function() {
    
    $("#PivotGrid1").ejPivotGrid({
        dataSource: {
            data: pivot_dataset,
            rows: [{
                fieldName: "Country",
                fieldCaption: "Country"
            }, {
                fieldName: "State",
                fieldCaption: "State"
            }],
            columns: [

                {
                    fieldName: "Product",
                    fieldCaption: "Product"
                }
            ],
            values: [{
                fieldName: "Amount",
                fieldCaption: "Amount",
                format: "currency"
            }, {
                fieldName: "Quantity",
                fieldCaption: "Quantity",
                format: "decimal"
            }]
        }
    });
});

{% endhighlight %}

![](Number-Format_images/Numberformat.png)


