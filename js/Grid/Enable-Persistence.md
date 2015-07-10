---
layout: post
title: Enable-Persistence
description: enable persistence
platform: js
control: Grid
documentation: ug
---

# Enable Persistence

**EnablePersistence** is used to maintain the current state of the grid model in browser's **local Storage**. When you refresh the page, stored state will be automatically used to render the grid. We can use [`enablePersistence`](/js/api/ejgrid#members:enablepersistence "enablePersistence") property to use enable persistence feature.

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

{% include image.html url="/js/Grid/Enable-Persistence_images/Enable-Persistence_img1.png"%}

