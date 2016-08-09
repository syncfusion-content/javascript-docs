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

Allow us to specify the required number format that PivotGrid should use in its values by setting the `format` option. Following number formats that are supported:

* number
* decimal
* currency
* percentage
* date
* time
* scientific
* accounting
* fraction


{% highlight js %}

<!--Create a tag which acts as a container for PivotGrid-->
 <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"></div>

$(function() {
    
    $("#PivotGrid1").ejPivotGrid({
        dataSource: {
            data: pivotData,
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


