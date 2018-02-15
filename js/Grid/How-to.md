---
layout: post
title: How to
description: How to
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# How to

## Binding SignalR endpoint

Grid  supports SignalR features for live updates in record. Please find the below option to configure signalR with Grid. 

1) Before configure SignalR with ejGrid. You need to Setup SignalR configuration in Visual Studio project. For reference, please find the link.

N> Getting started with [SignalR](http://www.asp.net/signalr/overview/getting-started/tutorial-getting-started-with-signalr#setup "signalr") 



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
{% highlight javascript %}

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
              if (args.requestType == "save" || args.requestType == "delete") window.signal.server.modify(args.requestType == "delete" ? args.requestType : window.previousAction, JSON.stringify(args.rowData));
              if (args.requestType != "delete") window.previousAction = args.requestType;
          }
      });
  });
  
</script>


{% endhighlight %}

## Copy data from Excel to Grid

Copy data from Excel to Grid is possible by converting Excel data to JSON data and then binding it to the Grid. Details are covered in this [blog](https://www.syncfusion.com/blogs/post/Copying-and-Pasting-Excel-Sheet-Data-to-Grid-ASPNET-MVC.aspx) post. 


## Prevent/Maintain persistence of properties

Grid actions can be persisted throughout by enabling the enablePersistence property of the Grid. However, we can maintain/prevent a grid action explicitly with the help of `addToPersist` and `ignoreOnPersist` methods respectively.

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
  
  So on navigating to another page by clicking on the link, by default the filterSettings and groupSettings will be persisted. But upon clicking the button and navigating, the persist state of the Grid actions are modified.
   
## External Search in Grid

Using [`search`](https://help.syncfusion.com/api/js/ejgrid#methods:search “search”) method of Grid, you can search the string in Grid externally without using in-built toolbar search support. While using [`search`](https://help.syncfusion.com/api/js/ejgrid#methods:search “search”) method it is necessary to set [`allowSearching`](https://help.syncfusion.com/api/js/ejgrid#members:allowsearching “allowSearching”) property as `true`. The following code example explains the above behavior.

{% tabs %}
{% highlight html %}
<div class="content-container-fluid">
    <div class="row">
        <div id="sampleProperties">
            <div class="prop-grid">
                <div class="row">
                    <div class="col-md-3">
                        <input type="text" id="searchString" class="e-ejinputtext" />
                        <input type="button" id="search" value="Searching" />
                    </div>
                </div>
            </div>
        </div>
        <div class="cols-sample-area">
            <div id="Grid"></div>
        </div>
    </div>
</div>


{% endhighlight %}

{% highlight js %}
<script>
    $(function () {
        $("#Grid").ejGrid({
            dataSource: window.gridData,
            allowPaging: true,
            allowSearching: true,
            columns: [
            { field: "OrderID" },
            { field: "CustomerID" },
            { field: "EmployeeID" },
            { field: "Freight" },
            { field: "ShipCity" },
            { field: "ShipCountry" }
            ]
        });
        $("#search").ejButton({ click: "onSearching", size: "small" });
    });
    function onSearching(args) {
        var obj = $("#Grid").ejGrid("instance");
        var val = $("#searchString").val();
        obj.search(val);
    }
</script>


{% endhighlight %}

{% endtabs %}
The following output is displayed as a result of the above code example.
![](externalsearch_images/externalsearch_img1.png)

## Reset Model Collections

Grid provides different Methods such as [`clearSorting`](https://help.syncfusion.com/api/js/ejgrid#methods:clearsorting "clearSorting"), [`clearFiltering`](https://help.syncfusion.com/api/js/ejgrid#methods:clearfiltering "clearFiltering") for clearing the respective models [`filterSettings.filteredColumns`](https://help.syncfusion.com/api/js/ejgrid#members:filtersettings-filteredcolumns "filteredColumns") and [`sortSettings.sortedColumns`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings-sortedcolumns "sortedColumns"). To set all these models to default value, Grid provides a [`resetModelCollections`](https://help.syncfusion.com/api/js/ejgrid#methods:resetmodelcollections "resetModelCollections") method. 

`resetModelCollections` will clear the grouping, sorting and filtering and it will set the current page to first page. 

{% tabs %}
{% highlight html %}

	<label>Methods</label>
	<select id="Methods" class="e-ddl" data-bind="value: field">
		<option value="default-Page" selected="selected">default-Page</option>
		<option value="clearSorting">clearSorting</option>
		<option value="clear-Grouping">clear-Grouping</option>
		<option value="clearFiltering">clearFiltering</option>
		<option value="resetModelCollections">resetModelCollections</option>
	</select>
    <div id="Grid"></div>

{% endhighlight %}

{% highlight js %}
    <script type="text/javascript">
        $(function () {
			$("#Methods").ejDropDownList({
				watermarkText: "Select Methods",
				width: "100%",
				change: function(args){
					var gridObj = $("#Grid").ejGrid("instance");
					if(args.selectedText == "default-Page") {
					    gridObj.model.pageSettings.currentPage = 1;
					    gridObj.refreshContent();
					}
					else if(args.selectedText == "clearSorting") gridObj.clearSorting();
					else if(args.selectedText == "clear-Grouping") {
					    gridObj.model.groupSettings.groupedColumns = [];
					    gridObj.refreshContent();
					}
					else if(args.selectedText == "clearFiltering") gridObj.clearFiltering();
					else { 
					    gridObj.resetModelCollections();
					    gridObj.refreshContent();
					}
					//clearSorting and clearFiltering methods will refresh the content on its own actions
					//resetModelCollections method and other actions requires, refreshContent method to refresh the content
				}
			});

            $("#Grid").ejGrid({
                dataSource: window.gridData,
                allowPaging: true,
				pageSettings: { currentPage: 3, pageSize: 8 },
                allowSorting: true,
				sortSettings: { sortedColumns: [{field: "OrderID", direction: "ascending"}] },
				allowGrouping: true, 
				groupSettings: { groupedColumns: ["OrderID"] },
                allowFiltering: true,
                filterSettings: { filterType: "excel", 
					filteredColumns: [{ field: "ShipCity", operator: "startswith", value: "r", predicate: "and", matchCase: true }]  
				}, 
				columns: [
				   { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right },
				   { field: "EmployeeID", headerText: 'Employee ID', textAlign: ej.TextAlign.Right },
				   { field: "OrderDate", headerText: 'Order Date', format:"{0:dd/MM/yyyy}", textAlign: ej.TextAlign.Right },
				   { field: "CustomerID", headerText: 'Customer ID' },
				   { field: "Freight", headerText: 'Freight', format: "{0:C}", textAlign: ej.TextAlign.Right },
				   { field: "ShipCity", headerText: 'Ship City' }
                ]
            });
        });
    </script>


{% endhighlight %}

{% endtabs %}


The following output is displayed as a result of the above code example.
![](externalsearch_images/ResetModel.png)

## Hierarchy Grid with different foreignKeyField in parent and child table

The `queryString` property is used to filter the childGrid data based on value in parent Grid data. But when the field name provided in `queryString` does not exists in Child Grid, then `foreignKeyField` property is used to filter the childGrid data. If the foreign key column name differes for parent and child grid then use `foreingnKeyField` property of Grid.

The following code example explains the above behavior.

{% highlight html %}
<a href="http://www.syncfusion.com">Navigate to another Page</a>
<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {
            var dataparent =[{EmployeeID:1,FirstName:"Nancy",City:"Seattle",Country:"USA"},
                            {EmployeeID:2,FirstName:"Andrew",City:"Takoma",Country:"USA"},
                            {EmployeeID:3,FirstName:"Margret",City:"Krickland",Country:"USA"},
                            {EmployeeID:4,FirstName:"Janet",City:"Seattle",Country:"USA"}];
                            
            var datachild = [{OrderID:10248,CustomerName :"Nancy",CustomerID:"VINET",ShipCity:"Graz",ShipName:"Ernst Handel"},
                            {OrderID:10249,CustomerName :"Takoma",CustomerID:"ANATR",ShipCity:"Oulu",ShipName:"Wartian Herkku"},
                            {OrderID:10251,CustomerName :"Krickland",CustomerID:"HANAR",ShipCity:"Bergamo",ShipName:"QUICK-Stop"}];            
                            
            $("#Grid").ejGrid({
                dataSource: dataparent,
                allowSorting: true,
                columns: [
                         { field: "EmployeeID", headerText: 'Employee ID', textAlign: ej.TextAlign.Right, width: 75 },
                         { field: "FirstName", headerText: 'First Name', textAlign: ej.TextAlign.Left, width: 100 },
                         { field: "City", headerText: 'City', textAlign: ej.TextAlign.Left, width: 100 },
                         { field: "Country", headerText: 'Country', textAlign: ej.TextAlign.Left, width: 100 }
                ],
                childGrid: {
                    dataSource: datachild,
                    queryString: "FirstName",
                    foreignKeyField:"CustomerName",
                    allowPaging: true,
                    columns: [
                             { field: "OrderID", headerText: 'Order ID', textAlign: ej.TextAlign.Right, width: 75 },
                             { field: "ShipCity", headerText: 'Ship City', textAlign: ej.TextAlign.Left, width: 100 },
                             { field: "CustomerName", headerText: 'First Name', textAlign: ej.TextAlign.Left, width: 100 },
                             { field: "CustomerID", headerText: 'Freight', textAlign: ej.TextAlign.Left, width: 120 },
                             { field: "ShipName", headerText: 'Ship Name', textAlign: ej.TextAlign.Left, width: 100 }
                    ],
                    
                },
            });
        });
    </script>
  {% endhighlight %}   
  
The following output is displayed as a result of the above code example.
![](Hierarchy-Grid_images/Hierarchy-Grid_images2.png)