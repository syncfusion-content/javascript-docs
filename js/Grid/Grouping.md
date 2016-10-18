---
layout: post
title: Grouping with Grid widget for Syncfusion Essential JS
description: How to enable grouping and its functionalities
platform: js
control: Grid
documentation: ug
--- 
# Grouping

The Grid control has options to group the records based on the required column. When grouping is applied, grouped records are organized into a hierarchical structure to facilitate easier expand and collapse of records. To enable grouping, set [`allowGrouping`](http://help.syncfusion.com/api/js/ejgrid#members:allowgrouping "allowGrouping") property as `true`.

Columns can be grouped by simply dragging the column header and drop on the group drop area or simply click the group button which is displayed in the column. By default, sorting is done while grouping the column.

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
		allowGrouping : true,
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img1.png)


## Initial Grouping

While initializing the grid itself, there is an option to group the column and display it in a hierarchical structure. To enable initial grouping, set array of column's [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name to be grouped to [`groupSettings.groupedColumns`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings-groupedcolumns "groupSettings.groupedColumns") property. Define the [`field`](http://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name in the array format.

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
		allowGrouping : true,
		groupSettings: { groupedColumns: ["ShipCountry"] },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img2.png)


## Multi-Column Grouping

Group multiple columns by simply drag and drop the columns one by one from column header into group drop area.

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
		allowGrouping : true,
		// More than one column is grouped while initializing the grid itself.
		groupSettings: { groupedColumns: ["ShipCountry", "CustomerID"] },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img3.png)


## Group buttons

To do grouping easily without doing drag and drop column header by setting [`showToggleButton`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings-showtogglebutton "showToggleButton") property of [`groupSettings`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `true`.

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
		allowGrouping : true,
		groupSettings: { showToggleButton: true },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img4.png)


## Hide Ungroup button

Hide ungroup button from grouped columns which is in the group drop area by setting the [`showUngroupButton`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings-showungroupbutton "showUngroupButton") property of [`groupSettings`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `false`.

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
		allowGrouping : true,
		groupSettings: { showUngroupButton: false },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img5.png)


## Hide Grouped Column

While grouping a particular column, there is an option to hide the grouped columns from grid. To enable hide grouped column option, set [`showGroupedColumn`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings-showgroupedcolumn "showGroupedColumn") property of [`groupSettings`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `false`.

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
		allowGrouping : true,
		groupSettings: { showGroupedColumn: false },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img6.png)


## AutoSize Drop Area

Drag any column header and move it to the group drop area, then its portion expands smoothly. Stop this animation by setting [`enableDropAreaAutoSizing`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings-enabledropareaautosizing "enableDropAreaAutoSizing") property of [`groupSettings`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `false`.

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
		allowGrouping : true,
		groupSettings: { enableDropAreaAutoSizing: false },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img7.png)


## Hide Drop area

To avoid ungrouping or further grouping of a column after an initial column grouping by setting [`showDropArea`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings-showdroparea "showDropArea") property of [`groupSettings`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `false`.

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
		allowGrouping : true,
		groupSettings: { showDropArea: false, groupedColumns: ["ShipCountry"] },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img8.png)


## Group Caption Format / Group Caption Template

Using [`captionFormat`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings-captionformat "captionFormat") property of [`groupSettings`](http://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") you can render any type of JsRender templates or customizing the group caption text. 

You can use JsRender syntax in the template.For more information about JsRender syntax, please refer [the link](http://www.jsviews.com/#jsrapi "the link").

N> 1. It's a standard way to enclose the `template` within the `script` tag with `type` as "text/x-jsrender". 
N> 2. Using locale property of `GroupCaptionFormat`, you can only customize the default group caption text.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="template" type="text/x-jsrender">
{{"{{"}}:field{{}}}} - {{"{{"}}:key{{}}}}
<button id="btn{{"{{"}}:field{{}}}}{{"{{"}}:key{{}}}}" class="btn">Collapse</button>
</script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"],
		allowGrouping : true,
		groupSettings: { captionFormat: "#template" },
		actionComplete : function (args) {
			$(".btn").ejButton({
				click : "btnClick"
			});
		}
	});
});

function btnClick(args) {
	var gridObj = $("#Grid").data("ejGrid");
	gridObj.expandCollapse(this.element.parent().prev());
	$("#" + this._id).ejButton("model.text", args.model.text == "Collapse" ? "Expand" : "Collapse");
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img9.png)


![](Grouping_images/Grouping_img10.png)


