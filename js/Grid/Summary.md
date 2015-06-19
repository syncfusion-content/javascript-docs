---
layout: post
title: Summary
description: summary 
platform: js
control: Grid
documentation: ug
---

# Summary 

**Summary** is a key feature of **Grid** that is used to aggregate a particular column. This is useful to analyse the details of a particular column. It has the following types:

* Sum

* Average 

* Count

* Minimum

* Maximum

* Custom

## Default Summary

There are some default summary types available for basic summary formula. The following code example is for Default Summary Types. We can render summary rows using **showSummary** and **summaryRows** property in **ejGrid.**

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          /// the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          showSummary: true,
          pageSettings: { pageSize: 5 },
          summaryRows: [
               { title: "Sum", summaryColumns: [{ summaryType: ej.Grid.SummaryType.Sum, displayColumn: "Freight", dataMember: "Freight", format: "{0:C2}" }] },
               { title: "Average", summaryColumns: [{ summaryType: ej.Grid.SummaryType.Average, displayColumn: "Freight", dataMember: "Freight", format: "{0:C2}" }] },
          ],
          columns: [
                     { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
                     { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 80 },
                     { field: "ShipCity", headerText: "Ship City", width: 90 },
                     { field: "ShipName", headerText: "Ship Name", width: 110 },
                     { field: "ShipCountry", headerText: "Ship Country", width: 100 },
                     { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 80, format: "{0:C}" }
          ]
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Summary_images/Summary_img1.png" Caption="Summary"%}

## Custom Summary by String

This property helps you to create custom summary formula for summary. The following code example is for custom summary using **Essential JavaScript**. Using **customSummaryValue** property to achieve custom summay for ejGrid.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
  
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          showSummary: true,
          pageSettings: { pageSize: 5 },
          summaryRows: [{ title: "Currency", summaryColumns: [{ summaryType: ej.Grid.SummaryType.Custom, customSummaryValue: currency(), displayColumn: "Freight", format: "{0:C2}" }] }
          ],
          columns: [
              { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 70 },
               { field: "CustomerID", headerText: "Customer ID", textAlign: ej.TextAlign.Left, width: 70 },
               { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 70 },
               { field: "ShipCity", headerText: "Ship City", textAlign: ej.TextAlign.Left, width: 70 },
               { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 70, format: "{0:C2}" }
          ],
      });
      function currency() {
          var rs = 100000;
          var dol = 0.017
          return (rs * dol);
      }
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Summary_images/Summary_img2.png" Caption="Custom Summary"%}

## Custom Summary by Function

**Custom Summary** is used to create custom summary formula for summary. The following code example is for custom summary using **Essential JavaScript**.

{% highlight html %}



 <div id="Grid"></div>

    <script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from jsondata.min.js
                dataSource: window.gridData,
                allowPaging: true,
                showSummary: true,
                pageSettings: { pageSize: 5 },
                summaryRows: [{
                    title: "Currency", summaryColumns: [{
                        summaryType: ej.Grid.SummaryType.Custom,
                        customSummaryValue: currency, displayColumn: "Freight", format: "{0:C2}"
                    }]
                }],
                columns: ["OrderID", "EmployeeID", "ShipCity", "Freight"],
            });

        });

        function currency() {
            var rs = 100000;
            var dol = 0.017;
            return (rs * dol);
        }

    </script>



{% endhighlight %}



{% include image.html url="/js/Grid/Concepts-and-Features/Summary_images/Summary_img3.png" Caption="Custom Summary by Function"%}

## Group Summary

This property helps you to enable the group summary column in **Grid**. The following code example is for Group summary.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      // the datasource "window.gridData" is referred from jsondata.min.js
      var data = window.gridData;
      $("#Grid").ejGrid({
          dataSource: data,
          allowPaging: true,
  
          allowGrouping: true,
          showSummary: true,
          pageSettings: { pageSize: 8 },
          summaryRows: [
              { summaryColumns: [{ summaryType: ej.Grid.SummaryType.Sum, displayColumn: "Freight", dataMember: "Freight", format: "{0:C2}", prefix: "Sum = " }], showTotalSummary: false }
          ],
          groupSettings: { groupedColumns: ["CustomerID"] },
          columns: [
                    { field: "OrderID", headerText: "Order ID", width: 80, isPrimaryKey: true, textAlign: ej.TextAlign.Right,  },
                    { field: "CustomerID", headerText: "Customer ID", textAlign: ej.TextAlign.Left, width: 75 },
                    { field: "ShipCity", headerText: 'Ship City', textAlign: ej.TextAlign.Left, width: 150 },
                    { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "Freight", headerText: "Freight", width: 75, textAlign: ej.TextAlign.Right, format: "{0:C}" }
          ]
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Summary_images/Summary_img4.png" Caption="Group Summary"%}

## Caption Summary

This property is used to create Caption Summary column in **Grid**. **showCaptionSummary** property is used to show the caption summary in grid. The following code example is for Caption Summary.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      // the datasource "window.gridData" is referred from jsondata.min.js
  
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowPaging: true,
          allowGrouping: true,
          showSummary: true,
          pageSettings: { pageSize: 10 },
          summaryRows: [{ showCaptionSummary: true, summaryColumns: [{ summaryType: ej.Grid.SummaryType.Average, displayColumn: "Freight", dataMember: "Freight", format: "{0:C2}", prefix: "Average = " }], showTotalSummary: false }],
          groupSettings: { groupedColumns: ["CustomerID"] },
          columns: [
                    { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 80, isPrimaryKey: true },
                    { field: "CustomerID", headerText: "Customer ID", textAlign: ej.TextAlign.Left, width: 75 },
                    { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "Freight", headerText: "Freight", width: 75, textAlign: ej.TextAlign.Right, format: "{0:C}" }
          ]
      });
  });
</script>

{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Summary_images/Summary_img5.png" Caption="Caption Summary"%}

