---
layout: post
title: Rows and Columns with Spreadsheet widget for Syncfusion Essential JS
description: How to use and customize the Spreadsheet rows and columns
platform: js
control: Spreadsheet
documentation: ug
--- 

# Rows and columns

Spreadsheet is a tabular format consisting of rows and columns. Rows and Columns are used to represent the editing area in Spreadsheet. The intersection point of rows and columns are called as Cells. In that you can perform editing. You have [`rowCount`](http://help.syncfusion.com/js/api/ejspreadsheet#members:rowcount "rowCount") and [`columnCount`](http://help.syncfusion.com/js/api/ejspreadsheet#members:columncount "columnCount") in sheets property and model for defining the rows and columns count. By default Spreadsheet creates `20` rows and `21` columns. Based on this grid content will be created.

## Rows 

Rows are a collection of cells that run horizontally. Each row is identified by the row number in the row header.

## Columns

Columns are a collection of cells that run vertically. Each column is identified by column heading in the column header.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from   
        'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
         sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, startCell: "A1", showHeader: true }],                               
        }],
        rowCount: 50,
        columnCount: 36,
    });
});
{% endhighlight %}

## List of operations 

You can perform following operations in rows and columns, 

* Insert
* Delete
* Show and Hide
* Resizing

## Insert 

You can insert blank cells, rows or columns based on the selection in a worksheet. You have to enable the [`allowInsert`](http://help.syncfusion.com/js/api/ejspreadsheet#members:allowinsert "allowInsert") property to perform the insert operation. 
You can access insert operation through,

* OTHERS tab in ribbon.
* Context menu

N> In the header context menu you can insert only rows or columns.

#### Insert Shift Bottom

You can dynamically insert blank cells to the top of the selected range and shift the selected cells to down by following,

* Click Insert in the context menu and select "Shift Cells Down" option in Insert dialog.
* Select Insert Cells option in Insert button of OTHERS tab in Ribbon and select "Shift Cells Down" option in Insert dialog.

You can also perform insert shift bottom using [`insertShiftBottom`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:insertshiftbottom "insertShiftBottom") method.

#### Insert Shift Right

You can dynamically insert blank cells to the left of the selected range and shift the selected cells to right by following,

* Click Insert in the context menu and select "Shift Cells Right" option in Insert dialog.
* Select Insert Cells option in Insert button of OTHERS tab in Ribbon and select "Shift Cells Right" option in Insert dialog.

You can also perform insert shift right using [`insertShiftRight`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:insertshiftright "insertShiftRight") method.

#### Insert Entire Row

You can dynamically insert the selected number of blank rows to the top of the selected range by following,

* Click Insert in the context menu and select "Entire Row" option in Insert dialog.
* Select Insert Cells option in Insert button of OTHERS tab in Ribbon and select "Entire Row" option in Insert dialog.
* Select Insert Sheet Rows option in Insert button of OTHERS tab in Ribbon.
* Click Insert option in row header context menu. 

You can also perform insert entire row using [`insertEntireRow`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:insertentirerow "insertEntireRow") method.

#### Insert Entire Column

You can dynamically insert the selected number of blank columns to the left of the selected range by following,

* Click Insert in the context menu and select "Entire Column" option in Insert dialog.
* Select Insert Cells option in Insert button of OTHERS tab in Ribbon and select "Entire Column" option in Insert dialog.
* Select Insert Sheet Columns option in Insert button of OTHERS tab in Ribbon.
* Click Insert option in column header context menu. 

You can also perform insert entire column using [`insertEntireColumn`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:insertentirecolumn "insertEntireColumn") method.

## Delete 

You can delete a range of cells, rows or columns based on the selection in worksheet. You have to enable the [`allowDelete`](http://help.syncfusion.com/js/api/ejspreadsheet#members:allowdelete "allowDelete") property to perform Delete Operation. 

You can access delete operation through,

* OTHERS tab in Ribbon
* Context menu

N> In header Context menu you can delete only rows or columns.

#### Delete Shift Up

You can dynamically delete the selected range of cells and shift the other cells to top by following,

* Click Delete in the context menu and select "Shift Cells Up" option in Delete dialog.
* Select Delete Cells option in Delete button of OTHERS tab in Ribbon and select "Shift Cells Up" option in Delete dialog.

You can also perform delete shift up using [`deleteShiftUp`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:deleteshiftup "deleteShiftUp") method.

#### Delete Shift Left

You can dynamically delete the selected range of cells and shift the other cells to left by following,

* Click Delete in the context menu and select "Shift Cells Left" option in Delete dialog.
* Select Delete Cells in Delete button of OTHERS tab in Ribbon and select "Shift Cells Left" option in Delete dialog.

You can also perform delete shift up using [`deleteShiftLeft`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:deleteshiftleft "deleteShiftLeft") method.

#### Delete Entire Row

You can dynamically delete the selected rows and shift the other rows to top by following,

* Click Delete in the context menu and select "Entire Row" option in Delete dialog.
* Select Delete Cells option in Delete button of OTHERS tab in Ribbon and select "Entire Row" option in Delete dialog.
* Select Delete Sheet Rows option in Delete button of OTHERS tab in Ribbon.
* Click Delete option in row header context menu. 

You can also perform delete entire row using [`deleteEntireRow`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:deleteentirerow "deleteEntireRow") method.

#### Delete Entire Column

You can dynamically delete a selected columns and shift other columns to left by following,

* Click Delete in the context menu and select "Entire Column" option in Delete dialog.
* Select Delete Cells option in Delete button of OTHERS tab in Ribbon and select "Entire Column" option in Delete dialog.
* Select Delete Sheet Columns option in Delete button of OTHERS tab in Ribbon.
* Click Delete option in column header context menu. 

You can also perform delete entire column using [`deleteEntireColumn`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:deleteentirecolumn "deleteEntireColumn") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from   
        'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, startCell: "A1", showHeader: true }],                               
        }],
        allowInsert: true,
        allowDelete: true,
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    var xlObj = this.XLObj;
    if(!xlObj.isImport) {
        xlObj.insertEntireRow(2, 2);
        xlObj.insertEntireColumn(2, 2);
        xlObj.deleteEntireRow(4, 4);
        xlObj.deleteEntireColumn(4, 4);
        xlObj.insertShiftBottom({rowIndex: 4, colIndex: 4}, {rowIndex: 4, colIndex: 4});
        xlObj.insertShiftRight({rowIndex: 3, colIndex: 4}, {rowIndex: 3, colIndex: 4});
        xlObj.deleteShiftUp({rowIndex: 4, colIndex: 6}, {rowIndex: 4, colIndex: 6});
        xlObj.deleteShiftLeft({rowIndex: 3, colIndex: 6}, {rowIndex: 3, colIndex: 6});
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](RowsAndColumns_images/RowsAndColumns_img1.png)

