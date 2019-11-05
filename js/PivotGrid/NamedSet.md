---
layout: post
title: Named Set with PivotGrid widget for Syncfusion Essential JS
description: named set
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Named Sets

Named sets is a multidimensional expression (MDX) that returns a set of dimension members, that can be created by combining cube data, arithmetic operators, numbers, and functions.

## Client mode

You can bind the named sets in the PivotGrid by setting it's unique name in the [`fieldName`](/api/js/ejpivotclient#members:datasource-columns-fieldname) property either in row or column axis and the [`isNamedSets`](/api/js/ejpivotclient#members:datasource-columns-isnamedsets) boolean property to "true".

{% highlight js %}

<!--Create a tag which acts as a container for PivotGrid-->
 <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
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

![NamedSet in JavaScript pivot grid OLAP client mode](KPI_images/namedset.png)


## Server mode

You can add named sets in the PivotGrid by using NamedSetElement Class in the OlapReport.

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

![NamedSset in JavaScript pivot grid OLAP server mode](KPI_images/servernamedset.png)


