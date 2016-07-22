---
layout: post
title: Worksheets with Spreadsheet widget for Syncfusion Essential JS
description: How to use and customize the Spreadsheet Worksheet
platform: js
control: Spreadsheet
documentation: ug
--- 

# Worksheet

Worksheet is a collection of cells organized in the form of rows and columns that allow us to store, format, manipulate and display data in grid format. You can create multiple sheets in Spreadsheet and use sheet tab for switching between those worksheets.
By default Spreadsheet creates single worksheet since default sheetCount value is `1`.

## List of Sheet Operation 

You can perform following operations in Worksheet,

* Add
* Remove
* Rename
* Move and Copy

### Add

The Spreadsheet has support for inserting new sheet. You can dynamically insert sheet by one of the following ways,

* Click the New sheet button in the spreadsheet sheet tab.
* Click OTHERS tab in the ribbon and select Insert dropdown button. Then click Insert Sheet.

You can also add new sheet using [`addNewSheet`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:addnewsheet "addNewSheet") method.

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
        if(!this.isImport)
            this.addNewSheet();
    }
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img1.png)

### Remove

The Spreadsheet has support for removing an existing worksheet. You can dynamically remove the existing sheet by following ways,

* Right click on the worksheet in the sheet tab and then click delete option in the context menu.
* Select the existing worksheet, Click OTHERS tab in the ribbon and select Delete dropdown button. Then click Delete Sheet.

You can also remove an active worksheet using [`deleteSheet`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:deletesheet "deleteSheet") method.

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
![](Worksheet_images/Worksheet_img2.png)

### Rename

The Spreadsheet has support for renaming an existing worksheet. You can dynamically rename worksheet by using one of the following ways,

* Right clicking on the worksheet on the sheet tab and then click Rename in the context menu. 
* Rename an active worksheet using [`sheetRename`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:sheetrename "sheetRename") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({                                                       
            loadComplete: "loadComplete"               
        });
    });
    function loadComplete(args) {          
        if(!this.isImport)
            this.sheetRename("RenameSheet")
    }
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img3.png)

### Move

The Spreadsheet provides support to move an existing worksheet. You can dynamically move a worksheet by using one of the following ways,

* Right clicking on the worksheet on the sheet tab and then click Move or Copy in the context menu. Then select the sheet that you have to move in the "Move or Copy" dialog.
* Move an existing worksheet using [`copySheet`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:copysheet "copySheet") method.

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
![](Worksheet_images/Worksheet_img4.png)

### Copy

The Spreadsheet provides support to create a copy an existing worksheet. You can dynamically copy a worksheet by using one of the following ways,

* Right clicking on the worksheet in the sheet tab that you have to copy and then click Move or Copy in the context menu. Then check the "Create a copy" checkbox in the "Move or Copy" dialog. 
* Copy an existing worksheet using [`copySheet`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:copysheet "copySheet") method.

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
![](Worksheet_images/Worksheet_img5.png)

## Headers

Headers in the spreadsheet are numbered rows and lettered columns in worksheets. It makes ease of view and reference your data. You can dynamically show/ hide worksheet header by using one of the following ways,

* Select PAGE LAYOUT tab in the ribbon and uncheck Headings in the Show group.
* Show/Hide the worksheet headers using [`showHeadings`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-showheadings "showHeadings") property and [`showHeadings`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:showheadings "showHeadings") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div> 
{% endhighlight %}

{% highlight javascript %}
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({               
            loadComplete: "loadComplete"
        });
    });
    function loadComplete(args) {
        if (!this.isImport)
            this.showHeadings(false);
    }
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Worksheet_images/Worksheet_img6.png)

## Show/Hide Sheets

You can dynamically show/ hide worksheet by using one of the following ways,

* Right click worksheet on the sheet tab and then click Hide or Unhide in the context menu.
* Hide the sheet using [`hideSheet`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:hidesheet "hideSheet") method.
* Show the hidden sheet using [`unhideSheet`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:unhidesheet "unhideSheet") method.

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

* Select PAGE LAYOUT tab in the ribbon and uncheck Gridlines in the Show group.
* Show/Hide gridlines in a worksheet using [`showGridlines`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-showgridlines "showGridlines") property and [`showGridlines`](http://help.syncfusion.com/js/api/ejspreadsheet#methods:showgridlines "showGridlines") method.

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