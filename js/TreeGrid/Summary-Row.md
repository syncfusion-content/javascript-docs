---
layout: post
title: Summary Row
description: summary row
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Summary Row

Summary rows in TreeGrid is used to summarize every hierarchy with the set of predefined summary types using the column values. 

* [`summaryRows`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows "summaryRows") - Using this property, user can define the summary rows in TreeGrid.
* [`summaryRows.title`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-title "summaryRows.title") - Title for each summary row can be defined using this property. 
* [`summaryRows.summaryColumns`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns "summaryRows.summaryColumns") - Using this property, it is possible to defined the summary for specific columns alone in a summary row.
* [`showSummaryRow`](https://help.syncfusion.com/api/js/ejtreegrid#members:showsummaryrow "showSummaryRow") - This property is to make the summary row visible. 
* [`showTotalSummary`](https://help.syncfusion.com/api/js/ejtreegrid#members:showtotalsummary "showTotalSummary") - This property is to make the total summary row visible which is the overall summary row displayed for all the rows in the TreeGrid content.

## Defining summary columns

* [`summaryType`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-summarytype "summaryRows.summaryColumn.summaryType") - Using this property, user can define the type of summary to be displayed in a column. 
* [`dataMember`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-datamember "summaryRows.summaryColumns.dataMember") - This property is used to map the field values which is used for summary calculations.
* [`displayColumn`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-displaycolumn "summaryRows.summaryColumns.displayColumn") - This property is used to specify the column in which the summary to be displayed.
* [`prefix`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-prefix "summaryRows.summaryColumns.prefix") and [`suffix`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-suffix "summaryRows.summaryColumns.suffix") properties are used to define the text should be displayed along with the summary column value.
* [`format`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-format "summaryRows.summaryColumns.format") property is used for formatting the summary column value.

The below code snippet explains defining a summary row in TreeGrid,
{% highlight js %}
        $("#treegrid").ejTreeGrid({
            showSummaryRow: true,
            showTotalSummary: true,
            summaryRows: [
                       {
                           title: "Maximum",
                           summaryColumns: [
                               {
                                   summaryType: ej.TreeGrid.SummaryType.Maximum,
                                   dataMember: "TotalUnits",
                                   displayColumn: "TotalUnits",
                                   prefix: "Maximum unit = "
                               },
                               {
                                   summaryType: ej.TreeGrid.SummaryType.Maximum,
                                   dataMember: "TotalCosts",
                                   displayColumn: "TotalCosts",
                                   prefix: "Maximum Cost = ",
                                   format: "{0:C}"
                               }
                           ]
                       },
                       {
                           title: "Total",
                           summaryColumns: [
                               {
                                   summaryType: ej.TreeGrid.SummaryType.Sum,
                                   dataMember: "TotalCosts",
                                   displayColumn: "TotalCosts",
                                   prefix: "Total costs = ",
                                   format: "{0:C}"
                               },
                               {
                                   summaryType: ej.TreeGrid.SummaryType.Sum,
                                   dataMember: "UnitWeight",
                                   displayColumn: "UnitWeight",
                                   prefix: "Total weight = ",
                                   suffix: " Pounds"
                               }]
                       }
            ],
            //...
        });
{% endhighlight %}
The below screenshot shows the output of above code example.
![](SummaryRows_images/SummaryRows_img1.png)

## Customize height of total summary

Using [`totalSummaryHeight`](https://help.syncfusion.com/api/js/ejtreegrid#members:totalSummaryHeight "totalSummaryHeight") property we can customize the height of the total summary container.
The below code example shows how to update the footer summary container height.
{% highlight js %}
  $("#treegrid").ejTreeGrid({
        showTotalSummary: true,
        totalSummaryHeight: 120,
            //...
        });
{% endhighlight %}
The below screenshot shows the output of above code example.
![](SummaryRows_images/SummaryRows_img2.png)

## Expand/collapse total summary row

We can expand/collapse the total summary rows in TreeGrid using following methods.

* Using Expander Icon
* Using Method

### Using Expander Icon

We can enable expander icon in total summary row by using [`collapsibleTotalSummary`](https://help.syncfusion.com/api/js/ejtreegrid#members:collapsibleTotalSummary "collapsibleTotalSummary") property. By default expander icon will be rendered in first row of 0th column in total summary rows.
Please find the below code example to enable collapsible total summary row in TreeGrid.
{% highlight js %}
  $("#treegrid").ejTreeGrid({
        showTotalSummary: true,
        collapsibleTotalSummary:true,       
            //...
        });
{% endhighlight %}
![](SummaryRows_images/SummaryRows_img3.png)

N> We can also customize the expander icon column in total summary row by using `_summaryColumnIndex` property and [`load`](https://help.syncfusion.com/api/js/ejgantt#events:load "load") event.

### Using  Method

Total summary rows in TreeGrid can be expanded/collapsed by using [`expandCollapseTotalSummary`](https://help.syncfusion.com/api/js/ejgantt#methods:expandCollapseTotalSummary "expandCollapseTotalSummary") method.
Please find the code example to collapse the total summary rows below.
{% highlight js %}
    <button onclick="expandCollapse()">expandCollapse</button>
    $("#treegrid").ejTreeGrid({
        showTotalSummary: true,
        collapsibleTotalSummary:true,
            //..
        });
    function expandCollapse() {
            var treeObj = $("#TreeGridContainer").data("ejTreeGrid");
            treeObj.expandCollapseTotalSummary(false);
        }
{% endhighlight %}

[Click](https://js.syncfusion.com/demos/web/#!/bootstrap/treegrid/rows/summaryrow) here to view the demo sample for summary row in TreeGrid.