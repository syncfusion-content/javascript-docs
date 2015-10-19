---
layout: post
title: Enable-Persistence
description: enable persistence
platform: js
control: Grid
documentation: ug
---

# Enable Persistence

**Grid** widget can store the model value in the browser **cookies** and on every time after initial rendering, the control get the model from the cookie only.Using [`enablePersistence`](/js/api/ejgrid#members:enablepersistence "enablePersistence") property you can store the model value in cookies. Thus when any changes are made dynamically then those values are updated in cookie. On refreshing the page the past state of the Grid control is maintained in cookie and control is rendered from it. They following features support persistence in Grid.

* Paging
* Grouping
* Sorting
* Filtering
* Selection


{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSorting: true,
          allowGrouping: true,
          enableAltRow: true,
          enablePersistence: true,
          columns: [
                 { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 65 },
                 { field: "CustomerID", headerText: "Customer ID", width: 90 },
                 { field: "ShipCity", headerText: "Ship City", width: 90 },
                 { field: "Freight", headerText: "Freight", width: 90, textAlign: ej.TextAlign.Right, format: "{0:C}" },
                 { field: "ShipCountry", headerText: "Ship Country", width: 90 },
                 { field: "EmployeeID", headerText: "Employee ID", width: 90, textAlign: ej.TextAlign.Right }
          ]
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

![](/js/Grid/Enable-Persistence_images/Enable-Persistence_img1.png)

