---
layout: post
title: Row with Grid widget for Syncfusion Essential JS
description: How to use and customize the grid row
platform: js
control: Grid
documentation: ug
--- 
# Row

It represents the record details that are fetched from the datasource.

## Row Hover

You can see the mouse hovering effect on the corresponding grid rows using [`enableRowHover`](http://help.syncfusion.com/js/api/ejgrid#members:enablerowhover "enableRowHover") property. By default its value is `true`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		enableRowHover : true,
		allowPaging : true,
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Row_images/Row_img1.png)


## Details Template

It provides a detailed view /additional information about each row of the grid. You can render any type of JsRender template and assign the script template id in the [`detailsTemplate`](http://help.syncfusion.com/js/api/ejgrid#members:detailstemplate "detailsTemplate") property. And also you can change HTML elements in detail template row into JavaScript controls using [`detailsDataBound`](http://help.syncfusion.com/js/api/ejgrid#events:detailsdatabound "detailsDataBound") event.

On enabling details template, new column will be added in grid with an expander button in it and that can be expanded or collapsed to show or hide the underlying details row respectively.

N> It's a standard way to enclose the template within the `script` tag with `type` as "text/x-jsrender".

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="tabGridContents" type="text/x-jsrender">
   <div class="tabcontrol" id="Test">
   <ul>
   <li><a href="#gridTab{{"{{"}}:EmployeeID{{}}}}">Stock Grid</a></li>
   </ul>
   <div id="gridTab{{:EmployeeID}}">
   <div id="detailGrid">
   </div>
   </div>
   </div>
</script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.employeeView" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.employeeView,
		detailsTemplate : "#tabGridContents",
		detailsDataBound : "detailGridData",
		columns : ["EmployeeID", "FirstName", "Title", "City", "Country"]
	});
});

