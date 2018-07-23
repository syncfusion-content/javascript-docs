---
layout: post
title: Web Accessibility with Grid widget for Syncfusion Essential JS
description: Web accessibilties standard used in ejGrid
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Web Accessibility

Web Accessibility is achieved in the Grid control through Keyboard Navigation and WAI-ARIA Standard. 

## Keyboard Navigation

Supported Keyboard Interactions keys with its description and its corresponding Grid [`keySettings`](https://help.syncfusion.com/api/js/ejgrid#members:keysettings) properties are tabulated as follows.

<table>
<tr>
<th>
Interaction Keys</th><th>
Description</th><th>
KeySettings Property</th></tr>
<tr>
<td>
Alt + j</td><td>
Focus the Grid</td></tr>
<tr>
<td>
Insert</td><td>
Insert record in Grid</td><td>
insertRecord</td></tr>
<tr>
<td>
Delete</td><td>
Delete record in Grid</td><td>
deleteRecord</td></tr>
<tr>
<td>
F2</td><td>
Edit record in Grid</td><td>
editRecord</td></tr>
<tr>
<td>
Enter </td><td>
Save edited or added </td><td>
saveRequest</td></tr>
<tr>
<td>
Esc</td><td>
Cancel add or edit state</td><td>
cancelRequest</td></tr>
<tr>
<td>
PgDn</td><td>
Go to next Page</td><td>
nextPage</td></tr>
<tr>
<td>
PgUp</td><td>
Go to previous Page</td><td>
previousPage</td></tr>
<tr>
<td>
Ctrl +Alt +PgDn</td><td>
Go to last page</td><td>
lastPage</td></tr>
<tr>
<td>
Ctrl + Alt + PgUp</td><td>
Go to first page </td><td>
firstPage</td></tr>
<tr>
<td>
Alt + PgDown</td><td>
Go to next Pager</td><td>
nextPager</td></tr>
<tr>
<td>
Alt + PgUp</td><td>
Go to previous Pager</td><td>
previousPager</td></tr>
<tr>
<td>
Home</td><td>
Go to first cell</td><td>
firstCellSelection</td></tr>
<tr>
<td>
End</td><td>
Go to last cell</td><td>
lastCellSelection</td></tr>
<tr>
<td>
Ctrl + Home</td><td>
Go to first row</td><td>
firstRowSelection</td></tr>
<tr>
<td>
Ctrl + End</td><td>
Go to last row</td><td>
lastRowSelection</td></tr>
<tr>
<td>
Up arrow</td><td>
Move to up cell selection</td><td>
upArrow</td></tr>
<tr>
<td>
Down arrow</td><td>
Move to down cell selection</td><td>
downArrow</td></tr>
<tr>
<td>
Right arrow</td><td>
Move to right cell selection</td><td>
rightArrow</td></tr>
<tr>
<td>
Left arrow</td><td>
Move to left cell selection</td><td>
leftArrow</td></tr>
<tr>
<td>
Shift + Up arrow</td><td>
Select cells or rows from current cell to its top cell</td><td>
multiSelectionByUpArrow</td></tr>
<tr>
<td>
Shift + Down arrow</td><td>
Select cells or rows from current cell to its down cell</td><td>
multiSelectionByDownArrow</td></tr>
<tr>
<td>
Shift + Left arrow</td><td>
Select cells from current cell to its left cell</td><td>
multiSelectionByLeftArrow</td></tr>
<tr>
<td>
Shift + Right arrow</td><td>
Select cells from current cell to its Right cell</td><td>
multiSelectionByRightArrow</td></tr>
<tr>
<td>
Tab</td><td>
Go to next cell</td><td>
moveCellRight</td></tr>
<tr>
<td>
Shift + tab</td><td>
Go to previous cell</td><td>
moveCellLeft</td></tr>
<tr>
<td>
Alt + DownArrow</td><td>
Expand selected group</td><td>
selectedGroupExpand</td></tr>
<tr>
<td>
Ctrl + DownArrow</td><td>
Expand All visible groups</td><td>
totalGroupExpand</td></tr>
<tr>
<td>
Alt + UpArrow</td><td>
Collapse selected group</td><td>
selectedGroupCollapse</td></tr>
<tr>
<td>
Ctrl + UpArrow</td><td>
Collapse All visible groups</td><td>
totalGroupCollapse</td></tr>
</table>

To change the keyboard interaction keys for the grid actions mentioned in above table, modify the corresponding properties of Grid [`keySettings`](https://help.syncfusion.com/api/js/ejgrid#members:keysettings).

The default key for moving to next page in grid is "PageDown" key and in the following code example, we have changed it to "Right Arrow".

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		keySettings: {
                 nextPage: "39", previousPage: "37"
        },
		allowPaging : true,
		columns : [
					{ field: "OrderID"},
					{ field: "CustomerID" },
					{ field: "EmployeeID" },
					{ field: "ShipCity" },
					{ field: "ShipCountry" }
				]
	});
});
{% endhighlight %}


## WAI - ARIA

This helps in enabling better user interaction in ejGrid and uses the W3C's Widget Design specification and added customize attributes. Please find the list of ARIA attributes used.
* grid (role)
* row (role)
* gridcell (role)
* aria-selected (attribute)

