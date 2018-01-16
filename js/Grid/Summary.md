---
layout: post
title: Summary with Grid widget for Syncfusion Essential JS
description: How to enable summary and its functionalities
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Summary

Summary rows visibility can be controlled by the [`showSummary`](https://help.syncfusion.com/api/js/ejgrid#members:showsummary "showSummary") property and it can be added to grid by using the [`summaryRows`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows "summaryRows") array property. The following code example describes the above behavior.

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

N> [`dataMember`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-datamember "dataMember") denotes the aggregation column whereas the [`displayColumn`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-displaycolumn "displayColumn") denotes the value to be displayed column.


![](Summary_images/summaryGrid_img1.png)


## Supported Aggregates 

Following are the supported list of [aggregates](https://help.syncfusion.com/js/datamanager/summary#) 

* Sum
* Average
* Maximum
* Minimum
* False Count
* True Count

### Sum, Average, Maximum and Minimum


Summaries with the [`Sum`](https://help.syncfusion.com/js/datamanager/summary#sum "sum"),[`Average`](https://help.syncfusion.com/js/datamanager/summary#avg "Average"),[`Maximum`](https://help.syncfusion.com/js/datamanager/summary#max "maximum") and [`Minimum`](https://help.syncfusion.com/js/datamanager/summary#min "min") aggregate can be defined by using the [`summaryType`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-summarytype "summaryType") in [`summaryColumns`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns "summaryColumns") collections. These aggregate are used in `Number` column.

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


### True and False count 

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

Custom Summary can be used to create summary values based on your required custom logic and calculations. To enable Custom Summary, [`summaryType`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-summarytype "summaryType") should be [`custom`](https://help.syncfusion.com/js/grid/summary#custom-summary-by-string "custom") and [`customSummaryValue`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-customsummaryvalue "customSummaryValue") property need to define as function. In this property `value` function, you need to use Grid instance to access the `model.dataSource` and `model.currentViewData`. After the custom calculation, the returned value will be displayed in corresponding Summary cell.


{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  function currency() {
      //to get grid instance
      var gridObj = $("#Grid").ejGrid("instance");
      //ej.sum is aggregate to add data of freight from datasource
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

## Prefix And Suffix

Summaries with Prefix and Suffix can be added using the [`summaryColumns.prefix`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-prefix "summaryColumns.prefix") and summaryColumn.suffix [`summaryColumns.suffix`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-suffix "summaryColumns.suffix").

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
              format: "{0:C2}",
              prefix: "Summation = ", 
              suffix: " in US"
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

![](Summary_images/summaryGrid_img8.png)

## Title for Summary

Title name of any summary value can be change using [`title`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-title "title") property of [`summaryColumns`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns "summaryColumns"). Title displaying column can also be alter using the [`titleColumn`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-titlecolumn "titleColumn").

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
     // the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      showSummary: true,
      summaryRows: [{
          title: "Summation",
          titleColumn: "EmployeeID",
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

![](Summary_images/summaryGrid_img9.png)

## Group Summary

Group Summary is used to summarize values of a particular column based on group and it shows at bottom of each Group. To enable Group Summary for particular Group, you need to define the [`showTotalSummary`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-showtotalsummary "showTotalSummary") as false.

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

To show summaries in each Group's Caption row, particular [summary row](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows) should have the [`showTotalSummary`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-showtotalsummary "showtotalsummary") as `false` and [`showCaptionSummary`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-showcaptionsummary "showCaptionSummary") as `true`.


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

## Summary Template

Using the [`template`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-template "template") property of `summaryColumns` you can render any type of JsRender templates or customizing the summary value.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="templateData" type="text/x-jsrender">
     Freight has Average of {{:summaryValue}} in  dollars
</script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
    	 dataSource: ej.DataManager(window.gridData).executeLocal(new ej.Query().take(5)),
         showSummary: true,
         summaryRows: [{ 
             title: "Average",
             summaryColumns: [{ 
                 summaryType: ej.Grid.SummaryType.Average, 
                 displayColumn: "Freight", 
                 dataMember: "Freight",  
                 template: "#templateData",
                 format: "{0:C2}"
             }]
          }],
         columns: [{ field: "OrderID" },{ field: "EmployeeID" },{ field: "Freight", format: "{0:C}" }]
	});
});

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Summary_images/summaryGrid_img8.png)

## Format

To format Summary values, the [`format`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns-format "format") property needs to be assigned in the [`summaryColumns`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows-summarycolumns "summaryColumns") collection object.  To know more about formatting options. Please refer to [**globalize.js**](https://github.com/jquery/globalize/tree/v0.1.1#)

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



