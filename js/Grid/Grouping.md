---
layout: post
title: Grouping with Grid widget for Syncfusion Essential JS
description: How to enable grouping and its functionalities
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Grouping

The Grid control has options to group the records based on the required column. When grouping is applied, grouped records are organized into a hierarchical structure to facilitate easier expand and collapse of records. To enable grouping, set [`allowGrouping`](https://help.syncfusion.com/api/js/ejgrid#members:allowgrouping "allowGrouping") property as `true`.

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

While initializing the grid itself, there is an option to group the column and display it in a hierarchical structure. To enable initial grouping, set array of column's [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name to be grouped to [`groupSettings.groupedColumns`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings-groupedcolumns "groupSettings.groupedColumns") property. Define the [`field`](https://help.syncfusion.com/api/js/ejgrid#members:columns-field "field") name in the array format.

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

To do grouping easily without doing drag and drop column header by setting [`showToggleButton`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings-showtogglebutton "showToggleButton") property of [`groupSettings`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `true`.

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

Hide ungroup button from grouped columns which is in the group drop area by setting the [`showUngroupButton`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings-showungroupbutton "showUngroupButton") property of [`groupSettings`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `false`.

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

While grouping a particular column, there is an option to hide the grouped columns from grid. To enable hide grouped column option, set [`showGroupedColumn`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings-showgroupedcolumn "showGroupedColumn") property of [`groupSettings`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `false`.

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

Drag any column header and move it to the group drop area, then its portion expands smoothly. Stop this animation by setting [`enableDropAreaAutoSizing`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings-enabledropareaautosizing "enableDropAreaAutoSizing") property of [`groupSettings`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `false`.

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

To avoid ungrouping or further grouping of a column after an initial column grouping by setting [`showDropArea`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings-showdroparea "showDropArea") property of [`groupSettings`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") as `false`.

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

Using [`captionFormat`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings-captionformat "captionFormat") property of [`groupSettings`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings "groupSettings") you can render any type of JsRender templates or customizing the group caption text. 

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


### Perform Grouping by External Action:-

To control the grid Group actions externally use the following methods,

1.[`groupColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:groupcolumn "groupColumn")

2.[`ungroupColumn`](https://help.syncfusion.com/api/js/ejgrid#methods:ungroupcolumn "removeSortedColumns")

3.[`expandGroupDropArea`](https://help.syncfusion.com/api/js/ejgrid#methods:expandgroupdroparea "expandGroupDropArea")

3.[`collapseGroupDropArea`](https://help.syncfusion.com/api/js/ejgrid#methods:collapsegroupdroparea "collapseGroupDropArea")

The following code example describes the above behavior.

{% highlight html %}
 <button id="groupColumn" style="width: 100px">GroupColumn</button>
 <button id="ungroupColumn" style="width: 100px">unGroupColumn</button>
 <button id="ExpandArea" style="width: 100px">ExpandGroupDropArea</button>
 <button id="collapseArea" style="width: 100px">CollapseGroupDropArea</button>
 <div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
                $("#Grid").ejGrid({
                    // the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js' 
                    dataSource: window.gridData,
                    allowPaging: true,
                    allowGrouping:true,
                    columns: [
                                  { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
                                  { field: "CustomerID", headerText: "Customer ID", width: 90 },
                                  { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                                  { field: "ShipCountry", headerText: "Ship Country", width: 110 }
                    ],
                });
                 $("#groupColumn,#ungroupColumn").ejButton({ "click": "groupColumn", width: "100" });
	               $("#expandArea,#collapseArea").ejButton({ "click": "DropArea", width: "160" });
        });
            function groupColumn(args){
               var gridObj = $("#Grid").ejGrid("instance");
		              if (this.element.attr("id") == "groupColumn") {
		                 gridObj.groupColumn("OrderID");
                   }
                  else 
                     gridObj.ungroupColumn("OrderID"); 
              }
            function DropArea(args){
		          var gridObj = $("#Grid").ejGrid("instance");
		             if (this.element.attr("id") == "expandArea") {
		               gridObj.expandGroupDropArea(); 
                   }
		            else
		               gridObj.collapseGroupDropArea(); 
            }
{% endhighlight %}

The following output is displayed as a result of the previous code example.

![](Grouping_images/Grouping_img11.png)

## Handling grouped records count in server-side    

When binding remote data to grid with on-demand data loading, only current page data knowledge is available to grid and so grouped records count would be shown based on current Page only. 

This can be rectified when binding data to grid using [UrlAdaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#url-adaptor) of DataManager. The grouped column values should be passed into the `groupDs` property of return object from server-side along with datasource and count.

The following code example describes the above behavior.

{% tabs %}
 
{% highlight html %}
 <div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
                $("#Grid").ejGrid({
                    dataSource: ej.DataManager({
			                  url:"/Grid/UrlDataSource",
			                  adaptor: new ej.UrlAdaptor()
                		});,
                    allowPaging: true,
                    allowSorting: true,
                    allowGrouping:true,
                    groupSettings: { groupedColumns: ["EmployeeID"] },
                    columns: [
                                  { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 80 },
                                  { field: "CustomerID", headerText: "Customer ID", width: 90 },
                                  { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 90 },
                                  { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                                  { field: "OrderDate", headerText: "Order Date", textAlign: ej.TextAlign.Right, width: 75, format: "{0:MM/dd/yyyy}"}
                    ],
                });
                
        });
           
{% endhighlight %}

{% highlight c# %}

    namespace MVCSampleBrowser.Controllers
        {
            public class GridController : Controller
              { 
                public ActionResult GridFeatures()
                 {
                   var DataSource = new NorthwindDataContext().OrdersViews.ToList();
                   ViewBag.DataSource = DataSource;
                   return View();
                 }
                public ActionResult UrlDataSource(DataManager value)
                 {
                    IEnumerable DataSource = new NorthwindDataContext().OrdersViews.ToList();
                    int count = DataSource.AsQueryable().Count();
                    IEnumerable GroupDs = new List<object>(); ;
                    DataOperations operations = new DataOperations();
                    List<string> str = new List<string>();
                    if (value.Group != null)
                        GroupDs = operations.PerformSelect(DataSource, value.Group); //Pass grouped column records
                    if (value.Sorted != null)
                        DataSource = operations.PerformSorting(DataSource, value.Sorted);
                    DataSource = operations.PerformSkip(DataSource, value.Skip);
                    DataSource = DataSource.AsQueryable().Take(value.Take);
                    return Json(new {result = DataSource, count =count, groupDs = GroupDs }, JsonRequestBehavior.AllowGet);
                 }  
             }     
        } 
{% endhighlight  %}   
{% endtabs %}  

The following output is displayed as a result of the above code example.

![](Grouping_images/Grouping_img12.png)