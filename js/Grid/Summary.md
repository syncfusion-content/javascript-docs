---
layout: post
title: Summary with Grid widget for Syncfusion Essential JS
description: How to enable summary and its functionalities
platform: js
control: Grid
documentation: ug
---
# Summary

Summary rows visibility can be controlled by [`showSummary`](https://help.syncfusion.com/api/js/ejgrid#members:showsummary "showSummary") property and it can be added to grid by using [`summaryRows`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows "summaryRows") array property. The following code example describes the above behavior.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
     // the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      showSummary: true,
      summaryRows: [{
          title: "Sum",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Sum,
              displayColumn: "Freight",
              dataMember: "Freight",
              format: "{0:C2}"
          }]
      }],
      allowPaging: true,
      columns: [
          { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
          {field: "EmployeeID",headerText: "Employee ID",editType: ej.Grid.EditingType.NumericEdit,textAlign: ej.TextAlign.Right,width: 80 },
          {field: "ShipCity",headerText: "Ship City",width: 90},
          {field: "ShipCountry",headerText: "Ship Country", width: 100},
          { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 80, format: "{0:C}" }
      ]
  });
  
</script>
{% endhighlight %}

![](Summary_images/summaryGrid_img1.png)


## Supported Aggregates 

Following are the supported list of [aggregates](https://help.syncfusion.com/js/datamanager/summary#) 

* Sum
* Average
* Maximum
* Minimum
* False Count
* True Count

### Sum, Average, Maximum and minimum


Summaries with [`Sum`](https://help.syncfusion.com/js/datamanager/summary#sum "sum"),[`Average`](https://help.syncfusion.com/js/datamanager/summary#avg "Average"),[`Maximum`](https://help.syncfusion.com/js/datamanager/summary#max "maximum") and [`Minimum`](https://help.syncfusion.com/js/datamanager/summary#min "min") aggregate can be defined by using  [`summaryType`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-summarytype "summaryType") in [`summaryColumns`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns "summaryColumns") collections. These aggregate are used in `Number` column.

{% highlight html %}
<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
      /// the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      showSummary: true,
      summaryRows: [{
          title: "Sum",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Sum,
              displayColumn: "Freight",
              dataMember: "Freight",
              format: "{0:C2}"
          }]
      }, {
          title: "Average",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Average,
              displayColumn: "Freight",
              dataMember: "Freight",
              format: "{0:C2}"
          }]
      }, {
          title: "Maximum",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Maximum,
              displayColumn: "Freight",
              dataMember: "Freight",
              format: "{0:C2}"
          }]
      }, {
          title: "Minimum",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Minimum,
              displayColumn: "Freight",
              dataMember: "Freight",
              format: "{0:C2}"
          }]
      }],
      allowPaging: true,
      columns:
          [
              { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
              { field: "EmployeeID", headerText: "Employee ID", editType: ej.Grid.EditingType.NumericEdit, textAlign: ej.TextAlign.Right, width: 80 },
              { field: "ShipCity", headerText: "Ship City", width: 90 },
              { field: "ShipCountry", headerText: "Ship Country", width: 100 },
              { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 80, format: "{0:C}" }
          ]
  });
</script>



{% endhighlight %}

![](Summary_images/summaryGrid_img2.png)


### True and False Count 

Summaries with `True` and `False` count aggregate can be defined by using [`summaryType`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-summarytype "summaryType") [`summaryColumns`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns "summaryColumns") collections. `True` and `False` count aggregates are used for Boolean columns.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
      /// the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      showSummary: true,
      summaryRows: [{
          title: "False Count",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.FalseCount,
              displayColumn: "Verified",
              dataMember: "Verified"
          }]
      }, {
          title: "True Count",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.TrueCount,
              displayColumn: "Verified",
              dataMember: "Verified"
          }]
      }],
      allowPaging: true,
      columns:
          [
              { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
              { field: "EmployeeID", headerText: "Employee ID", editType: ej.Grid.EditingType.NumericEdit, textAlign: ej.TextAlign.Right, width: 80 },
              { field: "ShipCity", headerText: "Ship City", width: 90 },
              { field: "ShipCountry", headerText: "Ship Country", width: 100 },
              { field: "Verified", headerText: "Verified", width: 80 }
          ]
  });
</script>



{% endhighlight %}

![](Summary_images/summaryGrid_img3.png)


## Custom Summary

