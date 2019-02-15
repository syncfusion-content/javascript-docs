---
layout: post
title: KPI with PivotGrid widget for Syncfusion Essential JS
description: key performance indicator (KPI)
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# KPI

Key Performance Indicators (KPI) are business metrics that help you to figure out the progress of an enterprise when meeting its business goals.

The different indicators available in the KPI are:

* KPI value: A physical measure or a calculated measure.
* KPI goal: Defines the target for the measure.
* KPI status: Evaluates the current status of the value compared to the goal.
* KPI trend: Evaluates the current trend of the value compared to the goal.

The **“KpiElements”** class in the OLAP base library holds the KPI name, and when its object is added to an OlapReport, you can view the resultant information in the PivotGrid.

## Client mode

{% highlight js %}

<!--Create a tag which acts as a container for PivotGrid-->
 <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            dataSource: {
                data: "https://bi.syncfusion.com/olap/msmdpump.dll",
                catalog: "Adventure Works DW 2008 SE",
                cube: "Adventure Works",
                rows: [{
                    fieldName: "[Date].[Fiscal]"
                }, ],
                columns: [{
                    fieldName: "[Product].[Product Categories]"
                }],
                values: [{
                    measures: [{
                        fieldName: "[Measures].[Internet Sales Amount]"
                    }, {
                        fieldName: "[Measures].[Growth in Customer Base Trend]"
                    }],
                    axis: ej.olap.AxisName.Column
                }]
            }
        });
    });
</script>

{% endhighlight %}


![Key Performance indicator, aka KPI support in JavaScript pivot grid client mode](KPI_images/ClientSideKPI.png)

## Server mode

{% highlight c# %}

OlapReport olapReport = new OlapReport();
olapReport.Name = "Sample Report";
olapReport.CurrentCubeName = "Adventure Works";

MeasureElements measureElementColumn = new MeasureElements();
measureElementColumn.Elements.Add(new MeasureElement {
    Name = "Gross Profit"
});

DimensionElement dimensionElementRow = new DimensionElement();
dimensionElementRow.Name = "Date";
dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");

KpiElements kpiElement = new KpiElements();
kpiElement.Elements.Add(new KpiElement {
    Name = "Revenue", ShowKPIStatus = true, ShowKPIGoal = false, ShowKPITrend = true, ShowKPIValue = true
});

olapReport.CategoricalElements.Add(kpiElement);
olapReport.CategoricalElements.Add(measureElementColumn);
olapReport.SeriesElements.Add(dimensionElementRow);

{% endhighlight %}

![Key Performance indicator, aka KPI support in JavaScript pivot grid server mode](KPI_images/kpi.png)

