---
layout: post
title: Hierarchical binding with Grid widget for Syncfusion Essential JS
description: How to bind the hierarchical data
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Hierarchical Bindings

Hierarchical binding can be used to create the Grid with parent and child relation, this facilitate you to view the child records for a particular row by clicking on the Expander button present in first column of each grid row. This can be enabled by defining [`childGrid`](https://help.syncfusion.com/api/js/ejgrid#members:childgrid "childGrid") and `childGrid.queryString`. [`childGrid`](https://help.syncfusion.com/api/js/ejgrid#members:childgrid "childGrid") is to define options of child and `childGrid.queryString` is to define the relation between parent and child grid.

N> The Grid's responsive and exporting support is not applicable for Hierarchical binding.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  // the datasource "window.employeeView" is referred from jsondata.min.js
  
  var data = window.employeeView;
  
  var dataManger = ej.DataManager({
  
      url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/"
  
  });
  
  $("#Grid").ejGrid({
      dataSource: data,
      childGrid: {
          dataSource: dataManger,
          queryString: "EmployeeID",
          allowPaging: true,
          pageSettings: {
              pageSize: 5
          },
          columns: [
              { field: "OrderID", headerText: 'Order ID', textAlign: ej.TextAlign.Right, width: 85 },
              { field: "ShipCity",headerText: 'Ship City', textAlign: ej.TextAlign.Left,width: 100},
              { field: "Freight", headerText: 'Freight',  textAlign: ej.TextAlign.Left,width: 120},
              { field: "ShipName", headerText: 'Ship Name', textAlign: ej.TextAlign.Left, width: 100 }
          ]
      },
      columns:
          [
              {field: "EmployeeID", headerText: 'Employee ID',textAlign: ej.TextAlign.Right,width: 85},
              {field: "FirstName",headerText: 'First Name',textAlign: ej.TextAlign.Left,width: 100},
              { field: "Title", headerText: 'Title', textAlign: ej.TextAlign.Left, width: 120 },
              { field: "City", headerText: 'City', textAlign: ej.TextAlign.Left, width: 10 },
              { field: "Country", headerText: 'Country', textAlign: ej.TextAlign.Left, width: 100 }
          ]
  
  });
  
</script>



{% endhighlight %}

![](Hierarchy-Grid_images/HierarchyGrid_img1.png)


## Expand or Collapse All Child

The Grid can able to expand and collapse all the [`childGrid`](https://help.syncfusion.com/api/js/ejgrid#members:childgrid "childGrid") through programmatically using [`expandAll`](https://help.syncfusion.com/api/js/ejgrid#methods:expandall "expandAll") and [`collapseAll`](https://help.syncfusion.com/api/js/ejgrid#methods:collapseall "collapseAll") method.

{% highlight html %}
<button id="expand">expandAll</button>
<button id="collapse">collapseAll</button>
<div id="Grid"></div>
<script type="text/javascript">
  var data = window.employeeView;
  var dataManger = ej.DataManager({
    url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/"
  });
  $("#expand,#collapse").ejButton({
    showRoundedCorner: true,
    size: "mini",
    width: 150,
    click: function(args) {
      $("#Grid").ejGrid(args.model.text); //invokes expandAll & collapseAll method based on button name
    }
  });
  $("#Grid").ejGrid({
    dataSource: data,
    childGrid: {
      dataSource: dataManger,
      queryString: "EmployeeID",
      allowPaging: true,
      pageSettings: {
        pageSize: 5
      }
    }
  });
</script>



{% endhighlight %}

