---
layout: post
title: Grouping-Bar
description: grouping bar
platform: js
control: PivotGrid
documentation: ug
---

# Grouping Bar

## Initialization 
Grouping Bar allows user to dynamically alter the report by filter and remove operations in the PivotGrid control. Based on the OLAP datasource and report bound to the PivotGrid control, Grouping Bar will be automatically populated. You can enable Grouping Bar option in PivotGrid by setting the [`enableGroupingBar`](/api/js/ejpivotgrid#members:enablegroupingbar) property to true.

### Client Mode

{% highlight js %}

<!--Create a tag which acts as a container for PivotGrid-->
    <div id="PivotGrid1" style="width: 55%; height: 670px; overflow: scroll; float: left;"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            dataSource: {
                data: "http://bi.syncfusion.com/olap/msmdpump.dll", //data
                catalog: "Adventure Works DW 2008 SE",
                cube: "Adventure Works",
                rows: [{
                    fieldName: "[Date].[Fiscal]"
                }],
                columns: [{
                    fieldName: "[Customer].[Customer Geography]"
                }],
                values: [{
                    measures: [{
                        fieldName: "[Measures].[Internet Sales Amount]",
                    }],
                    axis: "columns"
                }]
            },
            enableGroupingBar: true
        });
    });
</script>

{% endhighlight %}

![](Grouping-Bar_images/olapclientgroupingbar.png)


### Server Mode

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
        url: "/OLAPService",
        enableGroupingBar: true
    });
});

{% endhighlight %}

![](Grouping-Bar_images/olapgroupingbar.png)

## Searching Values
Search option available in Grouping Bar allows you to search a specific value that needs to be filtered from the list of values inside the filter pop-up window.

![](Grouping-Bar_images/OlapClntFiltering.png)

![](Grouping-Bar_images/olapclientsearching.png)

## Filtering Values
Filtering option available in Grouping Bar allows you to select a specific set of values that needs to be displayed in the PivotGrid control. At least one value needed to be in checked state while filtering otherwise “Ok” button will be disabled.

![](Grouping-Bar_images/OlapClntFiltering.png)

![](Grouping-Bar_images/olapclientfiltering.png)

## Removing Field
Remove option available in the Grouping Bar allows you to completely remove a specific field from the PivotGrid control. Remove operation can be either achieved by clicking remove icon available inside each field or by dragging and dropping field out of Grouping Bar region.

![](Grouping-Bar_images/Olapclientremove.png)

![](Grouping-Bar_images/OlapAFRemoving.png)


