---
layout: post
title: Selection
description: selection
platform: js
control: Grid
documentation: ug
--- 

# Selection

[Selection](http://help.syncfusion.com/js/api/ejgrid#members:allowselection "") provides an interactive support to highlight the row, cell or column that you select. Selection can be done through simple Mouse down or Keyboard interaction. To enable selection, set [`allowSelection`](http://help.syncfusion.com/js/api/ejgrid#members:allowselection "") as `true`. 

## Types of Selection

There are two types of selections available in grid. They are

1. Single 
2. Multiple 

Single Selection

[Single](http://help.syncfusion.com/js/api/ejgrid#members:selectiontype "") selection is an interactive support to select a specific row, cell or column in grid by mouse or keyboard interactions. To enable single selection by setting [`selectionType`](http://help.syncfusion.com/js/api/ejgrid#members:selectiontype "") property as `single` and also set [`allowSelection`](http://help.syncfusion.com/js/api/ejgrid#members:allowselection "") property as `true`.

Multiple Selections

[Multiple](http://help.syncfusion.com/js/api/ejgrid#members:selectiontype "") selections is an interactive support to select a group of rows, cells or columns in grid by mouse or keyboard interactions. To enable multiple selections by set [`selectionType`](http://help.syncfusion.com/js/api/ejgrid#members:selectiontype "") property as `multiple` and also set [`allowSelection`](http://help.syncfusion.com/js/api/ejgrid#members:allowselection "") property as `true`.

### Row Selection

[Row selection](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings-selectionmode "") is enabled by set [`selectionMode`](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings-selectionmode "") property of [`selectionSettings`](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings "") as `row`. For random row selection, press “Ctrl + mouse left” click and for continuous row selection press “Shift + mouse left” click on the grid rows. To unselect selected rows, by press “Ctrl + mouse left click on selected row.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowSelection : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["row"] },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}



The following output is displayed as a result of the above code example

![](selection_images/selection_img1.png)


### Cell Selection

[Cell selection](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings-selectionmode "") is enabled by set [`selectionMode`](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings-selectionmode "") property of [`selectionSettings`](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings "") as `cell`. For random cell selection, press “Ctrl + mouse left” click and for continuous cell selection, press “Shift + mouse left” click on the grid cells. To unselect selected cells, press “Ctrl + mouse left on selected cell” click.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowSelection : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["cell"] },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example

![](selection_images/selection_img2.png)


#### Cell Selection Mode

There are two types of cell selection available in grid. They are

1. Continuous Selection
2. Box Selection

Box cell selection is to select multiple cells vertically based on the initial column index selection.  

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowSelection : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["cell"], cellSelectionMode: "box" },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example

![](selection_images/selection_img3.png)


### Column Selection

[Column selection](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings-selectionmode "") can be enabled by setting [`selectionMode`](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings-selectionmode "") property of [`selectionSettings`](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings "") as `column`. For random column selection, press “Ctrl + mouse left click” and for continuous column selection, press “Shift + mouse left click” on the top of the column header. To unselect selected columns, press “Ctrl + mouse left click” on top of the selected column header.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowSelection : true,
		selectionType : "multiple",
		selectionSettings: {selectionMode: ["column"] },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example

![](selection_images/selection_img4.png)


## Touch options

While using grid in a [touch](http://help.syncfusion.com/js/api/ejgrid#members:enabletouch "") device environment, there is an option for multi selection through single tap on the row and it will shows a popup with multi-selection symbol. Tap the icon to enable multi selection in a single tap.

The following code example describes the above behavior. 

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
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

The [Toggle](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings-enabletoggle "") selection allows to perform selection and unselection of the particular row, cell or column.  To enable toggle selection, set [`enableToggle`](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings-enabletoggle "") property of [`selectionSettings`](http://help.syncfusion.com/js/api/ejgrid#members:selectionsettings "") as `true`. If you click on the selected row, cell or column then it will be unselected and vice versa. 

I> If multi selection is enabled, then in first click on any selected row (without pressing Ctrl key), it will clear multi selection and in second click on the same row, it will be unselected. 

The following code example describes the above behavior. 

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	// the datasource "window.gridData" is referred from jsondata.min.js
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		allowPaging : true,
		enableRowHover : false,
		selectionSettings: { enableToggle: true },
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

