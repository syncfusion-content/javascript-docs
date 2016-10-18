---
layout: post
title: Cells with Grid widget for Syncfusion Essential JS
description: How to define the cells and its features
platform: js
control: ejGrid
documentation: ug
--- 
# Cell

## Auto wrap 

Auto wrap enables the Grid to wrap cell content or header content to next line when the content exceeds the boundary of the cell width. To enable auto wrap, set [`allowTextWrap`](http://help.syncfusion.com/api/js/ejgrid#members:allowtextwrap "allowTextWrap") property as `true`. 

We can specify the mode of auto wrap using [`wrapMode`](http://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings-wrapmode "wrapMode") property of the [`textWrapSettings`](http://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings "textWrapSettings"). 

Three types of wrapMode are available and they are,
  
 1. Both
 2. Header
 3. Content 
 
N> 1. By default the [`wrapMode`](http://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings-wrapmode "wrapMode") will be set as `both`. 

N> 2. While using [`textWrapSettings`](http://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings "textWrapSettings") then it is must to set [`allowTextWrap`](http://help.syncfusion.com/api/js/ejgrid#members:allowtextwrap "allowTextWrap") as `true`.

N> 3. For [`wrapMode`](http://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings-wrapmode "wrapMode") property you can assign either `string` value (`both`) or `enum` value (`ej.Grid.WrapMode.Both`).
 
## Both

When [`wrapMode`](http://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings-wrapmode "wrapMode") of [`textWrapSettings`](http://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings "textWrapSettings") property set as `both` then the auto wrap will be enable for both grid content and header. 

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
		allowTextWrap : true,
		textWrapSettings: {wrapMode: "both"},
		columns : [
			{ field: "OrderID", width: 100 },
			{ field: "EmployeeID", width: 100 },
			{ field: "Freight", width: 100 },
			{ field: "ShipCity", width: 150 },
			{ field: "ShipAddress",headerText:"Ship Address", width: 200 }
		]
	});
	});

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img1.png)

## Header

When [`wrapMode`](http://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings-wrapmode "wrapMode") of [`textWrapSettings`](http://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings "textWrapSettings") property set as `header` then the auto wrap will be enable only for grid header alone. 

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
		allowTextWrap : true,
		textWrapSettings: {wrapMode: "header"},
		columns : [
			{ field: "OrderID", width: 100 },
			{ field: "EmployeeID", width: 100 },
			{ field: "Freight", width: 100 },
			{ field: "ShipCity", width: 150 },
			{ field: "ShipAddress",headerText:"Ship Address", width: 200 }
		]
	});
	});
	
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img1_1.png)

## Content

When [`wrapMode`](http://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings-wrapmode "wrapMode") of [`textWrapSettings`](http://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings "textWrapSettings") property set as `content` then the auto wrap will be enable only for grid content alone. 

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
		allowTextWrap : true,
		textWrapSettings: {wrapMode: "content"},
		columns : [
			{ field: "OrderID", width: 100 },
			{ field: "EmployeeID", width: 100 },
			{ field: "Freight", width: 100 },
			{ field: "ShipCity", width: 150 },
			{ field: "ShipAddress",headerText:"Ship Address", width: 200 }
		]
	});
	});
	
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img1_2.png)

## Cell Merging

The Grid has options to merge the Grid cells based on the required conditions. This can be enabled by setting [`allowCellMerging`](http://help.syncfusion.com/api/js/ejgrid#members:allowcellmerging "allowCellMerging") property as `true` and the merge conditions can be defined in [`mergeCellInfo`](http://help.syncfusion.com/api/js/ejgrid#events:mergecellinfo "mergeCellInfo") event. In this event, you can get the column details and data of that particular row and column which is helpful in defining conditions. 

You can merge the rows and cells of grid, using `rowMerge`, `colMerge` and `merge` functions available in [`mergeCellInfo`](http://help.syncfusion.com/api/js/ejgrid#events:mergecellinfo "mergeCellInfo") event's argument.

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
		allowCellMerging : true,
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"],
		mergeCellInfo : function (args) {
			if (args.column.field == "EmployeeID" && args.data.OrderID == 10248)
				args.rowMerge(3);
			else if (args.column.field == "ShipCity" && args.data.OrderID == 10252)
				args.colMerge(3);
			else if (args.column.field == "ShipCity" && args.data.OrderID == 10255)
				args.merge(0, 3);
		}
	});
});
{% endhighlight %}