function detailGridData(e) {
	// Here you can get the parent details from "data". EmployeeID is the unique column value in parent row.
	var filteredData = e.data["EmployeeID"];
	// the datasource "window.ordersView" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	var data = ej.DataManager(window.ordersView).executeLocal(ej.Query().where("EmployeeID", "equal", parseInt(filteredData), true).take(5)); // form the query to filter the detail row data by using EmplooyeeID column value.
	//detailsElement contains all the elements which are mentioned in the template.
	// Here the detailGrid element is changed as ejGrid control
	e.detailsElement.find("#detailGrid").ejGrid({
		dataSource : data,		
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
	// Here the element which has tabcontrol class is changed as ejTab control
	e.detailsElement.find(".tabcontrol").ejTab();
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Row_images/Row_img2.png)


## Row Template

Row template enables you to set the customized look and behavior to grid all rows. [`rowTemplate`](http://help.syncfusion.com/js/api/ejgrid#members:rowtemplate "rowTemplate") property can be used bind the `id` of HTML template.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="templateData" type="text/x-jsrender">
   <tr>
   <td class="photo">
   <img style="width: 130px; height: 160px" src="/13.2.0.29/themes/web/images/employees/{{"{{"}}:EmployeeID{{}}}}.png" alt="{{"{{"}}:EmployeeID{{}}}}" />
   </td>
   <td class="details">
   <table class="CardTable" cellpadding="3" cellspacing="2">
   <colgroup>
   <col width="50%">
   <col width="50%">
   </colgroup>
   <tbody>
   <tr>
   <td class="CardHeader">First Name </td>
   <td>{{:FirstName}}</td>
   </tr>
   <tr>
   <td class="CardHeader">Last Name</td>
   <td>{{:LastName}}</td>
   </tr>
   <tr>
   <td class="CardHeader">Title
   </td>
   <td>{{:Title}}</td>
   </tr>
   </tbody>
   </table>
   </td>
   </tr>
</script>
{% endhighlight %}

{% highlight css %}
.photo img {
	width: 130px;
}
.photo, .details {
	border-color: #c4c4c4;
	border-style: solid;
}
.photo {
	border-width: 1px 0px 0px 0px;
}
.details {
	border-width: 1px 0px 0px 1px;
}
.details > table {
	width: 100%;
}
.CardHeader {
	font-weight: bolder;
}
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.employeeView" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : ej.DataManager(window.employeeView).executeLocal(ej.Query().take(2)),
		rowTemplate : "#templateData", // row template
		columns : [
			{ headerText: "Photo", width: 30 },
			{ headerText: 'Employee Details', width: 70 }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Row_images/Row_img3.png)


## Alternate row styling

Alternate row styling enhances the readability of grid rows by setting different background color for every alternate row. You can enable the alternative row styling in grid by using [`enableAltRow`](http://help.syncfusion.com/js/api/ejgrid#members:enablealtrow "enableAltRow") property. 

By default its value is `true`, so the following code example describes the how to turn off alternate row behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		enableAltRow : false,
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Row_images/Row_img4.png)


## Drag-and-Drop

Grid rows can be reordered, dropped to another Grid or custom control by enabling [`allowRowDragAndDrop`](http://help.syncfusion.com/js/api/ejgrid#members:allowRowDragAndDrop "allowRowDragAndDrop") Grid property.

N> To enable selection of multiple rows by mouse dragging on Grid rows, [`selectionType`](http://help.syncfusion.com/js/api/ejgrid#members:selectiontype "selectionType") property of Grid must be set to `multiple`.

### Reorder

By simply enabling the property [`allowRowDragAndDrop`](http://help.syncfusion.com/js/api/ejgrid#members:allowRowDragAndDrop "allowRowDragAndDrop"), Grid rows can be reordered within the same Grid.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
                $("#Grid").ejGrid({
                    // the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js' 
                    dataSource: window.gridData,
                    allowPaging: true,
                    allowRowDragAndDrop: true,
                    selectionType: "multiple",
                    columns: [
                                  { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
                                  { field: "CustomerID", headerText: "Customer ID", width: 90 },
                                  { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                                  { field: "ShipCountry", headerText: "Ship Country", width: 110 }
                    ],
                });           
 });

{% endhighlight %}

The following output is displayed before reordering rows. 

![](Row_images/Row_img5.png)

The following output is displayed after reordering rows.

![](Row_images/Row_img6.png)

### Grid-to-Grid

To drag and drop rows between two Grid, enable the Grid property [`allowRowDragAndDrop`](http://help.syncfusion.com/js/api/ejgrid#members:allowRowDragAndDrop "allowRowDragAndDrop") and specify the target Grid ID in [`dropTargetID`](http://help.syncfusion.com/js/api/ejgrid#members:rowDropSettings-dropTargetID "dropTargetID") property of Grid [`rowDropSettings`](http://help.syncfusion.com/js/api/ejgrid#members:rowDropSettings "rowDropSettings").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid" style="float:left;width:49%"></div>
<div id="DestGrid" style="float:right;width:49%"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
                $("#Grid").ejGrid({
                    / the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js' 
                    dataSource: window.gridData,
                    allowPaging: true,
                    allowRowDragAndDrop: true,
                    selectionType: "multiple",
                    rowDropSettings: { dropTargetID: "#DestGrid" },
                    columns: [
                                  { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
                                  { field: "CustomerID", headerText: "Customer ID", width: 90 },
                                  { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                                  { field: "ShipCountry", headerText: "Ship Country", width: 110 }
                    ],
                });
                $("#DestGrid").ejGrid({
                    dataSource: [],
                    allowPaging: true,
                    allowRowDragAndDrop: true,
                    rowDropSettings: { dropTargetID: "#Grid" },
                    selectionType: "multiple",
                    columns: [
                                  { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
                                  { field: "CustomerID", headerText: "Customer ID", width: 90 },
                                  { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                                  { field: "ShipCountry", headerText: "Ship Country", width: 110 }
                    ],
                });
});

{% endhighlight %}

The following output is displayed before dropping Grid rows.

![](Row_images/Row_img7.png)

The following output is displayed after dropping Grid rows.

![](Row_images/Row_img8.png)

### Grid-to-Custom control

You can also drag and drop grid rows to any custom control. For instance, let it be a form.

Enable the Grid property [`allowRowDragAndDrop`](http://help.syncfusion.com/js/api/ejgrid#members:allowRowDragAndDrop "allowRowDragAndDrop") and specify the target form element ID in [`dropTargetID`](http://help.syncfusion.com/js/api/ejgrid#members:rowDropSettings-dropTargetID "dropTargetID") property of Grid [`rowDropSettings`](http://help.syncfusion.com/js/api/ejgrid#members:rowDropSettings "rowDropSettings").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid" style="float:left;width:60%"></div>
<div style="float:right;width:38%">
<form role="form" id="dropForm" style="width:98%">
                        <fieldset style="text-align:center; font-weight:700"><legend>Record Details</legend></fieldset>
                        <div class="form-group row">
                            <label for="OrderID">Order ID:</label>
                            <input class="form-control" name="OrderID">
                        </div>
                        <div class="form-group row">
                            <label for="CustomerID">Customer ID:</label>
                            <input name="CustomerID" class="form-control">
                        </div>
                        <div class="form-group row">
                            <label for="EmployeeID">Employee ID:</label>
                            <input name="EmployeeID" class="form-control">
                        </div>
                        <div class="form-group row">
                            <label for="Freight">Freight:</label>
                            <input name="Freight" class="form-control">
                        </div>
                        <div class="form-group row">
                            <label for="ShipCity">Ship City:</label>
                            <input name="ShipCity" class="form-control">
                        </div>
                        <br />
                    </form>
                </div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'            
                dataSource: ej.DataManager(window.gridData),
                allowPaging: true,
                allowRowDragAndDrop: true,
                rowDropSettings: { dropTargetID: "#dropForm" },
                rowDrop: "rowDropHandler",				
                columns: [
                              { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
                              { field: "CustomerID", headerText: "Customer ID", width: 120 },
                              { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 120 },
                              { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                              { field: "ShipCity", headerText: "Ship City", width: 140 }
                ],
            });
});
        function rowDropHandler(args) {
            for (var key in args.data[0]) {
                $('#dropForm input[name=' + key + ']').val(args.data[0][key]);
            }
        }
{% endhighlight %}

The following output is displayed before dropping the rows on Form.

![](Row_images/Row_img9.png)

The following output is displayed after dropping the rows on Form.

![](Row_images/Row_img10.png)