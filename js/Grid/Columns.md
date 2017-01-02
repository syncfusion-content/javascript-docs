---
layout: post
title: Columns with Grid widget for Syncfusion Essential JS
description: How to define the columns and its features
platform: js
control: Grid
documentation: ug
--- 
# Columns

Column definitions are used as the [`dataSource`](http://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") schema in Grid and it plays vital role in rendering column values in required format. Grid operations such as sorting, filtering, editing would be performed based on the column definitions. The [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") property of the [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") is necessary to map the datasource values in Grid columns.

N> 1. If the column with [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") is not in the datasource, then the column values will be displayed as empty.
N> 2. If the [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name contains "dot" operator then it is considered as complex binding.

## Auto generation

The [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") are automatically generated when [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") declaration is empty or undefined while initializing the Grid. Also, all the columns which are in [`dataSource`](http://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") are bound as a Grid columns.

The following code example shows auto-generate columns behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img1.png)


### How to set isPrimaryKey for auto generated columns when editing is enabled:

Using [`dataBound`](http://help.syncfusion.com/api/js/ejgrid#events:databound "dataBound") event, you can set [`isPrimaryKey`](http://help.syncfusion.com/api/js/ejgrid#members:columns-isprimarykey "isPrimaryKey") value as `true` by two ways. The following code example demonstrates the above behavior.

1. If primary key "column index" is known then refer the following code example
{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		editSettings : {
			allowEditing : true
		},
		dataBound : function (args) {
			var column = args.model.columns[0];
			//(or)
			var column = this.getColumnByIndex(0);
			column.isPrimaryKey = true;
			//Here columns method used to update the particular column
			this.columns(column, "update");
		}
	});
});
{% endhighlight %}

2. If primary key "column field name" is known then refer the following code example
{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		editSettings : { allowEditing : true },
		dataBound : function (args) {
			var column = this.getColumnByField("OrderID");
			column.isPrimaryKey = true;
			//Here columns method used to update the particular column
			this.columns(column, "update");
		}
	});
});
{% endhighlight %}

## Headers

### HeaderText

