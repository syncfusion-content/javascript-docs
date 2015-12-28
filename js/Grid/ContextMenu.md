---
layout: post
title: Context Menu with Grid widget for Syncfusion Essential JS
description: How to enable contextMenu and its functionalities  
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
            <th>
                Section
            </th>
            <th>
                Context menu items
            </th>
            <th>
                Action
            </th>
        </tr>
        <tr>
            <td rowspan="4">
                Header
            </td>
            <td>
                Sort in Ascending Order
            </td>
            <td>
                Sort column in Ascending order
            </td>
        </tr>
        <tr>
            <td>
                Sort in Descending Order
            </td>
            <td>
                Sort column in Descending order
            </td>
        </tr>
        <tr>
            <td>
                Group
            </td>
            <td>
                Group the current column
            </td>
        </tr>
        <tr>
            <td>
                Ungroup
            </td>
            <td>
                Ungroup the current column if already grouped
            </td>
        </tr>
        <tr>
            <td rowspan="5">
                Body
            </td>
            <td>
                Add Record
            </td>
            <td>
                Start Add new record
            </td>
        </tr>
        <tr>
            <td>
                Edit Record
            </td>
            <td>
                Start Edit in current record
            </td>
        </tr>
        <tr>
            <td>
                Delete Record
            </td>
            <td>
                Delete the current record
            </td>
        </tr>
        <tr>
            <td>
                Save
            </td>
            <td>
                Save the record if Add/Edit record is started
            </td>
        </tr>
        <tr>
            <td>
                Cancel
            </td>
            <td>
                Cancel Added/Edited state
            </td>
        </tr>
        <tr>
            <td rowspan="4">
                Pager
            </td>
            <td>
                Next Page
            </td>
            <td>
                Go to Next Page
            </td>
        </tr>
        <tr>            
            <td>
                Last Page
            </td>
            <td>
                Go to Last page
            </td>
        </tr>
        <tr>
            <td>
                Previous page
            </td>
            <td>
                Go to previous page
            </td>
        </tr>
        <tr>
            <td>
                First page
            </td>
            <td>
                Go to first page
            </td>
        </tr>
    </table>


{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

 $("#Grid").ejGrid({
            // the datasource "window.gridData" is referred from jsondata.min.js
            dataSource: window.gridData,
            contextMenuSettings: { enableContextMenu: true },
            allowPaging: true,
            allowSorting: true,
            allowGrouping: true,
            pageSettings: { pageCount: 5 },
            editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true, },
            columns:
                [
                    { field: "OrderID", isPrimaryKey: true, headerText: 'Order ID', textAlign: ej.TextAlign.Right, width: 90 },
                    { field: "CustomerID", headerText: 'Customer ID', width: 90 },
                    { field: "EmployeeID", headerText: 'Employee ID', textAlign: ej.TextAlign.Right, width: 90 },
                    { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, width: 80, format: "{0:C}" },
                    { field: "ShipName", headerText: 'Ship Name', width: 150, }
                ]
 });

</script>

{% endhighlight %}

![](Context-Menu_images/ContextMenu_img1.png)
{:catption}

Contextmenu at header

![](Context-Menu_images/ContextMenu_img2.png)
{:catption}

Contextmenu at body

![](Context-Menu_images/ContextMenu_img3.png)
{:caption}

Contextmenu at pager

N> `allowGrouping`, `allowSorting` should be enabled to perform default context menu actions in Grid header. `allowEditing`, `allowDeleting` and `allowAdding` should be enabled to perform default actions in body.

## Custom Context Menu

Custom context menu is used to create your own menu item and its action. To add customized context menu items, you need to use [`contextMenuSettings.customContextMenuItems`](http://help.syncfusion.com/js/api/ejgrid#members:contextmenusettings-customcontextmenuitems "contextMenuSettings.customContextMenuItems") property and to bind required actions for this, use [`contextClick`](http://help.syncfusion.com/js/api/ejgrid#events:contextclick "contextClick") event.


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
            contextMenuSettings: { enableContextMenu: true, contextMenuItems: [], customContextMenuItems: ["Clear Selection"] },
            allowPaging: true,
            columns: [
                { field: "OrderID", headerText: 'Order ID', textAlign: ej.TextAlign.Right, width: 90 },
                { field: "CustomerID", headerText: 'Customer ID', width: 90 },
                { field: "EmployeeID", headerText: 'Employee ID', textAlign: ej.TextAlign.Right, width: 90 },
                { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, width: 80, format: "{0:C}" },
                { field: "ShipCountry", headerText: 'Ship Country', width: 90 }
            ]
 });

</script>

{% endhighlight %}


![](Context-Menu_images/ContextMenu_img4.png)


