---
layout: post
title: Calculated Field | Essential JS PivotGrid widget | Syncfusion
description: This document illustrates that how to define calculated field through code-behind/UI in JavaScript PivotGrid control 
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Calculated Field in PivotGrid

N> This feature is applicable only for the relational data source.

The pivot grid provides support to insert a new calculated field based on the existing pivot fields through the calculated field dialog or code behind.

### Through UI
To insert a new calculated field, open the calculated field dialog by using the grouping bar context menu. You can define "Name" for the new calculated field, and "Formula" can be entered by inserting required fields through the fields section. For inserting numbers and operators, you can use the formula pop-up as shown in the below screen-shot:

![Calculated field dialog in JavaScript pivot grid control](Calculated-Field_images/Calculated-Field-Popup.png)

Click **Add** to add the respective calculated field, and then click **OK** to populate the pivot grid control.

### Through code-behind

For client mode, the calculated field can be created at code-behind by defining formula based on the existing pivot fields in the pivot grid. To indicate a field as a calculated field, you should set the [`isCalculatedField`](/api/js/ejpivotgrid#members:datasource-values-iscalculatedfield) property to true and [`formula`](/api/js/ejpivotgrid#members:datasource-values-formula) property to set the expression.

{% highlight html %}

    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            dataSource: {
                //...
                values: [
                    {
                        fieldName: "Amount",
                        fieldCaption: "Amount"
                    },
                    {
                        fieldName: "Price",
                        fieldCaption: "Price",
                        isCalculatedField: true,
                        formula: "Amount*15"
                    }
                ]
            },
            enableGroupingBar: true
        });
    });

{% endhighlight %}

For server mode, you should set the **CalculationType** property to **CalculationType.Formula** and the **Formula** property to set the expression for the PivotComputation item in the PivotReport.

{% highlight c# %}

    private PivotReport BindDefaultData()
    {
        PivotReport pivotSetting = new PivotReport();
        pivotSetting.PivotRows.Add(new PivotItem { FieldMappingName = "Country", FieldHeader = "Country", TotalHeader = "Total" });
        pivotSetting.PivotColumns.Add(new PivotItem { FieldMappingName = "Product", FieldHeader = "Product", TotalHeader = "Total" });
        pivotSetting.PivotCalculations.Add(new PivotComputationInfo { CalculationName = "Amount", Description = "Amount", FieldHeader = "Amount", FieldName = "Amount", SummaryType = Syncfusion.PivotAnalysis.Base.SummaryType.DoubleTotalSum });
        pivotSetting.PivotCalculations.Add(new PivotComputationInfo  {
            CalculationName = "Price",
            FieldHeader = "Price",
            FieldName = "Price",
            CalculationType = CalculationType.Formula,
            Formula = "Amount * 10 + 12"
        });
        return pivotSetting;
    }

{% endhighlight %}


![JavaScript pivot grid control with user-defined field, aka calculated field](Calculated-Field_images/Calculated-Field1.png)