---
layout: post
title:  Summary Customization
description: Summary Customization
platform: js
control: PivotGrid
documentation: ug
---

# Summary Customization

Allows you to show or hide the PivotGrid totals in column and row sections. Summary customization can been classified into two different categories.

* Sub Total Customization
* Grand Total Customization


## Sub Total Customization

You can hide the **Sub Total** for respective fields in rows and columns by setting the property [`showSubTotal`](/js/api/ejpivotgrid#members:showSubTotal) to `false`

## Client Mode

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


## Server Mode


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

![](Summary-Customization_images/SubTotal.png)


## Grand Total Customization

Grand Total Customization can be classified into three categories.

* Row Grand Total Customization
* Column Grand Total Customization
* Both

## Row Grand Total Customization

You can hide the **Grand Total** in row alone by setting the property [`enableRowGrandTotal`](/js/api/ejpivotgrid#members:enablerowgrandtotal) to `false`

{% highlight html %}

<script>
    $(function() {    
        $("#PivotGrid1").ejPivotGrid({
        //...
        enableRowGrandTotal: false
        });
    });
</script>
{% endhighlight %}

![](Summary-Customization_images/enableRowGrandTotal.png)

## Column Grand Total Customization

You can hide the **Grand Total** in column alone by setting the property [`enableColumnGrandTotal`](/js/api/ejpivotgrid#members:enablecolumngrandtotal) to `false`


{% highlight html %}

<div id="PivotGrid1"></div>
<script>
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableColumnGrandTotal: false
        });
    });
</script>

{% endhighlight %}

![](Summary-Customization_images/enableColumnGrandTotal.png)

## Both

You can hide the **Grand Total** in both row and column by setting the property [`enableGrandTotal`](/js/api/ejpivotgrid#members:enablegrandtotal) to `false`

{% highlight html %}

<div id="PivotGrid1"></div>

<script>
    $(function() {            
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableGrandTotal: false
        });
    });
</script>

{% endhighlight %}

![](Summary-Customization_images/enableGrandTotal.png)