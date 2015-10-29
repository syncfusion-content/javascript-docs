---
layout: post
title: Scrolling
description: scrolling
platform: js
control: Grid
documentation: ug
--- 

# Scrolling

[Scrolling](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "") can be enabled by setting [`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "") as `true`. The height and width can be set to grid by using the properties [`scrollSettings.height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "") and [`scrollSettings.width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "") respectively. 

I> [If [`width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "") and [`height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "") is not defined in the [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "") property then the horizontal and vertical scrollbar is enabled, only when the grid width is exceeded the browser width.]

The height and width can be set in percentage and pixel. The default value for [`height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "") and [`width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "") in [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "") is 0 and `auto` respectively.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: 400, height: 300},  
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img1.png)


## Set width and height in pixel 	

To specify the [`scrollSettings.width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "") and [`scrollSettings.height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "") in pixel, set value in integer. 

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: 500 , height: 300},     
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img2.png)


## Set width and height in percentage

To set the [`scrollSettings.width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "") and [`scrollSettings.height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "") in percentage, specify percentage value as string.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: "70%", height: "5%" },  
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img3.png)


## Set width as auto

Specify [`width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "") property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "") as auto, and then the scrollbar is rendered only when grid width is greater than browser window size.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: "auto", height: 300 },     
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img4.png)


## Frozen columns

Specify [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "") property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "") to freeze particular columns at the time of scrolling. Horizontal scrollbar must be enabling while specifying [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "") then only you can scroll and see the remaining columns with freeze pane.

I> [[`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "") must be `true` while specifying [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "").]

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: 550, height: 300, frozenColumns: 2 },    
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img5.png)


Freeze particular columns:

To freeze selected columns in grid at the time of scrolling, set [`isFrozen`](http://help.syncfusion.com/js/api/ejgrid#members:columns-isfrozen "") property of columns as `true`. [`isFrozen`](http://help.syncfusion.com/js/api/ejgrid#members:columns-isfrozen "") columns are rendered first in the grid even the columns index is different while declaring the `columns`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings : { width : 550, height : 400 },
		columns : [
			{ field: "OrderID" },
			{ field: "EmployeeID"},
			{ field: "CustomerID"},
			{ field: "Freight", isFrozen: true},
			{ field: "OrderDate", format: "{0:dd/MM/yyyy}" },
			{ field: "ShipCity" },
			{ field: "ShipCountry", isFrozen: true, width: 100 },
			{ field: "ShipAddress" },
			{ field: "ShipPostalCode" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img6.png)


Frozen Columns alert Messages:

1. If [`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "") is false while using [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "") then "Enable [`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "") while using frozen Columns" alert message is thrown.
2. If [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "") is specified out of the grid column view then "Frozen columns should be in grid view area" alert message is thrown.
3. Frozen Rows and Columns are not supported the following features
 Grouping
 Row Template
 Detail Template
 Hierarchy Grid 
 Batch Editing

If any one of the above feature is enabled along with Frozen Rows and Columns, then "Frozen Columns and Rows are not supported for Grouping, Row Template, Detail Template, Hierarchy Grid and Batch Editing" alert message is thrown.

## Frozen Rows

Specify [`frozenRows`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozenrows "") property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "") to freeze particular rows at the time of scrolling. Vertical scrollbar must be enabling while specifying [`frozenRows`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozenrows "") then only you can scroll and see the remaining rows with freeze pane.

I> [[`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "") must be `true` while specifying [`frozenRows`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozenrows "").]

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: 550, height: 300, frozenRows: 4 }, 
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img7.png)


## Touch scroll

In [touch](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-enabletouchscroll "") supported devices you can scroll and show the content by swipe left, right, top and bottom. Disable touch scroll by setting [`enableTouchScroll`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-enabletouchscroll "") property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "") as `false`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: 550, height: 300, enableTouchScroll: false },     
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

## Virtual Scrolling

The virtual scrolling support allows you to load data that you require (load data based on page size) without buffering the entire huge database. To enable virtual scrolling by setting `[allowVirtulScrolling](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-allowvirtualscrolling "")` property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "") as `true`. It supports two mode of virtualization. They are,

1. Normal Mode
2. Continuous Mode

T> [The following features are not supported by virtual scrolling <BR> 1. Grouping <BR> 2. Frozen Rows <BR> 3. Cell merging <BR> 4. Detail template <BR> 5. Row template <BR> 6. Hierarchy] 

Normal Mode:

It allows you to load the grid with data while scrolling. This can be achieved by setting [`virtualScrollMode`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-virtualscrollmode "") as `normal`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		dataSource : ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders"),
		allowScrolling : true,
		scrollSettings: { width: 550, height: 300, allowVirtualScrolling: true, virtualScrollMode: "normal" },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img8.png)


Continuous Mode:

In `Continuous` mode, the data is loaded in grid when the scrollbar reaches the end.  You can enable the continuous mode by setting the [`virtualScrollMode`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-virtualscrollmode "") property as `continuous`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
$(function () {
	$("#Grid").ejGrid({
		dataSource : ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders"),
		allowScrolling : true,
		scrollSettings: { width: 550, height: 300, allowVirtualScrolling: true, virtualScrollMode: "continuous" },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img9.png)


