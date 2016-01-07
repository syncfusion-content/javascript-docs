---
layout: post
title: Tooltip and signalR binding with Grid widget for Syncfusion Essential JS
description: How to use tooltip and signalR binding in Grid
platform: js
control: Grid
documentation: ug
---
# How to

## Display Tooltip

To apply tooltip for cells, You need to use [`customAttributes`](http://help.syncfusion.com/js/api/ejgrid#members:columns-customattributes) in columns. For more reference, about [`cutomAttributes`](http://help.syncfusion.com/js/grid/columns#custom-attribute).

{% highlight html %}
<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                allowPaging: true,
                columns: [
                    { field: "OrderID", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "CustomerID", headerText: "Customer ID", width: 80, customAttributes: { title: "{{:CustomerID}}" } },
                    { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right }]
            });
        });
  {% endhighlight %}   
  
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


## Prevent/Maintain persistence of properties

Grid actions can be persisted throughout by enabling the enablePersistence property of the Grid. But we can maintain/prevent a grid action explicitly with the help of `addToPersist` and `ignoreOnPersist` methods respectively.

{% highlight html %}
<a href="http://www.syncfusion.com">Navigate to another Page</a>
<button id="btn">Prevent/Maintain persistence</button>
<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                allowFiltering: true,
                filterSettings: {filterType: "menu"},
                allowPaging: true,
                allowGrouping: true,
                enablePersistence: true,
                columns: [
                    { field: "OrderID", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "CustomerID", headerText: "Customer ID", width: 80},
                    { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right }]
            });
            $("#btn").ejButton({
            click: function(args){
                var gridObj = $("#Grid").ejGrid("instance");//get the gridObject
                // by default the enableAltRow property of the grid is true.
                gridObj.option("model.enableAltRow", false);   //set the enableAltRow property of the grid as false 
                //by default the filterSettings and groupSettings will be persisted upon navigating to another page.
                gridObj.ignoreOnPersist(["filterSettings", "groupSettings"]);// set the properties that are to be prevented from being persisted
                //by default the enableAltRow property of the grid will not be persisted
                gridObj.addToPersist("enableAltRow");// set the properties that are to be maintained for persistence.
            }
            });
        });
  {% endhighlight %}   
  
  So on navigating to another page by clicking on the link, by default the filterSettings and groupSettings will be persisted. But upon clicking the button and navigating, the persist state of the grid actions are modified.