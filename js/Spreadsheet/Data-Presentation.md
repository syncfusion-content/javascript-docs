---
layout: post
title: Data presentation with Spreadsheet widget for Syncfusion Essential JS.
description: How to perform Spreadsheet Data presentation.
platform: js
control: Spreadsheet
documentation: ug
--- 

# Data Presentation

Data presentation is helpful for proper representation of data in Spreadsheet. You have following features in Data Presentation.

* Cell types
* Chart
* Conditional formatting
* Filtering 
* Picture
* Pivot table
* Sorting 
* Table

## Cell Type

You can insert the controls like Button, Checkbox, Dropdown list and Date picker. You can use [`allowCellType`](http://help.syncfusion.com/api/js/ejspreadsheet#members:allowcelltype "allowCellType") property to enable/disable cell type operations.

### To Insert a Cell Type.

You can insert the cell type to the selected range of cells by using [`addCellTypes`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlcelltype-addcelltypes "addCellTypes") method.

### To remove Cell Type

You can delete the cell type in the selected range of cells by using [`removeCellTypes`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlcelltype-removecelltypes "removeCellTypes") method.

The following code example describes the above behavior. 

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, showHeader: true }],                               
        }],
        allowCellType: true,
        loadComplete: "loadComplete"
     });
});
function loadComplete() {
    var xlCellType = this.XLCellType;
    if (!this.isImport) {
        xlCellType.addCellTypes("D1", {"type" : ej.Spreadsheet.CustomCellType.Button, "text" : "Button1", "background-color" : "green" },  1);
        xlCellType.addCellTypes("B1", {"type" : ej.Spreadsheet.CustomCellType.DatePicker, 'value' : '2/12/2016'},  1);
        xlCellType.addCellTypes("A1", {"type" : ej.Spreadsheet.CustomCellType.DropDownList, 'dataSourceRange': 'A2:A11'},  1);
        xlCellType.addCellTypes("C1", {"type" : ej.Spreadsheet.CustomCellType.DropDownList, 'dataSourceRange': 'A2:A11'},  1);
        xlCellType.addCellTypes("E1", {"type" : ej.Spreadsheet.CustomCellType.CheckBox, "isChecked" : true },  1);
        xlCellType.removeCellTypes("C1");
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img1.png)

## Chart

Chart is a graphical representation of data, that organizes and represents a set of numerical or qualitative data. It mostly displays the selected range of data in terms of x axis and y axis. You can use [`allowCharts`](http://help.syncfusion.com/api/js/ejspreadsheet#members:allowcharts "allowCharts") property to enable/disable chart operations.

### Type of Charts

The following types of charts are available in Spreadsheet.

* Area Chart
* Bar Chart
* Column Chart
* Line Chart
* Pie Chart
* Radar Chart
* Scatter Chart

You can create the Chart by one of the following ways,

* Using "Chart Type" button to Select the type of chart under Charts group of INSERT Tab in ribbon.
* Using [`createChart`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlchart-createchart "createChart") method to create the chart.

### Chart Customization

You can perform the following customizations for chart. These are available in DESIGN Tab which is enabled while clicking the chart element.

<table>
    <colgroup><col width="180px" /></colgroup>
    <tr><th>Feature</br></th><th>Description</br></th></tr>
    <tr><td>Add Chart Elements</br></td><td>You can add a chart element like chart axes, legends, chart title, axis title, data labels and grid lines.</br></td></tr>
    <tr><td>Switch Row/Column</br></td><td>You can switch the row of the chart to column of the chart and vice versa.</br></td></tr>
    <tr><td>Select Data</br></td><td>You can modify the data source of Chart.</br></td></tr>
    <tr><td>Chart Type</br></td><td>You can change the type of the chart using Chart Type dialog.</br></td></tr>
    <tr><td>Height and Width</br></td><td>You can change the height and width of the chart.</br></td></tr>
    <tr><td>Chart Themes</br></td><td>You can change the theme of the chart. The available themes are saffron, lemon and azure in dark, light themes.</br></td></tr>
</table>

The following code example describes the above behavior.
{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, showHeader: true }],                               
        }],
        allowCharting: true,
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    if (!this.isImport) {
        this.XLChart.createChart("D1:E6", { type: "column", enable3D: false, marker: false, top: 40, left: 260, width: 340, height: 250 });
        this.performSelection("E1");
        this.XLChart.createChart("E1:F6", { type: "stackingcolumn", enable3D: false, marker: { visible: false }, top: 40, left: 620, width: 340, height: 250 });                     
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img2.png)

