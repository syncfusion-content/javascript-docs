---
layout: post
title: Paging with Grid widget for Syncfusion Essential JS
description: How to enable paging and its functionalites.
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Paging

You can display the Grid records in paged view, by setting [`allowPaging`](https://help.syncfusion.com/api/js/ejgrid#members:allowpaging "allowPaging") property as `true`. 

The code snippet to enable paging is as follows.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](paging_images/paging_img1.png)


## Pager with query string

You can pass the current page information as a query string while navigating to other page. To enable query string, set the [`enableQueryString`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-enablequerystring "enableQueryString") property of [`pageSettings`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings "pageSettings") as `true`.

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
		pageSettings: { enableQueryString: true },
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](paging_images/paging_img2.png)


## Pager template

Apart from default pager, there is an option to render a specific custom template in a grid pager. To render template in pager, set [`enableTemplates`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-enabletemplates "enableTemplates") as true and [`template`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-template "template") properties of [`pageSettings`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings "pageSettings").

By enabling the pager [`template`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-template "template") it prevents the display of default pager elements. You can display those with pager template by setting the [`showDefaults`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-showdefaults "showDefaults") property of [`pageSettings`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings "pageSettings") as `true`.

N> It's a standard way to enclose the [`template`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-template "template") within the `script` tag with `type` as "text/x-jsrender".

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="template" type="text/x-jsrender">
<input id="currentPage" type="text" style="text-align: center; width: 32px; height: 21px; background: white;" value="1" />
<label>of 200</label>
<button id="btn">Go to</button>
</script>
{% endhighlight %}

{% highlight css %}
.e-grid .e-pager .e-pagercontainer {
	border-width: 0px;
	overflow: visible;
}
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		allowPaging : true,
		pageSettings: { enableTemplates: true, template: "#template", showDefaults: false },  
		columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"],
		create : function (args) {
			$("#btn").ejButton({
				click : "btnClick"
			});
		}
	});
});

function btnClick(args) {
	var val = $("#currentPage").val();
	var gridObj = $("#Grid").data("ejGrid");
	gridObj.gotoPage(val);
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](paging_images/paging_img3.png)


## Pager with pageSize drop down

There is an option to set the size of page by means of selecting the pageSize you wish from the options available at the dropdown in pager. To render drop down in pager, provide the pageSize values you wish to display in drop down as `array` values to [`pageSizeList`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-pagesizelist "pageSizeList") property of [`pageSettings`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings "pageSettings").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
        dataSource: window.gridData,
        allowPaging: true,
        pageSettings: { pageSize: 14, pageSizeList: [8,12,9,5] }
    });
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](paging_images/paging_img4.png)

## Pager with pageSettings

We can customize the following default  [`pageSettings`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings "pageSettings") properties of Grid control.

1. [`pageCount`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-pagecount "pageCount")
2. [`pageSize`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-pagesize "pageSize")
3. [`currentPage`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-currentpage "currentPage") 
4. [`printMode`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-printmode "printMode")   

To get the value of  total number of pages and total number of records in the grid use [`totalPages `](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-totalpages  "totalPages ") and [`totalRecordsCount `](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-totalrecordscount  "totalRecordsCount ") properties of [`pageSettings`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings "pageSettings") respectively.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
        dataSource: window.gridData,
        allowPaging: true,
        pageSettings: { pageSize: 8, pageCount:3, currentPage:2, printMode:ej.Grid.PrintMode.CurrentPage }
    });
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](paging_images/paging_img6.png)
