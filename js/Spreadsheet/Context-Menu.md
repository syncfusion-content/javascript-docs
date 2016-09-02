---
layout: post
title: Context Menu with Spreadsheet widget for Syncfusion Essential JS
description: How to use the Spreadsheet Context Menu
platform: js
control: Spreadsheet
documentation: ug
---

# Context Menu

Context Menu is used to improve user interaction with Spreadsheet. This will open when right clicking on Spreadsheet elements. You can use [`enableContextMenu`](http://help.syncfusion.com/js/api/ejspreadsheet#members:enablecontextmenu "enableContextMenu") property to enable/disable context menu. 

## Types Of Context Menu

You have following context menus in ejSpreadsheet.

* Cell Context Menu.
* Column Header Context Menu.
* Pager Context Menu.
* Row Header Context Menu.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({                                            
        enableContextMenu: true,
    });
});
{% endhighlight %}

### Cell Context Menu

The following output is displayed when right click on a cell.

![](Context-Menu_images/context-menu_img1.png)

### Column Header Context Menu

The following output is displayed when right click on a column header.

![](Context-Menu_images/context-menu_img2.png)

### Pager Context Menu

The following output is displayed when right click on a pager.

![](Context-Menu_images/context-menu_img4.png)

### Row Header Context Menu

The following output is displayed when right click on a row header.

![](Context-Menu_images/context-menu_img3.png)

## Default Context Menu items

You can use some default items in context menu. Please find the below table for default context menu items and its actions.

<table>
    <colgroup><col width= "225px"/><col width = "125px"/></colgroup>
    <tr><th>Section<br/></th><th>Menu items<br/></th><th>Action<br/></th></tr>
    <tr><td>Row Cell<br/></td><td>Cut<br/></td><td>Cut the selected cells content to the clipboard, so that you can paste it to somewhere else.<br/></td></tr>
    <tr><td><br/></td><td>Copy <br/></td><td>Copy the selected cells content to the clipboard, so that you can paste it to somewhere else.<br/></td></tr>
    <tr><td><br/></td><td>Paste<br/></td><td>Paste the content from clipboard to spreadsheet.<br/></td></tr>
    <tr><td><br/></td><td>Insert<br/></td><td>Insert new cells or rows or columns to worksheet.<br/></td></tr>
    <tr><td><br/></td><td>Delete<br/></td><td>Delete existing cells or rows or columns from worksheet.<br/></td></tr>
    <tr><td><br/></td><td>Sort<br/></td><td>Perform sorting to the selected range of cells by ascending or descending.<br/></td></tr>
    <tr><td><br/></td><td>Filter<br/></td><td>Perform filtering to the selected cells based an active cell's value or active cell's color.<br/></td></tr>
    <tr><td><br/></td><td>Hyperlink<br/></td><td>Create a link in the spreadsheet for quick access to webpages or worksheet reference.<br/></td></tr>
    <tr><td><br/></td><td>Comment<br/></td><td>Add a note or extra information about the cells.<br/></td></tr>
    <tr><td><br/></td><td>Format Cells<br/></td><td>Apply number format to the selected cells.<br/></td></tr>
    <tr><td><br/></td><td>Clear Contents<br/></td><td>Delete the contents in the selected cells.<br/></td></tr>
    <tr><td>Row Header / Column Header<br/></td><td>Cut<br/></td><td>Cut the selected cells content to the clipboard, so that you can paste it to somewhere else.<br/></td></tr>
    <tr><td><br/></td><td>Copy <br/></td><td>Copy the selected cells content to the clipboard, so that you can paste it to somewhere else.<br/></td></tr>
    <tr><td><br/></td><td>Paste<br/></td><td>Paste the content from clipboard to spreadsheet.<br/></td></tr>
    <tr><td><br/></td><td>Clear Contents<br/></td><td>Delete the contents in the selected cells.<br/></td></tr>
    <tr><td><br/></td><td>Insert<br/></td><td>Insert new cells or rows or columns to worksheet.<br/></td></tr>
    <tr><td><br/></td><td>Delete<br/></td><td>Delete existing cells or rows or columns from worksheet.<br/></td></tr>
    <tr><td><br/></td><td>Hide<br/></td><td>Hide the selected worksheet.<br/></td></tr>
    <tr><td><br/></td><td>Unhide<br/></td><td>Opens unhide dialog to unhide worksheet.<br/></td></tr>
    <tr><td>Pager<br/></td><td>Insert<br/></td><td>Insert new worksheet to spreadsheet.<br/></td></tr>
    <tr><td><br/></td><td>Delete<br/></td><td>Delete the selected worksheet from spreadsheet.<br/></td></tr>
    <tr><td><br/></td><td>Move or copy<br/></td><td>Opens move or copy dialog to move or create duplicate worksheet.<br/></td></tr>
    <tr><td><br/></td><td>Rename<br/></td><td>Rename the selected work sheet.<br/></td></tr>
    <tr><td><br/></td><td>Protect Sheet<br/></td><td>Prevent unwanted changes from others by limiting their ability to edit.<br/></td></tr>
    <tr><td><br/></td><td>Hide <br/></td><td>Hide the selected worksheet.<br/></td></tr>
    <tr><td><br/></td><td>Unhide<br/></td><td>Opens unhide dialog to unhide worksheet.<br/></td></tr>
</table>
