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

Using [`search`](https://help.syncfusion.com/api/js/ejgrid#methods:search “search”) method of Grid, you can search the string in Grid externally without using in-built toolbar search support. While using [`search`](https://help.syncfusion.com/api/js/ejgrid#methods:search “search”) method it is necessary to set [`allowSearching`](https://help.syncfusion.com/api/js/ejgrid#members:allowsearching “allowSearching”) property as `true`. To clear the searching by external action use  [`clearSearching`](https://help.syncfusion.com/api/js/ejgrid#methods:clearsearching “clearSearching”) method. The following code example explains the above behavior.

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
                        <input type="button" id="clear" value="Clear Searching" />
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
        $("#search").ejButton({ click: "onSearching" });
        $("#clear").ejButton({ click: "onClearing" });
    });
    function onSearching(args) {
        var obj = $("#Grid").ejGrid("instance");
        var val = $("#searchString").val();
        obj.search(val);
    }
    function onClearing(args){
        var obj = $("#Grid").ejGrid("instance");
        $("#searchString").val("");
        obj.clearSearching();
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

The `queryString` property is used to filter the childGrid data based on value in parent Grid data. But when the field name provided in `queryString` does not exists in Child Grid, then `foreignKeyField` property is used to filter the childGrid data. If the foreign key column name differs for parent and child grid then use `foreignKeyField` property of Grid.

The following code example explains the above behavior.

{% highlight html %}
<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {
            var Parent =[{EmployeeID:1,FirstName:"Nancy",City:"Seattle",Country:"USA"},
                            {EmployeeID:2,FirstName:"Andrew",City:"Tahoma",Country:"USA"},
                            {EmployeeID:3,FirstName:"Margret",City:"Seattle",Country:"USA"},
                            {EmployeeID:4,FirstName:"Janet",City:"Seattle",Country:"USA"}];
                            
            var Child = [{OrderID:10248,CustomerName :"Nancy",CustomerID:"VINET",ShipCity:"Graz",ShipName:"Ernst Handel"},
                            {OrderID:10249,CustomerName :"Tahoma",CustomerID:"ANATR",ShipCity:"Oulu",ShipName:"Wartier"},
                            {OrderID:10251,CustomerName :"Seattle",CustomerID:"HANAR",ShipCity:"Bergamo",ShipName:"QUICK-Stop"}];            
                            
            $("#Grid").ejGrid({
                dataSource: Parent,
                allowSorting: true,
                columns: [
                         { field: "EmployeeID", headerText: 'Employee ID', textAlign: ej.TextAlign.Right, width: 75 },
                         { field: "FirstName", headerText: 'First Name', textAlign: ej.TextAlign.Left, width: 100 },
                         { field: "City", headerText: 'City', textAlign: ej.TextAlign.Left, width: 100 },
                         { field: "Country", headerText: 'Country', textAlign: ej.TextAlign.Left, width: 100 }
                ],
                childGrid: {
                    dataSource: child,
                    queryString: "FirstName",
                    foreignKeyField:"CustomerName",
                    allowPaging: true,
                    columns: [
                             { field: "OrderID", headerText: 'Order ID', textAlign: ej.TextAlign.Right, width: 75 },
                             { field: "ShipCity", headerText: 'Ship City', textAlign: ej.TextAlign.Left, width: 100 },
                             { field: "CustomerName", headerText: 'First Name', textAlign: ej.TextAlign.Left, width: 100 },
                             { field: "CustomerID", headerText: 'Customer ID', textAlign: ej.TextAlign.Left, width: 120 },
                             { field: "ShipName", headerText: 'Ship Name', textAlign: ej.TextAlign.Left, width: 100 }
                    ],
                    
                },
            });
        });
    </script>
  {% endhighlight %}   
  
The following output is displayed as a result of the above code example.
![](Hierarchy-Grid_images/Hierarchy-Grid_images2.png)

## Display other Syncfusion controls in Grid columns

