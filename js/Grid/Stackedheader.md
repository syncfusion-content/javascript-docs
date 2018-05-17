---
layout: post
title: Stacked Headers with Grid widget for Syncfusion Essential JS
description: How to stack column Header and customize it
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Stacked Headers

The stacked headers helps you to group the logical columns in the Grid. It can be shown by setting the [`showStackedHeader`](https://help.syncfusion.com/api/js/ejgrid#members:showstackedheader "showStackedHeader") as `true` and by defining the [`stackedHeaderRows`](https://help.syncfusion.com/api/js/ejgrid#members:stackedheaderrows "stackedHeaderRows").

## Adding stacked header columns

To stack columns in stacked header, you need to define the [`column`](https://help.syncfusion.com/api/js/ejgrid#members:stackedheaderrows-stackedheadercolumns-column "column") property in the [`stackedHeaderColumns`](https://help.syncfusion.com/api/js/ejgrid#members:stackedheaderrows-stackedheadercolumns "stackedHeaderColumns") with field names of visible columns.

You can also define the [`cssClass`](https://help.syncfusion.com/api/js/ejgrid#members:stackedheaderrows-stackedheadercolumns-cssclass "cssClass"),  [`headerText `](https://help.syncfusion.com/api/js/ejgrid#members:stackedheaderrows-stackedheadercolumns-headertext  "headerText "), [`textAlign `](https://help.syncfusion.com/api/js/ejgrid#members:stackedheaderrows-stackedheadercolumns-textalign "textAlign  ") and [`tooltip `](https://help.syncfusion.com/api/js/ejgrid#members:stackedheaderrows-stackedheadercolumns-tooltip "tooltip ") properties in the [`stackedHeaderColumns`](https://help.syncfusion.com/api/js/ejgrid#members:stackedheaderrows-stackedheadercolumns "stackedHeaderColumns") .

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
