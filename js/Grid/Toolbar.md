---
layout: post
title: Toolbar
description: Toolbar
platform: js
control: Grid
documentation: ug
---
# Toolbar

Toolbar can be shown by defining [`toolbarSettings.showToolbar`](http://help.syncfusion.com/js/api/ejgrid#members:toolbarsettings-showtoolbar "toolbarSettings.showToolbar") should be true. Toolbar has option to add default items in [`toolbarSettings.toolbarItems`](http://help.syncfusion.com/js/api/ejgrid#members:toolbarsettings-toolbaritems "toolbarSettings.toolbarItems") and customized items in [`toolbarSettings.customToolbarItems`](http://help.syncfusion.com/js/api/ejgrid#members:toolbarsettings-customtoolbaritems "").

## Default Toolbar items

The following table shows default toolbar items and its action. 

<table>
<tr>
<td>
Default toolbar items<br/><br/></td><td>
Action<br/><br/></td></tr>
<tr>
<td>
Add<br/><br/></td><td>
Add a new row<br/><br/></td></tr>
<tr>
<td>
Edit<br/><br/></td><td>
Edit an existing<br/><br/></td></tr>
<tr>
<td>
Delete<br/><br/></td><td>
Delete a row<br/><br/></td></tr>
<tr>
<td>
Update<br/><br/></td><td>
Update edited or added row<br/><br/></td></tr>
<tr>
<td>
Cancel<br/><br/></td><td>
Cancel edited or added row<br/><br/></td></tr>
<tr>
<td>
Search<br/><br/></td><td>
Search text in records<br/><br/></td></tr>
</table>


{% highlight html %}
<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
  
      // the datasource "window.gridData" is referred from jsondata.min.js
  
      dataSource: window.gridData,
  
      toolbarSettings: {
  
          showToolbar: true,
  
          toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel]
  
      },
  
      allowPaging: true,
  
      editSettings: { allowEditing: true, allowAdding: true,allowDeleting: true},
  
      columns:
          [
              { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 90 },
              { field: "CustomerID", headerText: 'Customer ID', width: 90 },
              { field: "EmployeeID", headerText: 'Employee ID',editType: ej.Grid.EditingType.Dropdown,textAlign: ej.TextAlign.Right,width: 80 },
              { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, width: 80, format: "{0:C}" },
              { field: "ShipName", headerText: 'Ship Name', width: 150 }
          ]
  
  });
  
</script>


{% endhighlight %}

![](Toolbar_images/Toolbar_img1.png)


I>[ [`editSettings.allowAdding`](http://help.syncfusion.com/js/api/ejgrid#members:editsettings-allowadding ""), [`editSettings.allowEditing`](http://help.syncfusion.com/js/api/ejgrid#members:editsettings-allowediting "") and [`editSettings.allowDeleting`](http://help.syncfusion.com/js/api/ejgrid#members:editsettings-allowdeleting "") need to be enabled for add, delete, edit, save & cancel in [`toolbarItems`](http://help.syncfusion.com/js/api/ejgrid#members:toolbarsettings-toolbaritems ""). [`allowSearching`](http://help.syncfusion.com/js/api/ejgrid#members:allowsearching "")` to be enabled while adding Search in toolbar to perform search action.]

## Custom Toolbar items

Custom toolbar is used to create your own toolbar items in toolbar. It can add by defining [`toolbarSettings.customToolbarItems`](http://help.syncfusion.com/js/api/ejgrid#members:toolbarsettings-customtoolbaritems "").  Actions for this customized toolbar is defined in [`toolbarClick`](http://help.syncfusion.com/js/api/ejgrid#events:toolbarclick "") event.

{% highlight html %}
<div id="Grid"></div>
<script id="Refresh" type="text/x-jsrender">
  <a class="e-toolbaricons e-icon refresh" />
</script>
<script type="text/javascript">
  function onToolBarClick(args) {
      var tbarObj = $(args.target),
        grid = this;
      if (tbarObj.hasClass("Collapse")) grid.collapseAll(); //collapse Grid using grid instance, `this` is grid instance
      else grid.refreshContent(); //refresh content using grid instance
  }
  $("#Grid").ejGrid({
      // the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      toolbarSettings: {
          showToolbar: true,
          customToolbarItems: ["Collapse", {
              templateID: "#Refresh"
          }]
      },
      toolbarClick: "onToolBarClick",
      allowPaging: true,
      allowGrouping: true,
      groupSettings: {
          groupedColumns: ["ShipCity"]
      },
      columns:
          [
              { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 75 },
              { field: "CustomerID", headerText: "Customer ID", width: 100 },
              { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 75 },
              { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 70, format: "{0:C}" },
              { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
  });
</script>
<style type="text/css" class="cssStyles">
  .Collapse:before {
  content: "\e625";
  }
  .refresh:before {
  content: "\e677";
  }
</style>


{% endhighlight %}

![](Toolbar_images/Toolbar_img2.png)