## Conditional Formatting

Conditional formatting helps you to apply formats to a cell or range with certain color based on the cells values. You can use [`allowConditionalFormats`](http://help.syncfusion.com/api/js/ejspreadsheet#members:allowconditionalformats "allowConditionalFormats") property to enable/disable Conditional formats.

### Condition definition

You can define conditions such as greater than, less than, between, equal to, text contains and date occurring for selected cells and defining value for condition. It highlights the specified cell. 
You can do this by one of the following ways,

* Using "Conditional Formatting" option in Conditional Formatting button of HOME Tab in ribbon to open the conditional formatting dialog.
* Using [`setCFRule`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlcformat-setcfrule "setCFRule") method to define the condition.

The following code example describes the above behavior.
{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
`   $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData}],                               
        }],
        allowConditionalFormats: true,
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    var xlCFormat = this.XLCFormat;
    if (!this.isImport) {
        xlCFormat.setCFRule({ "action": "greaterthan", "inputs": ["10"], "color": "redft", "range": "G2:G11" });
        xlCFormat.setCFRule({ "action": "lessthan", "inputs": ["20"], "color": "yellowft", "range": "E1:E11" });
        xlCFormat.setCFRule({ "action": "between", "inputs": ["300", "600"], "color": "greenft", "range": "F2:F11" });
        xlCFormat.setCFRule({ "action": "equalto", "inputs": ["20"], "color": "redf", "range": "D2:D11" });
        xlCFormat.setCFRule({ "action": "textcontains", "inputs": ["loafers"], "color": "redt", "range": "A1:A11" });
        xlCFormat.setCFRule({ "action": "dateoccur", "inputs": ["02/04/2014"], "color": "redft", "range": "B1:B11" });
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img3.png)

### Clear rules

You can clear the defined rules by using one of the following ways,

* Using "Clear Rules" option in Conditional Formatting button of HOME Tab in ribbon to clear the rule.
* Using [`clearCF`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlcformat-clearcf "clearCF") method to clear the defined rules.

The following code example describes the above behavior.
{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData}],                               
        }],
        allowConditionalFormats: true,
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    var xlCFormat = this.XLCFormat;
    if (!this.isImport) {
        xlCFormat.setCFRule({ "action": "greaterthan", "inputs": ["10"], "color": "redft", "range": "G2:G11" });
        xlCFormat.setCFRule({ "action": "lessthan", "inputs": ["20"], "color": "yellowft", "range": "E1:E11" });
        xlCFormat.setCFRule({ "action": "between", "inputs": ["300", "600"], "color": "greenft", "range": "F2:F11" });
        xlCFormat.clearCF(true, "G2:G11");
        xlCFormat.clearCF(true, "F2:F11");
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img4.png)

## Filtering

Filtering allows you to view specific rows in Spreadsheet, while hiding the other rows. When a filter is added to the header row, a drop-down menu appears in each cell of the header row. You can use [`allowFiltering`](http://help.syncfusion.com/api/js/ejspreadsheet#members:allowfiltering "allowFiltering") property to enable/disable filtering. 

You can apply filtering by one of the following ways,

* Using "Filter" option in Sort & Filter button under Editing group of HOME Tab in ribbon.
* Using "Filter" button under Sort and Filter group of DATA Tab in ribbon.

You have following options in Filtering.

* Filter by Value.
* Filter by Color.
* Clear Filter.

### Filter by Value

You can perform filtering by using number, string. The filtered rows are only visible in the Spreadsheet. All the other rows within the filtered range were hidden.

You can do this by one of the following ways,

* Using dropdown button in filter header to open the filter dialog.
* Using context menu to select "Filter by Selected Cell's Value" option in Filter. 
* Using [`filterByActiveCell`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlfilter-filterbyactivecell "filterByActiveCell") method.

The following code example describes the above behavior.
{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, showHeader: true }],
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    var xlFilter = this.XLFilter;
    if (!this.isImport) {
        this.performSelection("E2");
        xlFilter.filterByActiveCell();
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img5.png)

### Filter by Color

You can perform filtering by the selected cell color or font color. The filtered rows are only visible in the Spreadsheet. You can do this by clicking "Filter by Color" option in filter dialog to select filter by cell color or font color.

N> This option is only available if the selected range of cells having any color.

### Clear Filter

You can clear the filtering to show all the filtered rows in the spreadsheet within the filtered range.

You can do this by one of the following ways,

* Using "Clear Filter" option in the filter dialog.
* Using context menu to select "Clear Filter" option in Filter.
* Using "Clear Filter" option in "Sort & Filter" button under Editing group of HOME Tab in ribbon.
* Using "Clear Filter" option under Sort and Filter group of DATA Tab in ribbon.
* Using [`clearFilter`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlfilter-clearfilter "clearFilter") method to perform clear filtering.

The following code example describes the above behavior.
{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, showHeader: true }],                               
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    var xlFilter = this.XLFilter;
    if (!this.isImport) {
        this.performSelection("E2");
        xlFilter.filterByActiveCell();
        xlFilter.clearFilter();
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img6.png)

## Picture

You can insert a picture by selecting the "Pictures" button under Illustrations group of INSERT Tab in ribbon.

### Picture Customization

You can perform the following customizations for picture. These are available in DESIGN Tab which is enabled while clicking the picture element.

<table>
    <colgroup><col width="150px" /></colgroup>
    <tr><th>Feature</br></th><th>Description</br></th></tr>
    <tr><td>Change Picture</br></td><td>You can change the picture with existing picture.</br></td></tr>
    <tr><td>Reset Picture</br></td><td>You can reset the changes done in the picture such as border changes, height and width changes.</br></td></tr>
    <tr><td>Picture Border</br></td><td>You can add border to the picture. You have Border Color, Border Type and Border weight options to draw a border.</br></td></tr>
    <tr><td>Height and Width</br></td><td>You can change the height and width of the picture.</br></td></tr>
</table>

## Pivot Table

Pivot table is a program tool that allows you to reorganize and summarize selected columns and rows of data to obtain a desired report. You can use [`enablePivotTable`](http://help.syncfusion.com/api/js/ejspreadsheet#members:enablepivottable "enablePivotTable") property to enable/disable pivot table operations. 

You can do this by one of the following ways,

* Using "Pivot Table" option under Tables group of INSERT Tab in ribbon.
* Using [`createPivotTable`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlpivot-createpivottable "createPivotTable") method to create pivot table
* Using [`deletePivotTable`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlpivot-deletepivottable "deletePivotTable") method to remove the pivot table.

The following code example describes the above behavior.
{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.pivot" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.pivot, showHeader: true }],                               
        }],
        enablePivotTable: true,
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    if (!this.isImport) {
        var settings = {
            rows: [{fieldName: "Country"}, { fieldName: "State"}],
            columns: [{fieldName: "Product"}],
            values: [{fieldName: "Amount"},{fieldName: "Quantity"}],
            filters: [{fieldName: "Date"}]
        };
        this.XLPivot.createPivotTable("Sheet1!$A$1:$F$25", null, null, settings); 
        //this.XLPivot.deletePivotTable("name");
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img7.png)

## Sorting

Sorting helps you to arrange the data to particular order in a selected range of cells. You can use [`allowSorting`](http://help.syncfusion.com/api/js/ejspreadsheet#members:allowsorting "allowSorting") property to enable/disable sorting. 

You have following options in sorting.

* Sort by Ascending or Descending.
* Sort by Color.

### Sort by Ascending and Descending

You can perform number sorting by ascending or descending and string sorting by A to Z or Z to A to arrange the data. 

You can do this by one of the following ways,

* By choosing "Sort A to Z" or "Sort Z to A" in Sort & Filter button under Editing group of HOME Tab in ribbon. 
* Using "Sort A to Z" or "Sort Z to A" button in Sort & Filter group of DATA Tab in ribbon.
* Using context menu to select "Sort A to Z" or "Sort Z to A" for strings and option in Sort.
* Using "Sort A to Z" or "Sort Z to A" for strings an "Sort Smallest to Largest" or "Sort Largest to Smallest" for numbers in filter dialog.
* Using [`sortByRange`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlsort-sortbyrange "sortByRange") method.

The following code example describes the above behavior.
{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, showHeader: true }],                               
        }],
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    var xlSort = this.XLSort, xlFormat = this.XLFormat;
    if (!this.isImport) {
        xlSort.sortByRange("A2:A10", "A", "ascending");
        xlSort.sortByRange("E2:E10", "E", "descending");     
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img8.png)

### Sort by Color

You can perform sort by color to arrange the data based on the selected cell's background color or font color. This option is only available if the selected range of cells having any color.

You can do this by one of the following ways,

* Using "Sort By Color" option in filter dialog to perform sorting by cell color or font color.
* Using context menu to select "Put Selected Cell Color To The Top" or "Put Selected Font Color To The Top" in Sort option.

## Table

A table is a data structure that organizes information into rows and columns. You can use [`allowFormatAsTable`](http://help.syncfusion.com/api/js/ejspreadsheet#members:allowformatastable "allowFormatAsTable") property enable/disable table operations. 

You can do this by one of the following ways,

* Using "Format As Table" under Styles group of HOME Tab in ribbon.
* Using Table option under Tables group of INSERT Tab in ribbon.
* Using [`createTable`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlformat-createtable "createTable") method to insert a table and [`removeTable`](http://help.syncfusion.com/api/js/ejspreadsheet#methods:xlformat-removetable "removeTable") to delete a table.

### Table Customization

You can perform the following customizations for table. These are available in DESIGN Tab which is enabled while clicking the table.

<table>
    <colgroup><col width="150px" /></colgroup>
    <tr><th>Feature</br></th><th>Description</br></th></tr>
    <tr><td>Resize Table</br></td><td>You can resize the table only to increase row count.</br></td></tr>
    <tr><td>Convert to Range</br></td><td>You can remove the table using this option.</br></td></tr>
    <tr><td>First Column</br></td><td>You can highlight the first column of the table.</br></td></tr>
    <tr><td>Last Column</br></td><td>You can highlight the last column of the table.</br></td></tr>
    <tr><td>Total Row</br></td><td>You can insert a new row in the bottom of the table to display the total value of the last column. You can toggle this by using checkbox.</br></td></tr>
    <tr><td>Filter Button</br></td><td>You can able to hide or unhide the filter icons in the filter header of a table.</br></td></tr>
</table>

The following code example describes the above behavior.
{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.bill" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.bill, showHeader: true }],                               
        }],
        allowFormatAsTable: true,
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    var i, format = [], formatObj = [],xlFormat = this.XLFormat, formatName = ["TableStyleLight8", "TableStyleLight10"];
    if (!this.isImport) {
        for (i = 0; i < formatName.length; i++)
	        formatObj[i] = { "header": true, "name": formatName[i].substr(10), "formatName": formatName[i] };
        xlFormat.createTable(formatObj[0], "A1:B4");
        xlFormat.createTable(formatObj[1], "D1:E4");
    }
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data-Presentation_images/Data-Presentation_img9.png)