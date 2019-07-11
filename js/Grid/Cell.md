---
layout: post
title: Cells with Grid widget for Syncfusion Essential JS
description: How to define the cells and its features
platform: js
control: ejGrid
documentation: ug
api: /api/js/ejgrid
--- 
# Cell

## Auto wrap 

Auto wrap enables the Grid to wrap the cell content or header content to next line when the content exceeds the boundary of the cell width. To enable auto wrap, set the  [`allowTextWrap`](https://help.syncfusion.com/api/js/ejgrid#members:allowtextwrap "allowTextWrap") property as `true`. 

We can specify the mode of auto wrap using [`wrapMode`](https://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings-wrapmode "wrapMode") property of the [`textWrapSettings`](https://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings "textWrapSettings"). 

Three types of `wrapMode` are available and they are,
  
 1. Both
 2. Header
 3. Content 
 
N> 1. By default the [`wrapMode`](https://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings-wrapmode "wrapMode") will be set as `both`. 

N> 2. While using [`textWrapSettings`](https://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings "textWrapSettings") then it is must to set [`allowTextWrap`](https://help.syncfusion.com/api/js/ejgrid#members:allowtextwrap "allowTextWrap") as `true`.

N> 3. For [`wrapMode`](https://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings-wrapmode "wrapMode") property you can assign either `string` value (`both`) or `enum` value (`ej.Grid.WrapMode.Both`).
 
## Both

When the [`wrapMode`](https://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings-wrapmode "wrapMode") of [`textWrapSettings`](https://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings "textWrapSettings") property is set as `both` then the auto wrap will be enabled for both the grid content and header.  

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

![Both Wrap Mode](Cell_images/cell_img1.png)

## Header

When the [`wrapMode`](https://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings-wrapmode "wrapMode") of [`textWrapSettings`](https://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings "textWrapSettings") property is set as `header` then the auto wrap will be enabled only for the grid header alone. 

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

![Header Wrap Mode](Cell_images/cell_img1_1.png)

## Content

When the [`wrapMode`](https://help.syncfusion.com/api/js/ejgrid#members:textWrapSettings-wrapmode "wrapMode") of [`textWrapSettings`](https://help.syncfusion.com/api/js/ejgrid#members:textwrapsettings "textWrapSettings") property is set as `content` then the auto wrap will be enable only for the grid content alone. 

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

![Content Wrap Mode](Cell_images/cell_img1_2.png)

N> By using [`getRowHeight`](https://help.syncfusion.com/api/js/ejgrid#methods:getrowheight "getRowHeight") method, you can get the row height of the Grid.

## Cell Merging

The Grid has options to merge the Grid cells based on the required conditions. This can be enabled by setting [`allowCellMerging`](https://help.syncfusion.com/api/js/ejgrid#members:allowcellmerging "allowCellMerging") property as `true` and the merge conditions can be defined in [`mergeCellInfo`](https://help.syncfusion.com/api/js/ejgrid#events:mergecellinfo "mergeCellInfo") event. In this event, you can get the column details and data of that particular row and column which is helpful in defining conditions. 

You can merge the rows and cells of grid, using `rowMerge`, `colMerge` and `merge` functions available in [`mergeCellInfo`](https://help.syncfusion.com/api/js/ejgrid#events:mergecellinfo "mergeCellInfo") event's argument.


N>  [`mergeHeaderCellInfo`](https://help.syncfusion.com/api/js/ejgrid#events:mergeheadercellinfo "mergeHeaderCellInfo") event triggered every time a request is raised while merging the header cell which contains header cell information and element.

N> The following features are not supported with Cell Merging
N> 1. Normal Mode Editing
N> 2. Inline Mode Editing
N> 3. Inline TemplateForm Mode Editing
N> 4. Grouping
N> 5. Virtual Scrolling
N> 6. Frozen Columns
N> 7. Cell Selection Modes
N> 8. Column Selection

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
			if (args.column.field == "EmployeeID" && args.rowData.OrderID == 10248)
				args.rowMerge(3);
			else if (args.column.field == "ShipCity" && args.rowData.OrderID == 10252)
				args.colMerge(3);
			else if (args.column.field == "ShipCity" && args.rowData.OrderID == 10255)
				args.merge(0, 3);
		}
	});
});
{% endhighlight %}



The following output is displayed as a result of the above code example.

![Cell Merging](Cell_images/cell_img2.png)


## Custom Attribute

You can add the [custom attribute](https://help.syncfusion.com/api/js/ejgrid#members:columns-customattributes "custom attribute") for the particular column `td` element by using the [`customAttributes`](https://help.syncfusion.com/api/js/ejgrid#members:columns-customattributes "customAttributes") property of column.

Based on custom attribute you can customize the style and appearance of the `td` element or handling jQuery functionalities. 

You can use JsRender syntax in the template.For more information about JsRender syntax, please refer to [this link](http://www.jsviews.com/#jsrapi "the link").

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
			{ field: "EmployeeID"}, // JsRender syntax usage in custom Attribute
			{ field: "ShipCity", customAttributes: { "title": "{{"{{"}}:ShipCity {{}}}}" } },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Custom Attribute](Cell_images/cell_img3.png)


## Displaying HTML content

This will helps you to show actual [HTML](https://help.syncfusion.com/api/js/ejgrid#members:columns-disablehtmlencode "HTML") value in the  grid content and header. To disable HTML code, set the [`disableHtmlEncode`](https://help.syncfusion.com/api/js/ejgrid#members:columns-disablehtmlencode "disableHtmlEncode") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") as true. 

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
			{ field: "CustomerID", headerText: "<div>Customer ID</div>", disableHtmlEncode: true },
			{ field: "EmployeeID", headerText: "<div>Employee ID</div>", disableHtmlEncode: false },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Display HTML](Cell_images/cell_img4.png)


## Tooltip

When you move the cursor over the particular cell it provides an information about the corresponding cell value.

**Template**

HTML templates can be specified in the   [tooltip ](https://help.syncfusion.com/api/js/ejgrid#members:columns-tooltip "tooltip ")  property of the particular column cell as a string (HTML element) or ID of the template's HTML element.You can use JsRender syntax in the template. For more information about JsRender syntax, please refer to [this link](http://www.jsviews.com/#jsrapi "this link"). 

N> It's a standard way to enclose the template within the `script` tag with `type` as "text/x-jsrender".

N> To modify the tooltip for the Grid column header alone, use   [headerTooltip  ](https://help.syncfusion.com/api/js/ejgrid#members:columns-headertooltip "headerTooltip  ")
 
N> The  [tooltip ](https://help.syncfusion.com/api/js/ejgrid#members:columns-tooltip "tooltip ") template must contain `value` property to bind the corresponding cell text in tooltip
 
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

![Tooltip](Cell_images/cell_img5.png)

## ClipMode

When the cell value contains a long text that will not fit into the grid column cell, the [clipMode  ](https://help.syncfusion.com/api/js/ejgrid#members:columns-clipmode "clipMode") property is used. By using the [clipMode  ](https://help.syncfusion.com/api/js/ejgrid#members:columns-clipmode "clipMode"), the cell value will be displayed with ellipsis or with clipped content when the text overflows inside a column cell.

N> 1. By default the [clipMode  ](https://help.syncfusion.com/api/js/ejgrid#members:columns-clipmode "clipMode  ") will be set as `clip`. 

N> 2. For [[clipMode  ](https://help.syncfusion.com/api/js/ejgrid#members:columns-clipmode "clipMode  ")] property you can assign either `string` value (`ellipsis`)  or `enum` value (`ej.Grid.ClipMode.Ellipsis`).


**List of Enumeration types**
  
 1. Clip
 2. Ellipsis
 3. EllipsisWithTooltip 
 
### Clip

When the content overflows, the remaining content will be hidden in the particular cell.

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

![Clip Mode](Cell_images/cell_img6.png)
 
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

![Ellipsis](Cell_images/cell_img7.png)

### Ellipsis With Tooltip

Ellipsis will be displayed when the content overflows its column width. Here the tooltip will be shown only for the corresponding column cells that shows ellipsis.

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

![Ellipsis with Tooltip](Cell_images/cell_img8.png)

