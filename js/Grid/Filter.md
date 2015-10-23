---
layout: post
title: Filter
description: filter
platform: js
control: Grid
documentation: ug
--- 

# Filter 

Filtering helps to view particular or related records from datasource which meets a given filtering criteria. To enable filter, set `allowFiltering` as `true`. 

There are three types of filter is supported by grid, they are

1. Filter bar
2. Menu 
3. Excel

There are four types of filtering available in menu filter, they are

1. String 
2. Numeric 
3. Date 
4. Boolean

The corresponding filter menu is opened based on the column type.

T> [1. Need to specify the [`type`](http://help.syncfusion.com/js/api/ejgrid#members:columns-type "") of column when first record data value is empty or null otherwise the filter menu is not opened. <BR> 2. The default filter type is Filter bar when `allowFiltering` is enabled and [`filterType`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") is not set.]

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
		allowFiltering : true,
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](filtering_images/filtering_img1.jpeg)


## Menu filter

[Menu filtering](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") can be enabled by setting [`filterType`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") as `menu` in the [`filterSettings`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings "") property. 

There is an option to show or hide the additional filter options in the menu by setting [`filterSettings.showPredicate`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-showpredicate "") as `true` or `false` respectively.

I>  [For [`filterType`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") property you can assign either `string` value (“menu”) or `enum` value (`ej.Grid.FilterType.Menu`)]

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
		allowFiltering : true,
		filterSettings : {
			filterType : "menu"
		},
		columns : [
			{ field: "OrderID" },
			{ field: "EmployeeID" },
			{ field: "CustomerID" },
			{ field: "OrderDate", format: "{0:dd/MM/yyyy}" },
			{ field: "Verified" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](filtering_images/filtering_img2.jpeg)


![](filtering_images/filtering_img3.jpeg)


![](filtering_images/filtering_img4.jpeg)


![](filtering_images/filtering_img5.jpeg)


## Excel-like filter

You can enable [excel menu](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") by setting  [`filterSettings.filterType`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") as `excel`. The excel filter menu contains an option such as Sorting, Clear filter, submenu for the advanced filter options.

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
		allowSorting : true,
		allowFiltering : true,
		filterSettings : {
			filterType : "excel"
		},
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](filtering_images/filtering_img6.jpeg)


Checkbox list generation:

By default, the checkbox list generated from distinct values of the filter column from data source which give easy option search and select the required items.

Also on checkbox list generation, if the number of distinct values are higher than 1000, the excel filter will display only first 1000 values to ensure the best performance on rendering and search. However this limit customized to according to your requirement by setting [`filterSettings.maxFilterChoices`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-maxfilterchoices "") with required limit in integer.

T> [1. Using filter events you can change the datasource of the checkbox list. <BR> 2. [`ej.Query`](http://help.syncfusion.com/js/api/ejquery# "") of checkbox list can also be changed using filter events.]

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
		allowSorting : true,
		allowFiltering : true,
		filterSettings : { filterType : "excel", maxFilterChoices : 4 },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](filtering_images/filtering_img7.jpeg)


### Case Sensitivity

To perform filter operation with case sensitive in excel styled filter menu mode by setting [`enableCaseSensitivity`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-enablecasesensitivity "") as `true`.

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
		allowFiltering : true,
		filterSettings : { enableCaseSensitivity : true, filterType : "excel" },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](filtering_images/filtering_img8.jpeg)


## Filter bar

[Filter bar](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") row is located next to column header row. It enables you to filter the records with different expressions depending upon the column type. To show the filter bar row, set the [`filterType`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") as `filterbar`.

List of Filter bar Expressions:

You can enter the below filtering expressions manually in the filter bar.

<table>
<tr>
<td>
Expression<br/><br/></td><td>
Example<br/><br/></td><td>
Description<br/><br/></td><td>
Column Type<br/><br/></td></tr>
<tr>
<td>
=<br/><br/></td><td>
= value<br/><br/></td><td>
equal<br/><br/></td><td>
Numeric<br/><br/></td></tr>
<tr>
<td>
!= <br/><br/></td><td>
!= value<br/><br/></td><td>
notequal<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
><br/><br/></td><td>
> value<br/><br/></td><td>
greaterthan<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<<br/><br/></td><td>
< value<br/><br/></td><td>
lessthan<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
>=<br/><br/></td><td>
>= value<br/><br/></td><td>
greaterthanorequal<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<=<br/><br/></td><td>
<= value<br/><br/></td><td>
lessthanorequal<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
N/A<br/><br/></td><td>
N/A<br/><br/></td><td>
Always `startswith` operator will be used for string filter<br/><br/></td><td>
String<br/><br/></td></tr>
<tr>
<td>
N/A<br/><br/></td><td>
N/A<br/><br/></td><td>
Always `equal` operator will be used for Date filter <br/><br/></td><td>
Date<br/><br/></td></tr>
<tr>
<td>
N/A<br/><br/></td><td>
N/A<br/><br/></td><td>
Always `equal` operator will be used for Boolean filter<br/><br/></td><td>
Boolean<br/><br/></td></tr>
</table>

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
		allowFiltering : true,
		filterSettings : { filterType : "filterbar" },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](filtering_images/filtering_img9.jpeg)


Filter bar modes:

This specifies the grid to starts the filter action while typing in the filter bar or after pressing the enter key based on [`filterBarMode`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filterbarmode "").There are two types of [`filterBarModes`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filterbarmode ""), they are

1. OnEnter
2. Immediate

I> [For [`filterBarMode`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filterbarmode "") property you can assign either `string` value (onenter) or `enum` value (`ej.Grid.FilterBarMode.OnEnter`)]

Filter bar message:

The filter bar message is supported only for the [`filterType`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-filtertype "") as filterbar. The filtered data with column name is displayed in the grid pager itself. By default [`showFilterBarMessage`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings-showfilterbarmessage "") is true.

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
		allowFiltering : true,
		filterSettings : { showFilterBarMessage : true },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](filtering_images/filtering_img10.jpeg)


## Filter Operators

The grid controls uses filter operators from [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# ""), that are used at the time of filtering. Filter operators are used to denote filtering type.

List of Column type and Filter operators

<table>
<tr>
<td>
Column Type<br/><br/></td><td>
Filter Operators<br/><br/></td></tr>
<tr>
<td>
Number<br/><br/></td><td>
ej.FilterOperators.greaterThan<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.greaterThanOrEqual<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.lessThan<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.lessThanOrEqual<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.equal<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.notEqual<br/><br/></td></tr>
<tr>
<td>
String<br/><br/></td><td>
ej.FilterOperators.startsWith<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.endsWith<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.contains<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.equal<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.notEqual<br/><br/></td></tr>
<tr>
<td>
Boolean<br/><br/></td><td>
ej.FilterOperators.equal<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.notEqual<br/><br/></td></tr>
<tr>
<td>
Date<br/><br/></td><td>
ej.FilterOperators.greaterThan<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.greaterThanOrEqual<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.lessThan<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.lessThanOrEqual<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.equal<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ej.FilterOperators.notEqual<br/><br/></td></tr>
</table>
