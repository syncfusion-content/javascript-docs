---
layout: post
title: KPI with PivotClient widget for Syncfusion Essential JS
description: This document illustrates that how to enable key performance indicator (KPI) in JavaScript PivotClient control
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# KPI

Key Performance Indicators (KPI) are the business metrics that help to figure out the progress of an enterprise when meeting its business goals.

The different indicators available in the KPI are:

* KPI value: A physical measure or a calculated measure.
* KPI goal: Defines the target for the measure.
* KPI status: Evaluates the current status of the value compared to the goal.
* KPI trend: Evaluates the current trend of the value compared to the goal.

The **“KpiElements”** class in OLAP Base library holds the KPI name, and when its object is added to an OlapReport, you can view the resultant information in the pivot client.

To enable the KPI option, set the [`enableKPI`](/api/js/ejpivotclient#members:enablekpi) property to `true`.

## Client mode

{% highlight js %}

<!--Create a tag which acts as a container for PivotClient-->
 <div id="PivotClient1"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotClient1").ejPivotClient({
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
                    }, {
                        fieldName: "[Measures].[Growth in Customer Base Status]"
                    }],
                    axis: ej.olap.AxisName.Column
                }]
            },
            enableKPI:true
        });
    });
</script>

{% endhighlight %}

![KPI in JavaScript pivot client with OLAP client mode](KPI_images/clientmode-kpi.png)

## Server mode

### Client side property declaration

{% highlight html %}

    $(function() {
        $("#PivotClient1").ejPivotClient({
        //...
        enableKPI:true
        });
    });

{% endhighlight %}

### Framing OLAP report with KPI elements

{% highlight c# %}

OlapReport olapReport = new OlapReport();
olapReport.Name = "KPI Report";
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

![KPI in JavaScript pivot client with OLAP server mode](KPI_images/KPI.png)

