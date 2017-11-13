---
layout: post
title: Drill-Down-Support
description: drill down support
platform: js
control: TreeMap
documentation: ug
api: /api/js/ejtreemap
---

# Drill Down Support

**Treemap** enables drill down to expose the hierarchy achieved by clicking on a node and this results in enabling the **Treemap** to move to the next level or sub level and can return back to the normal **Treemap** view by clicking on the node header. Only a single level of the **Treemap** is visible at once.

## Enable Drill Down

**Treemap** elements can be drilled down by setting the [`enableDrillDown`](../api/ejtreemap#members:enabledrilldown) property to true. You can view the hierarchy of the **Treemap** by clicking on the treemap items and can move to the previous level by clicking on the drill down header. The header color can be customized by changing the values in the property [`drillDownHeaderColor`](../api/ejtreemap#members:drilldownheadercolor) and the selection color can be done by changing the [`drillDownSelectionColor`](../api/ejtreemap#members:drilldownselectioncolor) property.

<table>
<tr>
<th>
Property</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
enableDrillDown</td><td>
bool</td><td>
Gets or sets a value that indicates whether the drill down feature is enabled or not</td></tr>
<tr>
<td>
drillDownHeaderColor</td><td>
string</td><td>
Gets or sets a color for header during drill down</td></tr>
<tr>
<td>
drillDownSelectionColor</td><td>
string</td><td>
Gets or sets a color for highlighting tree map item during drill down.</td></tr>
</table>


{% highlight js %}

    <div  id="treemap" style="width: 700px;height:400px;"></div>
    
    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemap").ejTreeMap({
                dataSource: population_data,
                enableDrillDown: true,
                drillDownHeaderColor: "#199DAF",
                drillDownSelectionColor: "#199DAF",
                uniColorMapping: { color: "#CCDFE3" },
                weightValuePath: "Population",
                levels: [
                    { groupPath: "Continent", showLabels: true, groupGap: 5, headerHeight: 25, showHeader: true, headerTemplate: 'Template' },
                    { groupPath: "Country", showLabels: true, groupGap: 0, headerHeight: 25, showHeader: true, headerTemplate: 'Template' },
                    { groupPath: "Name", showLabels: true, groupGap: 0, headerHeight: 25, showHeader: true, headerTemplate: 'Template' }
                ]

            });
        });
    </script>

{% endhighlight %}



![](/js/TreeMap/Drill-Down-Support_images/Drill-Down-Support_img1.png)

_Before Drill Down_

![](/js/TreeMap/Drill-Down-Support_images/Drill-Down-Support_img2.png)

_After Drill Down_

Try it: [DrillDown](http://jsplayground.syncfusion.com/Sync_mrof3n0r)
