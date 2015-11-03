---
layout: post
title: Paging
description: paging
platform: js
control: Grid
documentation: ug
--- 

# Paging

You can display the grid records in paged view, by setting [`allowPaging`](http://help.syncfusion.com/js/api/ejgrid#members:allowpaging "allowPaging") property as `true`. 

The code snippet to enable paging is follows.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
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

You can pass the current page information as a [query](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-enablequerystring "query") string while navigating to other page. To enable query string, set the [`enableQueryString`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-enablequerystring "enableQueryString") property of [`pageSettings`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings "pageSettings") as `true`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight js %}
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

Apart from default pager, there is an option to render a specific custom [template](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-template "template") in a grid pager. To render template in pager, set [`enableTemplates`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-enabletemplates "enableTemplates") as true and [`template`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-template "template") properties of [`pageSettings`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings "pageSettings").

Prevent to show the default pager while enabling the pager [`template`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-template "template") by setting [`showDefaults`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-showdefaults "showDefaults") property of [`pageSettings`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings "pageSettings") as `false`.

N> It's a standard way to enclose the [`template`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-template "template") within the `script` tag with `type` as "text/x-jsrender".

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

{% highlight js %}
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


