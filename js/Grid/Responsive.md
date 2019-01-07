---
layout: post
title: Responsive with Grid widget for Syncfusion Essential JS
description: How to set the grid, responsive to screen resolutions
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Responsive

The grid control has support for the responsive behavior based on client browser's width and height. To enable responsive, [`isResponsive`](https://help.syncfusion.com/api/js/ejgrid#members:isresponsive "isResponsive") property should be set as true. There are three modes of responsive layout is available in grid based on client width. They are.

* Mobile(<321px)
* Tablet (321px to 800px)
* Desktop(>800px)

N> The following features are not supported by Grid's Responsive
N> 1. Virtual Scrolling 
N> 2. Frozen Rows and Frozen Columns 
N> 3. Hierarchy
N> 4. Detail template 

I> `ejgrid.responsive.css` should be referred.

## Mobile Layout

If client width is less than 321px, the grid will render in mobile mode. In which, you can see that grid user interface is customized and redesigned for best view in small screens. The customized features includes responsive row rendering, filtering, sorting, searching and editing.

### Responsive Row

Enabling Responsive row makes the Grid to render the record values in vertical order which removes the need for horizontal scrolling to view complete record details. It can be enabled by defining [`enableResponsiveRow`](https://help.syncfusion.com/api/js/ejgrid#members:enableresponsiverow "enableResponsiveRow") property as `true`.

{% highlight html %}

<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({

		dataSource: window.gridData,
		isResponsive: true,
		enableResponsiveRow: true,
		allowPaging: true,
		pageSettings: {
		pageCount: 3,
		pageSize: 7
		},
		columns:
			 [
				 {field: "OrderID",isPrimaryKey: true,headerText: "Order ID"},
				 {field: "CustomerID",headerText: "CustomerID"},
				 {field: "EmployeeID",headerText: "Employee ID"},
				 {field: "ShipCity",headerText: "Ship City"},
				 {field: "Freight",headerText: 'Freight',format: "{0:C}"}
			]
	});

</script>



{% endhighlight %}

![ResponsiveRow](Responsive_images/Responsive_img1.png)


W> IE8 and IE9 does not support responsive row. `ejgrid.responsive.css` should be referred to display Responsive Row.

### Customized Features

The customized layout for filtering, sorting, searching and CRUD operations in mobile device can be seen in the following screen shots.

![customized resposive](Responsive_images/Responsive_img2.png)
{:caption}
Responsive row with filtering , sorting and searching

![crud](Responsive_images/Responsive_img3.png)

{:caption}
CRUD in mobile layout

![filtering4](Responsive_images/Responsive_img4.png)

{:caption}
Filtering in mobile layout

![filtering5](Responsive_images/Responsive_img5.png)
{:caption}

Filtering in mobile layout

![sorting](Responsive_images/Responsive_img6.png)

{:caption}
Sorting in mobile layout

![searching](Responsive_images/Responsive_img7.png)
{:caption}

Searching in mobile layout

{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({

	dataSource: window.gridData,
	enableResponsiveRow: true,
	isResponsive: true,
	allowPaging: true,
	editSettings: {allowAdding: true,allowDeleting: true,allowEditing: true},
	toolbarSettings: {
	showToolbar: true,
	toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel, ej.Grid.ToolBarItems.Search]	
},
	pageSettings: {pageCount: 3,pageSize: 7},
	allowFiltering: true,
	allowSorting: true,
	allowSearching: true,
	allowMultiSorting: true,
	filterSettings: {filterType: "menu"},
	columns:
	 	[
			 {field: "OrderID",isPrimaryKey: true,headerText: "Order ID",validationRules: {required: true,number: true},width: 90,textAlign: ej.TextAlign.Right},
			 {field: "CustomerID",headerText: "CustomerID",validationRules: {required: true},width: 100},
			 {field: "EmployeeID",headerText: "Employee ID",editType: ej.Grid.EditingType.Dropdown,width: 90,textAlign: ej.TextAlign.Right},
			 {field: "ShipCity",headerText: "Ship City",width: 120,editType: ej.Grid.EditingType.Dropdown},
			 {field: "Freight",headerText: 'Freight',width: 110,editParams: {decimalPlaces: 2},editType: ej.Grid.EditingType.Numeric,format: "{0:C}"}
			 ]
	});

</script>



{% endhighlight %}

## Tablet Layout

If the client width is between 321px and 800px, then the grid will render in tablet mode. Also, it has customized filtering design to match tablet screen size.

{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({

	dataSource: window.gridData,
	isResponsive: true,
	allowFiltering: true,
	filterSettings: {filterType: "menu"},
	allowPaging: true,
	pageSettings: {pageCount: 3,pageSize: 8},
	columns:
		 [
			 {field: "OrderID",isPrimaryKey: true,headerText: "Order ID",width: 90,textAlign: ej.TextAlign.Right},
			 {field: "CustomerID",headerText: "CustomerID",width: 100},
			 {field: "EmployeeID",headerText: "Employee ID",width: 90,textAlign: ej.TextAlign.Right},
			 {field: "ShipCity",headerText: "Ship City",width: 120},
			 {field: "Freight",headerText: 'Freight',width: 80,format: "{0:C}"}
			 ]

	});

</script>



{% endhighlight %}

![tab](Responsive_images/Responsive_img8.png)
{:caption}

Default tab layout

![filtertab](Responsive_images/Responsive_img9.png)

{:caption}
Filtering design in tab layout.

## Width

By default, the grid is adaptable to its parent container. It can adjust its width of columns based on parent container width. You can also assign `width` of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") in percentage. 

{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({
	dataSource: window.gridData,
	columns:
	 [
		 {field: "OrderID",isPrimaryKey: true,headerText: "Order ID",width: "10%",textAlign: ej.TextAlign.Right},
		 {field: "CustomerID",headerText: "CustomerID",width: "15%"},
		 {field: "EmployeeID",headerText: "Employee ID",width: "10%",textAlign: ej.TextAlign.Right}
		]
  });

</script>

{% endhighlight %}

I>  [`allowScrolling`](https://help.syncfusion.com/api/js/ejgrid#members:allowscrolling "allowScrolling") should be false while defining width in percentage.

## Min Width

Min Width is used to maintain minimum width for the Grid. To enable Min Width, [`minWidth`](https://help.syncfusion.com/api/js/ejgrid#members:minwidth "minWidth") should be defined. If the grid width is less than [`minWidth`](https://help.syncfusion.com/api/js/ejgrid#members:minwidth "minWidth") then the scrollbar will be displayed to maintain minimum width.

{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({

	dataSource: window.gridData,
	minWidth: 700, 
	allowPaging: true,
	columns:
	 	[
			 {field: "OrderID",isPrimaryKey: true,headerText: "Order ID",width: 90,textAlign: ej.TextAlign.Right}, 
			 {field: "CustomerID",headerText: "CustomerID",width: 100}, 
			 {field: "EmployeeID",headerText: "Employee ID",width: 90,textAlign: ej.TextAlign.Right}, 
			 {field: "ShipCity",headerText: "Ship City",width: 120}, 
			 {field: "Freight",headerText: 'Freight',width: 110,format: "{0:C}"}
			]
		});

</script>



{% endhighlight %}

![minwidth](Responsive_images/Responsive_img10.png)


MinWidth set to Grid

N> We can render the Grid to be height responsive by setting the scrollSettings `height` as `100%`. If the grid height is greater than its parent container's height then the vertical scrollbar will be displayed to view the content.

## Priority for Columns

Priority makes column to be visible or hidden based on the [`priority`](https://help.syncfusion.com/api/js/ejgrid#members:columns-priority "priority") value and browser's width, to accommodate the best possible columns. To enable [`priority `](https://help.syncfusion.com/api/js/ejgrid#members:columns-priority "priority ") for `columns`, [`priority `](https://help.syncfusion.com/api/js/ejgrid#members:columns-priority "priority ") needs to be defined in columns collection. These Priority values are from one to six.

{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({
	dataSource: window.gridData,
	allowPaging: true,
	columns: 
		[
			{field: "OrderID",isPrimaryKey: true,headerText: "Order ID",width: 90,priority: 1,textAlign: ej.TextAlign.Right},
			{field: "CustomerID",headerText: "CustomerID",width: 100,priority: 2},
			{field: "EmployeeID",headerText: "Employee ID",width: 90,priority: 1,textAlign: ej.TextAlign.Right},
			{field: "ShipCity",headerText: "Ship City",width: 120,priority: 3},
			{field: "Freight",headerText: 'Freight',width: 110,format: "{0:C}",priority: 4,}
		]
	});

</script>



{% endhighlight %}