The following output is displayed as a result of the above code example.

![](Cell_images/cell_img2.png)


## Custom Attribute

You can add [custom attribute](http://help.syncfusion.com/api/js/ejgrid#members:columns-customattributes "custom attribute") for particular column `td` element by using [`customAttributes`](http://help.syncfusion.com/api/js/ejgrid#members:columns-customattributes "customAttributes") property of the column.

Based on custom attribute you can customize the style and appearance of the `td` element or handling jQuery functionalities. 

You can use JsRender syntax in the template.For more information about JsRender syntax, please refer [the link](http://www.jsviews.com/#jsrapi "the link").

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
		columns : [
			{ field: "OrderID" },
			{ field: "CustomerID" },
			{ field: "EmployeeID"}, // jsrender syntax usage in custom Attribute
			{ field: "ShipCity", customAttributes: { "title": "{{"{{"}}:shipcity {{}}}}" } },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img3.png)


## Displaying HTML content

This will helps you to show actual [HTML](http://help.syncfusion.com/api/js/ejgrid#members:columns-disablehtmlencode "HTML") value in grid content and header. To disable HTML code, set [`disableHtmlEncode`](http://help.syncfusion.com/api/js/ejgrid#members:columns-disablehtmlencode "disableHtmlEncode") property of [`columns`](http://help.syncfusion.com/api/js/ejgrid#members:columns "columns") as true. 

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
		columns : [
			{ field: "OrderID" },
			{ field: "CustomerID", headerText: "<div>Cust ID</div>", disableHtmlEncode: true },
			{ field: "EmployeeID", headerText: "<div>Employee ID</div>", disableHtmlEncode: false },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img4.png)


## Tooltip

When you move the cursor over the particular cell it provides an information about the corresponding cell value.

**Template**

HTML templates can be specified in the `tooltip` property of the particular column cell as a string (HTML element) or ID of the template's HTML element.You can use JsRender syntax in the template. For more information about JsRender syntax, please refer [this link](http://www.jsviews.com/#jsrapi "this link"). 

N> It's a standard way to enclose the template within the `script` tag with `type` as "text/x-jsrender".
 
N> The `tooltip` template must contain `value` property to bind the corresponding cell text in tooltip
 
The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script type="text/template" id="colTip">
 {{"{{"}}:value {{}}}}  
</script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field: "OrderID" },
			{ field: "EmployeeID"},
			{ field: "ShipCity", tooltip: "#colTip"},
			{ field: "Freight"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img5.png)

## ClipMode

When the cell value contains a long text that is not fit into the grid column cell, the `clipMode` property is used. By using the `clipMode`, the cell value will be displayed with ellipsis or with clipped content when the text overflows inside a column cell.

N> 1. By default the `clipMode` will be set as `clip`. 
N> 2. For [`clipMode`] property you can assign either `string` value (`ellipsis`)  or `enum` value (`ej.Grid.ClipMode.Ellipsis`).


**List of Enumeration types**
  
 1. Clip
 2. Ellipsis
 3. EllipsisWithTooltip 
 
### Clip

When the content overflows, the remaining content will be hidden in the particular cell

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
		columns : [
			{ field: "OrderID" },
			{ field: "ShipCity"},
			{ field: "ShipName", clipMode: ej.Grid.ClipMode.Clip},
			{ field: "Freight"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img6.png)
 
### Ellipsis

Ellipsis will be displayed when the content overflows its column width. Here tooltip will not be shown for corresponding columns.

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
		columns : [
			{ field: "OrderID" },
			{ field: "ShipCity"},
			{ field: "ShipName", clipMode: ej.Grid.ClipMode.Ellipsis},
			{ field: "Freight"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img7.png)

### Ellipsis With Tooltip

Ellipsis will be displayed when the content overflows its column width. Here tooltip will be shown only for the corresponding column cells that shows ellipsis.

N> If `clipMode` is set as `EllipsisWithTooltip`, then `tooltip` must be given.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script type="text/template" id="colTip">
 {{"{{"}}:value {{}}}}  
 </script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : [
			{ field: "OrderID" },
			{ field: "ShipCity"},
			{ field: "ShipName",tooltip:"#colTip", clipMode: ej.Grid.ClipMode.EllipsisWithTooltip},
			{ field: "Freight"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cell_images/cell_img8.png)