We can display the other Syncfusion controls using [`template`](https://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") property of Grid columns and [`templateRefresh`](https://help.syncfusion.com/api/js/ejgrid#events:templaterefresh "templateRefresh") event of ejGrid control.

{% tabs %}
{% highlight html %}

<div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <script type="text/x-jsrender" id="columnTemplate">

                    {{"{{"}}if EmployeeID<3{{}}}}

                    <input type="text" class="rating" value="3" />

                    {{"{{"}}else EmployeeID>2 && EmployeeID<5{{}}}}

                    <input type="text" class="rating" value="3" />

                    {{"{{"}}else EmployeeID>4{{}}}}

                    <input type="text" class="rating" value="5" />

                    {{"{{"}}/if{{}}}}
                </script>
                <div id="Grid"></div>
            </div>
        </div>
    </div>
    
{% endhighlight %}

{% highlight js %}

<script>
    $(function () {
        $("#Grid").ejGrid({
            // the datasource "window.employeeView" is referred from jsondata.min.js
            dataSource: window.employeeView,
            allowPaging: true,
            columns: [
                { headerText: "Employee Rating", template: "#columnTemplate", width: 150 },
                { field: "EmployeeID", headerText: "Employee ID", width: 90 },
                { field: "FirstName", headerText: "First Name", width: 90 },
                { field: "LastName", headerText: "Last Name", width: 90 },
                { field: "Country", headerText: "Country", width: 80 }
            ],
            templateRefresh: "template",
        });
    });
    function template(args) {
        $(args.cell).find(".rating").ejRating({ allowReset: false });
    }
</script>

{% endhighlight %}

{% endtabs %}
The following output is displayed as a result of the above code example.
![](Display_Other_controls_images/Display_Other_controls_img1.png)

## Perform Grid Actions on External button click

### CRUD operations

