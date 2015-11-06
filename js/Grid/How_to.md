---
layout: post
title: How to Grid
description: How to Grid
platform: js
control: Grid
documentation: ug
---
# How to

## Display Tooltip

To apply tooltip for cells, You need to use [`customAttributes`](http://help.syncfusion.com/js/api/ejgrid#members:columns-customattributes) in columns. For more reference, about [`cutomAttributes`](columns/customAttributes).

<table>
<tr>
<td>
<div id="Grid"></div><br/><br/><script type="text/javascript"><br/><br/>$("#Grid").ejGrid({<br/><br/>dataSource: window.gridData,<br/><br/>allowPaging: true,<br/><br/>columns: [{<br/><br/>field: "OrderID",<br/><br/>headerText: "Order ID",<br/><br/>width: 75,<br/><br/>textAlign: ej.TextAlign.Right<br/><br/>},<br/><br/>{<br/><br/>field: "CustomerID",<br/><br/>headerText: "Customer ID",<br/><br/>width: 80,<br/><br/>customAttributes: {<br/><br/>title: "{{:CustomerID}}"<br/><br/>}<br/><br/>},<br/><br/>{<br/><br/>field: "EmployeeID",<br/><br/>headerText: "Employee ID",<br/><br/>width: 75,<br/><br/>textAlign: ej.TextAlign.Right<br/><br/>},<br/><br/>{<br/><br/>field: "Freight",<br/><br/>width: 75,<br/><br/>format: "{0:C}",<br/><br/>textAlign: ej.TextAlign.Right<br/><br/>}]<br/><br/>});<br/><br/></script><br/><br/></td></tr>
</table>
## Binding SignalR endpoint

Grid  supports SignalR features for live updates in record. Please find the below option to configure signalR with Grid. 

1) Before configure SignalR with ejGrid. You need to Setup SignalR configuration in visual studio project. For reference, please find the link.

N> [signalR](http://www.asp.net/signalr/overview/getting-started/tutorial-getting-started-with-signalr#setup "signalr") 



2) After configuration of SignalR, you have to create Hub for communication between different actions of grid. 
{% highlight c# %}

public class SignalHub: Hub

{

	public void modify(string action, string details)

	{

		Clients.All.modify(action, details);

	}

}

{% endhighlight %}

3) Implementation of SignalR communication with Grid through Hub.
{% highlight js %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      var data = ej.DataManager(window.gridData).executeLocal(ej.Query().take(50));
      $("#Editing").ejGrid({
          dataSource: data,
          allowPaging: true,
          allowSorting: true,
          actionComplete: "actionComplete",
          editSettings: {
              allowEditing: true,
              allowAdding: true,
              allowDeleting: true
          },
          toolbarSettings: {
              showToolbar: true,
              toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel]
          },
          columns:
              [
                  { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                  { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
              ]
      });
      window.signal = $.connection.signalHub;
      window.signal.client.modify = function (action, details) {
          details = JSON.parse(details);
          if (action == "add") $("#Editing").ejGrid("addRecord", details);
          else if (action == "beginedit") $("#Editing").ejGrid("updateRecord", "OrderID", details);
          else $("#Editing").ejGrid("deleteRecord", "OrderID", details);
      };
      $.connection.hub.start().done(function () {
          window.actionComplete = function (args) {
              if (args.requestType == "save" || args.requestType == "delete") window.signal.server.modify(args.requestType == "delete" ? args.requestType : window.previousAction, JSON.stringify(args.data));
              if (args.requestType != "delete") window.previousAction = args.requestType;
          }
      });
  });
  
</script>


{% endhighlight %}

## Copy data from Excel to Grid

This [blog](https://www.syncfusion.com/blogs/post/Copying-and-Pasting-Excel-Sheet-Data-to-Grid-ASPNET-MVC.aspx) is about conversion of Excel to JSON data. After got JSON data you can bind it to Grid. 


