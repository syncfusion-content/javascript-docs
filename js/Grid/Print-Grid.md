---
layout: post
title: Print with Grid widget for Syncfusion Essential JS
description: How to enable print option in Grid
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Print

You need to use [`print()`](https://help.syncfusion.com/api/js/ejgrid#methods:print) method from Grid instance to print the Grid. You can add Print option in Toolbar item by adding `ej.Grid.ToolBarItems.PrintGrid` in [`toolbarItems`](https://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-toolbaritems).

{% highlight html %}

<div id="Grid">
<script type="text/javascript">
  $("#Grid").ejGrid(
  // the datasource "window.gridData" is referred from jsondata.min.js
 	dataSource: window.gridData,
  	toolbarSettings:{showToolbar: true,toolbarItems: [ej.Grid.ToolBarItems.PrintGrid]},
  	allowPaging: true,
  	columns: 
  		[
  			{field: "OrderID",headerText: "Order ID",textAlign: ej.TextAlign.Right,width: 75},
  			{field: "CustomerID",headerText: "Customer ID",width: 90},
  			{field: "EmployeeID",headerText: "Employee ID",textAlign: ej.TextAlign.Right,width: 80},
  			{field: "Freight",headerText: "Freight",textAlign: ej.TextAlign.Right,width: 80},
  			{field: "ShipCity",headerText: "Ship City",width: 90}
  		]
	});
</script>
	
{% endhighlight %}

![](Print-Grid_images/Print_img1.png)


## Page Setup

Some of the print options are not configurable through the JavaScript code. You need to customize layout, paper size, and margins options through browser's page setup dialog. Please find the following guidelines link to browser page setup.

* [Chrome](https://support.google.com/chrome/answer/1379552?hl=en)
* [Firefox](https://support.mozilla.org/en-US/kb/how-print-web-pages-firefox)
* [Safari](http://www.mintprintables.com/print-tips/adjust-margins-osx/)
* [IE](http://www.helpteaching.com/help/print/index.htm) 

## Print on external Button Click

By default, the Grid can be printed from toolbar. To print from external button action, you need to call the grid's [`print()`](https://help.syncfusion.com/api/js/ejgrid#methods:print) method from required button event.

{% highlight html %}
<button id="print">Print</button>

<div id="Grid"></div>

<script type="text/javascript">

$("#print").ejButton({

	showRoundedCorner: true,
	size: "mini",
	click: function () {
		$("#Grid").ejGrid("print");
	}

});

$("#Grid").ejGrid({

// the datasource "window.gridData" is referred from jsondata.min.js

	dataSource: window.gridData,
	allowPaging: true,
	enableHeaderHover: true,
	columns: [
				{field: "OrderID",headerText: "Order ID",textAlign: ej.TextAlign.Right,width: 75},
				{field: "CustomerID",headerText: "Customer ID",width: 90},
				{field: "EmployeeID",headerText: "Employee ID",textAlign: ej.TextAlign.Right,width: 80},
				{field: "Freight",headerText: "Freight",textAlign: ej.TextAlign.Right,width: 80},
				{field: "ShipCity",headerText: "Ship City",width: 90}
			]

		});

</script>



{% endhighlight %}

![](Print-Grid_images/Print_img2.png)

{:caption}
Grid with external button for Print

![](Print-Grid_images/Print_img3.png)
{:caption}

Print dialog in Chrome browser

## Print Visible Page

By default, the Grid will print all records. To print current page, you need to set `pageSettings.printMode` as the `ej.Grid.PrintMode.CurrentPage`.

{% highlight  html %}

<div id="Grid"></div>
<script type="text/javascript">
$("#Grid").ejGrid({
	// the datasource "window.gridData" is referred from jsondata.min.js
	dataSource: window.gridData,
	allowPaging: true,
	pageSettings:{printMode:ej.Grid.PrintMode.CurrentPage},
	toolbarSettings: {showToolbar: true,toolbarItems: [ej.Grid.ToolBarItems.PrintGrid]},
	columns: 
	[
		{field: "OrderID",headerText: "Order ID",textAlign: ej.TextAlign.Right,width: 75}, 
		{field: "CustomerID",headerText: "Customer ID",width: 90}, 
		{field: "EmployeeID",headerText: "Employee ID",textAlign: ej.TextAlign.Right,width: 80}, 
		{field: "Freight",headerText: "Freight",textAlign: ej.TextAlign.Right,width: 80}, 
		{field: "ShipCity",headerText: "Ship City",width: 90}, 
		{field: "Verified",headerText: "Verified",width: 90}
	]
});
		</script>
		

{% endhighlight %}