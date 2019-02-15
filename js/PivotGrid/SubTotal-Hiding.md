---
layout: post
title:  SubTotal Hiding with PivotGrid widget for Syncfusion Essential JS
description: SubTotal Hiding
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Sub Total Hiding

N> This feature is applicable only for the relational data source.

You can hide the **Sub Total** for respective fields in rows and columns by setting the [`showSubTotal`](/api/js/ejpivotgrid#members:datasource-columns-showsubtotal) property to `false`.

## Client mode

{% highlight html %}

<div id="PivotGrid1"></div>
<script>
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            dataSource: {
                //...
                columns: [{
                    fieldName: "Country",
                    fieldCaption: "Country",
                    showSubTotal: false,
                }]
            }
        });
    });
</script>

{% endhighlight %}


## Server mode


{% highlight c# %}

private PivotReport BindDefaultData()
{
    PivotReport pivotSetting = new PivotReport();
    pivotSetting.PivotRows.Add(new PivotItem { FieldMappingName = "Date", FieldHeader = "Date", TotalHeader = "Total", ShowSubTotal = false });
    pivotSetting.PivotRows.Add(new PivotItem { FieldMappingName = "Product", FieldHeader = "Product", TotalHeader = "Total", ShowSubTotal = true });
    pivotSetting.PivotColumns.Add(new PivotItem { FieldMappingName = "Country", FieldHeader = "Country", TotalHeader = "Total", ShowSubTotal = false });
    pivotSetting.PivotCalculations.Add(new PivotComputationInfo { CalculationName = "Amount", Description = "Amount", FieldHeader = "Amount", FieldName = "Amount", Format = "C", SummaryType = Syncfusion.PivotAnalysis.Base.SummaryType.DoubleTotalSum });
    return pivotSetting;
}

{% endhighlight %}

![SubTotal hiding support in JavaScript pivot grid control](SubTotal-Hiding_images/SubTotal.png)
