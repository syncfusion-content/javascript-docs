---
layout: post
title: Worksheets with Spreadsheet widget for Syncfusion Essential JS
description: How to use and customize the Spreadsheet Worksheet
platform: js
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
--- 

# Worksheet

Worksheet is a collection of cells organized in the form of rows and columns that allow us to store, format, manipulate and display data in grid format. You can create multiple sheets in Spreadsheet and use sheet tab for switching between those worksheets. By default Spreadsheet creates single worksheet since default [`sheetCount`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheetcount "sheetCount") value is `1`.

By Using the method [`gotoPage`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:gotopage "gotoPage") you can send a paging request to the specified sheet Index in the Spreadsheet.

## List of Sheet Operations 

You can perform following operations in worksheet,

* Add
* Copy
* Move
* Remove
* Rename

### Add

The Spreadsheet has support for inserting new sheet. You can insert a sheet in two ways.

* Add a new sheet as a last sheet.
* Insert a new sheet before the active sheet.

#### Add Sheet

You can dynamically add a sheet by one of the following ways,

* Click the new sheet button in the spreadsheet sheet tab.
* Using [`addNewSheet`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:addnewsheet "addNewSheet") method.

#### Insert Sheet

You can dynamically insert a sheet by one of the following ways,

* Right clicking on the worksheet in the sheet tab and then click Insert option in the context menu.
* Click OTHERS tab in the ribbon and select Insert Sheet option in Insert dropdown button.
* Using [`insertSheet`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:insertsheet "insertSheet") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({                                            
        sheetCount: 1,
        loadComplete: "loadComplete"               
    });
});
function loadComplete(args) {          
    if(!this.isImport) {
        this.addNewSheet(); //To add as a last sheet.
        //this.insertSheet(); // To insert a sheet before the active sheet.
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img1.png)

### Copy

The Spreadsheet provides support to create a copy of an existing worksheet. You can dynamically copy a worksheet by using one of the following ways,

* Right clicking on the worksheet in the sheet tab and then click Move or Copy in the context menu. Check the “Create a copy” checkbox in the “Move or Copy” dialog.
* Copy an existing worksheet using [`copySheet`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:copysheet "copySheet") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({                                        
        sheetCount: 3,
        loadComplete: "loadComplete"               
    });
});
function loadComplete(args) {          
    if (!this.isImport)
        this.copySheet(1, 3, true); //arg1- from index, arg2 -to index, arg3 - isCopySheet
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img2.png)

### Move

The Spreadsheet provides support to move an existing worksheet. You can dynamically move a worksheet by using one of the following ways,

* Right clicking on the worksheet in the sheet tab and then click Move or Copy in the context menu. Select the sheet that you have to move in the “Move or Copy” dialog.
* Move an existing worksheet using [`copySheet`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:copysheet "copySheet") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({                                        
        sheetCount: 3,
        loadComplete: "loadComplete"               
    });
});
function loadComplete(args) {          
    if (!this.isImport)
        this.copySheet(1, 3, false); //arg1- from index, arg2 -to index, arg3 - isCopySheet
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img3.png)

### Remove

The Spreadsheet has support for removing an existing worksheet. You can dynamically remove the existing sheet by following ways,

* Right clicking on the worksheet in the sheet tab and then click Delete option in the context menu.
* Click OTHERS tab in the ribbon and select Delete Sheet option in Delete dropdown button.

You can also remove an active worksheet using [`deleteSheet`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:deletesheet "deleteSheet") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({                                        
        sheetCount: 2,
        loadComplete: "loadComplete"               
    });
});
function loadComplete(args) {          
    if(!this.isImport)
        this.deleteSheet();
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img4.png)

### Rename

The Spreadsheet has support for renaming an existing worksheet. You can dynamically rename worksheet by using one of the following ways,

* Right clicking on the worksheet in the sheet tab and then click Rename option in the context menu.
* Rename an active worksheet using [`sheetRename`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:sheetrename "sheetRename") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({                                                       
        loadComplete: "loadComplete",
        sheetCount: 2              
    });
});
function loadComplete(args) {          
    if(!this.isImport)
        this.sheetRename("RenameSheet")
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img5.png)

N> 1. To refresh the content in Spreadsheet, use [`refreshContent`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:refreshcontent "refreshContent") method.
N> 2. To refresh the Spreadsheet, use[`refreshSpreadsheet`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:refreshspreadsheet "refreshSpreadsheet")method.

## Headers

Headers in the spreadsheet are numbered rows and lettered columns in worksheets. It makes ease of view and reference your data. You can dynamically show/hide worksheet header by using one of the following ways,

* Select PAGE LAYOUT tab in the ribbon and then check or uncheck Headings in the Show group.
* Show/Hide the worksheet headers using [`showHeadings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-showheadings "showHeadings") property and [`showHeadings`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:showheadings "showHeadings") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({               
        sheets: [{ showHeadings: false }]
    });
});
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img6.png)

## Show/Hide Sheets

You can dynamically show/hide worksheet by using one of the following ways,

* Right clicking on the worksheet in the sheet tab and then click Hide or Unhide in the context menu
* Hide the sheet using [`hideSheet`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:hidesheet "hideSheet") method.
* Show the hidden sheet using [`unhideSheet`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:unhidesheet "unhideSheet") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        sheetCount: 3,
        loadComplete: "loadComplete"
    });
});
function loadComplete(args) {          
    if (!this.isImport) {
        this.hideSheet(1);
        this.hideSheet(2);
        this.unhideSheet(1);
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img7.png)

## Show/Hide Gridlines

Gridlines act as a border like appearance of cells. They are used to distinguish cells on the worksheet. You can dynamically show/hide gridlines by using one of the following ways,

* Select PAGE LAYOUT tab in the ribbon and then check or uncheck Gridlines in the Show group.
* Show/Hide gridlines in a worksheet using [`showGridlines`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-showgridlines "showGridlines") property and [`showGridlines`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:showgridlines "showGridlines") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        sheets: [{ showGridlines: false }]
    });
});
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img8.png)