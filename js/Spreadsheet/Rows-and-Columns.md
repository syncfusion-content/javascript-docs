---
layout: post
title: Rows and Columns with Spreadsheet widget for Syncfusion Essential JS
description: How to use and customize the Spreadsheet rows and columns
platform: js
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
--- 

# Rows and Columns

Spreadsheet is a tabular format consisting of rows and columns. Rows and columns are used to represent the editing area in Spreadsheet. The intersection point of rows and columns are called as cells. In that you can perform editing. You have [`rowCount`](https://help.syncfusion.com/api/js/ejspreadsheet#members:rowcount "rowCount") and [`columnCount`](https://help.syncfusion.com/api/js/ejspreadsheet#members:columncount "columnCount") in sheets property for defining the rows and columns count. By default Spreadsheet creates `20` rows and `21` columns. Based on this grid content will be created.

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

You can insert blank cells, rows or columns based on the selection in a worksheet. You have to enable the [`allowInsert`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowinsert "allowInsert") property to perform the insert operation. 
You can perform insert operation through,

* OTHERS tab in ribbon.
* Context menu

N> In the header context menu you can insert only rows or columns.

#### Insert Shift Bottom

You can dynamically insert blank cells to the top of the selected range and shift the selected cells to down by following,

* Click Insert in the context menu and select "Shift Cells Down" option in Insert dialog.
* Select Insert Cells option in Insert button of OTHERS tab in Ribbon and select "Shift Cells Down" option in Insert dialog.

You can also perform insert shift bottom using [`insertShiftBottom`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:insertshiftbottom "insertShiftBottom") method.

#### Insert Shift Right

You can dynamically insert blank cells to the left of the selected range and shift the selected cells to right by following,

* Click Insert in the context menu and select "Shift Cells Right" option in Insert dialog.
* Select Insert Cells option in Insert button of OTHERS tab in Ribbon and select "Shift Cells Right" option in Insert dialog.

You can also perform insert shift right using [`insertShiftRight`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:insertshiftright "insertShiftRight") method.

#### Insert Entire Row

You can dynamically insert the selected number of blank rows to the top of the selected range by following,

* Click Insert in the context menu and select "Entire Row" option in Insert dialog.
* Select Insert Cells option in Insert button of OTHERS tab in Ribbon and select "Entire Row" option in Insert dialog.
* Select Insert Sheet Rows option in Insert button of OTHERS tab in Ribbon.
* Click Insert option in row header context menu. 

You can also perform insert entire row using [`insertEntireRow`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:insertentirerow "insertEntireRow") method.

#### Insert Entire Column

You can dynamically insert the selected number of blank columns to the left of the selected range by following,

* Click Insert in the context menu and select "Entire Column" option in Insert dialog.
* Select Insert Cells option in Insert button of OTHERS tab in Ribbon and select "Entire Column" option in Insert dialog.
* Select Insert Sheet Columns option in Insert button of OTHERS tab in Ribbon.
* Click Insert option in column header context menu. 

You can also perform insert entire column using [`insertEntireColumn`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:insertentirecolumn "insertEntireColumn") method.

## Delete 

You can delete a range of cells, rows or columns based on the selection in worksheet. You have to enable the [`allowDelete`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowdelete "allowDelete") property to perform delete operation. 

You can perform delete operation through,

* OTHERS tab in Ribbon
* Context menu

N> In header Context menu you can delete only rows or columns.

#### Delete Shift Up

You can dynamically delete the selected range of cells and shift the other cells to top by following,

* Click Delete in the context menu and select "Shift Cells Up" option in Delete dialog.
* Select Delete Cells option in Delete button of OTHERS tab in Ribbon and select "Shift Cells Up" option in Delete dialog.

You can also perform delete shift up using [`deleteShiftUp`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:deleteshiftup "deleteShiftUp") method.

#### Delete Shift Left

You can dynamically delete the selected range of cells and shift the other cells to left by following,

* Click Delete in the context menu and select "Shift Cells Left" option in Delete dialog.
* Select Delete Cells in Delete button of OTHERS tab in Ribbon and select "Shift Cells Left" option in Delete dialog.

You can also perform delete shift left using [`deleteShiftLeft`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:deleteshiftleft "deleteShiftLeft") method.

#### Delete Entire Row

You can dynamically delete the selected rows and shift the other rows to top by following,

* Click Delete in the context menu and select "Entire Row" option in Delete dialog.
* Select Delete Cells option in Delete button of OTHERS tab in Ribbon and select "Entire Row" option in Delete dialog.
* Select Delete Sheet Rows option in Delete button of OTHERS tab in Ribbon.
* Click Delete option in row header context menu. 

You can also perform delete entire row using [`deleteEntireRow`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:deleteentirerow "deleteEntireRow") method.

#### Delete Entire Column

You can dynamically delete a selected columns and shift other columns to left by following,

* Click Delete in the context menu and select "Entire Column" option in Delete dialog.
* Select Delete Cells option in Delete button of OTHERS tab in Ribbon and select "Entire Column" option in Delete dialog.
* Select Delete Sheet Columns option in Delete button of OTHERS tab in Ribbon.
* Click Delete option in column header context menu. 

You can also perform delete entire column using [`deleteEntireColumn`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:deleteentirecolumn "deleteEntireColumn") method.

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
    if(!this.isImport) {
        this.insertEntireRow(2, 2);
        this.insertEntireColumn(2, 2);
        this.deleteEntireRow(4, 4);
        this.deleteEntireColumn(4, 4);
        this.insertShiftBottom({rowIndex: 4, colIndex: 4}, {rowIndex: 4, colIndex: 4});
        this.insertShiftRight({rowIndex: 3, colIndex: 4}, {rowIndex: 3, colIndex: 4});
        this.deleteShiftUp({rowIndex: 4, colIndex: 6}, {rowIndex: 4, colIndex: 6});
        this.deleteShiftLeft({rowIndex: 3, colIndex: 6}, {rowIndex: 3, colIndex: 6});
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Rows-and-Columns_images/Rows-and-Columns_img1.png)

## Show and Hide 

You can show or hide the rows and columns in Spreadsheet using methods and context menu. 

#### Hide Row

You can hide the rows dynamically by using one of the following ways,

* Click "Hide" option in row header context menu.
* Hide the rows using [`hideRow`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:hiderow "hideRow") method and [`hideRows`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-hiderows "hideRows") option in [`sheets`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets "sheets") property.

#### Hide Column

You can hide the columns dynamically by using one of the following ways,

* Click "Hide" option in column header context menu.
* Hide the columns using [`hideColumn`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:hidecolumn "hideColumn") method and [`hideColumns`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-hidecolumns "hideColumns") option in [`sheets`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets "sheets") property.

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
    this.setWidthToColumns([180, ]);
    if(!this.isImport){
        this.hideRow(2);
        this.hideColumn(2);
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Rows-and-Columns_images/Rows-and-Columns_img2.png)

#### Show Row

You can show the hidden rows dynamically by using one of the following ways,

* Click "Unhide" option in row header context menu.
* Show the hidden rows using [`showRow`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:showrow "showRow") method.

#### Show Column

You can show the hidden columns dynamically by using one of the following ways,

* Click "Unhide" option in column header context menu.
* Show the hidden columns using [`showColumn`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:showcolumn "showColumn") method.

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
    if(!this.isImport){
        this.showRow(2);
        this.showColumn(2);
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Rows-and-Columns_images/Rows-and-Columns_img3.png)

## Resizing

You can change [`columnWidth`](https://help.syncfusion.com/api/js/ejspreadsheet#members:columnwidth "columnWidth") and [`rowHeight`](https://help.syncfusion.com/api/js/ejspreadsheet#members:rowheight "rowHeight") with the specified value. You have to enable [`allowResizing`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowresizing "allowResizing") to perform resizing. 

You can perform resizing using one of the following ways,

* Resize option in column header and row header.
* Set the column width by using [`setColWidth`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlresize-setcolwidth "setColWidth") method or [`columnWidth`](https://help.syncfusion.com/api/js/ejspreadsheet#members:columnwidth "columnWidth") property.
* Set the row height by using [`setRowHeight`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlresize-setrowheight "setRowHeight") method or [`rowHeight`](https://help.syncfusion.com/api/js/ejspreadsheet#members:rowheight "rowHeight") property.
* To fit the height of rows in the spreadsheet use[`fitHeight`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlresize-fitheight "fitHeight") method.
* To fit the width of columns in the spreadsheet use[`fitWidth`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlresize-fitwidth "fitWidth") method.

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
    if(!this.isImport){
        this.XLResize.setColWidth(2, 100);
        this.XLResize.setRowHeight(2, 40);
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Rows-and-Columns_images/Rows-and-Columns_img4.png)