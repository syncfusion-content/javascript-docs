---
layout: post
title: Sorting with Grid widget for Syncfusion Essential JS
description: How to enable sorting and its functionalities
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Sorting

The Grid control has support to sort data bound columns in ascending or descending order. This can be achieved by setting the [`allowSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowsorting "allowSorting") property as `true`. 

To dynamically sort a particular column, click on its column header. The order switch between ascending and descending each time you click a column header for sorting.

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
		allowSorting : true,
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](sorting_images/sorting_img1.png)


## Initial Sorting

Through the `sortedColumns` property of [`sortSettings`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings "sortSettings"), you can sort the columns while initializing the grid itself. You need to specify the [`field`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings-sortedcolumns-field "field") (column) name and [`direction`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings-sortedcolumns-direction "direction") in the `sortedColumns`.

N> 1. For [`direction`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings-sortedcolumns-direction "direction") property you can assign either `string` value ("descending") or `enum` value (`ej.sortOrder.Descending`). 
N> 2. You can add multiple columns in the `sortedColumns` for multi column sorting while initializing the grid itself.

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
		allowSorting : true,
		sortSettings: { sortedColumns: [{ field: "EmployeeID", direction: "descending" }] },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](sorting_images/sorting_img2.png)


## Multi-Column Sorting

Sort multiple columns in grid by setting [`allowMultiSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowmultisorting "allowMultiSorting") property as true. The sorting order is displayed in the header while doing multi sorting.

You can sort more than one column by pressing "Ctrl key + mouse left click" on the column header. To clear sorting for particular column, press "Shift + mouse left click". 

N> [`allowSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowsorting "allowSorting") must be true while enabling multi sort.

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
		allowSorting : true,
		allowMultiSorting : true,
		//Sorting more than one column while initializing the grid itself. If direction is not specified, by default it takes as ascending.
		sortSettings: { sortedColumns: [{ field: "EmployeeID", direction: "descending" }, { field: "CustomerID" }] },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](sorting_images/sorting_img3.png)


## Stable sorting

For sorting, grid uses default browser's sort function for better performance. On multi column sorting in some browsers like chrome, the records order will be different due to unstable implementation of sorting algorithm in it. 

To resolve this, you need to set the `ej.support.stableSort` as `false`.

This will tell the "DataManager" to use custom sort function for sorting data. 

Please refer to this [link](https://en.wikipedia.org/wiki/Category:Stable_sorts# "link"), to know more information about stable sort.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
ej.support.stableSort = false;
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		allowSorting : true,
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](sorting_images/sorting_img4.png)


## Touch options

While using Grid in a touch device, you have an option for multi sorting in single tap on the grid header. By tapping on the grid header, it will show the toggle button in small popup with sort icon. Now tap the button to enable multi sorting in single tap.

Again if you tap the popup symbol, then the single tap multi sorting will be disabled. 

N> [`allowMultiSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowmultisorting "allowMultiSorting") and [`allowSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowsorting "allowSorting") should be `true` then only the popup will be shown.

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
		allowMultiSorting : true,
		allowSorting : true,
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](sorting_images/sorting_img5.png)


