---
layout: post
title: Columns with Grid widget for Syncfusion Essential JS
description: Learn about How to define the columns and its features in Syncfusion JavaScript Grid control and more details.
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Columns in JavaScript Grid

Column definitions are used as the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") schema in Grid and it plays a vital role in rendering column values in the required format. Grid operations such as sorting, filtering, editing would be performed based on the column definitions. The [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") property of the [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") is necessary to map the datasource values in Grid columns.

N> 1. If the column with [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") is not in the datasource, then the column values will be displayed as empty.

N> 2. If the [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name contains "dot" operator then it is considered as complex binding.

## Auto generation

The [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") are automatically generated when the [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") declaration is empty or undefined while initializing the Grid. Also, all the columns which are in [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") are bound as a Grid columns.

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

![Auto-generate columns in Javascript grid](columns_images/columns_img1.png)


### How to set isPrimaryKey for auto generated columns when editing is enabled:

Using the [`dataBound`](https://help.syncfusion.com/api/js/ejgrid#events:databound "dataBound") event, you can set you can set [`isPrimaryKey`](https://help.syncfusion.com/api/js/ejgrid#members:columns-isprimarykey "isPrimaryKey") value as true by two ways. Here we have used [`columns`](https://help.syncfusion.com/api/js/ejgrid#methods:columns "columns")  method for updating the particular column. The following code example demonstrates the above behavior.

1. If primary key "column index" is known then refer to the following code example

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

2. If primary key "column field name" is known then refer to the following code example

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

It represents the title for particular column. To enable header text, set [`headerText`](https://help.syncfusion.com/api/js/ejgrid#members:columns-headertext "headerText") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). The following code example describes the above behavior.

Use [`enableHeaderHover`](https://help.syncfusion.com/api/js/ejgrid#members:enableheaderhover "enableHeaderHover"), to enable mouse over effect on the corresponding column header cell of the grid.

N> If [`headerText`](https://help.syncfusion.com/api/js/ejgrid#members:columns-headertext "headerText") is not defined then the [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name is considered as header text for that particular column. If both [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name and [`headerText`](https://help.syncfusion.com/api/js/ejgrid#members:columns-headertext "headerText") are not defined then the column is rendered with "empty" header text.

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

![Header text of columns in Javascript grid](columns_images/columns_img2.png)


### Header Text alignment

[Align](https://help.syncfusion.com/api/js/ejgrid#members:columns-headertextalign "Align") the header text of a column header using the [`headerTextAlign`](https://help.syncfusion.com/api/js/ejgrid#members:columns-headertextalign "headerTextAlign") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). There are four possible ways to align header text, they are.

1. Right
2. Left
3. Center
4. Justify

N> For [`headerTextAlign`](https://help.syncfusion.com/api/js/ejgrid#members:columns-headertextalign "headerTextAlign") property you can assign either `string` value ("right") or `enum` value (`ej.TextAlign.Right`).

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

![Header text alignment of columns in Javascript grid](columns_images/columns_img3.png)

## Column header customization by external action

We can customize the columns header element by external action using the following methods,

1. [`getHeaderTable`](https://help.syncfusion.com/api/js/ejgrid#methods:getheadertable "getHeaderTable")
2. [`getHeaderContent`](https://help.syncfusion.com/api/js/ejgrid#methods:getheadercontent "getHeaderContent") 

The following code example describes the above behavior.

{% highlight html %}
<input id="change">
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$("#change").ejButton({
    text: "Update Grid header",
    click: function(args){
        var obj = $("#Grid").ejGrid("instance");
        obj.getHeaderContent().css("color","green");
        obj.getHeaderTable().css("font-family","fantasy");
    },
});
$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging:true,
        pageSettings:{pageSize:8},
        columns: [
            { field: "OrderID", isPrimaryKey: true, headerText: "Order ID",  width: 90 },
            { field: "CustomerID", headerText: 'Customer ID', width: 90 },
            { field: "Freight", headerText: 'Freight', format: "{0:C}", width: 90 },
            { field: "ShipCountry", headerText: "Ship Country", width: 90 },
            { field: "ShipCity", headerText: 'Ship City', width: 120 }
        ]
    });
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Header customization of columns in Javascript grid](columns_images/columns_img32.png)

## Header Template

The template design that applies on for the column header. To render template, set [`headerTemplateID`](https://help.syncfusion.com/api/js/ejgrid#members:columns-headertemplateid "headerTemplateID") property of the [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns").


N> It's a standard way to enclose the [`template`](https://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") within the `script` tag with `type` as `text/x-jsrender`.

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

![Header Template of columns in Javascript grid](columns_images/columns_img4.png)


## Text alignment

You can [align](https://help.syncfusion.com/api/js/ejgrid#members:columns-textalign "align") both content and header text of particular column using the [`textAlign`](https://help.syncfusion.com/api/js/ejgrid#members:columns-textalign "textAlign") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). There are four possible ways to align content and header text of column, they are.

1. Right
2. Left
3. Center
4. Justify

N> 1. For [`textAlign`](https://help.syncfusion.com/api/js/ejgrid#members:columns-textalign "textAlign") property you can assign either `string` value ("right") or `enum` value (`ej.TextAlign.Right`).

N> 2. The [`textAlign`](https://help.syncfusion.com/api/js/ejgrid#members:columns-textalign "textAlign") property will affect both content and header text of the grid.

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

![Text alignment  of columns in Javascript grid](columns_images/columns_img5.png)


## Format

[Format](https://help.syncfusion.com/api/js/ejgrid#members:columns-format "Format") is the process of customizing the particular column data with specified jQuery recognized globalize formats, such as currency, numeric, decimal, percentage or dates. The globalize format can be specified by using [`format`](https://help.syncfusion.com/api/js/ejgrid#members:columns-format "format") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns").

The [`format`](https://help.syncfusion.com/api/js/ejgrid#members:columns-format "format") value should be wrapped within "{0:" and "}". (For ex: "{0:C3}"). The [data format](https://github.com/jquery/globalize/tree/v0.1.1#format "data format") strings are available for the Date and Number types.

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

![Format process of columns in Javascript grid](columns_images/columns_img6.png)


## Width

You can specify the width for a particular column by setting [`width`](https://help.syncfusion.com/api/js/ejgrid#members:columns-width "width") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") as in the pixel (ex: 100) or in percentage (ex: 40%).

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

![Width property of columns in Javascript grid](columns_images/columns_img7.png)

## Column width customization by external action

To change the columns width by external action use  [`setWidthToColumns`](https://help.syncfusion.com/api/js/ejGrid#methods:setwidthtocolumns "setWidthToColumns") method.

The following code example describes the above behavior. 

{% highlight html %}
<button onclick="methods()">setWidthToColumns</button>
<br/><br/>
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging:true,
        pageSettings:{pageSize:8},
        columns: [
            { field: "OrderID", isPrimaryKey: true, headerText: "Order ID",  width: 90 },
            { field: "CustomerID", headerText: 'Customer ID', width: 90 },
            { field: "Freight", headerText: 'Freight', format: "{0:C}", width: 90 },
            { field: "ShipCountry", headerText: "Ship Country", width: 90 },
            { field: "ShipCity", headerText: 'Ship City', width: 120 }
        ]
    });
});
function methods(){
    var obj=$("#Grid").ejGrid("instance")
    obj.columnsWidthCollection=[70,80,90,78,100];
    obj.setWidthToColumns();
};
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Width customization of columns in Javascript grid](columns_images/columns_img31.png)

## Resizing

The [`allowResizing`](https://help.syncfusion.com/api/js/ejgrid#members:allowresizing "allowResizing") property enables the grid to set the width to columns based on resizing the grid column manually. To modify the resizing behavior use [`resizeSettings`](https://help.syncfusion.com/api/js/ejgrid#members:resizesettings "resizeSettings") property.

### Resizing modes

[`resizeSettings.resizeMode`](https://help.syncfusion.com/api/js/ejgrid#members:resizesettings-resizemode "resizeSettings.resizeMode") mode is used to change the resizing modes. It indicates whether to define mode of resizing.

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Normal</td>
<td class="description">New column size will be adjusted by all other Columns</td>
</tr>
<tr>
<td class="name">NextColumn</td>
<td class="description">New column Size will be adjusted using next column.</td>
</tr>
<tr>
<td class="name">Control</td>
<td class="description">New column Size will be adjusted using entire control</td>
</tr>
</table>

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"> </div> 
{% endhighlight %}

{% highlight javascript %}
<script>
$(function () {
            // the datasource "window.gridData" is referred from jsondata.min.js
          var data = ej.DataManager(window.gridData).executeLocal(ej.Query().take(40));
            $("#Grid").ejGrid({
                dataSource: data,
                allowResizing: true,
                resizeSettings: { resizeMode: "nextColumn" },
                columns: [
                    { field: "ShipCity", headerText: "Ship City", width: 80 },
                    { field: "ShipPostalCode", headerText: "Ship Postal Code", width: 40 },
                    { field: "ShipName", headerText: "Ship Name", width: 40 },
                    { field: "ShipAddress", headerText: "Ship Address", width: 100 },
                ]
            });
        });
</script>
{% endhighlight %}

## Resize to fit 

The [`allowResizeToFit`](https://help.syncfusion.com/api/js/ejgrid#members:allowresizetofit "allowResizeToFit") property enables the Grid to set width to columns based on maximum width of the particular column's content to facilitate full visibility of data in all the grid rows. This automatic behavior is applicable only for the columns which does not have width specified. 

On columns where "width is defined", double click on the particular column header's resizer symbol to resize the column to show the whole text. For example, refer to the "ShipCity" column in the below code snippet and output screen shot. 

By default the resize mode is normal, you can change the resize mode by using property [`resizeSettings.resizeMode `](https://help.syncfusion.com/api/js/ejgrid#members:resizesettings-resizemode "resizeSettings.resizeMode").

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

![Resize to fit property of columns in Javascript grid](columns_images/columns_img8.png)



## Reorder

Reordering can be done by drag and drop on the particular column header from one index to another index within the Grid. Reordering can be enabled by setting the [`allowReordering`](https://help.syncfusion.com/api/js/ejgrid#members:allowreordering "allowReordering") property as `true`.

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

![Reorder property of columns in Javascript grid](columns_images/columns_img10.png)

N> While reordering the columns following events are triggered. 

1. [`columnDragStart`](https://help.syncfusion.com/api/js/ejgrid#events:columndragstart "columnDragStart")
2. [`columnDrop`](https://help.syncfusion.com/api/js/ejgrid#events:columndrop "columnDrop") 

## Column reorder customization by external action

To reorder the column by external action use  [`reorderColumns`](https://help.syncfusion.com/api/js/ejgrid#methods:reordercolumns "reorderColumns") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<button onclick="methods()" >Reorder</button>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowReordering : true,
		columns : [
			{ field: "OrderID" },
			{ field: "EmployeeID"},
			{ field: "Freight" },
			{ field: "ShipCity" },
			{ field: "ShipCountry" }
		]
	});
});
function methods(){
    var obj=$("#Grid").ejGrid("instance")
    obj.reorderColumns( "EmployeeID","OrderID");
};
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Reorder customization of columns in Javascript grid](columns_images/columns_img36.png)


## Visibility

You can hide particular column in Grid view by setting [`visible`](https://help.syncfusion.com/api/js/ejgrid#members:columns-visible "visible") property of it as `false`.

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

![Visibility property of columns in Javascript grid](columns_images/columns_img11.png)

## Column visibility customization by external action

We can show or hide the grid columns externally by using the following methods,

1. [`showColumns`](https://help.syncfusion.com/api/js/ejgrid#methods:showcolumns "showColumns")
2. [`hideColumns`](https://help.syncfusion.com/api/js/ejgrid#methods:hidecolumns "hideColumns") 

We can get the visible or hidden column details by using the following methods,

1. [`getVisibleColumnNames`](https://help.syncfusion.com/api/js/ejgrid#methods:getvisiblecolumnnames "getVisibleColumnNames")
2. [`getHiddenColumnNames`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "getHiddenColumnNames") 

Here, we hide the `CustomerID` column using the [`hideColumns`](https://help.syncfusion.com/api/js/ejgrid#methods:hidecolumns "hideColumns") method and also we shows the hidden column in the text area.

The following code example describes the above behavior. 

{% highlight html %}
<select id="columnName" class="e-ddl" data-bind="value: field">
    <option value="Order ID" selected="selected">Order ID</option>
    <option value="Customer ID">Customer ID</option>
    <option value="Employee ID">Employee ID</option>
    <option value="Freight">Freight</option>
    <option value="Order Date">Order Date</option>
</select>
<input id="visible" type="button" value="Visible Columns" class="e-btn" />
<input id="hidden" type="button" value="Hidden Columns" class="e-btn" />
<textarea id="cols" style="width: 300px;height:50px"></textarea>
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(".e-btn").ejButton({ 
    size: "medium", 
    click: function(args){
        var txt = this.model.text;
        var names = $("#Grid").ejGrid(txt == "Visible Columns" ? "getVisibleColumnNames" : "getHiddenColumnNames");
        $("#cols").val(JSON.stringify(names));
    }
});
$("#columnName").ejDropDownList({width:"120",selectedIndices: [0, 1, 2, 3, 4], 
    change: function(args){
        var opera = args.isChecked ? "showColumns" : "hideColumns";
        $("#Grid").ejGrid(opera,args.selectedText);
}, 
showCheckbox: true}).ejDropDownList("disableItemsByIndices", "0");
$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging:true,
        pageSettings:{pageSize:8},
        columns: [
            { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right },
            { field: "CustomerID", headerText: "Customer ID"},
            { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, format: "{0:C}" },
            { field: "ShipCity", headerText: "Ship City" },
            { field: "ShipName", headerText: "Ship Name" },
            { field: "OrderDate", headerText: "OrderDate" ,format:"{0:dd/MM/yyyy}" }
        ]
    });
});

{% endhighlight %}

The following output is displayed as a result of the above code example.

![Visibility customization of columns in Javascript grid](columns_images/columns_img34.png)          

## Unbound Column

You can define the unbound columns in Grid by not defining the [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") property for that particular column. Value for these columns can be populated either manually using [`queryCellInfo`](https://help.syncfusion.com/api/js/ejgrid#events:querycellinfo "queryCellInfo") event or by using column [`template`](https://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") or by column [`format`](https://help.syncfusion.com/api/js/ejgrid#members:columns-format "format") property.

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
			{ headerText: "",format: "<a onclick =\"click(this)\" href=#>Delete</a>" }
		]
	});
});

function click(e) {
	var obj = $("#Grid").data("ejGrid");
	obj.deleteRecord("OrderID", obj.getSelectedRecords()[0]);
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Unbound Column in Javascript grid](columns_images/columns_img13.png)


## Column Template

HTML templates can be specified in the [`template`](https://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") property of the particular column as a string (HTML element) or ID of the template's HTML element.

You can use JsRender syntax in the template. For more information about JsRender syntax, please refer [this link](http://www.jsviews.com/#jsrapi "this link"). 

For template manipulation using JavaScript, either you can use JsRender [helper](https://www.jsviews.com/#helpers) function or [`templateRefresh`](https://help.syncfusion.com/api/js/ejgrid#events:templaterefresh "templateRefresh") grid event. For more information on [`templateRefresh`](https://help.syncfusion.com/api/js/ejgrid#events:templaterefresh "templateRefresh") event, refer [this link](https://help.syncfusion.com/js/grid/how-to#display-other-syncfusion-controls-in-grid-columns "this link").

N> If [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") is not specified, you will not able to perform editing, grouping, filtering, sorting, search and summary functionalities in particular column.

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

![Template property of columns in Javascript grid](columns_images/columns_img14.png)


## Controlling Grid actions

You can control the Grid actions of a particular column by setting [`allowSorting`](https://help.syncfusion.com/api/js/ejgrid#members:columns-allowsorting "allowSorting"), [`allowGrouping`](https://help.syncfusion.com/api/js/ejgrid#members:columns-allowgrouping "allowGrouping"), [`allow filtering`](https://help.syncfusion.com/api/js/ejgrid#members:columns-allowfiltering "allow filtering"), [`allowResizing`](https://help.syncfusion.com/api/js/ejgrid#members:columns-allowresizing "allowResizing") and [`allowEditing`](https://help.syncfusion.com/api/js/ejgrid#members:columns-allowediting "allowEditing") properties.

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

## Column resize customization by external action

To resize the columns by external action use [`resizeColumns`](https://help.syncfusion.com/api/js/ejgrid#methods:resizecolumns "resizeColumns") method.

The following code example describes the above behavior.

{% highlight html %}
<button onclick="methods()">resizeColumns</button>
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowReordering : true,
		columns : [
			{ field: "EmployeeID",  width:90 },
			{ field: "OrderID",     width:100 },
			{ field: "Freight",     width:75 },
			{ field: "ShipCity ,    width:80 },
			{ field: "ShipCountry", width:90 }
		]
	});
});
function methods(){
    var obj=$("#Grid").ejGrid("instance")
    obj.resizeColumns( "OrderID",80);
};
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Column resize customization in Javascript grid](columns_images/columns_img35.png)

N> 1. While resizing, the following events are triggered [`resized`](https://help.syncfusion.com/api/js/ejgrid#events:resized "resized"), [`resizeStart`](https://help.syncfusion.com/api/js/ejgrid#events:resizestart "resizeStart"), [`resizeEnd`](https://help.syncfusion.com/api/js/ejgrid#events:resizeend "resizeEnd")

## Read only

To make a column as "read-only" then set [`allowEditing`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-allowediting "allowEditing") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") as `false`.

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

![Read only property  of columns in Javascript grid](columns_images/columns_img15.png)


## Expression Column

[Expression](https://help.syncfusion.com/api/js/ejgrid#members:columns-template "Expression") column is possible only for the [`template`](https://help.syncfusion.com/api/js/ejgrid#members:columns-template "template") column.

You can use JsRender syntax in the template.For more information about JsRender syntax, please refer to [this link](http://www.jsviews.com/#jsrapi "the link"). 

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

![Expression Column in Javascript grid](columns_images/columns_img16.png)


## Command Column

### Default action buttons

Using [`command`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands "command") column, you can add CRUD action buttons as one of the Grid column, through [`type`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "type") property of [`commands`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands "commands"). The type property supports the below default [`UnboundType`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "UnboundType") buttons.

1. edit
2. save
3. delete
4. cancel

Through [`buttonOptions`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands-buttonoptions "buttonOptions") property of [`commands`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands "commands"), you can specify all the button options which are supported by Essential Studio JavaScript [`Button`](https://help.syncfusion.com/api/js/ejbutton# "Button") control. 

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

![Default action buttons of columns in Javascript grid](columns_images/columns_img17.png)


### Custom buttons

You can add custom button in the command column by specifying the [`type`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "type") property of [`commands`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands "commands") as "empty" or any other `string` which does not corresponds to the default [`UnboundType`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "UnboundType") buttons.

N> 1. For [`type`](https://help.syncfusion.com/api/js/ejgrid#members:columns-commands-type "type") property you can assign either `string` value ("edit") or `enum` value (`ej.Grid.UnboundType.Edit`).
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

![Custom buttons of columns in Javascript grid](columns_images/columns_img18.png)


## Column Chooser

Column chooser contains the list of all the columns which are defined in the [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") property. Using this you can control the visibility of columns in Grid. You can prevent the display of the particular column name in column chooser by setting [`showInColumnChooser`](https://help.syncfusion.com/api/js/ejgrid#members:columns-showincolumnchooser "showInColumnChooser") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") as `false`. 



Column Chooser would be shown in the top right corner of Grid. To enable column chooser, set the [`showColumnChooser`](https://help.syncfusion.com/api/js/ejgrid#members:showcolumnchooser "showColumnChooser") property as `true`. 

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

![Column chooser in Javascript grid](columns_images/columns_img19.png)


## Foreign Key Column

Lookup data source can be bound to [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). Data [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") and `text` can be set using the [`foreignKeyField`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField") and [`foreignKeyValue`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyvalue "foreignKeyValue") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns").

In the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property, we can bound local and remote data.

I> For foreign key column the sorting and grouping is based on [`foreignKeyField`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField") instead of [`foreignKeyValue`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyvalue "foreignKeyValue").

N> In remote data, server should be configured to perform select and filter operations since the Grid will try to fetch required columns using select operation and the required data using filter operation.

N> To render a Hierarchy Grid with different `foreignKeyField` in parent and child table, click [`here`](https://help.syncfusion.com/js/grid/how-to#hierarchy-grid-with-different-foreignkeyfield-in-parent-and-child-table "here").

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

![Foreign key column in Javascript grid](columns_images/columns_img20.png)

## Foreign Key Adaptor

The Grid can have a look up column. The Foreign key column using [`foreignKeyField`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField") has some limitations such as sort/group operations on column will happen based on `field` instead of [`foreignKeyField`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField"). The `ForeignKeyAdaptor` can be used to overcome this limitation.
      
N> It works by specifying a virtual column (which is not in the grid datasource) in the Grid. This Adaptor should be initialized in the [`load`](https://help.syncfusion.com/api/js/ejgrid#events:load "load") event of the grid. `ForeignKeyAdaptor` supported for only local data binding.

 I> 1. The `field` name of the virtual column should be the name of the field to display from foreign datasource.
 I> 2. By default, the `ForeignKeyAdaptor` uses `JsonAdaptor`, to use other Adaptors specify the Adaptor name as the second argument during initialization.


We have two cases while using ForeignKeyAdaptor.

1. foreignKeyField name is same as the Grid field name. 
2. foreignKeyField name differs with Grid field name.

### foreignKeyField name is same as the Grid field name

Initialize the foreignKeyAdaptor in the [`load`](https://help.syncfusion.com/api/js/ejgrid#events:load "load") event of Grid and define the Grid column field name as [`foreignKeyValue`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyvalue "foreignKeyValue") name.  

The following code example describes the above behavior.      


{% tabs %}  
{% highlight javascript %}

 <script type="text/javascript">
      var foreignObj = [
        {
            dataSource: window.employeeView,
            foreignKeyField: "EmployeeID", //Property in the Grid's main as well as foreignKey dataSource
            foreignKeyValue: "FirstName" //Property in foreignkey dataSource
        }
    ];
        $(function () {
            // the datasource "window.gridData" is referred from jsondata.min.js
            var data = window.gridData;
            $("#Grid1").ejGrid({
                dataSource: data,
                allowPaging: true,
                allowSorting: true,
                allowFiltering: true,
                allowGrouping: true,
                allowMultiSorting: true,
            	load: function(args){               
                	this.model.dataSource.adaptor = new ej.ForeignKeyAdaptor(foreignObj, "JsonAdaptor");
              	},
			columns: [
                         { field: "OrderID", width: 80, isPrimaryKey: true,textAlign: ej.TextAlign.Right,headerText: "Order ID" } ,
                         { field: "FirstName", width: 75, headerText: "First Name" },
                         { field: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                         { field: "ShipName", headerText: 'Ship Name', width: 150 },
                         { field: "ShipCountry", headerText: 'Ship Country', width: 90 }
                ]
            });
        });
    </script>
{% endhighlight  %}
{% endtabs %}           

The following output is displayed as a result of the above code example.

![Foreign key adaptor of columns in Javascript grid](columns_images/columns_img42.png)

### foreignKeyField name differs with Grid field name

In some cases [`foreignKeyField`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField") name does not match with Grid [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name. In this scenario we have to define the [`foreignKeyField`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField") along with [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") in the ForeignKeyAdaptor and initialize the ForeignKeyAdaptor to ejGrid in the [`load`](https://help.syncfusion.com/api/js/ejgrid#events:load "load") event.
      
Grid column field name must be a combination of Grid [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name and [`foreignKeyField`](https://help.syncfusion.com/api/js/ejgrid#members:columns-foreignkeyfield "foreignKeyField") name separated by "_".  

The following code example describes the above behavior.      


{% tabs %}  
{% highlight javascript %}

 <script type="text/javascript">
      var Data = [
         { FirstName: 'VINET', Employee: 1},
	     { FirstName: 'TOMSP', Employee: 2},
	     { FirstName: 'HANAR', Employee: 3},
	     { FirstName: 'ANTON', Employee: 4},
	     { FirstName: 'SUPRD', Employee: 5},
	     { FirstName: 'WELLI', Employee: 6},
	     { FirstName: 'HILLA', Employee: 7},
	     { FirstName: 'ANTON', Employee: 8},
	     { FirstName: 'AROUT', Employee: 9},
	     		 
       ];
      var foreignObj = [
        {
            dataSource: Data,
            foreignKeyField: "Employee",  //Property in foreignkey dataSource
            field: "EmployeeID",//Property in the Grid's main dataSource
            foreignKeyValue: "FirstName" //Property in foreignkey dataSource
        }
    ];
      
        $(function () {
            // the datasource "window.gridData" is referred from jsondata.min.js
            var data = window.gridData;
            $("#Grid1").ejGrid({
                dataSource: data,
                allowPaging: true,
                allowSorting: true,
                allowFiltering: true,
                allowGrouping: true,
                allowMultiSorting: true,
            	load: function(args){               
                	this.model.dataSource.adaptor = new ej.ForeignKeyAdaptor(foreignObj, "JsonAdaptor");
              	},
			    columns: [
                         { field: "OrderID", width: 80, isPrimaryKey: true,textAlign: ej.TextAlign.Right,headerText: "Order ID" } ,
                         { field: "EmployeeID_FirstName", width: 75, headerText: "First Name" },
                         { field: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                         { field: "ShipName", headerText: 'Ship Name', width: 150 },
                         { field: "ShipCountry", headerText: 'Ship Country', width: 90 }
                ]
            });
        });
    </script>
{% endhighlight  %}
{% endtabs %}           

The following output is displayed as a result of the above code example.

![Foreign key adaptor of columns in Javascript grid](columns_images/columns_img43.png)

## Customize column

You can [customize](https://help.syncfusion.com/api/js/ejgrid#members:columns-cssclass "customize") the header and content of the particular column by [`cssClass`](https://help.syncfusion.com/api/js/ejgrid#members:columns-cssclass "cssClass") property of the column.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight css %}
.customCSS.e-headercell {
	background-color: #2382c3;
	color: white;
	font-family: 'Bell MT';
	font-size: 20px;
}

.customCSS.e-rowcell {
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
			{ field: "EmployeeID", cssClass: "customCSS" },
			{ field: "Freight" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Column customization in Javascript grid](columns_images/columns_img23.png)


## Grid content customization

We can customize the Grid Content element by external action using the following methods,

1. [`getContent`](https://help.syncfusion.com/api/js/ejgrid#methods:getcontent "getContent")
2. [`getContentTable`](https://help.syncfusion.com/api/js/ejgrid#methods:getcontenttable "getContentTable") 

The following code example describes the above behavior.

{% highlight html %}
<input id="change">
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$("#change").ejButton({
    text: "Update Grid Content",
    click: function(args){
        var obj = $("#Grid").ejGrid("instance");
        obj.getContent().css("color","green");
        obj.getContentTable().css("font-family","fantasy");
    },
});
$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging:true,
        pageSettings:{pageSize:8},
        columns: [
            { field: "OrderID", isPrimaryKey: true, headerText: "Order ID",  width: 90 },
            { field: "CustomerID", headerText: 'Customer ID', width: 90 },
            { field: "Freight", headerText: 'Freight', format: "{0:C}", width: 90 },
            { field: "ShipCountry", headerText: "Ship Country", width: 90 },
            { field: "ShipCity", headerText: 'Ship City', width: 120 }
        ]
    });
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Grid content customization of columns in Javascript grid](columns_images/columns_img40.png)

We can modify the visibility of grid lines by using [`gridLines`](https://help.syncfusion.com/api/js/ejgrid#members:gridlines "gridLines") property.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                allowPaging:true,
                gridLines:ej.Grid.GridLines.Horizontal,        
                pageSettings:{pageSize:8},
                columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
            });
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Columns](columns_images/columns_img41.png)

## Type

Used to define the type of the particular column data. If the [`type`](https://help.syncfusion.com/api/js/ejgrid#members:columns-type "type") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") is not specified then its type is automatically defined based on the first row data of that column.

N> The [`type`](https://help.syncfusion.com/api/js/ejgrid#members:columns-type "type") is needed for filtering feature when first row of the data is "null" or "empty".

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
Gets or sets the type of the column value as string. </td>
</tr>
<tr>
<td>
number</td><td>
Gets or sets the type of the column value as number.</td>
</tr>
<tr>
<td>
date</td><td>
Gets or sets the type of the column value as date.</td>
</tr>
<tr>
<td>
datetime</td><td>
Gets or sets the type of the column value as datetime.</td>
</tr>
<tr>
<td>
boolean</td><td>
Gets or sets the type of the column value as true or false. </td>
</tr>
<tr>
<td>
guid</td><td>
Gets or sets the type of the column value as guid.</td>
</tr>
<tr>
<td>
checkbox </td><td>
Gets or sets the type of the column value as checkbox for row selection.</td>
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

![Type property of columns in Javascript grid](columns_images/columns_img24.png)

## Column Layout

You can set the Grid's columns layout based on either Grid width or its columns width using [`columnLayout`](https://help.syncfusion.com/api/js/ejgrid#members:columnlayout "columnLayout") property of Grid. There are two ways to set the column layout, they are. 

1. Auto
2. Fixed

N> 1. For [`columnLayout`](https://help.syncfusion.com/api/js/ejgrid#members:columnlayout "columnLayout") property you can assign either `string` value ("fixed") or `enum` value (`ej.Grid.ColumnLayout.Fixed`).

N> 2. Default [`columnLayout`](https://help.syncfusion.com/api/js/ejgrid#members:columnlayout "columnLayout") is `auto` which is set the columns layout based on the Grid's width.

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
        columnLayout:ej.Grid.ColumnLayout.Fixed,
		columns : [
			{ field: "OrderID", width: 80 },
            { field: "EmployeeID", width: 80 },
            { field: "ShipCity", width: 90 },
            { field: "ShipName", width: 110 },
            { field: "ShipCountry", width: 100 },
            { field: "Freight", headerText: "Freight", width: 80 }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Column Layout in Javascript grid](columns_images/columns_img25.png)

## Columns customization by external action

To control the grid column actions externally use the following methods,

1. [`getColumnByIndex`](https://help.syncfusion.com/api/js/ejgrid#methods:getcolumnbyindex "getColumnByIndex")
2. [`getColumnFieldNames`](https://help.syncfusion.com/api/js/ejgrid#methods:getcolumnfieldnames "getColumnFieldNames")
3. [`getColumnByHeaderText`](https://help.syncfusion.com/api/js/ejgrid#methods:getcolumnbyheadertext "getcolumnbyheadertext")
4. [`getColumnIndexByField`](https://help.syncfusion.com/api/js/ejgrid#methods:getcolumnindexbyfield "getColumnIndexByField")
5. [`getColumnIndexByHeaderText`](https://help.syncfusion.com/api/js/ejgrid#methods:getcolumnindexbyheadertext "getColumnIndexByHeaderText")
6. [`getFieldNameByHeaderText`](https://help.syncfusion.com/api/js/ejgrid#methods:getfieldnamebyheadertext "getFieldNameByHeaderText")
7. [`getHeaderTextByFieldName`](https://help.syncfusion.com/api/js/ejgrid#methods:getheadertextbyfieldname "getHeaderTextByFieldName") 
8. [`getColumnByField`](https://help.syncfusion.com/api/js/ejgrid#methods:getcolumnbyfield "getColumnByField") 

Here, we changed the Freight column CSS by using the corresponding method.

The following code example describes the above behavior.

{% highlight html %}
<body>
<input  type ="text" id='txtVal' > Enter Column/Index</input>
<style>
.style{
  color:green;
}
</style>
<div>
        <select name="selectIndex"style="width:100px" id="dropdown">
                <option value="getColumnByIndex">getColumnByIndex</option>
                <option value="getColumnByFieldNames">getColumnByFieldNames</option>
                <option value="getColumnIndexByField">getColumnIndexByField</option>
                <option value="getColumnIndexByHeaderText">getColumnIndexByHeaderText</option>
                <option value="getFieldNameByHeaderText">getFieldNameByHeaderText</option>
                <option value="getHeaderTextByFieldName">getHeaderTextByFieldName</option>
        </select>
</div>
<button onclick="methods()" >Click</button></br><br/>
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging: true,
        pageSettings:{pageSize:8},
        columns: [
            { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 90 },
            { field: "CustomerID", headerText: 'Customer ID', width: 90 },
            { field: "Freight", headerText: 'Freight', format: "{0:C}", textAlign: ej.TextAlign.Right, width: 90 },
            { field: "ShipCountry", headerText: "Ship Country", width: 90 },
            { field: "ShipCity", headerText: 'Ship City', width: 120 }
        ]
    });
});
function methods(){
    var option= $("#dropdown_input").val(), gridObj=$("#Grid").ejGrid("instance"), val = $('#txtVal').val();
    if(option=="getColumnByIndex"){
        var newField=obj.getColumnByIndex(val) 
        newField.cssClass = "style"; // CSS is added to Freight column
        obj.refreshContent(true);
    }
};
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Columns customization in Javascript grid](columns_images/columns_img30.png)