## Show and Hide 

You can show or hide the rows and columns in Spreadsheet using methods and context menu. 

#### Hide Row

You can hide the rows dynamically by using one of the following ways,

* Click "Hide" option in row header context menu.
* Hide the rows using [`hideRow`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:hiderow "hideRow") method.

#### Hide Column

You can hide the columns dynamically by using one of the following ways,

* Click "Hide" option in column header context menu.
* Hide the columns using [`hideColumn`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:hidecolumn "hideColumn") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from   
        'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, startCell: "A1", showHeader: true }],                               
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete(args) {
    var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
    if(!xlObj.isImport){
        xlObj.hideRow(2);
        xlObj.hideColumn(2);
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](RowsAndColumns_images/RowsAndColumns_img2.png)

#### Show Row

You can show the hidden rows dynamically by using one of the following ways,

* Click "Unhide" option in row header context menu.
* Show the hidden rows using [`showRow`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:showrow "showRow") method.

#### Show Column

You can show the hidden columns dynamically by using one of the following ways,

* Click "Unhide" option in column header context menu.
* Show the hidden columns using [`showColumn`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:showcolumn "showColumn") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from   
        'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, startCell: "A1", showHeader: true }],                               
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete(args) {
    var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
    if(!xlObj.isImport){
        xlObj.showRow(2);
        xlObj.showColumn(2);
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](RowsAndColumns_images/RowsAndColumns_img3.png)

## Resizing

You can change [`columnWidth`](http://help.syncfusion.com/js/api/ejspreadsheet#members:columnwidth "columnWidth") and [`rowHeight`](http://help.syncfusion.com/js/api/ejspreadsheet#members:rowheight "rowHeight") with the specified value. You have to enable [`allowResizing`](http://help.syncfusion.com/js/api/ejspreadsheet#members:allowresizing "allowResizing") to perform resizing. 

You can perform resizing using one of the following ways,

* Resize option in column header and row header.
* set the column width by using [`setColWidth`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:xlresize-setcolwidth "setColWidth") method or [`columnWidth`](http://help.syncfusion.com/js/api/ejspreadsheet#members:columnwidth "columnWidth") property.
* set the row height by using [`setRowHeight`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:xlresize-setrowheight "setRowHeight") method or [`rowHeight`](http://help.syncfusion.com/js/api/ejspreadsheet#members:rowheight "rowHeight") property.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from   
        'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, startCell: "A1", showHeader: true }],
            rowHeight: 21,
            columnWidth: 64
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete(args) {
    var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
    if(!xlObj.isImport){
        xlObj.XLResize.setColWidth(2, 100);
        xlObj.XLResize.setRowHeight(2, 40);
    }
}
{% endhighlight %}