It represents the title for particular column. To enable header text, set [`headerText`](http://help.syncfusion.com/api/js/ejgrid#members:columns-headertext "headerText") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). The following code example describes the above behavior.

N> If [`headerText`](http://help.syncfusion.com/api/js/ejgrid#members:columns-headertext "headerText") is not defined then the [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name is considered as header text for that particular column. If both [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name and [`headerText`](http://help.syncfusion.com/api/js/ejgrid#members:columns-headertext "headerText") are not defined then the column is rendered with "empty" header text.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field : "OrderID", headerText : "Order ID" },
			{ field : "EmployeeID",	headerText : "Emp ID" }, 
			{ field : "Freight", headerText : "Freight" }, 
			{ field : "ShipCountry", headerText : "Country" }, 
			{ field : "ShipCity", headerText : "City" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img2.png)


### Header Text alignment

[Align](http://help.syncfusion.com/api/js/ejgrid#members:columns-headertextalign "Align") the header text of column header using [`headerTextAlign`](http://help.syncfusion.com/api/js/ejgrid#members:columns-headertextalign "headerTextAlign") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). There are four possible ways to align header text, they are

1. Right
2. Left
3. Center
4. Justify

N> For [`headerTextAlign`](http://help.syncfusion.com/api/js/ejgrid#members:columns-headertextalign "headerTextAlign") property you can assign either `string` value ("right") or `enum` value (`ej.TextAlign.Right`).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field : "OrderID", headerText : "Order ID" }, 
			{ field : "EmployeeID",	headerText : "Emp ID", headerTextAlign : "right" },
			{ field : "Freight", headerText : "Freight" },
			{ field : "ShipCountry", headerText : "Country", headerTextAlign : "center" },
			{ field : "ShipCity", headerText : "City", headerTextAlign : "right" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img3.png)


## Header Template

The template design that applies on for the column header. To render template, set [`headerTemplateID`](http://help.syncfusion.com/api/js/ejgrid#members:columns-headertemplateid "headerTemplateID") property of the [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns").


N> It's a standard way to enclose the [`template`](http://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") within the `script` tag with `type` as `text/x-jsrender`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="empTemplate" type="text/x-jsrender">
Emp ID
<span class="e-userlogin e-icon employee"></span>
</script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field : "OrderID", headerText : "Order ID" },
			{ field : "EmployeeID", headerTemplateID : "#empTemplate" },
			{ field: "Freight", headerText: "Freight" },
			{ field: "ShipCountry", headerText: "Country" },
			{ field: "ShipCity", headerText: "City" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img4.png)


## Text alignment

You can [align](http://help.syncfusion.com/api/js/ejgrid#members:columns-textalign "align") both content and header text of particular column using [`textAlign`](http://help.syncfusion.com/api/js/ejgrid#members:columns-textalign "textAlign") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). There are four possible ways to align content and header text of column, they are 

1. Right
2. Left
3. Center
4. Justify

N> 1. For [`textAlign`](http://help.syncfusion.com/api/js/ejgrid#members:columns-textalign "textAlign") property you can assign either `string` value ("right") or `enum` value (`ej.TextAlign.Right`).
N> 2. The [`textAlign`](http://help.syncfusion.com/api/js/ejgrid#members:columns-textalign "textAlign") property will affect both content and header text of the grid.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field : "OrderID", textAlign : "right" }, 
			{ field : "EmployeeID", textAlign : "right" },
			{ field : "Freight", textAlign : "right" },
			{ field : "ShipCountry", textAlign : "center" }, 
			{ field : "ShipCity", textAlign : "justify" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img5.png)


## Format

[Format](http://help.syncfusion.com/api/js/ejgrid#members:columns-format "Format") is the process of customizing the particular column data with specified jQuery recognized globalize formats, such as currency, numeric, decimal, percentage or dates. The globalize format can be specified by using [`format`](http://help.syncfusion.com/api/js/ejgrid#members:columns-format "format") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns").

The [`format`](http://help.syncfusion.com/api/js/ejgrid#members:columns-format "format") value should be wrapped within "{0:" and "}". (For ex: "{0:C3}"). The [data format](https://github.com/jquery/globalize/tree/v0.1.1#format "data format") strings are available for the Date and Number types.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field: "OrderID" },
			{ field: "EmployeeID" },
			{ field: "Freight", format: "{0:C2}" },
			{ field: "OrderDate", format: "{0:dd/MM/yyyy}" },
			{ field: "ShipCity" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img6.png)


## Width

You can specify the width for particular column by setting [`width`](http://help.syncfusion.com/api/js/ejgrid#members:columns-width "width") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") as in pixel (ex: 100) or in percentage (ex: 40%).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
		    { field: "OrderID", width: "10%" },
			{ field: "EmployeeID", width: "15%" },
			{ field: "Freight", width: 100 },
			{ field: "ShipCity", width: 150 },
			{ field: "ShipCountry", width: 100 }
		]
	});
});
{% endhighlight %}



The following output is displayed as a result of the above code example.

![](columns_images/columns_img7.png)


## Resize to fit 

The [`allowResizeToFit`](http://help.syncfusion.com/api/js/ejgrid#members:allowresizetofit "allowResizeToFit") property enable the Grid to set width to columns based on maximum width of the particular column's content to facilitate full visibility of data in all the grid rows. This automatic behavior is applicable only for the columns which does not have width specified. 

On columns where "width is defined", double click on the particular column header's resizer symbol to resize the column to show the whole text. For example, refer the "ShipCity" column in the below code snippet and output screen shot. 

The following code example describes the above behavior. 

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowResizeToFit : true,
		columns : [
			{ field: "OrderID", width: 100 },
			{ field: "EmployeeID" },
			{ field: "Freight", width: 75 },
			{ field: "ShipCity", width: 50 },
			{ field: "ShipAddress" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img8.png)


## Reorder

Reordering can be done by drag and drop the particular column header from one index to another index within the Grid. Reordering can be enabled by setting [`allowReordering`](http://help.syncfusion.com/api/js/ejgrid#members:allowreordering "allowReordering") property as `true`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowReordering : true,
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img10.png)


## Visibility

You can hide particular column in Grid view by setting [`visible`](http://help.syncfusion.com/api/js/ejgrid#members:columns-visible "visible") property of it as `false`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field: "EmployeeID"},
			{ field: "OrderID", visible: false },
			{ field: "Freight" },
			{ field: "ShipCity" },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img11.png)


## Unbound Column

You can define the unbound columns in Grid by not defining [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") property for that particular column. Value for these columns can be populated either manually using [`queryCellInfo`](http://help.syncfusion.com/api/js/ejgrid#events:querycellinfo "queryCellInfo") event or by using column [`template`](http://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") or by column [`format`](http://help.syncfusion.com/api/js/ejgrid#members:columns-format "format") property.

N> Editing, grouping, filtering, sorting, summary and searching support are not available for unbound columns.

The following code example describes the above behavior. 

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		editSettings : {
			allowDeleting : true
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "EmployeeID" },
			{ field: "Freight" },
			{ headerText: "",format: "<a onclick =\"clk(this)\" href=#>Delete</a>" }
		]
	});
});

function clk(e) {
	var obj = $("#Grid").data("ejGrid");
	obj.deleteRecord("OrderID", obj.getSelectedRecords()[0]);
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img13.png)


## Column Template

HTML templates can be specified in the [`template`](http://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") property of the particular column as a string (HTML element) or ID of the template's HTML element.

You can use JsRender syntax in the template. For more information about JsRender syntax, please refer [this link](http://www.jsviews.com/#jsrapi "this link"). 

N> If [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") is not specified, you will not able to perform editing, grouping, filtering, sorting, search and summary functionalities in particular column.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.employeeView" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.employeeView,
		allowPaging : true,
		pageSettings : {
			pageSize : 4
		},
		columns : [
			{ headerText: "Photo", template: "<img style="width: 75px; height: 70px" src="/13.2.0.29/themes/web/images/employees/{{"{{"}}:EmployeeID{{}}}}.png" alt="{{"{{"}}:EmployeeID{{}}}}" />" },						
			{ field: "EmployeeID" },
			{ field: "FirstName" },
			{ field: "LastName" },
			{ field: "Country" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img14.png)


## Controlling Grid actions

You can control the Grid actions of a particular column by setting [`allowSorting`](http://help.syncfusion.com/api/js/ejgrid#members:allowsorting "allowSorting"), [`allowGrouping`](http://help.syncfusion.com/api/js/ejgrid#members:allowgrouping "allowGrouping"), `allowFiltering`, [`allowResizing`](http://help.syncfusion.com/api/js/ejgrid#members:allowresizing "allowResizing") and [`allowEditing`](http://help.syncfusion.com/api/js/ejgrid#members:editsettings-allowediting "allowEditing") properties.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		columns : [
			{ field: "OrderID", isPrimaryKey:true },
			{ field: "EmployeeID", allowEditing: false, allowResizing: false, allowSorting: false, allowGrouping: false, allowFiltering: false },
			{ field: "Freight" },
			{ field: "ShipCity" },
			{ field: "ShipCountry" }
		],
		allowPaging : true,
		allowFiltering : true,
		allowGrouping : true,
		allowSorting : true,
		allowResizing : true,
		editSettings : { allowEditing : true },
	});
});
{% endhighlight %}

