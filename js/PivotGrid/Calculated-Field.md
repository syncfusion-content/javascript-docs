---
layout: post
title: Calculated Field
description: calculated field
platform: js
control: PivotGrid
documentation: ug
---

# Calculated Field

N> This feature is applicable only for Relational data source.

PivotGrid provides support to insert a new calculated field based on the existing Pivot Fields either through Calculated Field dialog or code behind.

### Through UI
To insert a new calculated Field, open the Calculated Field dialog using the Grouping Bar context menu. We can define "Name" for the new Calculated Field and "Formula" can be entered by inserting required fields through Fields section. For inserting numbers and operators, you can use formula pop-up as shown in the below screen-shot.

![](Calculated-Field_images/Calculated-Field-Popup.png)

Click **Add** for adding the respective Calculated Field and **OK** to populate the PivotGrid control.

### Through Code-behind

For client mode, Calculated Field can be created at code-behind by defining formula based on the existing Pivot Fields in the PivotGrid. To indicate a field as a calculated field we need to set [`isCalculatedField`](/api/js/ejpivotgrid#members:isCalculatedField) property to true and [`formula`](/api/js/ejpivotgrid#members:formula) property to set the expression.

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

For server mode, we need to set **CalculationType** property to **CalculationType.Formula** and **Formula** property to set the expression for the PivotComputation item in the PivotReport.

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


![](Calculated-Field_images/Calculated-Field1.png)