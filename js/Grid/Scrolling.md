---
layout: post
title: scrolling with Grid widget for Syncfusion Essential JS
description: This section explains about the scrolling and its functionalities like Frozen Rows and Columns, Touch Scroll, Virtual Scroll and the types of Virtual Scroll.
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Enable Scrolling in Grid

Scrolling can be enabled by setting the [`allowScrolling`](https://help.syncfusion.com/api/js/ejgrid#members:allowscrolling "allowScrolling") as `true`. The height and width can be set to grid by using the properties [`scrollSettings.height`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-height "scrollSettings.height") and [`scrollSettings.width`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-width "scrollSettings.width") respectively.

The height and width can be set in percentage and pixel. The default value for [`height`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-height "height") and [`width`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-width "width") in the [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") is 0 and `auto` respectively.

N> If [`width`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-width "width") and [`height`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-height "height") is not defined in the [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") property then the horizontal and vertical scrollbar is enabled, only when the grid width exceeds the browser width.

The height and width can be set in percentage and pixel. The default value for [`height`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-height "height") and [`width`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-width "width") in the [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") is 0 and `auto` respectively.

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

![Scrolling](scrolling_images/scrolling_img1.png)

## Scroller appearance customization

We can show or hide the scrollbar while focus in or focus out of the Grid using  [`autoHide`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-autohide "autoHide") property of  [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") 

The height and width of button in the scrollbar can be customized by using [`buttonSize `](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-buttonsize  "buttonSize ") property of  [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") 

To specify the scroll down pixel of mouse wheel, to scroll mouse wheel and view the grid contents use [`scrollOneStepBy  `](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-scrollonestepby  "scrollOneStepBy  ") property of  [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") 

And to specify the scroller size use  [`scrollerSize `](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-scrollersize  "scrollerSize ") property of  [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") 

N> To get the scroller object use [`getScrollObject`](https://help.syncfusion.com/api/js/ejgrid#methods:getscrollobject "getScrollObject") method.

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
		scrollSettings:{width: 600, height: 337,autoHide: true,buttonSize:35,scrollerSize:40},
        columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCity"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Appearance](scrolling_images/scrolling_img12.png)




## Set width and height in pixel 	

To specify the [`scrollSettings.width`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-width "scrollSettings.width") and [`scrollSettings.height`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-height "scrollSettings.height") in pixel, set the pixel value as integer. 

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

![In pixel](scrolling_images/scrolling_img2.png)


## Set width and height in percentage

To specify the [`scrollSettings.width`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-width "scrollSettings.width") and [`scrollSettings.height`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-height "scrollSettings.height") in percentage, set the percentage value as string.

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

![In percentage](scrolling_images/scrolling_img3.png)


## Set width as auto

Specify the [`width`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-width "width") property of [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") as auto, then the scrollbar is rendered only when the grid width exceeds the browser window width.

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

![Auto Width](scrolling_images/scrolling_img4.png)


## Frozen columns

Specify the [`frozenColumns`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-frozencolumns "frozenColumns") property of [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") to freeze the columns (upto the specified frozenColumns value) at the time of scrolling. Horizontal scrollbar must be enabled while specifying the [`frozenColumns`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-frozencolumns "frozenColumns") then only you can scroll and see the remaining columns with freeze pane.

N> The [`allowScrolling`](https://help.syncfusion.com/api/js/ejgrid#members:allowscrolling "allowScrolling") must be `true` while specifying [`frozenColumns`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-frozencolumns "frozenColumns").

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

![Frozen Columns](scrolling_images/scrolling_img5.png)


### Freeze particular columns:

To freeze selected columns in grid at the time of scrolling, set the [`isFrozen`](https://help.syncfusion.com/api/js/ejgrid#members:columns-isfrozen "isFrozen") property of columns as `true`. The [`isFrozen`](https://help.syncfusion.com/api/js/ejgrid#members:columns-isfrozen "isFrozen") columns are rendered first in the grid even if the columns index is different while declaring the [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns").

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

![Frozen Column](scrolling_images/scrolling_img6.png)


### Frozen Columns alert Messages:

1. If [`allowScrolling`](https://help.syncfusion.com/api/js/ejgrid#members:allowscrolling "allowScrolling") is false while using [`frozenColumns`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-frozencolumns "frozenColumns") then "Enable [`allowScrolling`](https://help.syncfusion.com/api/js/ejgrid#members:allowscrolling "allowScrolling") while using frozen Columns" alert message is thrown.
2. If [`frozenColumns`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-frozencolumns "frozenColumns") is specified out of the grid column view then "Frozen columns should be in grid view area" alert message is thrown.
3. Frozen Rows and Columns are not supported by the following features.
- Grouping
- Row Template
- Detail Template
- Hierarchy Grid
- Batch Editing
- Virtual Scrolling

If any one of the above feature is enabled along with Frozen Rows and Columns, then "Frozen Columns and Rows are not supported for Grouping, Row Template, Detail Template, Hierarchy Grid and Batch Editing" alert message is thrown.

## Frozen Rows

Specify the [`frozenRows`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-frozenrows "frozenRows") property of [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") to freeze rows (upto the specified frozenRows value) at the time of scrolling. Vertical scrollbar must be enabled while specifying the [`frozenRows`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-frozenrows "frozenRows") then only you can scroll and see the remaining rows with freeze pane.

N>The [`allowScrolling`](https://help.syncfusion.com/api/js/ejgrid#members:allowscrolling "allowScrolling") must be `true` while specifying [`frozenRows`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-frozenrows "frozenRows").

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

![Frozen Rows](scrolling_images/scrolling_img7.png)


N> By using [`rowHeightRefresh`](https://help.syncfusion.com/api/js/ejgrid#methods:rowheightrefresh "rowHeightRefresh") method resolves row height issue when movable and frozen content height mismatch.


## Touch scroll

In [touch](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-enabletouchscroll "touch") supported devices you can scroll and show the content by swipe left, right, top and bottom. Disable touch scroll by setting [`enableTouchScroll`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-enabletouchscroll "enableTouchScroll") property of the [`scrollSettings`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings "scrollSettings") as `false`.

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

The virtual scrolling support allows you to load data that you require (load data based on page size) without buffering the entire huge database. To enable the virtual scrolling set the  [`allowVirtualScrolling `](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-allowvirtualscrolling "allowVirtualScrolling ")   property of `scrollSettings`  as `true`. 

We also have an enhanced virtual scrolling feature with an improvised performance. To enable improvised virtual scrolling feature set the  [`enableVirtualization  `](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-enablevirtualization "enableVirtualization  ")  property of `scrollSettings` as true and it doesn't require the [`allowVirtualScrolling `](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-allowvirtualscrolling "allowVirtualScrolling ") to be enabled. It allows you to load the grid with data while scrolling. Some of the relevant functionalities of this are.

1.	White space will not be appeared in the Grid. 
2.	Improved page rendering performance. 
3.  It can render nearly 500 thousand records.

It supports two mode of virtualization. They are,

1. Normal Mode
2. Infinite or Continuous Mode

N> Enhanced Virtual Scrolling supports only Normal mode
N> The following features are not supported by virtual scrolling 
N> 1. Grouping
N> 2. Frozen Rows 
N> 3. Cell merging 
N> 4. Detail template 
N> 5. Hierarchy
N> 6. Editing

### Normal Mode:

It allows you to load the grid with data while scrolling. This can be achieved by setting the [`virtualScrollMode`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-virtualscrollmode "virtualScrollMode") as `normal`.

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

![Normal Mode](scrolling_images/scrolling_img8.png)

#### Enhanced Virtual Scrolling:

In order to enable this, you need to set the  [`enableVirtualization  `](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-enablevirtualization "enableVirtualization  ") property of the `scrollSettings` as true. 

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

![Enhanced VirtualScroll](scrolling_images/scrolling_img10.png)


### Infinite or Continuous Mode:

In Infinite or Continuous mode, the data is loaded in grid when the scrollbar reaches the end.  You can enable the continuous mode by setting the [`virtualScrollMode`](https://help.syncfusion.com/api/js/ejgrid#members:scrollsettings-virtualscrollmode "virtualScrollMode") property as `continuous`.

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

![Infinite Mode](scrolling_images/scrolling_img9.png)
