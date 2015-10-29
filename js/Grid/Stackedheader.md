---
layout: post
title: Stacked Headers
description: Stacked Headers
platform: js
control: Grid
documentation: ug
---
# Stacked Headers

The stacked headers enable you to group the logical columns in grid. It can be shown by setting [`showStackedHeader`](http://help.syncfusion.com/js/api/ejgrid#members:showstackedheader "") as `true` and by defining [`stackedHeaderRows`](http://help.syncfusion.com/js/api/ejgrid#members:stackedheaderrows "").

## Adding Stacked header columns

To stack columns in stacked header, you need to define [`column`](http://help.syncfusion.com/js/api/ejgrid#members:stackedheaderrows-stackedheadercolumns-column "") property in [`stackedHeaderColumns`](http://help.syncfusion.com/js/api/ejgrid#members:stackedheaderrows-stackedheadercolumns "") with field names of visible columns.

{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({

// the datasource "window.gridData" is referred from jsondata.min.js
	dataSource: window.gridData,
	showStackedHeader: true,
	stackedHeaderRows: [{ stackedHeaderColumns: 
		[
			{headerText: "Order Details",column: "OrderID,OrderDate,Freight"},
			{headerText: "Ship Details",column: "ShipName,ShipCity,ShipCountry"}
			]
		}],
	columns: 
	[
		{field: "OrderID",headerText: "Order ID",width: 80},
		{field: "OrderDate",headerText: "Order Date",width: 80,format: "{0:MM/dd/yyyy}",textAlign: ej.TextAlign.Right},
		{field: "Freight",width: 75,format: "{0:C}",textAlign: ej.TextAlign.Right},
		{field: "ShipName",headerText: "Ship Name",width: 110},
		{field: "ShipCity",headerText: "Ship City",width: 110},
		{field: "ShipCountry",headerText: "Ship Country",width: 110}
	]
});

</script>



{% endhighlight %}

![](Stackedheader_images/Stackedheader_img1.png)

