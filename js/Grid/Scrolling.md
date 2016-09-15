---
layout: post
title: scrolling with Grid widget for Syncfusion Essential JS
description: How to enable scrolling and its functionalities
platform: js
control: Grid
documentation: ug
--- 
# Scrolling

Scrolling can be enabled by setting [`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "allowScrolling") as `true`. The height and width can be set to grid by using the properties [`scrollSettings.height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "scrollSettings.height") and [`scrollSettings.width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "scrollSettings.width") respectively. 

N> If [`width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "width") and [`height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "height") is not defined in the [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "scrollSettings") property then the horizontal and vertical scrollbar is enabled, only when the grid width exceeds the browser width.

The height and width can be set in percentage and pixel. The default value for [`height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "height") and [`width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "width") in [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "scrollSettings") is 0 and `auto` respectively.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
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

To specify the [`scrollSettings.width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "scrollSettings.width") and [`scrollSettings.height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "scrollSettings.height") in pixel, by set the pixel value as integer. 

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
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

To specify the [`scrollSettings.width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "scrollSettings.width") and [`scrollSettings.height`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-height "scrollSettings.height") in percentage, by set the percentage value as string.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
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

Specify [`width`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-width "width") property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "scrollSettings") as auto, then the scrollbar is rendered only when the grid width exceeds the browser window width.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
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

Specify [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "frozenColumns") property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "scrollSettings") to freeze the columns(upto the specified frozenColumns value) at the time of scrolling. Horizontal scrollbar must be enabling while specifying [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "frozenColumns") then only you can scroll and see the remaining columns with freeze pane.

N> [`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "allowScrolling") must be `true` while specifying [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "frozenColumns").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: 550, height: 300, frozenColumns: 2 },    
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img5.png)


### Freeze particular columns:

To freeze selected columns in grid at the time of scrolling, by set [`isFrozen`](http://help.syncfusion.com/js/api/ejgrid#members:columns-isfrozen "isFrozen") property of columns as `true`. [`isFrozen`](http://help.syncfusion.com/js/api/ejgrid#members:columns-isfrozen "isFrozen") columns are rendered first in the grid even the columns index is different while declaring the [`columns`](http://help.syncfusion.com/js/api/ejgrid#members:columns "columns").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
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


### Frozen Columns alert Messages:

1. If [`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "allowScrolling") is false while using [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "frozenColumns") then "Enable [`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "allowScrolling") while using frozen Columns" alert message is thrown.
2. If [`frozenColumns`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozencolumns "frozenColumns") is specified out of the grid column view then "Frozen columns should be in grid view area" alert message is thrown.
3. Frozen Rows and Columns are not supported the following features
 Grouping
 Row Template
 Detail Template
 Hierarchy Grid 
 Batch Editing

If any one of the above feature is enabled along with Frozen Rows and Columns, then "Frozen Columns and Rows are not supported for Grouping, Row Template, Detail Template, Hierarchy Grid and Batch Editing" alert message is thrown.

## Frozen Rows

Specify [`frozenRows`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozenrows "frozenRows") property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "scrollSettings") to freeze rows(upto the specified frozenRows value) at the time of scrolling. Vertical scrollbar must be enabling while specifying [`frozenRows`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozenrows "frozenRows") then only you can scroll and see the remaining rows with freeze pane.

N> [`allowScrolling`](http://help.syncfusion.com/js/api/ejgrid#members:allowscrolling "allowScrolling") must be `true` while specifying [`frozenRows`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-frozenrows "frozenRows").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
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

In [touch](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-enabletouchscroll "touch") supported devices you can scroll and show the content by swipe left, right, top and bottom. Disable touch scroll by setting [`enableTouchScroll`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-enabletouchscroll "enableTouchScroll") property of [`scrollSettings`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings "scrollSettings") as `false`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowScrolling : true,
		scrollSettings: { width: 550, height: 300, enableTouchScroll: false },     
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

## Virtual Scrolling

The virtual scrolling support allows you to load data that you require (load data based on page size) without buffering the entire huge database. 

To enable virtual scrolling by setting `AllowVirtualScrolling`  property of `ScrollSettings`  as `true`. It supports two mode of virtualization. They are,

1. Normal Mode
2. Continuous Mode

We also have an enhanced virtual scrolling feature with an improvised virtual scrolling performance. To enable improvised virtual scrolling feature by setting `EnableVirtualization` property of `ScrollSettings` as true and it doesn't requires `AllowVirtualScrolling` to enabled.

### Normal Mode:

It allows you to load the grid with data while scrolling. This can be achieved by setting [`virtualScrollMode`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-virtualscrollmode "virtualScrollMode") as `normal`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
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


### Continuous Mode:

In Continuous mode, the data is loaded in grid when the scrollbar reaches the end.  You can enable the continuous mode by setting the [`virtualScrollMode`](http://help.syncfusion.com/js/api/ejgrid#members:scrollsettings-virtualscrollmode "virtualScrollMode") property as `continuous`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
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

### Enhanced Virtual Scrolling:

It allows you to load the grid with data while scrolling. In order to enable this, you need to enable `EnableVirtualization` property of the `ScrollSettings`. Some of the relevant functionalities of this are,

1.	White space will not be appeared in the Grid. 
2.	Improved page rendering performance. 
3.  It can render nearly 5 lakhs records.

This can be achieved by setting `EnableVirtualization`  as `true`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		dataSource : ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders"),
		allowScrolling : true,
		scrollSettings: { width: 550, height: 300, enableVirtualization: true },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity", "ShipCountry", "ShipAddress", "ShipPostalCode", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](scrolling_images/scrolling_img10.png)

N> The following features are not supported by virtual scrolling 
N> 1. Grouping
N> 2. Frozen Rows 
N> 3. Cell merging 
N> 4. Detail template 
N> 5. Row template 
N> 6. Hierarchy
N> 7. Editing