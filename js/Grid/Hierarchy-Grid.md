---
layout: post
title: Hierarchy-Grid
description: hierarchy grid
platform: js
control: Grid
documentation: ug
---

# Hierarchy Grid

**Hierarchy Grid** feature allows you to add the **Grid** control inside the **Grid** row. When you want to view the child Grid, you can expand the **Grid**. Bind the data to child Grid by assign the foreign key field to **queryString** property.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      var data = ej.DataManager(window.employeeView).executeLocal(ej.Query().take(9));
      var dataManger = ej.DataManager({
          url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/"
      });
  
      var dataManger2 = ej.DataManager({
          url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Customers/"
      });
  
      $("#Grid").ejGrid({
          dataSource: data,
          allowPaging: true,
          allowSorting: true,
          columns: ["EmployeeID", "FirstName", "Title", "City", "Country"],
          childGrid: {
              dataSource: dataManger,
              queryString: "EmployeeID",
              allowPaging: true,
              columns: ["OrderID", "ShipCity", "Freight", "ShipName"],
              childGrid: {
                  dataSource: dataManger2,
                  queryString: "CustomerID",
                  columns: ["CustomerID", "Phone", "Address", "Country"],
              },
          },
      });
  });
  
</script>


{% endhighlight %}



{% include image.html url="/js/Grid/Hierarchy-Grid_images/Hierarchy-Grid_img1.png"%}

