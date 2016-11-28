---
layout: post
title: Toolbar with Grid widget for Syncfusion Essential JS
description: How to enable toolbar and its actions.
platform: js
control: Grid
documentation: ug
---
# Toolbar

Toolbar can be shown by defining [`toolbarSettings.showToolbar`](http://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-showtoolbar "showToolbar") should be true. Toolbar has option to add default items in [`toolbarSettings.toolbarItems`](http://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-toolbaritems "toolbarItems") and customized items in [`toolbarSettings.customToolbarItems`](http://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-customtoolbaritems "customToolbarItems").

## Default Toolbar items

The following table shows default toolbar items and its action. 

<table>
<tr>
<th>
Default toolbar items</th><th>
Action</th></tr>
<tr>
<td>
Add</td><td>
Add a new row</td></tr>
<tr>
<td>
Edit</td><td>
Edit an existing</td></tr>
<tr>
<td>
Delete</td><td>
Delete a row</td></tr>
<tr>
<td>
Update</td><td>
Update edited or added row</td></tr>
<tr>
<td>
Cancel</td><td>
Cancel edited or added row</td></tr>
<tr>
<td>
Search</td><td>
Search text in records</td></tr>
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


I> [`editSettings.allowAdding`](http://help.syncfusion.com/api/js/ejgrid#members:editsettings-allowadding "allowAdding"), [`editSettings.allowEditing`](http://help.syncfusion.com/api/js/ejgrid#members:editsettings-allowediting "allowEditing") and [`editSettings.allowDeleting`](http://help.syncfusion.com/api/js/ejgrid#members:editsettings-allowdeleting "allowdeleting") need to be enabled for add, delete, edit, save & cancel in [`toolbarItems`](http://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-toolbaritems "toolbaritems"). [`allowSearching`](http://help.syncfusion.com/api/js/ejgrid#members:allowsearching "allowsearching")` to be enabled while adding Search in toolbar to perform search action.

## Custom Toolbar items

Custom toolbar is used to create your own toolbar items in toolbar. It can add by defining [`toolbarSettings.customToolbarItems`](http://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-customtoolbaritems "customToolbarItems").  Actions for this customized toolbar is defined in [`toolbarClick`](http://help.syncfusion.com/api/js/ejgrid#events:toolbarclick "toolbarclick") event.

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


