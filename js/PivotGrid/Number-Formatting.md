---
layout: post
title: Number formatting with PivotGrid widget for Syncfusion Essential JS
description: Number format
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Number Format

I> This feature is applicable for all modes.

Allows you to specify the required number format that should be used in values of the PivotGrid by setting the `format`. Following are supported number formats:

* number
* decimal
* currency
* percentage
* date
* time
* scientific
* accounting
* fraction
* string

## Relational

### Client mode

{% highlight js %}

<script>
$(function() {
   $("#PivotGrid1").ejPivotGrid({
        dataSource: {
            //..
            values: [
                {
                    fieldName: "Amount",
                    fieldCaption: "Amount",
                    format: "currency" //Specify the format here
                },
                {
                    fieldName: "Quantity",
                    fieldCaption: "Quantity",
                    format: "decimal"
                }
            ]
        }
    });
 });
</script>

{% endhighlight %}

![Number formatting in JavaScript pivot grid relational client mode](Number-Format_images/RelationalClient.png)

### Server mode

You can set the number format through the `Format` property. You should specify the format to the property as per the MS standard notation.

{% highlight C# %}

private PivotReport BindDefaultData()
    {

        PivotReport pivotSetting = new PivotReport();
        pivotSetting.PivotRows.Add(new PivotItem { FieldMappingName = "Product", FieldHeader = "Product", TotalHeader = "Total" });
        pivotSetting.PivotColumns.Add(new PivotItem { FieldMappingName = "Country", FieldHeader = "Country", TotalHeader = "Total" });
        //specify the format here
        pivotSetting.PivotCalculations.Add(new PivotComputationInfo { CalculationName = "Amount", Description = "Amount", FieldHeader = "Amount", FieldName = "Amount", Format = "E", SummaryType = Syncfusion.PivotAnalysis.Base.SummaryType.DoubleTotalSum });
        return pivotSetting;
    }

{% endhighlight %}

![Number formatting in JavaScript pivot grid relational server mode](Number-Format_images/RelationalServer.png)

## OLAP

### Client mode

{% highlight html %}

<script>
$("#PivotGrid1").ejPivotGrid({
    dataSource: {
        //..
        values: [{
            measures: [{
                fieldName: "[Measures].[Internet Sales Amount]",
                format: "percent" //Specify the format here
            }],
            axis: "columns"
        }]
    }
});
</script>

{% endhighlight %}

![Number formatting in JavaScript pivot grid OLAP client mode](Number-Format_images/OlapClient.png)

### Server mode

 OLAP server mode supports the following number formats in addition to the above mentioned formats:

* General
* RoundTrip
* FixedPoint
* HexaDecimal

N> You can set the number format through the `Format` property.

{% highlight C# %}

private OlapReport CreateOlapReport()
{
     OlapReport olapReport = new OlapReport();
     olapReport.CurrentCubeName = "Adventure Works";

     MeasureElements measureElement = new MeasureElements();
     measureElement.Elements.Add(new MeasureElement { UniqueName = "[Measures].[Internet Sales Amount]", Format = NumberFormat.FixedPoint }); //Specify the format here

     DimensionElement dimensionElementRow = new DimensionElement();
     dimensionElementRow.Name = "Date";
     dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");

     DimensionElement dimensionElementColumn = new DimensionElement();
     dimensionElementColumn.Name = "Customer";
     dimensionElementColumn.AddLevel("Customer Geography", "Country");

     olapReport.SeriesElements.Add(dimensionElementRow);
     olapReport.CategoricalElements.Add(dimensionElementColumn);
     olapReport.CategoricalElements.Add(measureElement);

     return olapReport;
}
{% endhighlight %}

![Number formatting in JavaScript pivot grid OLAP server mode](Number-Format_images/OlapServer.png)