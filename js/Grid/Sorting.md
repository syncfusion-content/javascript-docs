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
		allowSorting : true,
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the previous code example.

![](sorting_images/sorting_img1.png)


## Initial sorting

Through the `sortedColumns` property of [`sortSettings`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings "sortSettings"), you can sort the columns while initializing the grid itself. You need to specify the [`field`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings-sortedcolumns-field "field") (column) name and [`direction`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings-sortedcolumns-direction "direction") in the `sortedColumns`.

N> 1. For the [`direction`](https://help.syncfusion.com/api/js/ejgrid#members:sortsettings-sortedcolumns-direction "direction") property you can assign either the `string` value ("descending") or `enum` value (`ej.sortOrder.Descending`). 
N> 2. You can add multiple columns in the `sortedColumns` for multi column sorting while initializing the grid itself.

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
		allowSorting : true,
		sortSettings: { sortedColumns: [{ field: "EmployeeID", direction: "descending" }] },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the previous code example.

![](sorting_images/sorting_img2.png)


## Multi-column sorting

Sort multiple columns in grid by setting the [`allowMultiSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowmultisorting "allowMultiSorting") property as true. The sorting order is displayed in the header while doing multi sorting.

You can sort more than one column by pressing "Ctrl key + mouse left click" on the column header. To clear sorting for particular column, press "Shift + mouse left click". 

N> The [`allowSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowsorting "allowSorting") must be true while enabling multi sort.

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
		allowSorting : true,
		allowMultiSorting : true,
		//Sorting more than one column while initializing the grid itself. If direction is not specified, by default it takes as ascending.
		sortSettings: { sortedColumns: [{ field: "EmployeeID", direction: "descending" }, { field: "CustomerID" }] },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the previous code example.

![](sorting_images/sorting_img3.png)


## Stable sorting

For sorting, grid uses default browser's sort function for better performance. On multi column sorting in some browsers like chrome, the records order will be different due to unstable implementation of sorting algorithm in it. 

To resolve this, you need to set the `ej.support.stableSort` as `false`.

This will tell the "DataManager" to use custom sort function for sorting data. 

Please refer to this [link](https://en.wikipedia.org/wiki/Category:Stable_sorts# "link"), to know more information about stable sort.

The following code example describes the previous behavior.

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

The following output is displayed as a result of the previous code example.

![](sorting_images/sorting_img4.png)


## Touch options

While using grid in a touch device, you have an option for multi sorting in single tap on the grid header. By tapping on the grid header, it will show the toggle button in small popup with sort icon. Now, tap the button to enable multi sorting in single tap.

If you tap the popup symbol, then the single tap multi sorting will be disabled. 

N> The [`allowMultiSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowmultisorting "allowMultiSorting") and [`allowSorting`](https://help.syncfusion.com/api/js/ejgrid#members:allowsorting "allowSorting") should be `true` then only the popup will be shown.

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
		allowMultiSorting : true,
		allowSorting : true,
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the previous code example.

![](sorting_images/sorting_img5.png)


### Perform Sorting by External Action:-

To control the grid Sort actions externally use the following methods,

1.[`sortColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:sortcolumn "sortColumn")

2.[`removeSortedColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:removesortedcolumns "removeSortedColumns")

3.[`clearSorting`](https://help.syncfusion.com/api/js/ejgrid#methods:clearsorting "clearSorting")

The following code example describes the above behavior.

{% highlight html %}
 <button id="doSorting" style="width: 100px">SortColumn</button>
 <button id="clearSort" style="width: 100px">ClearSorting</button>
 <button id="RemoveSort" style="width: 100px">RemoveSortedColumns</button>
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
                 $("#doSorting,#clearSort").ejButton({ "click": "Sorting", width: "100" });
	         $("#RemoveSort").ejButton({ "click": "RemoveSorting", width: "160" });           
        });
        function Sorting(args){
          var gridObj = $("#Grid").ejGrid("instance");
             if (this.element.attr("id") == "doSorting") {
		 gridObj.sortColumn("OrderID", "ascending");
              }
             else 
                 gridObj.clearSorting();
               }
        function RemoveSorting(args){
           var gridObj = $("#Grid").ejGrid("instance");
              gridObj.removeSortedColumns("OrderID");  
         }
{% endhighlight %}

N> You can get the field and sorted direction of the column by using [`getsortColumnByField`](https://help.syncfusion.com/api/js/ejgrid#methods:getsortcolumnbyfield "getSortColumnByField") method.

The following output is displayed as a result of the previous code example.

![](sorting_images/sorting_img6.png)

N> To get the sorted data of the grid after sorting a column you can refer the [`How To`](https://help.syncfusion.com/js/grid/how-to "Getting Datasource of Grid in Sorted Order").