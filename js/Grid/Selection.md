---
layout: post
title: Selection with Grid widget for Syncfusion Essential JS
description: Learn about How to enable selection and its functionalities in Syncfusion JavaScript Grid control and more details.
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Selection in JavaScript Grid

The selection provides an interactive support to highlight the row, cell or column that you select. Selection can be done through simple mouse down or keyboard interaction. To enable selection, set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") as `true`. 

## Types of selection

There are two types of selections available in grid. They are as follows:

1. Single 
2. Multiple 

### Single selection

Single selection is an interactive support to select a specific row, cell or column in the grid by mouse or keyboard interactions. To enable single selection set the [`selectionType`](https://help.syncfusion.com/api/js/ejgrid#members:selectiontype "selectionType") property as `single` and also set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") property as `true`.

### Multiple selections

Multiple selections is an interactive support to select a group of rows, cells or columns in grid by mouse or keyboard interactions. To enable multiple selections set the [`selectionType`](https://help.syncfusion.com/api/js/ejgrid#members:selectiontype "selectionType") property as `multiple` and also set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") property as `true`.

## Row selection

Row selection is enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `row`. For random row selection, press **"Ctrl + mouse left"** click and for continuous row selection press **"Shift + mouse left"** click on the grid rows. To unselect the selected rows, press **"Ctrl + mouse left"** click on the selected row.

To select the row while initializing the grid use the [`selectedRowIndex `](https://help.syncfusion.com/api/js/ejgrid#members:selectedrowindex "selectedRowIndex ") property. 

The array of selected records in the grid can be displayed by using the [`selectedRecords  `](https://help.syncfusion.com/api/js/ejgrid#members:selectedrecords "selectedRecords  ") property.

While row selecting the following events are triggered:

1. [`rowSelected`](https://help.syncfusion.com/api/js/ejgrid#events:rowselected "rowSelected")
2. [`rowSelecting`](https://help.syncfusion.com/api/js/ejgrid#events:rowselecting "rowSelecting")

N> While clearing the row selection the following events are triggered:

N> 1. [`rowDeselected`](https://help.syncfusion.com/api/js/ejgrid#events:rowdeselected "rowDeselected")
N> 2. [`rowDeselecting`](https://help.syncfusion.com/api/js/ejgrid#events:rowdeselecting "rowDeselecting")

The following code example describes the previous behavior.

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



The following output is displayed as a result of the previous code example.

![Row selection in Javascript grid](selection_images/selection_img1.png)

N> We can get the selected row elements in grid by using the [`getSelectedRows`](https://help.syncfusion.com/api/js/ejgrid#methods:getselectedrows "getSelectedRows") method.

## Multiple row selection using checkbox column

Select multiple rows in grid by using the Checkbox column and it can be enabled by setting the column `type` as `checkbox`. It also provides the option to select/deselect all the rows in Grid using a checkbox in the corresponding column header.

If the `field` property of checkbox column is not defined, then it acts as a template column. So, the `field` property is necessary to perform grid actions like sorting, editing, etc., for the corresponding Checkbox column.

The following code example describes the previous behavior.

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



The following output is displayed as a result of the previous code example.

![Multiple row selection in Javascript grid](selection_images/selection_img6.png)

## Cell selection

Cell selection is enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `cell`. For random cell selection, press **"Ctrl + mouse left"** click and for continuous cell selection, press **"Shift + mouse left"** click on the grid cells. To unselect selected cells, press **"Ctrl + mouse left"** on the selected cell.

While cell selecting the following events are triggered,

1. [`cellSelected`](https://help.syncfusion.com/api/js/ejgrid#events:cellselected "cellSelected")
2. [`cellSelecting`](https://help.syncfusion.com/api/js/ejgrid#events:cellselecting "cellSelecting")

N> While clearing the cell selection the following events are triggered,

N> 1. [`cellDeselected`](https://help.syncfusion.com/api/js/ejgrid#events:celldeselected "cellDeselected")
N> 2. [`cellDeselecting`](https://help.syncfusion.com/api/js/ejgrid#events:celldeselecting "cellDeselecting")


The following code example describes the previous behavior.

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

The following output is displayed as a result of the previous code example.

![Cell selection in Javascript grid](selection_images/selection_img2.png)

### Cell selection mode

Cell selection mode is enabled by setting the [`cellSelectionMode `](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-cellselectionmode "cellselectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings").

There are two types of cell selection available in the grid. 

They are as follows:

1. Continuous Selection
2. Box Selection

Box cell selection is to select multiple cells vertically based on the initial column index selection.  

The following code example describes the previous behavior.

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

The following output is displayed as a result of the previous code example.

![Cell selection mode in Javascript grid](selection_images/selection_img3.png)


## Column selection

[Column selection](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "Column selection") can be enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `column`. For random column selection, press **"Ctrl + mouse left click"** and for continuous column selection, press **"Shift + mouse left click"** on the top of the column header. To unselect selected columns, press **"Ctrl + mouse left click"** on top of the selected column header.

While column selecting the following events are triggered:

1. [`columnSelected`](https://help.syncfusion.com/api/js/ejgrid#events:columnselected "columnSelected")
2. [`columnSelecting`](https://help.syncfusion.com/api/js/ejgrid#events:columnselecting "columnSelecting")

N> While clearing the column selection the following events are triggered:

N> 1. [`columnDeselected`](https://help.syncfusion.com/api/js/ejgrid#events:columndeselected "columnDeselected")
N> 2. [`columnDeselecting`](https://help.syncfusion.com/api/js/ejgrid#events:columndeselecting "columnDeselecting")

The following code example describes the previous behavior.

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

The following output is displayed as a result of the previous code example.

![Column selection in Javascript grid](selection_images/selection_img4.png)

## Touch options

While using the grid in a [touch](https://help.syncfusion.com/api/js/ejgrid#members:enabletouch "touch") device environment, there is an option for multi selection through single tap on the row and it will show a popup with multi-selection symbol. Tap the icon to enable multi selection in a single tap.

The following code example describes the previous behavior. 

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



The following output is displayed as a result of the previous code example.

![Touch options of selection in Javascript grid](selection_images/selection_img5.png)


## Toggle selection

The Toggle selection allows to perform selection and unselection of the particular row, cell or column.  To enable toggle selection, set [`enableToggle`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-enabletoggle "enableToggle") property of the [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `true`. If you click on the selected row, cell or column then it will be unselected and vice versa. 

N> If multi selection is enabled, then first click on any selected row (without pressing Ctrl key), it will clear the multi selection and in second click on the same row, it will be unselected. 

The following code example describes the previous behavior. 

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

## Selection customization by external action

To control the grid selection by external action use the following methods:

1. [`selectRows`](https://help.syncfusion.com/api/js/ejgrid#methods:selectrows "selectRows")
2. [`selectCells`](https://help.syncfusion.com/api/js/ejgrid#methods:selectcells "selectCells")
3. [`selectColumns`](https://help.syncfusion.com/api/js/ejgrid#methods:selectcolumns "selectColumns") 
4. [`clearColumnSelection`](https://help.syncfusion.com/api/js/ejgrid#methods:clearcolumnselection "clearColumnSelection")
5. [`clearCellSelection`](https://help.syncfusion.com/api/js/ejgrid#methods:clearcellselection "clearCellSelection")
6. [`clearSelection`](https://help.syncfusion.com/api/js/ejgrid#methods:clearselection "clearSelection")

Here, we select the `EmployeeID`, `Freight` and `ShipCity` columns using the [`selectColumns`](https://help.syncfusion.com/api/js/ejgrid#methods:selectcolumns "selectColumns") method by providing the corresponding index value.

The following code example describes the previous behavior.

{% highlight html %}
<button id="selectRows" class ="buttons" >selectRows</button>
<button id="selectColumns" class ="buttons" >selectColumns</button>
<button id="selectCells" class ="buttons" >selectCells</button>     
<br/></br>
<button id="clearSelection" class ="buttons" >clearSelection</button>
<button id="clearColumnSelection" class ="buttons" >clearColumnSelection</button>
<button id="clearCellSelection" class ="buttons" >clearCellSelection</button>
<br/></br>
<div>Selection Mode</div>
<br/></br>
</div><select id="selectionMode">
        <option value="row">Row</option>
        <option value="cell">Cell</option>
        <option value="column">Column</option>
      </select>
</div>
<br/></br>
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging:true,
        pageSettings:{pageSize:8},
        selectionType: "multiple",
        enableRowHover: false,
		columns : ["OrderID", "EmployeeID","Freight", "ShipCity", "ShipCountry"]
	});
$("#selectionMode").ejDropDownList({ width: "120px", change: "onSelectionModeChange"});
});
function onSelectionModeChange(args) {
    var mode = $("#selectionMode").data("ejDropDownList")._selectedValue;
    $("#Grid").ejGrid({ selectionSettings: {selectionMode: [mode]} });
}
$(".buttons").ejButton({click:function(args){
     var option=args.target.id;
     if(option=="clearSelection" || option == "clearColumnSelection" || option == "clearCellSelection")
       $("#Grid").ejGrid(option);
     if(option=="selectRows" || option=="selectColumns")
       $("#Grid").ejGrid(option, 1, 3); // Selection based on the given index
     if(option == "selectCells")
       $("#Grid").ejGrid("selectCells", [[1, [4, 3, 2]]]); // Selects cells based on the given index
    }
});
{% endhighlight %}

The following output is displayed as a result of the previous code example.

![Selection customization in Javascript grid](selection_images/selection_img10.png)


## Drag selection

The Drag selection allows to perform the selection of the particular row or cell by performing mouse dragging.  To enable drag selection, set the [`allowDragSelection`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-allowdragselection "allowDragSelection") property of the [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `true`. Now you can select the cells or rows in the grid by dragging the mouse. 

N> The [`selectionType`](https://help.syncfusion.com/api/js/ejgrid#members:selectiontype "selectionType") property as should be set as `multiple`, to select multiple cells in grid by mouse dragging. 

The following code example describes the previous behavior. 

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from jsondata.min.js
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		allowPaging : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["cell"], allowDragSelection:true, cellSelectionMode: ej.Grid.CellSelectionMode.Flow },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the previous code example.

![Drag selection in Javascript grid](selection_images/selection_img11.png)