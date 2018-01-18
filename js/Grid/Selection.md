---
layout: post
title: Selection with Grid widget for Syncfusion Essential JS
description: How to enable selection and its functionalities
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Selection

The Selection provides an interactive support to highlight the row, cell or column that you select. Selection can be done through simple Mouse down or Keyboard interaction. To enable selection, set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") as `true`. 

## Types of Selection

There are two types of selections available in Grid. They are as follows:

1. Single 
2. Multiple 

### Single Selection

Single selection is an interactive support to select a specific row, cell or column in grid by mouse or keyboard interactions. To enable single selection set the [`selectionType`](https://help.syncfusion.com/api/js/ejgrid#members:selectiontype "selectionType") property as `single` and also set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") property as `true`.

### Multiple Selections

Multiple selections is an interactive support to select a group of rows, cells or columns in grid by mouse or keyboard interactions. To enable multiple selections set the [`selectionType`](https://help.syncfusion.com/api/js/ejgrid#members:selectiontype "selectionType") property as `multiple` and also set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") property as `true`.

## Row Selection

Row selection is enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `row`. For random row selection, press **"Ctrl + mouse left"** click and for continuous row selection press **"Shift + mouse left"** click on the grid rows. To unselect the selected rows, press **"Ctrl + mouse left"** click on the selected row.

To select the row while initializing the grid use [`selectedRowIndex `](https://help.syncfusion.com/api/js/ejgrid#members:selectedrecords "selectedRowIndex ") property.

While row selecting the following events are triggered,

1. [`rowSelected`](https://help.syncfusion.com/api/js/ejgrid#events:rowselected "rowSelected")
2. [`rowSelecting`](https://help.syncfusion.com/api/js/ejgrid#events:rowselecting "rowSelecting")

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
		allowSelection : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["row"] },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}



The following output is displayed as a result of the above code example.

![](selection_images/selection_img1.png)

N> We can get the selected row details in grid by using [`getSelectedRows`](https://help.syncfusion.com/api/js/ejgrid#methods:getselectedrows "getSelectedRows") method.

# Row selection by external action

To select the rows by external action use [`selectRows`](https://help.syncfusion.com/api/js/ejgrid#methods:selectrows "selectRows") by setting the starting and ending index we can select the rows.

The following code example describes the above behavior.

{% highlight javascript %}
var gridObj = $("#Grid").data("ejGrid");
gridObj.selectRows(1, 4); 
{% endhighlight %}

# Clear selection by external action

To clear the row selection by external action use [`clearSelection`](https://help.syncfusion.com/api/js/ejgrid#methods:clearselection "clearSelection") method.

The following code example describes the above behavior.

{% highlight javascript %}
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearSelection(); // clears all of the row selection
{% endhighlight %}

We can clear the specific row selection by providing the index value in the  [`clearSelection`](https://help.syncfusion.com/api/js/ejgrid#methods:clearselection "clearSelection") .

The following code example describes the above behavior.

{% highlight javascript %}
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearSelection(2); // Removes the selection based on the row index
{% endhighlight %}

While clearing the row selection the following events are triggered,

1. [`rowDeselected`](https://help.syncfusion.com/api/js/ejgrid#events:rowdeselected "rowDeselected")
2. [`rowDeselecting`](https://help.syncfusion.com/api/js/ejgrid#events:rowdeselecting "rowDeselecting")

## Multiple Row Selection using Checkbox Column

Select multiple rows in grid by using the Checkbox column and it can be enabled by setting column `type` as `checkbox`. It also provides the option to select/deselect all the rows in Grid using a checkbox in the corresponding column header.

If the `field` property of Checkbox column is not defined, then it acts as a template column. So, the `field` property is necessary to perform grid actions like sorting, editing, etc., for the corresponding Checkbox column.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
        $("#Grid").ejGrid({
            dataSource: window.gridData,
            allowPaging: true,
            columns: [
                      { type: "checkbox", width: 50 }, //enables the checkbox column
                      { field: "OrderID", isPrimaryKey: true, width: 80, textAlign: ej.TextAlign.Right },
                      { field: "CustomerID", headerText: "Customer ID", width: 75 },
                      { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                      { field: "Freight", headerText: "Freight", width: 75, textAlign: ej.TextAlign.Right, format: "{0:C}" },
            ]
        });
});
{% endhighlight %}



The following output is displayed as a result of the above code example.

![](selection_images/selection_img6.png)

## Cell Selection

Cell selection is enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `cell`. For random cell selection, press **"Ctrl + mouse left"** click and for continuous cell selection, press **"Shift + mouse left"** click on the grid cells. To unselect selected cells, press **"Ctrl + mouse left"** on the selected cell.

While cell selecting the following events are triggered,

1. [`cellSelected`](https://help.syncfusion.com/api/js/ejgrid#events:cellselected "cellSelected")
2. [`cellSelecting`](https://help.syncfusion.com/api/js/ejgrid#events:cellselecting "cellSelecting")


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
		allowSelection : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["cell"] },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](selection_images/selection_img2.png)

# Cell selection by external action

we can select the cell externally by using [`selectCells`](https://help.syncfusion.com/api/js/ejgrid#methods:selectcells "selectCells") method. By setting starting index of row and indexes of cells for that corresponding row for selecting cells.

The following code example describes the above behavior.

{% highlight javascript %}
var gridObj = $("#Grid").data("ejGrid");
gridObj.selectCells([[1, [4, 3, 2]]]); 
{% endhighlight %}


# Clear cell selection by external action

We can clear the cell selection using  [`clearCellSelection`](https://help.syncfusion.com/api/js/ejgrid#methods:clearcellselection "clearCellSelection") method.

The following code example describes the above behavior.

{% highlight javascript %}
var gridObj = $("#Grid").data("ejGrid");
gridObj.clearCellSelection();
{% endhighlight %}

While clearing the cell selection the following events are triggered,

1. [`cellDeselected`](https://help.syncfusion.com/api/js/ejgrid#events:celldeselected "cellDeselected")
2. [`cellDeselecting`](https://help.syncfusion.com/api/js/ejgrid#events:celldeselecting "cellDeselecting")

### Cell Selection Mode

Cell selection mode is enabled by setting the [`cellSelectionMode `](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-cellselectionmode "cellselectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings").There are two types of cell selection available in grid. 

They are as follows:

1. Continuous Selection
2. Box Selection

Box cell selection is to select multiple cells vertically based on the initial column index selection.  

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
		allowSelection : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["cell"], cellSelectionMode: ej.Grid.CellSelectionMode.Box },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](selection_images/selection_img3.png)


## Column Selection

[Column selection](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "Column selection") can be enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `column`. For random column selection, press **"Ctrl + mouse left click"** and for continuous column selection, press **"Shift + mouse left click"** on the top of the column header. To unselect selected columns, press **"Ctrl + mouse left click"** on top of the selected column header.

While column selecting the following events are triggered,

1. [`columnSelected`](https://help.syncfusion.com/api/js/ejgrid#events:columnselected "columnSelected")
2. [`columnSelecting`](https://help.syncfusion.com/api/js/ejgrid#events:columnselecting "columnSelecting")

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
		allowSelection : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["column"] },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](selection_images/selection_img4.png)

# Column selection by external action

we can select the column externally by using [`selectColumns`](https://help.syncfusion.com/api/js/ejgrid#methods:selectcolumns "selectColumns") method. By setting starting index of column for selecting columns.

The following code example describes the above behavior.

{% highlight javascript %}
var gridObj = $("#Grid").data("ejGrid");
gridObj.selectColumns(1,4); 
{% endhighlight %}

While clearing the column selection the following events are triggered,

1. [`columnDeselected`](https://help.syncfusion.com/api/js/ejgrid#events:columndeselected "columnDeselected")
2. [`columnDeselecting`](https://help.syncfusion.com/api/js/ejgrid#events:columndeselecting "columnDeselecting")

# Clear column selection by external action

To clear the column selection by external action use [`clearColumnSelection`](https://help.syncfusion.com/api/js/ejgrid#methods:clearcolumnselection "clearColumnSelection") method.

The following code example describes the above behavior.

{% highlight javascript %}
var gridObj = $("#Grid").ejGrid("instance")
gridObj.clearColumnSelection(); // clears all of the column selection
{% endhighlight %}

We can clear the specific column selection by providing the index value in the  [`clearColumnSelection`](https://help.syncfusion.com/api/js/ejgrid#methods:clearcolumnselection "clearColumnSelection") .

The following code example describes the above behavior.

{% highlight javascript %}
var gridObj = $("#Grid").ejGrid("instance")
gridObj.clearColumnSelection(2); // Removes the selection based on the row index
{% endhighlight %}


## Touch options

While using the Grid in a [touch](https://help.syncfusion.com/api/js/ejgrid#members:enabletouch "touch") device environment, there is an option for multi selection through single tap on the row and it will show a popup with multi-selection symbol. Tap the icon to enable multi selection in a single tap.

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
		allowSelection : true,
		selectionType : "multiple",
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}



The following output is displayed as a result of the above code example.

![](selection_images/selection_img5.png)


## Toggle Selection

The [Toggle](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-enabletoggle "Toggle") selection allows to perform selection and unselection of the particular row, cell or column.  To enable toggle selection, set [`enableToggle`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-enabletoggle "enableToggle") property of the [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `true`. If you click on the selected row, cell or column then it will be unselected and vice versa. 

N> If multi selection is enabled, then first click on any selected row (without pressing Ctrl key), it will clear the multi selection and in second click on the same row, it will be unselected. 

The following code example describes the above behavior. 

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from jsondata.min.js
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		allowPaging : true,
		enableRowHover : false,
		selectionSettings: { enableToggle: true },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