Custom Summary can be used to create summary values based on your required custom logic and calculations. To enable Custom Summary, [`summaryType`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-summarytype "summaryType") should be [`custom`](https://help.syncfusion.com/js/grid/summary#custom-summary-by-string "custom") and `value` property need to define as function. In this property `value` function, you need to use Grid instance to access `model.dataSource` and `model.currentViewData`. After the custom calculation, the returned value will be displayed in corresponding Summary cell.


{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  function currency() {
      //to get grid instance
      var gridObj = $("#Grid").ejGrid("instance");
      //ej.sum is aggreagte to add datas of freight from datasource
      return ej.sum(gridObj.model.dataSource, "Freight");
  }
  $("#Grid").ejGrid({
      // the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      showSummary: true,
      summaryRows: [{
          title: "Currency",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Custom,
              customSummaryValue: currency,
              displayColumn: "Freight",
              format: "{0:C2}"
          }]
      }],
      allowPaging: true,
      columns:
          [
              { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 70 },
              { field: "CustomerID", headerText: "Customer ID", textAlign: ej.TextAlign.Left, width: 70 },
              { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 70 },
              { field: "ShipCity", headerText: "Ship City", textAlign: ej.TextAlign.Left, width: 70 },
              { field: "Freight",  headerText: "Freight",textAlign: ej.TextAlign.Right, width: 70,format: "{0:C2}"}]
  });
</script>


{% endhighlight %}

![](Summary_images/summaryGrid_img4.png)


## Group Summary

Group Summary is used to summarize values of a particular column based on group and it shows at bottom of each Group. To enable Group Summary for particular Group, you need to define [`showTotalSummary`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-showtotalsummary "showTotalSummary") as false.

{% highlight html %}
<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
      // the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      showSummary: true,
      summaryRows: [{
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Sum,
              displayColumn: "Freight",
              dataMember: "Freight",
              format: "{0:C2}",
              prefix: "Sum = "
          }],
          showTotalSummary: false
      }],
      allowPaging: true,
      allowSorting: true,
      allowGrouping: true,
      groupSettings: {
          groupedColumns: ["CustomerID"]
      },
      columns:
          [
              { field: "OrderID", headerText: "Order ID", width: 80, isPrimaryKey: true },
              { field: "CustomerID", headerText: "Customer ID", textAlign: ej.TextAlign.Right, width: 75 },
              { field: "ShipCity", headerText: 'Ship City', width: 150 },
              { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
              { field: "Freight", headerText: "Freight", width: 75, textAlign: ej.TextAlign.Right, format: "{0:C}" }
          ]
  });
</script>



{% endhighlight %}

![](Summary_images/summaryGrid_img5.png)


W> Minimum one column should be grouped to show summary details.

## Group Caption Summary

To show summaries in each Group's Caption row, particular [summary row](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows) should have [`showTotalSummary`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-showtotalsummary "showtotalsummary") as `false` and [`showCaptionSummary`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-showcaptionsummary "showCaptionSummary") as `true`.


{% highlight html %}
<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
      dataSource: data,
      showSummary: true,
      summaryRows: [{
          showCaptionSummary: true,
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Average,
              displayColumn: "Freight",
              dataMember: "Freight",
              format: "{0:C2}",
              prefix: "Average = "
          }],
          showTotalSummary: false
      }],
      allowPaging: true,
      allowGrouping: true,
      groupSettings: {
          groupedColumns: ["EmployeeID"]
      },
      columns:
          [
              { field: "OrderID", headerText: "Order ID", width: 80, isPrimaryKey: true },
              { field: "CustomerID", headerText: "Customer ID", textAlign: ej.TextAlign.Right, width: 75 },
              { field: "ShipCity", headerText: 'Ship City', width: 150 },
              { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
              { field: "Freight", headerText: "Freight", width: 75, textAlign: ej.TextAlign.Right, format: "{0:C}" }
          ]
  });
</script>


{% endhighlight %}

![](Summary_images/summaryGrid_img6.png)


W> Minimum one column should be grouped to show summary details.

## Format

To format Summary values, [`format`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-format "format") property needs to be assigned in [`summaryColumns`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns "summaryColumns") collection object.  To know more about formatting options. Please refer [**globalize.js**](https://github.com/jquery/globalize/tree/v0.1.1#)

{% highlight html %}
<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
      /// the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      showSummary: true,
      summaryRows: [{
          title: "Sum",
          summaryColumns: [{
              summaryType: ej.Grid.SummaryType.Sum,
              displayColumn: "Freight",
              dataMember: "Freight",
              format: "{0:C2}"
          }]
      }],
      allowPaging: true,
      columns:
          [
              { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
              { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 80 },
              { field: "ShipCity", headerText: "Ship City", width: 90 },
              { field: "ShipCountry", headerText: "Ship Country", width: 100 },
              { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 80, format: "{0:C}" }
          ]
  });
</script>



{% endhighlight %}

![](Summary_images/summaryGrid_img7.png)