## Read only

To make a column as "read-only" then set [`allowEditing`](http://help.syncfusion.com/api/js/ejgrid#members:editsettings-allowediting "allowEditing") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") as `false`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		editSettings : {
			allowEditing : true
		},
		columns : [
			{ field: "OrderID", isPrimaryKey:true },
			{ field: "EmployeeID", allowEditing: false },
			{ field: "Freight" },
			{ field: "ShipCity" },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img15.png)


## Expression Column

[Expression](http://help.syncfusion.com/api/js/ejgrid#members:columns-template "Expression") column is possible only for [`template`](http://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") column.

You can use JsRender syntax in the template.For more information about JsRender syntax, please refer [the link](http://www.jsviews.com/#jsrapi "the link"). 

N> This expression column is supported at read only mode.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.FoodInformation" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.FoodInformation,
		allowPaging : true,
		columns : [
			{ field: "FoodName" },
			{ field: "Protein" },
			{ field: "Fat" },
			{ field: "Carbohydrate" },
			{ headerText: "Calories In Take", template: "<span>{{"{{"}}:Protein * 4  + Fat * 4 + Carbohydrate * 9 {{"}}"}}</span>" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img16.png)


## Command Column

### Default action buttons

Using [`command`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands "command") column, you can add CRUD action buttons as one of the Grid column, through [`type`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "type") property of [`commands`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands "commands"). The type property supports the below default [`UnboundType`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "UnboundType") buttons.

1. edit
2. save
3. delete
4. cancel

Through [`buttonOptions`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands-buttonoptions "buttonOptions") property of [`commands`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands "commands"), you can specify all the button options which are supported by Essential Studio JavaScript [`Button`](http://help.syncfusion.com/api/js/ejbutton# "Button") control. 

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "EmployeeID" },
			{ field: "Freight", editType: "numericedit"},
			{ field: "ShipCountry" },
			{
				headerText : "Manage Records",
				commands : [
					{ type : "edit", buttonOptions : { text : "Edit" } },
					{ type : "delete", buttonOptions : { text : "Delete" } },
					{ type : "save", buttonOptions : { text : "Save" } }, 
					{ type : "cancel", buttonOptions : { text : "Cancel" } }
				],
				width : 150
			}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img17.png)


### Custom buttons

You can add custom button in the command column by specifying the [`type`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "type") property of [`commands`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands "commands") as "empty" or any other `string` which does not corresponds to default [`UnboundType`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "UnboundType") buttons.

N> 1. For [`type`](http://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "type") property you can assign either `string` value ("edit") or `enum` value (`ej.Grid.UnboundType.Edit`).
N> 2. In command column you can add only buttons.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.employeeView,
		columns : [
			{ field : "EmployeeID" }, 
			{
				headerText : "Employee Details",
				commands : [
					{ type: "details", buttonOptions: { text: "Details", width: "100", click: "onClick" } }
				],				
				textAlign : ej.TextAlign.Center,
				width : 150
			}
		]
	});
});

