---
layout: post
title: Named Set with PivotClient widget for Syncfusion Essential JS
description: named set
platform: js
control: PivotClient
documentation: ug
---

# Named set

Named set is a multidimensional expression (MDX) that returns a set of dimension members, which can be created by combining the cube data, arithmetic operators, numbers, and functions. You can set the named set option in the pivot client by setting the [`isNamedSets`](/api/js/ejpivotclient#members:datasource-columns-isnamedsets) property to true for client mode.

## Client mode

You can bind the named sets in the pivot client by setting it's unique name in the [`fieldName`](/api/js/ejpivotclient#members:datasource-columns-fieldname) property either in row or column axis and [`isNamedSets`](/api/js/ejpivotclient#members:datasource-columns-isnamedsets) Boolean property to true.

{% highlight js %}

<!--Create a tag which acts as a container for PivotGrid-->
 <div id="PivotClient1" style="height: 350px; width: 100%; overflow: auto"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotClient1").ejPivotClient({
            dataSource: {
                data: "https://bi.syncfusion.com/olap/msmdpump.dll", //data
                catalog: "Adventure Works DW 2008 SE",
                cube: "Adventure Works",
                rows: [{
                    fieldName: "[Date].[Fiscal]"
                }],
                columns: [{
                    fieldName: "[Core Product Group]",
                    isNamedSets: true
                }],
                values: [{
                    measures: [{
                        fieldName: "[Measures].[Internet Sales Amount]",
                    }],
                    axis: "columns"
                }]
            }
        });
    });
</script>

{% endhighlight %}

## Server mode

You can add the named sets in the pivot client by using the `NamedSetElement` Class in the OLAP report.

{% highlight C# %}

OlapReport olapReport = new OlapReport();
olapReport.Name = "Customer Report";
olapReport.CurrentCubeName = "Adventure Works";

DimensionElement dimensionElementRow = new DimensionElement();
dimensionElementRow.Name = "Date";
dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");

MeasureElements measureElementColumn = new MeasureElements();
measureElementColumn.Elements.Add(new MeasureElement {
Name = "Internet Sales Amount"
});

NamedSetElement dimensionElementColumn = new NamedSetElement();
dimensionElementColumn.Name = "Core Product Group";

olapReport.CategoricalElements.Add(dimensionElementColumn);
olapReport.CategoricalElements.Add(measureElementColumn);
olapReport.SeriesElements.Add(dimensionElementRow);

{% endhighlight %}

![Named set in JavaScript pivot client control](KPI_images/namedset.png)