Using [`addRecord`](https://help.syncfusion.com/api/js/ejgrid#methods:addRecord “addRecord”) method of Grid, you can add a record to a Grid externally without using in-built toolbar add support. While using [`addRecord`](https://help.syncfusion.com/api/js/ejgrid#methods:addRecord “addRecord”) method it is necessary to set [`allowAdding`](https://help.syncfusion.com/api/js/ejgrid#members:allowAdding “allowAdding”) property as `true`.
Using [`deleteRecord`](https://help.syncfusion.com/api/js/ejgrid#methods:deleteRecord “deleteRecord”) method of Grid, you can delete a record to a Grid externally without using in-built toolbar delete support. While using [`deleteRecord`](https://help.syncfusion.com/api/js/ejgrid#methods:deleteRecord “deleteRecord”) method it is necessary to set [`allowDeleting`](https://help.syncfusion.com/api/js/ejgrid#members:allowDeleting “allowDeleting”) property as `true`.
Using [`updateRecord`](https://help.syncfusion.com/api/js/ejgrid#methods:updateRecord “updateRecord”) method of Grid, you can update a record to a Grid externally without using in-built toolbar update support. While using [`updateRecord`](https://help.syncfusion.com/api/js/ejgrid#methods:updateRecord “updateRecord”) method it is necessary to set [`allowEditing`](https://help.syncfusion.com/api/js/ejgrid#members:allowEditing “allowEditing”) property as `true`.

### Filtering

Using [`filterColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:filterColumn “filterColumn”) method of Grid, you can filter the data in the Grid externally without using in-built filter support. While using [`filterColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:filterColumn “filterColumn”) method it is necessary to set [`allowFiltering`](https://help.syncfusion.com/api/js/ejgrid#members:allowFiltering “allowFiltering”) property as `true`.

### Grouping

Using [`groupColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:groupColumn “groupColumn”) and [`ungroupColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:ungroupColumn “ungroupColumn”) method of Grid, you can group/ungroup the Grid externally without using in-built grouping support. While using [`groupColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:groupcolumn “groupColumn”) and [`ungroupColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:ungroupcolumn “ungroupColumn”) method it is necessary to set [`allowGrouping`](https://help.syncfusion.com/api/js/ejgrid#members:allowgrouping “allowGrouping”) property as `true`.

### Sorting

Using [`sortColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:sortcolumn “sortColumn”) method of Grid, you can sort the Grid externally without using in-built sorting support. While using [`sortColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:sortcolumn “sortColumn”) method it is necessary to set [`allowSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowsorting “allowSorting”) property as `true`.

The following code example explains the above behavior.

{% tabs %}
{% highlight html %}
<table>
    <tr>
        <td><b>CRUD</b><br><button id="AddRecord">Add record</button><br><button id="UpdateRecord">Update record</button><br><button id="DeleteRecord">DeleteRecord</button></td>
        <td><b>Filtering</b><br><br><input type="text" id="filterOne" /><input type="text" id="filterTwo" /><button id="filter">Filter</button> <button id="ClearFilter">Clear Filter</button></td>
        <div id="Order"><ul><li>10248</li><li>10249</li><li>10250</li><li>10251</li><li>10252</li></ul></div>
        <div id="Employee"><ul><li>1</li><li>2</li><li>3</li><li>4</li><li>5</li></ul></div>
        <td><b>Grouping</b><br><br>
            <select id="columnName" class="e-ddl" data-bind="value: field">
                <option value="OrderID" selected="selected">Order ID</option>
                <option value="CustomerID">Customer ID</option>
                <option value="Freight">Freight</option>
                <option value="ShipName">Ship Name</option>
                <option value="Verified">Verified</option>
            </select><br>
            <button id="groupColumn">GroupColumn</button>
            <button id="unGroupColumn">UnGroupColumn</button>
        </td>
        <td><b>Sorting</b><br><br>
            <select id="sortColumnName" class="e-ddl" style="width: 100px" data-bind="value: field">
                <option value="OrderID" selected="selected">Order ID</option>
                <option value="CustomerID">Customer ID</option>
                <option value="EmployeeID">Employee ID</option>
                <option value="Freight">Freight</option>
                <option value="OrderDate">Order Date</option>
            </select>
            <select id="directions" class="e-ddl" style="width: 100px" data-bind="value: field">
                <option value="ascending" selected="selected">Ascending</option>
                <option value="descending">Descending</option>
            </select>
            <button id="doSorting" style="width: 100px">Sort</button>
            <button id="clearSort" style="width: 100px">Clear</button>
        </td>
    </tr>
</table>
<div id="Grid"></div>

{% endhighlight %}

{% highlight js %}
<script type="text/javascript">
    $("#Grid").ejGrid({
        dataSource : window.gridData,
        allowPaging : true,
        isResponsive:true,
        allowSearching:true,
        allowFiltering:true,
        allowGrouping:true, 
        allowReordering:true,
        allowSorting:true,
        editSettings : {
            allowEditing : true,
            allowAdding : true,
            allowDeleting : true,
            editMode : "normal"
        },
        toolbarSettings : {
            showToolbar : true,
            toolbarItems : ["add", "edit", "delete", "update", "cancel"]
        },
        columns : [{ field: "OrderID", headerText: "Order ID",isPrimaryKey:true, width: 70 },
                   { field: "CustomerID", headerText: "Customer ID", width: 70 },
                   { field: "EmployeeID", headerText: "Employee ID", width: 70},
                   { field: "Freight", headerText: "Freight", width: 70},
                   { field: "OrderDate", headerText: "Order Date", width: 70}]
    });
    $('#filterOne').ejDropDownList({ targetID: "Order", watermarkText:"Select Filter value one", width: "230"});
    $('#filterTwo').ejDropDownList({ targetID: "Employee", watermarkText:"Select Filter value two", width: "230"});
    $("#columnName").ejDropDownList({ width: "115", selectedItemIndex: 0, change: "Grouping" });
    $("#groupColumn").ejButton({ size: "medium", click: "clickGroup", width: "100px" });
    $("#filter").ejButton({ size: "medium", click: "Filter", width: "100px" });
    $("#unGroupColumn").ejButton({ size: "medium", click: "clickGroup", width: "115px" });
    $("#AddRecord").ejButton({ size: "medium", click: "addRecord", width: "100px" });
    $("#DeleteRecord").ejButton({ size: "medium", click: "deleteRecord", width: "100px" });
    $("#UpdateRecord").ejButton({ size: "medium", click: "updateRecord", width: "100px" });
    $("#ClearFilter").ejButton({ size: "medium", click: "clearFilter", width: "100px" });
    $("#unGroupColumn").ejButton("disable");
    $("#sortColumnName").ejDropDownList({ width: "120" });
    $("#directions").ejDropDownList({ width: "120" });
    $("#sortColumnName").ejDropDownList("option",{"selectedItemIndex":1});
    $("#directions").ejDropDownList("option", { "selectedItemIndex": 0 });
    $("#doSorting,#clearSort").ejButton({ "click": "Sort", width: "100" });
    function addRecord(){
        var gridObj = $('#Grid').data("ejGrid");
        gridObj.addRecord({ "OrderID": 12333 });
    }
    function deleteRecord(){
        var gridObj = $('#Grid').data("ejGrid");
        gridObj.deleteRecord("OrderID", { OrderID: gridObj.model.dataSource[gridObj.model.selectedRowIndex].OrderID }); 
    }
    function updateRecord(){
        var gridObj = $('#Grid').data("ejGrid");
        gridObj.updateRecord("OrderID", { OrderID: 10249, EmployeeID: 3 }); 
    }
    var group = true;
    function Filter(args) {
        var gridObj = $("#Grid").data("ejGrid");
        var one = $('#filterOne').data("ejDropDownList");
        var two = $('#filterTwo').data("ejDropDownList");
        var One = one.getValue();
        var Two = two.getValue();
        gridObj.filterColumn([{field:"OrderID",operator:"equal",value:One,predicate:"and", matchcase:true},{field:"EmployeeID",operator:"equal",value:Two,predicate:"and", matchcase:true}]);
    }
    function clearFilter(args) {
        var gridObj = $("#Grid").data("ejGrid");
        gridObj.clearFiltering();
    }
    function Sort(args) {
        var gridObj = $("#Grid").data("ejGrid");
        var columnName = $("#sortColumnName").data("ejDropDownList")._selectedValue;
        var sortDirection = $("#directions").data("ejDropDownList")._selectedValue;
        if (this.element.attr("id") == "doSorting") {
            gridObj.sortColumn(columnName, sortDirection);
        }
        else {
            gridObj.clearSorting();
        }
    }
    function Grouping() {
        var gridObj = $("#Grid").data("ejGrid");
        var columnName = $("#columnName").ejDropDownList("getSelectedValue");
        if ($.inArray(columnName, gridObj.model.groupSettings.groupedColumns) != -1) {
            $("#unGroupColumn").ejButton("enable");
            $("#groupColumn").ejButton("disable");
        }
        else {
            $("#groupColumn").ejButton("enable");
            $("#unGroupColumn").ejButton("disable");
        }
    }
    function clickGroup(args) {
        var gridObj = $("#Grid").data("ejGrid");
        var columnName = $("#columnName").ejDropDownList("getSelectedValue");
        if (this.element.attr("id") == "groupColumn") {
            gridObj.groupColumn(columnName);
            if (group) {
                $("#groupColumn").ejButton("disable");
                $("#unGroupColumn").ejButton("enable");
            }
        }
        else {
            gridObj.ungroupColumn(columnName);
            group = true;
            $("#unGroupColumn").ejButton("disable");
            $("#groupColumn").ejButton("enable");
        }
    }
</script>

{% endhighlight %}

{% endtabs %}
The following output is displayed as a result of the above code example.
![](externalsearch_images/Actionswithexternalbutton_img1.png)


## Getting Datasource of Grid in Sorted Order

Grid column can be sorted and after sorting, the datasource can be obtained in the same order using `sortBy` query and `executeLocal` method of DataManager.

The following code example describes the above behavior.

{% tabs %}
{% highlight html %}
<div class="content-container-fluid">
    <div class="row">
        <div id="sampleProperties">
            <div class="prop-grid">
                <div class="row">
                    <div class="col-md-3">
                        <input type="button" id="Sort" value="Get Sorted Data" />
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
            allowSorting: true,
            columns: [
            { field: "OrderID" },
            { field: "CustomerID" },
            { field: "EmployeeID" },
            { field: "Freight" },
            { field: "ShipCity" },
            { field: "ShipCountry" }
            ]
        });
        $("#sort").ejButton({ click: "GetSortedData" });
    });
    function GetSortedData(args) {
            var obj = $("#Grid").ejGrid("instance");   
            var Sort = obj.model.sortSettings.sortedColumns;  
            var query = ej.Query();               
            if(obj.model.sortSettings.sortedColumns.length){
                for(var i=Sort.length-1;i>=0;i--){        
                  query.sortBy(Sort[i].field, Sort[i].direction); 
                }
            var SortedDatasource = ej.DataManager(obj.model.dataSource).executeLocal(query); 
    }
}
</script>

{% endhighlight %}

{% endtabs %}

N> This solution is applicable only for local data.

