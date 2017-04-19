---
layout: post
title: Freeze Pane with Spreadsheet widget for Syncfusion Essential JS
description: How to use the Spreadsheet Freeze Pane
platform: js
control: Spreadsheet
documentation: ug
keywords: Freeze, unfreeze, freezePanes, freezeleftcolumn, freezetoprow
api: /api/js/ejspreadsheet
--- 

# Freeze Pane 
Freeze pane allows you to keep a portion of the sheet visible, while scrolling through the rest of the worksheet. 

The freeze pane can be applied in a following ways,

1. User Interface
2. Initial Load
3. Method

### User Interface
Select any cell and on OTHERS tab click Freeze Panes in Freeze Panes dropdown list.

![](Freeze-Pane_images/Freeze-Pane_img1.png)

### Initial Load
You can use [`allowFreezing`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowfreezing "allowFreezing") property to enable or disable freeze pane in Spreadsheet.
To specify number of rows and columns to be frozen, use [`frozenRows`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-frozenrows "frozenRows") and [`frozenColumns`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-frozencolumns "frozenColumns") property in sheets.

The following code example describes the above behavior,

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}

$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.personList" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        allowFreezing: true,
        sheets: [{
            dataSource: window.personList, 
            frozenRows:5,
		    frozenColumns:2
        }],
    });
});
{% endhighlight %}

N> The default value of [`allowFreezing`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowfreezing "allowFreezing") property is true.

### Method
You can freeze rows or columns using [`freezePanes`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlfreeze-freezepanes "freezePanes") method. 

The following code example describes the above behavior,

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.personList" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            dataSource: window.personList  
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete(args) {
    if (!this.isImport)
        this.XLFreeze.freezePanes(5,2);
}
{% endhighlight %}

The following output is displayed as a result of the above behavior.
![](Freeze-Pane_images/Freeze-Pane_img2.png)

N> When we apply freeze pane by selecting cell “A1”, rows and columns are frozen based on the middle cell in the worksheet.

## Freeze Rows
It allows you to keep the certain number of rows visible while scrolling through the rest of the worksheet.

The freeze rows can be applied in a following ways,

1. Initial Load
2. Method

### Initial Load
You can freeze rows using [`frozenRows`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-frozenrows "frozenRows") property in sheets. 

The following code example describes the above behavior,

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.personList" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            dataSource: window.personList, 
            frozenRows:3,
        }],
    });
});
{% endhighlight %}

### Method
You can freeze rows using [`freezeRows`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlfreeze-freezerows "freezeRows") method. 

The following code example describes the above behavior,

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.personList" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            dataSource: window.personList  
        }],
    loadComplete: "loadComplete"
    });
});
function loadComplete(args) {
    if (!this.isImport)
        this.XLFreeze.freezeRows(3);
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Freeze-Pane_images/Freeze-Pane_img3.png)

N> On OTHERS tab click Freeze Top Row in FreezePanes dropdown list, to freeze top row. You can also freeze top row using [`freezeTopRow`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlfreeze-freezetoprow "freezeTopRow") method. 

## Freeze Columns
It allows you to keep the certain number of column visible while scrolling through the rest of the work sheet.

The freeze columns can be applied in a following ways,

1. Initial Load
2. Method

### Initial Load
You can apply freeze columns using [`frozenColumns`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-frozencolumns "frozenColumns") property in sheets.
The following code example describes the above behavior

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.personList" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            dataSource: window.personList, 
            frozenColumns: 3
        }],
    });
});

{% endhighlight %}

### Method
You can apply freeze columns using [`freezeColumns`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlfreeze-freezecolumns "freezeColumns") method. 
The following code example describes the above behavior

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.personList" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            dataSource: window.personList
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete(args) {
    if (!this.isImport)
        this.XLFreeze.freezeColumns(3);
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Freeze-Pane_images/Freeze-Pane_img4.png)

N> On OTHERS tab click Freeze First Column in FreezePanes dropdown list, to freeze left Column. You can also apply freeze first column using [`freezeLeftColumn`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlfreeze-freezeleftcolumn "freezeLeftColumn") method. 

## Unfreeze Pane
Unfreeze all the rows and columns to scroll through entire sheet.

The unfreeze pane can be applied in a following ways,

1. User Interface
2. Method

### User Interface
On OTHERS tab click Unfreeze Panes in Freeze Panes dropdown list.
![](Freeze-Pane_images/Freeze-Pane_img5.png)

### Method
You can unfreeze rows or columns using [`unfreezePanes`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlfreeze-unfreezepanes "unfreezePanes") method. 

The following code example describes the above behavior,

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.personList" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            dataSource: window.personList
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete(args) {
    if (!this.isImport){
        this.XLFreeze.freezePanes(5,2);
        this.XLFreeze.unfreezePanes();
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Freeze-Pane_images/Freeze-Pane_img6.png)