function onClick(args) {
	var grid = $("#Grid").ejGrid("instance");
	var index = this.element.closest("tr").index();
	var record = grid.getCurrentViewData()[index];
	alert("Record Details: " + JSON.stringify(record));
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img18.png)


## Column Chooser

Column chooser contains the list of all the columns which are defined in the [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") property. Using this you can control the visibility of columns in Grid. You can prevent to show the particular column name in column chooser by setting [`showInColumnChooser`](http://help.syncfusion.com/api/js/ejgrid#members:showcolumnchooser "showInColumnChooser") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") as `false`. 



Column Chooser would be shown in the top right corner of Grid. To enable column chooser, set [`showColumnChooser`](http://help.syncfusion.com/api/js/ejgrid#members:showcolumnchooser "showColumnChooser") property as `true`. 

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		showColumnChooser : true,
		columns : [
			{ field: "OrderID" },
			{ field: "EmployeeID", showInColumnChooser: false },
			{ field: "Freight" },
			{ field: "ShipCity" },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img19.png)


## Foreign Key Column

Lookup data source can be bound to [`dataSource`](http://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). Data [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") and `text` can be set using [`foreignKeyField`](http://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField") and [`foreignKeyValue`](http://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyvalue "foreignKeyValue") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns").

In the [`dataSource`](http://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property, we can bound local and remote data.

I> For foreign key column the sorting and grouping is based on [`foreignKeyField`](http://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField") instead of [`foreignKeyValue`](http://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyvalue "foreignKeyValue").

N> In remote data, server should be configured to perform select and filter operations since the Grid will try to fetch required columns using select operation and required data using filter operation.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" and "window.employeeView" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "EmployeeID", foreignKeyField: "EmployeeID", foreignKeyValue: "FirstName", dataSource: window.employeeView, headerText: "First Name" },
			         //(or)
			{ field: "EmployeeID", foreignKeyField: "EmployeeID", foreignKeyValue: "FirstName", dataSource: ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Employees/" }), headerText: "First Name" },
			{ field: "CustomerID" },
			{ field: "Freight" },
			{ field: "ShipCity" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img20.png)


## Customize column

You can [customize](http://help.syncfusion.com/api/js/ejgrid#members:columns-cssclass "customize") the header and content of the particular column by [`cssClass`](http://help.syncfusion.com/api/js/ejgrid#members:columns-cssclass "cssClass") property of the column.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight css %}
.customcss.e-headercell {
	background-color: #2382c3;
	color: white;
	font-family: 'Bell MT';
	font-size: 20px;
}

.customcss.e-rowcell {
	background-color: #ecedee;
	font-family: 'Bell MT';
	color: red;
	font-size: 20px;
}
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field: "OrderID" },
			{ field: "CustomerID" },
			{ field: "EmployeeID", cssClass: "customcss" },
			{ field: "Freight" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img23.png)


## Type

Used to define the type of the particular column data. If the [`type`](http://help.syncfusion.com/api/js/ejgrid#members:columns-type "type") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") is not specified then its type is automatically defined based on the first row data of that column.

N> The [`type`](http://help.syncfusion.com/api/js/ejgrid#members:columns-type "type") is needed for filtering feature when first row of the data is "null" or "empty".

The available column data type is tabulated as follows.

<table>
<tr>
<th>
Type</th><th>
Description</th>
</tr>
<tr>
<td>
string</td><td>
Gets or sets the type of the column value as string </td>
</tr>
<tr>
<td>
number</td><td>
Gets or sets the type of the column value as number</td>
</tr>
<tr>
<td>
date</td><td>
Gets or sets the type of the column value as date</td>
</tr>
<tr>
<td>
datetime</td><td>
Gets or sets the type of the column value as datetime</td>
</tr>
<tr>
<td>
boolean</td><td>
Gets or sets the type of the column value as true or false </td>
</tr>
<tr>
<td>
guid</td><td>
Gets or sets the type of the column value as guid</td>
</tr>
<tr>
<td>
checkbox </td><td>
Gets or sets the type of the column value as checkbox for row selection </td>
</tr>
</table>

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field: "OrderID" },
			{ field: "CustomerID", type: "string" },
			{ field: "EmployeeID", type:"number" },
			{ field: "Freight" },
			{ field: "ShipCountry"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](columns_images/columns_img24.png)


