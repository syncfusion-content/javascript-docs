
---
layout: post
title: Context Menu
description: Context Menu
platform: js
control: Grid
documentation: ug
---
# Context Menu

Context menu is used to improve user action with Grid using popup menu. It can be shown by defining [`contextMenuSettings.enableContextMenu`](http://help.syncfusion.com/js/api/ejgrid#members:contextmenusettings-enablecontextmenu "contextMenuSettings.enableContextMenu") as true. Context menu has option to add default items in [`contextMenuSettings.contextMenuItems`](http://help.syncfusion.com/js/api/ejgrid#members:contextmenusettings-contextmenuitems "contextMenuSettings.contextMenuItems") and customized items in [`contextMenuSettings.customContextMenuItems`](http://help.syncfusion.com/js/api/ejgrid#members:contextmenusettings-customcontextmenuitems "contextMenuSettings.customContextMenuItems").

## Default Context Menu items

Please find the below table for default context menu items and its actions.

<table>
<tr>
<td>
Section<br/><br/></td><td>
Context menu items<br/><br/></td><td>
Action<br/><br/></td></tr>
<tr>
<td>
Header <br/><br/></td><td>
Sort in Ascending Order<br/><br/></td><td>
Sort column in Ascending order<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Sort in Descending Order<br/><br/></td><td>
Sort column in Descending order<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Group<br/><br/></td><td>
Group the current column<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Ungroup<br/><br/></td><td>
Ungroup the current column if already grouped<br/><br/></td></tr>
<tr>
<td>
Body<br/><br/></td><td>
Add Record<br/><br/></td><td>
Start Add new record<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Edit Record<br/><br/></td><td>
Start Edit in current record<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Delete Record<br/><br/></td><td>
Delete the current record<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Save<br/><br/></td><td>
Save the record if Add/Edit record is started<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Cancel<br/><br/></td><td>
Cancel Added/Edited state<br/><br/></td></tr>
<tr>
<td>
Pager<br/><br/></td><td>
Next Page<br/><br/></td><td>
Go to Next Page<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Last Page<br/><br/></td><td>
Go to Last page<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Previous page<br/><br/></td><td>
Go to previous page<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
First page<br/><br/></td><td>
Go to first page<br/><br/></td></tr>
</table>


{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({

// the datasource "window.gridData" is referred from jsondata.min.js
	dataSource: window.gridData,
	contextMenuSettings: {enableContextMenu: true},
	allowPaging: true,
	allowSorting: true,
	allowGrouping: true,
	pageSettings: {	pageCount: 5},
	editSettings: {allowEditing: true,allowAdding: true,allowDeleting: true,},
	columns: 
		[
			{field: "OrderID",isPrimaryKey: true,headerText: 'Order ID',textAlign: ej.TextAlign.Right,width: 90},
			{field: "CustomerID",headerText: 'Customer ID',width: 90},
			{field: "EmployeeID",headerText: 'Employee ID',editType: ej.Grid.EditingType.Dropdown,textAlign: ej.TextAlign.Right,width: 90},
			{field: "Freight",headerText: 'Freight',textAlign: ej.TextAlign.Right,width: 80,format: "{0:C}"},
			{field: "ShipName",headerText: 'Ship Name',width: 150,}
		]

});

</script>



{% endhighlight %}

![](ContextMenu_images/ContextMenu_img1.png)
{:catption}

Contextmenu at header

![](ContextMenu_images/ContextMenu_img2.png)
{:catption}

Contextmenu at body

![](ContextMenu_images/ContextMenu_img3.png)
{:caption}

Contextmenu at pager

I>[`allowGrouping`, `allowSorting` should be enabled to perform default context menu actions in Grid header. `allowEditing`, `allowDeleting` and `allowAdding` should be enabled to perform default actions in body. ]____

## Custom Context Menu

Custom context menu is used to create your own menu item and its action. To add customized context menu items, you need to use [`toolbarSettings.customToolbarItems`](http://help.syncfusion.com/js/api/ejgrid#members:toolbarsettings-customtoolbaritems "") and bind Actions for this customized context menu in `contextClick` event.


{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$("#Grid").ejGrid({

// the datasource "window.gridData" is referred from jsondata.min.js

	dataSource: window.gridData,
	contextClick: function (args) {
		if (args.text == "Clear Selection")
			this.clearSelection();
		},
	contextMenuSettings: {enableContextMenu: true,contextMenuItems: [],customContextMenuItems: ["Clear Selection"]},
	allowPaging: true,
	columns: [
		{field: "OrderID",headerText: 'Order ID',textAlign: ej.TextAlign.Right,width: 90},
		{field: "CustomerID",headerText: 'Customer ID',width: 90},
		{field: "EmployeeID",headerText: 'Employee ID',textAlign: ej.TextAlign.Right,width: 90},
		{field: "Freight",headerText: 'Freight',textAlign: ej.TextAlign.Right,width: 80,format: "{0:C}"},
		{field: "ShipCountry",headerText: 'Ship Country',width: 90,}
		]

});

</script>



{% endhighlight %}


![](ContextMenu_images/ContextMenu_img4.png)


